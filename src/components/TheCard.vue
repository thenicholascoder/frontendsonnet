<template>
  <div class="col-md-3 p-0 m-0">
    <div class="card">
      <img class="card__img" :src="imgsrc" alt="Card image cap">
    </div>  
  </div>
</template>
<script>
export default {
  name: 'TheCard',

  props: {
    imgsrc: String
  },
  
  data() {
    return {

    }
  },

  methods: {
  }
}
</script>
<style scoped>
.card {
  margin: 2.5vw 1.4vw;
  padding: 0.3vw; 
  border-radius: 0.7vw;
  border: none;
  padding-bottom: 0.5em;
}

.card__img {
  padding: 1vw; 
  border-radius: 1.2vw;
}

.card__div {
  padding: 0 1vw; 
  padding-bottom: 1vw;
}

.card__p {
  padding: 0 0.1vw;
  margin-bottom: 0.8em;
}

.card__a {
  transition: all 0.5s;
  position: relative; 
  padding: 1em 1.8em; 
  text-decoration: none; 
  color: #333; 
  font-size: 0.8vw; 
  margin: 1vw 0;
  letter-spacing: 0.2vw;
  font-weight: 800;
}

.card__a::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: 1;
  transition: all 0.5s;
  border-radius: 2em; 
  padding: 0.75em 1.5em; 
  border: 0.3em solid rgba(45,45,45,1);
  background-color: rgba(0,0,0,0);
}

.card__a::after {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  z-index: 1;
  transition: all 0.5s;
  border-radius: 2em; 
  padding: 1em 1.5em; 
  border: 0.3em solid rgba(45,45,45,1);
  background-color: rgba(0,0,0,0);
}

.card__a:hover::before {
  transform: rotate(-45deg);
  background-color: rgba(0,0,0,0);
}

.card__a:hover::after {
  transform: rotate(45deg);
  background-color: rgba(255,255,255,0);
}

/* for mobile */
@media (max-width: 768px) {
  .card {
    margin: 25px;
    box-shadow: 0px 0px 8px 3px rgba(0, 0, 0, 0.06);
    padding-bottom: 2em;
  }

  .card__img {
    margin: 12.5px;
  }

  .card__p {
    font-size: 1em;
    margin: 0 1em;
    height: auto;
    margin-bottom: 2em;
  }

  .card__a {
    font-size: 0.9em;
  }
}

@media (min-width: 769px) { 
  .card {
    box-shadow: 0px 0px 0.2vw 0.2vw rgba(0, 0, 0, 0.05);
  }

  .card__p {
    font-size: 1.1vw;
    line-height: 1.5vw;
    height: 10em;
  }
}

/* .btn {
  line-height: 50px;
  height: 50px;
  text-align: center;
  width: 250px;
  cursor: pointer;
} */

</style>
