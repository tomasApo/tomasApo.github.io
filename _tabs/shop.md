---
layout: page
icon: fas fa-stream
order: 1
---
<div class="mx-master-container">
  <img src="/assets/img/mx_master_pic.png" alt="MX Master Mod" class="mx-master-img">

  <div class="mx-master-content">
    <h2 class="title">MX Master USB-C Mod</h2>
    <p class="mx-text">Upgrade your Logitech MX Master to USB-C with this sleek conversion kit.</p>
    
    <div class="shop-buttons">
      <a href="https://www.tindie.com/products/33549/" class="shop-btn eu-shop">Buy in EU</a>
      <a href="https://www.elecrow.com/mx-master-usb-c-conversion-kit.html" class="shop-btn intl-shop">Buy International</a>
    </div>
  </div>
</div>
<div class="mx-master-container">
  <img src="/assets/img/hinge-swivel/shop_pic.jpeg" alt="metal-hinge" class="mx-master-img">

   <div class="mx-master-content">
    <h2 class="title">Sony WH-1000XM4 Metal Hinge swivel</h2>
    <p class="mx-text">Replace the fragile origanl sony hinge with this stainless steel part</p>
    
    <div class="shop-buttons">
      <a href="https://www.tindie.com/products/37706/" class="shop-btn eu-shop">Buy in EU</a>
     <!-- <a href="https://www.elecrow.com/mx-master-usb-c-conversion-kit.html" class="shop-btn intl-shop">Buy International</a>  -->
  </div>
</div>


<style>
/* Default light mode styles */
.mx-master-container {
  display: flex;
  align-items: center;
  justify-content: flex-start; /* 👈 Ensures left alignment for images */
  gap: 20px;
  padding: 20px;
  background: var(--card-bg);
  box-shadow: var(--card-shadow);
  margin-bottom: 20px;
}


.mx-master-img {
  max-width: 200px;
}

.mx-master-content {
  text-align: left;
}

.title {
  color: var(--heading-color);
}

.mx-text {
  color: var(--text-color);
}

.shop-buttons {
  margin-top: 10px;
  /* margin-top: auto;  */
}

.shop-btn {
  display: inline-block;
  padding: 10px 15px;
  margin-right: 10px;
  text-decoration: none;
  font-weight: 700;
  transition: 0.2s;
}

/* ApoloElectro buttons: graphite primary, amber secondary */
.eu-shop {
  background: var(--heading-color);
  color: var(--main-bg);
}

.intl-shop {
  background: #f2a21f;
  color: #121418;
}

.content .shop-buttons a.shop-btn {
  border-bottom: 0;
}

.shop-btn:hover {
  background: #f2a21f;
  color: #121418;
  text-decoration: none;
}

/* Dark mode styles */
/* @media (prefers-color-scheme: dark) {
  .mx-master-container {
    background: #1e1e1e; /* Dark mode background */
    box-shadow: 0px 4px 10px rgba(255, 255, 255, 0.1);
  

  .mx-title, .mx-text {
    color: #f8f9fa; /* Light text for dark mode */
  } */

</style>
