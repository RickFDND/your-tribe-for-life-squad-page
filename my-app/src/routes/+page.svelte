<script>
    let { data } = $props();

    const members = data.members;
</script>

<h1>Squadpage</h1>

<div class="members">
    {#each members as member}
        <a href="/{member.id}">
            {member.name} - <br /><img
                src={member.avatar}
                alt="student avatar"
            />
        </a><br />
    {/each}
</div>

<style>
    :global(body) {
        background-color: #a675f5;
    }

    h1 {
        text-transform: uppercase;
        text-align: center;
        color: #050542;
        padding-top: 2rem;
    }

    .members {
        display: flex;
        justify-content: center;
        align-items: center;
        flex-wrap: wrap;
        margin-top: 2em;
    }

    a {
        display: flex;
        flex-direction: column;
        align-items: center; 
        border: 2px solid #66e5bf;
        height: 300px;
        width: 250px;
        text-align: center;
        margin-bottom: 2rem;
        text-decoration: none;
        color: #66e5bf;


        img {
            height: 200px;
            width: 200px;
        }
    }
</style>
