# Crawler SBC SOL

Este é um projeto de um crawler desenvolvido para baixar artigos da **Sociedade Brasileira de Computação (SBC)**, especificamente da biblioteca **SOL (SBC OpenLib)**. A ferramenta é capaz de extrair todos os artigos em formato PDF de um determinado evento.

---

## 📜 Descrição

O `Crawler_SBC_SOL` é um script em Python que automatiza o download de artigos de eventos da SBC. Ele navega pela página do evento, encontra todos os links de artigos disponíveis e os baixa, organizando-os em uma pasta com a sigla do evento.

---

## ✨ Funcionalidades

- Extrai a sigla do evento a partir da URL.
- Cria uma pasta com a sigla do evento para organizar os artigos baixados.
- Busca todos os links de artigos na página principal do evento.
- Realiza o download dos artigos em formato PDF.
- Renomeia os arquivos de forma organizada.
- Utiliza o Google Drive para salvar os arquivos.

---

## ⚙️ Requisitos

Para executar o script, é necessário ter as seguintes bibliotecas Python instaladas:

- **tqdm:** Para a barra de progresso.
- **requests:** Para realizar as requisições HTTP.
- **beautifulsoup4:** Para fazer o parsing do HTML.
- **google-colab:** Para integração com o Google Colab e Google Drive.

Você pode instalar a `tqdm` com o seguinte comando:
```bash
pip install tqdm
````

-----

## 🚀 Como Usar

1.  **Montar o Google Drive:** O script precisa de acesso ao seu Google Drive para salvar os artigos. Execute a célula de código correspondente para montar o seu drive.
2.  **Configurar o Caminho Base:** A variável `BASE_PATH` define onde os artigos serão salvos. O padrão é a raiz do seu Google Drive (`/content/drive/MyDrive/`).
3.  **Definir a URL do Evento:** Na seção "Iniciar Execução", substitua a URL na variável `proceedings_url` pela URL do evento da SBC que você deseja baixar.
4.  **Executar o Script:** Execute todas as células do notebook para iniciar o processo de download. Os artigos serão salvos na pasta criada com a sigla do evento dentro do caminho base que você definiu.

-----

## 🔧 Configuração

### Caminho de Saída

Você pode alterar o local onde os artigos serão salvos modificando a variável `BASE_PATH`:

```python
BASE_PATH = "/content/drive/MyDrive/sua_pasta_preferida/"
```

### URL do Evento

Para baixar artigos de um evento diferente, altere a variável `proceedings_url`:

```python
proceedings_url = "[https://sol.sbc.org.br/index.php/outro_evento](https://sol.sbc.org.br/index.php/outro_evento)"
```

