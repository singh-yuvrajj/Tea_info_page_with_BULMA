<template>

    <!-- navigation -->

    <nav class="navbar has-shadow is-white" >
        <div class="navbar-brand">
            <a class="navbar-item px-6">
                <img src="@/assets/logo.png" 
                alt="brand logo" 
                >
            </a>
            <a  class="navbar-burger " id="burger" @click="toggleItems">
            <span></span>
            <span></span>
            <span></span>
        </a>
        </div>
        <div class="navbar-menu is-active" id="nav-links">
            <div class="navbar-end is-light">
                <a class="navbar-item has-text-weight-light ">My Account</a>
                <a class="navbar-item has-text-weight-light">Shopping Cart (0)</a>
            </div>
        </div>
       
       <!-- breadcumbs -->

    </nav>
    <div class="section pt-4 pb-0">
        <nav class="breadcrumb is-small has-arrow-separator" aria-label="breadcrumbs">
  <ul>
    <li><a href="#">Coffee Barista</a></li>
    <li><a href="#">Shop</a></li>
    <li class="is-active"><a href="#">Black Latte</a></li>
  </ul>
</nav>
    </div>

    <!-- product detail -->

    <section class="section">
        <div class="container">
            <div class="columns is-vcentered is-multiline">
                <div class="column is-6-tablet is-3-desktop">
                <p class="is-size-1 title">Latte</p>
                <p class="is-size-6">Lorem ipsum dolor sit amet consectetur adipisicing elit. Possimus unde voluptatum, necessitatibus obcaecati neque praesentium consectetur ipsa sunt ullam, culpa veritatis laborum architecto eos cumque facere repudiandae aspernatur itaque suscipit.</p>
                </div>
                <div class="column is-6-tablet is-5-desktop">
                    <img src="@/assets/product.png" alt="Black Latte">
                </div>
                <div class="column is-12-tablet is-4-desktop">
                    <div class="is-size-5 mb-2">Rs. 400/</div>
                    <p class="is-size-7 mb-4">Lorem ipsum dolor sit amet consectetur adipisicing elit. Similique, eius?</p>
                    
                    <div class="field">
                    <div class="control">
                        <div class="select is-small is-dark">
                        <select>
                            <option>Small(50 ml)</option>
                            <option>Large(100 ml)</option>
                        </select>
                        </div>
                    </div>
                    </div>
                    <button class="button is-primary is-normal">Add to Cart</button>
                </div>
            </div>
        </div>

        <!-- information -->

        <section class="section">
            <div class="container">
                <div class="columns is-8 is-variable">
                    <div class="column is-7-tablet">       
                    <div class="tabs is-boxed">
                        <ul>
                            <li class="is-active" id="product"  @click="currTab = 'product'">
                            <a>Product Detail
                            </a>
                            </li>
                            <li id="delivery" @click="currTab = 'delivery'">
                            <a>Delivery Detail
                            </a>
                            </li>
                        </ul>
                    </div>
                    <div class="px-2" id="tab-content">
                        <div id="product-details" >
                            <h3 class="is-size-5 title">Product Detail</h3>
                            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Hic temporibus asperiores totam omnis animi delectus, rerum harum magnam assumenda placeat?
                            </p>
                        </div>
                        <div id="delivery-details" class="is-hidden">
                            <h3 class="is-size-5 title">Delivery Detail</h3>
                            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Hic temporibus asperiores totam omnis animi delectus, rerum harum magnam assumenda placeat?
                            </p>
                        </div>
                    </div>
                    </div>
                    <div class="column is-5-tablet">
                       <div class="message">
                        <div class="message-header">
                            <p>Earn points with coffee club</p>
                        </div>
                        <div class="message-body">
                            <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Explicabo quos tempora, inventore nam, eaque similique, repellendus expedita repudiandae nesciunt quidem reprehenderit corporis molestiae natus nemo? Provident quis perspiciatis facilis neque.</p>
                        </div>
                        <div class="has-text-centered">
                            <button class="button mt-3 mb-3 is-primary" @click="modalStatus=!modalStatus">Sign Up</button>
                        </div>

                       </div>
                    </div>
                </div>
            </div>
        </section>
    </section>

    <!-- cards -->
<div class="section is-hidden-mobile">
    <div class="container ">
        <h3 class="has-text-centered is-size-5 title">Related Products</h3>
        <div class="columns is-centered has-text-centered mt-4 is-8 is-variable">
            <div class="column is-4-tablet is-3-desktop">
                <div class="card">
                <div class="card-image has-text-centered">
                    <img src="@/assets/p2.png" class="mt-2" alt="Placeholder image">
                </div>
                <div class="card-content">
                    <p>Rs. 100/</p>
                    <p class="title is-size-5 mt-1">
                    Lorem Cup 
                    </p>
                </div>
                <footer class="card-footer">
                <a class="card-footer-item">View Page</a>
  </footer>
                </div>
            </div>
            <div class="column is-4-tablet is-3-desktop">
                <div class="card">
                <div class="card-image has-text-centered">
                    <img src="@/assets/p2.png" class="mt-2" alt="Placeholder image">
                </div>
                <div class="card-content">
                    <p>Rs. 100/</p>
                    <p class="title is-size-5 mt-1">
                    Lorem Cup 
                    </p>
                </div>
                <footer class="card-footer">
                <a class="card-footer-item">View Page</a>
  </footer>
                </div>
            </div>
            <div class="column is-4-tablet is-3-desktop ">
                <div class="card">
                <div class="card-image has-text-centered">
                    <img src="@/assets/p2.png" class="mt-2" alt="Placeholder image">
                </div>
                <div class="card-content">
                    <p>Rs. 100/</p>
                    <p class="title is-size-5 mt-1">
                    Lorem Cup 
                    </p>
                </div>
                <footer class="card-footer">
                <a class="card-footer-item">View Page</a>
                </footer>
                </div>
            </div>
        </div>
        

    </div>
</div>

<!-- modal -->

<div class="modal" id="sign-up-modal">
  <div class="modal-background" @click="modalStatus=!modalStatus"></div>
  <div class="modal-content has-background-white px-5 py-5 mt-4"><h3 class="has-text-centered title mb-5">Join The Club</h3>
  <form>
    <div class="field">
  <p class="control has-icons-left">
    <input class="input" type="text" placeholder="UserName">
    <span class="icon is-small is-left">
      <i class="fas fa-user"></i>
    </span>
  </p>
</div>
    <div class="field">
  <p class="control has-icons-left">
    <input class="input" type="email" placeholder="Email">
    <span class="icon is-small is-left">
      <i class="fas fa-envelope"></i>
    </span>
  </p>
</div>
<div class="field">
  <p class="control has-icons-left">
    <input class="input" type="password" placeholder="Password">
    <span class="icon is-small is-left">
      <i class="fas fa-lock"></i>
    </span>
  </p>
</div>
<div class="field">
  <p class="control">
    <label class="checkbox">
  <input type="checkbox">
  I agree to the <a href="#">terms and conditions</a>
</label>
  </p>
</div>
<div class="mt-4 has-text-centered">
    <button class="button is-primary">Sign Up</button>
</div>


    
  </form>
</div>
</div>


<!-- footer  -->

<footer class="footer has-background-light">
  <div class="content has-text-centered mt-4">
    <p>
      <strong>Made</strong> by <a href="https://jgthms.com">Jin</a>. The <a href="http://creativecommons.org/licenses/by-nc-sa/4.0/">CC BY NC SA 4.0</a>.
    </p>
  </div>
</footer>



</template>

<script>
export default {
name:'theNavbar',
data(){
    return{
        modalStatus:false,
        currTab:'product'
    }
},
methods:{
    toggleItems(){
        const navbarMenu = document.querySelector('#nav-links');
        navbarMenu.classList.toggle('is-active');
    }
},
watch:{
    modalStatus(newValue){
        const elem = document.querySelector('#sign-up-modal');
        if(newValue==true){
            elem.classList.add('is-active');
        }
        else{
            elem.classList.remove('is-active');
        }
    },
    currTab(newValue,oldValue){
        const oldTab = document.querySelector(`#${oldValue}-details`);
        const newTab = document.querySelector(`#${newValue}-details`);
        oldTab.classList.add('is-hidden');
        newTab.classList.remove('is-hidden');
        const oldTabList = document.querySelector(`#${oldValue}`);
        const newTabList = document.querySelector(`#${newValue}`);
        oldTabList.classList.remove('is-active');
        newTabList.classList.add('is-active');
    }
}
}

</script>

<style>
/* .navbar{
    padding:5px 10px;
} */
</style>