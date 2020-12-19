<template>
  <div >
    <div class="vueGallery">
      <div
        class="activePhoto"
        :style="'background-image: url(' + photos[activePhoto] + ');'"
      >
        <button
          type="button"
          aria-label="Previous Photo"
          class="previous"
          @click="previousPhoto()"
        >
          <i class="fas fa-chevron-circle-left"></i>
        </button>
        <button
          type="button"
          aria-label="Next Photo"
          class="next"
          @click="nextPhoto()"
        >
          <i class="fas fa-chevron-circle-right"></i>
        </button>
      </div>
      <div class="thumbnails">
        <div
          v-for="(photo, index) in photos"
          :src="(photo)"
          :key="index"
          @click="activePhoto = index"
          :class="{ active: activePhoto == index }"
           :style="'background-image: url(' + photo + ')'"
        ></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  
 

  data() {
    return {
      activePhoto: null,
      photos: [
        require('@/static/0.jpg'),
        require('@/static/1.jpg'),
        require('@/static/2.jpg'),
        require('@/static/3.jpg'),
        require('@/static/4.jpg'),
        require('@/static/5.jpg'),
        require('@/static/6.jpg'),
        require('@/static/7.jpg'),
        require('@/static/8.jpg'),
        require('@/static/9.jpg'),
          ]
    }
  },
   mounted () {
    this.activePhoto = 0
    document.addEventListener("keydown", (event) => {
      if (event.which == 37)
        this.previousPhoto()
      if (event.which == 39)
        this.nextPhoto()
    })
  },
    methods: {
    nextPhoto () {
      this.activePhoto = ( this.activePhoto+1 < this.photos.length ? this.activePhoto+1 : 0 )
    },
    previousPhoto () {
      this.activePhoto = ( this.activePhoto-1 >= 0 ? this.activePhoto-1 : this.photos.length-1 )
    }
  }
}
</script>

<style lang="scss" scoped>
$brand: #5c4084;

 
.heading {
  text-align: center;
  h1 {
    background: -webkit-linear-gradient(#fff, lighten($brand, 20%));
    -webkit-text-fill-color: transparent;
    -webkit-background-clip: text;
    text-align: center;
    margin: 0 0 5px 0;
    font-weight: 900;
    font-size: 4rem;
    color: #fff;
  }
  h4 {
    color: lighten($brand, 20%);
    text-align: center;
    margin: 0 0 35px 0;
    font-weight: 400;
    font-size: 24px;
  }
}

.vueGallery {

  .activePhoto {
    width: 100%;
      margin-bottom: 5px;
    padding-bottom: 65%;
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
    border: 2px solid #fff;
    position: relative;

    button {
      border: none;
      background-color: transparent;
      font-size: 32px;
      color: #fff;
      opacity: 0.5;
      position: absolute;
      outline: none;
      height: 100%;

      &:hover {
        opacity: 1;
      }
      &.previous {
        padding: 0 1em 0 0.7em;
        left: 0;
        background: -moz-linear-gradient(left,  rgba(0,0,0,0.5) 0%, rgba(0,0,0,0) 100%);
        background: -webkit-linear-gradient(left,  rgba(0,0,0,0.5) 0%,rgba(0,0,0,0) 100%);
        background: linear-gradient(to right,  rgba(0,0,0,0.5) 0%,rgba(0,0,0,0) 100%);
        filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='#80000000', endColorstr='#00000000',GradientType=1 );
      }
      &.next {
        padding: 0 0.7em 0 1em;
        right: 0;
        background: -moz-linear-gradient(left,  rgba(0,0,0,0) 0%, rgba(0,0,0,0.5) 100%);
        background: -webkit-linear-gradient(left,  rgba(0,0,0,0) 0%,rgba(0,0,0,0.5) 100%);
        background: linear-gradient(to right,  rgba(0,0,0,0) 0%,rgba(0,0,0,0.5) 100%);
        filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='#00000000', endColorstr='#80000000',GradientType=1 );
      }
    }
  }
  .thumbnails {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(140px, 1fr));
    grid-gap: 5px;

    div {
      width: 100%;
      height: 0;
      border: 2px solid #fff;
      outline: 2px solid #fff;
      cursor: pointer;
      padding-bottom: 65%;
      background-size: cover;
      background-position: center;
      background-repeat: no-repeat;
      opacity: 1;

      &:hover {
        opacity: 0.6;
      }
      &.active {
        outline-color: $brand;
        opacity: 1;
      }
    }
  }
}
 
  </style>