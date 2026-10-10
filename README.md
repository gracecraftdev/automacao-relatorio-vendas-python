# Automação de Relatório de Vendas com Python

Projeto de aprendizado em Python que automatiza a obtenção de uma planilha de vendas, calcula indicadores com **pandas** e prepara um e-mail de relatório utilizando **PyAutoGUI** e **Pyperclip**.

## Funcionalidades

- Acessar uma pasta do Google Drive por meio do navegador e executar cliques para baixar a planilha.
- Ler uma planilha Excel com `pandas`.
- Calcular o faturamento total (`Valor Final`) e a quantidade total vendida (`Quantidade`).
- Formatar os valores no padrão brasileiro.
- Preencher assunto e corpo de um e-mail no Gmail, preservando os acentos com `pyperclip`.
- Acionar o atalho de envio do e-mail.

## Tecnologias

Python, pandas, openpyxl, PyAutoGUI, Pyperclip e Jupyter Notebook.

## Como executar

1. Tenha Python instalado em um computador **Windows** e abra o projeto no Jupyter Notebook ou no VS Code com suporte a notebooks.
2. Instale as dependências:

   ```bash
   python -m pip install -r requirements.txt
   ```

3. No notebook, configure o link da pasta com a planilha, o caminho local do arquivo Excel e o e-mail do destinatário.
4. Confira se o arquivo possui as colunas `Valor Final` e `Quantidade`.
5. Execute as células em ordem e acompanhe a automação.

## Atenção antes de executar

- As coordenadas `pyautogui.click(x=..., y=...)` foram ajustadas para uma tela específica; **adapte-as à sua resolução**.
- A automação depende do foco, do layout do navegador e do tempo de carregamento das páginas.
- A última célula usa `Ctrl + Enter` no Gmail e **pode enviar o e-mail**. Para testar sem enviar, comente a última linha: `# pyautogui.hotkey('ctrl', 'enter')`.
- O caminho do arquivo e o endereço de destinatário presentes no notebook são **exemplos**, não valores prontos para produção.
- O notebook não inclui a planilha Excel; use uma planilha própria ou de teste. Não publique dados privados no repositório.
- Esta é uma automação de interface para fins de estudo, não uma integração oficial via API.

## Estrutura

```text
automacao-relatorio-vendas-python/
├── automacao_relatorio_vendas.ipynb
├── requirements.txt
├── .gitignore
└── README.md
```

## Contexto

Projeto prático para exercitar automação de processos, manipulação de planilhas Excel e geração de indicadores em Python.
