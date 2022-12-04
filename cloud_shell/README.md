# GCP Cloud Shell

Interface de Linha de Comando preparada com todas as bibliotecas comuns para uso do Google Cloud

Também há integrado um editor para facilitar a criação/edição de códigos na máquina provisionada para uso do cloud shell.

## Utilizando o Cloud Shell

Para utilizar o Cloud Shell, basta clicar em seu ícone na barra superior do console do GCP, como mostra a imagem abaixo:
![abrindo_cloudshell](./imagens/abrindo_cloudshell.png)

Para ter uma visualização melhor, é possível abri-lo em uma nova janela clicando no ícone indicado na imagem abaixo:
![abrindo_em_nova_janela](./imagens/abrindo_em_nova_janela.png)

Como o cloudshell tem todas as bibliotecas necessárias para uso do GCP, podemos verificar suas informações utilizando o comando ``gcloud info``, e informações sobre a instância provisionada serão obtidas, como o sitema operacional da mesma, e componentes instalados.
![gcloud_info](imagens/gcloud_info.png)

## Exemplo utilizando uma aplicação Java

A aplicação a ser utilizada na exemplificação se encontra no github do próprio GCP através do link [https://github.com/GoogleCloudPlatform/java-docs-samples](https://github.com/GoogleCloudPlatform/java-docs-samples)

A aplicação será clonada para dentro da instância do Cloud Shell utilizando o comando ``git clone https://github.com/GoogleCloudPlatform/java-docs-samples``

Entraremos no diretório da aplicação com o comand ``cd java-docs-samples/appengine-java11/quarkus-helloworld/``

Ao abrirmos a pasta do projeto com o editor de código do Cloud Shell o próprio editor identifica a aplicação e instala suas dependências.
![editor_identificando_projeto_java](imagens/editor_identificando_projeto_java.png)
![build_automática_realizada_pelo_editor](imagens/build_automática.png)

Para prosseguir com a instalção do projeto, executamos o comando ``mvn clea install``
![build_concluida_com_sucesso](imagens/build_concluida.png)

Por fim, entramos no diretório target com o comando ``cd target`` e executamos o comando ``java -jar quarkus-helloworld-1.0-SNAPSHOT-runner.jar`` para rodar a aplicação.
![rodando_a_aplicação](imagens/rodando_aplicacao.png)

Percebe-se que a aplicação está rodando com sucesso ao acessa-la no link forncedio
![aplicacao](imagens/aplicacao.png)