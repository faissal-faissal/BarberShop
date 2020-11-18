/*  Mise en place de la barre de navigation responsive  */

let constHmaburger = document.querySelector('.hamburger');
let menuNav = document.querySelector('.menu-nav');
let btnListeNav = document.querySelector('.liste-nav');

constHmaburger.addEventListener('click', presentation);

function presentation() {
    menuNav.classList.toggle('active');
    btnListeNav.classList.toggle('active');
}

const allLinks = document.querySelectorAll('.item-nav');

allLinks.forEach(function(item){
    item.addEventListener('click', presentation)
})



/*  Changement de couleur de la barre de navigation  */

let lienNav = document.getElementsByClassName('lien-nav');
let itemNav = document.getElementsByClassName('item-nav');

window.onscroll = function () {
    if(document.documentElement.scrollTop > 980) {
        menuNav.style.background = "#373737";
        btnListeNav.style.background = "#373737";
        constHmaburger.style.background = "#373737";
        lienNav[0].style.color = "white";
        lienNav[1].style.color = "white";
        lienNav[2].style.color = "white";
        lienNav[3].style.color = "white";
    }
    if(document.documentElement.scrollTop < 980) {
        menuNav.style.background = "#f0Ead6";
        btnListeNav.style.background = "#f0Ead6";
        constHmaburger.style.background = "#f0Ead6";
        lienNav[0].style.color = "#333";
        lienNav[1].style.color = "#333";
        lienNav[2].style.color = "#333";
        lienNav[3].style.color = "#333";
    }
}