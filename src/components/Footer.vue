<script setup>

</script>

<template>
    <div class="section-footer p-5 d-flex align-items-center justify-content-center col-lg-12">
        <div class="section-logo col-lg-3 mt-3">
            <div class="d-flex align-items-center">
                <div class="logo me-3"></div>
                <p class="text-white fs-5 fw-light mt-3">Planty</p>
            </div>
            <div class="info mt-2">
                Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore et
                dolore magna aliqua. Ut enim ad minim veniam
            </div>
            <div class="d-flex mt-1">
                <div class="icon-div d-flex justify-content-center align-items-center me-2 p-1">
                    <img class="icon" src="/assets/images/icons/fb.png" alt="fb">
                </div>
                <div class="icon-div d-flex justify-content-center align-items-center me-2 p-1">
                    <img class="icon" src="/assets/images/icons/linkedin.png" alt="linkedin">
                </div>
                <div class="icon-div d-flex justify-content-center align-items-center me-2 p-1">
                    <img class="icon" src="/assets/images/icons/instagram.png" alt="instagram">
                </div>
                <div class="icon-div d-flex justify-content-center align-items-center me-2 p-1">
                    <img class="icon" src="/assets/images/icons/pinterest.png" alt="pinterest">
                </div>
                <div class="icon-div d-flex justify-content-center align-items-center me-2 p-1">
                    <img class="icon" src="/assets/images/icons/twitter.png" alt="twitter">
                </div>
            </div>
        </div>
        <div class="section-links col-lg-2 mt-3">
            <div class="ms-4">
                <h5 class="text-white">Quick Links</h5>
                <div class="link-underline"></div>
            </div>
            <ul class="mt-4 link-list">
                <li>
                    <a href="">About Us</a>
                </li>
                <li>
                    <a href="">Blogs & Article</a></li>
                <li>
                    <a href="">Terms And Condition</a>
                </li>
                <li>
                    <a href=""> Privacy Policy</a>
                </li>
                <li>
                    <a href="">Contact Us</a>
                </li>
            </ul>
        </div>
        <div class="section-news-letter col-lg-3 mt-3">
            <div>
                <h5 class="text-white">News Letter</h5>
                <div class="link-underline"></div>
            </div>
            <input type="text" class="form-control mt-4" placeholder="Enter email address">
            <button class="btn mt-3 btn-subscribe" type="button">Subscribe</button>
            <p class="span-text mt-2">We never span you!</p>
        </div>
        <div class="contact col-lg-2 mt-3">
            <div>
                <h5 class="text-white">Contact</h5>
                <div class="link-underline"></div>
            </div>
            <ul class="list-unstyled contact-list">
                <li class="d-flex mt-3">
                    <img class="me-2" src="/assets/images/icons/location.png" alt="location">
                    <a href="" class="text-white text-decoration-none">121 King St, Melbourne den 3000, Australia</a>
                </li>
                <li class="d-flex mt-3">
                    <img class="me-2" src="/assets/images/icons/email.png" alt="email">
                    <a href="" class="text-white text-decoration-none">Info@example.com</a>
                </li>
                <li class="d-flex mt-3">
                    <img class="me-2" src="/assets/images/icons/phone.png" alt="phone">
                    <a href="" class="text-white text-decoration-none">+91 999999999</a>
                </li>
            </ul>
        </div>
    </div>
</template>

<style scoped>
.section-footer {
    flex-wrap: wrap;
    width: 100%;
    min-height: 356px;
    background-color: var(--main-color);
    margin-top: 5%;
}

.logo {
    width: 50px;
    height: 50px;
    background-image: url("/assets/images/logo-white.png");
    background-size: cover;
    background-repeat: no-repeat;
}

.info {
    width: 240px;
    height: 100px;
    font-size: 12px;
    color: var(--white);
}

.icon-div {
    width: 35px;
    height: 35px;
    background-color: var(--light-gray);
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;
}

.icon {
    height: 60%;
}

.link-underline {
    width: 40px;
    height: 2px;
    border-radius: 2px;
    background-color: var(--yellow-green);
}

.link-list li a {
    color: var(--white);
    text-decoration: none;
    font-weight: 200;
    font-size: 13px;
}

.link-list li {
    color: var(--white);
}

.section-news-letter {
    margin-left: 4%;
}

input::placeholder {
    color: var(--gray);
    font-weight: 200;
}

.btn-subscribe {
    background-color: var(--yellow-green);
    color: var(--main-color);
    font-weight: 300;
}

.span-text {
    color: var(--gray);
    font-weight: 300;
}

.contact {
    margin-left: 8%;
}

.contact-list li a {
    font-weight: 200;
    font-size: 13px;
}

.contact-list li img {
    height: 100%;
}
</style>