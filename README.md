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
        - `rc` (run commands) é uma conversão para scripts de inicialização, como seu arquivo de configuração do zsh o .zshrc
        