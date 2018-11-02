<template>
  <div class="container-fluid">
    <h1> Vue Draggable </h1>
    <div class="row">
      <draggable v-model="list1" class="col-sm-3 bg-light" :options="{ group: 'cool' }">
        <ul v-for="(element, index) in list1" :key="element.name + '-list1-' + index" class="list-group">
          <li class="list-group-item">{{ element.name }}</li>
        </ul>
      </draggable>

      <draggable v-model="list2" class="col-sm-3 bg-light" :options="{ group: 'cool' }">
        <ul v-for="(element, index) in list2" :key="element.name + '-list2-' + index" class="list-group">
          <li class="list-group-item" v-html="element.template"></li>
        </ul>
      </draggable>

      <div class="list-group col-sm-3 text-justify bg-light">
        <pre>{{ list1 }}</pre>
      </div>

      <div class="list-group col-sm-3 text-justify bg-light">
        <pre>{{ list2 }}</pre>
      </div>
      
    </div>
  </div>
</template>

<script>
import draggable from 'vuedraggable'
import 'jquery'
import 'bootstrap/dist/css/bootstrap.css'
import 'bootstrap/dist/js/bootstrap.js'
export default {
  name: "ListSharing",
  components: {
    draggable
  },
  data() {
    return {
      list1: [
        { name: 'Pig', template: '<b>Pig Temp</b>' }, 
        { name: 'Cow', template: '<b>Cow Temp</b>' },
        { name: 'Chicken', template: '<b>Chicken Temp</b>'},
        { name: 'Bird', template: '<b>Bird Temp</b>' }, 
        { name: 'Cat', template: '<b>Cat Temp</b>' },
        { name: 'Twitter', template: '<b>Twitter Temp</b>' }
      ],
      list2: [

      ]
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1,
h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
