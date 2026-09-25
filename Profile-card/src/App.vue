<script setup>
const name = 'David Chinemelum'
const bio = 
' Aspiring software developer focused on frontend development and modern web technologies. building with HTML, CSS, JavaScript, currently learning an Vue.js, and GitHub. I’m actively building practical projects to strengthen my skills in web development, Git/GitHub, responsive design, and problem-solving. I enjoy turning designs into responsive, user-friendly applications and continuously improving my problem-solving and development skills. '
</script>

<template>
  <div class="card">
      <img src="./assets/My-image.png" alt="Profile Pic">
      <h1>{{ name }}</h1>
      <p>{{ bio }}</p>
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
  margin: 20px 0 20px;
  font-size: 40px;
  color: goldenrod;
  font-family: cursive;
 }
 
 .card p {
  color: #8c8989;
  line-height: 1.5;
  font-size: 19px;
 }
</style>