# Barbearia Ananias

Site estático de pedidos de agendamento pelo WhatsApp, pronto para GitHub Pages.

## Publicar

1. Coloque `index.html`, `styles.css`, `app.js` e `.nojekyll` na raiz do repositório.
2. Abra **Settings → Pages**.
3. Em **Build and deployment**, escolha **Deploy from a branch**.
4. Selecione a branch **main**, pasta **/(root)**, e salve.

Não requer npm, servidor, banco, chaves nem compilação. Todos os arquivos usam caminhos relativos, compatíveis com endereços de projeto no GitHub Pages.

## Funcionamento

O cliente escolhe corte, dia e horário de preferência, informa nome e celular e revisa o pedido. O botão abre o WhatsApp com uma mensagem preenchida. O cliente precisa tocar em Enviar; só o barbeiro confirma o horário.

Não armazena agendamentos, não verifica disponibilidade real e não tem área administrativa. Nenhum dado é persistido pelo site. O código anterior com banco continua separado.

## Ajustes

- Telefone: `CONFIG.whatsapp` em `app.js`, além dos dois links de contato de `index.html`.
- Sugestões de horário: `CONFIG.firstHour`, `lastHour` e `interval` em `app.js`. A configuração inicial (07h–20h, a cada 30 minutos) é apenas uma grade de preferência e precisa ser conferida com a barbearia.
- Serviços e textos: `index.html`.
- Estilo: `styles.css`.

## Verificações

JavaScript validado com `node --check app.js`. Mensagens e dados do usuário são inseridos como texto e codificados na URL do WhatsApp.
