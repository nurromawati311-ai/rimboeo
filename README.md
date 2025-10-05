<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>TOKO RIMBERIO.SLAY</title>
<style>
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
  background: #A2D2FF;
  color: #333;
}

/* HEADER */
header {
  background: pink;
  color: white;
  padding: 15px;
  margin-top: 30px;
  border-radius: 10px;
  text-align: center;
   width: 100%
  max-width: 1000px
  box-sizing: border-box;
}
header img {
}
header img {
  height: 100px;
  border-radius: 8px;
}
header div {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-wrap: wrap;
  gap: 10px;
}
header h2 {
  margin: 0;
  font-size: 1.5em;
}

/* NAVIGASI */
nav {
  background: #FC6CB5;
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  padding: 10px;
}
nav a {
  color: #F2D2BD;
  text-decoration: none;
  margin: 8px 12px;
  font-weight: bold;
  font-size: 0.95em;
}

/* KONTEN */
.container {
  max-width: 1000px;
  margin: 20px auto;
  padding: 0 15px;
}

/* PRODUK GRID */
.products {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(160px, 1fr));
  gap: 15px;
  padding: 10px;
}

/* KARTU PRODUK */
.product {
  border: 1px solid #ccc;
  background: #F2D2BD;
  padding: 10px;
  border-radius: 10px;
  box-shadow: 0 2px 5px rgba(0,0,0,0.1);
  text-align: center;
}
.product img {
  width: 100%;
  height: 150px;
  object-fit: cover;
  border-radius: 5px;
}
.product h3 {
  margin: 8px 0 5px;
  font-size: 1em;
}
.price {
  color: #FC6CB5;
  font-weight: bold;
  font-size: 0.9em;
}
.btn {
  display: inline-block;
  margin-top: 10px;
  padding: 8px 12px;
  background: #F98088;
  color: white;
  border-radius: 5px;
  text-decoration: none;
  cursor: pointer;
  font-size: 0.9em;
}
.btn:hover { background: violet; }

/* KERANJANG BELANJA */
.cart {
  background: #F98088;
  padding: 15px;
  margin-top: 30px;
  border-radius: 10px;
  box-shadow: 0 2px 5px rgba(0,0,0,0.1);
}
.cart h3 {
  margin-top: 0;
  font-size: 1.2em;
}
.cart li {
  margin-bottom: 8px;
  font-size: 0.9em;
}
.removeBtn {
  margin-left: 10px;
  color: red;
  cursor: pointer;
  font-weight: bold;
}
.checkout {
  display: inline-block;
  margin: 5px 10px 5px 0;
  padding: 10px 15px;
  background: #F8ABA0;
  color: white;
  border-radius: 5px;
  text-decoration: none;
  font-weight: bold;
  transition: background 0.2s;
  font-size: 0.9em;
}
.checkout:hover { background: purple; }

/* POPUP */
.popup {
  position: fixed;
  top: 15px;
  right: 15px;
  background: #C5ADED;
  color: black;
  padding: 10px 16px;
  border-radius: 8px;
  box-shadow: 0 3px 8px rgba(0,0,0,0.2);
  opacity: 0;
  transform: translateY(-20px);
  transition: all 0.3s ease;
  z-index: 9999;
  font-size: 0.9em;
}
.popup.show { opacity: 1; transform: translateY(0); }

/* FOOTER */
footer {
  background: pink;
  color: white;
  text-align: center;
  padding: 20px;
  margin-top: 30px;
  font-size: 0.9em;
}


(max-width: 1000px) {
  header img {
    height: 80px;
	width: 100%
  }
  header h2 {
    font-size: 1.2em;
  }
  .products {
    grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
  }
  .product img {
    height: 120px;
  }
  .btn, .checkout {
    font-size: 0.8em;
    padding: 8px 10px;
  }
  nav a {
    font-size: 0.85em;
    margin: 5px;
  }
  footer {
    font-size: 0.8em;
  }
}
</style>
</head>
<body>
   <header>
    <div style="display:flex; align-items:center; gap:15px;">
      <img src="2.jpg" alt="Logo Toko RIMBERIO" style="height:200px; border-radius:9px;">
      <div>
        <h2 style="margin:0;">TOKO RIMBERIO.SLAY</h2>
        <p style="margin:0;">Menjual Kabel & Alat Jaringan dengan Harga Terjangkau</p>
      </div>
    </div>
  </header>
  <nav>
    <a href="#home">Home</a>
    <a href="#produk">Produk</a>
    <a href="#tentang">Tentang</a>
    <a href="#kontak">Kontak</a>
  </nav>
<div class="container" id="home">
    <h2>Selamat Datang di Toko RIMBERIO</h2>
    <p>Kami menyediakan berbagai kebutuhan jaringan seperti kabel UTP,
      konektor RJ-45, MIKRO USB, CASE HANDPHONE, kuliner dan lain-lain dengan harga bersaing.</p>
  </div>

  <div class="container" id="produk">
    <h2>Daftar Produk</h2>
    <div class="products">
      <div class="product">
        <img src="gambar1.jfif" alt="Kabel UTP">
        <h3>Kabel UTP Cat 5e</h3>
        <p class="price">Rp 3.000 / meter</p>
        <button class="btn" onclick="addToCart('Kabel UTP Cat 5e', 'Rp 3.000 / meter')">Tambah ke Keranjang</button>
      </div>

      <div class="product">
        <img src="gambar2.jfif" alt="RJ-45">
        <h3>Konektor RJ-45</h3>
        <p class="price">Rp 2.000 / 3pcs</p>
        <button class="btn" onclick="addToCart('Konektor RJ-45', 'Rp 2.000 / 3pcs')">Tambah ke Keranjang</button>
      </div>

      <div class="product">
        <img src="gambar3.jfif" alt="Mikro USB">
        <h3>MIKRO USB</h3>
        <p class="price">Rp 10.000</p>
        <button class="btn" onclick="addToCart('MIKRO USB', 'Rp 10.000')">Tambah ke Keranjang</button>
      </div>

      <div class="product">
        <img src="gambar4.jfif" alt="Case HP">
        <h3>CASE HANDPHONE</h3>
        <p class="price">Rp 10.000</p>
        <button class="btn" onclick="addToCart('CASE HANDPHONE', 'Rp 10.000')">Tambah ke Keranjang</button>
      </div>

      <div class="product">
        <img src="gambar5.jfif" alt="CARGER HANDPHONE">
        <h3>CARGER HANDPHONE</h3>
        <p class="price">Rp 20.000</p>
        <button class="btn" onclick="addToCart('CARGER HANDPHONE', 'Rp 20.000')">Tambah ke Keranjang</button>
      </div>

	  <div class="product">
        <img src="gambar6.jfif" alt="LAN ADAPTER USB">
        <h3>LAN ADAPTER USB</h3>
        <p class="price">Rp 30.000</p>
        <button class="btn" onclick="addToCart('LAN ADAPTER USB', 'Rp 30.000')">Tambah ke Keranjang</button>
      </div>

	  <div class="product">
        <img src="GAMBAR7.jfif" alt="HEADSET BLUETOOTH">
        <h3>HEADSET BLUETOOTH</h3>
        <p class="price">Rp 27.000</p>
        <button class="btn" onclick="addToCart('HEADSET BLUETOOTH', 'Rp 27.000')">Tambah ke Keranjang</button>
      </div>

      <div class="product">
        <img src="gambar7.jpg" alt="HEADSET Kabel">
        <h3>HEADSET Kabel</h3>
        <p class="price">Rp 15.000</p>
        <button class="btn" onclick="addToCart('HEADSET Kabel', 'Rp 15.000')">Tambah ke Keranjang</button>
      </div>

      <div class="product">
        <img src="GAMBAR8.jfif" alt="TEMPERED GLASS">
        <h3>TEMPERED GLASS</h3>
        <p class="price">Rp 5.000</p>
        <button class="btn" onclick="addToCart('TEMPERED GLASS', 'Rp 5.000')">Tambah ke Keranjang</button>
      </div>

      <div class="product">
        <img src="GAMBAR9.jfif" alt="Dimsum">
        <h3>DIMSUM_Rohma</h3>
        <p class="price">Rp 1.000/biji</p>
        <button class="btn" onclick="addToCart('DIMSUM DENONG', 'Rp 1.000')">Tambah ke Keranjang</button>
      </div>

	  <div class="product">
        <img src="download.jfif" alt="Strowbery">
        <h3>strowbery.Najwa</h3>
        <p class="price">Rp 4.000/pack kecil</p>
        <button class="btn" onclick="addToCart('strowbery.Najwa', 'Rp 4.000')">Tambah ke Keranjang</button>
      </div>

	  <div class="product">
        <img src="10.jfif" alt="Cheese roll">
        <h3>cheese roll.Diana</h3>
        <p class="price">Rp 1.000/BIJI</p>
        <button class="btn" onclick="addToCart('cheese roll.Diana', 'Rp 1.000')">Tambah ke Keranjang</button>
      </div>

	  <div class="product">
        <img src="1.jfif" alt="Pangsit lumer">
        <h3>Pangsit lumer.Rindu</h3>
        <p class="price">Rp 2.000/pcs</p>
        <button class="btn" onclick="addToCart('Pangsit lumer.Rindu', 'Rp 2.000')">Tambah ke Keranjang</button>
      </div>
    </div>
  </div>

  <div class="container cart" id="cart">
    <h3>Keranjang Belanja</h3>
    <ul id="cart-items"></ul>
    <p class="total">Total: Rp 0</p>
    <div id="checkout-buttons" style="display:none; margin-top:10px;">
      <a href="#" id="checkout1" class="checkout">Checkout ke WA 1</a>
      <a href="#" id="checkout2" class="checkout">Checkout ke WA 2</a>
      <a href="#" id="checkout3" class="checkout">Checkout ke WA 3</a>
      <a href="#" id="checkout4" class="checkout">Checkout ke WA 4</a>
    </div>
    <button class="btn" style="background:#e91e63; margin-top:10px; display:none;" id="clearCartBtn" onclick="clearCart()">Kosongkan Keranjang</button>
  </div>

  <div id="popup" class="popup">Produk berhasil ditambahkan ✅</div> <!-- FIX emoji -->
  
<div class="container" id="tentang">
    <h2>Tentang Kami</h2>
    <p>Toko RIMBERIO.SLAY adalah usaha kecil yang bergerak di bidang penjualan kabel, alat-alat GADGET dan alat-alat jaringan.
      Produk diambil langsung dari supplier online terpercaya dengan harga grosir, lalu dijual kembali
      dengan harga terjangkau. Kecuali (DIMSUM, Cheese roll, strowbery, dan Pangsit lumer) adalah produk kami sendiri.</p>
  </div>
   <div class="container" id="kontak">
    <h2>Kontak Kami</h2>
    <p>Hubungi kami melalui WhatsApp menggunakan tombol checkout di atas.</p>
  </div>
 
  <script>
    let cart = [];

    // Load keranjang dari LocalStorage saat halaman dibuka
    window.onload = function() {
      let savedCart = localStorage.getItem("cart");
      if (savedCart) {
        cart = JSON.parse(savedCart);
        renderCart();
      }
    };

    function saveCart() {
      localStorage.setItem("cart", JSON.stringify(cart));
    }

    function showPopup(msg) {
      let popup = document.getElementById("popup");
      popup.textContent = msg;
      popup.classList.add("show");
      setTimeout(() => {
        popup.classList.remove("show");
      }, 3000);
    }

    function addToCart(name, price) {
      let item = cart.find(p => p.name === name);
      if (item) {
        item.qty++;
      } else {
        cart.push({ name, price, qty: 1 });
      }
      saveCart();
      renderCart();
      showPopup(name + " berhasil ditambahkan ke keranjang ✅");
    }

    function removeFromCart(index) {
      cart.splice(index, 1);
      saveCart();
      renderCart();
    }

    function updateQty(index, value) {
      if (value < 1) value = 1;
      cart[index].qty = parseInt(value);
      saveCart();
      renderCart();
    }

    function clearCart() {
      cart = [];
      saveCart();
      renderCart();
      showPopup("Keranjang sudah dikosongkan ❌");
    }

    function renderCart() {
      let cartList = document.getElementById("cart-items");
      cartList.innerHTML = "";

      let total = 0;

      cart.forEach((item, index) => {
        let li = document.createElement("li");
        let harga = parseInt(item.price.replace(/[^0-9]/g, ""));
        let subtotal = harga * item.qty;
        total += subtotal;

        li.innerHTML = `
          ${item.name} - ${item.price} x 
          <input type="number" value="${item.qty}" min="1" style="width:50px;text-align:center" onchange="updateQty(${index}, this.value)">
          = Rp ${subtotal.toLocaleString()}
        `;

        let removeBtn = document.createElement("span");
        removeBtn.textContent = " ❌";
        removeBtn.className = "removeBtn";
        removeBtn.onclick = () => removeFromCart(index);
        li.appendChild(removeBtn);

        cartList.appendChild(li);
      });

      document.querySelector(".total").textContent = "Total: Rp " + total.toLocaleString();

      let checkoutBtns = document.getElementById("checkout-buttons");
      let clearCartBtn = document.getElementById("clearCartBtn");

      if (cart.length > 0) {
        checkoutBtns.style.display = "block";
        clearCartBtn.style.display = "inline-block";

        let message = "Hallo Teteh, saya ingin memesan:%0A";
        cart.forEach(item => {
          message += `- ${item.name} (${item.price}) x ${item.qty}%0A`;
        });
        message += `%0ATotal: Rp ${total.toLocaleString()}`;

        let Rohma = "6283152859084";
        let Diana = "6281280279925";
        let Rindu = "6289531547651";
        let Najwa = "6281779419293";

        document.getElementById("checkout1").href = "https://wa.me/" + Rohma + "?text=" + message;
        document.getElementById("checkout2").href = "https://wa.me/" + Diana + "?text=" + message;
        document.getElementById("checkout3").href = "https://wa.me/" + Rindu + "?text=" + message;
        document.getElementById("checkout4").href = "https://wa.me/" + Najwa + "?text=" + message;
      } else {
        checkoutBtns.style.display = "none";
        clearCartBtn.style.display = "none";
      }
    }
  </script>
  <footer>
  <p>&copy; 2025 Toko RIMBERIO.NET - Semua Hak Dilindungi</p>
  <p>Alamat: Jl. Nyimas Rara Kerta, Kec. Jamblang, Kab. Cirebon, SMKN 1 JAMBLANG, Kelas XI TJKT</p>
  <p>WhatsApp: <a href="https://wa.me/6283152859084" style="color:white; text-decoration:underline;">+62 831-5285-9084</a></p>
</footer>
</body>
</html>
