# Sistema Inteligente de Análise de Ocupação de Estacionamentos Utilizando Aprendizado de Máquina

Projeto Final da disciplina de **Aprendizado de Máquina**.

## Descrição

Este projeto apresenta um sistema inteligente para análise automática da ocupação de estacionamentos utilizando técnicas de Visão Computacional e Aprendizado de Máquina.

O sistema utiliza o modelo **YOLOv8x** para detectar veículos em imagens de estacionamentos e, a partir das detecções, calcula indicadores de ocupação e gera automaticamente um dashboard executivo contendo estatísticas e visualizações dos resultados.

---

## Funcionalidades

- Detecção automática de veículos utilizando YOLOv8x;
- Filtragem das classes de interesse (carros, motocicletas, ônibus e caminhões);
- Cálculo do número de veículos detectados;
- Estimativa da taxa de ocupação do estacionamento;
- Geração de mapa de calor (Kernel Density Estimation - KDE);
- Dashboard executivo com indicadores e gráficos.

---

## Tecnologias Utilizadas

- Python 3
- Ultralytics YOLOv8
- OpenCV
- NumPy
- SciPy
- Matplotlib

---

## Estrutura do Projeto

```
Projeto/
│
├── ProjetoFinal.ipynb
├── README.md
├── requirements.txt
├── relatorio.pdf
│
├── imagens/
│   └── patio1.jpg
│
├── resultados/
│   └── dashboard.png
│
└── modelos/
```

---

## Instalação

Clone o repositório:

```bash
git clone https://github.com/SEU_USUARIO/NOME_DO_REPOSITORIO.git
```

Entre na pasta do projeto:

```bash
cd NOME_DO_REPOSITORIO
```

Instale as dependências:

```bash
pip install -r requirements.txt
```

Ou instale manualmente:

```bash
pip install ultralytics opencv-python matplotlib numpy scipy
```

---

## Como Executar

1. Abra o notebook `ProjetoFinal.ipynb` no Google Colab ou Jupyter Notebook.

2. Execute todas as células na ordem.

3. O sistema irá:

- carregar a imagem do estacionamento;
- executar a detecção utilizando YOLOv8x;
- calcular os indicadores;
- gerar o mapa de calor;
- produzir o dashboard final.

O dashboard será salvo automaticamente na pasta:

```
resultados/dashboard.png
```

---

## Metodologia

O fluxo do sistema é apresentado abaixo:

```
Imagem do estacionamento
            │
            ▼
      YOLOv8x (Detecção)
            │
            ▼
Filtragem das classes de veículos
            │
            ▼
Extração das informações
            │
            ▼
 Cálculo da taxa de ocupação
            │
            ▼
 Geração do Heatmap (KDE)
            │
            ▼
 Dashboard Executivo
```

---

## Estimativa da Ocupação

O número total de vagas do estacionamento é previamente conhecido (etapa de calibração).

A taxa de ocupação é calculada por:

\[
\text{Ocupação}=
\frac{\text{Número de veículos detectados}}
{\text{Número total de vagas}}
\times100
\]

---

## Resultados

O sistema produz automaticamente:

- imagem com os veículos detectados;
- mapa de calor da distribuição dos veículos;
- gráfico de ocupação;
- dashboard executivo contendo:

  - número de veículos;
  - taxa de ocupação;
  - confiança média das detecções;
  - tempo de processamento.

---

## Trabalhos Futuros

Como possíveis melhorias, destacam-se:

- detecção automática das vagas do estacionamento;
- processamento em tempo real utilizando vídeo;
- integração com câmeras IP;
- armazenamento histórico das ocupações;
- interface web para monitoramento remoto.

---

## Autor

**Pedro Nunes de Oliveira Pessanha**

Engenharia Matemática

Universidade Federal do Rio de Janeiro (UFRJ)

---

## Licença

Este projeto foi desenvolvido exclusivamente para fins acadêmicos na disciplina de Aprendizado de Máquina.
