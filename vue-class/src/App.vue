<template>
  <div>
    <header class="header">
      <a href="#"> <img src="./components/logo.svg" alt="logo" /></a>
      <ul class="header-menu">
        <li class="header-item">
          <a href="#" class="header-link">Home</a>
        </li>
        <li class="header-item">
          <a href="#" class="header-link">Product</a>
        </li>
        <li class="header-item">
          <a href="#" class="header-link">Pricing</a>
        </li>
        <li class="header-item">
          <a href="#" class="header-link">Testimonials</a>
        </li>
        <li class="header-item">
          <a href="#" class="header-link">Contact Us</a>
        </li>
      </ul>
      <button class="header-btn">Buy Now</button>
    </header>
    <div class="citeAbout">
      <div class="citeLeft">
        <p class="text1">Sweet fun, full of milk.</p>
        <h1>Feel inside cold with our delicious ice-cream.</h1>
        <p class="text2">
          Some food has looked so awful that it's looked like something that the
          dog's brought home, yet after one mouthful I've been left eating my
          thoughts, my words.
        </p>
        <button class="left-btn">Buy Now</button>
      </div>
      <div class="citeRight">
        <img src="./components/ice.svg" alt="iceCream" />
      </div>
    </div>
    <hr />
    <div class="purchases">
      <div class="card1">
        <h2 class="title">A delicious dessert</h2>
        <img
          src="./components/cream1.svg"
          alt="cream"
          style="width: 350px; height: 350px"
        />
        <h3 class="add-purchases">
          Purchases: <span>{{ obj.count }}</span>
        </h3>
        <button @click="increment" class="card-button">Add</button>
        <button @click="reset" class="card-button2">Reset</button>
      </div>
      <div class="card2">
        <h2 class="title">Cayenne chocolate</h2>
        <img
          src="./components/cream2.svg"
          alt="cream"
          style="width: 350px; height: 350px"
        />
        <h3 class="add-purchases">
          Purchases: <span>{{ obj.count }}</span>
        </h3>
        <button @click="increment" class="card-button">Add</button>
        <button @click="reset" class="card-button2">Reset</button>
      </div>
      <div class="card3">
        <h2 class="title">Ice cream dessert</h2>
        <img
          src="./components/cream3.svg"
          alt="cream"
          style="width: 350px; height: 350px"
        />
        <h3 class="add-purchases">
          Purchases: <span>{{ obj.count }}</span>
        </h3>
        <button @click="increment" class="card-button">Add</button>
        <button @click="reset" class="card-button2">Reset</button>
      </div>
    </div>
  </div>
</template>
<script setup lang="ts">
import { reactive } from "vue";

const obj = reactive({ count: 0 });

const increment = () => {
  obj.count++;
};

const reset = () => {
  obj.count = 0;
};
</script>
<style></style>
