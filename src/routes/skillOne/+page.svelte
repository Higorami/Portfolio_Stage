<svelte:head>
	<title>Compétence 1 niveau 2</title>
	<meta name="description" content="Compétence 1 niveau 2" />
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

        // Carousels Ac11
        import imageAc41API1 from '$lib/images/ac41/ac41_API.png';
        import imageAc41API2 from '$lib/images/ac41/ac41_API2.png';
        import imageAc41Phonelogs from '$lib/images/ac41/ac41_Phonelogs.png';
        import imageAc41Codes from '$lib/images/ac41/ac41_Codes.png';

        let imagesApiAc41 = [
            { src: imageAc41API1, alt: 'image API du swagger 1'},
            { src: imageAc41API2, alt: 'image API du swagger 2'},
        ];

        // Carousels Ac12
        import imageAc42Phonelogs1 from '$lib/images/ac42/ac42_Phonelogs1.png';
        import imageAc42Phonelogs2 from '$lib/images/ac42/ac42_Phonelogs2.png';
        import imageAc42Phonelogs3 from '$lib/images/ac42/ac42_Phonelogs3.png';
        import imageAc42Phonelogs4 from '$lib/images/ac42/ac42_Phonelogs4.png';
        import imageAc42Codes from '$lib/images/ac42/ac42_Codes.png';

        let imagesPhonelogsAc42 = [
            { src: imageAc42Phonelogs1, alt: 'image liste journaux téléphoniques 1'},
            { src: imageAc42Phonelogs2, alt: 'image liste journaux téléphoniques 2'},
            { src: imageAc42Phonelogs3, alt: 'image liste journaux téléphoniques 3'},
            { src: imageAc42Phonelogs4, alt: 'image liste journaux téléphoniques 4'},
        ];

        // Carousels Ac13
        import imageAc13Comms from '$lib/images/ac13/ac13_Commentaires.png';
        import imageAc13Docs from '$lib/images/ac13/ac13_doc.png';

        let imagesDocAc13 = [
            { src: imageAc13Comms, alt: 'image commentaires code module'},
            { src: imageAc13Docs, alt: 'image doc module'},
        ];

</script>

<div class="all">
    <div class="box-titre">
        <h1>Compétence 1 niveau 2</h1>
        <h2>Partir des exigences et aller jusqu'à une application complète</h2>
    </div>
    <div class="sous-nav">
        <button 
            class="btn-sous-nav {btns[0] ? 'btn-sous-nav-clicked' : ''}"
            on:click={() => changeBtn(0)}
        >Apprentissage Critique 1</button>
        <button 
            class="btn-sous-nav {btns[1] ? 'btn-sous-nav-clicked' : ''}"
            on:click={() => changeBtn(1)}
        >Apprentissage Critique 2</button>
        <button 
            class="btn-sous-nav {btns[2] ? 'btn-sous-nav-clicked' : ''}"
            on:click={() => changeBtn(2)}
        >Apprentissage Critique 3</button>
    </div>
    <div class="onglet {btns[0] ? 'onglet-displayed' : 'onglet-not-displayed'}">
        <div class="sous-titre">
            <h2>Élaborer et implémenter les spécifications fonctionnelles et non fonctionnelles à partir des exigences</h2> + api
        </div>
        <div class="contenu">
            <span class="description left">
                Lors de mon stage de deuxième année de BUT informatique j'ai dû créer une API. Celle-ci interroge et met à jour une base de donnée mySQL qui était déjà existante et qui contient certaines tables que j'ai ajouté.
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
        <div class="sous-titre">
            <h2>Appliquer des principes d'accessibilité et d'ergonomie</h2> + liste
        </div>
        <div class="contenu">
            <span class="preuves left">
                <Splide aria-label="preuves Codes ac42">
                    {#each imagesPhonelogsAc42 as {src, alt}}
                        <SplideSlide>
                            <img src="{src}" alt="{alt}"/>
                        </SplideSlide>
                    {/each}
                </Splide>
            </span>
            <span class="description right">
                J'ai également été amené à créer une page web pour la gestion et la visualisation des codes téléphoniques.
            </span>
        </div>
    </div>
    <div class="onglet {btns[2] ? 'onglet-displayed' : 'onglet-not-displayed'}">
        <div class="sous-titre">
            <h2>Adopter de bonnes pratiques de conception et de programmation</h2>
        </div>
        <div class="contenu">
            <span class="description left">
                J'ai été amené à concevoir deux tables que j'ai du inclure dans la base de donnée existante de Dolibarr. La première était une table regroupant les journaux téléphoniques et qui contient donc les informations de l'appelant comme son numéro de téléphone mais également les caractéristiques de l'appel comme la durée de celui-ci. La seconde table à été conçu pour stocker des listes d'id de contacts et tiers générées lors de la recherche via l'API et étant affichées dans une page web que j'ai crée.
            </span>
            <span class="preuves right">
                <Splide aria-label="preuves Phonelogs ac43">
                    {#each imagesDocAc13 as {src, alt}}
                        <SplideSlide>
                            <img src="{src}" alt="{alt}"/>
                        </SplideSlide>
                    {/each}
                </Splide>
            </span>
        </div>
    </div>
</div>

<style>

.all{
    overflow: hidden;
}

.box-titre{
    margin-top: 5vh;
    margin-bottom: 10vh;
}

.box-titre h1{
    font-size: 3em;
    color: black;
    text-align: center;
}

.box-titre h2{
    font-size: 1.8em;
    color: rgb(97, 97, 97);
    text-align: center;
    width: 40vw;
    margin: auto;
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

.onglet{
    background-color: grey;
}

.onglet-displayed{
    display: block;
}

.onglet-not-displayed{
    display: none;
}

.sous-titre{
    height: auto;
    width: 50vw;
    display: flex;
    padding-top: 5vh;
    padding-bottom: 8vh;
    padding-left: 25vw;
    padding-right: 25vw;
}

.sous-titre h2{
    margin: auto;
    font-size: 4em;
    color: orange;
    filter: drop-shadow(0px 0px 3px rgb(255, 196, 0));
    text-align: center;
}

.preuves{
    width: 50vw;
    height: fit-content;
    border: 5px solid rgb(46, 24, 3);
    border-radius: 10px;
    background-color: aliceblue;
}

.preuves img{
    width: 100%;
    height: auto;
    object-fit: cover;
    border-radius: 6px;
}

.description{
    width: 34vw;
    font-size: 1.5rem;
    background-color: rgb(247, 232, 213);
    border-radius: 10px;
    padding: 1.5rem;
    text-align: justify;
    min-height: fit-content;
    max-height: fit-content;
}

.contenu{
    display: flex;
}

.right{
    margin-right: 3vw;
    margin-left: auto;
    margin-bottom: 15vh;
}

.left{
    margin-left: 3vw;
    margin-right: auto;
    margin-bottom: 15vh;
}

</style>