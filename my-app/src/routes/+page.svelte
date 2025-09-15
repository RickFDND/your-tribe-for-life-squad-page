<script>
    let { data } = $props();

    const members = data.members;

   const member = data.member;

   import { Logo } from '$lib';

    
</script>

<Logo/>

<h1 class="title animation-fade-in--up" style="--delay: 0.1s">Squadpage 2025-2026</h1>

<div class="hero-buttons">
    <a class="first-btn animation-fade-in--up" style="--delay: 0.3s" href="/squad-2e">Squad 2E</a>
    <a class="second-btn animation-fade-in--up" style="--delay: 0.3s" href="/squad-2f">Squad 2F</a>
</div>

<div class="members">
    {#each members as member}
        <a class="members-link animation-fade-in--up" style="--delay: 0.5s" href="/{member.id}">
            <h2>Student</h2>
            <img
                style="--vt-merge: member-card-{member.id};"
                src={member.avatar}
                alt="student avatar"
            />
            <p>{member.name}</p>
        </a>
    {/each}
</div>


 {#each member as m}
      <img
        src={`https://fdnd.directus.app/assets/${m.mugshot}?w=50&h=50&fit=cover`}
        alt={m.name}
        width="200" height="auto"
      />
{/each}

<style>
    :global(body) {
        background-color: #a675f5;
        font-family: "Poppins", "inter", arial;
    }

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
                transform: translateY(-2px);
            }
        }

        .first-btn {
            border: 3px solid #66e5bf;
            background-color: #050542;
            color: #66e5bf;

            &:active {
                transform: translateY(2px);
            }
        }

        .second-btn {
            border: 3px solid #050542;
            background-color: #66e5bf;
            color: #050542;

            &:active {
                transform: translateY(4px);
            }
        }
    }

    .members {
        display: flex;
        justify-content: center;
        align-items: center;
        flex-wrap: wrap;
        margin-top: 2em;
        view-transition-class: member-card;
        view-transition-name: var(--vt-merge);

        @media (min-width: 530px) {
            gap: 1rem;
        }

        @media (min-width: 600px) {
            gap: 3rem;
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
            transform: scale(0.97);
        }

        &:active {
            transform: translateY(4px);
        }

        img {
            height: 180px;
            width: 180px;
            border-radius: 8px;
            view-transition-name: var(--vt-merge);
        }
    }

    .animation-fade-in--up {
        @media (prefers-reduced-motion: no-preference) {
            transform: translateY(100px);
            opacity: 0;
            animation: fade-in-translate 0.5s var(--delay, 0s) ease-out forwards;
        }
    }

    @keyframes fade-in-translate {
        to {
            transform: translateY(0);
            opacity: 1;
        }
    }
</style>
