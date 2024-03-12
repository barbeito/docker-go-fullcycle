# Dasafio docker GO

## Enuciado do desafio

Esse desafio é muito empolgante principalmente se você nunca trabalhou com a linguagem Go!
Você terá que publicar uma imagem no docker hub. Quando executarmos:

docker run <seu-user>/fullcycle

Temos que ter o seguinte resultado: Full Cycle Rocks!!

Se você perceber, essa imagem apenas realiza um print da mensagem como resultado final, logo, vale a pena dar uma conferida no próprio site da Go Lang para aprender como fazer um "olá mundo".

Lembrando que a Go Lang possui imagens oficiais prontas, vale a pena consultar o Docker Hub.

> A imagem de nosso projeto Go precisa ter menos de 2MB =)

Dica: No vídeo de introdução sobre o Docker quando falamos sobre o sistema de arquivos em camadas, apresento uma imagem "raiz", talvez seja uma boa utilizá-la.

Suba o projeto em um repositório Git remoto e coloque o link da imagem que subiu no Docker Hub.

Compartilhe o link do repositório do Git remoto para corrigirmos seu projeto.

Divirta-se!

## Explicação sobre o projeto

Dentro da pasta go se encontram os arquivos:

- go.mod;
- main.go => arquivo com a função que imprime a mensagem: "Full Cycle Rocks!!"
- Dockerfile => arquivo para geração da imagem;

link para a imagem no docker hub:

> https://hub.docker.com/r/barbeito/fullcycle

Para atender o critério de tamanho máximo da imagem de 2MB, foi utilizado como base para a imagem da aplicação a imagem "***scratch***", que é uma imagem bem enxuta para criação de imagens no docker.

## Comando para criar a imagem

Para criar a imagem acessa a pasta raiz do projeto e executar o seguinte comando, lambrando de definir um nome para a imagem:

```
docker build -t <nome_imagem> ./go
```

## Comando para executar o container

Após a criação da imagem, executar o seguinte comando para iniciar um contêiner:

```
docker run -it --rm --name <nome_contaimer> <nome_imagem>
```