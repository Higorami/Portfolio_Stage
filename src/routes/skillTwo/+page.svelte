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
        import imageAc11ARI from '$lib/images/ac61/creation_ggmap.png';

        let imagesAc61 = [
            { src: imageAc11ARI, alt: 'Figure V - Code de la création de la carte Google Maps'},
        ];

        // Carousels Ac12
        import imageAc12StatsBefore from '$lib/images/ac12/stats_before.png';
        import imageAc12StatsAfter from '$lib/images/ac12/stats_after.png';
        import imageAc12MapBefore from '$lib/images/ac63/map_before.png';
        import imageAc12MapAfter from '$lib/images/ac63/map_after.png';

        let imagesAc63 = [
            { src: imageAc12StatsBefore, alt: 'Figure II - Statistiques avant amélioration'},
            { src: imageAc12StatsAfter, alt: 'Figure III - Statistiques après amélioration'},
            { src: imageAc12MapBefore, alt: 'Figure VI - Carte avant mise à jour'},
            { src: imageAc12MapAfter, alt: 'Figure VII - Carte après mise à jour'},
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
            <h2>Organiser et partager une veille numérique</h2>
        </div>
        <div class="contenu">
            <span class="description left">
                <p>Le frontend de l’application HORUS se base sur le framework TypeScript Angular, c’est un framework très robuste et grandement utilisé dans les applications de taille importante. Il n’est cependant pas étudié durant les cours et il a donc fallu que je l’apprenne de zéro, même si avoir étudié un autre framework javascript (Vue.js) durant les cours m’a quand même facilité le processus. De plus, le framework possédant des mises à jour de version et l’application souhaitant être fonctionnelle et stable le plus longtemps possible, il a fallu que j’effectue une certaine veille informatique afin de développer mon code avec les dernières bonnes pratiques d’Angular pour garantir sa validité dans le temps. J’ai également dû effectuer cette veille pour d’autres parties de l’application ce qui m'a amené à changer entièrement le code de la page (un extrait est visible sur la figure V) celui-ci étant uniquement sous la forme de balises auparavant, l’API avait effectivement subi un changement récent apportant de nombreuses modifications qui ont demandé un grand investissement dans la documentation afin de trouver des solutions pour garder les mêmes fonctionnalités. J’ai bien évidemment fait part de mes trouvailles à mon maître de stage pour qu’il puisse lui aussi se maintenir à niveau.</p>
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
            <h2>Guider la conduite du changement informatique au sein d’une équipe informatique</h2>
        </div>
        <div class="contenu">
            <span class="preuves left">
                {#each imagesAc63 as {src, alt}}
                    <img src="{src}" alt="{alt}"/>
                    <p>{alt}</p>
                {/each}
            </span>
            <span class="description right">
                <p>Au cours de mon stage et dans le cadre du projet HORUS, j’ai été amené à réaliser de nombreuses tâches diverses et variées, celles-ci étaient plus ou moins réalisables et dans un état de conception plus ou moins avancé. J’ai donc eu l’occasion de parfois proposer et apporter des changements dans la direction qui m'était indiquée.</p>
                <p>J’ai deux exemples qui illustrent ces changements, un premier avec une idée qui n’était pas encore claire de la tâche et que j’ai donc dû élaborer, et un deuxième avec une tâche qui a dû se confronter à une limitation technique et que j’ai donc dû modifier.</p>
                <p>Le premier exemple est survenu lorsque j’ai reçu comme tâche la refonte de la page des statistiques. Celle-ci étant alors dans un état uniquement textuel (voir figure II), il a donc fallu que j’associe chaque donnée à un graphique adapté et que je crée le visuel de la page. J’ai pu faire mes propositions qui ont été adoptées et ainsi prendre la direction que je souhaitais (extrait de la page finale sur la figure III).</p>
                <p>Le deuxième exemple est survenu lors de la mise à niveau de l’API Google Maps sur la page de la carte. J’avais pour objectif de retrouver un affichage identique à la version précédente avec la version mise à jour, cependant certains changements majeurs m’ont forcé à changer un minimum le visuel pour pallier des limitations techniques. La solution que j’ai proposée a été acceptée et le visuel a donc été légèrement changé (voir figures VI et VII).</p>
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
    color: #d3d3d3;
    border: 2px solid #660708;
}

.btn-sous-nav:hover {
    background-color: grey;
    color: #ba181b;
    transition: 0.2s;
}

.btn-sous-nav-clicked{
    background-color: rgba(128, 128, 128, 0.8);
    color: #a4161a;
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
    color: #660708;
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