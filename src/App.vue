<script setup>
import HelloWorld from './components/HelloWorld.vue'

   const products = [
  {
    id: 1,
    title: "iPhone 15 Pro",
    description: "Флагманский смартфон Apple с новым процессором",
    price: 1200,
    image: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTqSW_Ya4_t5sHnCMjrk1BHufFyaoDZCMLbvQ&s"
  },
  {
    id: 2,
    title: "Samsung Galaxy S24",
    description: "Мощный Android-смартфон с отличной камерой",
    price: 1100,
    image: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTqSW_Ya4_t5sHnCMjrk1BHufFyaoDZCMLbvQ&s"
  },
  {
    id: 3,
    title: "MacBook Air M3",
    description: "Лёгкий и производительный ноутбук для работы",
    price: 1500,
    image: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTqSW_Ya4_t5sHnCMjrk1BHufFyaoDZCMLbvQ&s"
  },
  {
    id: 4,
    title: "AirPods Pro 2",
    description: "Беспроводные наушники с шумоподавлением",
    price: 250,
    image: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTqSW_Ya4_t5sHnCMjrk1BHufFyaoDZCMLbvQ&s"
  },
  {
    id: 5,
    title: "iPad Air",
    description: "Планшет для работы и развлечений",
    price: 800,
    image: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTqSW_Ya4_t5sHnCMjrk1BHufFyaoDZCMLbvQ&s"
  },
  {
    id: 6,
    title: "Sony PlayStation 5",
    description: "Игровая консоль нового поколения",
    price: 600,
    image: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTqSW_Ya4_t5sHnCMjrk1BHufFyaoDZCMLbvQ&s"
  },
  {
    id: 7,
    title: "Xiaomi Smart Watch",
    description: "Умные часы с мониторингом здоровья",
    price: 180,
    image: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTqSW_Ya4_t5sHnCMjrk1BHufFyaoDZCMLbvQ&s"
  },
  {
    id: 8,
    title: "Dell XPS 13",
    description: "Компактный и мощный ультрабук",
    price: 1400,
    image: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTqSW_Ya4_t5sHnCMjrk1BHufFyaoDZCMLbvQ&s"
  },
  {
    id: 9,
    title: "Logitech MX Master 3",
    description: "Профессиональная беспроводная мышь",
    price: 120,
    image: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTqSW_Ya4_t5sHnCMjrk1BHufFyaoDZCMLbvQ&s"
  },
  {
    id: 10,
    title: "Samsung 4K Monitor",
    description: "27-дюймовый монитор с разрешением 4K",
    price: 500,
    image: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTqSW_Ya4_t5sHnCMjrk1BHufFyaoDZCMLbvQ&s"
  }
]
</script>



<template>
<div v-if="products != 0" class="cont">
    <div v-for="product in products" :key="product.id" class="product-card">
      <img :src="product.image" :alt="product.image" class="product-image">
      
      <div class="product-block">
        <h3 class="product-title">{{ product.title }}</h3>
        <p class="product-description">{{ product.description }}</p>
        
        <div class="product-footer">
          <span class="product-price">{{ product.price  }} $</span>
          <button class="add-cart">
            Sotib olish
          </button>
        </div>
      </div>
    </div>

  </div>
  <div v-else="">
    <h1>Hozrcha malumot yoq !</h1>
  </div>
</template>
<style>

.cont {
  display: flex;
  flex-wrap: wrap; 
  justify-content: center; 
  gap: 20px;
  padding: 20px;
  background-color: #f9f9f9;
}

.product-card {
  display: flex;
  flex-direction: column;
  flex: 0 1 calc(25% - 20px);
  min-width: 250px;
  background: #fff;
  border-radius: 12px;
  border: 1px solid #e0e0e0;
  overflow: hidden;
  transition: transform 0.2s ease;
  padding: 10px;
}

.product-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 10px 20px rgba(0,0,0,0.08);
}

.product-image {
  width: 100%;
  height: 200px;
  object-fit: cover;
}

.product-block {
  padding: 16px;
  display: flex;
  flex-direction: column;
  flex-grow: 1; 
}

.product-title {
  font-size: 1.1rem;
  margin: 0 0 10px 0;
  color: #2c3e50;
}

.product-description {
  font-size: 0.9rem;
  color: #7f8c8d;
  line-height: 1.5;
  margin-bottom: 15px;
  flex-grow: 1;
}

.product-footer {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding-top: 10px;
  border-top: 1px solid #f1f1f1;
}

.product-price {
  font-weight: 700;
  font-size: 1.2rem;
  color: #e67e22;
}

.add-cart {
  background-color: #34495e;
  color: white;
  border: none;
  padding: 8px 16px;
  border-radius: 6px;
  cursor: pointer;
  transition: background 0.3s;
}

.add-to-cart:hover {
  background-color: #2c3e50;
}


</style>