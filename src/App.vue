<script setup>
import { ref } from 'vue';

//membuat variabel reaktif
const counter = ref(0);

//membuat text interpolation
const nama = ref("Rizqy");

//membuat form binding
const inputNama = ref("");

//event listener
const alertMessage = () => alert(`Halo, ${nama.value}!`);

//attribute binding
const gambar = ref("https://vuejs.org/images/logo.png");

//conditional rendering
const tampilkan = ref(true);

</script>

<template>
  <div>
<!-- variabel reaktif -->
 <h2>Counter</h2>
 <p>Nilai : {{ counter }}</p>
 <button @click="counter++">Tambah</button>

 <hr/>

<!-- Text interpolation --> 
 <h2>Text Interpolation</h2>
 <p>Halo, {{ nama }}</p>

<hr/>

<!-- form binding -->
 <h2>Form Binding</h2>
 <input v-model="inputNama" placeholder="Masukkan nama"/>
<p>Nama yang anda inputkan : {{ inputNama }}</p>

<hr/>

<!-- event listener -->
<h2>Event LIstener</h2>
<button @click="alertMessage">Klik Saya</button>

<hr/>

<!-- attribute binding -->
 <h2>Atribute Binding</h2>
 <img :src="gambar" alt="Vue Logo" width="100">

 <hr/>

 <!-- conditional rendering -->
  <h2>Conditional Rendering</h2>
  <button @click="tampilkan = !tampilkan">
    {{ tampilkan ? "Sembunyikan" : "Tampilkan" }} Teks
  </button>
  <p v-if="tampilkan">Ini adalah teks yang dapat disembunyikan</p>

  </div>


</template>