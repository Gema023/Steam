<template>
  <div class="games-grid">
    <div v-for="(game, index) in games" :key="index" class="game-item" @click="openGameModal(game)">
      <img :src="game.image" :alt="game.name" />
      <div class="overlay">
        <h3>{{ game.name }}</h3>
        <div class="overlay_info">
          <div class="icons">
            <h3>Tipo de artículo</h3>
          </div>
          <div class="prices">
            <span class="original-price">{{ game.originalPrice }}</span>
            <span class="discounted-price">{{ game.discountedPrice }}</span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      currentIndex: 0,
      games: [
        {
          image: '/article_1_2.svg',
          name: 'Nombre del artículo',
          discountedPrice: '100Pts.',
        },
        {
          image: '/article_1_2.svg',
          name: 'Nombre del artículo',
          discountedPrice: '100Pts.',
        },
        {
          image: '/article_1_2.svg',
          name: 'Nombre del artículo',
          discountedPrice: '100Pts.',
        },
        {
          image: '/article_1_2.svg',
          name: 'Nombre del artículo',
          discountedPrice: '100Pts.',
        },
        {
          image: '/article_1_2.svg',
          name: 'Nombre del artículo',
          discountedPrice: '100Pts.',
        },
        {
          image: '/article_1_2.svg',
          name: 'Nombre del artículo',
          discountedPrice: '100Pts.',
        },
        {
          image: '/article_1_2.svg',
          name: 'Nombre del artículo',
          discountedPrice: '100Pts.',
        },
        {
          image: '/article_1_2.svg',
          name: 'Nombre del artículo',
          discountedPrice: '100Pts.',
        },
        {
          image: '/article_1_2.svg',
          name: 'Nombre del artículo',
          discountedPrice: '100Pts.',
        },
        {
          image: '/article_1_2.svg',
          name: 'Nombre del artículo',
          discountedPrice: '100Pts.',
        },
        {
          image: '/article_1_2.svg',
          name: 'Nombre del artículo',
          discountedPrice: '100Pts.',
        },
        {
          image: '/article_1_2.svg',
          name: 'Nombre del artículo',
          discountedPrice: '100Pts.',
        },
        {
          image: '/article_1_2.svg',
          name: 'Nombre del artículo',
          discountedPrice: '100Pts.',
        },
        {
          image: '/article_1_2.svg',
          name: 'Nombre del artículo',
          discountedPrice: '100Pts.',
        },
        {
          image: '/article_1_2.svg',
          name: 'Nombre del artículo',
          discountedPrice: '100Pts.',
        },
        {
          image: '/article_1_2.svg',
          name: 'Nombre del artículo',
          discountedPrice: '100Pts.',
        },
      ],
    };
  },
};
</script>

<style postcss>
h2 {
  font-family: 'Cairo', sans-serif;
  font-weight: bold;
  font-size: 26px;
}

h3 {
  font-weight: bold;
  font-size: 20px;
  margin-bottom: 10px;
}

.ver-todos-container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1.4em;
  margin: 1em 0;
}

.ver-todos-link {
  color: #C714E4;
  text-decoration: none;
  font-family: 'Cairo', sans-serif;
  font-weight: lighter;
  font-size: 18px;
}

.ver-todos-link:hover {
  text-decoration: underline;
}

.games-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 20px;
  padding: 20px;
}

.game-item {
  position: relative;
  box-sizing: border-box;
}

.game-item img {
  width: 100%;
  height: auto;
}

.overlay {
  height: 114px;
  background-color: #FFFFFF;
  color: #2B2B2B;
  padding: 10px;
  border: 2px solid #2B2B2B;
  border-radius: 0 0 40px 40px;
  padding: 12px 12px 12px 24px;
}

.overlay:hover {
  background-color: #C714E4;
  color: #ffffff;
  border: 2px solid #C714E4;
}

.overlay h3 {
  margin: 0;
  font-size: 18px;
}

.overlay_info {
  display: flex;
  flex-direction: row;
  justify-content: start;
  align-content: center;
  margin-top: 16px;
  font-size: 16px;
  gap: 80px;
}

.icons {
  display: flex;
  justify-content: space-between;
  margin-top: 5px;
  gap: 14px;
}

.icon {
  font-family: 'Material Icons';
  font-size: 24px;
  color: #2B2B2B;
  cursor: pointer;
  transition: color 0.3s, background-color 0.3s;
}

.icon:hover {
  color: #FF0000;
}

.icon.active {
  background-color: #FF0000;
}

.prices {
  display: flex;
  margin-top: 5px;
  max-width: 29px;
}

.original-price {
  font-family: 'Cairo', sans-serif;
  font-weight: lighter;
  font-size: 16px;
  text-decoration: line-through;
  color: #2B2B2B;
  margin-right: 10px;
}

.original-price:hover {
  color: #ffffff;
}

.discounted-price {
  font-family: 'Cairo', sans-serif;
  font-weight: bold;
  font-size: 22px;
  color: #C714E4;
}

.discounted-price:hover {
  color: #FFFFFF;
}

.carousel-control {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  color: #C714E4;
  border: none;
  font-size: 4rem;
  cursor: pointer;
  z-index: 1000;
  padding: 0 10px;
}

/* Media Queries */
@media (max-width: 1200px) {
  .games-grid {
    grid-template-columns: repeat(3, 1fr);
    gap: 15px;
  }
}

@media (max-width: 992px) {
  .games-grid {
    grid-template-columns: repeat(2, 1fr);
    gap: 10px;
  }
}

@media (max-width: 768px) {
  .games-grid {
    grid-template-columns: 1fr;
    gap: 5px;
  }
}
</style>
