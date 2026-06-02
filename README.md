# 🌟 Portfolio Technique — Stage Fin d'Année (EPSI Paris)

<p align="center">
  <!-- Remplace ce lien par le lien de ta propre photo de profil une fois importée sur GitHub -->
  <img src="https://github.com/votre-identifiant/votre-depot/raw/main/votre-photo.jpeg" alt="Ndeye Mbasse Ndiaye" width="150" style="border-radius: 50%; border: 3px solid #7FA99B;"/>
</p>

## 🧑‍💻 À propos de moi
Je m'appelle **Ndeye Mbasse Ndiaye**, étudiante à l'**EPSI Paris**. Passionnée par l'architecture des systèmes, les réseaux et le développement d'infrastructures applicatives, j'ai réalisé mon stage de fin d'année en tant que **Développeuse Web / Intégratrice ERP**.

---

## 🏢 Présentation du Stage
* **Entreprise d'accueil :** NET-CO SERVICES (Expertise en nettoyage de copropriétés et services de proximité)
* **Période :** 4 mai au 30 juin 2026
* **Objectif :** Mener à bien la transformation digitale de l'entreprise en concevant un écosystème web unifié (Site vitrine + Boutique e-commerce) entièrement centralisé sur l'ERP **Odoo**, ainsi que la création de supports graphiques terrain.

---

## 🛠️ Réalisations Techniques & Codes Sources Customisés

Dans cette section, vous trouverez les extraits de code (HTML/CSS) que j'ai injectés et personnalisés au sein de l'éditeur avancé d'Odoo pour adapter la plateforme aux besoins métiers spécifiques de l'entreprise.

### 1. Stylisation des Rubans Fléchés Latéraux (Menu d'Action Rapide)
* **Ce que fait ce code :** Ce code CSS permet de construire et de positionner les trois rubans fléchés interactifs présents sur le côté droit de l'écran (`image_57bd24.png`). Ils offrent un accès direct et permanent aux fonctionnalités clés : **CONTACT**, **DEVIS GRATUIT SOUS 24H** et **REJOIGNEZ-NOUS**, optimisant ainsi le taux de conversion du site vitrine.

```css
/* Positionnement et design des rubans fléchés latéraux */
.side-ribbon-container {
    position: fixed;
    right: 0;
    top: 30%;
    z-index: 9999;
    display: flex;
    flex-direction: column;
    gap: 10px;
}

.ribbon-item {
    display: flex;
    align-items: center;
    padding: 10px 20px;
    font-weight: bold;
    color: #FFFFFF !important;
    text-transform: uppercase;
    text-decoration: none;
    position: relative;
    transition: transform 0.2s ease;
}

.ribbon-item:hover {
    transform: translateX(-5px); /* Effet de survol */
}

/* Couleurs personnalisées selon la charte NET-CO SERVICES */
.ribbon-contact {
    background-color: #FCE6CC; /* Beige clair */
    color: #0B3C5D !important;
}

.ribbon-devis {
    background-color: #7FA99B; /* Vert d'eau emblématique */
}

.ribbon-jobs {
    background-color: #5B707A; /* Gris bleu ardoise */
}

/* Création de la pointe de flèche orientée vers la gauche */
.ribbon-item::before {
    content: '';
    position: absolute;
    left: -15px;
    top: 0;
    width: 0;
    height: 0;
    border-top: 20px solid transparent;
    border-bottom: 20px solid transparent;
}

.ribbon-contact::before { border-right: 15px solid #FCE6CC; }
.ribbon-devis::before { border-right: 15px solid #7FA99B; }
.ribbon-jobs::before { border-right: 15px solid #5B707A; }
