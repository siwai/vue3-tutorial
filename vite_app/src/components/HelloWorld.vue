<template>
    <div class="alert alert-primary">
      <h1>{{data.title}}</h1>
      <p class="mt-3 h5">{{$store.state.message}}</p>
    <hr>
    <div class="btn"
    @click="$store.commit('count')">
    @click.ctrl="$store.commit('reset')">
        <a >
            clicked: {{$store.state.counter}}
        </a>
    </div>
    </div>
  </template>
  
  <script>
  import { ref, reactive } from 'vue'
  
  export default {
    setup(props) {
      const data = reactive({
        title: 'Vuex',
      })
      return {
        data
      }
    }
  }
  </script>