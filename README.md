# toutpres-landingtoutpres-landing/
├── index.html
├── style.css
├── script.js
├── assets/
│   ├── logo.svg
│   ├── app-mockup.png
│   ├── app-store-badge.svg
│   ├── google-play-badge.svg
```
Commençons par le fichier `index.html` :
```html
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Toutprès - L'app qui rend visible l'invisible près de chez vous</title>
    <link rel="stylesheet" href="style.css">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@600;700&family=Nunito:wght@400;700&display=swap" rel="stylesheet">
    <link rel="icon" href="assets/favicon.ico" type="image/x-icon">
</head>
<body>
    <header>
        <div class="container">
            <img src="assets/logo.svg" alt="Logo Toutprès" class="logo">
            <nav>
                <ul>
                    <li><a href="#features">Fonctionnalités</a></li>
                    <li><a href="#download">Télécharger</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>
    <section class="hero">
        <div class="container">
            <div class="hero-text">
                <h1>Votre ville devient solidaire</h1>
                <p>Trouvez en temps réel les aides, jobs et événements gratuits autour de vous.</p>
                <div class="cta-buttons">
                    <a href="#" class="btn primary">Devenez bêta-testeur</a>
                    <a href="#download" class="btn secondary">Voir la démo</a>
                </div>
            </div>
            <div class="hero-image">
                <img src="assets/app-mockup.png" alt="Mockup de l'application Toutprès">
            </div>
        </div>
    </section>
    <section id="features" class="features">
        <div class="container">
            <h2>Comment ça marche ?</h2>
            <div class="features-grid">
                <div class="feature-card">
                    <div class="icon food">🍎</div>
                    <h3>J'ai faim</h3>
                    <p>Repas gratuits, invendus, épiceries solidaires à proximité.</p>
                </div>
                <div class="feature-card">
                    <div class="icon job">💼</div>
                    <h3>Je cherche un job</h3>
                    <p>Offres d'emploi urgentes ou missions ponctuelles près de chez vous.</p>
                </div>
                <div class="feature-card">
                    <div class="icon learn">📚</div>
                    <h3>Je veux apprendre</h3>
                    <p>Ateliers gratuits, cours ouverts, partage de compétences.</p>
                </div>
            </div>
        </div>
    </section>
    <section id="download" class="download">
        <div class="container">
            <h2>Téléchargez l'application</h2>
            <p>Disponible bientôt sur iOS et Android</p>
            <div class="badges">
                <a href="#"><img src="assets/app-store-badge.svg" alt="Télécharger sur l'App Store"></a>
                <a href="#"><img src="assets/google-play-badge.svg" alt="Disponible sur Google Play"></a>
            </div>
            <div class="counter">
                <span id="user-count">1,243</span>
                <span>voisins déjà engagés !</span>
            </div>
        </div>
    </section>
    <footer id="contact">
        <div class="container">
            <div class="footer-content">
                <div class="footer-brand">
                    <img src="assets/logo.svg" alt="Logo Toutprès" class="logo">
                    <p>L'entraide géolocalisée</p>
                </div>
                <div class="footer-links">
                    <h4>Liens</h4>
                    <ul>
                        <li><a href="#">Mentions légales</a></li>
                        <li><a href="#">Politique de confidentialité</a></li>
                        <li><a href="#">CGU</a></li>
                    </ul>
                </div>
                <div class="footer-contact">
                    <h4>Contact</h4>
                    <p>contact@toutpres.app</p>
                    <div class="social-icons">
                        <a href="#"><img src="assets/facebook-icon.svg" alt="Facebook"></a>
                        <a href="#"><img src="assets/instagram-icon.svg" alt="Instagram"></a>
                        <a href="#"><img src="assets/twitter-icon.svg" alt="Twitter"></a>
                    </div>
                </div>
            </div>
            <div class="footer-bottom">
                <p>&copy; 2025 Toutprès. Tous droits réservés.</p>
            </div>
        </div>
    </footer>
    <script src="script.js"></script>
</body>
</html>
```
Maintenant, le fichier `style.css` :
```css
/* RESET & BASE STYLES */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
:root {
    --primary: #FF6B6B;
    --secondary: #4ECDC4;
    --dark: #2E2E2E;
    --light: #F8F9FA;
    --gray: #6C757D;
    --success: #A5D6A7;
    --warning: #FFD166;
}
body {
    font-family: 'Nunito', sans-serif;
    color: var(--dark);
    background-color: var(--light);
    line-height: 1.6;
}
h1, h2, h3, h4 {
    font-family: 'Poppins', sans-serif;
    font-weight: 700;
}
.container {
    width: 90%;
    max-width: 1200px;
    margin: 0 auto;
}
.btn {
    display: inline-block;
    padding: 12px 24px;
    border-radius: 50px;
    text-decoration: none;
    font-weight: bold;
    transition: all 0.3s ease;
    text-align: center;
}
.btn.primary {
    background-color: var(--primary);
    color: white;
}
.btn.primary:hover {
    background-color: #e55a5a;
    transform: translateY(-3px);
}
.btn.secondary {
    background-color: transparent;
    color: var(--primary);
    border: 2px solid var(--primary);
}
.btn.secondary:hover {
    background-color: var(--primary);
    color: white;
}
/* HEADER STYLES */
header {
    padding: 20px 0;
    position: fixed;
    width: 100%;
    top: 0;
    z-index: 1000;
    background-color: rgba(255, 255, 255, 0.95);
    box-shadow: 0 2px 10px rgba(0,0,0,0.1);
}
header .container {
    display: flex;
    justify-content: space-between;
    align-items: center;
}
.logo {
    height: 40px;
}
nav ul {
    display: flex;
    list-style: none;
}
nav ul li {
    margin-left: 30px;
}
nav ul li a {
    text-decoration: none;
    color: var(--dark);
    font-weight: 600;
    transition: color 0.3s;
}
nav ul li a:hover {
    color: var(--primary);
}
/* HERO SECTION */
.hero {
    padding: 150px 0 100px;
}
.hero .container {
    display: flex;
    align-items: center;
    gap: 50px;
}
.hero-text {
    flex: 1;
}
.hero-text h1 {
    font-size: 3rem;
    margin-bottom: 20px;
    line-height: 1.2;
}
.hero-text p {
    font-size: 1.2rem;
    margin-bottom: 30px;
    color: var(--gray);
}
.cta-buttons {
    display: flex;
    gap: 20px;
}
.hero-image {
    flex: 1;
    text-align: center;
}
.hero-image img {
    max-width: 100%;
    border-radius: 20px;
    box-shadow: 0 10px 30px rgba(0,0,0,0.15);
}
/* FEATURES SECTION */
.features {
    padding: 100px 0;
    background-color: white;
}
.features h2 {
    text-align: center;
    margin-bottom: 60px;
    font-size: 2.5rem;
}
.features-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 30px;
}
.feature-card {
    text-align: center;
    padding: 40px 30px;
    border-radius: 15px;
    background-color: var(--light);
    box-shadow: 0 5px 15px rgba(0,0,0,0.05);
    transition: transform 0.3s ease;
}
.feature-card:hover {
    transform: translateY(-10px);
}
.feature-card .icon {
    font-size: 3rem;
    margin-bottom: 20px;
    display: inline-block;
}
.feature-card h3 {
    margin-bottom: 15px;
    font-size: 1.5rem;
}
/* DOWNLOAD SECTION */
.download {
    padding: 100px 0;
    text-align: center;
    background: linear-gradient(135deg, #FF6B6B 0%, #4ECDC4 100%);
    color: white;
}
.download h2 {
    font-size: 2.5rem;
    margin-bottom: 20px;
}
.download p {
    font-size: 1.2rem;
    margin-bottom: 40px;
    opacity: 0.9;
}
.badges {
    display: flex;
    justify-content: center;
    gap: 20px;
    margin-bottom: 40px;
}
.badges img {
    height: 60px;
    transition: transform 0.3s;
}
.badges img:hover {
    transform: scale(1.05);
}
.counter {
    font-size: 2rem;
    font-weight: bold;
    display: flex;
    justify-content: center;
    align-items: baseline;
    gap: 10px;
}
.counter span:first-child {
    color: var(--warning);
}
/* FOOTER */
footer {
    background-color: var(--dark);
    color: white;
    padding: 60px 0 30px;
}
.footer-content {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 40px;
    margin-bottom: 40px;
}
.footer-brand img {
    height: 40px;
    margin-bottom: 20px;
}
.footer-brand p {
    opacity: 0.7;
}
.footer-links h4, .footer-contact h4 {
    margin-bottom: 20px;
    font-size: 1.2rem;
}
.footer-links ul {
    list-style: none;
}
.footer-links ul li {
    margin-bottom: 10px;
}
.footer-links ul li a {
    color: white;
    text-decoration: none;
    opacity: 0.7;
    transition: opacity 0.3s;
}
.footer-links ul li a:hover {
    opacity: 1;
}
.social-icons {
    display: flex;
    gap: 15px;
    margin-top: 15px;
}
.social-icons img {
    height: 24px;
    opacity: 0.7;
    transition: opacity 0.3s;
}
.social-icons img:hover {
    opacity: 1;
}
.footer-bottom {
    text-align: center;
    padding-top: 30px;
    border-top: 1px solid rgba(255,255,255,0.1);
    opacity: 0.7;
}
/* RESPONSIVE */
@media (max-width: 768px) {
    .hero .container {
        flex-direction: column;
    }
    
    .hero-text, .hero-image {
        width: 100%;
    }
    
    .cta-buttons {
        flex-direction: column;
    }
    
    nav ul {
        display: none;
    }
}
```
Et le fichier `script.js` :
```javascript
// Compteur animé
const counter = document.getElementById('user-count');
let count = 0;
const target = 1243;
function updateCounter() {
    if (count < target) {
        count += Math.ceil(target / 100);
        if (count > target) count = target;
        counter.innerText = count.toLocaleString();
        setTimeout(updateCounter, 20);
    }
}
// Démarrer le compteur lorsque la section est visible
const observer = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
        if (entry.isIntersecting) {
            updateCounter();
            observer.disconnect();
        }
    });
}, { threshold: 0.5 });
observer.observe(document.querySelector('.download'));
// Smooth scrolling
document.querySelectorAll('a[href^="#"]').forEach(anchor => {
    anchor.addEventListener('click', function(e) {
        e.preventDefault();
        const targetId = this.getAttribute('href');
        if (targetId === '#') return;
        
        const targetElement = document.querySelector(targetId);
        if (targetElement) {
            window.scrollTo({
                top: targetElement.offsetTop - 80,
                behavior: 'smooth'
            });
        }
    });
});
// Gestion du formulaire (exemple basique)
document.querySelector('.btn.primary').addEventListener('click', function(e) {
    e.preventDefault();
    alert('Merci ! Le formulaire bêta sera disponible très bientôt. En attendant, vous pouvez nous suivre sur les réseaux sociaux !');
});
```
