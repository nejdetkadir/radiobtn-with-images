<template>
  <div class="container mt-5">
    <div class="row">
      <div class="col-md-8 mx-auto shadow-lg p-3 mb-5 bg-white rounded">
        <form>
          <div class="form-check form-check-inline" v-for="item in dataList" :key="item.name">
            <input class="form-check-input" type="checkbox" v-model="selectedInterest" :value="item.name">
            <img class="form-check-label" :src="item.img" :alt="item.name" height="50">
          </div>
        </form>
      </div>
    </div>
    <div v-if="selectedInterest.length > 0">
      <hr>
      <div class="row">
        <div class="col-md-3 mx-auto shadow-lg p-3 mb-5 bg-white rounded" id="selected-list">
          <ul>
            <li v-for="item in selectedInterest" :key="item">{{ item }}</li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    data: () => {
      return{
        selectedInterest: [],
        dataList: [
          {
            name: 'Android',
            img: require('@/assets/android.png')
          },
          {
            name: 'Angular',
            img: require('@/assets/angular.png')
          },
          {
            name: 'Arduino',
            img: require('@/assets/arduino.png')
          },
          {
            name: 'Bootstrap',
            img: require('@/assets/bootstrap.png')
          },
          {
            name: 'CSS',
            img: require('@/assets/css.png')
          },
          {
            name: 'Dart',
            img: require('@/assets/dart.png')
          },
          {
            name: 'ES6',
            img: require('@/assets/es6.png')
          },
          {
            name: 'Flutter',
            img: require('@/assets/flutter.png')
          },
          {
            name: 'HTML',
            img: require('@/assets/html.png')
          },
          {
            name: 'Java',
            img: require('@/assets/java.png')
          },
          {
            name: 'Javascript',
            img: require('@/assets/javascript.png')
          },
          {
            name: 'NodeJS',
            img: require('@/assets/nodejs.png')
          },
          {
            name: 'Php',
            img: require('@/assets/php.png')
          },
          {
            name: 'Python',
            img: require('@/assets/python.png')
          },
          {
            name: 'Ruby',
            img: require('@/assets/ruby.png')
          },
          {
            name: 'VueJS',
            img: require('@/assets/vue.png')
          },
          {
            name: 'Firebase',
            img: require('@/assets/firebase.png')
          },
          {
            name: 'Git',
            img: require('@/assets/git.png')
          }
        ]
      }
    }
  }
</script>

<style>
  #selected-list{
    background-color: lightblue !important;
    color: black;
  }
</style>
