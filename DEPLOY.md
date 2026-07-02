# CentraLux Ponto — Deploy no GitHub Pages

> ⚠️ **SEGURANÇA:** o token que você compartilhou no chat está **comprometido** (foi exposto em texto aberto).
> Revogue-o AGORA em: GitHub → Settings → Developer settings → Personal access tokens → Revoke.
> Gere um token novo com escopo `repo` e use-o apenas localmente — nunca cole tokens em chats, códigos ou commits.

## Passo a passo (Windows / PowerShell ou Git Bash)

Pasta local: `C:\Users\FS\Desktop\Github\CentraLux Ponto`

```bash
# 1. Entrar na pasta do projeto (com os arquivos do site já dentro)
cd "C:\Users\FS\Desktop\Github\CentraLux Ponto"

# 2. Iniciar o repositório
git init
git add .
git commit -m "CentraLux Ponto - sistema de controle de ponto e horas extras"

# 3. Criar o repositório no GitHub (crie 'centralux-ponto' pelo site github.com/new)
#    Depois conecte usando SEU_USUARIO e o TOKEN NOVO quando o Git pedir a senha:
git remote add origin https://github.com/SEU_USUARIO/centralux-ponto.git

# 4. Publicar na branch gh-pages
git branch -M gh-pages
git push -u origin gh-pages
```

Quando o Git pedir credenciais: usuário = seu usuário do GitHub, senha = o **token novo**.

## Ativar o GitHub Pages
1. No repositório: **Settings → Pages**
2. Source: **Deploy from a branch** → Branch: **gh-pages** → pasta **/ (root)** → Save
3. O site ficará em: `https://SEU_USUARIO.github.io/centralux-ponto/`

## Requisitos do arquivo
- O arquivo principal deve se chamar `index.html` na raiz da branch `gh-pages`.
  (Peça a exportação "HTML autônomo" aqui no chat — ele gera um único index.html pronto.)
- A planilha do Google Sheets precisa continuar com acesso "Qualquer pessoa com o link pode ver".

## Atualizações futuras
```bash
cd "C:\Users\FS\Desktop\Github\CentraLux Ponto"
git add .
git commit -m "atualizacao"
git push
```
