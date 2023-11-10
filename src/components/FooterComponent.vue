<template>
    <footer>
     <section class="bg-top-footer">
        <div class="container">
            <div class="row py-4 position-relative">
                <div class="col">
                <ul>
                <span>dc comics</span>
                <li><a href="#">Characters</a></li>
                <li><a href="#">Comics</a></li>
                <li><a href="#">Movies</a></li>
                <li><a href="#">TV</a></li>
                <li><a href="#">Games</a></li>
                <li><a href="#">Videos</a></li>
                <li><a href="#">News</a></li>
            </ul>
            <ul>
                <span>shop</span>
                <li><a href="#">Shop DC</a></li>
                <li><a href="#">Shop DC Collectible</a>s</li>
            </ul>
        </div>
                <div class="col">
                 <ul>
                <span>dc</span>
                <li><a href="#">Terms Of use</a></li>
                <li><a href="#">Privacy policy (New)</a></li>
                <li><a href="#">Ad Choices</a></li>
                <li><a href="#">Advertising</a></li>
                <li><a href="#">Jobs</a></li>
                <li><a href="#">Supscriptions</a></li>
                <li><a href="#">Talent Workshops</a></li>
                <li><a href="#">CPSC Certificates</a></li>
                <li><a href="#">Ratings</a></li>
                <li><a href="#">Shop Help</a></li>
                <li><a href="#">ontact Us</a>C</li>
            </ul></div>
                <div class="col">
                <ul>
                <span>sites</span>
                <li><a href="#">DC</a></li>
                <li><a href="#">MAD Magazine</a></li>
                <li><a href="#">DC Kids</a></li>
                <li><a href="#">DC Universe</a></li>
                <li><a href="#">DC power Visa</a></li>
            </ul></div>
                <div class="col-6">
                    <img src="/images/dc-logo-bg.png" alt="logo" class="position-absolute start-50 end-0 translate-middle-y my-logo-w ">
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
                <span class="px-2"><img src="/images/footer-facebook.png" alt="icon"></span>
                <span class="px-2"><img src="/images/footer-twitter.png" alt=""></span>
                <span class="px-2"><img src="/images/footer-youtube.png" alt=""></span>
                <span class="px-2"><img src="/images/footer-pinterest.png" alt=""></span>
                <span class="px-2"><img src="/images/footer-periscope.png" alt=""></span>
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
    background-image: url('/images/footer-bg.jpg');
    background-repeat: no-repeat;
    background-size: cover;
    height: 43vh;
    color: white; 
    overflow: hidden;
}

.bg-bot-footer{
    background-color: #303030;
    height:15vh;
}
.my-logo-w{
    width: 450px;
    top: 50%;
}
ul li{
    list-style: none;
    font-weight: 300;
    font-size: 0.7em;
    color:rgb(172, 169, 169) ; 
    font-family: 'Open Sans', sans-serif;
}
a{
    text-decoration: none;
    color: inherit;

    &:hover{
    text-decoration: underline;
    color: inherit;
}
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
