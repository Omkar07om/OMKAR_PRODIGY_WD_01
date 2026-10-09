from pathlib import Path

html = r'''<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<meta name="theme-color" content="#176b4d">
<meta name="description" content="Shop everyday essentials from your trusted local store. Place an order online and we'll contact you to confirm.">
<title>Apna Local Store | Everyday essentials</title>
<style>
:root{--green:#176b4d;--green-dark:#10523a;--mint:#eaf5ef;--cream:#fbfaf6;--ink:#1e2a24;--muted:#68756e;--line:#e4e9e4;--white:#fff;--orange:#f1a94e;--shadow:0 10px 30px rgba(22,65,45,.09)}
{box-sizing:border-box}html{scroll-behavior:smooth}body{margin:0;background:var(--cream);color:var(--ink);font-family:system-ui,-apple-system,BlinkMacSystemFont,"Segoe UI",sans-serif;line-height:1.5}button,input,textarea,select{font:inherit}button{cursor:pointer}button:focus-visible,a:focus-visible,input:focus-visible,textarea:focus-visible{outline:3px solid #e9ad55;outline-offset:3px}a{color:inherit}.wrap{width:min(1120px,calc(100% - 32px));margin:auto}.topline{background:var(--green-dark);color:#fff;text-align:center;padding:8px 12px;font-size:.82rem}.header{background:rgba(255,255,255,.94);border-bottom:1px solid var(--line);position:sticky;top:0;z-index:20;backdrop-filter:blur(12px)}.head-inner{min-height:76px;display:flex;align-items:center;justify-content:space-between;gap:14px}.brand{display:flex;align-items:center;gap:11px;text-decoration:none;min-width:0}.logo{width:44px;height:44px;border-radius:14px;background:var(--green);color:white;display:grid;place-items:center;font-size:1.4rem;flex:none}.brand-name{font-weight:850;letter-spacing:-.03em;font-size:1.12rem;line-height:1.2}.brand-tag{font-size:.78rem;color:var(--muted);margin-top:3px}.head-actions{display:flex;gap:9px;align-items:center}.btn{border:0;border-radius:12px;padding:11px 15px;font-weight:750;display:inline-flex;align-items:center;justify-content:center;gap:8px;transition:transform .18s,background .18s; text-decoration:none}.btn:active{transform:scale(.97)}.btn-primary{background:var(--green);color:#fff}.btn-primary:hover{background:var(--green-dark)}.btn-light{background:var(--mint);color:var(--green)}.cart-count{background:#fff;color:var(--green);font-size:.75rem;border-radius:999px;min-width:22px;height:22px;display:inline-grid;place-items:center;padding:0 5px}.hero{padding:34px 0 26px}.hero-card{background:linear-gradient(115deg,#eaf5ef 0%,#f4f7e9 62%,#fff0d9 100%);border-radius:25px;padding:clamp(24px,5vw,52px);display:grid;grid-template-columns:1.3fr .7fr;align-items:center;gap:20px;overflow:hidden}.eyebrow{color:var(--green);font-size:.78rem;text-transform:uppercase;letter-spacing:.13em;font-weight:850}.hero h1{font-size:clamp(2rem,5vw,3.5rem);line-height:1.04;letter-spacing:-.055em;margin:12px 0}.hero p{color:#52635a;max-width:520px;margin:0 0 22px}.hero-art{display:grid;place-items:center;font-size:clamp(6rem,16vw,10rem);filter:drop-shadow(0 14px 8px #45634b22);transform:rotate(-5deg)}.benefits{display:flex;gap:16px;flex-wrap:wrap;margin-top:18px;color:#52635a;font-size:.85rem}.benefits span{display:flex;align-items:center;gap:6px}.section-head{display:flex;align-items:end;justify-content:space-between;gap:12px;margin:22px 0 16px}.section-head h2{margin:0;font-size:1.6rem;letter-spacing:-.04em}.section-head p{margin:4px 0 0;color:var(--muted);font-size:.9rem}.search{width:min(100%,260px);border:1px solid var(--line);border-radius:12px;background:#fff;padding:10px 13px}.filters{display:flex;gap:8px;overflow-x:auto;padding:2px 0 14px;scrollbar-width:thin}.filter{border:1px solid var(--line);background:#fff;color:#506057;padding:9px 15px;border-radius:999px;white-space:nowrap;font-weight:700;font-size:.88rem}.filter.active,.filter:hover{background:var(--green);border-color:var(--green);color:white}.products{display:grid;grid-template-columns:repeat(4,minmax(0,1fr));gap:16px;padding-bottom:42px}.product{background:#fff;border:1px solid var(--line);border-radius:18px;overflow:hidden;display:flex;flex-direction:column;transition:transform .2s,box-shadow .2s;min-width:0}.product:hover{transform:translateY(-3px);box-shadow:var(--shadow)}.product-img{width:100%;aspect-ratio:1.28;object-fit:cover;background:#f0f2ec}.product-info{padding:13px;display:flex;flex-direction:column;flex:1}.category-label{font-size:.7rem;font-weight:800;text-transform:uppercase;letter-spacing:.08em;color:var(--green)}.product h3{font-size:1rem;line-height:1.3;margin:5px 0 4px}.description{font-size:.82rem;color:var(--muted);margin:0 0 12px;flex:1}.product-bottom{display:flex;align-items:center;justify-content:space-between;gap:8px;margin-top:auto}.price{font-size:1.1rem;font-weight:850;white-space:nowrap}.add-btn{border:0;border-radius:10px;background:var(--mint);color:var(--green);font-weight:800;padding:9px 11px}.add-btn:hover{background:#d8ecdf}.empty{grid-column:1/-1;padding:36px 16px;text-align:center;color:var(--muted);background:#fff;border:1px dashed var(--line);border-radius:16px}.footer{background:#173c2d;color:#fff;padding:28px 0 90px}.footer-inner{display:flex;align-items:start;justify-content:space-between;gap:20px;flex-wrap:wrap}.footer p{color:#c7d8ce;margin:6px 0;font-size:.9rem}.footer a{color:#fff}.floating-cart{position:fixed;right:18px;bottom:18px;z-index:30;box-shadow:0 8px 28px #123e2b3d;border-radius:999px;padding:14px 19px}.whatsapp{position:fixed;left:18px;bottom:18px;z-index:29;border-radius:999px;padding:13px 16px;background:#168b51;color:white;text-decoration:none;font-weight:800;box-shadow:0 8px 25px #123e2b2b}.overlay{position:fixed;inset:0;background:#14251dc0;z-index:50;display:none;align-items:flex-end;justify-content:center;padding:0}.overlay.open{display:flex}.modal{background:var(--cream);width:min(620px,100%);max-height:92dvh;overflow:auto;border-radius:24px 24px 0 0;padding:20px;box-shadow:0 -10px 50px #0002;animation:rise .22s ease-out}.modal-head{display:flex;justify-content:space-between;align-items:center;gap:12px;position:sticky;top:-20px;background:var(--cream);padding:2px 0 13px;z-index:2}.modal-head h2{margin:0;font-size:1.35rem}.icon-btn{width:38px;height:38px;border:1px solid var(--line);background:white;border-radius:50%;font-size:1.15rem}.cart-line{display:grid;grid-template-columns:60px 1fr auto;gap:12px;align-items:center;padding:13px 0;border-bottom:1px solid var(--line)}.cart-line img{width:60px;height:60px;object-fit:cover;border-radius:12px;background:#eee}.line-title{font-weight:800;font-size:.92rem}.line-price{font-weight:800;white-space:nowrap}.line-sub{font-size:.82rem;color:var(--muted)}.quantity{display:flex;align-items:center;gap:10px;margin-top:7px}.quantity button{width:29px;height:29px;border:1px solid var(--line);background:white;border-radius:9px;font-weight:900}.remove{border:0;background:transparent;color:#b14a3d;font-size:.8rem;text-decoration:underline;margin-left:3px}.total-row{display:flex;justify-content:space-between;align-items:center;padding:18px 0;font-weight:850;font-size:1.08rem}.total-row strong{font-size:1.35rem}.full{width:100%}.note{font-size:.8rem;color:var(--muted);margin:8px 0 14px}.form-grid{display:grid;gap:13px}.field label{display:block;font-weight:750;font-size:.87rem;margin-bottom:5px}.field input,.field textarea{width:100%;border:1px solid #d7dfd8;border-radius:11px;padding:12px;background:#fff;color:var(--ink)}.field textarea{min-height:82px;resize:vertical}.field input:focus,.field textarea:focus{border-color:var(--green)}.form-error{color:#a12f24;font-size:.86rem;margin:10px 0}.confirmation{text-align:center;padding:18px 8px 10px}.success-icon{width:68px;height:68px;border-radius:50%;background:#dff3e5;color:var(--green);display:grid;place-items:center;font-size:2rem;margin:0 auto 15px}.confirmation h3{font-size:1.5rem;margin:0 0 8px}.confirmation p{color:var(--muted)}.hidden{display:none!important}.toast{position:fixed;bottom:88px;left:50%;transform:translate(-50%,12px);opacity:0;pointer-events:none;z-index:80;background:#183e2e;color:white;padding:11px 17px;border-radius:999px;font-weight:700;font-size:.9rem;transition:.2s;white-space:nowrap}.toast.show{opacity:1;transform:translate(-50%,0)}@keyframes rise{from{transform:translateY(20px);opacity:.7}to{transform:translateY(0);opacity:1}}@media(min-width:700px){.overlay{align-items:center;padding:20px}.modal{border-radius:24px;max-height:88dvh}.whatsapp{bottom:20px}.floating-cart{bottom:20px}}@media(max-width:850px){.products{grid-template-columns:repeat(3,minmax(0,1fr))}.hero-card{grid-template-columns:1fr .45fr}.hero-art{font-size:7rem}}@media(max-width:600px){.wrap{width:min(100% - 24px,520px)}.topline{font-size:.76rem}.head-inner{min-height:68px}.logo{width:39px;height:39px}.brand-name{font-size:1rem}.brand-tag{font-size:.7rem}.head-actions .btn{padding:9px 11px;font-size:.84rem}.hero{padding-top:18px}.hero-card{grid-template-columns:1fr;padding:25px 22px;border-radius:20px}.hero-art{display:none}.hero h1{font-size:2.35rem}.section-head{align-items:stretch;flex-direction:column}.search{width:100%}.products{grid-template-columns:repeat(2,minmax(0,1fr));gap:10px}.product{border-radius:15px}.product-info{padding:10px}.product h3{font-size:.92rem}.description{font-size:.77rem}.price{font-size:1rem}.add-btn{padding:8px 9px;font-size:.8rem}.floating-cart{right:12px;bottom:12px;padding:12px 15px}.whatsapp{left:12px;bottom:12px;padding:12px 13px;font-size:.84rem}.footer{padding-bottom:82px}.cart-line{grid-template-columns:52px 1fr auto;gap:9px}.cart-line img{width:52px;height:52px}.modal{padding:17px}.toast{bottom:78px;font-size:.82rem;max-width:calc(100% - 24px);white-space:normal;text-align:center}}@media(prefers-reduced-motion:reduce){,::before,::after{scroll-behavior:auto!important;animation:none!important;transition:none!important}}
</style>
</head>
<body>
<div class="topline">Local love, everyday essentials · Order online, pay directly to the shop</div>
<header class="header"><div class="wrap head-inner">
<a class="brand" href="#" aria-label="Apna Local Store home"><span class="logo">🛍️</span><span><span class="brand-name" id="brandName">Apna Local Store</span><span class="brand-tag" id="brandTag">Everyday essentials, delivered with care</span></span></a>
<div class="head-actions"><button class="btn btn-light" id="headerCart" aria-label="Open shopping cart">🛒 <span class="cart-count" id="headerCount">0</span></button></div>
</div></header>
<main>
<section class="hero"><div class="wrap"><div class="hero-card">
<div><div class="eyebrow">Your neighbourhood shop</div><h1>Good things.<br>Right around the corner.</h1><p id="heroTag">Shop your daily favourites from a local business you can trust. Add items to your cart and send your order in just a few taps.</p><button class="btn btn-primary" onclick="document.querySelector('#shop').scrollIntoView({behavior:'smooth'})">Explore products <span aria-hidden="true">↓</span></button><div class="benefits"><span>✓ Simple ordering</span><span>✓ Local service</span><span>✓ No online payment</span></div></div>
<div class="hero-art" aria-hidden="true">🥬🍊</div>
</div></div></section>
<section class="wrap" id="shop">
<div class="section-head"><div><h2>Shop our products</h2><p>Fresh picks and everyday favourites.</p></div><input class="search" type="search" id="searchInput" placeholder="Search products…" aria-label="Search products"></div>
<div class="filters" id="filters" aria-label="Filter by category"></div>
<div class="products" id="products" aria-live="polite"></div>
</section>
</main>
<footer class="footer"><div class="wrap footer-inner"><div><strong id="footerName">Apna Local Store</strong><p id="footerTag">Everyday essentials, delivered with care</p><p id="shopLocation">📍 Bengaluru, Karnataka</p></div><div><strong>Need help?</strong><p>Call or WhatsApp: <a id="footerPhone" href="https://wa.me/919876543210">+91 98765 43210</a></p><p>Orders are confirmed by the shop before delivery.</p></div></div></footer>
<a class="whatsapp" id="whatsappFloat" href="https://wa.me/919876543210" target="_blank" rel="noopener" aria-label="Chat with the shop on WhatsApp">☏ Chat on WhatsApp</a>
<button class="btn btn-primary floating-cart" id="floatingCart">🛒 View cart <span class="cart-count" id="floatCount">0</span></button>
<div class="overlay" id="cartOverlay" role="dialog" aria-modal="true" aria-labelledby="cartTitle"><div class="modal">
<div class="modal-head"><h2 id="cartTitle">Your cart</h2><button class="icon-btn" id="closeCart" aria-label="Close cart">×</button></div>
<div id="cartContents"></div>
<div id="cartFooter" class="hidden"><div class="total-row"><span>Grand total</span><strong id="grandTotal">₹0</strong></div><p class="note">This is an order request, not a payment. The shop will confirm availability and delivery details.</p><button class="btn btn-primary full" id="checkoutBtn">Continue to checkout →</button></div>
</div></div>
<div class="overlay" id="checkoutOverlay" role="dialog" aria-modal="true" aria-labelledby="checkoutTitle"><div class="modal">
<div class="modal-head"><h2 id="checkoutTitle">Delivery details</h2><button class="icon-btn" id="closeCheckout" aria-label="Close checkout">×</button></div>
<div id="checkoutFormWrap"><p class="note">Enter your details and send your order to the shop. No payment is collected on this website.</p>
<form id="orderForm" class="form-grid">
<div class="field"><label for="customerName">Your name *</label><input id="customerName" name="customer_name" autocomplete="name" required maxlength="100" placeholder="Full name"></div>
<div class="field"><label for="customerPhone">Phone number *</label><input id="customerPhone" name="customer_phone" type="tel" autocomplete="tel" required maxlength="20" placeholder="e.g. 98765 43210"></div>
<div class="field"><label for="customerAddress">Delivery address *</label><textarea id="customerAddress" name="delivery_address" autocomplete="street-address" required maxlength="600" placeholder="House/flat, street, area, landmark"></textarea></div>
<div class="field"><label for="instructions">Special instructions (optional)</label><textarea id="instructions" name="instructions" maxlength="600" placeholder="Preferred delivery time, substitutions, etc."></textarea></div>
<input type="hidden" name="order_summary" id="orderSummaryField">
<input type="hidden" name="grand_total" id="orderTotalField">
<input type="hidden" name="_subject" id="emailSubject" value="New order from Apna Local Store">
<div id="formError" class="form-error" role="alert"></div>
<button type="submit" class="btn btn-primary full" id="submitOrder">Send order request</button>
<p class="note">Your order is sent to the shop for confirmation. Please do not submit payment details here.</p>
</form></div>
<div id="confirmation" class="confirmation hidden"><div class="success-icon">✓</div><h3>Order request sent!</h3><p id="confirmationText">Apna Local Store will contact you on WhatsApp to confirm.</p><a class="btn btn-primary" id="confirmationWhatsApp" href="https://wa.me/919876543210" target="_blank" rel="noopener">Message us on WhatsApp</a><button class="btn btn-light full" style="margin-top:10px" id="doneBtn">Back to shop</button></div>
</div></div>
<div class="toast" id="toast" role="status" aria-live="polite"></div>
<script>
/* ===================== SHOP SETUP =====================
   1) Replace these values with your real shop details.
   2) Create a free form at https://formspree.io/ and paste its endpoint
      into FORMSPREE_ENDPOINT, e.g. https://formspree.io/f/abcdefgh.
   3) Replace the sample image URLs below with direct imgbb image URLs.
   Until Formspree is configured, orders are NOT emailed; the page will
   show a clear setup error rather than pretending an order was sent.
======================================================== */
const SHOP = {
  name: "Apna Local Store",
  tagline: "Everyday essentials, delivered with care",
  location: "Bengaluru, Karnataka",
  phoneDisplay: "+91 98765 43210",
  whatsapp: "919876543210", // country code + number, digits only
  ownerEmail: "orders@example.com" // informational; Formspree delivers to your verified inbox
};
const FORMSPREE_ENDPOINT = "https://formspree.io/f/YOUR_FORM_ID";

const PRODUCTS = [
 {id:"atta",name:"Whole Wheat Atta (5kg)",price:280,category:"Groceries",description:"Everyday whole wheat flour for soft rotis.",image:"https://images.unsplash.com/photo-1627485937980-221c88ac04f9?auto=format&fit=crop&w=700&q=80",alt:"Whole wheat flour in a bowl"},
 {id:"rice",name:"Daily Rice (5kg)",price:340,category:"Groceries",description:"A pantry staple for your everyday meals.",image:"https://images.unsplash.com/photo-1586201375761-83865001e31c?auto=format&fit=crop&w=700&q=80",alt:"Uncooked white rice grains"},
 {id:"dal",name:"Toor Dal (1kg)",price:155,category:"Groceries",description:"Protein-rich lentils for comforting dal.",image:"https://images.unsplash.com/photo-1515543904379-3d757adores?auto=format&fit=crop&w=700&q=80",alt:"Dry lentils and pulses"},
 {id:"oil",name:"Sunflower Oil (1L)",price:145,category:"Groceries",description:"A kitchen essential for daily cooking.",image:"https://images.unsplash.com/photo-1474979266404-7eaacbcd87c5?auto=format&fit=crop&w=700&q=80",alt:"Cooking oil in a glass bottle"},
 {id:"milk",name:"Fresh Milk (1L)",price:64,category:"Dairy",description:"A daily favourite for tea, coffee and breakfast.",image:"https://images.unsplash.com/photo-1563636619-e9143da7973b?auto=format&fit=crop&w=700&q=80",alt:"Glass of fresh milk"},
 {id:"butter",name:"Butter (100g)",price:58,category:"Dairy",description:"Creamy butter for toast and cooking.",image:"https://images.unsplash.com/photo-1589985270826-4b7bb135bc9d?auto=format&fit=crop&w=700&q=80",alt:"Fresh butter on a plate"},
 {id:"bread",name:"Milk Bread",price:45,category:"Bakery",description:"Soft sliced bread for quick breakfasts.",image:"https://images.unsplash.com/photo-1509440159596-0249088772ff?auto=format&fit=crop&w=700&q=80",alt:"Freshly baked bread loaf"},
 {id:"biscuits",name:"Butter Biscuits",price:35,category:"Snacks",description:"A crunchy companion for your chai break.",image:"https://images.unsplash.com/photo-1558961363-fa8fdf82db35?auto=format&fit=crop&w=700&q=80",alt:"Biscuits arranged on a plate"},
 {id:"apples",name:"Fresh Apples (1kg)",price:180,category:"Fruits",description:"Crisp fruit for a refreshing snack.",image:"https://images.unsplash.com/photo-1560806887-1e4cd0b6cbd6?auto=format&fit=crop&w=700&q=80",alt:"Fresh red apples"},
 {id:"bananas",name:"Bananas (6 pcs)",price:50,category:"Fruits",description:"Naturally sweet and ready to enjoy.",image:"https://images.unsplash.com/photo-1571771894821-ce9b6c11b08e?auto=format&fit=crop&w=700&q=80",alt:"A bunch of ripe bananas"},
 {id:"juice",name:"Orange Juice (1L)",price:120,category:"Beverages",description:"A fruity drink for a bright start.",image:"https://images.unsplash.com/photo-1600271886742-f049cd451bba?auto=format&fit=crop&w=700&q=80",alt:"Glass of orange juice"},
 {id:"tea",name:"Assam Tea (250g)",price:135,category:"Beverages",description:"A robust, comforting cup of everyday tea.",image:"https://images.unsplash.com/photo-1544787219-7f47ccb76574?auto=format&fit=crop&w=700&q=80",alt:"A cup of freshly brewed tea"}
];
const money = n => new Intl.NumberFormat("en-IN",{style:"currency",currency:"INR",maximumFractionDigits:2}).format(n);
const $ = id => document.getElementById(id);
let activeCategory = "All";
let cart = loadCart();
function loadCart(){try{const saved=JSON.parse(localStorage.getItem("apna-store-cart")||"{}");return saved&&typeof saved==="object"?saved:{}}catch{return {}}}
function saveCart(){try{localStorage.setItem("apna-store-cart",JSON.stringify(cart))}catch{}}
function safeText(value){return String(value).replace(/[&<>"']/g,c=>({"&":"&amp;","<":"&lt;",">":"&gt;",'"':"&quot;","'":"&#39;"}[c]))}
function setupShop(){
 $("brandName").textContent=SHOP.name;$("footerName").textContent=SHOP.name;
 $("brandTag").textContent=SHOP.tagline;$("footerTag").textContent=SHOP.tagline;$("heroTag").textContent=SHOP.tagline+" Shop your daily favourites from a local business you can trust. Add items to your cart and send your order in just a few taps.";
 $("shopLocation").textContent="📍 "+SHOP.location;$("footerPhone").textContent=SHOP.phoneDisplay;
 const wa="https://wa.me/"+SHOP.whatsapp;
 $("footerPhone").href=wa;$("whatsappFloat").href=wa;$("confirmationWhatsApp").href=wa;
 $("emailSubject").value="New order for "+SHOP.name;
 document.title=SHOP.name+" | Shop local";
}
function categories(){return ["All",...new Set(PRODUCTS.map(p=>p.category))]}
function renderFilters(){
 $("filters").innerHTML=categories().map(c=><button class="filter ${c===activeCategory?"active":""}" data-category="${safeText(c)}" aria-pressed="${c===activeCategory}">${safeText(c)}</button>).join("");
 $("filters").querySelectorAll("button").forEach(b=>b.addEventListener("click",()=>{activeCategory=b.dataset.category;renderFilters();renderProducts()}));
}
function renderProducts(){
 const q=$("searchInput").value.trim().toLowerCase();
 const list=PRODUCTS.filter(p=>(activeCategory==="All"||p.category===activeCategory)&&(${p.name} ${p.description} ${p.category}).toLowerCase().includes(q));
 $("products").innerHTML=list.length?list.map(p=><article class="product"><img class="product-img" src="${safeText(p.image)}" alt="${safeText(p.alt)}" loading="lazy" decoding="async" onerror="this.onerror=null;this.style.visibility='hidden';this.parentElement.style.background='#eef3ed'"><div class="product-info"><div class="category-label">${safeText(p.category)}</div><h3>${safeText(p.name)}</h3><p class="description">${safeText(p.description)}</p><div class="product-bottom"><span class="price">${money(p.price)}</span><button class="add-btn" data-add="${safeText(p.id)}" aria-label="Add ${safeText(p.name)} to cart">＋ Add</button></div></div></article>).join(""):<div class="empty">No products found. Try another search or category.</div>;
 $("products").querySelectorAll("[data-add]").forEach(b=>b.addEventListener("click",()=>addToCart(b.dataset.add)));
}
function cartItems(){return Object.entries(cart).map(([id,qty])=>({product:PRODUCTS.find(p=>p.id===id),qty:Number(qty)})).filter(x=>x.product&&Number.isFinite(x.qty)&&x.qty>0)}
function countItems(){return cartItems().reduce((s,x)=>s+x.qty,0)}
function cartTotal(){return cartItems().reduce((s,x)=>s+x.product.price*x.qty,0)}
function updateCounts(){$("headerCount").textContent=countItems();$("floatCount").textContent=countItems()}
function addToCart(id){if(!PRODUCTS.some(p=>p.id===id))return;cart[id]=(Number(cart[id])||0)+1;saveCart();updateCounts();renderCart();showToast("Added to cart ✓")}
function changeQty(id,delta){const next=(Number(cart[id])||0)+delta;if(next<=0)delete cart[id];else cart[id]=next;saveCart();updateCounts();renderCart()}
function removeItem(id){delete cart[id];saveCart();updateCounts();renderCart();showToast("Item removed")}
function renderCart(){
 const items=cartItems();$("cartFooter").classList.toggle("hidden",!items.length);
 if(!items.length){$("cartContents").innerHTML='<div class="empty">🛒<br><strong>Your cart is empty</strong><br>Add a few favourites to get started.</div>'}
 else{$("cartContents").innerHTML=items.map(({product:p,qty})=><div class="cart-line"><img src="${safeText(p.image)}" alt="${safeText(p.alt)}" loading="lazy"><div><div class="line-title">${safeText(p.name)}</div><div class="line-sub">${money(p.price)} each · Subtotal: <strong>${money(p.price*qty)}</strong></div><div class="quantity"><button data-change="${safeText(p.id)}" data-delta="-1" aria-label="Decrease ${safeText(p.name)} quantity">−</button><strong>${qty}</strong><button data-change="${safeText(p.id)}" data-delta="1" aria-label="Increase ${safeText(p.name)} quantity">+</button><button class="remove" data-remove="${safeText(p.id)}">Remove</button></div></div><div class="line-price">${money(p.price*qty)}</div></div>).join("");}
 $("grandTotal").textContent=money(cartTotal());
 $("cartContents").querySelectorAll("[data-change]").forEach(b=>b.addEventListener("click",()=>changeQty(b.dataset.change,Number(b.dataset.delta))));
 $("cartContents").querySelectorAll("[data-remove]").forEach(b=>b.addEventListener("click",()=>removeItem(b.dataset.remove)));
}
function openOverlay(id){$(id).classList.add("open");document.body.style.overflow="hidden"}
function closeOverlay(id){$(id).classList.remove("open");if(!$("cartOverlay").classList.contains("open")&&!$("checkoutOverlay").classList.contains("open"))document.body.style.overflow=""}
function showToast(msg){const t=$("toast");t.textContent=msg;t.classList.add("show");clearTimeout(showToast.timer);showToast.timer=setTimeout(()=>t.classList.remove("show"),1800)}
function orderSummary(){
 return cartItems().map(({product:p,qty})=>${p.name} | Qty: ${qty} | Unit price: ${money(p.price)} | Subtotal: ${money(p.price*qty)}).join("\n")+"\n\nGRAND TOTAL: "+money(cartTotal());
}
function openCheckout(){
 if(!cartItems().length){showToast("Your cart is empty");return}
 $("formError").textContent="";$("orderSummaryField").value=orderSummary();$("orderTotalField").value=money(cartTotal());
 $("checkoutFormWrap").classList.remove("hidden");$("confirmation").classList.add("hidden");closeOverlay("cartOverlay");openOverlay("checkoutOverlay");
}
$("headerCart").addEventListener("click",()=>{renderCart();openOverlay("cartOverlay")});
$("floatingCart").addEventListener("click",()=>{renderCart();openOverlay("cartOverlay")});
$("closeCart").addEventListener("click",()=>closeOverlay("cartOverlay"));
$("closeCheckout").addEventListener("click",()=>closeOverlay("checkoutOverlay"));
$("checkoutBtn").addEventListener("click",openCheckout);
$("doneBtn").addEventListener("click",()=>{closeOverlay("checkoutOverlay");window.scrollTo({top:0,behavior:"smooth"})});
$("searchInput").addEventListener("input",renderProducts);
["cartOverlay","checkoutOverlay"].forEach(id=>$(id).addEventListener("click",e=>{if(e.target===$(id))closeOverlay(id)}));
document.addEventListener("keydown",e=>{if(e.key==="Escape"){closeOverlay("cartOverlay");closeOverlay("checkoutOverlay")}});
$("orderForm").addEventListener("submit",async e=>{
 e.preventDefault();const error=$("formError");error.textContent="";
 if(!cartItems().length){error.textContent="Your cart is empty. Please add items before ordering.";return}
 if(!/^https:\/\/formspree\.io\/f\/[A-Za-z0-9]+$/.test(FORMSPREE_ENDPOINT)||FORMSPREE_ENDPOINT.includes("YOUR_FORM_ID")){
   error.textContent="Shop setup needed: add your real Formspree endpoint in the HTML before sending orders. Your order has not been sent.";return;
 }
 const button=$("submitOrder");button.disabled=true;button.textContent="Sending order…";
 $("orderSummaryField").value=orderSummary();$("orderTotalField").value=money(cartTotal());
 const payload=new FormData(e.currentTarget);
 payload.append("shop_name",SHOP.name);payload.append("shop_location",SHOP.location);payload.append("shop_whatsapp",SHOP.phoneDisplay);payload.append("shop_owner_email_reference",SHOP.ownerEmail);
 try{
   const response=await fetch(FORMSPREE_ENDPOINT,{method:"POST",body:payload,headers:{"Accept":"application/json"}});
   if(!response.ok)throw new Error("The order service did not accept the request. Please try again or message the shop on WhatsApp.");
   cart={};saveCart();updateCounts();renderCart();e.currentTarget.reset();
   $("checkoutFormWrap").classList.add("hidden");$("confirmation").classList.remove("hidden");
   $("confirmationText").textContent="Order placed! "+SHOP.name+" will contact you on WhatsApp to confirm.";
 }catch(err){error.textContent=(err&&err.message)||"Could not send your order. Please try again or contact the shop on WhatsApp."}
 finally{button.disabled=false;button.textContent="Send order request"}
});
setupShop();renderFilters();renderProducts();renderCart();updateCounts();
</script>
</body>
</html>'''

path = Path("/mnt/data/apna-local-store.html")
path.write_text(html, encoding="utf-8")
print(f"Created {path} ({path.stat().st_size:,} bytes)")
