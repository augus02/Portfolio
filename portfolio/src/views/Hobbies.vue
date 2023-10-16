<template>
    <main class="hobbies-page">
        <h1 class="pageTitle">
            Hobbies
        </h1>
        <h2 class="hobbyTitle">Learning CAD</h2>
        <div class="hobby">
            <div class="element">
                <img class="hobby-image" src="../assets/Images/pedalier.jpg">
                <p class="desc"> SolidWorks </p>
            </div>
            <div class="element">
                <img class="hobby-image" src="../assets/Images/Agricycle_v2_2.png">
                <p class="desc"> Fusion360 </p>
            </div>
            <div class="element">
                <img class="hobby-image" src="../assets/Images/blender_doughnut.png">
                <p class="desc"> Blender </p>
            </div>
        </div>
        <h2 class="hobbyTitle">Computational Fluid Dynamics</h2>
        <div class="hobby">
            <div class="element">
                <img class="hobby-image" src="../assets/Images/Centrifugal_pump_1.jpg">
                <p class="desc"> Traces of velocity magnitude </p>
            </div>
            <div class="element">
                <img class="hobby-image" src="../assets/Images/centrifugal_pump_plan.jpg">
                <p class="desc"> Plans of velocity magnitude </p>
            </div>
        </div>
        <h2 class="hobbyTitle">Additive manufacturing</h2>
        <div class="hobby">
            <div class="element">
                <img class="hobby-image" src="../assets/Images/Impeller.jpg">
                <p class="desc"> FDM 3D printed impeller </p>
            </div>
            <div class="element">
                <img class="hobby-image" src="../assets/Images/Taystick.jpg">
                <p class="desc"> SLS 3D printed Taystick </p>
            </div>
        </div>
    </main>
</template>

<style scoped>
    .hobbies-page{
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

    .hobby-image{
        width: 98%;
        height: 80%;
        margin-left: 12px;
        margin-right: 12px;
        margin-bottom: 24px;
    }

    .hobby{
        display: flex;
        margin-bottom: 96px;
    }

    .hobbyTitle{
        color: azure;
        margin-bottom: 24px;
    }

    .desc{
        color: azure;
    }

    .element{
        flex-direction: row;
        text-align: center;
        align-items: center;
        justify-content: center;
        width: 100%;
    }
</style>