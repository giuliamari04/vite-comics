<template>
    <footer>
     <section class="bg-top-footer">
        <div class="container">
            <div class="row py-4 position-relative overflow-hidden">
                <div class="col">
                <ul>
                <span>dc comics</span>
                <li>Characters</li>
                <li>Comics</li>
                <li>Movies</li>
                <li>TV</li>
                <li>Games</li>
                <li>Videos</li>
                <li>News</li>
            </ul>
            <ul>
                <span>shop</span>
                <li>Shop DC</li>
                <li>Shop DC Collectibles</li>
            </ul>
        </div>
                <div class="col">
                 <ul>
                <span>dc</span>
                <li>Terms Of use</li>
                <li>Privacy policy (New)</li>
                <li>Ad Choices</li>
                <li>Advertising</li>
                <li>Jobs</li>
                <li>Supscriptions</li>
                <li>Talent Workshops</li>
                <li>CPSC Certificates</li>
                <li>Ratings</li>
                <li>Shop Help</li>
                <li>Contact Us</li>
            </ul></div>
                <div class="col">
                <ul>
                <span>sites</span>
                <li>DC</li>
                <li>MAD Magazine</li>
                <li>DC Kids</li>
                <li>DC Universe</li>
                <li>DC power Visa</li>
            </ul></div>
                <div class="col-8">
                    <img src="/src/assets/images/dc-logo-bg.png" alt="logo" class="position-absolute top-50 start-50 end-0 translate-middle-y my-logo-w ">
                </div>
            </div>
        </div>
     </section>
     <section class="bg-bot-footer">
        <div class="container d-flex align-items-center justify-content-between">
            <div class="py-4">
                <button class="glow-on-hover text-uppercase" type="button">sign-up now!</button>
            </div>
            <div>
                <span class="text-primary text-uppercase px-2">follow us</span>
                <span class="px-2"><img src="/src/assets/images/footer-facebook.png" alt="icon"></span>
                <span class="px-2"><img src="/src/assets/images/footer-twitter.png" alt=""></span>
                <span class="px-2"><img src="/src/assets/images/footer-youtube.png" alt=""></span>
                <span class="px-2"><img src="/src/assets/images/footer-pinterest.png" alt=""></span>
                <span class="px-2"><img src="/src/assets/images/footer-periscope.png" alt=""></span>
            </div>
        </div>
     </section>
    </footer>
</template>

<script>
 export default{
    name:'FooterComponent',
    components:{
           
        },
        data(){
            return{

            }
        },
        methods:{

        },
 }
</script>

<style lang="scss" scoped>
@use '/src/assets/styles/partials/variables.scss' as *;
.bg-top-footer{
    background-image: url('src/assets/images/footer-bg.jpg');
    height: 42vh;
    color: white; 
}

.bg-bot-footer{
    background-color: #303030;
    height:15vh;
}
.my-logo-w{
    width: 35%;
}
ul li{
    list-style: none;
    font-weight: 300;
    font-size: 0.7em;
    color:rgb(172, 169, 169) ; 
    font-family: 'Open Sans', sans-serif;
}

span{
    text-transform: uppercase;
    font-weight: 700;
   padding-bottom: 10px;
}

.glow-on-hover {
    width: 140px;
    height: 50px;
    border: none;
    outline: none;
    color: #fff;
    background:transparent;
    border: 2px solid $blue_primary;
    cursor: pointer;
    position: relative;
    z-index: 0;
}

.glow-on-hover:before {
    content: '';
    background: linear-gradient(45deg, #ff0000, #ff7300, #fffb00, #48ff00, #00ffd5, #002bff, #7a00ff, #ff00c8, #ff0000);
    position: absolute;
    top: -2px;
    left:-2px;
    background-size: 400%;
    z-index: -1;
    filter: blur(5px);
    width: calc(100% + 4px);
    height: calc(100% + 4px);
    animation: glowing 20s linear infinite;
    opacity: 0;
    border: 2px solid $blue_primary;
    transition: opacity .3s ease-in-out;

}

.glow-on-hover:active {
    color: #000
}

.glow-on-hover:active:after {
    background: transparent;
}

.glow-on-hover:hover:before {
    opacity: 1;
}

.glow-on-hover:after {
    z-index: -1;
    content: '';
    position: absolute;
    width: 100%;
    height: 100%;
    background:#303030;
    left: 0;
    top: 0;
}

@keyframes glowing {
    0% { background-position: 0 0; }
    50% { background-position: 400% 0; }
    100% { background-position: 0 0; }
}
</style>
