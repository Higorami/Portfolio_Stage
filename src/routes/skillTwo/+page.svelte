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
        import imageAc41API1 from '$lib/images/ac41/ac41_API.png';
        import imageAc41API2 from '$lib/images/ac41/ac41_API2.png';
        import imageAc41Phonelogs from '$lib/images/ac41/ac41_Phonelogs.png';
        import imageAc41Codes from '$lib/images/ac41/ac41_Codes.png';

        let imagesApiAc41 = [
            { src: imageAc41API1, alt: 'image API du swagger 1'},
            { src: imageAc41API2, alt: 'image API du swagger 2'},
        ];
        let imagesPhonelogsCodesAc41 = [
            { src: imageAc41Codes, alt: 'image edit codes téléphoniques'},
        ];

        // Carousels Ac42
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
            { src: imageAc42Codes, alt: 'image liste codes téléphoniques'},
        ];

        // Carousels Ac43
        import imageAc43Phonelogs from '$lib/images/ac43/ac43_Phonelogs.png';
        import imageAc43Contacts from '$lib/images/ac43/ac43_Contacts.png';
        import imageAc43CodesTiers from '$lib/images/ac43/ac43_Codes_tiers.png';
        import imageAc43CodesContact from '$lib/images/ac43/ac43_Codes_contact.png';

        let imagesBDDAc43 = [
            { src: imageAc43Phonelogs, alt: 'image BDD journaux téléphoniques'},
            { src: imageAc43Contacts, alt: 'image BDD contacts'},
            { src: imageAc43CodesTiers, alt: 'image BDD codes tiers'},
            { src: imageAc43CodesContact, alt: 'image BDD codes contact'},
        ];

</script>

<div class="all">
    <div class="box-titre">
        <h1>Compétence 4 niveau 1</h1>
        <h2>Concevoir et mettre en place une base de données à partir d'un cahier des charges client</h2>
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
            <h2>Mettre à jour et interroger une base de donnée relationnelle (en requêtes directes ou à travers une application)</h2>
        </div>
        <div class="contenu">
            <span class="description left">
                Lors de mon stage j’ai été amené à créer une API me permettant d’interagir avec la base de données de Dolibarr et ainsi interagir et mettre à jour les données des différentes tables de cette dernière aussi bien celles qui étaient déjà présentes que celles que j’ai ajoutées pour les besoins du module.
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
                <Splide aria-label="preuves Phonelogs ac41">
                    {#each imagesPhonelogsCodesAc41 as {src, alt}}
                        <SplideSlide>
                            <img src="{src}" alt="{alt}"/>
                        </SplideSlide>
                    {/each}
                </Splide>
            </span>
            <span class="description right">
                Mais je n’ai pas été confronté à la base de données seulement lors du développement de l’API mais bien de l’entièreté du module. En effet j’ai en permanence manipulée différentes données dans chacune des fonctionnalités. La plus notable dans ce cas est celle de la gestion des codes téléphoniques qui sous la forme d’une page web permet aussi bien de générer aléatoirement un code unique, que d’en créer un au choix ou bien encore d’en modifier ou supprimer un.
            </span>
        </div>
    </div>
    <div class="onglet {btns[1] ? 'onglet-displayed' : 'onglet-not-displayed'}">
        <div class="sous-titre">
            <h2>Visualiser des données</h2>
        </div>
        <div class="contenu">
            <span class="preuves left">
                <Splide aria-label="preuves Phonelogs ac42">
                    {#each imagesPhonelogsAc42 as {src, alt}}
                        <SplideSlide>
                            <img src="{src}" alt="{alt}"/>
                        </SplideSlide>
                    {/each}
                </Splide>
            </span>
            <span class="description right">
                J’ai implémenté dans le module que j’ai développé plusieurs pages web permettant de visualiser diverses données. Cette visualisation pouvait se faire sous la forme de liste avec différents filtrages, c’était le cas pour les journaux téléphoniques, ou encore d’une forme plus spécifique comme celle des codes téléphoniques qui sont une succession de formulaires indépendants liés au contact ou tiers sélectionné.
            </span>
        </div>
    </div>
    <div class="onglet {btns[2] ? 'onglet-displayed' : 'onglet-not-displayed'}">
        <div class="sous-titre">
            <h2>Concevoir une base de données relationnelle à partir d'un cahier des charges</h2>
        </div>
        <div class="contenu">
            <span class="description left">
                Dolibarr possédait déjà une base de données donc j’ai simplement créé et ajouté les tables nécessaires aux différentes fonctionnalités du module. Cela inclut une table pour stocker les journaux téléphoniques, une table pour les listes de contacts/tiers utilisés dans la recherche de 3CX, et deux tables pour stocker les codes téléphoniques respectivement des tiers et des contacts.
            </span>
            <span class="preuves right">
                <Splide aria-label="preuves Phonelogs ac43">
                    {#each imagesBDDAc43 as {src, alt}}
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
    background-color: rgb(46, 24, 3);
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