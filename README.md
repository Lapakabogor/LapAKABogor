<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>LapAKABogor Store</title>
  <style>
    /* Basic Styles */
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      background-color: #f5f5f5;
    }

    header {
      background-color: #007bff; /* Blue */
      color: white;
      text-align: center;
      padding: 1rem;
    }

    header h1 {
      margin: 0;
      font-size: 2rem;
    }

    .carousel {
      width: 100%;
      overflow: hidden;
      margin-top: 1rem;
    }

    .carousel-images {
      display: flex;
      animation: slide 10s infinite;
    }

    .carousel img {
      width: 100%;
      height: auto;
    }

    @keyframes slide {
      0% { transform: translateX(0); }
      33% { transform: translateX(-100%); }
      66% { transform: translateX(-200%); }
      100% { transform: translateX(0); }
    }

    .category-menu {
      display: flex;
      justify-content: center;
      gap: 1rem;
      background-color: #e9ecef;
      padding: 0.5rem;
    }

    .category-btn {
      background-color: #ffffff;
      border: 1px solid #007bff;
      padding: 0.5rem 1rem;
      border-radius: 20px;
      cursor: pointer;
      transition: background-color 0.3s;
    }

    .category-btn:hover {
      background-color: #ff5733; /* Red */
      color: white;
    }

    .product-list {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      padding: 1rem;
    }

    .product-card {
      background-color: white;
      border-radius: 8px;
      width: 200px;
      margin: 0.5rem;
      box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
      text-align: center;
      overflow: hidden;
    }

    .product-card img {
      width: 100%;
      height: 150px;
      object-fit: cover;
    }

    .product-info {
      padding: 1rem;
    }

    .product-name {
      font-weight: bold;
      font-size: 1rem;
    }

    .product-price {
      color: #007bff;
      font-weight: bold;
      margin-top: 0.5rem;
    }

    .add-to-cart-btn {
      background-color: #28a745; /* Green */
      color: white;
      padding: 0.5rem;
      width: 100%;
      border: none;
      border-radius: 0 0 8px 8px;
      cursor: pointer;
      transition: background-color 0.3s;
    }

    .add-to-cart-btn:hover {
      background-color: #218838; /* Dark Green */
    }

    #cart {
      position: fixed;
      top: 70px;
      right: 10px;
      width: 320px;
      background-color: white;
      border-radius: 8px;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
      max-height: 80vh;
      overflow-y: auto;
      padding: 1rem;
      z-index: 100;
      display: flex;
      flex-direction: column;
    }

    #cart h2 {
      margin-top: 0;
      font-size: 1.2rem;
      border-bottom: 1px solid #ddd;
      padding-bottom: 0.5rem;
    }

    .cart-item {
      display: flex;
      justify-content: space-between;
      margin-bottom: 0.5rem;
    }

    .cart-item-name {
      font-size: 1rem;
    }

    .cart-item-price {
      font-weight: bold;
      color: #007bff;
    }

    #checkout-btn {
      background-color: #ff5733; /* Red */
      color: white;
      padding: 0.7rem;
      width: 100%;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      margin-top: 1rem;
    }

    #checkout-btn:hover {
      background-color: #e03e1f; /* Dark Red */
    }

    .order-form {
      margin-top: 1rem;
    }

    .order-form input, .order-form select {
      width: 100%;
      padding: 0.5rem;
      margin-bottom: 1rem;
      border: 1px solid #ddd;
      border-radius: 4px;
    }

    /* Responsiveness */
    @media(max-width: 768px) {
      .product-card {
        width: 100%;
        margin: 0.5rem 0;
      }

      #cart {
        position: static;
        width: 100%;
      }
    }
  </style>
</head>
<body>

<header>
  <h1>LapAKABogor Store</h1>
</header>

<!-- Carousel Promo -->
<div class="carousel">
  <div class="carousel-images">
    <img src="https://via.placeholder.com/1000x300?text=Promo+1" alt="Promo 1">
    <img src="https://via.placeholder.com/1000x300?text=Promo+2" alt="Promo 2">
    <img src="https://via.placeholder.com/1000x300?text=Promo+3" alt="Promo 3">
  </div>
</div>

<!-- Kategori Produk -->
<div class="category-menu">
  <button class="category-btn">Makanan Berat 🍛</button>
  <button class="category-btn">Makanan Ringan 🍪</button>
  <button class="category-btn">Minuman 🥤</button>
  <button class="category-btn">Alat dan Bahan Kimia ⚗️</button>
  <button class="category-btn">Produk Inovasi Mahasiswa AKA 💡</button>
  <button class="category-btn">Lain-lain 🛍️</button>
</div>

<!-- Daftar Produk -->
<div class="product-list">
  <div class="product-card">
    <img src="https://via.placeholder.com/200x150?text=Produk+1" alt="Produk 1">
    <div class="product-info">
      <p class="product-name">Produk 1</p>
      <p class="product-price">Rp 50.000</p>
      <button class="add-to-cart-btn">Tambah ke Keranjang</button>
    </div>
  </div>
  <div class="product-card">
    <img src="https://via.placeholder.com/200x150?text=Produk+2" alt="Produk 2">
    <div class="product-info">
      <p class="product-name">Produk 2</p>
      <p class="product-price">Rp 35.000</p>
      <button class="add-to-cart-btn">Tambah ke Keranjang</button>
    </div>
  </div>
  <!-- More products go here -->
</div>

<!-- Keranjang Belanja -->
<div id="cart">
  <h2>Keranjang Belanja</h2>
  <div id="cart-items">
    Keranjang kosong
  </div>
  <div id="total-price"></div>
  <button id="checkout-btn" onclick="checkout()">Checkout</button>
</div>

<!-- Formulir Pembeli -->
<div class="order-form">
  <label for="name">Nama Pembeli</label>
  <input type="text" id="name" placeholder="Masukkan nama Anda" required>

  <label for="prodi">Prodi/Kelas</label>
  <input type="text" id="prodi" placeholder="Masukkan Prodi/Kelas Anda" required>

  <label for="whatsapp">Nomor WhatsApp</label>
  <input type="text" id="whatsapp" placeholder="Masukkan Nomor WhatsApp" required>

  <label for="address">Alamat (opsional, hanya jika memilih pengantaran)</label>
  <input type="text" id="address" placeholder="Masukkan alamat Anda">
</div>

<script>
  function checkout() {
    const buyerName = document.getElementById("name").value;
    const whatsapp = document.getElementById("whatsapp").value;
    const address = document.getElementById("address").value;

    const cartItems = []; // Replace with actual cart data
    let orderDetails = `Nama: ${buyerName}\nWhatsApp: ${whatsapp}\nAlamat: ${address}\n\nDaftar Pesanan:\n`;

    cartItems.forEach(item => {
      orderDetails += `${item.name} x ${item.quantity} = ${item.totalPrice}\n`;
    });

    const totalAmount = "Total: Rp" + cartItems.reduce((sum, item) => sum + item.totalPrice, 0);

    const url = `https://wa.me/089664363463?text=${encodeURIComponent(orderDetails + totalAmount)}`;
    window.open(url, '_blank');
  }
</script>

</body>
</html>
