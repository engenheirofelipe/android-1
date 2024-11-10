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

# Iniciando a View

Colocando uma view dentro da activity.

1.  Escrever setContentView();
2.  Criar instância da view : TextView aluno new TextView(this);
3.  Depois chamar em aluno.setText("felipe) e chamar em setContentView(aluno)

Porém essa técnica não pe uma boa prática, porque coloca muita responsabilidade na activity. Quanto menos responsabilidade melhor.

# Outra maneira 

1. Cria um diretório layout (main) dentro de res, depois um file activity_main

Próximo passo.

Pegar os componentes views e fazer o vínculo com o código fonte.

2. Criar uma list que vai representar os alunos. (No arquivo MainActivity)
list<String> alunos = new ArrayList<>(Arrays.asList())
Criar lista de maneira dinâmica.

3. Depois utilizar TextView primeiroAluno = findViewById(R.id.textView), para localizar a view.

# Maneira correta 

1.  Cria um ListView no arquivo do layout. E dá o nome do id de activity_main_lista_de_alunos

2.  Depois no código em , Main Activity.java, aplicar um Array.

    *   List<String> listaAlunos = new ArrayList<>(Arrays.asList("Felipe Ferreira", "Martelo Dias", "Carolina Azevedo"))

3. Ainda no arquivo MainActivity.java fazer:

    *  ListView listaAlunos = findViewById(R.id.activity_main_lista_de_alunos)
    *  listaAlunos.setAdapter(new ArrayAdapter<String>(context:this, android.R.layout.simple_list_item_1, alunos))   Adapter é um intermediário que sincroniza os dados da lista com a ListView. O ArrayAdapter serve para simplificar a implementação. 


#   views

Para utilizar uma view dentro de outra basta inserir a ViewGroup. e vai formar as lauputs 

  A url xmlns:android="http://schemas.android.com/apk/res/android" do arquivo da activity_Main.xml é o que vai fazer importar o restande dos atributos no código

  Além disso adicionar :

*   android:layout_alignParentEnd="true"
*   android:layout_alignParentBottom="true"
*   android:layout_marginEnd="26dp"
*   android:layout_marginBottom="26dp"