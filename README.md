# PROJETO-BD-GOT-M4

<img src="./images/got-project.png">

<h2>Descrição</h2>

<p>Projeto do Módulo 4 do curso Programador Web Full Stack Resilia SENAC com o objetivo de utilizar um banco de dados existente e analisar seus dados através de gráficos.</p>

<h2>Sobre a série</h2>
<p>"Situada nos continentes fictícios de Westeros e Essos, a série centra-se no Trono de Ferro dos Sete Reinos e segue um enredo de alianças e conflitos entre as famílias nobres dinásticas, seja competindo para reivindicar o trono ou lutando por sua independência."</p>

<h2>Dados que recebemos e cruzamos:</h2>
<ul>
<li>personagens</li>
<li>episódios</li>
<li>casas</li>



<h2>Perguntas e Respostas:</h2>


1) Em que regiões se concentram a maioria das casas?<br>
SELECT houses.Region, COUNT(houses.House_name) as Frequence
FROM houses
WHERE houses.Region = houses.Region
GROUP BY houses.Region
ORDER BY COUNT(houses.House_name) DESC
LIMIT 10;

2) Quais foram os episódios mais vistos?<br>
SELECT episodes.Title, episodes.US_Viewers AS Views
FROM episodes
ORDER BY episodes.US_Viewers DESC
LIMIT 5;

3) Quais foram os melhores episódios em avaliação?<br>
SELECT * FROM episodes ORDER BY Rating DESC

4) Quais atores permanecem na série desde o ano de estreia?<br>
SELECT * FROM episodes ORDER BY Rating DESC
e
SELECT Season,Episode, Title, Rating FROM episodes
ORDER BY Rating DESC

5) Qual temporada foi mais votada e melhor avaliada?<br>
