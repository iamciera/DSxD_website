---
title: "Nuestra Historia: Los derechos globales de los queer a través de una lente histórica colonial"
date: 2023-07-05 00:00:00
description: Melissa Kagen
featured_image: /assets/img/theme/dickinson_header.png
locale: sp
uid: global-queer-rights
---

{% include language-selector.html %}

Al igual que en Estados Unidos, el colonialismo británico ha proyectado una larga sombra de violencia colonial sobre la homosexualidad en todo el mundo. Como persona interesada en los derechos comparados de las personas queer a nivel mundial, considerar este contexto histórico me hizo preguntarme sobre la relación entre los derechos LGBTQ+ en la actualidad y el legado del colonialismo británico.

Antes de profundizar, quiero ante todo reconocer que la colonización empezó destruyendo las culturas indígenas y que debería terminar mejorándolas. Como descendiente de colonizadores, siento que es importante para mí estar al servicio de los líderes indígenas para intentar reparar lo que está roto. El futuro de la liberación queer debería centrarse en los movimientos queer indígenas de todo el mundo.

En 2009, cuando Uganda (miembro de la Commonwealth británica) presentó un proyecto de ley que prohibía cualquier forma de sexo homosexual y la "promoción de las relaciones sexuales", la protesta mundial no se hizo esperar. El entonces primer ministro británico, David Cameron, declaró que todos los países que recibían ayuda del Reino Unido debían "adherirse a los derechos humanos", sugiriendo que habría algún impacto en la ayuda futura como resultado de la decisión de Uganda.

Aunque no descarto la homofobia de Estado de Uganda, el duro juicio procedente de las pasadas potencias coloniales que originaron estas leyes es irrisorio, dadas sus historias de poder directo e indirecto sobre sus leyes y prácticas. Quiero oponerme a la narrativa de la supuesta "inferioridad moral" de estos países utilizando datos para hacer hincapié en la causa histórica de fondo: El colonialismo europeo y el código penal británico.

<center>
<figure>
	<img src="../assets/img/theme/dickinson_figure1.png" alt="Un globo terráqueo en el que los países están coloreados a rayas arco iris. Alrededor del globo hay esbozos de visualizaciones de datos como un gráfico de barras y un diagrama de líneas. Los anillos, que recuerdan a un monitor de fitness, están parcialmente completados van camino de una marca del 100%.">
</figure>
</center>

## Empezar a construir un conjunto de datos

Para comprender la historia de la homofobia y la transfobia mundiales, busqué una medida de los derechos de los homosexuales por países, así como una medida para aproximarme a la influencia del colonialismo en la actualidad.
Investigué la historia de las leyes contra la sodomía —leyes contra los actos sexuales considerados "antinaturales o inmorales"— y el uso del código penal británico. Después construí un conjunto de datos de cuándo se introdujeron esas leyes para cada uno de los cincuenta y cinco países de la Commonwealth británica y añadí las fechas en que esos países de la Commonwealth fueron formalmente colonizados.

Empecé con un conjunto de datos del Barómetro Global de los Derechos de los Gays (GBGR®) y del Barómetro Global de los Derechos de los Transexuales (GBTR™) de Franklin & Marshall. Franklin y Marshall utilizaron veintisiete factores para su GBGR y quince factores para su GBTR para determinar la puntuación gay o trans de un país, que oscila entre 0 y 1. Algunos de estos factores incluyen la protección ante la ley, la protección civil, la defensa de los derechos LGBT, los derechos socioeconómicos y la persecución social. Además, busqué en documentos de investigación, en la Enciclopedia Británica, en los informes sobre homofobia de Estado de la Asociación Internacional de Lesbianas y Gays (ILGA) y, a veces, en Wikipedia como último recurso cuando no podía encontrar la información en ningún otro sitio...

## Comprender los datos justifica un enfoque iterativo

Al principio, utilicé el "año de la independencia" como medida del tiempo transcurrido lejos de la influencia británica. Esta información era fácil de encontrar, ya que los países tienen días festivos en torno a estas fechas, pero a medida que pensaba más en ello, me di cuenta de que el año de independencia por sí solo no puede abordar la historia de las leyes dirigidas a las personas queer. Así que cambié de orientación. En su lugar, opté por investigar las fechas de introducción de los códigos penales, así como las fechas originales de la colonización oficial, para captar mejor la historia de los países.

Encontrar la fecha de la colonización oficial fue un asunto complicado, ya que cada país tiene un pasado diferente. Por ejemplo, países como Kenia y la India fueron colonizados primero por empresas, no por gobiernos oficiales, y por ello tuve que decidir qué aspecto tiene la colonización "oficial". Decidí elegir las fechas en las que la potencia colonial estableció algún tipo de gobierno oficial en esos países. Aparte de eso, algunos países tienen historias coloniales en las que cambiaron de poder en poder. Es el caso de Sudáfrica, por ejemplo, que osciló entre el colonialismo británico y el holandés. En esta situación, generalmente elegí el gobierno colonial establecido más antiguo. Por último, también dejé que la fecha de introducción de los códigos penales guiara la fecha de colonización, ya que una ratificación oficial del gobierno solía ir seguida de una introducción del código penal.

## La exploración inicial de datos conduce a más preguntas

Creé algunos gráficos iniciales con ggplot2 en R (Figura 1) para explorar la relación entre las fechas de introducción de las leyes sobre la sodomía y las fechas de colonización. Mi hipótesis inicial no estaba necesariamente respaldada por los datos preliminares, pero al visualizar los datos observé otras tendencias.

Por ejemplo, un diagrama de dispersión de las puntuaciones GBGR® muestra tres agrupaciones: países con puntuaciones bajas, medias y altas. Aunque inicialmente sólo había considerado la relación entre los derechos de los homosexuales y el tiempo transcurrido desde la colonización, estas agrupaciones pueden orientar otras preguntas e investigaciones. ¿Cuáles son las historias que distinguen a estos grupos y qué pueden decirnos sobre las repercusiones en la actualidad? ¿En qué se diferencian los derechos de los transexuales y los derechos de los homosexuales en estos países? ¿Cómo podrían verse influidos esos derechos en el futuro con el aumento de la visibilidad trans? ¿Qué hay de otras potencias coloniales? Este conjunto de datos también podría ampliarse para incluir países colonizados por otros países europeos. ¿En qué se parecen y en qué se diferencian sus legados del colonialismo? Está claro que queda mucho trabajo por hacer en este espacio. El conjunto de datos se comparte en Github1, e invito a otros a aportar sus propios enfoques y preguntas al respecto. Agradecimientos a AT Craig por la idea inicial que puso en marcha este proyecto.

**Bio:**

EB Dickinson es miembro del Servicio AmeriCorps VISTA de Política y Defensa de la Alianza para Escuelas Seguras de Illinois. Es licenciada en ecología con especialización en arte y música por la Universidad de Georgia. Está interesada en la intersección entre la visualización de datos, la cartografía y los derechos LGBTQ+ en todo el mundo. En su tiempo libre, le gusta tocar el bajo y espera producir algún día un álbum funk sobre bueyes almizcleros. Puede ponerse en contacto con ella en ebaydickinson@gmail.com.

En el margen lateral / Referencias

1. DSxD Vol II Book. Github. Accedido el 1 de febrero de 2023. [https://github.com/ebaydickinson/Our-History-Global-Queer-Rights-Through-a-Historical-Colonial-Lens](https://github.com/ebaydickinson/Our-History-Global-Queer-Rights-Through-a-Historical-Colonial-Lens).
