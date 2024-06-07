<template>
  <div>
    <div class="categories-nav">
      <div
        class="category-item"
        v-for="(category, index) in categories"
        :key="index"
        @click="currentCategory = category.name"
        :class="{ active: currentCategory === category.name }"
      >
        <span class="material-icons">{{ category.icon }}</span>
        <span class="category-name">{{ category.name }}</span>
      </div>
    </div>
    <div v-if="currentCategory === 'Cómo funcionan los puntos'">
      <p class="info-text">Consigue puntos por comprar o por contribuir en la Comunidad Steam. Usa tus puntos para personalizar tu presencia en Steam o premia a otros miembros de la Comunidad.<br>

          109 puntos por cada 1,00€ que gastes.
          Compra cualquier juego, DLC, hardware, aplicación, banda sonora o artículo del juego y obtén puntos.<br>

          La tienda de puntos es donde encontrarás una variedad de artículos para personalizar tu presencia en Steam. Canjea tus puntos por artículos de perfil o chat.<br>

          Los avatares animados, marcos, fondos, insignias y artículos de chat que obtienes son tuyos para siempre.<br>
          La tienda de puntos está aquí para quedarse, ahora abierta todo el año.<br>
          Los artículos de la tienda de puntos no se pueden comercializar ni intercambiar.
      </p>

      <p class="info-text">
        <b>ARTÍCULOS DE LOS JUEGOS QUE JUEGAS</b><br>
        ¿Quieres un emoticono de tu juego favorito? Puedes canjear tus puntos para obtener un fondo o un emoticono para juegos que ya tienes.<br>
        Los emoticonos y fondos que estaban anteriormente relacionados con cromos pueden ahora adquirirse directamente usando puntos de Steam. No te preocupes, todavía puedes usar la fabricación de cromos de Steam para conseguir esos artículos si lo deseas.
      </p>

      <p class="info-text">
        <b>PREMIOS DE LA COMUNIDAD</b><br>
        Usa tus puntos para destacar —con un premio— reseñas, perfiles, mensajes en foros de discusión y contenido generado por los usuarios en Steam. El premio aparecerá donde todos lo vean y le dará al colaborador un donativo de 100 puntos o más.<br>

        A veces lees una reseña que te resulta útil, te parece única o simplemente está tan bien escrita que te dan ganas de estrecharle la mano a esa persona. Ahora puedes reconocer su trabajo otorgándole un premio.
        Busca juegos y lee algunas reseñas.<br>

        Algunos contenidos generados por los usuarios son tan geniales que los quieres imprimir, enmarcar y colgar en la pared. Ahora también puedes reconocer ese artículo del Workshop, captura de pantalla o guía otorgándole un premio.
        Visita el Workshop.<br>

        ¿Te ha impresionado el perfil de otro jugador? ¿Sorprendido con lo perspicaz de sus publicaciones en el foro de discusión? Ahora puedes usar puntos para recompensar y reconocer perfiles de jugador de Steam y publicaciones de los foros.<br>
      </p>

      <p class="info-text">
        <b>PREGUNTAS FRECUENTES</b><br>
        ¿Cómo puedo obtener puntos de Steam?<br>
        Cada vez que hagas una compra en Steam se te darán puntos de Steam en función de cuánto hayas gastado. Primero convertiremos esta cantidad a USD, y luego se convertirá directamente a la cantidad de puntos que recibirás.
        No recibirás ningún punto por añadir fondos a tu Cartera de Steam ni por las compras en el Mercado de la Comunidad Steam.
        También puedes obtener puntos de Steam si alguien de la Comunidad otorga un premio a una de tus reseñas de usuario u otro contenido que hayas subido (por ejemplo, capturas de pantalla, guías o artículos del Workshop).<br>

        ¿Caducan los puntos de Steam?<br>

        ¡No! Además la tienda de puntos está aquí para quedarse. Ahora permanecerá abierta todo el año.<br>
        En eventos de rebajas anteriores, algunos de estos artículos expiraron después de un cierto período de tiempo o tuvieron un número limitado de usos. ¿Sigue siendo el caso?<br>
        Los artículos de la tienda de puntos te los puedes quedar para siempre y usar ilimitadamente, con la excepción del perfil especial de temporada, que lo puedes mostrar durante un máximo de 30 días desde el momento de la compra.<br>

        ¿Puedo intercambiar o vender los artículos que obtengo de la tienda de puntos?<br>

        No, todos los artículos de la tienda de puntos están vinculados a tu cuenta y no se pueden transferir a otras.<br>

        ¿Cuál es la diferencia entre esto y los cromos de Steam?<br>

        Ahora puedes canjear tus puntos de Steam por emoticonos y fondos de perfil relacionados con los juegos que posees. El programa de puntos de Steam está basado en el existente sistema de cromos, haciéndolo accesible a más jugadores. Además de coleccionar y crear cromos, el programa de puntos ofrece ahora otra, más directa, manera de adquirir estos emoticonos y fondos.<br>

        ¿Qué va a pasar con los cromos de Steam? ¿Se van a quitar?<br>

        ¡No! Sabemos que la gente disfruta coleccionando cromos de Steam y creando insignias, por lo que no hay planes de eliminarlos por el momento.<br>

        ¿Qué ocurre con mis puntos de Steam cuando devuelvo un juego?<br>

        Cuando devuelves un juego, los puntos que ganaste con esa compra se deducirán de tu cuenta. Si eso hace que tu saldo de puntos sea negativo, también eliminaremos los artículos más recientes y los premios de la Comunidad (y donativos relacionados) para los que hayas utilizado puntos hasta que tu saldo ya no sea negativo.<br>

        No he canjeado todas mis fichas del Año Nuevo lunar 2020. ¿Qué pasa con ellas?<br>

        Los puntos que hayas adquirido y no hayas canjeado durante el último evento de temporada se pierden. Pero se te han concedido puntos por cualquier compra que hicieras en Steam desde que acabó el Año Nuevo lunar de 2020.<br>

        Oye, he notado que mi perfil de Steam se ve un poco diferente. ¿Qué ha cambiado?<br>

        Hemos actualizado algunos de los estilos de los perfiles de Steam y te hemos dado la posibilidad de seleccionar temas de colores para aún más opciones de personalización.<br>

        ¿Para qué más puedo usar mis puntos?<br>

        Si no encuentras nada que quieras en la tienda de puntos, siempre puedes usar tus puntos para conceder un premio a una reseña de usuario, mostrando a otros lo valiosa que crees que es esa reseña. Este premio se mostrará públicamente en la reseña y el autor también recibirá algunos puntos de Steam.
        De manera similar, también puedes usar tus puntos para otorgar un premio a otros tipos de contenido generado por el usuario, incluidos artículos del Workshop, guías, capturas de pantalla y vídeos.<br>
        También planeamos expandir el conjunto de cosas en las que puedes usar tus puntos en el futuro.
      </p>

    </div>
    <div v-else><ArticleCard_1_2 /></div>
  </div>
</template>

<script>
import ArticleCard_1_2 from '@/components/ArticleCard_1_2.vue';

export default {
  components: {
    ArticleCard_1_2,
  },
  data() {
    return {
      categories: [
        { name: 'Destacados', icon: 'star' },
        { name: 'Interfaz', icon: 'desktop_windows' },
        { name: 'Perfil', icon: 'person' },
        { name: 'Chat', icon: 'chat' },
        { name: 'Cómo funcionan los puntos', icon: 'help' },
      ],
      currentCategory: 'Destacados',
    };
  }
};
</script>

<style postcss>
@import url('https://fonts.googleapis.com/css2?family=Cairo:wght@400;700&display=swap');
@import url('https://fonts.googleapis.com/icon?family=Material+Icons');

.categories-nav {
  display: flex;
  justify-content: space-around;
  align-items: center;
  color: #2B2B2B;
  padding: 20px;
  margin: 20px 0;
}

.category-item {
  display: flex;
  align-items: center;
  gap: 10px;
  cursor: pointer;
  transition: color 0.3s ease, border-bottom 0.3s ease;
  position: relative;
}

.category-item:hover,
.category-item.active {
  color: #C714E4;
}

.category-item::after {
  content: '';
  position: absolute;
  bottom: -5px;
  left: 0;
  width: 100%;
  height: 2px;
  background-color: #C714E4;
  opacity: 0;
  transform: scaleX(0);
  transition: opacity 0.3s ease, transform 0.3s ease;
}

.category-item:hover::after,
.category-item.active::after {
  opacity: 1;
  transform: scaleX(1);
}

.material-icons {
  font-size: 30px;
}

.category-name {
  font-size: 1.2rem;
}

.info-text {
  padding: 20px;
  font-size: 1.1rem;
  color: #000000;
}

@media only screen and (max-width: 768px) {
  .categories-nav {
    flex-direction: column;
    gap: 10px;
  }

  .category-item {
    gap: 10px;
  }

  .material-icons {
    font-size: 25px;
  }

  .category-name {
    font-size: 1rem;
  }
}
</style>
