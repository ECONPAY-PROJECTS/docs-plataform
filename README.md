# EconPay API Documentation

Documentação oficial da API EconPay construída com Mintlify.

## 🚀 Desenvolvimento Local

### Pré-requisitos

- Node.js 18+ instalado
- npm ou yarn

### Instalação

1. Instale o Mintlify CLI globalmente:

```bash
npm install -g mint
```

2. Clone o repositório e navegue até a pasta de documentação:

```bash
cd docs-plataform
```

3. Inicie o servidor de desenvolvimento:

```bash
mint dev
```

4. Abra http://localhost:3000 no navegador

As mudanças serão refletidas automaticamente ao editar os arquivos.

## 📁 Estrutura do Projeto

```
docs-plataform/
├── docs.json                 # Configuração principal (navegação, cores, etc)
├── index.mdx                 # Página inicial
├── quickstart.mdx            # Guia de início rápido
├── authentication.mdx        # Documentação de autenticação
├── guides/                   # Guias gerais
│   ├── environments.mdx      # Ambientes (prod/sandbox)
│   ├── errors.mdx            # Códigos de erro
│   └── webhooks.mdx          # Guia de webhooks
├── api-reference/            # Referência da API
│   ├── auth/                 # Endpoints de autenticação
│   │   ├── login.mdx
│   │   └── profile.mdx
│   ├── payments/             # Endpoints de pagamentos
│   │   ├── create-payment.mdx
│   │   └── refund.mdx
│   ├── transactions/         # Endpoints de transações
│   │   ├── list.mdx
│   │   └── details.mdx
│   └── webhooks/             # Documentação de webhooks
│       └── overview.mdx
├── logo/                     # Logos (light/dark)
└── images/                   # Imagens e assets
```

## 🎨 Customização

### Cores

Edite as cores no `docs.json`:

```json
{
  "colors": {
    "primary": "#0066FF",
    "light": "#3399FF",
    "dark": "#0052CC"
  }
}
```

### Logo

Substitua os arquivos em `/logo/`:
- `light.svg` - Logo para tema claro
- `dark.svg` - Logo para tema escuro

### Navegação

Edite a estrutura de navegação em `docs.json` na seção `navigation`.

## 📝 Adicionando Conteúdo

### Nova Página

1. Crie um arquivo `.mdx` na pasta apropriada
2. Adicione o frontmatter:

```mdx
---
title: "Título da Página"
description: "Descrição breve"
---

## Conteúdo

Seu conteúdo aqui...
```

3. Adicione a página no `docs.json`:

```json
{
  "group": "Nome do Grupo",
  "pages": [
    "caminho/para/sua-pagina"
  ]
}
```

### Novo Endpoint da API

Use o template de endpoint:

```mdx
---
title: "POST /endpoint"
api: "POST https://api.econpay.com.br/endpoint"
auth: "bearer"
description: "Descrição do endpoint"
---

## Descrição

Descrição detalhada...

## Request Body

<ParamField body="campo" type="string" required>
  Descrição do campo
</ParamField>

## Response

<ResponseField name="campo" type="string">
  Descrição do campo de resposta
</ResponseField>

<RequestExample>
```bash cURL
curl --request POST \
  --url https://api.econpay.com.br/endpoint \
  --header 'Authorization: Bearer TOKEN'
```
</RequestExample>

<ResponseExample>
```json 200 - Success
{
  "success": true
}
```
</ResponseExample>
```

## 🚀 Deploy

### Deploy Automático

O Mintlify faz deploy automático quando você:

1. Faz push para a branch `main`
2. Tem o GitHub App do Mintlify instalado

### Configurar Deploy

1. Acesse https://dashboard.mintlify.com
2. Conecte seu repositório GitHub
3. Configure a branch de deploy (main)
4. O deploy será automático a cada push

### Domínio Customizado

Configure um domínio customizado no dashboard do Mintlify:
- Recomendado: `docs.econpay.com.br`

## 📚 Recursos

- [Documentação do Mintlify](https://mintlify.com/docs)
- [Componentes Disponíveis](https://mintlify.com/docs/components)
- [Exemplos de Documentação](https://mintlify.com/customers)

## 🐛 Troubleshooting

### Mintlify dev não inicia

```bash
mint update
```

### Página carrega como 404

Certifique-se de que:
- O arquivo existe na pasta correta
- O caminho está correto no `docs.json`
- Você está rodando `mint dev` na pasta com `docs.json`

### Mudanças não aparecem

- Salve o arquivo
- Aguarde alguns segundos
- Recarregue a página no navegador
- Se persistir, reinicie o `mint dev`

## 📞 Suporte

Para dúvidas sobre a documentação:
- Email: suporte@econpay.com.br
- Dashboard: https://app.econpay.com.br

## ✅ Funcionalidades Documentadas

- ✅ Autenticação (Login e Profile)
- ✅ Pagamentos (PIX, Cartão de Crédito, Débito, Boleto)
- ✅ Reembolsos/Estornos
- ✅ Listagem de Transações com filtros
- ✅ Detalhes de Transação
- ✅ Webhooks (payment.approved, payment.failed, payment.refunded)
- ✅ Guias de Ambientes (Produção/Sandbox)
- ✅ Códigos de Erro
- ✅ Exemplos em múltiplas linguagens (cURL, JavaScript, Python, PHP)
