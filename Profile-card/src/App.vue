<script setup>
import { reactive } from 'vue'
import image from './assets/My-image.png'

const user = reactive({
 name: 'David Chinemelum',
 role: 'Frontend Dev', 
 bio: 
 ' Aspiring software developer focused on frontend development and modern web technologies. building with HTML, CSS, JavaScript, currently learning Vue.js, and GitHub. I’m actively building practical projects to strengthen my skills in web development, Git/GitHub, responsive design, and problem-solving. I enjoy turning designs into responsive, user-friendly applications and continuously improving my problem-solving and development skills. ',
 image: image,
 isOnline: true,
})

</script>

<template>
  <div class="card">
      <img :src="user.image" alt="Profile Pic">
      <h1>{{ user.name }}</h1>
      <h3 class="role" :style="{ color: user.themeColor }">{{ user.role }}</h3>
      <p>{{ user.bio }}</p>
      <span class="status" :class="{ online: user.isOnline, offline: !user.isOnline }">
        {{ user.isOnline ? 'Online' : 'Offline' }}
      </span>
  </div>
</template>

<style>
#app{
 width: 1126px; 
}
 .card {
  width: 500px;
  margin: 100px auto;
  padding: 30px;
  text-align: center;
  border-radius: 15px;
  background: black;
  box-shadow: 0 5px 20px rbga(0, 0, 0, 0.15);
 }

 .card img{
  width: 250px;
  border-radius: 5%;
  object-fit: cover;
 }
 .card h1 {
  margin: 20px 0 10px;
  font-size: 40px;
  color: goldenrod;
  font-family: cursive;
 }
 
 .card p {
  color: #8c8989;
  line-height: 1.5;
  font-size: 16px;
 }
 .status { 
  display: inline-block;
  margin-top: 20px;
  padding: 2px 10px; 
  border-radius: 9px;
  font-family:Verdana, Geneva, Tahoma, sans-serif; 
  font-size: 1rem; 

 }
 .status.online { 
  color: #0de868;
  background: #161817; 
}
.status.offline { 
  color: #b38989;
  background: #261e21; 
  }
</style>