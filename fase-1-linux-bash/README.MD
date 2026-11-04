Agora que começa os estudos referente a bash e outros, vou fazer do 0 até o 15

level0 do bandit
Só dar cat no arquivo de readme msm, antes, entrei no SSH deles.

Level1 
Como - é um comando que confunde o linux com cat, devemos usar ./- para especificar que é um arquivo.

Level2 
 -- avisa ao comando cat que todas as opções terminaram ali e o que vem a seguir é estritamente o nome do arquivo. Combine isso com as aspas por conta dos espaços.

Level3
Era um arquivo oculto, devemos usar o ls -a para listar arquivos ocultos.

Level4
Era um arquivo only human readable, com isso eu vi em um site de um cara que eu deveria usar o comando file + * para ver qual de todos tinha um ascii ou algo que desse para uma pessoa comum ler, ahei a chave 6C7h9GD8M6ai5nr7wo1RonrzFjj9yIrG
file ./* <- listar todos os files e que tipo de texto eles tinham

Level5
Esse já ta ficando pegado, usar um monte de comando, como find . -ls para listar todos e depois filtrar com | grep, ele busca referente ao valor que colocarmos, que no caso é 1033 que pede no site
com isso ele retorna um arquivo, assim podemos usar o cat e o path para ver a senha do file, que no caso é pXa26xhMWaC2SvDotA4r9EgZkulOeSBW

level6
Tá ficando mais tenso, agora estamos indo para file permissions, todo file é de alguem ou de um grupo
nesse caso como temos o nome do user e do group, podemos filtrar por file -> file / pro dir e então -> file / -user bandit7 -group bandit6 -size 33c <-- isso pede o tamanho do arquivo em bytes, o c é bytes vai retornar isso (/var/lib/dpkg/info/bandit7.password) -> 

level7
FIz direto, botei um grep millionth e rodei em data.txt -> VR1ljMayciFxbnUokuQmJFw6QC9VKtub

level8
Estou aprendendo vários comandos no linux, essa eu precisava achar uma linha de texto que aparecia apenas 1 vez no arquivo todo, que eu acho que era enorme.
usando o comando você recebe essa password EjmOSvuAu7sGAHqHVcBDPirRe9T03kxl

level9
To igual o Lula, pergunta pro Gûgu, estou dando uma vasculhada e vi que ele pede string,     com isso coloquei strings data.txt | grep "==" (Isso filtra as strings em data que possuem == nelas) a passkey deu -> B0s2khmbT9u0geKuOoVGW3JZKhndE3BG

level10
usei o base64 e dei decode no arquivo, é isso... (base64 -d arquivo.txt)
pYfOY6HwUsDj5rL9UvyhU7MCmv8vN5Ro