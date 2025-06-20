document.addEventListener('DOMContentLoaded', function() {
    // Elementos del DOM
    const profileCard = document.getElementById('profileCard');
    const profileImage = document.getElementById('profileImage');
    const profileName = document.getElementById('profileName');
    const toggleInfoBtn = document.getElementById('toggleInfo');
    const changeThemeBtn = document.getElementById('changeTheme');
    const additionalInfo = document.getElementById('additionalInfo');
    const skills = document.querySelectorAll('.skill');
    
    // Contador de clics
    let clickCount = 0;
    
    // Mostrar/ocultar información adicional
    toggleInfoBtn.addEventListener('click', function() {
        additionalInfo.classList.toggle('visible');
        toggleInfoBtn.textContent = additionalInfo.classList.contains('visible') ? 
            'Mostrar menos' : 'Mostrar más';
        
        // Incrementar contador y mostrar en consola (podría mostrarse en UI)
        clickCount++;
        console.log(`Botón clickeado ${clickCount} veces`);
    });
    
    // Cambiar tema (claro/oscuro)
    changeThemeBtn.addEventListener('click', function() {
        profileCard.classList.toggle('dark');
        changeThemeBtn.textContent = profileCard.classList.contains('dark') ? 
            'Tema claro' : 'Tema oscuro';
    });
    
    // Efecto hover en la imagen
    profileImage.addEventListener('mouseenter', function() {
        this.style.transform = 'scale(1.05) rotate(5deg)';
    });
    
    profileImage.addEventListener('mouseleave', function() {
        this.style.transform = 'scale(1) rotate(0deg)';
    });
    
    // Mostrar habilidad destacada al pasar el ratón
    skills.forEach(skill => {
        skill.addEventListener('mouseenter', function() {
            const skillName = this.getAttribute('data-skill');
            this.textContent = `★ ${skillName} ★`;
            this.style.fontWeight = 'bold';
        });
        
        skill.addEventListener('mouseleave', function() {
            const skillName = this.getAttribute('data-skill');
            this.textContent = skillName;
            this.style.fontWeight = 'normal';
        });
    });
    
    // Cambiar nombre al hacer clic en la tarjeta (interacción adicional)
    profileCard.addEventListener('click', function(e) {
        // Evitar que se active cuando se hace clic en elementos hijos
        if (e.target === this) {
            const names = ['María García', 'María G.', 'María', 'MG'];
            const currentIndex = names.indexOf(profileName.textContent);
            const nextIndex = (currentIndex + 1) % names.length;
            profileName.textContent = names[nextIndex];
        }
    });
});
