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
        import imageTest from '$lib/images/image_test.png';
        let imagesApiAc41 = [
            { src: imageTest, alt: 'API2'},
            { src: imageTest, alt: 'API3'},
        ];
        let imagesPhonelogsAc41 = [
            { src: imageTest, alt: 'API2'},
            { src: imageTest, alt: 'API3'},
        ];
        let imagesCodesAc41 = [
            { src: imageTest, alt: 'API2'},
            { src: imageTest, alt: 'API3'},
        ];

        // Carousels Ac42
        let imagesPhonelogsAc42 = [
            { src: imageTest, alt: 'API2'},
            { src: imageTest, alt: 'API3'},
        ];
        let imagesCodesAc42 = [
            { src: imageTest, alt: 'API2'},
            { src: imageTest, alt: 'API3'},
        ];

        // Carousels Ac43
        let imagesPhonelogsAc43 = [
            { src: imageTest, alt: 'API2'},
            { src: imageTest, alt: 'API3'},
        ];
        let imagesContactsAc43 = [
            { src: imageTest, alt: 'API2'},
            { src: imageTest, alt: 'API3'},
        ];

</script>

<div class="all">
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
        <div class="sous-titre">
            <h2>Sous titre ac41</h2>
        </div>
        <div class="contenu">
            <span class="description left">
                Description API ac41
            </span>
            <span class="preuves right">
                <Splide aria-label="preuves API ac41">
                    {#each imagesApiAc41 as {src, alt}}
                        <SplideSlide>
                            <img src="{src}" alt="{alt}"/>
                        </SplideSlide>
                    {/each}
                </Splide>
            </span>
        </div>
        <div class="contenu">
            <span class="preuves left">
                <Splide aria-label="preuves API ac41">
                    {#each imagesApiAc41 as {src, alt}}
                        <SplideSlide>
                            <img src="{src}" alt="{alt}"/>
                        </SplideSlide>
                    {/each}
                </Splide>
            </span>
            <span class="description right">
                Description Phonelogs ac41
            </span>
        </div>
        <div class="contenu">
            <span class="description left">
                Description Codes ac41
            </span>
            <span class="preuves right">
                <Splide aria-label="preuves API ac41">
                    {#each imagesApiAc41 as {src, alt}}
                        <SplideSlide>
                            <img src="{src}" alt="{alt}"/>
                        </SplideSlide>
                    {/each}
                </Splide>
            </span>
        </div>
    </div>
    <div class="onglet {btns[1] ? 'onglet-displayed' : 'onglet-not-displayed'}">
        Phonelogs
        Codes
        <div class="sous-titre">
            Sous titre ac42
        </div>
        <div class="contenu">
            <span class="description left">
                Description Phonelogs ac42
            </span>
            <span class="preuves right">
                <Splide aria-label="preuves API ac41">
                    {#each imagesApiAc41 as {src, alt}}
                        <SplideSlide>
                            <img src="{src}" alt="{alt}"/>
                        </SplideSlide>
                    {/each}
                </Splide>
            </span>
        </div>
        <div class="contenu">
            <span class="preuves left">
                <Splide aria-label="preuves API ac41">
                    {#each imagesApiAc41 as {src, alt}}
                        <SplideSlide>
                            <img src="{src}" alt="{alt}"/>
                        </SplideSlide>
                    {/each}
                </Splide>
            </span>
            <span class="description right">
                Description Codes ac42
            </span>
        </div>
    </div>
    <div class="onglet {btns[2] ? 'onglet-displayed' : 'onglet-not-displayed'}">
        Phonelogs
        Contacts
        <div class="sous-titre">
            Sous titre ac43
        </div>
        <div class="contenu">
            <span class="description left">
                Description Phonelogs ac43
            </span>
            <span class="preuves right">
                <Splide aria-label="preuves API ac41">
                    {#each imagesApiAc41 as {src, alt}}
                        <SplideSlide>
                            <img src="{src}" alt="{alt}"/>
                        </SplideSlide>
                    {/each}
                </Splide>
            </span>
        </div>
        <div class="contenu">
            <span class="preuves left">
                <Splide aria-label="preuves API ac41">
                    {#each imagesApiAc41 as {src, alt}}
                        <SplideSlide>
                            <img src="{src}" alt="{alt}"/>
                        </SplideSlide>
                    {/each}
                </Splide>
            </span>
            <span class="description right">
                Description Contacts ac43
            </span>
        </div>
    </div>
</div>

<style>

.all{
    overflow: hidden;
}

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

.sous-titre{
    height: 20vh;
    width: 100vw;
    display: flex;
}

.sous-titre h2{
    margin: auto;
    font-size: 4em;
    color: orange;
    filter: drop-shadow(0px 0px 3px rgb(255, 196, 0));
}

.preuves{
    width: 100%;
}

.preuves img{
    width: 100%;
    min-width: fit-content;
    height: auto;
    border: 5px solid rgb(46, 24, 3);
    border-radius: 10px;
}

.description{
    font-size: 1.5rem;
}

.contenu{
    display: flex;
}

.right{
    width: 45vw;
    margin-right: 3vw;
    margin-left: auto;
    margin-bottom: 7vh;
}

.left{
    width: 45vw;
    margin-left: 3vw;
    margin-right: auto;
    margin-bottom: 7vh;
}

</style>