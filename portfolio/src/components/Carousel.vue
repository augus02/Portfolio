<template>
    <body style="background-color: var(--dark-alt   );">
        <div class="gallery-wrap">
            <span class="material-icons" id="prev">west</span>
            <div class="gallery">
                <div>
                    <span style="text-align: center;">
                        <img src="../assets/Images/Design_bioreactor.jpg">
                        <div class="caption"> Design bioreactor for spirulina</div>
                    </span>
                    <span>
                        <img src="../assets/Images/Functional_bioreactor.jpg">
                        <div class="caption"> Functional bioreactor for optimal algal growth</div>
                    </span>
                    <span>
                        <img src="../assets/Images/Agricycle_v2_2.png">
                        <div class="caption"> Agricycle: Light agricole vehicle </div>
                    </span>
                </div>
                    
                <div>
                    <span>
                        <img src="../assets/Images/Lighting_ExpeTech.jpg">
                        <div class="caption"> Platform for indoor plant growth </div>
                    </span>
                    <span>
                        <img src="../assets/Images/Boitier.jpg">
                        <div class="caption"> Automatically adapting LED controller </div>
                    </span>
                    <span>
                        <img src="../assets/Images/RollAShape_overview.jpg">
                        <div class="caption"> Roll-A-Shape: machine to solder baromorph objects </div>
                    </span>
                </div>
            </div>
            <span class="material-icons" id="next">east</span>
        </div>
    </body>
</template>

<style scoped>

    .carouselElement{
        text-align: center;
        justify-content: center;

    }
    .gallery{
        width: 1200px;
        display: flex;
        overflow-x: scroll;
    }
    .gallery div{
        width: 100%;
        display: grid;
        grid-template-columns: auto auto auto;
        grid-gap: 20px;
        padding: 10px;
        flex: none;
    }

    .gallery div img{
        width: 100%;
        height: 80%;
        filter: grayscale(100%);
        transition: transform 0.5s;
        margin-bottom: 24px;
    }

    .caption{
        text-align: center;
        justify-content: center;
        background-color: var(--dark-alt);
        color: azure;
    }
    .gallery::-webkit-scrollbar{
        display: none;
    }
    
    .gallery-wrap{
        display: flex;
        align-items: center;
        justify-content: center;
        margin: 3% auto;
    }

    #prev, #next{
        width: 50px;
        size: 50px;
        color: azure    ;
        cursor: pointer;
        margin: 40px;
    }

    .gallery div img:hover{
        filter: grayscale(0);
        cursor: pointer;
        transform: scale(1.1);
    }
</style>

<script>
    export default {
        mounted(){
            let scrollZone = document.querySelector(".gallery");
            let prev = document.getElementById("prev");
            let next = document.getElementById("next");

            scrollZone.addEventListener("onwheel" in document ? "wheel" : "mousewheel", (evt) => {
                evt.preventDefault();
                scrollZone.scrollLeft += evt.deltaY;
            });

            prev.addEventListener("click", () =>{
                scrollZone.scrollLeft -= 300;
            })

            next.addEventListener("click", () =>{
                scrollZone.scrollLeft += 300;
            })
        },
    }
    
</script>