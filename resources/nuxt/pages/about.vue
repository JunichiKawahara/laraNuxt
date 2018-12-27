<template>
  <div>
    <h1 class="title">About this App</h1>

    <p>アプリケーションの紹介文がここに入ります。</p>

    <ul>
        <li><a href="/">トップページへ戻る(aタグ)</a></li>   
        <li><router-link to="/">トップページへ戻る（router-link）</router-link></li>
    </ul>
  </div>
</template>

<script>
export default {
  data(){
    return { }
  }  
}
</script>