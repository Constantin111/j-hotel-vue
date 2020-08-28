<template>
    <div class="age-gate__block active">
        <div class="block-wrap wellcome-block">
            <div class="wellcome-block__title">
                <div class="d_flex align_items justify_center wellcome-block__title-text">
                    Добро пожаловать
                </div>
                <div class="d_flex align_items justify_center wellcome-block__title-logo">
                    <img src="img/logo-1.png" alt="">
                </div>
                <div class="d_flex align_items justify_center wellcome-block__title-description">
                    Введите дату вашего рождения
                </div>
            </div>
            <div class="wellcome-block__date">

                <form action="" class="date-old">
                    <div class="d_flex justify_center align_items wellcome-block__date-items">
                        <div class="wellcome-block__date-item">
                            <div class="d_flex justify_center align_items wellcome-block__date-item__input">
                                <input type="number" maxlength="2" id="oldDay" name="oldDay" placeholder="ДД"
                                       autofocus autocomplete="off">
                            </div>
                            <div class="wellcome-block__date-item__text">
                                День
                            </div>
                        </div>
                        <div class="wellcome-block__date-item">
                            <div class="d_flex justify_center align_items wellcome-block__date-item__input">
                                <input tabindex="1" type="number" maxlength="2" id="oldMonth" name="oldMonth"
                                       placeholder="ММ" autocomplete="off">
                            </div>
                            <div class="wellcome-block__date-item__text">
                                Месяц
                            </div>
                        </div>
                        <div class="wellcome-block__date-item">
                            <div class="d_flex justify_center align_items wellcome-block__date-item__input">
                                <input tabindex="2" type="number" maxlength="4" min="1910" max="2020" step="1"
                                       id="oldYear"
                                       name="oldYear" placeholder="ГГГГ" autocomplete="off">
                            </div>
                            <div class="wellcome-block__date-item__text">
                                Год
                            </div>
                        </div>
                    </div>
                </form>
                <div class="wellcome-block__date-acces">
                    <div class="d_flex justify_center align_items wellcome-block__date-acces__block">
                        <div class="d_flex justify_center align_items wellcome-block__date-acces__btn"
                             @click="ageComplit">
                            Подтвердить
                        </div>
                    </div>
                </div>

            </div>
            <div class="wellcome-block__attention">
                <div class="wellcome-block__attention-text">
                    Нажимая кнопку «Подтвердить»,<br>
                    вы соглашаетесь перейти на сайт, содержащий<br>
                    информацию об алкогольной продукции
                </div>
            </div>
        </div>

    </div>
</template>

<script>

    export default {
        name: "age-gate",
        data() {
            return {
                fieldValid: '',
            }
        },
        props: ['ageComplite'],
        methods: {
            ageComplit() {
                this.$emit('ageGateComplit', event)
            }
        }
    }

</script>

<style scoped>

</style>