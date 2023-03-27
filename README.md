<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <!-- ------------------ Favicon ------------------ -->
    <link rel="shortcut icon" href="./assets/img/favicon.ico" type="image/x-icon">

    <!-- ------------------ Title ------------------ -->
    <title>Disney+ Hotstar - Watch TV Shows Online</title>

    <!-- ------------------ Style Sheet ------------------ -->
    <link rel="stylesheet" href="./assets/css/style.css">
    <style>/* ---------------- Google Fonts ---------------- */
        @import url('https://fonts.googleapis.com/css2?family=Roboto:wght@100;300;400;500;700&display=swap');
        
        /* ---------------- Root ---------------- */
        :root {
            --background: #0c111b;
            --text-color: #fff;
            --button: #1f80e0;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        html {
            scroll-behavior: smooth;
        }
        
        body {
            width: 100%;
            background: var(--background);
            position: relative;
            font-family: "Roboto", sans-serif;
        }
        
        /* ---------------- Navbar ---------------- */
        .navbar {
            width: 100%;
            height: 80px;
            position: fixed;
            top: 0;
            left: 0;
            padding: 0 4%;
            background: var(--background);
            z-index: 9;
            display: flex;
            align-items: center;
        }
        
        .logo {
            height: 80px;
            width: 140px;
        }
        
        .nav-links {
            margin-top: 10px;
            display: flex;
            list-style: none;
        }
        
        .nav-items a {
            text-decoration: none;
            color: rgba(255, 255, 255, 0.8);
            opacity: 0.9;
            font-size: 16px;
            font-weight: 400;
            padding: 20px 15px 20px;
        }
        
        .nav-items a:hover {
            color: var(--text-color);
        }
        
        .nav-links .icon {
            margin-left: 15px;
            width: 40px;
            height: 15px;
            background: url(../img/kids.svg) no-repeat;
        }
        
        .right-container {
            display: block;
            margin-left: auto;
        }
        
        .search-box {
            border: none;
            border-bottom: 1px solid #aaa;
            background: transparent;
            outline: none;
            height: 30px;
            color: var(--text-color);
            width: 250px;
            text-transform: capitalize;
            font-size: 16px;
            font-weight: 500;
            transition: 0.5s;
        }
        
        .search-box:focus {
            width: 400px;
            border-color: var(--button);
        }
        
        .sub-btn {
            background: var(--button);
            height: 30px;
            padding: 0 20px;
            color: var(--text-color);
            border-radius: 5px;
            border: none;
            outline: none;
            text-transform: uppercase;
            font-weight: 700;
            font-size: 12px;
            margin: 0 10px;
        }
        
        .login-link {
            color: var(--text-color);
            opacity: 0.9;
            text-transform: uppercase;
            font-size: 15px;
            font-weight: 700;
            text-decoration: none;
        }
        
        .carousel-container {
            position: relative;
            width: 100%;
            height: 500px;
            padding: 20px 0;
            overflow-x: hidden;
            margin-top: 80px;
        }
        
        .carousel {
            display: flex;
            width: 92%;
            height: 100%;
            position: relative;
            margin: auto;
        }
        
        .slider {
            flex: 0 0 auto;
            margin-right: 30px;
            position: relative;
            background: rgba(0, 0, 0, 0.5);
            border-radius: 5px;
            width: 100%;
            height: 100%;
            left: 0;
            transition: 1s;
            overflow: hidden;
        }
        
        .slider img {
            width: 70%;
            min-height: 100%;
            object-fit: cover;
            display: block;
            margin-left: auto;
        }
        
        .slide-content {
            position: absolute;
            width: 50%;
            height: 100%;
            z-index: 2;
            background: linear-gradient(to right, #030b17 80%, #0c111b00);
            color: var(--text-color);
            top: 0;
        }
        
        .movie-title {
            padding-left: 50px;
            text-transform: capitalize;
            margin-top: 80px;
        }
        
        .movie-des {
            width: 80%;
            line-height: 30px;
            padding-left: 50px;
            margin-top: 30px;
            opacity: 0.8;
        }
        
        .video-card-container {
            position: relative;
            width: 92%;
            margin: auto;
            height: 10vw;
            display: flex;
            margin-bottom: 20px;
            justify-content: space-between;
        }
        
        .video-card {
            position: relative;
            min-width: calc(100%/5 - 10px);
            width: calc(100%/5 - 10px);
            height: 100%;
            border-radius: 5px;
            overflow: hidden;
            background: #030b17;
        }
        
        .video-card-image,
        .card-video {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        
        .card-video {
            position: absolute;
        }
        
        .video-card:hover .video-card-image {
            display: none;
        }
        
        .title {
            color: var(--text-color);
            opacity: 0.9;
            padding-left: 4%;
            text-transform: capitalize;
            font-size: 22px;
            font-weight: 500;
        }
        
        .movies-list {
            width: 100%;
            height: 220px;
            position: relative;
            margin: 10px 0 20px;
        }
        
        .card-container {
            position: relative;
            width: 92%;
            padding-left: 10px;
            height: 220px;
            display: flex;
            margin: 0 auto;
            align-items: center;
            overflow-x: auto;
            overflow-y: visible;
            scroll-behavior: smooth;
        }
        
        .card-container::-webkit-scrollbar {
            display: none;
        }
        
        .card {
            position: relative;
            min-width: 150px;
            width: 150px;
            height: 200px;
            border-radius: 5px;
            overflow: hidden;
            margin-right: 10px;
            transition: 0.5s;
            background: #000;
        }
        
        .card-img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        
        .card:hover {
            transform: scale(1.1);
        }
        
        .card:hover .card-body {
            opacity: 1;
        }
        
        .card-body {
            opacity: 0;
            width: 100%;
            height: 100%;
            position: absolute;
            top: 0;
            left: 0;
            z-index: 2;
            background: linear-gradient(to bottom, rgba(4, 8, 15, 0), #192133 90%);
            padding: 10px;
            transition: 0.5s;
        }
        
        .name {
            color: var(--text-color);
            font-size: 15px;
            font-weight: 500;
            text-transform: capitalize;
            margin-top: 60%;
        }
        
        .des {
            color: var(--text-color);
            opacity: 0.8;
            margin: 5px 0;
            font-weight: 500;
            font-size: 12px;
        }
        
        .watchlist-btn {
            position: relative;
            width: 100%;
            text-transform: capitalize;
            background: none;
            border: none;
            font-weight: 500;
            text-align: right;
            color: rgba(255, 255, 255, 0.5);
            margin: 5px 0;
            cursor: pointer;
            padding: 10px 5px;
            border-radius: 5px;
        }
        
        .watchlist-btn::before {
            content: '';
            position: absolute;
            top: 0;
            left: -5px;
            height: 35px;
            width: 35px;
            background-image: url(../img/add.png);
            background-size: cover;
            transform: scale(0.4);
        }
        
        .watchlist-btn:hover {
            color: var(--text-color);
            background: rgba(255, 255, 255, 0.1);
        }
        
        .pre-btn,
        .nxt-btn {
            position: absolute;
            top: 0;
            width: 5%;
            height: 100%;
            z-index: 2;
            border: none;
            cursor: pointer;
            outline: none;
        }
        
        .pre-btn {
            left: 0;
            background: linear-gradient(to right, #0c111b 0%, #0c111b00);
        }
        
        .nxt-btn {
            right: 0;
            background: linear-gradient(to right, #0c111b 0%, #0c111b00);
        }
        
        .pre-btn img,
        .nxt-btn img {
            width: 15px;
            height: 20px;
            opacity: 0;
        }
        
        .pre-btn:hover img,
        .nxt-btn:hover img {
            opacity: 1;
        }</style>
</head>

<body>
    <!-- ------------------ Navbar ------------------ -->
    <nav class="navbar">
        <img src="./assets/img/logo (1).svg" class="logo" alt="Logo">
        <ul class="nav-links">
            <li class="nav-items"><a href="#">TV</a></li>
            <li class="nav-items"><a href="#">Movies</a></li>
            <li class="nav-items"><a href="#">Sports</a></li>
            <li class="nav-items"><a href="#">Premium</a></li>
            <li class="nav-items"><a href="#">Disney+</a></li>
            <li class="icon"><a href="#"></a></li>
        </ul>

        <div class="right-container">
            <input type="text" class="search-box" placeholder="search">
            <button class="sub-btn">Subscribe</button>
            <a href="#" class="login-link">login</a>
        </div>
    </nav>

    <!-- ------------------ Carousel ------------------ -->
    <div class="carousel-container">
        <div class="carousel">
            <!-- <div class="slider">
                <div class="slide-content">
                    <h1 class="movie-title">loki</h1>
                    <p class="movie-des">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quam distinctio molestiae quis praesentium cum obcaecati eveniet voluptates exercitationem eum accusantium.</p>
                </div>
                <img src="./assets/img/slider 1.png" alt="Slider">
            </div> -->
        </div>
    </div>

    <!-- ------------------ Video Card ------------------ -->
    <div class="video-card-container">
        <div class="video-card">
            <img src="./assets/img/disney.png" class="video-card-image" alt="">
            <video src="./assets/video/disney.mp4" mute loop class="card-video"></video>
        </div>
        <div class="video-card">
            <img src="./assets/img/pixar.png" class="video-card-image" alt="">
            <video src="./assets/video/pixar.mp4" mute loop class="card-video"></video>
        </div>
        <div class="video-card">
            <img src="./assets/img/marvel.png" class="video-card-image" alt="">
            <video src="./assets/video/marvel.mp4" mute loop class="card-video"></video>
        </div>
        <div class="video-card">
            <img src="./assets/img/star-wars.png" class="video-card-image" alt="">
            <video src="./assets/video/star-war.mp4" mute loop class="card-video"></video>
        </div>
        <div class="video-card">
            <img src="./assets/img/geographic.png" class="video-card-image" alt="">
            <video src="./assets/video/geographic.mp4" mute loop class="card-video"></video>
        </div>
    </div>

    <!-- ------------------ Recommendation ------------------ -->
    <h1 class="title">recommended for you</h1>
    <div class="movies-list">
        <button class="pre-btn"><img src="./assets/img/pre.png" alt=""></button>
        <button class="nxt-btn"><img src="./assets/img/nxt.png" alt=""></button>
        <div class="card-container">
            <div class="card">
                <img src="./assets/img/poster 4.webp" class="card-img" alt="">
                <div class="card-body">
                    <h2 class="name">Chichore</h2>
                    <h6 class="des">Lorem ipsum dolor sit consectetur elit.</h6>
                    <button class="watchlist-btn">add to watchlist</button>
                </div>
            </div>
            <div class="card">
                <img src="./assets/img/poster 4.png" class="card-img" alt="">
                <div class="card-body">
                    <h2 class="name">Avengers Endgame</h2>
                    <h6 class="des">Lorem ipsum dolor sit consectetur elit.</h6>
                    <button class="watchlist-btn">add to watchlist</button>
                </div>
            </div>
            <div class="card">
                <img src="./assets/img/poster 11.png" class="card-img" alt="">
                <div class="card-body">
                    <h2 class="name">Ford v Ferrari</h2>
                    <h6 class="des">Lorem ipsum dolor sit consectetur elit.</h6>
                    <button class="watchlist-btn">add to watchlist</button>
                </div>
            </div>
            <div class="card">
                <img src="./assets/img/poster 2.png" class="card-img" alt="">
                <div class="card-body">
                    <h2 class="name">Mulan</h2>
                    <h6 class="des">Lorem ipsum dolor sit consectetur elit.</h6>
                    <button class="watchlist-btn">add to watchlist</button>
                </div>
            </div>
            <div class="card">
                <img src="./assets/img/poster 1.png" class="card-img" alt="">
                <div class="card-body">
                    <h2 class="name">Loki</h2>
                    <h6 class="des">Lorem ipsum dolor sit consectetur elit.</h6>
                    <button class="watchlist-btn">add to watchlist</button>
                </div>
            </div>
            <div class="card">
                <img src="./assets/img/poster 5.png" class="card-img" alt="">
                <div class="card-body">
                    <h2 class="name">Thor Ragnarok</h2>
                    <h6 class="des">Lorem ipsum dolor sit consectetur elit.</h6>
                    <button class="watchlist-btn">add to watchlist</button>
                </div>
            </div>
            <div class="card">
                <img src="./assets/img/poster 6.png" class="card-img" alt="">
                <div class="card-body">
                    <h2 class="name">Avengers</h2>
                    <h6 class="des">Lorem ipsum dolor sit consectetur elit.</h6>
                    <button class="watchlist-btn">add to watchlist</button>
                </div>
            </div>
            <div class="card">
                <img src="./assets/img/card 10.webp" class="card-img" alt="">
                <div class="card-body">
                    <h2 class="name">Ok Computer</h2>
                    <h6 class="des">Lorem ipsum dolor sit consectetur elit.</h6>
                    <button class="watchlist-btn">add to watchlist</button>
                </div>
            </div>
            <div class="card">
                <img src="./assets/img/card 11.webp" class="card-img" alt="">
                <div class="card-body">
                    <h2 class="name">Dil Bechara</h2>
                    <h6 class="des">Lorem ipsum dolor sit consectetur elit.</h6>
                    <button class="watchlist-btn">add to watchlist</button>
                </div>
            </div>
            <div class="card">
                <img src="./assets/img/poster 8.png" class="card-img" alt="">
                <div class="card-body">
                    <h2 class="name">Soul</h2>
                    <h6 class="des">Lorem ipsum dolor sit consectetur elit.</h6>
                    <button class="watchlist-btn">add to watchlist</button>
                </div>
            </div>
            <div class="card">
                <img src="./assets/img/card 13.webp" class="card-img" alt="">
                <div class="card-body">
                    <h2 class="name">The Office</h2>
                    <h6 class="des">Lorem ipsum dolor sit consectetur elit.</h6>
                    <button class="watchlist-btn">add to watchlist</button>
                </div>
            </div>
            <div class="card">
                <img src="./assets/img/poster 10.png" class="card-img" alt="">
                <div class="card-body">
                    <h2 class="name">Luca</h2>
                    <h6 class="des">Lorem ipsum dolor sit consectetur elit.</h6>
                    <button class="watchlist-btn">add to watchlist</button>
                </div>
            </div>
            <div class="card">
                <img src="./assets/img/poster 12.png" class="card-img" alt="">
                <div class="card-body">
                    <h2 class="name">Dark Phoenix</h2>
                    <h6 class="des">Lorem ipsum dolor sit consectetur elit.</h6>
                    <button class="watchlist-btn">add to watchlist</button>
                </div>
            </div>
            <div class="card">
                <img src="./assets/img/card 12.webp" class="card-img" alt="">
                <div class="card-body">
                    <h2 class="name">TanHaji</h2>
                    <h6 class="des">Lorem ipsum dolor sit consectetur elit.</h6>
                    <button class="watchlist-btn">add to watchlist</button>
                </div>
            </div>
            <div class="card">
                <img src="./assets/img/card 14.webp" class="card-img" alt="">
                <div class="card-body">
                    <h2 class="name">Euphoria</h2>
                    <h6 class="des">Lorem ipsum dolor sit consectetur elit.</h6>
                    <button class="watchlist-btn">add to watchlist</button>
                </div>
            </div>
        </div>
    </div>

    <!-- ------------------ Papular Shows ------------------ -->
    <h1 class="title">Popular Shows</h1>
    <div class="movies-list">
        <button class="pre-btn"><img src="./assets/img/pre.png" alt=""></button>
        <button class="nxt-btn"><img src="./assets/img/nxt.png" alt=""></button>
        <div class="card-container">
            <div class="card">
                <img src="./assets/img/card 3.webp" class="card-img" alt="">
                <div class="card-body">
                    <h2 class="name">Yeh Rishta</h2>
                    <h6 class="des">Lorem ipsum dolor sit consectetur elit.</h6>
                    <button class="watchlist-btn">add to watchlist</button>
                </div>
            </div>
            <div class="card">
                <img src="./assets/img/card 4.webp" class="card-img" alt="">
                <div class="card-body">
                    <h2 class="name">Anupama</h2>
                    <h6 class="des">Lorem ipsum dolor sit consectetur elit.</h6>
                    <button class="watchlist-btn">add to watchlist</button>
                </div>
            </div>
            <div class="card">
                <img src="./assets/img/card 2.webp" class="card-img" alt="">
                <div class="card-body">
                    <h2 class="name">Imlie</h2>
                    <h6 class="des">Lorem ipsum dolor sit consectetur elit.</h6>
                    <button class="watchlist-btn">add to watchlist</button>
                </div>
            </div>
            <div class="card">
                <img src="./assets/img/card 1.webp" class="card-img" alt="">
                <div class="card-body">
                    <h2 class="name">City of Dreams</h2>
                    <h6 class="des">Lorem ipsum dolor sit consectetur elit.</h6>
                    <button class="watchlist-btn">add to watchlist</button>
                </div>
            </div>
            <div class="card">
                <img src="./assets/img/card 5.webp" class="card-img" alt="">
                <div class="card-body">
                    <h2 class="name">Shin-chan</h2>
                    <h6 class="des">Lorem ipsum dolor sit consectetur elit.</h6>
                    <button class="watchlist-btn">add to watchlist</button>
                </div>
            </div>
            <div class="card">
                <img src="./assets/img/card 8.webp" class="card-img" alt="">
                <div class="card-body">
                    <h2 class="name">Doraemon</h2>
                    <h6 class="des">Lorem ipsum dolor sit consectetur elit.</h6>
                    <button class="watchlist-btn">add to watchlist</button>
                </div>
            </div>
            <div class="card">
                <img src="./assets/img/card 9.webp" class="card-img" alt="">
                <div class="card-body">
                    <h2 class="name">Mahadev</h2>
                    <h6 class="des">Lorem ipsum dolor sit consectetur elit.</h6>
                    <button class="watchlist-btn">add to watchlist</button>
                </div>
            </div>
            <div class="card">
                <img src="./assets/img/card 7.webp" class="card-img" alt="">
                <div class="card-body">
                    <h2 class="name">Grahan</h2>
                    <h6 class="des">Lorem ipsum dolor sit consectetur elit.</h6>
                    <button class="watchlist-btn">add to watchlist</button>
                </div>
            </div>
            <div class="card">
                <img src="./assets/img/card 6.webp" class="card-img" alt="">
                <div class="card-body">
                    <h2 class="name">Pandya Store</h2>
                    <h6 class="des">Lorem ipsum dolor sit consectetur elit.</h6>
                    <button class="watchlist-btn">add to watchlist</button>
                </div>
            </div>
            <div class="card">
                <img src="./assets/img/poster 10.png" class="card-img" alt="">
                <div class="card-body">
                    <h2 class="name">Luca</h2>
                    <h6 class="des">Lorem ipsum dolor sit consectetur elit.</h6>
                    <button class="watchlist-btn">add to watchlist</button>
                </div>
            </div>
            <div class="card">
                <img src="./assets/img/card 15.webp" class="card-img" alt="">
                <div class="card-body">
                    <h2 class="name">Mahabharat</h2>
                    <h6 class="des">Lorem ipsum dolor sit consectetur elit.</h6>
                    <button class="watchlist-btn">add to watchlist</button>
                </div>
            </div>
            <div class="card">
                <img src="./assets/img/card 16.webp" class="card-img" alt="">
                <div class="card-body">
                    <h2 class="name">RadhaKrishn</h2>
                    <h6 class="des">Lorem ipsum dolor sit consectetur elit.</h6>
                    <button class="watchlist-btn">add to watchlist</button>
                </div>
            </div>
            <div class="card">
                <img src="./assets/img/card 17.webp" class="card-img" alt="">
                <div class="card-body">
                    <h2 class="name">Phineas and Ferb</h2>
                    <h6 class="des">Lorem ipsum dolor sit consectetur elit.</h6>
                    <button class="watchlist-btn">add to watchlist</button>
                </div>
            </div>
            <div class="card">
                <img src="./assets/img/poster 1.png" class="card-img" alt="">
                <div class="card-body">
                    <h2 class="name">Loki</h2>
                    <h6 class="des">Lorem ipsum dolor sit consectetur elit.</h6>
                    <button class="watchlist-btn">add to watchlist</button>
                </div>
            </div>
            <div class="card">
                <img src="./assets/img/card 18.webp" class="card-img" alt="">
                <div class="card-body">
                    <h2 class="name">Special Ops</h2>
                    <h6 class="des">Lorem ipsum dolor sit consectetur elit.</h6>
                    <button class="watchlist-btn">add to watchlist</button>
                </div>
            </div>
            <div class="card">
                <img src="./assets/img/card 19.webp" class="card-img" alt="">
                <div class="card-body">
                    <h2 class="name">Hostages</h2>
                    <h6 class="des">Lorem ipsum dolor sit consectetur elit.</h6>
                    <button class="watchlist-btn">add to watchlist</button>
                </div>
            </div>
            <div class="card">
                <img src="./assets/img/card 20.webp" class="card-img" alt="">
                <div class="card-body">
                    <h2 class="name">Criminal Justice</h2>
                    <h6 class="des">Lorem ipsum dolor sit consectetur elit.</h6>
                    <button class="watchlist-btn">add to watchlist</button>
                </div>
            </div>
        </div>
    </div>

    <!-- ------------------ New Releases ------------------ -->
    <h1 class="title">New Releases</h1>
    <div class="movies-list">
        <button class="pre-btn"><img src="./assets/img/pre.png" alt=""></button>
        <button class="nxt-btn"><img src="./assets/img/nxt.png" alt=""></button>
        <div class="card-container">
            <div class="card">
                <img src="./assets/img/poster 3.webp" class="card-img" alt="">
                <div class="card-body">
                    <h2 class="name">Collar Bomb</h2>
                    <h6 class="des">Lorem ipsum dolor sit consectetur elit.</h6>
                    <button class="watchlist-btn">add to watchlist</button>
                </div>
            </div>
            <div class="card">
                <img src="./assets/img/poster 5.webp" class="card-img" alt="">
                <div class="card-body">
                    <h2 class="name">WandaVision</h2>
                    <h6 class="des">Lorem ipsum dolor sit consectetur elit.</h6>
                    <button class="watchlist-btn">add to watchlist</button>
                </div>
            </div>
            <div class="card">
                <img src="./assets/img/poster 8.webp" class="card-img" alt="">
                <div class="card-body">
                    <h2 class="name">Carbon</h2>
                    <h6 class="des">Lorem ipsum dolor sit consectetur elit.</h6>
                    <button class="watchlist-btn">add to watchlist</button>
                </div>
            </div>
            <div class="card">
                <img src="./assets/img/poster 1.webp" class="card-img" alt="">
                <div class="card-body">
                    <h2 class="name">Hungama 2</h2>
                    <h6 class="des">Lorem ipsum dolor sit consectetur elit.</h6>
                    <button class="watchlist-btn">add to watchlist</button>
                </div>
            </div>
            <div class="card">
                <img src="./assets/img/poster 2.webp" class="card-img" alt="">
                <div class="card-body">
                    <h2 class="name">Hanuman</h2>
                    <h6 class="des">Lorem ipsum dolor sit consectetur elit.</h6>
                    <button class="watchlist-btn">add to watchlist</button>
                </div>
            </div>
            <div class="card">
                <img src="./assets/img/poster 9.webp" class="card-img" alt="">
                <div class="card-body">
                    <h2 class="name">Boys Don't Cry</h2>
                    <h6 class="des">Lorem ipsum dolor sit consectetur elit.</h6>
                    <button class="watchlist-btn">add to watchlist</button>
                </div>
            </div>
            <div class="card">
                <img src="./assets/img/poster 10.webp" class="card-img" alt="">
                <div class="card-body">
                    <h2 class="name">Shaadisthan</h2>
                    <h6 class="des">Lorem ipsum dolor sit consectetur elit.</h6>
                    <button class="watchlist-btn">add to watchlist</button>
                </div>
            </div>
            <div class="card">
                <img src="./assets/img/poster 1.png" class="card-img" alt="">
                <div class="card-body">
                    <h2 class="name">Loki</h2>
                    <h6 class="des">Lorem ipsum dolor sit consectetur elit.</h6>
                    <button class="watchlist-btn">add to watchlist</button>
                </div>
            </div>
            <div class="card">
                <img src="./assets/img/poster 7.webp" class="card-img" alt="">
                <div class="card-body">
                    <h2 class="name">Love, Simon</h2>
                    <h6 class="des">Lorem ipsum dolor sit consectetur elit.</h6>
                    <button class="watchlist-btn">add to watchlist</button>
                </div>
            </div>
            <div class="card">
                <img src="./assets/img/poster 14.webp" class="card-img" alt="">
                <div class="card-body">
                    <h2 class="name">Betty</h2>
                    <h6 class="des">Lorem ipsum dolor sit consectetur elit.</h6>
                    <button class="watchlist-btn">add to watchlist</button>
                </div>
            </div>
            <div class="card">
                <img src="./assets/img/poster 15.webp" class="card-img" alt="">
                <div class="card-body">
                    <h2 class="name">Chhuri</h2>
                    <h6 class="des">Lorem ipsum dolor sit consectetur elit.</h6>
                    <button class="watchlist-btn">add to watchlist</button>
                </div>
            </div>
            <div class="card">
                <img src="./assets/img/poster 16.webp" class="card-img" alt="">
                <div class="card-body">
                    <h2 class="name">Cars 3</h2>
                    <h6 class="des">Lorem ipsum dolor sit consectetur elit.</h6>
                    <button class="watchlist-btn">add to watchlist</button>
                </div>
            </div>
            <div class="card">
                <img src="./assets/img/poster 13.webp" class="card-img" alt="">
                <div class="card-body">
                    <h2 class="name">Pose</h2>
                    <h6 class="des">Lorem ipsum dolor sit consectetur elit.</h6>
                    <button class="watchlist-btn">add to watchlist</button>
                </div>
            </div>
            <div class="card">
                <img src="./assets/img/poster 6.webp" class="card-img" alt="">
                <div class="card-body">
                    <h2 class="name">Modern Family</h2>
                    <h6 class="des">Lorem ipsum dolor sit consectetur elit.</h6>
                    <button class="watchlist-btn">add to watchlist</button>
                </div>
            </div>
            <div class="card">
                <img src="./assets/img/poster 17.webp" class="card-img" alt="">
                <div class="card-body">
                    <h2 class="name">Brave</h2>
                    <h6 class="des">Lorem ipsum dolor sit consectetur elit.</h6>
                    <button class="watchlist-btn">add to watchlist</button>
                </div>
            </div>
            <div class="card">
                <img src="./assets/img/poster 18.webp" class="card-img" alt="">
                <div class="card-body">
                    <h2 class="name">Dil Bechara</h2>
                    <h6 class="des">Lorem ipsum dolor sit consectetur elit.</h6>
                    <button class="watchlist-btn">add to watchlist</button>
                </div>
            </div>
        </div>
    </div>

    <!-- ------------------ JavaScript ------------------ -->
    <script src="./assets/js/data.js">
        let movies = [
  {
    name: "wanda vision",
    des: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Velit porro et veniam excepturi, eaque voluptatem impedit nulla laboriosam facilis ut laboriosam libero!",
    image: "assets/img/slider 3.png",
  },
  {
    name: "falcon and the winter soldier",
    des: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Velit porro et veniam excepturi, eaque voluptatem impedit nulla laboriosam facilis ut laboriosam libero!",
    image: "assets/img/slider 2.png",
  },
  {
    name: "raya and the last dragon",
    des: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Velit porro et veniam excepturi, eaque voluptatem impedit nulla laboriosam facilis ut laboriosam libero!",
    image: "assets/img/slider 4.png",
  },
  {
    name: "loki",
    des: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Velit porro et veniam excepturi, eaque voluptatem impedit nulla laboriosam facilis ut laboriosam libero!",
    image: "assets/img/slider 1.png",
  },
  {
    name: "luca",
    des: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Velit porro et veniam excepturi, eaque voluptatem impedit nulla laboriosam facilis ut laboriosam libero!",
    image: "assets/img/slider 5.png",
  },
];
    </script>
    <script src="./assets/js/main.js">// Carousel
        const carousel = document.querySelector(".carousel");
        let sliders = [];
        
        let slideIndex = 0;
        
        const createSlide = () => {
          if (slideIndex >= movies.length) {
            slideIndex = 0;
          }
        
          // Creating DOM element
          let slide = document.createElement("div");
          let imgElement = document.createElement("img");
          let content = document.createElement("div");
          let h1 = document.createElement("h1");
          let p = document.createElement("p");
        
          // Attaching all elements
          imgElement.appendChild(document.createTextNode(""));
          h1.appendChild(document.createTextNode(movies[slideIndex].name));
          p.appendChild(document.createTextNode(movies[slideIndex].des));
          content.appendChild(h1);
          content.appendChild(p);
          slide.appendChild(imgElement);
          slide.appendChild(content);
          carousel.appendChild(slide);
        
          // Setting up image
          imgElement.src = movies[slideIndex].image;
          slideIndex++;
        
          // Setting elements class-name
          slide.className = "slider";
          content.className = "slide-content";
          h1.className = "movie-title";
          p.className = "movie-des";
        
          sliders.push(slide);
        
          if (sliders.length) {
            sliders[0].style.marginLeft = `calc(-${100 * (sliders.length - 2)}% - ${
              30 * (sliders.length - 2)
            }px)`;
          }
        };
        
        for (let i = 0; i < 3; i++) {
          createSlide();
        }
        
        setInterval(() => {
          createSlide();
        }, 5000);
        
        // Video cards
        const videoCards = [...document.querySelectorAll(".video-card")];
        
        videoCards.forEach((item) => {
          item.addEventListener("mouseover", () => {
            let video = item.children[1];
            video.play();
          });
          item.addEventListener("mouseleave", () => {
            let video = item.children[1];
            video.pause();
          });
        });
        
        // Movie cards
        let cardContainers = [...document.querySelectorAll(".card-container")];
        let preBTns = [...document.querySelectorAll(".pre-btn")];
        let nxtBtns = [...document.querySelectorAll(".nxt-btn")];
        
        cardContainers.forEach((item, i) => {
          let containerDimensions = item.getBoundingClientRect();
          let containerWidth = containerDimensions.width;
        
          nxtBtns[i].addEventListener("click", () => {
            item.scrollLeft += containerWidth - 200;
          });
        
          preBTns[i].addEventListener("click", () => {
            item.scrollLeft -= containerWidth + 200;
          });
        });</script>

</body>

</html>
