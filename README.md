# Selfmap

Selfmap é um projeto para explorar o "mapa de si" por meio de uma aplicação web simples em Next.js. O objetivo é ter um repositório organizado para desenvolvimento, revisão e deploy, com foco em colaboração por branch, pull requests e CI.

## O que é este projeto

- É uma aplicação construída com **Next.js 16** e **TypeScript**.
- Tem uma estrutura de frontend leve para exibir o conteúdo do mapa pessoal.
- Serve como base para compartilhar e evoluir o projeto em equipe.
- Usa **GitHub Actions** para CI e validação automática.

## Estrutura do repositório

- `app/`
  - Contém a aplicação Next.js com as páginas e componentes principais.
  - `app/page.tsx` é a página principal.
  - `app/layout.tsx` define o layout e o HTML base.
  - `app/globals.css` traz o estilo global.

- `public/`
  - Imagens e ícones públicos usados pela aplicação.

- `.github/workflows/ci.yml`
  - Workflow de CI do GitHub Actions.
  - Executa `npm install`, `npm run lint` e `npm run build` em cada PR ou push para `main`.

- `package.json`
  - Define scripts e dependências do projeto.
  - Importante para rodar localmente, compilar e fazer lint.

- `tsconfig.json`
  - Configuração do TypeScript.

- `eslint.config.mjs`
  - Regras do ESLint para manter o código consistente.

- `next.config.ts`
  - Configuração do Next.js.

## Como rodar localmente

```bash
npm install
npm run dev
```

Depois, abra `http://localhost:3000` no navegador.

## Fluxo de colaboração

1. Crie uma branch a partir de `main`:
   ```bash
git checkout -b feature/nome-da-feature
```
2. Faça commits pequenos e claros.
3. Envie a branch para o GitHub:
   ```bash
git push -u origin feature/nome-da-feature
```
4. Abra um Pull Request para `main`.
5. Aguarde o workflow `CI` rodar e as revisões serem feitas.

## Proteção de branch e CI

- O repositório usa regras de proteção para `main`.
- O workflow `CI` deve ser usado como check obrigatório quando disponível.
- Isso garante que o código seja revisado e que o build/lint passe antes do merge.

## Sobre o mapa de si

O projeto se propõe a ser um espaço onde você organiza ideias e reflexões sobre si mesmo — um mapa pessoal em formato digital. A ideia é que o repositório cresça conforme o conteúdo e a interface evoluem, sempre com controle de versão e colaboração segura.
