<template>
  <div id="app">
    <Header />
    <TextBox :createNote="createNote" />
    <CardGrid :quoteList="quotes" :viewNote="viewNote" :deleteNote="deleteNote" />
    <ViewCard :selectedNote="selectedNote" />
  </div>
</template>

<script>
import TextBox from "./components/TextBox.vue";
import CardGrid from "./components/CardGrid.vue";
import Header from "./components/Header.vue";
import ViewCard from "./components/ViewCard";
import { format } from "date-fns";
const uuidv1 = require("uuid/v1");

export default {
  name: "app",
  components: {
    TextBox,
    CardGrid,
    Header,
    ViewCard
  },
  data() {
    return {
      quotes: [
        {
          date: format(new Date(), "PPpp"),
          text:
            "Workin' on the weekend like usual Way off in the deep end like usual",
          id: uuidv1()
        },
        {
          date: format(new Date(), "PPpp"),
          text:
            "Haven't done my taxes, I'm too turnt up Virgil got a Patek on my wrist going nuts",
          id: uuidv1()
        },
        {
          date: format(new Date(), "PPpp"),
          text:
            "Someone hit your block up, I'd tell you if it was us Manor house in Rosewood, this shit too plush",
          id: uuidv1()
        },
        {
          date: format(new Date(), "PPpp"),
          text: "Hello My name is Max",
          id: uuidv1()
        }
      ],
      quote: "",
      selectedNote: null
    };
  },
  methods: {
    createNote(newNote) {
      this.quotes.push({
        id: uuidv1(),
        date: format(new Date(), "PPpp"),
        text: newNote
      });
    },
    viewNote(note) {
      let foundNote = this.quotes.find(quote => quote.id === note.id);
      this.selectedNote = foundNote;
    },
    deleteNote(note) {
      this.quotes = this.quotes.filter(quote => quote.id != note.id);
    }
  }
};
</script>

<style>
#app {
  font-family: "Rubik", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  max-width: 1024px;
  padding: 0 30px;
  margin: 0 auto;
}
</style>
