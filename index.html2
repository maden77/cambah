<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Kecambah Sehat - Neon Glitch Edition</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* Animasi Neon Kelap-Kelip */
        @keyframes flicker {
            0%, 18%, 22%, 25%, 53%, 57%, 100% {
                text-shadow: 
                    0 0 4px #fff,
                    0 0 11px #fff,
                    0 0 19px var(--neon-green),
                    0 0 40px var(--neon-green),
                    0 0 80px var(--neon-green);
                opacity: 1;
            }
            20%, 24%, 55% {
                text-shadow: none;
                opacity: 0.5;
            }
        }

        @keyframes pulse {
            0% { box-shadow: 0 0 5px var(--neon-green), inset 0 0 5px var(--neon-green); }
            50% { box-shadow: 0 0 20px var(--neon-green), inset 0 0 10px var(--neon-green); }
            100% { box-shadow: 0 0 5px var(--neon-green), inset 0 0 5px var(--neon-green); }
        }

        @keyframes border-flicker {
            0%, 19%, 21%, 23%, 25%, 54%, 56%, 100% { border-color: var(--neon-green); box-shadow: var(--neon-shadow); }
            20%, 24%, 55% { border-color: #111; box-shadow: none; }
        }

        :root {
            --bg-dark: #050505;
            --neon-green: #39ff14;
            --neon-orange: #ff9e00;
            --neon-pink: #ff0055;
            --text-color: #e0e0e0;
            --glass-bg: rgba(255, 255, 255, 0.02);
            --neon-shadow: 0 0 10px var(--neon-green), 0 0 5px var(--neon-green);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Orbitron', sans-serif;
        }

        body {
            background: var(--bg-dark);
            color: var(--text-color);
            overflow-x: hidden;
            position: relative;
        }

        /* Efek Garis Scan TV Tua */
        body::before {
            content: "";
            position: fixed;
            top: 0; left: 0; width: 100%; height: 100%;
            background: linear-gradient(rgba(18, 16, 16, 0) 50%, rgba(0, 0, 0, 0.25) 50%), 
                        linear-gradient(90deg, rgba(255, 0, 0, 0.06), rgba(0, 255, 0, 0.02), rgba(0, 0, 255, 0.06));
            background-size: 100% 4px, 3px 100%;
            z-index: 1000;
            pointer-events: none;
        }

        .container {
            width: 90%;
            max-width: 1200px;
            margin: auto;
        }

        /* HEADER */
        header {
            background: rgba(0, 0, 0, 0.9);
            position: sticky;
            top: 0;
            z-index: 999;
            border-bottom: 2px solid var(--neon-green);
            animation: border-flicker 5s infinite;
        }

        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 15px 0;
        }

        .logo {
            font-size: 1.8rem;
            color: var(--neon-green);
            font-weight: bold;
            text-transform: uppercase;
            letter-spacing: 3px;
            animation: flicker 3s infinite;
        }

        .logo span {
            color: var(--neon-orange);
            text-shadow: 0 0 10px var(--neon-orange);
        }

        /* HERO */
        .hero {
            position: relative;
            background: linear-gradient(rgba(0,0,0,0.85), rgba(0,0,0,0.85)),
                        url('https://images.unsplash.com/photo-1589923186741-b7d59d6b2c4a');
            background-size: cover;
            background-position: center;
            padding: 150px 0;
            text-align: center;
            border-bottom: 1px solid var(--neon-pink);
        }

        .hero h2 {
            font-size: 4rem;
            margin-bottom: 15px;
            color: #fff;
            text-shadow: 0 0 20px var(--neon-green);
            animation: flicker 4s infinite reverse;
        }

        .hero p {
            font-size: 1.4rem;
            color: var(--neon-orange);
            letter-spacing: 5px;
            text-transform: uppercase;
        }

        /* BUTTONS */
        .btn {
            background: var(--bg-dark);
            color: var(--neon-green);
            padding: 15px 40px;
            border: 2px solid var(--neon-green);
            cursor: pointer;
            font-weight: bold;
            text-transform: uppercase;
            transition: 0.2s;
            position: relative;
            overflow: hidden;
            box-shadow: var(--neon-shadow);
        }

        .btn:hover {
            background: var(--neon-green);
            color: #000;
            box-shadow: 0 0 50px var(--neon-green);
        }

        .btn-orange {
            border-color: var(--neon-orange);
            color: var(--neon-orange);
            box-shadow: 0 0 10px var(--neon-orange);
        }

        /* PRODUCT CARDS */
        .products {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 40px;
            padding: 40px 0;
        }

        .product-card {
            background: #0a0a0a;
            border: 1px solid #222;
            border-radius: 5px;
            transition: 0.3s;
            position: relative;
        }

        .product-card:hover::before {
            content: "";
            position: absolute;
            top: 0; left: 0; right: 0; bottom: 0;
            border: 1px solid var(--neon-green);
            animation: pulse 1.5s infinite;
            pointer-events: none;
        }

        .product-img img {
            width: 100%;
            height: 250px;
            object-fit: cover;
            filter: grayscale(100%);
            transition: 0.5s;
        }

        .product-card:hover .product-img img {
            filter: grayscale(0%);
        }

        .product-info {
            padding: 25px;
            text-align: center;
        }

        .product-name {
            font-size: 1.2rem;
            margin-bottom: 10px;
            color: #fff;
        }

        .product-price {
            color: var(--neon-green);
            font-size: 1.5rem;
            margin-bottom: 20px;
        }

        /* CART ICON */
        .cart-icon {
            position: relative;
            font-size: 1.8rem;
            color: var(--neon-green);
            cursor: pointer;
            animation: flicker 5s infinite;
        }

        .cart-count {
            position: absolute;
            top: -10px;
            right: -12px;
            background: var(--neon-pink);
            color: #fff;
            padding: 2px 8px;
            font-size: 12px;
            box-shadow: 0 0 15px var(--neon-pink);
        }

        /* MARQUEE */
        .marquee {
            background: var(--neon-pink);
            color: #000;
            padding: 5px 0;
            font-size: 0.8rem;
            font-weight: bold;
            overflow: hidden;
            white-space: nowrap;
        }

        .marquee span {
            display: inline-block;
            padding-left: 100%;
            animation: marquee 20s linear infinite;
        }

        @keyframes marquee {
            0% { transform: translate(0, 0); }
            100% { transform: translate(-100%, 0); }
        }

        /* MODAL */
        .modal {
            display: none;
            position: fixed;
            top: 0; left: 0; width: 100%; height: 100%;
            background: rgba(0,0,0,0.9);
            justify-content: center;
            align-items: center;
            z-index: 1001;
        }

        .modal-content {
            background: #000;
            border: 3px solid var(--neon-green);
            width: 90%;
            max-width: 500px;
            padding: 30px;
            box-shadow: 0 0 50px rgba(57, 255, 20, 0.4);
        }

        .cart-item {
            display: flex;
            justify-content: space-between;
            border-bottom: 1px dashed #333;
            padding: 10px 0;
            color: #fff;
        }

        footer {
            border-top: 5px solid var(--neon-pink);
            padding: 60px 0;
            background: #000;
            margin-top: 50px;
        }
    </style>
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700;900&display=swap" rel="stylesheet">
</head>

<body>

<div class="marquee">
    <span> dari biji kacang hijau yang berkualitas baik, tumbuhlah tauge sehat segar kaya nutrisi !!! KECAMBAH ORGANIC KUALITAS TINGGI !!! HARGA TERBAIK  !!!</span>
</div>

<header>
  <div class="container header-container">
    <div class="logo">KECAMBAH<span>SEHAT</span></div>
    <div class="cart-icon" id="openCartBtn">
      <i class="fas fa-shopping-cart"></i>
      <span class="cart-count">0</span>
    </div>
  </div>
</header>

<section class="hero">
  <div class="container">
    <h2>PRODUK READY</h2>
    <p>FRESH SPROUTS INVENTORY</p>
    <br>
    <a href="#products" class="btn">LIHAT PRODUK</a>
  </div>
</section>

<section class="container" id="products" style="margin-top: 50px;">
  <div style="text-align: center; margin-bottom: 50px;">
    <h2 style="color: var(--neon-orange); font-size: 2.5rem; text-shadow: 0 0 10px var(--neon-orange);">PRODUK_LIST</h2>
  </div>
  <div class="products" id="products-container"></div>
</section>

<footer>
    <div class="container">
        <div style="display: grid; grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); gap: 40px;">
            <div>
                <h3 style="color: var(--neon-green);">INFO_CORE</h3>
                <p>Distributor kecambah organik terpercaya dengan sistem hidroponik modern.</p>
            </div>
            <div>
                <h3 style="color: var(--neon-pink);">CONTACT</h3>
                <p>WA: 0852-7513-5061</p>
            </div>
        </div>
    </div>
</footer>

<!-- MODAL KERANJANG -->
<div class="modal" id="cartModal">
  <div class="modal-content">
    <h3 style="color: var(--neon-green); margin-bottom: 20px;">CARGO_MANIFEST</h3>
    <div id="cartItems"></div>
    <div style="margin: 20px 0; text-align: right; border-top: 2px solid var(--neon-pink); padding-top: 15px;">
        <strong style="font-size: 1.4rem;">TOTAL: <span style="color: var(--neon-green);">Rp <span id="cartTotal">0</span></span></strong>
    </div>
    <div style="display: flex; gap: 10px;">
        <button class="btn btn-orange" id="closeCartBtn" style="flex:1; padding: 10px;">TUTUP</button>
        <button class="btn" id="checkoutBtn" style="flex:2; padding: 10px; border-color: #25D366; color: #25D366;">CHECKOUT WA</button>
    </div>
  </div>
</div>

<script>
const products = [
    { id: 1, name: "KECAMBAH HIJAU [A1]", price: 12000, img: "IMG_20251230_014159.jpg" },
    
];

let cart = [];

// Fungsi Render Produk
function renderProducts() {
    const container = document.getElementById("products-container");
    container.innerHTML = products.map(p => `
    <div class="product-card">
      <div class="product-img"><img src="${p.img}"></div>
      <div class="product-info">
        <h3 class="product-name">${p.name}</h3>
        <div class="product-price">Rp ${p.price.toLocaleString("id-ID")}</div>
        <button class="btn" onclick="addToCart(${p.id})">AMBIL</button>
      </div>
    </div>`).join("");
}

// Tambah ke Keranjang
function addToCart(id) {
    const p = products.find(x => x.id === id);
    const item = cart.find(i => i.id === id);
    if (item) {
        item.qty++;
    } else {
        cart.push({ ...p, qty: 1 });
    }
    updateUI();
}

// Update UI Keranjang
function updateUI() {
    const count = cart.reduce((s, i) => s + i.qty, 0);
    document.querySelector(".cart-count").textContent = count;
    
    const cartItemsDiv = document.getElementById("cartItems");
    if(cart.length === 0) {
        cartItemsDiv.innerHTML = "<p style='color:#444; text-align:center;'>KOSONG</p>";
    } else {
        cartItemsDiv.innerHTML = cart.map(i => `
            <div class="cart-item">
                <span>${i.name}</span>
                <span>x${i.qty} | Rp ${(i.qty * i.price).toLocaleString("id-ID")}</span>
            </div>
        `).join("");
    }
    
    const total = cart.reduce((s, i) => s + i.qty * i.price, 0);
    document.getElementById("cartTotal").textContent = total.toLocaleString("id-ID");
}

// Kontrol Modal
const modal = document.getElementById("cartModal");
const openBtn = document.getElementById("openCartBtn");
const closeBtn = document.getElementById("closeCartBtn");
const checkoutBtn = document.getElementById("checkoutBtn");

openBtn.addEventListener('click', () => {
    modal.style.display = "flex";
    updateUI();
});

closeBtn.addEventListener('click', () => {
    modal.style.display = "none";
});

// Tutup modal jika klik di luar box
window.addEventListener('click', (e) => {
    if (e.target == modal) modal.style.display = "none";
});

// Checkout WA
checkoutBtn.addEventListener('click', () => {
    if (cart.length === 0) return alert("Keranjang Kosong!");
    let total = cart.reduce((s, i) => s + i.qty * i.price, 0);
    let msg = "*ORDER KECAMBAH*%0A%0A";
    msg += cart.map(i => `- ${i.name} (x${i.qty})`).join("%0A");
    msg += `%0A%0A*TOTAL: Rp ${total.toLocaleString("id-ID")}*`;
    window.open(`https://wa.me/6285275135061?text=${msg}`);
});

renderProducts();
</script>

</body>
</html>

