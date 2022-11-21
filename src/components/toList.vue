<template>
  <div class="conteiner">
    <h1>Todo-List</h1>
    <div class="col-3">
      <h3>A fazer</h3>
      <draggable :list="list1" group="people" @change="log">
        <div v-for="(element) in list1" :key="element.name">{{ element.name }}</div>
      </draggable>
    </div>

    <div class="col-3">
      <h3>Fazendo</h3>
      <draggable :list="list2" group="people" @change="log">
        <div v-for="(element) in list2" :key="element.name">{{ element.name }} </div>
      </draggable>
    </div>

    <div class="col-3">
      <h3>Feito</h3>
      <draggable :list="list3" group="people" @change="log">
        <div v-for="(element) in list3" :key="element.name">{{ element.name }}</div>
      </draggable>
    </div>
  </div>
    <!-- <rawDisplayer class="col-3" :value="list1" title="List 1" />
    <rawDisplayer class="col-3" :value="list2" title="List 2" /> -->

</template>
<script>
import draggable from "vuedraggable";

export default {
  // name: "two-lists",
  // display: "Two Lists",
  // order: 1,
  components: {
    draggable
  },
  data() {
    return {
      list1: [
        { name: "John", id: 1 },
        { name: "Joao", id: 2 },
        { name: "Jean", id: 3 },
        { name: "Gerard", id: 4 }
      ],
      list2: [
        { name: "Juan", id: 5 },
        { name: "Edgard", id: 6 },
        { name: "Johnson", id: 7 }
      ],
      list3: [
        { name: "Edivan"},
        { name: "Edigar" },
        { name: "Jumento"}
      ]
    };
  },
  methods: {
    add: function() {
      this.list.push({ });
    },
    replace: function() {
      this.list = [{ }];
    },
    clone: function(el) {
      return {
        name: el.name + " cloned"
      };
    },
    log: function(evt) {
      window.console.log(evt);
    }
  }
};
</script>