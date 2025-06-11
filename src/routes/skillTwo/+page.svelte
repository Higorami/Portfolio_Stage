<svelte:head>
	<title>Compétence 6 niveau 3</title>
	<meta name="description" content="Compétence 6 niveau 3" />
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

        // Carousels Ac11
        import imageAc11ARI from '$lib/images/ac11/controleurARI.png';

        let imagesAc61 = [
            { src: imageAc11ARI, alt: 'Figure I - Contrôleur ARI'},
        ];

        // Carousels Ac12
        import imageAc12StatsBefore from '$lib/images/ac12/stats_before.png';
        import imageAc12StatsAfter from '$lib/images/ac12/stats_after.png';

        let imagesAc63 = [
            { src: imageAc11ARI, alt: 'Figure I - Contrôleur ARI'},
            { src: imageAc12StatsBefore, alt: 'Figure II - Statistiques avant amélioration'},
            { src: imageAc12StatsAfter, alt: 'Figure III - Statistiques après amélioration'},
        ];

</script>

<div class="all">
    <div class="box-titre">
        <h1>Compétence 6 niveau 3</h1>
        <h2>Manager une équipe informatique</h2>
        <h3>Cette compétence sera essentiellement illustrée par le travail que j'ai réalisé lors de mon stage de 16 semaines dans l'entreprise Isara Technologies. Ma tâche principale au cours de ce stage étant l'amélioration de l'application web à destination des pompiers HORUS.</h3>
    </div>
    <div class="sous-nav">
        <button 
            class="btn-sous-nav {btns[0] ? 'btn-sous-nav-clicked' : ''}"
            on:click={() => changeBtn(0)}
        >Apprentissage Critique 1</button>
        <button 
            class="btn-sous-nav {btns[1] ? 'btn-sous-nav-clicked' : ''}"
            on:click={() => changeBtn(1)}
        >Apprentissage Critique 3</button>
    </div>
    <div class="onglet {btns[0] ? 'onglet-displayed' : 'onglet-not-displayed'}">
        <div class="sous-titre">
            <h2>Choisir et implémenter les architectures adaptées</h2>
        </div>
        <div class="contenu">
            <span class="description left">
                <p>L’application HORUS a été conçue dans le but d’aider les équipes départementales de pompiers dans leur quotidien. Pour cela elle leur permet de consulter de nombreuses informations de façon claire et concise pour les aider dans leurs prises de décisions, des statistiques et des prédictions par IA sont aussi disponible dans ce but, ainsi que de nombreux outils permettant de faciliter leur quotidien comme le contrôleur ARI (Appareil Respiratoire Isolant) apparaissant sur la figure I et permettant le suivi des pompiers au sein d’un bâtiment en feu.</p>
            </span>
            <span class="preuves right">
                {#each imagesAc61 as {src, alt}}
                    <img src="{src}" alt="{alt}"/>
                    <p>{alt}</p>
                {/each}
            </span>
        </div>
    </div>
    <div class="onglet {btns[1] ? 'onglet-displayed' : 'onglet-not-displayed'}">
        <div class="sous-titre">
            <h2>Appliquer des principes d'accessibilité et d'ergonomie</h2>
        </div>
        <div class="contenu">
            <span class="preuves left">
                {#each imagesAc63 as {src, alt}}
                    <img src="{src}" alt="{alt}"/>
                    <p>{alt}</p>
                {/each}
            </span>
            <span class="description right">
                <p>L’application HORUS est en production et donc dans un état fonctionnel depuis 2022. Ayant rejoint le développement en 2025 j’ai été amené à faire évoluer une application existante. Dans ce cadre j’ai apporté trois types d’évolutions, l’ajout de fonctionnalités et la modification de fonctionnalités existantes que j’aborderai ensuite, ainsi que la correction de bugs diverses de manière plus succincte.</p>
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

.box-titre h3{
    font-size: 1.2em;
    color: rgb(97, 97, 97);
    text-align: center;
    width: 40vw;
    margin: auto;
    margin-top: 1rem;
    margin-bottom: 2rem;
}

.sous-nav{
    display: flex;
    max-width: fit-content;
    width: 80vw;
    margin: 0 auto;
}

.btn-sous-nav{
    left: 0;
    margin: 0;
    width: 15rem;
    height: 3rem;
    background-color: rgb(68, 67, 67);
    color: orange;
    border: 2px solid goldenrod;
}

.btn-sous-nav:hover {
    background-color: grey;
    color: gold;
    transition: 0.2s;
}

.btn-sous-nav-clicked{
    background-color: rgba(128, 128, 128, 0.8);
    color: gold;
    border-bottom: none;
}

.onglet{
    background-image: linear-gradient(to bottom, rgba(128, 128, 128, 0.8), rgba(128, 128, 128, 0.8)), url('$lib/images/background.jpg');
    background-size: cover;
    background-position: center;
    background-repeat: repeat;
    padding: 2rem;
    margin: 0 auto;
    width: 80vw;
    border-radius: 10px;
    margin-bottom: 5vh;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
    transition: background-color 0.3s ease;
    display: none;
    position: relative;
    overflow: hidden;   
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
    margin: 0 auto;
}

.sous-titre h2{
    margin: auto;
    font-size: 3em;
    color: orange;
    text-align: center;
    width: 100%;
    padding: 1rem;
}

.preuves{
    width: 40vw;
    height: fit-content;
    background-color: rgba(255, 255, 255, 0.8);
}

.preuves img{
    width: 100%;
    height: auto;
    object-fit: cover;
    border-radius: 6px;
}

.preuves p{
    text-align: center;
    font-size: 1.2rem;
    color: rgb(97, 97, 97);
    margin-top: 0.5rem;
    border-bottom: 1px solid rgb(97, 97, 97);
    margin-bottom: 0;
}

.description{
    width: 24vw;
    font-size: 1.5rem;
    background-color: rgb(247, 232, 213);
    border-radius: 10px;
    padding: 1.5rem;
    text-align: justify;
    max-height: min-content;
    height: min-content;
}

.contenu{
    display: flex;
    justify-content: space-evenly;
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