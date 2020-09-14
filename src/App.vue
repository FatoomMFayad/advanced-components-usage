<template>
  <div class="container">
    <div class="row">
          <div class="col-xs-12">
            <button @click="selected = 'appQuote'">Quote</button>
            <button @click="selected = 'appAuthor'">Author</button>
            <button @click="selected = 'appNew'">New</button>
            <hr>
            <p>{{ selected }}</p>
            <keep-alive>
              <component :is='selected'>
                <p>Default Content</p>
              </component>
            </keep-alive>            
            <!-- <appQuote>
              <h2 slot="title">{{ quoteTitle }}</h2>
              <p>a wonderful Quote</p>
            </appQuote> -->
            <hr>
          </div>
    </div>   
  </div>
</template>

<script>
import Quote from './components/Quote';
import Author from './components/Author';
import New from './components/New';

export default {
  data: function(){
    return{
      quoteTitle: 'The Quote',
      selected: 'appQuote'
    }
  },
  components:{
    appQuote: Quote,
    appAuthor: Author,
    appNew: New
  }
 
}
</script>

<style>

</style>
