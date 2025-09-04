<script>
    let { data } = $props()

    const member = data.member
</script>


<h1>{member.name}</h1>
<h2>{member.role.fav_hobby}</h2>

<a href="/">overzicht</a>
