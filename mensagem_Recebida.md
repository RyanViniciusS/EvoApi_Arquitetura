#Ponto Incial :  src\api\integrations\channel\whatsapp\whatsapp.baileys.service.ts  →
eventHandler → 

recebe eventos emitidos pelo Baileys dento da funcao eventHandler
```javascript      
if (events['messages.upsert']) {
const payload = events['messages.upsert'];
console.log(payload, "dadosbayles")

// this.messageProcessor.processMessage(payload, settings);
 await this.messageHandle['messages.upsert'](payload, settings);
```
→
depois chama o messageHandle → 

```javascript
await this.messageHandle['messages.upsert'](payload, settings);
}
```
→ private readonly messageHandle → 'messages.upsert' → valida tudo  e depois criar a message no banco de dados →

```javascript
const msg = await this.prismaRepository.message.create({ data: messageData });
```

