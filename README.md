# GFCTech — Landing Page

Landing page responsiva para apresentação da plataforma de gestão de cursos e eventos da GFCTech.

O projeto apresenta os principais diferenciais da plataforma, números de uso, clientes, fluxo de criação de eventos, modelos de cobrança e um formulário de contato para consultoria.

## Recursos

- Layout responsivo para desktop, tablet e celular
- Formulário de geração de leads
- Validação dos campos obrigatórios
- Campo de telefone com código de país via `intl-tel-input`
- Verificação da soma apresentada no formulário
- Integração preparada para envio de dados por API
- Botões de contato e WhatsApp
- Estrutura totalmente estática

## Tecnologias

- HTML5
- CSS3
- JavaScript
- [intl-tel-input](https://github.com/jackocnr/intl-tel-input)
- Google Fonts

## Pré-requisitos

Não há dependências para instalar. O projeto pode ser executado por qualquer servidor HTTP estático.

Python 3 é necessário somente se você optar pelo servidor de exemplo abaixo.

## Executando localmente

Na pasta do projeto, execute:

```bash
python -m http.server 4173
```

Depois, acesse `http://127.0.0.1:4173` no navegador.

## Estrutura

```text
landing-page-css/
├── index.html
├── styles.css
├── script.js
├── logosteste/
└── assets/
```

## Configuração do formulário

O envio é realizado em `script.js` por uma requisição `POST` para:

```text
http://localhost:5269/api/email/send
```

A API deve aceitar um corpo JSON com os seguintes campos:

```json
{
  "toEmail": "cliente@exemplo.com",
  "subject": "Novo contato de evento",
  "message": "Dados do contato e do evento"
}
```

Para publicar o site, substitua o endereço local pela URL da API disponível no ambiente de produção.

## Personalização

- Alterações de conteúdo: `index.html`
- Cores, tipografia e layout: `styles.css`
- Comportamento do formulário: `script.js`
- Imagens e logotipos: `logosteste/`

## Licença

Este projeto está sob a licença MIT. Consulte o arquivo [LICENSE](LICENSE) para mais detalhes.
