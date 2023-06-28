# Gerador de Tabela de Hash

Este projeto contém um script Python simples para gerar uma tabela de hash de todos os arquivos em um diretório fornecido, salvando as informações em um arquivo Excel (.xlsx).

## Características

1. Calcula o hash SHA-256 de cada arquivo no diretório fornecido.
2. Gera uma planilha Excel com os seguintes dados para cada arquivo:
   - Caminho do arquivo
   - Nome do arquivo
   - Tamanho do arquivo (em bytes)
   - Hash SHA-256 do arquivo

## Dependências

Este script Python depende dos seguintes módulos:

- `os`
- `hashlib`
- `openpyxl`

Certifique-se de que todos os módulos necessários estejam instalados antes de executar o script. Se algum deles não estiver instalado, você pode usar o seguinte comando para instalá-los:

```
pip install -r requirements.txt
```

## Como usar

1. Abra o terminal (ou prompt de comando) no local onde o arquivo Python está localizado.
2. Execute o seguinte comando:

```
python main.py
```

3. Será solicitado que você digite o caminho do diretório que deseja processar. Insira o caminho e pressione Enter.

## Saída

O script irá gerar um arquivo Excel (.xlsx) com a tabela de hash dos arquivos no diretório fornecido. O nome do arquivo será "(Hash) nome_do_diretorio.xlsx".

## Notas

- O script ignora o arquivo "Thumbs.db".
- A tabela de hash inclui o caminho do arquivo, o nome do arquivo, o tamanho do arquivo em bytes e o hash SHA-256 do arquivo.
- A função `criar_tabela_hash` percorre todos os arquivos na árvore de diretórios do diretório fornecido, calcula o hash SHA-256 de cada arquivo, obtém o tamanho do arquivo em bytes e adiciona essas informações à tabela de hash.
- A função `calcular_hash_arquivo` é usada para calcular o hash SHA-256 de um arquivo.