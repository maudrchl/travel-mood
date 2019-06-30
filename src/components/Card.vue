<template class="card">
<body>
    <div class="card">
        <img src="../assets/img/norway.png"/>
        <h2 class="title-card">{{card.title}}</h2>
        <h3 class="country-card">{{card.country}}</h3>
        <h3 class="date-card">{{card.date}}</h3>
    </div>
</body>
</template>

<style>
.card {
    width: 385px;
    height: 452px;
    background: white;
    margin: 0 auto;
    user-select: none;
    /* position: absolute; */
    /* opacity: 0.1; */
}

img {
    width: 345px;
    margin-left: 20px;
    margin-top: 20px;
    user-select: none;
}

h2 {
    color: #2A2A2A;
    font-size: 24px;
    margin-left: 20px;
    font-weight: 400;
    font-family: 'CanelaWeb-Regular'
}

h3 {
    color: #C1C1C1;
    font-size: 19px;
    margin-left: 20px;
    margin-top: -10px;
    font-weight: 400;
    float: left;
}

.date-card
{
    float:right;
    margin-right: 20px;
}

</style>
