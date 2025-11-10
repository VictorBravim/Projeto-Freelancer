# Freelancer Dashboard

![{31A27E95-C9A9-49B6-B752-85F49144468B} 1](https://github.com/user-attachments/assets/0418484b-6b54-4162-bf73-d3226e5d88f3)

## <code>Introdução</code>

Freelancer Dashboard é uma aplicação web desenvolvida com Next.js, focada em ajudar freelancers a gerenciar seus projetos, organização financeira e metas. A dashboard possui quatro páginas principais: controle financeiro, metas, projetos e login.

## <code>Pré-requisitos</code>

- Node.js
- Firebase
- ReactIcons
- npm
 
## <code>Configuração</code>

1. Clone o repositório:

```
git clone https://github.com/VictorBravim/Dashboard-Freelancer/edit/main/README.md
```

2. Navegue até o diretório do projeto:

```
cd DashboardFreelancer
```

3. Instale as dependências:

```
npm install
```

4. Execute o servidor de desenvolvimento:

```
npm run dev
```

## <code>Firebase</code>

Para integrar o Firebase ao projeto, siga os seguintes passos:

1. Crie um projeto no Firebase Console.

2. Adicione um novo aplicativo web e copie as chaves de configuração fornecidas.

3. No diretório do projeto, crie um arquivo .env.local e cole as chaves do Firebase:

```
const firebaseConfig = {
    apiKey: "Your apiKey",
    authDomain: "Your authDomain",
    projectId: "Your projectId",
    storageBucket: "Your storageBucket",
    messagingSenderId: "Your messagingSenderId",
    appId: "Your appId"
};
```

## <code>Segurança Firebase</code>

Para proteger o banco de dados, adicione as seguintes regras de segurança no Firestore:

```
rules_version = '2';
service cloud.firestore {
 match /databases/{database}/documents {
    match /{document=**} {
      allow read, write: if true;
    }
  }
}
```

## <code>Estrutura</code>

- components/: Contém componentes React reutilizáveis na aplicação.
- pages/: Páginas principais do Next.js representando diferentes rotas.
- /financeiro: Página de controle financeiro com tabela de gastos, receitas e gestão de cartões.
- /metas: Página para organização e acompanhamento de metas.
- /projetos: Página de controle de projetos com informações sobre preço, status e tipo de projeto.
- /login: Página de autenticação para acesso ao sistema.
- public/: Arquivos estáticos como imagens e ícones.
- styles/: Arquivos de estilo global e componentes estilizados com Tailwind CSS.

## <code>Licença</code>

- Este projeto está licenciado sob a [Licença MIT](LICENSE).
