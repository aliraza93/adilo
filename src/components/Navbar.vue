<template>
    <div class="topnav" id="myTopnav">
        <a href="#"><img src="../assets/logo.png" alt="Logo"></a>
        <a href="#dashboard">Dashboard</a>
        <a href="#messages">Messages</a>
        <a href="#orders" class="active">Orders</a>
        <a href="#gigs">Gigs</a>
        <a href="#analytics">Analytics</a>
        <a href="#earnings">Earnings</a>
        <a style="float: right; margin-top: -3px;" href="#"><img style="width: 35px; height: 35px; border-radius: 50%;" src="https://images.unsplash.com/flagged/photo-1570612861542-284f4c12e75f?ixid=MnwxMjA3fDB8MHxzZWFyY2h8Mnx8cGVyc29ufGVufDB8fDB8fA%3D%3D&ixlib=rb-1.2.1&w=1000&q=80" alt=""></a>
        <a href="javascript:void(0);" class="icon" @click="myFunction">
            <i class="fas fa-bars"></i>
        </a>
    </div>
</template>
<script>
export default {
    name: 'Navbar',
    methods: {
        myFunction() {
        var x = document.getElementById("myTopnav");
        if (x.className === "topnav") {
            x.className += " responsive";
        } else {
            x.className = "topnav";
        }
        }
    }
}
</script>
<style scoped>
    /* Add a black background color to the top navigation */
    .topnav {
        font-family: "Helvetica Neue", sans-serif, Arial;
        overflow: hidden;
        background-color: white;
    }

    /* Style the links inside the navigation bar */
    .topnav a {
        float: left;
        display: block;
        color: grey;
        text-align: center;
        padding: 20px 23px;
        text-decoration: none;
        font-weight: 500;
        font-size: 17px;
    }

    .topnav img {
        width: 30px;
        height: 30px;
        margin-top: -3px;
    }

    /* Change the color of links on hover */
    .topnav a:hover {
        color: #04AA6D;
        border-bottom: 2px solid #04AA6D;
    }

    /* Add an active class to highlight the current page */
    .topnav a.active {
        color: #04AA6D;
        border-bottom: 2px solid #04AA6D;
    }

    /* Hide the link that should open and close the topnav on small screens */
    .topnav .icon {
        display: none;
    }

    /* When the screen is less than 800 pixels wide, hide all links, except for the first one ("Home"). Show the link that contains should open and close the topnav (.icon) */
    @media screen and (max-width: 800px) {
    .topnav a:not(:first-child) {display: none;}
        .topnav a.icon {
            float: right;
            display: block;
        }
    }

    /* The "responsive" class is added to the topnav with JavaScript when the user clicks on the icon. This class makes the topnav look good on small screens (display the links vertically instead of horizontally) */
    @media screen and (max-width: 800px) {
    .topnav.responsive {position: relative;}
        .topnav.responsive a.icon {
            position: absolute;
            right: 0;
            top: 0;
        }
        .topnav.responsive a {
            float: none;
            display: block;
            text-align: left;
        }
    }
</style>
