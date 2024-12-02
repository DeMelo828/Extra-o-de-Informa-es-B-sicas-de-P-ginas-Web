# Analisador de Páginas Web (Bash)

Este script Bash permite extrair informações básicas de uma página web, como o título, servidor web, linguagem de programação, URLs, formulários e inputs. Ele faz isso de maneira simples e rápida, utilizando comandos como `curl`, `grep` e `awk`.

## Funcionalidades

- **Título do site**: Extrai o conteúdo da tag `<title>` da página.
- **Servidor web**: Exibe o tipo de servidor (ex: Apache, Nginx) presente nos cabeçalhos HTTP.
- **Linguagem de programação**: Mostra a linguagem ou framework utilizado pela página (se disponível no cabeçalho `X-Powered-By`).
- **URLs**: Lista todas as URLs encontradas nos atributos `href` das tags `<a>`.
- **Formulários e Inputs de texto**: Exibe as ações dos formulários (`action`) e os campos de entrada (`<input>`).

## Requisitos

- Bash (geralmente disponível por padrão em sistemas Unix-like)
- Curl (para realizar requisições HTTP)

## Como Usar

1. Clone ou baixe o script para seu diretório local.
2. Abra o terminal e navegue até o diretório onde o script está localizado.
3. Torne o script executável (se necessário):

   ```bash
   chmod +x script.sh
## Execute o script passando a URL do site que deseja analisar:

```bash
./script.sh <URL>
./script.sh https://example.com
```

## Exemplo de Saída
```bash
Título do site: Example Domain
Servidor web: nginx
Linguagem de programação: PHP
Todas as URLs do site:
https://example.com
https://example.com/about
...

Formulários e inputs de texto:
action="/submit"
<input type="text" name="username" />
<input type="password" name="password" />
