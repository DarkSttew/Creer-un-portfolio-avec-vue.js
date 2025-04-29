<script setup>
    import { computed } from 'vue'

    const copyright = computed(() =>{
        const currentYear = new Date().getFullYear()
        return `© Copyright ${currentYear} | Mickaël Lesseline`
    });
</script>

<template>
    <footer class="footer">
        <div class="footer__content">
            <div class="footer__adress">
                <h3>Mes contacts</h3>
                <address>
                    <a href="mailto:evaluation@gmail.com">evaluation@gmail.com</a>
                    <a href="tel:+0640059650">06.06.06.06.06</a>
                    <p>Lille 59000</p>
                </address>
            </div>
            <div class="footer__borderRight"></div>
            <div class="footer__social">
                <h3>Me retrouver</h3>
                <a class="footer__social__icon" href="https://github.com/DarkSttew" target="_blank" rel="noopener noreferrer">
                    <img src="../assets/images/gitHub.png" alt="Logo GitHub">
                </a>
                <a class="footer__social__icon" href="https://www.linkedin.com/in/mickael-lesseline-99591b215/" target="_blank" rel="noopener noreferrer">
                    <img src="../assets/images/linkedin.ico" alt="Logo LinkedIn">
                </a>
                <a class="footer__social__icon" href="https://www.instagram.com/mickael.lsl/" target="_blank" rel="noopener noreferrer">
                    <img src="../assets/images/instagram.png" alt="Logo Instagram">
                </a>
            </div>
        </div>
        <div class="footer__copyright">
            <p>Dernières modifications le<time datetime="2025-02-26">26 février 2025</time></p>
            <p class="copyright">{{ copyright }}</p>
        </div>
    </footer>
</template>

<style scoped>
    .footer__content {
        display: flex;
        justify-content: space-evenly;
    }

    footer * {
        background-color: #277C9F;
        color: white;
        padding: 10px;
    }
    
    .footer__borderRight {
        border-right: 1px solid #EFFAFD;
    }

    address {
        display: flex;
        flex-direction: column;
    }

    .footer__copyright {
        text-align: center;
    }

    time {
        font-style: italic;
    }

    .copyright {
        font-style: italic;
        font-size: 0.8em;
    }

    .footer__social__icon:hover {
        opacity: 50%;
    }
</style>