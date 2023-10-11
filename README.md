this a javascript project
<!DOCTYPE HTML>
<html>
    <head>
        <meta name="viewport" content="width=device-width,initial-scale=1.0">
        <title>Responsive Sidebar Menu</title>
    </head>
    <body>
        <div class="navigation">
            <ul>
                <li>
                    <a href="#">
                        <span class="icon"><ion-icon name="home-outline"></ion-icon></span>
                        <span class="title">Home</span>
                    </a>
                </li>
                <li>
                    <a href="#">
                        <span class="icon"><ion-icon name="image-outline"></ion-icon></span>
                        <span class="title">Profile</span>
                    </a>
                </li>
                <li>
                    <a href="#">
                        <span class="icon"><ion-icon name="chatbox-ellipses-outline"></ion-icon></span>
                        <span class="title">Messages</span>
                    </a>
                </li>
                <li>
                    <a href="#">
                        <span class="icon"><ion-icon name="help-outline"></ion-icon></span>
                        <span class="title">Help</span>
                    </a>
                </li>
                <li>
                    <a href="#">
                        <span class="icon"><ion-icon name="settings-outline"></ion-icon></span>
                        <span class="title">Setting</span>
                    </a>
                </li>
                <li>
                    <a href="#">
                        <span class="icon"><ion-icon name="lock-closed-outline"></ion-icon></span>
                        <span class="title">Password</span>
                    </a>
                </li>
                <li>
                    <a href="#">
                        <span class="icon"><ion-icon name="log-out-outline"></ion-icon></span>
                        <span class="title">Sign Out</span>
                    </a>
                </li>
            </ul>
        </div>
        <div class="toggle" onclick="toggleMenu()"></div>
        <style>
            *{
                margin: 0;
                padding: 0;
                box-sizing: border-box;
                font-family: 'poppins',sans-serif;
            }
            body{
                min-height: 100vh;
                background: #150019;
            }
            .navigation{
                position: fixed;
                width: 60px;
                height: 100%;
                background: #3e0748;
                transition: 0.5s;
                overflow: hidden;
            }
            .navigation:hover,
            .navigation.active{
                width: 300px;
            }
            .navigation ul{
                position: absolute;
                top: 0;
                left: 0;
                width: 100%;
            }
            .navigation ul li{
                position: relative;
                width: 100%;
                list-style: none;
            }
            .navigation ul li:hover{
                background: #ea1d63;
            }
            .navigation ul li a{
                position: relative;
                display: block;
                width: 100%;
                display: flex;
                text-decoration: none;
                color: #fff;
            }
            .navigation ul li a .icon{
                position: relative;
                display: block;
                min-width: 60px;
                height: 60px;
                line-height: 60px;
                text-align: center;
            }
            .navigation ul li a .icon .fa{
                font-size: 24px;
            }
            .navigation ul li a .title{
                position: relative;
                display: block;
                padding: 0 10px;
                height: 60px;
                line-height: 60px;
                text-align: start;
                white-space: nowrap;
            }
            .toggle{
                position: absolute;
                top: 0;
                right: 0;
                width: 60px;
                height: 60px;
                background: #330748;
                cursor: pointer;
            }
            .toggle.active{
                background: #ea1d63;
            }
            .toggle:before{
                content: '=';
                font-family:'fontAwesome';
                position: absolute;
                width: 100%;
                height: 100%;
                line-height: 60px;
                text-align: center;
                font-size: 24px;
                color: #fff;
            }
            .toggle.active:before{
                content: '/';
            }
            @media(max-width: 767px){
                .navigation{
                    left: -60px;
                }
                .navigation.active{
                    left: 0px;
                    width: 100%;
                }
            }
        </style>
        <script>
            function toggleMenu(){
                let navigation = document.querySelector('.navigation');
                let toggle = document.querySelector('.toggle');
                navigation.classList.toggle('active');
                toggle.classList.toggle('active');
            }
        </script>
    </body>
</html>
