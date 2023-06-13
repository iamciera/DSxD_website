---
title: ¿Cómo documentar un proyecto tecnológico con cómics?
date: 2023-08-02 01:00:00
description: Julia Evans
featured_image: /assets/img/theme/Evans_Figure1.jpeg
locale: sp
uid: tech-comics
---

{% include language-selector.html %}

De vez en cuando, recibo correos electrónicos de gente que me dice básicamente: "¡Hola Julia! ¡Tenemos un proyecto de código abierto! ¡Nos gustaría utilizar cómics/revistas/arte para documentar nuestro proyecto! ¿Podemos contratarte?"

Spoiler: La respuesta es "No, no podéis contratarme"; no hago encargos. Pero creo que es una idea genial, y a menudo he deseado tener algo más útil que decir a la gente que "No", así que si le interesa, ¡aquí tiene algunas ideas sobre cómo conseguirlo!

<center>
<figure>
	<img src="../assets/img/theme/Evans_Figure1.jpeg" alt="Zine de seis paneles de Julia Evans (Twitter @b0rk) sobre el software de chat Zulip. El primer panel afirma que 'Zulip tiene canales, algo así como Slack'. El segundo panel explica que 'cada canal está organizado en hilos'. El tercer panel muestra cómo 'ponerse al día es más fácil con Zulip' con una persona que piensa: 'Leeré la discusión sobre el cálculo lambda e ignoraré el resto'. El panel señala que ya no hay notificaciones de más de 100 mensajes sin leer en Slack. El cuarto panel dice al lector que 'puede responder fácilmente a un mensaje horas más tarde'. El quinto panel le dice al lector que Zulip es de código abierto y que pueden 'pagar por un Zulip alojado en zulipchat.com (u obtener más información al respecto)'. El último panel da el enlace al servicio (chat.zulip.org) y tiene una figura de palo de Julia diciendo: 'Llevo 4 años usándolo todos los días y me encanta'.">
    Cómic Zulip de Julia
</figure>
</center>

##### Los cómics sin buena información no sirven para nada

Normalmente, cuando la gente me pregunta: "Oye, ¿podríamos hacer un cómic que explique X?", no parece que tengan una idea clara de qué información quieren transmitir exactamente; sólo tienen una vaga idea de que quizá sería genial dibujar algunos cómics. Esto tiene sentido: ¡descubrir qué información sería útil contar a la gente es todo un reto! Ése es probablemente el 80% de mi tiempo cuando hago cómics.

Debería pensar en los cómics del mismo modo que en cualquier tipo de documentación. Empiece por la información que quiere transmitir, su público objetivo y cómo quiere distribuirla (¿Twitter? ¿En su página web? ¿En persona?), y después piense cómo ilustrarla. :) La información es lo principal, ¡no el arte!
Una vez que tenga claro lo que quiere transmitir, ¡puede empezar a pensar en cómo representarlo mediante ilustraciones!

##### Céntrese en los conceptos que no cambian

Dibujar cómics es una inversión mucho mayor que escribir documentación —me lleva
como, cinco veces más tiempo transmitir la misma información en un cómic que por escrito— ¡así que utilícelo sabiamente! Dado que no es tan fácil editar el arte, si va a convertir algo en un cómic, querrá centrarse en conceptos que es muy poco probable que cambien. Así que, ¡hable de las ideas centrales de su proyecto en lugar de los argumentos exactos de la línea de comandos que lleva!

Aquí tiene un par de opciones sobre cómo podría utilizar los cómics/ilustraciones para documentar su proyecto.

##### Opción 1: un único gráfico

Un formato que podría probar es un único gráfico pequeño que explique de qué trata su proyecto y por qué podría interesar a la gente. Por ejemplo: Zulip comic1.

Se trata de algo breve que podría publicar en Twitter o imprimir como panfleto para repartir en persona. El contenido informativo aquí probablemente sería básicamente lo que hay en la página de inicio de su proyecto, pero presentado de una forma más divertida y emocionante. :)

Puede volcar una cantidad bastante pequeña de contenido en un solo cómic. Con ese cómic de Zulip, los fragmentos de información que elegí fueron:

- Zulip es algo así como Slack, pero con hilos de conversación.
- Es fácil seguir los hilos aunque la conversación se desarrolle a lo largo de varios días.
- Es mucho más fácil ponerse al día de forma selectiva con Zulip.
- Zulip es de código abierto.
- Hay un servidor Zulip abierto que puede probar.

¡No es mucha información! Son sólo cincuenta palabras, así que para hacerlo con eficacia, tiene que destilar su proyecto hasta reducirlo a cincuenta palabras de forma que siga siendo útil. No es fácil.

##### Opción 2: muchos cómics

Otro enfoque es hacer un cómic/ilustración más en profundidad, como la Guía de Google sobre Kubernetes2 o La Guía Infantil Ilustrada de Kubernetes3.
Para ello, necesita un concepto mucho más sólido que "Uh, quiero explicar nuestro proyecto": ¡quiere tener en mente un público objetivo claro! Por ejemplo, si estuviera dibujando un conjunto de cómics sobre Docker, probablemente me centraría en la gente que quiere utilizar Docker en producción. Por tanto, querría hablar de

- Publicar sus contenedores en un registro público/privado
- Algunas buenas prácticas para etiquetar sus contenedores
- Cómo asegurarse de que sus hosts no se quedan sin espacio en disco por descargar demasiados contenedores
- Cómo utilizar capas para ahorrar espacio en disco/descargar menos cosas
- Si es razonable ejecutar los mismos contenedores en producción y en desarrollo

¡Eso es totalmente distinto del juego de cómics que escribiría para la gente que sólo quiere usar Docker para desarrollar localmente!

##### Opción 3: Un fanzine impreso

Un fanzine es un folleto corto autoeditado, normalmente impreso de forma bastante barata, como una pequeña revista.

Lo que lo diferencia de la opción 2 es que los fanzines se imprimen. Por eso, para que este proyecto tenga sentido, necesita tener un lugar donde repartir los ejemplares impresos. Por ejemplo, ¿quizá vaya a presentar su proyecto en una conferencia importante? ¿Quizá vaya a impartir talleres sobre su proyecto y quiera repartir el fanzine como apuntes? ¿Quizá quiera enviársela por correo a la gente?

##### Cómo contratar a alguien que le ayude

Existen básicamente tres formas de contratar a alguien que le ayude a crear un gráfico, un cómic o un fanzine:

1. Contrate a alguien que entienda (o pueda aprender rápidamente) la tecnología que desea documentar y que sepa ilustrar bien. Sin embargo, no conozco a nadie a quien pueda contratar para hacer esto, así que probablemente no sea la mejor opción. Hay muy pocas personas en la intersección de "tener un gran conocimiento de la tecnología", "ser bueno escribiendo" y "estar disponible para trabajar como autónomo".
2. Colabore con un ilustrador para que se lo dibuje. La cuestión principal aquí es que si no le da al ilustrador explicaciones claras de su tecnología para que trabaje con ella, no acabará teniendo una explicación clara y útil. Por lo que he visto, la mayoría de la gente invierte poco en escribir explicaciones claras para sus ilustradores; he visto unos cuantos cómics tecnológicos realmente adorables que no me parecen útiles ni claros en absoluto. Me encantaría que más gente hiciera un mejor trabajo en este sentido. ¿Qué sentido tiene tener una ilustración adorable si en realidad no enseña nada a nadie?
3. Dibújelo usted mismo. Esto es lo que yo hago, obviamente. :) ¡Los muñecos de palitos están bien!
   La mayoría de la gente parece utilizar la opción 2. En realidad no conozco a ningún técnico que haya encargado cómics, ¡aunque estoy seguro de que ha ocurrido! Creo que colaborar con artistas es una gran opción, y me encantaría que más gente lo hiciera. ¡Pagar a los ilustradores es realmente divertido!

**Bio:**

Julia Evans es desarrolladora de software y creadora de Wizard Zines, una colección de fanzines de programación dibujados a mano y centrados en fundamentos libres de jerga. El último fanzine de la colección es La Guía de Bolsillo para Depurar.

Referencias:

1. Evans, Julia. zulip: software de chat que me encanta. Twitter [https://twitter.com/b0rk/status/986444234365521920](https://twitter.com/b0rk/status/986444234365521920) (2018).
2. Despliegue el código más rápido: con CI/CD y Kubernetes. Google Cloud [https://cloud.google.com/kubernetes-engine/kubernetes-comic](https://cloud.google.com/kubernetes-engine/kubernetes-comic).
3. La Guía Infantil Ilustrada de Kubernetes. Cloud Native Computing Foundation [https://www.cncf.io/phippy/the-childrens-illustrated-guide-to-kubernetes/](https://www.cncf.io/phippy/the-childrens-illustrated-guide-to-kubernetes/).
