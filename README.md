Requisitos para persistência no Firebase Funcionar:

1. O campo comentário está com check de tamanho > 10 posições.

2. No firebase regras liberar escrita:
   rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /contacts/{docId} {
      allow create: if true;
    }
  }
}

3. No vercel as variáveis de ambiente devem estar exatamente assim:
<img width="417" height="753" alt="image" src="https://github.com/user-attachments/assets/5fadaa0d-f4f3-438d-a69d-6551bf55a134" />
