![](https://github.com/juapgaua/ProtejAI/blob/main/protejai.png)

# ProtejAI
Este código implementa um chatbot que utiliza o modelo Gemini Pro do Google AI para analisar a conformidade de uma política de privacidade com a Lei Geral de Proteção de Dados (LGPD). O usuário pode fornecer a política de privacidade como texto ou como um arquivo PDF. O chatbot então avalia vários aspectos da política e fornece uma análise concisa e objetiva da conformidade com a LGPD.

# Dependências:

  google-generativeai: Biblioteca do Google AI para interagir com modelos generativos.
  
  PyPDF2: Biblioteca para ler e extrair texto de arquivos PDF.
  
  textwrap: Módulo para formatação de texto.
  
  IPython.display: Módulo para exibir saídas formatadas no Jupyter Notebook.
  
  google.colab: Módulo para acessar dados do usuário no Google Colab (opcional).

# Configuração

## Instalação das Dependências:
!pip install -q -U google-generativeai PyPDF2

## Configuração da API:

Google Colab: O código tenta obter a chave da API do Google AI a partir dos dados do usuário no Google Colab. A chave da API deve ser armazenada na variável SECRET_KEY.

Outros Ambientes: A chave da API deve ser definida manualmente na variável api_key.

Inicialização do Modelo Gemini Pro: model = genai.GenerativeModel('gemini-pro')

Funções:

to_markdown(text): Formata o texto de entrada como Markdown, adicionando quebras de linha após os pontos e recuo.

extract_text_from_pdf(file_path): Extrai o texto de um arquivo PDF.

evaluate_aspect(aspect, policy_text): Avalia um aspecto específico da política de privacidade em relação à conformidade com a LGPD. Esta função usa o modelo Gemini Pro para gerar uma análise concisa e objetiva.

## Fluxo do Chatbot:

Inicialização: O chatbot é iniciado e uma mensagem de boas-vindas é exibida.

Entrada da Política de Privacidade: O usuário escolhe entre digitar a política de privacidade como texto ou fornecer o caminho para um arquivo PDF.

Extração de Texto: Se um arquivo PDF for fornecido, o texto é extraído usando a função extract_text_from_pdf.

Avaliação dos Aspectos: O chatbot avalia os seguintes aspectos da política de privacidade:

Finalidade da coleta de dados

Base legal para o tratamento de dados

Direitos dos titulares dos dados

## Medidas de segurança

Transferência internacional de dados

## Exibição da Análise: 

Para cada aspecto, o chatbot exibe o aspecto sendo avaliado e a análise gerada pelo modelo Gemini Pro.

## Observações

Este código demonstra um exemplo básico de como usar o Gemini Pro para analisar a conformidade com a LGPD. Ele pode ser estendido para incluir mais aspectos e fornecer análises mais detalhadas.
A precisão da análise depende da qualidade da política de privacidade fornecida e da capacidade do modelo Gemini Pro em entender e interpretar a LGPD.
É importante lembrar que este chatbot é apenas uma ferramenta de apoio e não substitui a consulta a um profissional jurídico especializado em LGPD.
