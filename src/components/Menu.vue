<template>
    <nav>
        <div class="d-flex justify-content-between align-items-center container">
            <a href="#">
                <img src="../assets/images/dark-logo.png" alt="Logo MaxCoach">
            </a>
            <ul class="d-flex align-items-center">
                <li>
                    <a href="#" class="menu_link">Link <i class="fas fa-chevron-down"></i></a>
                </li>
            </ul>
            <ul class="d-flex align-items-center menu_socials">
                <li>
                    <a href="#" class="menu_social">Social</a>
                </li>
            </ul>
        </div>
    </nav>
</template>

<script>
export default {
    name: 'Menu'
}
</script>

<style lang="scss" scoped>
    @import '../assets/style/variables.scss';
    @import '../assets/style/mixins.scss';

    nav {
        height: 90px;

        div {
            height: 100%;

            a {
                img {
                    width: 150px;
                }
            }

            ul {
                li {
                    margin: 0 20px;

                    a {
                        i {
                            margin-left: 3px;
                            vertical-align: middle;
                            font-size: 10px;
                        }
                    }

                    .menu_link {
                        color: $link-color;
                    }

                    .menu_social {
                        color: $social-color;
                    }
                }
            }
        }
    }

</style>