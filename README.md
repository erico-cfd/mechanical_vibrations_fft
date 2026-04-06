# Análise de Vibrações Mecânicas com FFT

## Descrição
Este repositório contém um Jupyter Notebook (`mechanical_vibrations_fft.ipynb`) dedicado à modelagem e análise de sistemas mecânicos de 1 Grau de Liberdade (1 GDL). O código realiza a simulação numérica da resposta do sistema no domínio do tempo e aplica a Transformada Rápida de Fourier (FFT) para extrair o comportamento do sistema no domínio da frequência.

## Contexto Matemático
O script resolve numericamente a equação diferencial ordinária clássica que rege um sistema massa-mola-amortecedor de 1 GDL:

$$m\ddot{x} + c\dot{x} + kx = F(t)$$

Onde:
* $m$ é a massa.
* $c$ é o coeficiente de amortecimento.
* $k$ é a rigidez da mola.
* $F(t)$ é a força de excitação no tempo.

Após a obtenção da resposta temporal, o sinal é convertido para o domínio da frequência utilizando a Transformada de Fourier discreta, permitindo identificar as frequências naturais e picos de amplitude do sistema.

## Principais Funcionalidades
* **Integração Numérica:** Resolução da EDO do sistema vibratório utilizando o módulo `scipy.integrate.odeint`.
* **Análise no Tempo:** Obtenção e visualização gráfica da resposta transitória e em regime permanente.
* **Análise em Frequência (FFT):** Aplicação do módulo `numpy.fft` para transformar a série temporal de velocidades/deslocamentos em espectro de frequências.
* **Identificação de Picos:** Visualização semilogarítmica do espectro para extração automática das frequências dominantes da vibração.

## Tecnologias e Pré-requisitos
O código foi desenvolvido em Python. Para executá-lo corretamente, é necessário ter as seguintes bibliotecas instaladas:
* `numpy` (Para operações matriciais e cálculo da FFT)
* `scipy` (Para a integração numérica de equações diferenciais)
* `matplotlib` (Para a plotagem dos gráficos de tempo e frequência)

Pode instalar as dependências através do seu terminal:

```bash
pip install numpy scipy matplotlib
