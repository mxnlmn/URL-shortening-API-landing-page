<script>
export default{
    name: "Header"
}
</script>
<template>
    <div class = "header">
        <img src="../assets/images/logo.svg"/>
        <div class = "navigation">
            <ul class = "nav-links">
                <li>Features</li>
                <li>Pricing</li>
                <li>Resources</li>
            </ul>
            <ul class = "nav-login">
                <li>Login</li>
                <li class = "rounded-btn">Sign Up</li>
            </ul>
        </div>
    </div>
</template>
<style>
    .header{
        margin: 2em 5em;
        display: flex;
        align-items: center;
        gap: 1em;
    }
    .navigation{
        width: 100%;
        display:flex;
        justify-content: space-between;
    }
    ul{
        display: flex;
        align-items: center;
        gap: 1.5em;
    }
    li{
        list-style: none;
        color: gray;
        transition: .2s;
        cursor: pointer;
    }
    li:active{
        transform: scale(.8)
    }
    img{
        cursor: pointer;
        transition: .2s;
    }
    img:active{
        transform: scale(.8)
    }
</style>