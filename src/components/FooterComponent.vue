<template>
    <footer>
     <section class="bg-top-footer">
        <div class="container">
            <div class="row py-4">
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
                <div class="col-8">2</div>
            </div>
           
           
          
        </div>
     </section>
     <section>2</section>
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

<style scoped>
.bg-top-footer{
    background-image: url('C:\BooleanEsercizi\vite-comics\src\assets\images\footer-bg.jpg');
    height: 40vh;
    color: white;
    
   
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
</style>
