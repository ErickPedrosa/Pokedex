
<img src="https://img.shields.io/static/v1?label=Status&message=Finished&color=FFCB05&style=lat-square&logo=POKEMON"/> <img src="https://img.shields.io/static/v1?label=Version&message=v1.2&color=FF3333&style=lat-square&logo=POKEMON"/> <img src="https://img.shields.io/static/v1?label=License&message=MIT&color=33DD33&style=lat-square&logo=POKEMON"/>    

<br>

<h1 align="center">
    <a href="https://erickpedrosa.github.io/Pokedex/">🔗 Pokédex</a>
</h1>

<p align="center">Uma pokédex completa que permite procurar por um pokémon especifico e saber de suas informações, como abilidades e fraquezas.</p>    

<br>
<br>

<p align="center">
 <a href="#objetivo">Objetivo</a> •
 <a href="#desenvolvimento">Desenvolvimento</a> •
 <a href="#status">Status do Projeto</a> •
 <a href="#funcionamento">Features</a> • 
 <a href="#tecnologias">Tecnologias</a> • 
 <a href="#licenca">Licença</a> • 
 <a href="#autor">Autor</a>
</p>

<br>
<br>

<h2 id="objetivo">Objetivos</h2>
<p>Esse projeto foi desenvolvido para um uso recreativo e de aprendizagem, o projeto surgiu baseado em um outro que eu fiz que seguia o vídeo do canal Manual do Dev, que se utilizava de uma API para construir uma pokédex bem simples.</p>
<p><a href="https://www.youtube.com/watch?v=SjtdH3dWLa8" target="_blank">Link do vídeo</a></p>
<p><a href="https://github.com/ErickPedrosa/Pokedex-Manual-Do-Dev" target="_blank">Link do projeto realizado</a></p>
<p><a href="https://pokeapi.co/" target="_blank">Link da API utilizada</a></p>
<br>

<p>Por mais que eu tenha achado esse projeto do vídeo muito legal, como uma pessoa que gosta bastante da franquia pokémon senti falta de algumas informações que na minha opinião eram fundamentais para uma pokédex de verdade.</p>
<p>Então decidi refazer o projeto implementando essas features que eu achava necessarias. Comecei montando o design de como a página deveria ser no Figma, fiz um design bem simples como era minha primeira vez utilizando o Figma, além de querer que o projeto fosse o mais minimalista possível, sem muita poluição visual e de fácil utilização.</p>
<p><a href="https://www.figma.com/file/LI8pT0x2keOQFTYbfG5Kck/Pokedex?node-id=2%3A4&t=anoEE9nvZjemOZQ9-1" target="_blank">Link design no Figma</a></p>
<br>

<p>Então baseado nesse design, no projeto anterior, na pokeAPI e nas funcionalidades que eu pretendia implementar comecei a desenvolver o projeto.</p>

<br>
<br>

<h2 class="desenvolvimento">Desenvolvimento</h2>
<h3>Versão v1.0 - O início de tudo</h3>
<p>Começando do projeto fiz rapidamente o html e fiz boa parte do css (deixei um pouco de lado a responsividade e me foquei apenas na estilização para desktops, pois era onde eu estava desenvolvendo o projeto).</p>
<p>Logo voltei-me para o js, com base no projeto anterior já tinha algumas funções que eu acabei reutilizando, como a de renderizar a imagem, o nome e o id do pokemon, então quando acabei de adaptá-las para o novo projeto voltei-me para outras funcionalidades ainda não realizadas, algumas foram bem fáceis porque se baseavam nos mesmos princípios que as já implementadas, como a funcionalidade que gera a altura, o peso e as abilidades de um pokémon.</p>
<p>Então rapidamente acabei de implementá-las e finalmente estava pronta a primeira versão da Pokédex. Ainda com algumas features faltando, mas estava funcional.</p>
<br>

<h3>Versão v1.1 - Terminando as features necessárias</h3>
<p>Após terminar a primeira versão, me foquei em terminar as features que faltavam, que eram:</p>
<ul>
    <li>Renderizar o tipo do pokémon.</li>
    <li>Calular as fraquezas e vantegens de um tipo</li>
    <li>Renderizar as fraquezas e vantegens de um pokémon</li>
</ul>
<p>A primeira feature foi relativamente fácil, pois só tive que ler a documentação da API para fazê-la, foi bem rápida.</p>
<p>Já quando comecei a realizar a segunda, me deparei com a primeira grande dor de cabeça desse projeto, a feature que calcula as fraquezas e vantagens de um pokémon, gastei bastante tempo nessa feature para fazê-la funcionar. A API não devolvia nada que continha as fraquezas do pokémon, mas reparei que havia um request que devolvia as informações sobre um determinado tipo, incluindo informações como "Recebe o dobro de dano de um determinado tipo", então tive que utilizar isso e um sistema de pesos para cada resposta para calcular o dano total. Depois de finalmente conseguir calibrar o sistema de pesos corretamente, o que me deu bastante trabalho pois um pokémon pode ter mais de um tipo o que complicou um pouco o cálculo, a feature estava pronta.</p>
<p>A terceira feature foi de longe a que me causou mais problemas, como as funções que dependiam da API eram assíncronas, inclusive a de cálculo, quando eu chamava a função ela me devolvia um Array incializado com 1, que o padrão, quando eu estava esperando o Array com os danos já cálculados. O que acontecia era que acabava por não renderizar nada já que ele devolvia o Array antes dele calcular, a forma que encontrei de solução foi utilizar um setTimeout para fazer a função de renderização esperar o cálculo terminar e só então tentar renderizar as fraquezas e vantagens. <strong>Obs: Não sei se essa foi a melhor forma de contornar esse problema, inclusive gera um pequeno bug, em que ele não renderiza as fraquezas mas para voltar para o normal é só ir para o próximo pokémon e então voltar para o anterior.</strong></p>
<br>

<h3>Versão v1.2 - Responsividade</h3>
<p>Com o projeto praticamente acabado, nessa versão eu apenas dediquei-me a estilizar o projeto e melhorar sua responsividade, já que ele estva quebrando completamente em telas menores que 600px.</p>
<p>Também acabei adicionando uma nova feature que eu não havia programado que foi a do botão de pesquisar, que te permite achar um pokémon por seu nome ou id.</p>

<br>
<br>

<h2 id="status">Status do Projeto</h2>
<p>O projeto atualmente se encontra concluído e está atualmente na sua versão 1.2, embora pretenda daqui a algum tempo retomá-lo para adicionar novas features.</p>

<br>
<br>

<h2 id="funcionamento">Funcionamento</h2>

<br>
<br>

<h2 id="tecnologias">Tecnologias</h2>

<br>
<br>

<h2 id="autor">Autor</h2>

