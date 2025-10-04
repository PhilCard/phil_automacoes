# 🤖 Agent IA de Ligação – n8n Automation

Automação criada com **n8n** que combina **inteligência artificial e comunicação multicanal** para oferecer uma experiência completa de atendimento automatizado.  
O sistema entende mensagens de **texto, áudio e imagem**, e é capaz de **realizar ligações telefônicas automáticas** quando solicitado pelo usuário, permitindo uma conversa fluida com o **agent de IA** em tempo real.

---

## 🎯 Objetivo da Automação

Criar um **agente inteligente capaz de interagir com usuários em múltiplos formatos** (mensagens, voz e imagem) e **iniciar uma ligação automatizada** para continuar a conversa via telefone com inteligência artificial.

**Fluxo resumido:**
1. O usuário envia uma mensagem (texto, áudio ou imagem).  
2. A automação interpreta o conteúdo com ajuda da IA.  
3. Se o usuário solicitar uma ligação, o sistema automaticamente:
   - Gera o prompt da conversa para o modelo da OpenAI.  
   - Aciona o **Twilio** para realizar a ligação.  
   - Mantém a conversa com o **agent de IA** durante a chamada.  

---

## 🧩 Ferramentas e Tecnologias Utilizadas

- **[n8n](https://n8n.io/)** → Plataforma de automação principal, responsável pela orquestração dos fluxos  
- **[OpenAI API](https://platform.openai.com/)** → Inteligência artificial para compreensão de linguagem natural e respostas contextualizadas  
- **[Z-API](https://z-api.io/)** → Envio e recebimento de mensagens via WhatsApp  
- **[V-API](https://vapi.ai/)** → Integração avançada com sistemas de WhatsApp Business e gerenciamento de contatos  
- **[Twilio](https://www.twilio.com/)** → Realização de ligações e gerenciamento de chamadas de voz via API  

---

## ⚙️ Como Funciona o Fluxo (Visão Geral)

```text
Usuário envia mensagem → n8n recebe via Z-API → IA analisa conteúdo (OpenAI)
→ Caso solicite ligação → Twilio realiza chamada → IA responde em tempo real
```

### 🧠 Funcionamento da Automação

- Mensagens recebidas (**texto**, **áudio**, **imagem**) são interpretadas pela **IA**.  
- A decisão de fazer a ligação é **automatizada** de acordo com o contexto da conversa.  
- O **Twilio** faz a chamada e conecta o usuário a um fluxo controlado pela **IA**.  
- Todo o histórico pode ser registrado via **Airtable**, **Notion** ou outro banco, se configurado.

---

### 🚀 Possíveis Aplicações

- Atendimento automatizado em **clínicas**, **restaurantes**, **delivery** ou **e-commerce**  
- **Agendamentos automáticos por voz**  
- **Suporte ao cliente com IA híbrida** (texto + voz)  
- Ligações automáticas para **follow-ups**, **confirmação de agendamento** ou **pesquisas de satisfação**

---

### ⚠️ Observações Importantes

- As **credenciais de API** (OpenAI, Twilio, Z-API, V-API) **não são incluídas** no JSON exportado.  
- Ao importar o fluxo no **n8n**, **crie suas próprias credenciais seguras**.  
- É possível adicionar **camadas de autenticação** e **limites de uso** para ambiente de produção.

