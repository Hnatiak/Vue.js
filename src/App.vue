<template>
  <div :id="$style.app">
    <ApartmentsList :items="apartments">
      <template v-slot:apartment="{ apartment }">
        <ApartmentsItem
          :key="apartment.id"
          :descr="apartment.descr"
          :rating="apartment.rating"
          :price="apartment.price"
          :imgSrc="apartment.imgUrl"
          class="apartments-list__item"
        />
      </template>
      <template v-slot:title>New title</template>
      <template v-slot:description>New description</template>
    </ApartmentsList>
  </div>
</template>

<script>
import ApartmentsItem from './components/apartments/ApartmentsItem.vue';
import ApartmentsList from './components/apartments/ApartmentsList.vue';
import apartments from './components/apartments/apartments';

export default {
  name: 'App',
  components: {
    ApartmentsItem,
    ApartmentsList,
  },
  data() {
    return {
      apartments
    }
  }
}
</script>

<style module>
#app {
  font-family: Montserrat, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

/* .content {
  flex-grow: 1;
} */
</style>
