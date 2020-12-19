<template>
  <div>
    <div>
      <b-card
        overlay
        class="text-center infoCard mt-3 mb-3"
        img-alt=""
        text-variant="black"
      >
        <b-row class="info_sub">
          <b-col class="mt-3">
            <b-img
              style="border-radius: 30px"
              :src="require('@/static/' + img + '')"
              fluid-grow
              alt="Responsive image"
            ></b-img>
          </b-col>
          <b-col>
              <div class="textArea" >
                <b-card-text>
                <h2>{{ title }}</h2>

               <h4> {{ cardText }}</h4>
              </b-card-text>  
              </div>
               
           </b-col>
        </b-row>
      </b-card>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
    },
    cardText: {
      type: String,
    },
    img: {
      type: String,
      default: '1.jpg',
    },
  },
  data() {
    return {
      title: 'title',
      cardText: 'cardText',
    }
  },
}
</script>

<style scoped>
.infoCard {
  border-radius: 20px;
  overflow: hidden;
  max-height: 300px;
}
.card-img-overlay {
  position: relative !important;
}
.card-img,
.card-img-bottom {
  max-height: 300px !important;
}
.info_sub {
    display: flex;
    justify-content: center;
    align-items: center;
  
}
.textArea{
     border-radius:5px;
    height: 100%;
}

@media only screen and (max-width: 600px) {
  h2 {
    font-size: 1.2rem;
  }
  h4{
      font-size: 1rem
  }
}
</style>
