# APP-DanceSP

Carolina de Oliveira Alves 3°DS

Isabela de Oliveira Alves 3°DS

##     O DanceSP será um aplicativo onde obterá informações sobre os grupos de "Street's Dance" mais famosos de São Paulo, informações como a história do grupo, localização, criador ou lider do grupo, modalidades e informações sobre as criadoras da aplicação, assim podendo levar conhecimento sobre os grupos de São Paulo.

# Tela Inicial - Estática.
![image](https://github.com/IsabelaCSS/Dance-App/assets/128037357/c7458d60-ec76-4bcb-b35a-f33e86754c9d)

Essa tela de apresentação irá mostrar uma foto de fundo, o nome, a logo do app e o copyright.

### Widgets - Inicial 
**1 - Image:** É a implementação de uma imagem

**Parametro** 

    const Image(
      image: NetworkImage('https://flutter.github.io/assets-for-api-docs/assets/widgets/owl.jpg'),
    )

--------------------------------------------------------------------------------------------------

**2 - Text:** Implementação de Texto

**Parametro** 

    RichText(
        const TextSpan(text: 'texto'),)


# Tela Home - Dinâmica.
![image](https://github.com/IsabelaCSS/Dance-App/assets/128037357/c8d9a26f-d99b-4a51-b6c1-1b952dd04066)

Essa tela irá apresentar 3 escolhas para o usuário decidir qual modalidade, mostrando uma imagem representativa da modalidade e o nome, sendo as modalidades Hip Hop, Ballet e Jazz.
Logo abaixo da opções terá um rodapé com botões que irão indicar a navegação do usuário durante toda a aplicação.

### Widgets - Home
**1 - TextButton:** Ultilizado como botão com um texto.

**Parametro** 

    TextButton(
        style: TextButton.styleFrom(
          primary: Colors.blue,
          ),
          onPressed: () { },
          child: Text('TextButton'),
    )

--------------------------------------------------------------------------------------------------

**2 - Text:** Implementação de Texto.

**Parametro** 

    RichText(
      const TextSpan(text: 'texto'),)

--------------------------------------------------------------------------------------------------

**3 - IconButton:** Ultilizado como botão com imagem.

**Parametro** 
 
    IconButton(
          splashRadius: 100,
          iconSize: 200,
          icon: Ink.image(
            image: const NetworkImage(
                'https://picsum.photos/250?image=9'),
    ),

        
# Tela modalidade Hip-Hop/Ballet/Jazz - Dinâmicas.
![image](https://github.com/IsabelaCSS/Dance-App/assets/128037357/2921d0aa-51d1-48f3-b5f8-ee3c050ba9d8)

Essas telas serão exatamentes indenticas na sua funcionalidade, como um botão em formato de estrela que irá adicionar aos favoritos, imagem e o nome de cada grupo e um botão que irá direcionar as informações do grupo. 

### Widgets - Modalidades
**1 - Container:** Ultilizado para pintar uma parte especifica na tela.

**Parametro** 

    Container(
      color: Colors.black,
        child: Text('Container'),
    );

--------------------------------------------------------------------------------------------------

**2 - Image:** É a implementação de uma imagem.

**Parametro** 

    const Image(
      image: NetworkImage('https://flutter.github.io/assets-for-api-docs/assets/widgets/owl.jpg'),
      )

--------------------------------------------------------------------------------------------------

**3 - IconButton:** Ultilizado como botão com imagem.

**Parametro -** 

    IconButton(
          splashRadius: 100,
          iconSize: 200,
          icon: Ink.image(
            image: const NetworkImage(
                'https://picsum.photos/250?image=9'),
          ),

--------------------------------------------------------------------------------------------------

**4 - Text:** Implementação de Texto.

**Parametro** 

    RichText(
      const TextSpan(text: 'texto'),)

# Tela do grupo de dança - Dinâmica.
![image](https://github.com/IsabelaCSS/Dance-App/assets/128037357/1b831d87-90a7-4545-9a2f-1b73269e9e9e)

Essa tela irá apresentar uma foto do grupo junto,o nome e um botão de favoritos, logo abaixo o nome do lider/gerente, história e turmas disponiveis do grupo. Também será implementado um mapa para a vizualização do endereço para o usuário, um botão de matricular que direcionará para o site de inscrição do grupo, comentários e avaliações do google sobre o local.

### Widgets - Telas do grupo.  
**1 - Container:** Ultilizado para pintar uma parte especifica na tela.

**Parametro** 

    Container(
        color: Colors.black,
        child: Text('Container'),
    );

--------------------------------------------------------------------------------------------------

**2 - Image:** É a implementação de uma imagem.

**Parametro** 

    const Image(
      image: NetworkImage('https://flutter.github.io/assets-for-api-docs/assets/widgets/owl.jpg'),
    )

--------------------------------------------------------------------------------------------------

**3 - Text:** Implementação de Texto.

**Parametro** 

    RichText(
      const TextSpan(text: 'texto'),)

--------------------------------------------------------------------------------------------------

**4 - TextButton:** Ultilizado como botão com um texto.

**Parametro** 

    TextButton(
        style: TextButton.styleFrom(
          primary: Colors.blue,
          ),
          onPressed: () { },
          child: Text('TextButton'),
    )

--------------------------------------------------------------------------------------------------

**5 - IconButton:** Ultilizado como botão com imagem.

**Parametro -** 

    IconButton(
          splashRadius: 100,
          iconSize: 200,
          icon: Ink.image(
            image: const NetworkImage(
                'https://picsum.photos/250?image=9'),
          ),
          
--------------------------------------------------------------------------------------------------

**6 - FlutterMap:** Ultilizado para mapa do google.

**Parametro -** 

        Widget build(BuildContext context) {
          return FlutterMap(
            options: MapOptions(
              initialCenter: LatLng(51.509364, -0.128928),
                 initialZoom: 9.2,
        ),
        children: [
          TileLayer(
            urlTemplate: 'https://tile.openstreetmap.org/{z}/{x}/{y}.png',
            userAgentPackageName: 'com.example.app',
          ),
          RichAttributionWidget(
            attributions: [
              TextSourceAttribution(
                'OpenStreetMap contributors',
                onTap: () => launchUrl(Uri.parse('https://openstreetmap.org/copyright')),
              ),
            ],
          ),
        ],
      );
    }
    
--------------------------------------------------------------------------------------------------

*7 - Scrollbar:** Ultilizado para rolagem de tela.
**Parametro -** 

        Scrollbar(
         child: listView.builder(
             itemCount: 20,
             itemBuilder:(c, i) => MyItem(i).
            ),
        )
        
# Tela QuemSomos - Estática 
![image](https://github.com/IsabelaCSS/Dance-App/assets/128037357/681a1f66-53f2-48f5-89ce-6ff730be03fa)

Essa tela será apresentado as criadoras do aplicativo com seus nomes e fotos, o objetivo e informações sobre a aplicação.

### Widgets - Quem Somos
**1 - Container:** Ultilizado para pintar uma parte especifica na tela.

**Parametro** 

    Container(
        color: Colors.black,
        child: Text('Container'),
    );

--------------------------------------------------------------------------------------------------

**2 - Image:** É a implementação de uma imagem.

**Parametro** 

    const Image(
      image: NetworkImage('https://flutter.github.io/assets-for-api-docs/assets/widgets/owl.jpg'),
    )

--------------------------------------------------------------------------------------------------

**3 - Text:** Implementação de Texto.

**Parametro** 

    RichText(
      const TextSpan(text: 'texto'),)

--------------------------------------------------------------------------------------------------

**4 - IconButton:** Ultilizado como botão com imagem.

**Parametro -** 

    IconButton(
          splashRadius: 100,
          iconSize: 200,
          icon: Ink.image(
            image: const NetworkImage(
                'https://picsum.photos/250?image=9'),
          ),

# Tela Favoritos - Dinâmica 
![image](https://github.com/IsabelaCSS/Dance-App/assets/128037357/ba45f4b8-da1f-418c-a665-5781001d7087)

Essa tela mostrará e salvará os grupos escolhidos como favoritos pelo usuário, assim estabelecendo um histórico de favoritos do usuário.

### Widgets - Favoritos
**1 - IconButton:** Ultilizado como botão com imagem.

**Parametro -** 

    IconButton(
          splashRadius: 100,
          iconSize: 200,
          icon: Ink.image(
            image: const NetworkImage(
                'https://picsum.photos/250?image=9'),
          ),

  --------------------------------------------------------------------------------------------------

**2 - Text:** Implementação de Texto.

**Parametro** 

    RichText(
      const TextSpan(text: 'texto'),)

--------------------------------------------------------------------------------------------------

**3 - Image:** É a implementação de uma imagem.

**Parametro** 

    const Image(
      image: NetworkImage('https://flutter.github.io/assets-for-api-docs/assets/widgets/owl.jpg'),
    )

--------------------------------------------------------------------------------------------------

**4 - Container:** Ultilizado para pintar uma parte especifica na tela.

**Parametro** 

    Container(
        color: Colors.black,
        child: Text('Container'),
    );

# Tela de Cadastro/Login - Dinâmica 
![image](https://github.com/IsabelaCSS/Dance-App/assets/128037357/117cc094-7658-4cd9-89af-e7a23de9451c)

Ambas telas terão o mesmo layout onde irá cadastrar o email e senha do usuário, um botão para prosseguir com o login ou cadastro do usuário.

### Widgets - Login/Cadastro

**1 - Container:** Ultilizado para pintar uma parte especifica na tela.

**Parametro** 

    Container(
        color: Colors.black,
        child: Text('Container'),
    );

 --------------------------------------------------------------------------------------------------

**2 - TextField:** Caixa de texto.

**Parametro** 

    TextField(
      decoration: InputDecoration(
          border: OutlineInputBorder(),
        hintText: 'Enter a search term',
    ),
),

 --------------------------------------------------------------------------------------------------

**3 - IconButton:** Ultilizado como botão com imagem.

**Parametro -** 

    IconButton(
          splashRadius: 100,
          iconSize: 200,
          icon: Ink.image(
            image: const NetworkImage(
                'https://picsum.photos/250?image=9'),
          ),

  --------------------------------------------------------------------------------------------------

**4 - Text:** Implementação de Texto.

**Parametro** 

    RichText(
      const TextSpan(text: 'texto'),)

--------------------------------------------------------------------------------------------------

**5 - TextButton:** Ultilizado como botão com um texto.

**Parametro** 

    TextButton(
        style: TextButton.styleFrom(
          primary: Colors.blue,
          ),
          onPressed: () { },
          child: Text('TextButton'),
    )

# Tela de Perfil - Dinâmica 
![image](https://github.com/IsabelaCSS/Dance-App/assets/128037357/00315f6f-7904-4d82-be0c-f5992e080d41)

Essa tela será onde as informações de login serão mostradas ao usuário, como o nome, email, foto de perfil e foto de fundo. Será implementado um botão para os favoritos do usuário.

### Widgets - Perfil

**1 - TextButton:** Ultilizado como botão com um texto.

**Parametro** 

    TextButton(
        style: TextButton.styleFrom(
          primary: Colors.blue,
          ),
          onPressed: () { },
          child: Text('TextButton'),
    )

  --------------------------------------------------------------------------------------------------

**2 - Text:** Implementação de Texto.

**Parametro** 

    RichText(
      const TextSpan(text: 'texto'),)

--------------------------------------------------------------------------------------------------

**3 - IconButton:** Ultilizado como botão com imagem.

**Parametro -** 

    IconButton(
          splashRadius: 100,
          iconSize: 200,
          icon: Ink.image(
            image: const NetworkImage(
                'https://picsum.photos/250?image=9'),
          ),
          
--------------------------------------------------------------------------------------------------

**4 - Container:** Ultilizado para pintar uma parte especifica na tela.

**Parametro** 

    Container(
        color: Colors.black,
        child: Text('Container'),
    );

--------------------------------------------------------------------------------------------------

**5 - Image:** É a implementação de uma imagem.

**Parametro** 

    const Image(
      image: NetworkImage('https://flutter.github.io/assets-for-api-docs/assets/widgets/owl.jpg'),
      )
