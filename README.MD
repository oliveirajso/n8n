# Como executar o Docker Compose

Para executar o Docker Compose e iniciar os serviços do MySQL e n8n, siga os passos abaixo:

## Pré-requisitos
- Certifique-se de ter o Docker e o Docker Compose instalados em sua máquina. Se ainda não tiver, você pode instalá-los seguindo as instruções em: [Docker](https://www.docker.com/get-started) e [Docker Compose](https://docs.docker.com/compose/install/).

## Passo 1: Obtenha o arquivo docker-compose.yml
- Faça o download do arquivo `docker-compose.yml` do repositório ou projeto onde ele está disponível. Certifique-se de salvá-lo em um diretório de sua escolha.

## Passo 2: Navegue até o diretório com o arquivo docker-compose.yml
- Abra o terminal ou prompt de comando do seu sistema operacional.
- Use o comando `cd` para navegar até o diretório onde você salvou o arquivo `docker-compose.yml`.

## Passo 3: Execute o Docker Compose
- Com o terminal ainda aberto no diretório do arquivo `docker-compose.yml`, execute o seguinte comando:

```bash
docker-compose up
```

O Docker Compose iniciará o processo de download das imagens necessárias, criará os contêineres e configurará os serviços do MySQL e n8n de acordo com o que foi especificado no arquivo `docker-compose.yml`.

## Passo 4: Acesse o n8n
- Após o Docker Compose concluir a inicialização dos serviços, você poderá acessar o n8n através de um navegador da web.
- Abra seu navegador e insira o seguinte endereço na barra de URL:

```
http://localhost:5678
```

Se você não especificou uma porta personalizada no arquivo `docker-compose.yml`, o n8n estará disponível na porta padrão 5678.

## Passo 5: Encerrando os serviços
- Para interromper a execução dos serviços, pressione `Ctrl + C` no terminal em que o Docker Compose foi iniciado.
- Se desejar parar e remover todos os contêineres e volumes, execute o seguinte comando no mesmo diretório do arquivo `docker-compose.yml`:

```bash
docker-compose down
```

Isso encerrará os serviços e removerá os contêineres, mas o volume persistente `mysql_data` permanecerá intacto para futuras execuções.

Agora você está pronto para executar o Docker Compose e utilizar o MySQL e n8n em sua máquina local. Lembre-se de que o arquivo `docker-compose.yml` pode ser ajustado para atender a diferentes necessidades e configurações.