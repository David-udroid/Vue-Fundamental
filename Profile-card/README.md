# Day 1  — Setup & First Component. ✅

- Topic:
 Node/Vite setup, project structure.


- Milestone:
  Scaffold a Vite + Vue 3 app and render a personal profile card (name, photo, bio).

## Project Setup.✨
1. Created a new project folder - Vue-Fundamental.

```sh
# Vue Installation.
 npm create vite@latest Profile-card -- --template vue
```
this automatically creates the project folder, install dependencies and run the dev.

### Terminal Output
 ![Screenshot](./screenshot/vue-install.png)

## Creation of Profile Card
<!-- Unveiling the base of every .vue file:
```sh
# <template></template> → what appears on the page
# <script> → the logic/data
# <style> → how it looks
``` -->

- Name: created in srcipt section with "const name ='David Chinemelum' 
- Photo: imported from "src/assets/" 
- Bio: description of my tech background.

## Styling
This contains the overall look of the Profile card.

## Script
The logic/functional of the profile card.

### Terminal Output🔥
 ![Screenshot](./screenshot/app.png)
 ![Screenshot](./screenshot/app-2.png)

## GitHub.🔥
1. Git initialization:
  git init
2. Commiting, Staging and Pushing:
```sh
  git add .
  git commit -m "Initial commit"
  git branch -M main
  git remote add origin https://github.com/David-udroid/Vue-fundamental.git
  git push -u origin main
```
## Final Result👩🏿‍💻
- Day 1 final deliverable is:

A polished, responsive personal developer profile card built with Vue 3 + Vite and hosted in your GitHub repository.

![Screenshot](./screenshot/final.png)

### What I learned
 - learnt how to setup and bulid a profile card.

# Day 2 — Template Syntax & Interpolation.✅

### Topic:
`{{ }}` interpolation, `v-bind` (attribute binding), and class/style binding.

### Milestone:
Make the profile card dynamic — data comes from a JS object, not hardcoded HTML.

## Project Overview
 For Day 2, I updated my Vue.js profile card to make it dynamic. Instead of writing the profile information directly in the HTML, I stored the information inside a JavaScript object and used Vue template syntax to display it.

## Step Completed☑️:
1. Created a Profile Object.
I created a JavaScript object containing my profile information:
```js
const user = reactive({
 name: 'David Chinemelum',
 role: 'Frontend Dev', 
 bio: 
 ' A software developer focused on frontend development ...',
 image: image,
 isOnline: false,
})
```
2. Used Interpolation.
 Replaced hardcoded text in the template with `{{ }}` interpolation.
```html
 <h1>{{ user.name }}</h1>
 <h3 class="role" :style="{ color: user.themeColor }">{{ user.role }}</h3>
 <p>{{ user.bio }}</p>
```
3. Added Attribute Binding.
 Replaced hardcoded attributes (`src`, `alt`, `href`) with `v-bind` (`:`) bindings.
```html
<img :src="user.image" alt="Profile Pic">
```
4. Added Class Binding.
I used :class to dynamically apply a CSS class.
```html
 <span class="status" :class="{ online: user.isOnline, offline: !user.isOnline }">
  {{ user.isOnline ? 'Online' : 'Offline' }}
   </span>
```
5. Added Style Binding.
Bound the card border and role text color to `user.themeColor` with style binding.
```html
<h3 class="role" :style="{ color: user.themeColor }">{{ user.role }}</h3>
```
![Day 2](./screenshot/day2.png)
## Bound Properties.
- Interpolation - `{{ user.name }}` , `{{ user.bio }}`
- Attribute binding - `:src="user.avatar"` 
- Class binding - `:class="{ online: user.isOnline }" `

## Git Commands

git add .
git commit -m "Complete Day 2 dynamic profile card"
git push

## Result👩🏾‍💻.
A screenshot of the completed ynamic profile card
![Day 2](./screenshot/online.png)

Offline -  `isOnline: false`
![Day 2](./screenshot/offline.png)

## What I learned

- **Interpolation (`{{ }}`)** renders text from data. It accepts expressions only (no `if` statements), so I used a ternary for conditional text.
- **`v-bind` (shorthand `:`)** connects an HTML attribute to a JS expression. Attribute binding is its most common use, e.g. `:src` and `:href`.
- **Class binding** uses the object syntax to toggle classes based on data, e.g. `:class="{ online: user.isOnline }"`.
- **Style binding** takes an object with camelCase properties, e.g. `:style="{ borderColor: user.themeColor }"`.

