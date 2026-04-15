# Checklist de Equipamentos — Demax

App web para inspeção, guarda e transferência de equipamentos de limpeza.  
Funciona em qualquer browser (celular ou PC), sem instalação.

## Estrutura do repositório

```
index.html   → app completo (HTML + CSS + JS em um único arquivo)
vercel.json  → configuração de deploy no Vercel
```

## Deploy (primeira vez)

### 1. GitHub

1. Acesse [github.com](https://github.com) e crie uma conta (se ainda não tiver)
2. Clique em **New repository**
3. Nome sugerido: `demax-checklist`
4. Deixe **Public** (necessário para o Vercel gratuito)
5. Clique em **Create repository**
6. Na tela seguinte, clique em **uploading an existing file**
7. Arraste os três arquivos: `index.html`, `vercel.json`, `.gitignore`
8. Clique em **Commit changes**

### 2. Vercel

1. Acesse [vercel.com](https://vercel.com) e clique em **Sign up with GitHub**
2. Autorize o Vercel a acessar seus repositórios
3. Clique em **Add New Project**
4. Selecione o repositório `demax-checklist`
5. Não altere nenhuma configuração — clique em **Deploy**
6. Em ~30 segundos você recebe o link público

O link terá o formato: `demax-checklist.vercel.app`  
Você pode configurar um domínio personalizado nas configurações do projeto no Vercel.

## Atualizar o app no futuro

1. Edite o `index.html` localmente
2. No GitHub, abra o arquivo `index.html` e clique no ícone de lápis (editar)
3. Cole o conteúdo novo e clique em **Commit changes**
4. O Vercel detecta a mudança e publica automaticamente em ~30 segundos

## Primeiro uso após publicar

1. Abra o link do app
2. Toque em **Admin** (canto superior direito)
3. Senha: `Demax@2025`
4. Aba **Contratos** → cadastre cada contrato com código, nome e município
5. Aba **Colaboradores** → cadastre cada colaborador com nome, função e contrato padrão
6. Saia do Admin — o app está pronto para uso

## Senha admin

A senha padrão é `Demax@2025`.  
Para alterar, edite a linha abaixo no `index.html`:

```js
const ADMIN_PASS = 'Demax@2025';
```

Substitua pela senha desejada e faça o commit no GitHub.

## Armazenamento

Os dados ficam no `localStorage` do browser de cada dispositivo.  
Isso significa que cada celular tem seu próprio histórico — não há sincronização entre dispositivos nesta versão.

Para uma versão com banco de dados centralizado (todos os dispositivos vendo os mesmos registros), o app já está estruturado para essa migração.

## Equipamentos cobertos

1. Excentr 40-25 — Limpadora orbital 230V
2. Haste I-Wash 8.05 — Haste telescópica waterfed ~8 m
3. I-Suit — Sistema ergonômico waterfed backpack
4. DRYFT V1 S-Motion — Lavadora-secadora orbital cordless
5. Unger HydroPower Filter — Filtro DI água pura (nLite)
6. Varredeira Makita VS001GZ — Varredeira Brushless HEPA 40V XGT

Cada equipamento tem três tipos de inspeção: **Uso diário**, **Guarda** e **Transferência**.
