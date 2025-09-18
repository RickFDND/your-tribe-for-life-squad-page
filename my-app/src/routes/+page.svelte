<script>
    let { data } = $props();

    const members = data.members;

   const member = data.member;

   import { Logo } from '$lib';    // Import het Logo component
</script>

<Logo/> <!--Voeg het Logo component toe aan de pagina -->

<h1 class="title animation-fade-in--up" style="--delay: 0.1s">Squadpage 2025-2026</h1> <!--Titel van de pagina en fade in animatie --> 

<div class="hero-buttons">
    <a class="first-btn animation-fade-in--up" style="--delay: 0.3s" href="/squad-2e">Squad 2E</a> <!--Knop naar Squad 2E met fade in animatie -->
    <a class="second-btn animation-fade-in--up" style="--delay: 0.3s" href="/squad-2f">Squad 2F</a> <!--Knop naar Squad 2F met fade in animatie -->
</div>

<ul class="members">
    {#each members as member} <!--Loop door de members array en maak voor elk lid een lijst item aan -->
    <li>
        <a class="members-link animation-fade-in--up" style="--delay: 0.5s" href="/{member.id}"> <!--Link naar de individuele pagina van het lid met fade in animatie -->
            <h2>Student</h2>
            <img
                style="--vt-merge: member-card-{member.id};" 
                src={member.avatar}
                alt="student avatar"
            /> <!--Afbeelding van het lid met view transition naam voor animatie -->
            <p>{member.name}</p> <!--Naam van het lid -->
        </a>
    </li>
    {/each}
</ul>


 {#each member as m} <!--Loop door de member array en maak voor elk lid een afbeelding aan -->
      <img
        src={`https://fdnd.directus.app/assets/${m.mugshot}?w=50&h=50&fit=cover`}
        alt={m.name}
        width="200" height="auto"
      />
{/each}

<style>
    .title {
        text-transform: uppercase;
        text-align: center;
        color: #050542;
        line-height: 1;
        margin-top: 5rem;
        margin-bottom: 3rem;

        @media (min-width: 385px) {
            font-size: 3rem;
        }
    }

    .hero-buttons {
        display: flex;
        justify-content: center;
        gap: 3rem;
        margin-bottom: 3rem;

        a {
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 0.75rem;
            width: 125px;
            border-radius: 30px;
            text-decoration: none;
            transition: transform 0.3s;

            &:hover {
                transform: translateY(-2px); /* Verhoog de knop lichtjes bij hover */
            }
        }

        .first-btn {
            border: 3px solid #66e5bf;
            background-color: #050542;
            color: #66e5bf;

            &:active {
                transform: translateY(2px); /* Verlaag de knop lichtjes bij active state */
            }
        }

        .second-btn {
            border: 3px solid #050542;
            background-color: #66e5bf;
            color: #050542;

            &:active {
                transform: translateY(4px); /* Verlaag de knop iets meer bij active state */
            }
        }
    }

    .members {
        display: flex;
        justify-content: center;
        align-items: center;
        flex-wrap: wrap;
        margin-top: 2em;
        padding: 0;
        view-transition-class: member-card; /* Class voor view transition animatie */
        view-transition-name: var(--vt-merge); /* Naam voor view transition animatie */

        @media (min-width: 530px) {
            gap: 1rem;
        }

        @media (min-width: 600px) {
            gap: 3rem;
        }

        li {
            list-style-type: none;
        }
    }

    .members-link {
        display: flex;
        flex-direction: column;
        align-items: center;
        border: 3px solid #66e5bf;
        height: 320px;
        width: 250px;
        text-align: center;
        margin-bottom: 2rem;
        text-decoration: none;
        color: #66e5bf;
        background-color: #050542;
        border-radius: 10px;
        transition: transform 0.3s;

        &:hover {
            transform: scale(0.97); /* Verklein de kaart lichtjes bij hover */
        }

        &:active {
            transform: translateY(4px); /* Verlaag de kaart iets meer bij active state */
        }

        img {
            height: 180px;
            width: 180px;
            border-radius: 8px;
            view-transition-name: var(--vt-merge); /* Naam voor view transition animatie */
        }
    }

    .animation-fade-in--up {
        @media (prefers-reduced-motion: no-preference) { /* Controleer of de gebruiker geen voorkeur heeft voor verminderde beweging */
            transform: translateY(100px); 
            opacity: 0;
            animation: fade-in-translate 0.5s var(--delay, 0s) ease-out forwards; /* Fade-in en vertaal animatie met variabele vertraging */
        }
    }

    @keyframes fade-in-translate { /* Definieer de keyframes voor de fade-in en vertaal animatie */
        to {
            transform: translateY(0); 
            opacity: 1;
        }
    }
</style>
