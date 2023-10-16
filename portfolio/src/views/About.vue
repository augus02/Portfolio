<template>
    <main class="about-page">
        <h1 class="pageTitle">
            About me
        </h1>
        <div class="textContainer">
            <p class="text"> 
                I am currently a Creative Technology M2 student at ESILV. 
                The major takes place at the DVIC, the innovation center of ESILV. 
                During this cursus, I have had the opportunity to conduct many projects combining electronics, programming, mechanics and fabrication.
                Furthermore, these projetcs have been made alone and in groups, which allowed be to strengthen my project management skills.
            </p>
            <p class="text"> 
                I am passionate about 3D printing and additive manufacturing oriented design.
                In this context, I developed my skills in Fusion360, SolidWorks and slicing software sucha as Prusa slicer and Creality slicer.
                This year, I am also working on the 3DExperience platform for a large-scale project that requires collaborative software.
                Moreover, while working on a crowdfunded project, I discovered the technologies used in industrial additive manufacturing to produce our object.
            </p>
            <p class="text"> 
                Curiosity and autonomy are my main strengths and I like developing new skills while finding real applications for them.
                This is why I spend some of my free time building small projects involving software, electronics and fabrication to build a larger knowledge database.
                At the DVIC, I've had the chance of discovering the research world by reading papers and using them as state of the art for my own projects. 
                It makes me value scientific rigor even more and pushes me to apply that mindset in my work.
            </p>
        </div>
    </main>
</template>

<style scoped>
    .about-page{
        flex-direction: row;
        text-align: center;
        align-items: center;
        justify-content: center;
        width: 100%;
    }

    .pageTitle{
        color: azure;
        font: larger;
        text-align: center;
        padding-top: 48px;
        padding-bottom: 48px;
    }

    .text{
        font-size: 22px;
        color: azure;
        text-align: left;
        margin: 12px;
    }
    .textContainer{
        width: 800px;
        margin-left: 25%;
        margin-right: 25%;
    }
</style>
