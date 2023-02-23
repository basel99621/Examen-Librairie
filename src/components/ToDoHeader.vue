
<template>
  <header>
    <div class="Bienvenue">
      <img
        id="logo"
        src="https://th.bing.com/th/id/R.777a724279a813f1a14ebb55c79a21c7?rik=FxILDSXK6whCpQ&riu=http%3a%2f%2fwww.clipartbest.com%2fcliparts%2fncB%2f6Lq%2fncB6LqRcA.jpeg&ehk=58qsQ%2bjL5UrV7094bQo1%2f4FPqS4lCu8ea5jg4fW%2bYRo%3d&risl=&pid=ImgRaw&r=0"
        alt="logo"
        height="90px"
        width="90px"
      />
      <h3>Bienvenue dans la librairie de BASEL AL KHATIB</h3>
    </div>
    <nav>
      <ul>
        <li><a href="#accueil">Accueil</a></li>
        <li><a href="#mesLivres">Mes livres</a></li>
        <li><a href="#propos">A propos</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </nav>
  </header>
</template>

<style scoped>
@media only screen and (max-width: 600px) {
  header {
    flex-direction: column;
    height: auto;
  }

  nav {
    display: none;
  }

  nav.show {
    display: flex;
    flex-direction: column;
    text-align: center;
  }

  nav.show li {
    margin: 10px 0;
  }

  .menu-icon {
    cursor: pointer;
    display: block;
    padding: 28px 20px;
    position: relative;
    user-select: none;
  }

  .menu-icon .navicon {
    background: #fff;
    display: block;
    height: 2px;
    position: relative;
    transition: background 0.2s ease-out;
    width: 18px;
  }

  .menu-icon .navicon:before,
  .menu-icon .navicon:after {
    background: #fff;
    content: "";
    display: block;
    height: 100%;
    position: absolute;
    transition: all 0.2s ease-out;
    width: 100%;
  }

  .menu-icon .navicon:before {
    top: 5px;
  }

  .menu-icon .navicon:after {
    top: -5px;
  }

  .menu-btn {
    display: none;
  }

  .menu-btn:checked + .menu {
    display: none;
  }

  .menu-btn:checked + .menu-icon .navicon {
    background: transparent;
  }

  .menu-btn:checked + .menu-icon .navicon:before {
    transform: rotate(-45deg);
  }

  .menu-btn:checked + .menu-icon .navicon:after {
    transform: rotate(45deg);
  }

  .menu-btn:checked + .menu-icon:not(.steps) .navicon:before,
  .menu-btn:checked + .menu-icon:not(.steps) .navicon:after {
    top: 0;
  }
}
.Bienvenue {
  color: wheat;
  text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.5);
  font-size: 18px;
  display: flex;
  align-items: center; /* Pour centrer horizontalement */
  justify-content: center; /* Pour centrer verticalement */
  height: 50%; /* Hauteur de l'élément parent */
}
.Bienvenue h3:hover {
  color: gold;
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5), 0 0 20px gold;
}

#logo {
  margin-right: 10px;
}

body {
  font-family: "Arial";
  font-size: 0.8em;
  padding: 0;
  margin: 0;
  color: #ffffff;
  background-color: rgb(228, 250, 255);
}
h1 {
  margin: 0;
  text-transform: uppercase;
  display: flex;
  flex: 2;
  font-size: 2.2vw; /* Utilisation de vw pour la taille de police */
}
ul {
  margin-left: 0px;
  display: flex;
  text-align: right;
  margin: 0px;
  padding: 0px;
}

header {
  background-color: #ff383861;
  display: flex; /* permet d'utiliser les propriétés align-items et justify-content */
  align-items: center; /* aligne verticalement les éléments */
  justify-content: space-between; /* aligne horizontalement les éléments */
}
nav {
  display: flex;
  justify-content: flex-end;
}
/*section {
  height: 100vh;
  width: 100%;
  background-size: cover;
  background-position: center;
  display: flex;
  flex-direction: column;
  justify-content: center;
}*/
li {
  display: inline-block;
  list-style-type: none;
}
a {
  text-decoration: none;
  font-family: "Roboto";
  color: white;
  text-transform: uppercase;
  font-size: 1.4em;
  padding: 0px 10px;
  display: flex;
  justify-content: center;
  align-items: center;
}
ul li a:not(:last-child) {
  border-right: 1px solid rgba(255, 255, 255, 0.2);
}
#monImage {
  display: flex;
  text-align: left;
}
</style>

