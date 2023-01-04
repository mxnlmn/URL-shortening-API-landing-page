<script>
export default{
    name: "Header",
    data(){
        return{
            isActive: false
        }
    },
    methods:{
        openMenu(){
            this.isActive = !this.isActive
        }
    }
}
</script>
<template>
    <div class = "header">
        <img src="../assets/images/logo.svg"/>
        <div class = "navigation" 
            :class = "{ open: isActive }">
            <ul class = "nav-links">
                <li>Features</li>
                <li>Pricing</li>
                <li>Resources</li>
            </ul>
            <ul class = "nav-login">
                <li>Login</li>
                <li class = "sign-btn rounded-btn">Sign Up</li>
            </ul>
        </div>
        <img @click = "openMenu" class = "menu-btn" src="../assets/images/hamburger.svg"/>
    </div>
</template>
<style>
    .menu-btn{
        display: none;
    }
    
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
        transition: .05s;
    }
    img:active{
        transform: scale(.8)
    }
    @media screen and (max-width: 768px){
        .header{
            display: flex;
            justify-content: space-between;
            position: relative;
        }
        .menu-btn{
            display: block;
        }
        .navigation{
            position: absolute;
            top: -25em;
            flex-direction: column;
            justify-content: center;
            background-color: hsl(257, 27%, 26%);
            border-radius: 1em;
            padding: 2em;
            transition: .5s ease-in-out;
        }
        .open{
            top: 3em;
        }
        .nav-links{
            border-bottom: 1px solid gray;
            padding-top: 0;
        }
        .nav-login{
            padding-bottom: 0;
        }
        ul{
            flex-direction: column;
            padding: 2em 0;
        }
        li{
            color: white;
            font-weight: 700;
        }

    }
    @media screen and (max-width: 425px){
        .header{
            margin: 1em 2em;
        }
    }
</style>