# DermoScan: Análise Inteligente de Lesões de Pele

DermoScan é um protótipo de aplicação que utiliza um modelo de Visão Computacional para classificar lesões de pele em diferentes categorias, incluindo melanoma, nevo melanocítico, entre outras. O objetivo é oferecer uma ferramenta de triagem preliminar, incentivando o usuário a procurar um dermatologista para um diagnóstico definitivo.

**Atenção:** Este projeto é uma prova de conceito e **não substitui um diagnóstico médico profissional**.

---

## 🚀 Funcionalidades

* **Upload de Imagem:** Permite que o usuário envie uma foto de uma lesão de pele.
* **Análise com IA:** A imagem é processada e analisada por um modelo de Rede Neural Convolucional (CNN).
* **Classificação de Risco:** A aplicação retorna uma classificação da lesão com uma probabilidade de confiança e um nível de risco sugerido (Baixo, Médio, Alto).
* **Histórico (Funcionalidade Futura):** Armazenamento do histórico de análises para acompanhamento.

---

## 🛠️ Como Executar (Backend/API)

Para executar o servidor da API localmente, siga estes passos.

1.  **Clone o repositório:**
    ```bash
    git clone https://github.com/seu-usuario/DermoScan.git
    cd DermoScan
    ```

2.  **Crie um ambiente virtual e instale as dependências:**
    ```bash
    # Crie o ambiente
    python -m venv venv

    # Ative o ambiente
    # No Windows:
    # venv\Scripts\activate
    # No Linux/macOS:
    source venv/bin/activate

    # Instale as bibliotecas
    pip install -r requirements.txt
    ```

3.  **Baixe o modelo treinado** (`.h5` ou `.keras`) e coloque-o na pasta `/models`.
    *(Nota: adicione aqui o link para download do seu modelo quando o tiver).*

4.  **Inicie o servidor da API:**
    ```bash
    cd src/api
    uvicorn main:app --reload
    ```
    A API estará disponível para testes em `http://127.0.0.1:8000/docs`.

---

## 📚 Dataset Utilizado

O modelo foi treinado utilizando o dataset **HAM10000 ("Human Against Machine with 10000 Training Images")**, que é um recurso público para pesquisa dermatológica.

* **Fonte:** [Harvard Dataverse](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/DBW86T)
* **Artigo de Referência:** Tschandl, P., Rosendahl, C., & Kittler, H. (2018). *The HAM10000 dataset*.

---