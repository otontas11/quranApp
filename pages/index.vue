<template>
  <div>
    <div v-for="(item, index) of info" :key="index" :item="item">
      <Info :title="item.title" :img="item.img" :cardText="item.cardText" />
    </div>
  </div>
</template>

<script>
import Info from '../components/info'
export default {
  components: {
    Info,
  },
  data() {
    return {
      info: [
        {
          title: 'Learn Alifba',
          cardText:
            'The easiest way to learn Quran alphabets\n' +
            'Listen - Repeat - Learn - Memorize ',
          img: '0.jpg',
        },
        {
          title: 'Quran Alphabets',
          cardText:
            'Designed particularly for kids.\n' +
            'Sure everyone can learn easily by using this app\n',
          img: '1.jpg',
        },
        {
          title: 'Game Area Type : 1 ',
          cardText:
            'In these area you can test yourself.\n' +
            'This is the funniest part after learning some alphabets\n' +
            'Listen and find true choice\n',
          img: '2.jpg',
        },
        {
          title: 'Game Area Type : 2',
          cardText:
            'Every lesson has a game section also. \n' +
            'Wtih this way you can learn so quickly.\n',
          img: '3.jpg',
        },
        {
          title: 'Listen Surah',
          cardText:
            'This area exactly for you If you want to listen Quran Surahs like mp3.\n' +
            'Click and Listen\n',
          img: '4.jpg',
        },
        {
          title: 'Listen Surah Line by Line',
          cardText:
            'You want to lsten surahs ayat by ayat?\n' +
            'This area was designed exactly for this job\n',
          img: '5.jpg',
        },
        {
          title: 'Listen Surah',
          cardText:
            'This area exactly for you If you want to listen Quran Surahs like mp3.\n' +
            'Click and Listen\n',
          img: '6.jpg',
        },
        {
          title: 'Memory Game Area',
          cardText:
            'Click card listen alphabet and find true letter\n' +
            'Click and Listen\n',
          img: '7.jpg',
        },
      ],
    }
  },
}
</script>

<style lang="scss" scoped></style>
