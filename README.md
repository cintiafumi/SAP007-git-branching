# Git Branching

Este repositório tem como objetivo exercitar o uso de _branches_ (ramos) no git.

## Fluxo de trabalho

Segue o link para um vídeo explicativo do GitHub:

[![What is GitHub?](https://img.youtube.com/vi/w3jLJU7DT5E/0.jpg)](https://youtu.be/w3jLJU7DT5E/?yt:cc=on&hl=pt_BR&cc_lang_pref=pt_BR)

### 1. Acesso ao repositório como colaborador(a)

Um dos mentores enviará um convite de colaboração para o repositório. Você receberá esse convite pelo seu e-mail cadastrado no GitHub.

### 2. Clone

Clone o repositório:

- opção SSH (caso você tenha configurado a chave SSH anteriormente):

```bash
git clone git@github.com:USERNAME/SAP007-git-branching.git
```

- **ou**, opção HTTPS:

```bash
git clone https://github.com/USERNAME/SAP007-git-branching.git
```

> Ⓘ onde `USERNAME` é o nome de usuário da conta que enviou o convite de colaboração.

Navegue até o diretório do repositório:

```bash
cd SAP007-git-branching
```

### 3. Branch

Crie uma _branch_ nova com um nome adequado ([dicas de nomenclatura](#dicas)):

```bash
git checkout -b feat/add-fulana-image
```

### 4. Install

Instale as dependências do projeto:

```bash
npm install
```

Rode o projeto:

```bash
npm start
```

### 5. Hacking

Altere a parte do código onde você quer que a funcionalidade seja implementada.

### 6. Commit

Realize o fluxo de _commit_.

Adicione o(s) arquivo(s) alterados da sua _branch_ para a área de preparação (_staging area_):

```bash
git add src/index.html
```

Adicione a mensagem de _commit_ ([dicas de mensagem](#dicas)):

```bash
git commit -m "feat: adicionada a imagem da estudante fulana"
```

### 7. Push

Os colaboradores estão com permissão de dar _push_ de sua _branch_ local `feat/add-fulana-image` para o endereço remoto `origin`.

```bash
git push origin feat/add-fulana-image
```

### 8. Pull request (PR)

No github, você pode solicitar um _pull request_ para o repositório remoto. Partindo da _branch_ `feat/add-fulana-image` que você deseja implementar a funcionalidade para a _branch_ `main`.

Adicione _reviewers_ ao _pull request_ para que possam revisar e aprovar sua solicitação de PR.

### 9. Merge

Após aprovado o _PR_, você deve fazer o _merge_ da _branch_ `feat/add-fulana-image` para _branch_ `main`.

Deletar a _branch_ `feat/add-fulana-image` do repositório remoto, pois ela já cumpriu o seu objetivo.

### 10. Pull

Em sua máquina, volte para a _branch_ `main`:

```bash
git checkout main
```

Atualize o repositório local após o merge no GitHub em seu terminal:

```bash
git pull origin main
```

Delete a _branch_ `feat/add-fulana-image` localmente:

```bash
git branch -D feat/add-fulana-image
```

### 11. Start

Verifique se o projeto está funcionando corretamente:

```bash
npm start
```

### 12. Deploy

Caso tudo esteja funcionando corretamente, você pode fazer o _deploy_ do projeto:

```bash
npm run deploy
```

## Dicas

### Nomenclatura de _branch_ e mensagens de _commit_

A padronização de mensagens de commit e nomes de _branch_ facilitam o entendimento entre desenvolvedores.

Uma forma seria o formato do **Commit Amigão**:

- **feat** (nova funcionalidade para o usuário)
- **style** (formatação geral no código, como lint. Não confundir com CSS)
- **refactor** (refatoração de código de produção)
- **test** (adicionar/refatorar testes)
- **fix** (correção de bug para o usuário)
- **docs** (mudanças na documentação)
- **chore** (atualização de tarefas ou código que não está relacionado a código em produção)

![Conversa entre dois desenvolvedores sobre mensagem de commit](https://vidadeprogramador.com.br/uploads/2017/07/tirinha1713.png 'Conversa entre dois desenvolvedores sobre mensagem de commit')

Fonte: [Vida de Programador](https://vidadeprogramador.com.br/uploads/2017/07/tirinha1713.png) 🇧🇷

### Referências

- [O que é GitHub?](https://youtu.be/w3jLJU7DT5E) (Youtube) áudio: 🇺🇸 | legenda: 🇧🇷

- [Guia do Commit Amigão](https://github.com/BeeTech-global/bee-stylish/tree/master/commits) 🇧🇷

- [Conventional Commits](https://www.conventionalcommits.org/pt-br/v1.0.0-beta.4/) 🇧🇷
