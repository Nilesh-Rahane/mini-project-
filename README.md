# mini-project
A simple mini project featuring a responsive sidebar menu with toggle functionality, built using HTML and CSS

******HTML CODE*******
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta http-equiv="X-UA-Compatible" content="IE=edge" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>CSS Project</title>
    <link rel="stylesheet"  href="style.css"/>
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link
      href="https://fonts.googleapis.com/css2?family=Poppins&display=swap"
      rel="stylesheet"
    />
    <link
      rel="stylesheet"
      href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css"
    />
    <link href="https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&family=Roboto+Serif:ital,opsz,wght@0,8..144,100..900;1,8..144,100..900&family=Roboto:ital,wght@0,100..900;1,100..900&display=swap" rel="stylesheet">

  </head>
  <body>
    <div class="main_box">
      <input type="checkbox" id="check" />
      <div class="btn_one">
        <label for="check">
          <i class="fa-solid fa-bars"></i>
        </label>
      </div>

      <div class="sidebar_menu">
        <div class="logo">
          <a href="#">Apna College</a>
        </div>

        <div class="btn_two">
          <label for="check">
            <i class="fa-solid fa-xmark"></i>
          </label>
        </div>

        <div class="menu">
          <ul>
            <li>
              <i class="fa-solid fa-image"></i>
              <a href="#">Gallery</a>
            </li>
            <li>
              <i class="fa-solid fa-arrow-up-right-from-square"></i>
              <a href="#">Shortcuts</a>
            </li>
            <li>
              <i class="fa-solid fa-photo-film"></i>
              <a href="#">Exhibits</a>
            </li>
            <li>
              <i class="fa-solid fa-calendar-days"></i>
              <a href="#">Events</a>
            </li>
            <li>
              <i class="fa-solid fa-store"></i>
              <a href="#">Store</a>
            </li>
            <li>
              <i class="fa-solid fa-phone"></i>
              <a href="#">Contact</a>
            </li>
            <li>
              <i class="fa-regular fa-comments"></i>
              <a href="#">Feedback</a>
            </li>
          </ul>
        </div>
        <div class="social_media">
          <ul>
            <a href="#"><i class="fa-brands fa-facebook"></i></i></a>
            <a href="#"><i class="fa-brands fa-twitter"></i></a>
            <a href="#"><i class="fa-brands fa-instagram"></i></i></a>
            <a href="#"><i class="fa-brands fa-youtube"></i></a>
          </ul>
        </div>
      </div>
    </div>
  </body>
</html>





****CSS CODE****
*{
    margin: 0;
    padding: 0;
    font-family: "Poppins", sans-serif;
}
.main_box{
    background: url(photo.jpg);
    height: 100vh;  /* vh----> viewport height*/
    background-size: cover;

}
.btn_one i{
    font-size: 25px;
    font-weight: 700px;
    color: white;
    position: absolute;
    line-height: 60px;
    left:16px;
    transition: all 0.2s linear;
}
.sidebar_menu{
    position: fixed;
    height: 100vh;
    width: 300px;
    left: -350px;
    background-color: rgba(255, 255,255, 0.1);
    box-shadow: 0 0 6px rgba(255,255,255,0.5);
    transition: all 0.3s linear;
}
.sidebar_menu .logo{
    position:absolute;
    width: 100%;
    line-height: 60px;
    box-shadow: 0 2px 4px rgba(255,255,255,0.5);
    height: 60px;

}
.sidebar_menu .logo a {
    position: absolute;
    left: 50px;
    color: white;
    text-decoration: none;
    font-size: 20px;
    font-weight: 500;
}
.sidebar_menu .menu{
    color: white;
   position: absolute;
   top: 80px;
   width: 100%;
}
.sidebar_menu .btn_two i{
    position: absolute;
    font-size: 25px;
    height: 60px;
    color: gray;
    left: 270px;
    top: 15px;
    /* opacity: 0.5; */
    cursor: pointer;
    transition: all 0.2s linear;
}
.sidebar_menu .menu li{
    margin: 5px;
    padding: 10px 20px;
}
.sidebar_menu .menu i,a
{
    color: white;
    text-decoration: none;
    font-size: 15px;
}
.sidebar_menu .menu i{
    padding-right:4px;
}
.sidebar_menu .social_media{
    position: absolute;
    left: 25%;
    bottom: 50px;
}
.sidebar_menu .social_media i {
    opacity: 0.5;
    padding: 5px;
    color: white;
    position: relative;
    padding-bottom: 0 5px;
}
#check{
    display: none;
}
.sidebar_menu .menu li:hover{
    box-shadow: 0 0 4px rgba(255,255,255,0.5);
}
.btn_one i:hover{
    font-size: 30px;
}
.btn_two i:hover{
    font-size: 30px;
}
.sidebar_menu .social_media i:hover{
    opacity: 1;
    transform: scale(1.1);
}
#check:checked ~ .sidebar_menu
{
    left:0;
}
#check:checked ~ .btn_one i{
    opacity: 0;
}
#check:checked ~ .sidebar_menu .btn_two i{
    opacity: 1;
}



