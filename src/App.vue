<template>
  <div id="app">
    <Header />
    <div style="display : flex; flex-direction: row">
      <div id="toolbar_container">
        <Sidebar />
      </div>
      <div id="template_view_container">
        <TemplateView />
      </div>
    </div>
  </div>
</template>

<script>
import Header from './components/base/Header'
import Sidebar from './components/sidebar/Sidebar'
import TemplateView from './components/templates/TemplateView'

export default {
  name: 'App',
  components: {
    Header,
    Sidebar,
    TemplateView
  }
}
</script>

<style>
    
    body{
      margin: 0px;
    }

    #template_view_container{
      flex-grow: 2;
      margin: 50px;
    }
</style>
