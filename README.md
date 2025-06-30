# MindhunterBR
Investigação de padrões de crimes violentos no Brasil usando dados públicos do SIM/DATASUS. Inspirado em Mindhunter, o projeto busca identificar possíveis serial killers com base em padrões temporais, geográficos e comportamentais.

---

# 🔎 Análise de Padrões Criminais no Brasil (SIM/DATASUS)

Este projeto investiga **possíveis padrões de crimes violentos no Brasil** a partir dos dados do SIM (Sistema de Informações sobre Mortalidade), fornecidos pelo DATASUS.

Inspirado na abordagem da série **Mindhunter**, o estudo parte da hipótese de que **as bases policiais brasileiras têm baixa integração**, o que pode dificultar a identificação de **crimes em série**.

---

## 🎯 Objetivos

- Identificar padrões temporais, geográficos e sociais recorrentes entre vítimas de homicídio.
- Mapear indícios de atuação serial (modus operandi repetido, perfil das vítimas, local das ocorrências).
- Explorar a utilidade de dados públicos de saúde para análises criminais.

---

## 🧠 Hipóteses Investigadas

### 1. Padrões Temporais
- Vítimas morrendo em datas próximas ou cíclicas (ex: a cada 30 dias).
- Óbitos ocorrendo sempre em horários similares (ex: madrugada).

### 2. Padrões Geográficos
- Concentração em bairros ou municípios próximos.
- Expansão geográfica com padrão (ex: círculos concêntricos).

### 3. Perfil das Vítimas
- Faixas etárias semelhantes (ex: jovens entre 18 e 25 anos).
- Mesma identidade de gênero, raça/cor, escolaridade ou ocupação.

### 4. Modo de Morte
- Códigos CID-10 repetidos indicando agressão (ex: Wxxx, X8xx, Y0xx).
- Mesmos métodos: estrangulamento, afogamento, arma branca, etc.

### 5. Local da Ocorrência
- Locais com padrões (ex: sempre via pública ou domicílios precários).
- Diferença entre município de residência e local da ocorrência.

### 6. Mortes “Limpas”
- Ausência de necropsia ou exames.
- Causa da morte genérica e repetida (“indeterminada”).
- Pouca investigação no histórico da vítima.

---

## 📊 Variáveis Utilizadas

| Coluna       | Descrição                                      | Relevância para Análise                          |
|--------------|------------------------------------------------|--------------------------------------------------|
| `DTOBITO`    | Data do óbito                                  | Permite detectar padrões temporais               |
| `HORAOBITO`  | Hora do óbito                                  | Pode indicar atuação em horários específicos     |
| `IDADE`      | Idade da vítima                                | Serial killers tendem a focar em faixas etárias  |
| `SEXO`       | Sexo da vítima                                 | Pode haver preferência por um gênero             |
| `RACACOR`    | Raça/cor da vítima                             | Indica possível viés racial                      |
| `ESC2010`    | Escolaridade da vítima                         | Associações com vulnerabilidade social           |
| `OCUP`       | Ocupação da vítima                             | Ex: alvos recorrentes como lavradores, entregadores |
| `CODMUNRES`  | Município de residência                        | Cruzamento com local do óbito                    |
| `CODMUNOCOR` | Município da ocorrência                        | Mapeamento geográfico dos crimes                 |
| `LOCOCOR`    | Local da ocorrência                            | Ajuda a entender o modus operandi                |
| `CAUSABAS`   | Causa da morte (CID-10)                        | Verifica repetição do tipo de morte              |

---

## 🛠️ Tecnologias e Ferramentas

- Python (Pandas, NumPy, Seaborn, Scikit-learn, Geopandas)
- Google Colab
- Dados do SIM/DATASUS (convertidos de `.dbc` para `.dbf`)

---

## 🚧 Status

Em desenvolvimento. Limpeza de dados realizada e dataframe montado. Análise exploratória apenas iniciada.

---

## 📌 Inspiração

> “Os dados não mentem. Mas é preciso saber onde procurar.”  
> – *Baseado na lógica investigativa de Mindhunter*

## 🧪 Como rodar este projeto localmente
### 1. Clone o repositório
```bash
git clone https://github.com/LunusMax/MindhunterBR.git
cd MindhunterBR
### 2. Instale todas as dependências de uma vez
pip install -r requirements.txt
### 3. Rode o notebook
Abra o arquivo dentro da pasta notebooks/ com Jupyter ou no Google Colab.
