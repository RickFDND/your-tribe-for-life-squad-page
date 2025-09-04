<script>
    let { data } = $props()

    const member = data.member
</script>

<img class="logo" src="src/lib/assets/logo-fdnd.svg">

<section class="details">
    <h1>{member.name}</h1>
    <img class="student" src="{member.avatar}" alt="{member.avatar || 'Avatar Unknown'}">
    <h2>Favorite Hobby: {member.fav_hobby || 'Hobby Unknown'}</h2>
    <h2>Birthdate: {member.birthdate || 'Birthdate Unknown'}</h2>
</section>  

<a class="return" href="/">
    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 32 32"><title>4-Arrow Left</title><g id="_4-Arrow_Left" data-name="4-Arrow Left"><path d="M32,15H3.41l8.29-8.29L10.29,5.29l-10,10a1,1,0,0,0,0,1.41l10,10,1.41-1.41L3.41,17H32Z"/></g></svg>
</a>

<style>

    .logo {
        position: fixed;
        top: 20px;
        left: 20px;
    }

    .details {
        display: flex;
        align-items: center;
        flex-direction: column;
        padding-inline: 20px;
    }

    h1 {
        color: #050542;
        font-size: 28px;

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
        color: #050542;
        font-size: 20px;

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

    .student {
        width: 300px;
        height: 300px;
        background-color: white;
        object-fit: cover;
        border: 3px solid #050542;
        border-radius: 10px;

        @media (min-width: 500px) {
            height: 400px;
            width: 400px;
        }

        @media (min-width: 834px) {
            height: 500px;
            width: 500px;
        }
    }


    a {
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
    }

    svg {
        height: 50px;
        fill: #050542;
    }
</style>