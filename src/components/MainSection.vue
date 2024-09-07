<template>
    <main>
        <section class="section" id="section1">
            <div class="image"></div>
            <div class="myclass">
                <h1>Who Am I?</h1>
            </div>
            <div>
                <p class="myclass1">
                    Hello, I am Utku Yeşil. Being a student with immense passion for computer programming and
                    technology, currently I am preparing for university entrance exams with a goal to get a degree in
                    Computer Engineering. Since childhood, interest in this area has been within me and motivated me to
                    develop my abilities further.
                </p>
                <p class="myclass2">
                    I have experience working with C#, Python, Unity, Unreal Engine, and JavaScript (Node.js, Vue) and I
                    share my projects on my <a href="https://github.com/utkysl" target="_blank"
                        rel="noopener noreferrer">GitHub page</a>, where you can get a glimpse of them.
                </p>
                <p class="myclass3">
                    I would love to build up more knowledge and experience in software development during my future
                    career. I am motivated for continuous learning and staying updated with the latest technologies so
                    that I can be part of successful projects in the future.
                </p>
            </div>
        </section>
        <section class="section" id="section2">
            <div>
                <h2 class="mylinkstext">My Links</h2>
                <div class="buttons">
                    <button @click="goTo('https://www.linkedin.com/in/utku-ye%C5%9Fil-095a79325/')">LinkedIn</button>
                    <button @click="goTo('https://github.com/utkysl')">Github</button>
                    <button @click="goTo('mailto:utkuyesil189@gmail.com')">Gmail</button>
                    <button @click="goTo('https://instagram.com/utkysll')">Instagram</button>
                    <button @click="goTo('https://x.com/UtkuYesil781')">X</button>
                    <button @click="goTo('https://www.youtube.com/@Bilgisayarmuhendisi_26')">YouTube</button>
                </div>
            </div>
        </section>
        <section class="section" id="section3">
            <repos></repos>
        </section>
    </main>
</template>

<script>
export default {
    name: 'MainSection',
    methods: {
        goTo(url) {
            window.open(url, '_blank');
        }
    }
}
</script>

<style scoped>
.section {
    padding: 20px;
    box-sizing: border-box;
    display: flex;
    flex-direction: column;
    align-items: center;
}

#section1 {
    background-color: #252425;
    color: #ffffff;
    margin-bottom: 20px;
}

#section2 {
    background-color: #252425;
    color: #ffffff;
}

p {
    font-size: 15px;
}

@media (max-width: 768px) {
    .section {
        padding: 10px;
        margin-bottom: 10px;
    }

    .myclass,
    .myclass1,
    .myclass2,
    .myclass3 {
        font-size: 14px;
    }

    .image {
        width: 100px;
        height: 100px;
    }
}

.image {
    width: 140px;
    height: 140px;
    border-radius: 50%;
    background-image: url('./resim.png');
    background-position: center center;
    background-size: cover;
    display: inline-block;
    vertical-align: middle;
    max-width: 100%;
    max-height: 100%;
}

.myclass {
    text-align: left;
    text-decoration: underline;
    color: rgb(221, 159, 159);
    padding-top: 2%;
}

.myclass1 {
    text-align: left;
    color: white;
}

.myclass2 {
    text-align: left;
    color: white;
    padding-top: 1%;
}

.myclass3 {
    text-align: left;
    color: white;
    padding-top: 1%;
}

.mylinkstext {
    font-size: 30px;
    text-align: center;
    color: rgb(116, 255, 139);
    text-decoration: underline;
}

.buttons {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    justify-content: center;
    margin: 20px 0;
}

.buttons button {
    background-color: #4CAF50;
    border: none;
    color: white;
    padding: 15px 32px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 16px;
    margin: 4px 2px;
    cursor: pointer;
    border-radius: 8px;
    transition: background-color 0.3s, transform 0.2s;
}

.buttons button:hover {
    background-color: #45a049;
    transform: scale(1.05);
}

.buttons button:active {
    background-color: #397d3b;
    transform: scale(0.98);
}

.buttons button:nth-child(1) {
    background-color: #0077b5;
}

.buttons button:nth-child(2) {
    background-color: #333;
}

.buttons button:nth-child(3) {
    background-color: #d14836;
}

.buttons button:nth-child(4) {
    background-color: #e4405f;
}

.buttons button:nth-child(5) {
    background-color: #1da1f2;
}

.buttons button:nth-child(6) {
    background-color: #ff0000;
}
</style>
