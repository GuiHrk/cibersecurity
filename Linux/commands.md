Comandos :

pwd : informa em qual pasta voce está navegando

cd: change directory // muda o diretório/ pasta  ( cd /  vai para a raiz do sistema) 

cd .. : Volta um diretório atrás

cd ../ {arquivo do diretório anterior} :  volta um diretório e já abre o arquivo depois da barra

cd ~ : seleciona direto a pasta do usuário

Tecla TAB 2x lista os diretórios sem fechar o comando

ls : lista os arquivos e diretórios presentes

ls | more : se não tiver barrar de rolagem para visualizar lista, este comando apresenta a lista

ls  {nome do arquivo} ele apresenta diretamente o nome do arquivo, se existe ou não

ls  {começo do nome} clicar 2x no tab ele vai selecionado

ls {letra} : seleciona arquivos iniciados com a letra

ls {letra}* : informa arquivos e diretórios 

ls {letra1} ? {letra3} * : seleciona arquivos que a primeira letra tem que ser igual o digitado, a segunda (?) tanto faz, a terceira tem que ser correspondente a letra digitada, * o restante não importa. 

touch nome_do_arquivo.formato 

ls {nome_arquivo}[1 - x (algarismos numericos representantes do arquivo)].{formato} ou * (seleciona todos)

### **cat**

O comando **cat** exibe o conteúdo de um arquivo. Por exemplo, digitar **cat updates.txt** retorna todo o conteúdo do arquivo **updates.txt**.

### **head**

O comando **head** exibe apenas o início de um arquivo, por padrão, 10 linhas. O comando **head** pode ser útil quando você deseja conhecer o conteúdo básico de um arquivo, mas não precisa do conteúdo completo. Digitar **head updates.txt** retorna apenas as primeiras 10 linhas do arquivo **updates.txt**.

 Se quiser alterar o número de linhas retornadas por **head**, você pode especificar o número de linhas incluindo **-n**. Por exemplo, se quiser exibir apenas as cinco primeiras linhas do arquivo **updates.txt**, digite **head -n 5 updates.txt**.

### tail

O comando **tail** faz o oposto de **head**. Esse comando pode ser usado para exibir apenas o final de um arquivo, por padrão 10 linhas. Digitar **tail updates.txt** retorna apenas as últimas 10 linhas do arquivo **updates.txt**.

**Dica profissional**: é possível usar **tail** para ler as informações mais recentes em um arquivo de log.

### less

O comando **less** retorna o conteúdo de um arquivo, uma página de cada vez. Por exemplo, digitar **less updates.txt** muda a janela do terminal para exibir o conteúdo de **updates.txt** uma página de cada vez. Isso permite que você avance e retroceda facilmente no conteúdo.

Depois de acessar o conteúdo com o comando **less**, é possível usar vários controles de teclado para percorrer o arquivo:

- **Space bar**: Avançar uma página
- **b**: Avançar uma página : Retroceder uma página
- **Down arrow**: Avançar uma linha
- **Up arrow**: Avançar uma linha : Retroceder uma linha
- **q**: Sair e retornar à janela anterior do terminal

### **Diretórios padrão da FHS**

Diretamente abaixo do diretório raiz, você encontrará os diretórios padrão da FHS. No diagrama, **home**, **bin** e **etc** são diretórios padrão do FHS. Aqui estão alguns exemplos do que os diretórios padrão contêm:

- **/home**: Cada usuário do sistema tem seu próprio diretório pessoal.
- **/bin**: Esse diretório significa "binary" (binário) e contém arquivos binários e outros executáveis. Executáveis são arquivos que contêm uma série de comandos que o computador precisa seguir para executar programas e realizar outras funções.
- **/etc**: Esse diretório armazena os arquivos de configuração do sistema.
- **/tmp**: Esse diretório armazena muitos arquivos temporários. O diretório **/tmp** é comumente usado por atacantes porque qualquer pessoa no sistema pode modificar os dados nesses arquivos.
- **/mnt**: Esse diretório significa "montagem" e armazena mídia, como unidades USB e discos rígidos.

**Dica profissional**: você pode usar o comando **man hier** para saber mais sobre o FHS e seus diretórios padrão.

# Grep

Pesquisa um arquivo especificada e retorna todos o conteudo contando uma string especificada. 

Exemplo: no diretório updates, buscamos todos as strings com argumento. 

Grep  OS {O que estamos procurando } updates.txt = retorna todas as linhas contendo o argumento. 

“| ” piping = tubulação. 

Exemplo: ls /home/analyst/reports | grep users 

retorna os nomes de arquivos e diretórios no diretório reports que contêm users. 

# Comandos

mkdir: cria novo diretorio

rmdir: remova ou exclui diretório. 

touch: cria novo arquivo

rm: remove ou excluir arquivo

mv: move arquivo ou diretório

cp: copia arquivo ou diretório em outro local

Para abrir um arquivo existente no nano a partir do diretório que o contém, digite nano seguido do nome do arquivo.

# Permissões e propriedade de arquivos. 

**Autorização** Conceito de conceder acesso especifico a recursos no sistema. 

## Tipos de permissão em Linux

- Read : conteudo do arquivo do diretório pode ser lido.  R
- Write/ gravação : Permite modificiação no arquivo do diretório W
- Execute/ Execução : O arquivo pode ser executado se for um executável. X 

## Tipos de proprietários

- user/ usuário: Proprietário do arquivo. 
- group/ grupo: Um grupo consiste em vários usuários.
- other/ outro: qualquer outra pessoa com acesso do sistema. 

- ls -l : Mostra as permissões dos arquivos e diretórios. 
- ls -a : mostra arquivos escondidos
- combinar as duas opções é uma possibilidade: `ls -la`: Mostra as permissões de arquivos e diretórios com arquivos ocultos. 

## Mudança de permissões

`chmod` Muda as permiossões em arquivos e diretórios. 

- user/ Usuário: u 
- group/ Grupo: g
- other/ Outro: o

Exemplo:
t
cgmod g+w,o-r access.txt

g = g indica que serão realizadas alterações nas permissões de grupo.
o = indica que serão realizadas alterações nas permissões de outros. 

"+" indica que o comando irá adicionar permissões
"-" indica que o comando irá retirar permissões

Ou seja, no comando está sendo adicionado as permissões de gravação ao grupo, e retirando as permissões de leitura de outros. 