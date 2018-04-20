<template class="bmailEditor">

  <textarea :id="id">
 
</textarea>

</template>

<script>
export default {
    props:["id"],
  mounted() {
    ClassicEditor.create(document.querySelector("#"+this.$props.id))
      .then(editor => {
        console.log(editor);
      })
      .catch(error => {
        console.error(error);
      });
  }
};
</script>

<style>
.bmailEditor {
  width: 100%;
  height: 100%;
  
}
</style>


