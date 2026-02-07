# EvoApi_Arquitetura

eventHandler → recebe eventos emitidos pelo Baileys 
```javascript      
if (events['messages.upsert']) {
              const payload = events['messages.upsert']; 
```

depois chama o messageHandle → 
```
 if (events['messages.upsert']) {
const payload = events['messages.upsert'];
console.log(payload, "dadosbayles")

// this.messageProcessor.processMessage(payload, settings);
await this.messageHandle['messages.upsert'](payload, settings);
}
```

sendMessage → envia eventos para o whatsApp
```javascript      
  private async sendMessage(
    sender: string,
    message: any,
    mentions: any,
    linkPreview: any,
    quoted: any,
    messageId?: string,
    ephemeralExpiration?: number,
    contextInfo?: any,
    // participants?: GroupParticipant[],
  ) {
    sender = sender.toLowerCase(); 
```

