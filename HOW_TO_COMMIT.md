## Passo-a-Passo para os commits

### 1. Sempre atualizar o repositório local

Para evitar Bugs ou conflitos, sempre use o comando antes de qualquer alteração no ficheiro.

```sh
git pull
```

### 2. Criar uma Branch própria

É necessário que se crie uma branch própria com o seu nome.

Para criar basta:

```sh
git branch [nome]
```

e então comece a usá-la com

```sh
git checkout [nome da branch]
```

ou uma forma de juntar os dois comandos anteriores em um só, basta escrever

```sh
git checkout -b [nome]
```

que será criada uma branch nova e já irá mudar para a mesma.

> **Façam as alterações necessárias apenas na própria branch**
> Alterações na branch Main apenas quando extremamente necessário.

### 3. Começar a editar a Branch

Após criar e fazer as alterações necessárias na própria branch, use os comandos convencionais pra realizar o commit

```sh
git add .
git commit -m "[menssagem]"
```

### 4. Criar um Pull Request

Para poder atualizar o repositório no GitHub com as suas alterações com um Merge na Main, é necessário que crie um Pull Request.

Primeiro, é necessário adicionar a sua branch (que por enquanto só existe na sua máquina) no repositório da nuvem. Basta fazer:

```sh
git push --set-upstream origin [nome da branch]
```

> **Esse comando só é necessário uma única vez, após, para as próximas vezes basta executar o comando:** `git push`
> Após isso, crie um PR.

1. Basta ir até o repositório na aba de [Pull Request](https://github.com/EnzoVieira/stack-machine/pulls) e clicar em <mark style="background-color: #347d39; color: white;padding: 4px 10px; border-radius: 6px;">Compare & pull request<mark>
2. (opcional) Adicione um título e uma descrição para o commit
3. Clique em <mark style="background-color: #347d39; color: white;padding: 4px 10px; border-radius: 6px;">Create pull request<mark>

### 5. Atualizar o repositório local

Após o merge ser feito no repositório no GitHub, é necessário atualizar o repositório local para estarem de acordo.

1. Ainda na sua branch: `git pull`
2. Migrar para a main `git checkout main`
3. Atualizar a main `git pull`

---

Em casos extremos, em que se deu algum erro na sua branch e você quiser recomeçar a partir do último commit da branch Main, basta executar

```sh
git reset --hard origin/main
```

**O comando irá <mark style="background-color: #ffffff00; color: red; font-weight: 600;">apagar</mark> todas as alterações na sua branch que foram feitos após o último commit da branch Main**
