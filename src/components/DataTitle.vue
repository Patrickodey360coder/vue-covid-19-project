<template>
  <div>
    <p>hello</p>
    <h1>{{text}}</h1>
    <h1>{{dataDate}}</h1>
  </div>
</template>

<script>

export default {
  name: 'DataTile',
  props: ['text', 'dataDate']
}
</script>

