# Activity

Activity é o ponto de entrada do aplicativo.  É composta por :

*   View - > É o aspecto visual
*   Lógica - > Código  responsável por fazer a lógica funcionar.

Para criar a activity é preciso utilizar técnicas da programação orientada a objetos com a herança. Então cria uma subclasse chamada de MainActivity que vai herdar de Activity.
Tem que entrar na pasta manifests para fazer as configurações principais do aplicativo. Em application é onde fica o estado global do aplicativo.
É preciso fechar a tag application e inserir a tag activity com o nome da classe criada MainActivity. 

1. Então cria uma subclasse chamada de MainActivity que vai herdar de Activity.
2. Tem que entrar na pasta manifests para fazer as configurações principais do aplicativo.
3. Em application é onde fica o estado global do aplicativo.
4. Depois inserir a tag insert-filter.
5. Dentro da tag insert-filter , colocar action e category.

A execução é feita em um ambiente simulado. Poderia muito bem ser executado em um celular, por exemplo.

Ciclo de vida, as entidades dos android vai ter estados que vai criar e destruir activitys.

Exemplo, adicionar um comportamento quando a activity for criada, consegue sobrescrever os métodos. É assim que adiciona novos comportamentos na activity.