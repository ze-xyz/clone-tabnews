## dia 2
- relação entre github e youtube

- criando repositório

- codespaces

## dia 3
- nunca criamos de fato algo `from scratch`, sempre começamos com algo que outras pessoas criaram 

- vamos usar o `nvm`(node version manager) para garantir que todas as partes do projeto usem a mesma versão do `node.js`
    - com o comando `nvm ls` lista versões disponíveis do node
    - a escolhida foi a `lts/hydrogen`, onde `lts` (long term support) = suporte maior e mais atualizado.
    - com o comando `nvm install <versão>` o nvm baixa, instala e configura a versão escolhida, MASSS *somente na instancia atual do terminal*
    - para definir uma versão padrão usar comando `nvm alias default <versão>`
    - criar arquivo `.nvmrc` que vai garantir que todos que contribuirem saibam a versão que recomendo. 
        - `rc` (run commands) é uma convensão para scripts de inicialização, como seu arquivo de configuração do zsh o .zshrc

- usaremos o `next.js` como framework pra web dev
- para isso devemos criar um arquivo de manifesto que irá listar todas as dependências do projeto. o `package.json`
- agora sim, podemos instalar as dependências usando o gerenciador de pacotes `npm`
    - `npm install nome@versão`
        - `next@13.1.6`
        - `react@18.2.0`
        - `react-dom@18.2.0`
    - note que em muitos casos a versão x de y pode estar desatualizada, vamos instalar de proposito assim.

## dia 4
- protocolo = regras e normas que permitem a comunicação entre dispositivos em uma rede.
    - **protocolos de aplicação**, definem como dados são apresentados e transferidos.
        - http = regras para transferência de arquivos na web
        - ftp = regras para transferências de arquivos entre sistemas
        - smtp = regras para transferência de emails
    - **protocolos de transporte**
        - tcp = transmissão de dados confiável e ordenada
        - udp = transmissão de dados rapidas mas sem garantia de entrega ou ordem

- criando um alias pra encurtar o comando `npm run next dev` no `package.json` deixando somente `npm run dev`

- como o next usa um sistema de `file-based routing` onde as páginas no seu site correspondem exatamente a estrutura das pastas e diretórios. 
- ao rodar o comando `npm run dev` ele retorna um erro, dizendo que não foi possivel encontrar um diretório com uma página.
- No next todas as páginas criadas estarão em `pages`.
    - criamos dentro dela um arquivo `index.js` que ira agir como a "home" do nosso projeto.
        - criamos uma função `Home` e dentro dela retornamos algo pra aparecer na tela e testar.
        - como queremos que a função `Home` seja de fato renderizada, usaremos o comando `export Home;`. 
        - queremos que a função `Home` seja a padrão e para isso adicionamos `default` apos `export`
        - ao executar `npm run dev` a página está rodando de forma local.

## dia 5
- versionamento de codigo
    - centralizado = existe uma única cópia do repositório em um servidor central. Quando alguém precisa trablhar em qualquer arquivo desse repositório, eles reservam, fazem o `checkout`, travando o arquivo. O restante da organização ainda pode le-lo, mas so podem modifica-lo após a pessoa que o reservou fazer o `checkin`.
        - isso tudo era feito para evitar o `merge`. Se apenas uma pessoa está editando o arquivo e pro resto está bloqueado, não tem como informações diferentes de um mesmo arquivo conflitarem.
    - distribuido = com a evolução dos algoritmos de `merge` todos os envolvidos no projeto agora podem ter acesso a um cópia de todo o repositório. Desse modo, todos podem modifica-lo sem nenhuma trava. // **estudar sobre algoritmos de merge e git**

- git `log`
- estágios de um arquivo git
    - `untracked` 
    - `modified`
    - `staged`
    - `commit`
- usando `amend` pra adicionar novos arquivos a um commit anterior ou melhor "voltar no tempo".

## dia 6
- git push