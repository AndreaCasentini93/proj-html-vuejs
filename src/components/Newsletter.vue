<template>
    <section>
        <div class="container d-flex justify-content-around align-items-center flex-wrap">
            <div class="d-flex align-items-center text-end">
                <h2>Newsletter to get<br>in touch</h2>
            </div>
            <form>
                <span v-if="emailError" class="error">ERROR! Insert your email please.</span>
                <div>
                    <input type="email" v-model.trim="enteredEmail" @keyup.enter="enterEmail" placeholder="Your e-mail">
                    <button type="submit" @click.prevent="enterEmail">&#x2192;</button>
                </div>
            </form>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Newsletter',
    data: function() {
        return {
            enteredEmail: '',
            emailError: false
        }
    },
    methods: {
        enterEmail: function() {
            if (this.enteredEmail.length > 0 && this.enteredEmail.includes('@')) {
                this.emailError = false;
                this.$emit('userEmail', this.enteredEmail);
                this.enteredEmail = '';
            } else if (this.enteredEmail.length == 0 && !this.emailError) {
                this.emailError = false;
            } else {
                this.emailError = true;
                this.enteredEmail = '';
            }
        }
    }
}
</script>

<style lang="scss" scoped>
    @import '../assets/style/variables.scss';
    @import '../assets/style/mixins.scss';

    section {
        padding: 50px 0;
        color: #FFFFFF;
        background-color: $bg-newsletter;

        h2 {
            margin: unset;
            font-family: unset;
        }

        form {
            padding: 1px 0;
            margin-top: 10px;
            margin-left: 30px;
            border-bottom: 1px solid #FFFFFF;

            .error {
                font-size: 17px;
                color: $ashtag-color;
            }

            input {
                width: 600px;
                padding: 5px 3px;
                border: unset;
                color: #FFFFFF;
                background-color: unset;
                font-size: 19px;

                &::placeholder {
                    font-size: 19px;
                    color: #FFFFFF;
                }
            }

        button {
                border: unset;
                font-size: 25px;
                background-color: unset;
                color: #FFFFFF;
                @include transition-type-1(transform);

                &:hover {
                    transform: scale(1.3);
                }
            }
        }
    }

    @media screen and (max-width: 991px) {

        input {
            width: 200px !important;
        }

    }
    @media screen and (max-width: 404px) {

        h2 {
            font-size: 18px !important;
        }

        .error {
                font-size: 12px;
            }

        input {
            font-size: 14px !important;

            &::placeholder {
                font-size: 14px !important;
            }
        }

        button {
            font-size: 14px !important;
        }

    }
</style>