<template>
    <aside :class="`${is_expanded && 'is-expanded'}`">
        <div class="logo">
            <img src="../assets/vue.svg" alt="Vue">
        </div>

        <div class="menu-toggle-wrap">
            <button class="menu-toggle" @click="ToggleMenu">
                <span class="material-icons">menu_open</span>
            </button>
        </div>

        <h3>Menu</h3>
        <div class="menu">
            <router-link class="button" to="/">
                <span class="material-icons">home</span>
                <span class="text">Home</span>
            </router-link>
            <router-link class="button" to="/about">
                <span class="material-icons">person</span>
                <span class="text">About</span>
            </router-link>
            <router-link class="button" to="/projects">
                <span class="material-icons">precision_manufacturing</span>
                <span class="text">Projects</span>
            </router-link>
            <router-link class="button" to="/hobbies">
                <span class="material-icons">hiking</span>
                <span class="text">Hobbies</span>
            </router-link>
            <router-link class="button" to="/contact">
                <span class="material-icons">email</span>
                <span class="text">Contact</span>
            </router-link>
        </div>
    </aside>
</template>

<script setup>
import { ref } from 'vue';

const is_expanded = ref(localStorage.getItem("is_expanded") === "true")

    const ToggleMenu = () => {
        is_expanded.value = !is_expanded.value
        localStorage.setItem("is_expanded", is_expanded.value)
    }
</script>

<style lang="scss" scoped>
aside{
    display: flex;
    flex-direction: column;
    width: calc(2rem + 32px);
    min-height: 100vh;
    overflow: hidden;
    padding: 1rem;

    background-color: var(--dark);
    color: var(--light);

    transition: 0.2s ease-in-out;

    .logo{
        margin-bottom: 1rem;

        img{
            width: 2rem;
        }
    }

    .menu-toggle-wrap{
        display: flex;
        justify-content: flex-end;
        margin-bottom: 1rem;

        position: relative;
        top:0;
        transition: 0.2s ease-in-out;

        .menu-toggle{
            transition: 0.2s ease-out;

            .material-icons{
                font-size: 2rem;
                color: var(--light);
            }

            &:hover{
                .material-icons{
                    color: var(--primary);
                    transform: translateX(0.25rem);
                    transition: 0.2s ease-in-out;
                }

            }
        }
    }

    h3, .button .text{
        opacity: 0;
        transition: 0.3s ease-in-out;
    }

    h3 {
        color: var(--grey);
        font-size: 3rem;
        text-transform: uppercase;
        margin-bottom: 0.5rem;
    }

    .menu{
        margin: 0 -1rem;

        .button{
            display: flex;
            align-items: center;
            text-decoration: none;

            padding: 0.5rem 1rem;
            transition: 0.1s ease-in-out;

            .material-icons{
                font-size: 2rem;
                color: var(--light);
                transition: 0.2s ease-in-out;
            }

            .text{
                color: var(--light);
                transition: 0.2s ease-in-out;
            }

            &:hover, &.router-link-exact-active{
                background-color: var(--dark-alt);
                .material-icons, .text{
                    color: var(--primary);
                }
            }
            &.router-link-exact-active{
                border-right: 5px solid var(--primary);
            }

        }
    }

    &.is-expanded{
        width: var(--sidebar-width);
        .menu-toggle-wrap{
            top: -3rem;
            .menu-toggle{
                transform: rotate(180deg);
            }
        }

        h3, .button, .text{
        opacity: 1;
        transition: 0.3s ease-in-out;
        }

        .button{
            .material-icons{
                margin-right: 1rem;
            }
        }
    }

    @media (max-width: 768px){
        position: fixed;
        z-index: 99;
    }
}
</style>