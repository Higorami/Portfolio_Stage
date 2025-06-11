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

        // Carousels Ac11
        import imageAc11ARI from '$lib/images/ac11/controleurARI.png';

        let imagesAc41 = [
            { src: imageAc11ARI, alt: 'Figure I - Contrôleur ARI'},
        ];

        // Carousels Ac12
        import imageAc12StatsBefore from '$lib/images/ac12/stats_before.png';
        import imageAc12StatsAfter from '$lib/images/ac12/stats_after.png';

        let imagesAc12 = [
            { src: imageAc11ARI, alt: 'Figure I - Contrôleur ARI'},
            { src: imageAc12StatsBefore, alt: 'Figure II - Statistiques avant amélioration'},
            { src: imageAc12StatsAfter, alt: 'Figure III - Statistiques après amélioration'},
        ];

        // Carousels Ac13
        import imageAc13Diagramme from '$lib/images/ac13/diagramme_environnement_prod.png';

        let imagesAc13 = [
            { src: imageAc13Diagramme, alt: 'Figure IV - Diagramme de l’environnement de production'},
        ];

</script>

<div class="all">
    <div class="box-titre">
        <h1>Compétence 1 niveau 3</h1>
        <h2>Adapter des applications sur un ensemble de supports</h2>
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
        >Apprentissage Critique 2</button>
        <button 
            class="btn-sous-nav {btns[2] ? 'btn-sous-nav-clicked' : ''}"
            on:click={() => changeBtn(2)}
        >Apprentissage Critique 3</button>
    </div>
    <div class="onglet {btns[0] ? 'onglet-displayed' : 'onglet-not-displayed'}">
        <div class="sous-titre">
            <h2>Choisir et implémenter les architectures adaptées</h2>
        </div>
        <div class="contenu">
            <span class="description left">
                <p>L’application HORUS a été conçue dans le but d’aider les équipes départementales de pompiers dans leur quotidien. Pour cela elle leur permet de consulter de nombreuses informations de façon claire et concise pour les aider dans leurs prises de décisions, des statistiques et des prédictions par IA sont aussi disponible dans ce but, ainsi que de nombreux outils permettant de faciliter leur quotidien comme le contrôleur ARI (Appareil Respiratoire Isolant) apparaissant sur la figure I et permettant le suivi des pompiers au sein d’un bâtiment en feu.</p>
                <p>Comme vous pouvez l'imaginer, les pompiers utilisent donc cette application sur divers supports, que ce soit sur un ordinateur dans leurs bureaux, sur un téléphone lors des interventions ou sur une tablette pour le contrôleur ARI. J’ai donc dû adapter chacun de mes ajouts à leur usage majoritaire tout en m’assurant qu’ils fonctionnaient sur tous les supports possibles.</p>
                <p>Dans ce but il à donc fallu que j’adapte le style de l’application via une variable vérifiant le support de l’utilisateur, mais également que je m’adapte au navigateur de celui-ci. Ceux-ci ne disposant pas toujours des mêmes fonctionnalités, il a fallu que j’adapte parfois mes implémentations en conséquence comme lors du développement de la fonctionnalité de capture d’écran qui ne fonctionnait mal avec les navigateurs Firefox et Safari.</p>
            </span>
            <span class="preuves right">
                {#each imagesAc41 as {src, alt}}
                    <img src="{src}" alt="{alt}"/>
                    <p>{alt}</p>
                {/each}
            </span>
        </div>
    </div>
    <div class="onglet {btns[1] ? 'onglet-displayed' : 'onglet-not-displayed'}">
        <div class="sous-titre">
            <h2>Faire évoluer une application existante</h2>
        </div>
        <div class="contenu">
            <span class="preuves left">
                {#each imagesAc12 as {src, alt}}
                    <img src="{src}" alt="{alt}"/>
                    <p>{alt}</p>
                {/each}
            </span>
            <span class="description right">
                <p>L’application HORUS est en production et donc dans un état fonctionnel depuis 2022. Ayant rejoint le développement en 2025 j’ai été amené à faire évoluer une application existante. Dans ce cadre j’ai apporté trois types d’évolutions, l’ajout de fonctionnalités et la modification de fonctionnalités existantes que j’aborderai ensuite, ainsi que la correction de bugs diverses de manière plus succincte.</p>
                <p>Pour la partie sur l’ajout d’une fonctionnalité je vais prendre la page du contrôleur ARI comme exemple, celle-ci est visible sur la figure I. Pour la réalisation de cette page je suis passé par deux étapes. Tout d’abord pour la partie conception j’ai commencé par récolter le besoin utilisateur. Une fois toutes les informations essentielles récupérées j’ai pu dessiner une maquette sur papier en m’inspirant de solutions existantes. Après validation de mon maître de stage j’ai commencé l’implémentation, pour ce faire j’ai commencé par un placement rapide des éléments majeurs puis par la création de toute la logique. J’ai pu ajouter un compteur, un calcul de l’heure de sortie, un calcul de l’oxygène restant en fonction des paramètres de l’utilisateur, etc…. Pour les finitions du style de la page j’ai dû veiller à respecter l’esthétique globale de l’application déjà existante.</p>
                <p>Pour la partie sur l’amélioration d’une fonctionnalité déjà existante j’ai choisi comme exemple la page des statistiques. Avant mes modifications les informations étaient simplement affichées de manière textuelle (voir figure II). Il à donc fallu que j’adapte chacune des données sous forme du graphique le plus adapté afin que l’utilisateur puisse les comprendre de la manière la plus intuitive et rapide possible à l’aide le la bibliothèque AGCharts. J’ai donc dû apprendre cette bibliothèque avant de pouvoir implémenter chaque graphique avec les données associées (voir figure III).</p>
            </span>
        </div>
    </div>
    <div class="onglet {btns[2] ? 'onglet-displayed' : 'onglet-not-displayed'}">
        <div class="sous-titre">
            <h2>Intégrer des solutions dans un environnement de production</h2>
        </div>
        <div class="contenu">
            <span class="description left">
                <p>L’application HORUS étant déjà en production, il était nécessaire de prendre toutes les précautions avant de faire le moindre changement pour éviter d’impacter les utilisateurs. Dans cette optique, j'ai donc dû suivre une procédure rigoureuse lors de mon travail.</p>
                <p>Cette procédure commençait par le travail personnel normal d’un développeur consistant à mener des tests sur les ajouts que j’apportais au code. Le reste de cette procédure se faisait en concordance avec le cycle du projet dont le diagramme est visible sur la figure IV. À chaque nouvelle nouvelle fonctionnalité je commençais par créer une nouvelle branche sur le repository github du projet, avec des commit régulier pour éviter les pertes, je travaillais uniquement sur cette branche jusqu’à ce que la fonctionnalité soit entièrement finie. À ce moment-là je lançais une pull request, une fois mon code revu par mon maître de stage, ma branche était fusionnée à la branche principale du projet. Tout le développement se passe sur le serveur de développement qui est différencié du serveur de production. Après quelques tests et lorsque le serveur de développement est stabilisé, le code de celui-ci est envoyé vers le serveur de production pour le mettre à jour.</p>
            </span>
            <span class="preuves right">
                {#each imagesAc13 as {src, alt}}
                    <img src="{src}" alt="{alt}"/>
                    <p>{alt}</p>
                {/each}
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