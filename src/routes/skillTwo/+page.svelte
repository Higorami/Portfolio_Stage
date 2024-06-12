<svelte:head>
	<title>Compétence 4 niveau 1</title>
	<meta name="description" content="Compétence 4 niveau 1" />
</svelte:head>

<script>

    // Sous-onglets

    var btns = [true, false, false];

    function changeBtn(index){
        for (let i = 0; i < btns.length; i++) {
            if(i == index){
                btns[i] = true;
            }else{
                btns[i] = false;
            }
        }
    }

    // carousels

    import { Splide, SplideSlide } from '@splidejs/svelte-splide';
    import '@splidejs/svelte-splide/css';

        // Carousels Ac41
        let indexApiAc41 = 0;
        let imagesApiAc41 = [
            { src: '../../../static/image_test.png', alt: 'API1'},
            { src: '../../../static/image_test.png', alt: 'API2'},
            { src: '../../../static/image_test.png', alt: 'API3'},
        ];
        let indexPhonelogsAc41 = 0;
        let indexCodesAc41 = 0;

        // Carousels Ac42
        let indexPhonelogsAc42 = 0;
        let indexCodesAc42 = 0;

        // Carousels Ac43
        let indexPhonelogsAc43 = 0;
        let indexContactsAc43 = 0;

</script>

<div>
    <div class="box-titre">
        <h1>Compétence 4 niveau 1</h1>
        <h2>Concevoir et mettre en place une base de données à partir d'un cahier des charges client</h2>
    </div>
    Sous-onglets "cards"
    <div class="sous-nav">
        <button 
            class="btn-sous-nav {btns[0] ? 'btn-sous-nav-clicked' : ''}"
            on:click={() => changeBtn(0)}
        >ac41</button>
        <button 
            class="btn-sous-nav {btns[1] ? 'btn-sous-nav-clicked' : ''}"
            on:click={() => changeBtn(1)}
        >ac42</button>
        <button 
            class="btn-sous-nav {btns[2] ? 'btn-sous-nav-clicked' : ''}"
            on:click={() => changeBtn(2)}
        >ac43</button>
    </div>
    <div class="onglet {btns[0] ? 'onglet-displayed' : 'onglet-not-displayed'}">
        API
        Phonelogs
        Codes
        <div class="ac41-sous-titre">
            Sous titre ac41
        </div>
        <div class="ac41-API">
            <span class="description-API">
                Description API ac41
            </span>
            <span class="preuves-API">
                <Splide aria-label="preuves API ac41">
                    {#each imagesApiAc41 as {src, alt}}
                        <SplideSlide>
                            <img src="{src}" alt="{alt}"/>
                        </SplideSlide>
                    {/each}
                </Splide>
            </span>
        </div>
        <div class="ac41-Phonelogs">
            <span class="description-Phonelogs">
                Description Phonelogs ac41
            </span>
            <span class="preuves-Phonelogs">
    
            </span>
        </div>
        <div class="ac41-Codes">
            <span class="description-Codes">
                Description Codes ac41
            </span>
            <span class="preuves-Codes">
    
            </span>
        </div>
    </div>
    <div class="onglet {btns[1] ? 'onglet-displayed' : 'onglet-not-displayed'}">
        Phonelogs
        Codes
        <div class="ac42-sous-titre">
            Sous titre ac42
        </div>
        <div class="ac42-Phonelogs">
            <span class="description-Phonelogs">
                Description Phonelogs ac42
            </span>
            <span class="preuves-Phonelogs">
    
            </span>
        </div>
        <div class="ac42-Codes">
            <span class="description-Codes">
                Description Codes ac42
            </span>
            <span class="preuves-Codes">
    
            </span>
        </div>
    </div>
    <div class="onglet {btns[2] ? 'onglet-displayed' : 'onglet-not-displayed'}">
        Phonelogs
        Contacts
        <div class="ac43-sous-titre">
            Sous titre ac43
        </div>
        <div class="ac43-Phonelogs">
            <span class="description-Phonelogs">
                Description Phonelogs ac43
            </span>
            <span class="preuves-Phonelogs">
    
            </span>
        </div>
        <div class="ac43-Contacts">
            <span class="description-Contacts">
                Description Contacts ac43
            </span>
            <span class="preuves-Contacts">
    
            </span>
        </div>
    </div>
</div>

<style>

.sous-nav{
    display: flex;
    max-width: fit-content;
}

.btn-sous-nav{
    left: 0;
    margin: 0;
    width: 15rem;
    height: 3rem;
    background-color: rgb(68, 67, 67);
    color: orange;
    border: 2px solid goldenrod;
    border-left: none;
}

.btn-sous-nav:hover{
    background-color: grey;
    color: gold;
    transition: 0.2s;
}

.btn-sous-nav-clicked{
    background-color: grey;
    color: gold;
    border-bottom: none;
}

.onglet-displayed{
    display: block;
    background-color: grey;
}

.onglet-not-displayed{
    display: none;
}

</style>