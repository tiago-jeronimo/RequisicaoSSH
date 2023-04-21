# Acesso seguro e remoto ao Linux com SSH

O SSH (Secure Shell) é uma ferramenta de linha de comando que permite o acesso seguro a um servidor Linux remotamente. Com o SSH, você pode se conectar a um servidor Linux de qualquer lugar do mundo, desde que tenha as credenciais de login corretas.

O SSH funciona criando um túnel seguro entre o seu computador e o servidor remoto. Esse túnel é criptografado, o que significa que qualquer informação que você envie ou receba durante a conexão é protegida contra interceptação ou hacking.

## Acessando o servidor

Para se conectar a um servidor Linux usando o SSH, você precisará do endereço IP do servidor e das credenciais de login (nome de usuário e senha). Em seguida, abra o terminal em seu computador e digite o seguinte comando:


    ssh <nome_de_usuario>@<endereco_IP_do_servidor>

Substitua `<nome_de_usuario>` pelo seu nome de usuário e `<endereco_IP_do_servidor>` pelo endereço IP do servidor Linux. Em seguida, pressione Enter e digite sua senha quando solicitado.

Observação: Em `ssh <nome_de_usuario>@<endereco_IP_do_servidor>`, o `nome_de_usuario` refere-se ao nome de usuário do servidor remoto. Ou seja, é a conta de usuário que você deseja acessar no servidor remoto. É importante ter as credenciais de login corretas do servidor para poder acessar e fazer login com sucesso usando o SSH. O usuário que está fazendo o acesso é aquele que está digitando o comando SSH em seu próprio terminal, e não é necessário especificar seu nome de usuário nesse comando.

Depois de fazer login no servidor Linux, você poderá executar comandos e interagir com o sistema operacional remotamente.

## Transferindo arquivos

Você também pode transferir arquivos entre seu computador e o servidor usando o SCP (Secure Copy), que é um utilitário de linha de comando que acompanha o SSH.

Para transferir um arquivo do seu computador para o servidor, use o seguinte comando:


       scp <caminho_do_arquivo_local> <nome_de_usuario>@<endereco_IP_do_servidor>:<caminho_do_destino_no_servidor>



Substitua `<caminho_do_arquivo_local>` pelo caminho para o arquivo em seu computador e `<caminho_do_destino_no_servidor>` pelo caminho para o diretório no servidor onde você deseja armazenar o arquivo. Novamente, substitua `<nome_de_usuario>` e `<endereco_IP_do_servidor>` pelos detalhes de login do servidor.

Para transferir um arquivo do servidor para o seu computador, use o seguinte comando:

    scp <nome_de_usuario>@<endereco_IP_do_servidor>:<caminho_do_arquivo_no_servidor> <caminho_do_destino_local>

Substitua `<caminho_do_arquivo_no_servidor>` pelo caminho para o arquivo no servidor e `<caminho_do_destino_local>` pelo caminho para o diretório em seu computador onde você deseja armazenar o arquivo.




