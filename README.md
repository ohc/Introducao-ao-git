# Introdução ao Git

## O que é um SCV (VCS)

Um sistema de controle de versão é um tipo de prática para controle de mudanças no código fonte de algum projeto. Normalmente também é utilizado para controlar as documentações, configurações e arquivos que fazem parte desse projeto.


### Por que usar?

O uso de um SCV é muito importante para o controle e evolução do software, melhorando a produtividade, deixando os desenvolvedores focados em solucionar problemas de desenvolvimento.

Em um projeto é comum serem criadas várias versões do mesmo software e em alguns casos versões diferentes aplicadas em sistemas diferentes. Com um SCV os desenvolvedores podem simplesmente manter e gerenciar apropriadamente várias cópias organizadas de diferentes versões do programa.
 
Sistemas de controle de versão também são convenientes quando diversos desenvolvedores trabalham sobre o mesmo projeto simultaneamente, resolvendo eventuais conflitos entre as alterações. A maioria dos sistemas possui diversos recursos como ramificação e mesclagem de histórico para auxiliar nessas tarefas.

Para que seja possível o trabalho em equipe, o sistema de controle de versão pode possuir um mini sistema de controle de usuários embutido ou pode utilizar algum outro sistema de autenticação separado. Assim, é possível identificar cada usuário, que geralmente fica protegido por uma senha pessoal, ou alguma senha criada pelo administrador de sistemas.


## Tipos de SCV

O funcionamento de um SCV consiste em manter um repositório com os arquivos que serão controlados e o histórico de suas mudanças.

Para otimizar o espaço ocupado em disco pelas versões de um arquivo, uma parte dos SCVs utiliza o método de compressão Delta, que armazena apenas as diferenças entre as versões de um determinado arquivo. O princípio da compressão delta é que as somas das diferenças entre versões sequenciais de um determinado arquivo, partindo da versão original (ou mais antiga), é capaz de produzir a versão mais nova.


### Centralizado

Um SCV centralizado, possui um único servidor como repositório contendo todos os arquivos versionados. Cada desenvolvedor ao efetuar uma alteração em um arquivo qualquer atualiza o repositório enviando suas alterações para o servidor.

Os SCVs centralizados são extremamente dependentes do repositório que contém os dados, de tal maneira que um desenvolvedor não pode sequer requisitar informações de um determinado arquivo se não existir uma conexão com o repositório, embora isto não o impeça de continuar editando os arquivos.

### Descentralizado

O SCV descentralizado também possui um servidor que contém os arquivos, mas cada usuário pode possuir um repositório filho com todas as revisões do repositório pai.

Do ponto de vista operacional, um SCV descentralizado não é muito diferente de um SCV centralizado, a grande diferença está no fato que não existe somente um repositório, mas sim vários repositórios e um repositório para cada usuário, dependendo da ferramenta utilizada. Deste modo, é possível fazer, por exemplo, com que repositórios filhos de um mesmo repositório pai compartilhem suas mudanças entre si.

Em um SCV descentralizado, uma conexão permanente com o servidor não é requisito fundamental para
o funcionamento do sistema. Uma vez que cada usuário mantém o seu próprio repositório, as mudanças podem sofrer alterações locais e somente depois de atingirem o repositório pai ou os repositórios irmãos.

Esta maneira de organizar e acessar os repositórios torna os SCVs descentralizados ideais para grupos de trabalho espalhados ao redor do mundo, aonde uma conexão entre os membros nem sempre existe ou é estável.

O que não quer dizer que uma conexão de rede, ou pelo menos uma forma de propagar estas modificações não seja importante para um SCV descentralizado. Ocorre que, um desenvolvedor utilizando um SCV descentralizado poderá ter acesso as informações do repositório pai mesmo que, no momento, não exista uma conexão com o mesmo. Estas informações, porém, serão referentes à última sincronização do repositório local, com o repositório pai ou irmão.

Além disto, o fato de ser descentralizado não quer dizer que este repositório filho não necessite replicar as suas modificações para o seu repositório pai, caso contrário as suas modificações não seriam replicadas para os outros membros do conjunto.

## Git

Um repositório Git é um banco de dados simples que contem toda a informação necessária para administrar o histórico de um projeto. No Git como na maioria dos sistemas de controle de versão, um repositório contem uma cópia completa do projeto em todo seu tempo de vida.


### História

O Git foi criado em 2005 pelo Linus Torvalds, o criador do Linux, pois o vinculo da comunidade com a empresa que desenvolvia o sistema utilizado para versionar os códigos do kernel do linux na época se desfez. Linus procurou e estudou pacotes de software livre para controle de versão mas acabou encontrando muitas limitações e falhas, fazendo ele desenvolver sua própria ferramenta.

Desde sua concepção, o Git evoluiu e amadureceu a ponto de ser um sistema fácil de usar e ainda assim mantém essas qualidades iniciais. É incrivelmente rápido e bastante eficiente em grandes projetos.

### Desenvolvimento distribuído

Pelo fato do Git ser um sistema distribuído, é vital obter uma garantia absoluta da integridade dos dados. Para isso o Git usa uma criptografia de hash (SHA1) para nomear e identificar objetos no seu banco de dados. Embora talvez não absoluta, na prática, tem provado ser sólido o suficiente para garantir a integridade e confiança de grandes repositórios.

### Arquivos grandes

Um dos aspectos-chave de um sistema de controle de versão é saber que os arquivos alterados e, se possível, por que. Git impõe um log de alterações em cada commit. As informações armazenadas no log de alteração são deixadas por conta do desenvolvedor.

### Merges complexos

Os merges são combinações de uma ou mais branches em uma unica branch. O git compara dois conjuntos de alterações e determina quando as mudanças ocorreram. Quando as mudanças ocorrem em partes diferentes de um arquivo, o git pode fazer o merge automaticamente, porem as vezes pode ocorrer algum conflito que deverá ser solucionado manualmente.


### Vários branches

As branches são uma forma de manter vários históricos alternativos do mesmo projeto. Você pode usar uma branch para manter uma cópia do projeto que já está estável e funcionando e ao mesmo tempo usar uma outra branch para continuar o desenvolvimento sem afetar a ultima versão.

### Ser muito rápido

### Ser robusto

## Anexo

Para você que quer começar com git o quanto antes, mas mesmo depois de ter lido ainda não sabe como, experimente git online :D.

[TryGitHub](https://try.github.io/)
[LearnGit](http://pcottle.github.io/learnGitBranching/)
