<svelte:head>
    <title>Petrichor CA Program</title>
</svelte:head>

<div class="container">
    <div class="sidebar">
        <span class="sidebar-text">
             Petrichor / IIT Palakkad // Petrichor / IIT Palakkad // Petrichor / IIT Palakkad // Petrichor / IIT Palakkad // 
        </span>
    </div>
    <div class="main">
        <slot></slot>
    </div>
</div>

<!-- <span class="credits">
</span>
    The Petrichor Web Development Team, IIT Palakkad -->
<footer>
    <div class="links">
        <a href="/contactus">Contact Us</a>
        <a href="/contactus">Technical Issues?</a>
        <a href="https://petrichor.events">Main Website</a>
    </div>
</footer>
<style>
    footer{
        position: fixed;
        width: 100vw;
        bottom: 0;
        display: grid;
        place-items: center;
        padding-top: .4em;
        padding-bottom: .4em;
        background-color: rgb(26, 26, 26);
        font-size:min(20px, 4vw);
    }
    .credits{
        display: grid;
        place-items: center;
    }
    .links{
        display: inline;
        /* margin-bottom: 1em; */
    }
    .links > a{
        text-decoration: unset;
        color: inherit;
        margin-inline: .3em;
        position: relative;
        cursor: pointer;
    }
    .links > a::after{
        content: "";
        position: absolute;
        width: 100%;
        height: .4em;
        z-index: -1;
        background-color: var(--accent);
        left: 0;
        bottom: 0;
    }
    .links > a:hover:after{
        height: 1em;
        transition: 200ms ease-in-out;
    }
    .sidebar{
        width: 2vw;
        background-color: var(--accent-light);
        color: var(--accent-dark);
        writing-mode: sideways-lr;
        -webkit-writing-mode: vertical-lr;
        text-orientation: mixed;
        height: max-content ;
        font-size: 1.5vw;
        bottom: 0;
        display: flex;
        overflow: hidden;
        align-items: center;
        position: fixed;
        z-index: 1000;
    }
    .sidebar-text{
        position: relative;
        animation: scrolldown 2s linear infinite;
    }
    @keyframes scrolldown{
        from{
            bottom: 0;
        }
        to{
            bottom: -25.15%;
        }
    }
    @keyframes scrollleft{
        from{
            left: 0;
        }
        to{
            left: -25.15%;
        }
    }
    .container{
        display: flex;
    }
    .main{
        display: flex;
        flex-direction: column;
        align-items: center;
        width: 100vw;
        height: 100%;
    }
   
    @media (max-width: 1000px){
        
        .sidebar{
            width: max-content;
            height: 5vh;
            background-color: white;
            color: black;
            writing-mode: unset;
            -webkit-writing-mode: unset;
            font-size: 6vw;
            top: 0;
            display: flex;
            overflow: hidden;
            position: fixed;
        }
        .sidebar-text{
            animation: scrollleft 3s linear infinite;
            overflow: unset;
            width: max-content;
            white-space: nowrap;
        }
        .main{
            margin-top: 5vh;
            width: max-content;
            /* align-items: unset; */
        }
    }
</style>