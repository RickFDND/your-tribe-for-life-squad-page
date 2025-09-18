<script>
    let { data } = $props()

    const member = data.member
</script>

{#snippet logo()}
    <a class="logo" href="/" aria-label="Ga naar home">
        <svg
            width="349"
            height="148"
            viewBox="0 0 349 148"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
        >
            <rect
                x="2"
                y="18.1693"
                width="328.367"
                height="127.15"
                rx="18"
                fill="#66E5BF"
                stroke="#050542"
                stroke-width="4"
            />
            <rect
                x="18.1693"
                y="2"
                width="328.367"
                height="127.15"
                rx="18"
                fill="#66E5BF"
                stroke="#050542"
                stroke-width="4"
            />
            <path
                d="M73.2906 97.5682H57.4905V35.9316H92.5838V49.2961H73.2906V61.0584H91.0809V74.4228H73.2906V97.5682Z"
                fill="#050542"
            />
            <path
                d="M149.411 65.443C149.411 72.61 148.124 78.5685 145.552 83.3184C142.979 88.0683 139.351 91.6378 134.666 94.0268C130.009 96.3877 124.526 97.5682 118.216 97.5682H99.0045V35.9316H119.557C125.947 35.9316 131.363 37.0699 135.804 39.3465C140.245 41.6231 143.616 44.9537 145.917 49.3382C148.246 53.7228 149.411 59.091 149.411 65.443ZM132.757 66.0332C132.757 62.2951 132.27 59.2034 131.295 56.7582C130.347 54.2849 128.912 52.4439 126.99 51.2354C125.067 49.9987 122.644 49.3804 119.719 49.3804H115.048V83.9086H118.623C123.497 83.9086 127.071 82.4471 129.346 79.5241C131.62 76.573 132.757 72.076 132.757 66.0332Z"
                fill="#050542"
            />
            <path
                d="M213.305 97.5682H192.265L170.575 54.1443H170.21C170.345 55.4653 170.467 57.0533 170.575 58.9083C170.684 60.7633 170.778 62.6605 170.86 64.5998C170.941 66.511 170.981 68.2395 170.981 69.7854V97.5682H156.765V35.9316H177.724L199.332 78.7652H199.576C199.495 77.4161 199.414 75.8562 199.332 74.0856C199.251 72.2868 199.17 70.4739 199.089 68.6471C199.034 66.8202 199.007 65.2041 199.007 63.7988V35.9316H213.305V97.5682Z"
                fill="#050542"
            />
            <path
                d="M273.218 65.443C273.218 72.61 271.932 78.5685 269.36 83.3184C266.787 88.0683 263.159 91.6378 258.474 94.0268C253.817 96.3877 248.333 97.5682 242.024 97.5682H222.812V35.9316H243.365C249.755 35.9316 255.171 37.0699 259.612 39.3465C264.052 41.6231 267.424 44.9537 269.725 49.3382C272.054 53.7228 273.218 59.091 273.218 65.443ZM256.565 66.0332C256.565 62.2951 256.078 59.2034 255.103 56.7582C254.155 54.2849 252.72 52.4439 250.798 51.2354C248.875 49.9987 246.452 49.3804 243.527 49.3804H238.856V83.9086H242.43C247.304 83.9086 250.879 82.4471 253.153 79.5241C255.428 76.573 256.565 72.076 256.565 66.0332Z"
                fill="#050542"
            />
        </svg>
    </a>
{/snippet}

{@render logo()}

<section class="details">
    <h1>{member.name}</h1>
    <img class="student" style="--vt-merge: member-card-{member.id}" src="{member.avatar}" alt="{member.avatar || 'Avatar Unknown'}"> <!--Afbeelding van het lid met view transition naam voor animatie -->
    <h2>Favorite Hobby: {member.fav_hobby || 'Hobby Unknown'}</h2> 
    <h2>Birthdate: {member.birthdate || 'Birthdate Unknown'}</h2> 
</section>  

<a class="return" href="/">
    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 32 32"><title>4-Arrow Left</title><g id="_4-Arrow_Left" data-name="4-Arrow Left"><path d="M32,15H3.41l8.29-8.29L10.29,5.29l-10,10a1,1,0,0,0,0,1.41l10,10,1.41-1.41L3.41,17H32Z"/></g></svg>
</a>

<style>

    svg {
        height: 50px;
        width: auto;
        transition: transform 0.3s;

        &:hover {
            transform: scale(1.03);
        }

        &:active {
            transform: translateY(4px); /* Druk de knop naar beneden bij klikken */
        }
    }

    .details {
        display: flex;
        align-items: center;
        flex-direction: column;
        padding-inline: 20px;
    }

    h1 {
        font-family: 'Poppins', 'inter', arial;
        text-transform: uppercase;
        font-size: 28px;
        color: #050542;
        margin-top: -10px;

        @media (min-width: 500px) {
            font-size: 34px;
        }

        @media (min-width: 834px) {
            font-size: 40px;
        }

        @media (min-width: 834px) {
            font-size: 40px;
        }

        @media (min-width: 1150px) {
            font-size: 48px;
        }
    }

    h2 {
        font-family: 'Poppins', 'inter', arial;
        font-size: 20px;
        color: #050542;

        @media (min-width: 500px) {
            font-size: 24px;
        }

        @media (min-width: 834px) {
            font-size: 28px;
        }

        @media (min-width: 1150px) {
            font-size: 32px;
        }
    }

    h2:nth-of-type(1) { /* Eerste h2 (favoriete hobby) */
        margin-bottom: -10px;
    }

    .student {
        width: 300px;
        height: 300px;
        background-color: white;
        object-fit: cover;
        border: 3px solid #050542;
        border-radius: 10px;
        view-transition-name: var(--vt-merge); /* Naam voor view transition animatie */

        @media (min-width: 500px) {
            height: 400px;
            width: 400px;
        }
    }


    .return {
        display: flex;
        align-items: center;
        justify-content: center;
        position: fixed;
        bottom: 20px;
        left: 20px;
        background-color: #66e5bf;
        border: 3px solid #050542;
        border-radius: 10px;
        width: 80px;
        height: 60px;
        transition: transform 0.3s;


        &:hover {
            transform: scale(1.03);
        }

        &:active {
            transform: translateY(4px);
        }
    }

    svg {
        height: 50px;
        fill: #050542;
    }
</style>