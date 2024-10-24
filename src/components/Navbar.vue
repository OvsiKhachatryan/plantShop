<script setup>
import {ref} from 'vue';

const showMenu = ref(false);

function toggleMenu() {
    showMenu.value = !showMenu.value;
}
</script>

<template>
    <div class="navbar">
        <div class="section-logo">
            <div class="logo-img"></div>
            <span class="logo-name">Planty</span>
        </div>
        <div class="section-menu d-flex" :class="{ 'show-menu': showMenu }">
            <div class="list">
                <ul class="nav">
                    <li class="nav-item">
                        <a class="nav-link" href="#">Home</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">About</a>
                    </li>
                    <li class="nav-item dropdown">
                        <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button"
                           data-bs-toggle="dropdown" aria-expanded="false">
                            All Category
                        </a>
                        <ul class="dropdown-menu" aria-labelledby="navbarDropdown">
                            <li><a class="dropdown-item" href="#">Category 1</a></li>
                            <li><a class="dropdown-item" href="#">Category 2</a></li>
                            <li><a class="dropdown-item" href="#">Category 3</a></li>
                            <li><a class="dropdown-item" href="#">Category 4</a></li>
                        </ul>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">Shop</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">Blog</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#">Contact Us</a>
                    </li>
                </ul>
            </div>
            <div class="auth-btn">
                <button class="btn btn-green ms-5 btn-login">Login</button>
                <button class="btn btn-green ms-2 btn-register">Register</button>
            </div>
        </div>

        <button
                @click="toggleMenu"
                class="navbar-toggler"
                type="button"
                aria-controls="navbarNav"
                aria-expanded="showMenu"
                aria-label="Toggle navigation"
        >
            <span class="navbar-toggler-icon"></span>
        </button>
    </div>
</template>

<style scoped>
.navbar {
    position: relative;
    display: flex;
    justify-content: space-between;
    align-items: center;
    width: 1279px;
    min-height: 70px;
    background-color: rgba(53, 136, 86, 0.2);
    margin: 30px 0 0 81px;
    padding: 10px 30px;
}

.section-logo {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.logo-img {
    width: 52px;
    height: 48px;
    background-image: url("/public/assets/images/logo.png");
    background-size: cover;
    margin-right: 15px;
}

.logo-name {
    color: var(--main-color);
    font-size: 25px;
}

ul li a {
    color: var(--main-color);
}

ul li a:hover {
    color: var(--main-color);
}

.btn-green {
    background-color: var(--main-color);
    color: var(--white);
    width: 100px;
    height: 35px;
}

.navbar-toggler {
    display: none;
}

.show-menu{
    z-index: 1000;
}
/* Extra Small Devices */
@media (max-width: 575px) {
    .navbar {
        width: 100%;
        margin: 0;
    }

    .navbar-toggler {
        display: block;
        padding: 0 6px;
    }

    .navbar-toggler-icon {
        width: 15px;
        height: 24px;
    }

    .section-menu {
        flex-direction: column;
        align-items: center;
        display: none !important;
        position: absolute;
        top: 100%;
        left: 28%;
        background-color: var(--main-color);
        height: 100vh;
    }

    ul li a {
        color: var(--white);
        font-size: 13px;
    }

    ul li a:hover {
        color: var(--yellow-green);
    }

    .nav {
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    .show-menu {
        display: block !important;
        right: 0;
    }

    .logo-img {
        width: 24px;
        height: 24px;
        margin-right: 10px;
    }

    .logo-name {
        font-size: 15px;
    }

    .btn-register {
        margin: 0.5rem 3rem !important
    }

    .btn-register, .btn-login {
        background-color: var(--white);
        color: var(--main-color);
        font-size: 13px;
    }

    .auth-btn {
        display: flex;
        justify-content: center;
        align-items: center;
    }


}

/* Small Devices */
@media (min-width: 576px) and (max-width: 767px) {
    .navbar {
        margin: 0;
        width: 100%;
    }

    .navbar-toggler {
        display: block;
        padding: 0 6px;
    }

    .navbar-toggler-icon {
        width: 15px;
        height: 24px;
    }

    .section-menu {
        flex-direction: column;
        align-items: center;
        display: none !important;
        position: absolute;
        top: 100%;
        left: 28%;
        background-color: var(--main-color);
        height: 100vh;
    }

    ul li a {
        color: var(--white);
        font-size: 13px;
    }

    ul li a:hover {
        color: var(--yellow-green);
    }

    .nav {
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    .show-menu {
        display: block !important;
        right: 0;
    }

    .logo-img {
        width: 24px;
        height: 24px;
        margin-right: 10px;
    }

    .logo-name {
        font-size: 15px;
    }

    .btn-register {
        margin: 0.5rem 3rem !important
    }

    .btn-register, .btn-login {
        background-color: var(--white);
        color: var(--main-color);
        font-size: 13px;
    }

    .auth-btn {
        display: flex;
        justify-content: center;
        align-items: center;
    }

}

/* Medium Devices */
@media (min-width: 768px) and (max-width: 991px) {
    .navbar {
        width: 100%;
        margin: 0 auto;
        padding: 10px 10px;
    }
    .logo-img {
        width: 24px;
        height: 24px;
        margin-right: 10px;
    }

    .logo-name {
        font-size: 15px;
    }

    ul li a {
        font-size: 13px;
    }

    .btn-register, .btn-login{
        font-size: 12px;
    }

    .btn-register{
        width: 40%;
    }

    .btn-login{
        width: 30%;
    }

    .auth-btn{
        display: flex;
    }

}

/* Large Devices */
@media (min-width: 992px) and (max-width: 1199px) {
    .navbar {
        width: 100%;
        margin: 0 auto;
    }
}

/* Extra Large Devices */
@media (min-width: 1200px) {
    .navbar {
        width: 100%;
        margin: 0 auto;
    }
}
</style>
