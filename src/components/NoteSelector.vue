<template>
  <div class="note-selector" v-bind:class="{ active: selectedNoteId === note.id }" v-on:click="selectNote(note)">
    <p class="note-selector-title">{{ note.body }}</p>
    <p class="note-selector-timestamp">{{ note.timestamp }}</p>
  </div>
</template>

<script>
export default {
  props: ["note", "selectedNoteId"],
  methods: {
    selectNote: function(note) {
      console.log("HELLO");
      this.$emit("selectNote", note);
      // this.selectedNoteId = note.id;
    },
  },
};
</script>
