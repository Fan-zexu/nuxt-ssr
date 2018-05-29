<template>
  <div>
    <h2>News Index page</h2>
    <img src="~static/star.png" alt="">
    <p>NewsId: {{$route.params.newsId}}</p>
    <ul>
      <li><nuxt-link to="/">Home</nuxt-link></li>
      <li><nuxt-link :to="{name: 'news-id', params: {id: 123, title: 'this is news 1'}}">news 1</nuxt-link></li>
      <li><nuxt-link to="/news/456">news 2</nuxt-link></li>      
    </ul>
  </div>
</template>
