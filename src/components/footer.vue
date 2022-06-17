<template>
    <div class="container">
        <div class="img-container "> <img class="earth"
                src="https://img.freepik.com/photos-gratuite/vue-du-globe-terrestre-planete-depuis-espace-montrant-surface-realiste-terre-carte-du-monde_31965-32896.jpg" />
            <a href="https://inova.io/" class="inova-link" target="_blank">
                <img class="inova"
                    src="https://mms.businesswire.com/media/20181003005049/fr/681850/23/Inova-logo-blue_PNG.jpg" />
            </a>
        </div>

        <div class="magic-container">
            <div class="credits-container">
                <span class="credits"> Developping team composition: Zaki (project chief),
                    <a href="https://www.instagram.com/libertine_doncle_en_soeur/">Calvin (we don't know)</a>
                    and
                    <a href="https://www.instagram.com/malo_lbld/"> Malo(a little bit developer front-end)</a>
                </span>
            </div>
        </div>
        

    </div>
</template>

<script>

export default {
    name: 'MyFooter',
    components: {

    }
}
</script>

<style scoped>




.container {
    font-size: 50px;
    color: white;
   
}

.magic-container {
    display: flex;
    justify-content: center;
    margin-top:7%;
}
.earth {
    border-radius: 50px;
    border: 4px ridge white;
    width: 30%;
    height: 30%;


}

.inova {
width: -webkit-fill-available;
    height: auto;
    border-radius: 50px;
    border: 5px ridge white;
}

.inova-link{
    width:30%;
}

.credits {
    color: white;
    font-size: 15px;
    text-align: center;

}

.credits-container {
    border: 2px white;
    border-style: ridge;
    border-radius: 10px;
    display: flex;
    justify-content: center;
    justify-items: center;
    justify-self: center;
    width: fit-content;
    padding: 5px 10px;

}

a {
    color: white;
    text-decoration: none;
}

.img-container {
    display: flex;
    justify-content: space-between;
    margin-right:20px;
    margin-left: 20px;
    margin-top:20px;

}
</style>