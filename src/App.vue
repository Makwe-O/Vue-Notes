<template>
  <div id="app">
    <Header />
    <TextBox :createNote="createNote" />
    <CardGrid :quoteList="quotes" />
  </div>
</template>

<script>
import TextBox from './components/TextBox.vue';
import CardGrid from './components/CardGrid.vue';
import Header from './components/Header.vue';
import { format } from 'date-fns';
const uuidv1 = require('uuid/v1');

export default {
  name: 'app',
  components: {
    TextBox,
    CardGrid,
    Header
  },
  data() {
    return {
      quotes: [
        {
          date: format(new Date(), 'PPpp'),
          text: 'Hello My name is Max',
          id: uuidv1()
        },
        {
          date: format(new Date(), 'PPpp'),
          text: 'Hello My name is Max',
          id: uuidv1()
        },
        {
          date: format(new Date(), 'PPpp'),
          text: 'Hello My name is Max',
          id: uuidv1()
        },
        {
          date: format(new Date(), 'PPpp'),
          text: 'Hello My name is Max',
          id: uuidv1()
        }
      ],
      quote: ''
    };
  },
  methods: {
    createNote(newNote) {
      this.quotes.push({
        id: uuidv1(),
        date: format(new Date(), 'PPpp'),
        text: newNote
      });
    }
  }
};
</script>

<style>
#app {
  font-family: 'Rubik', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  max-width: 1024px;
  padding: 0 30px;
  margin: 0 auto;
}
</style>
