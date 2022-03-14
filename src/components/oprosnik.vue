<template>
    <div class="ml-10 mt-2">
        <div>
            <div>
                <h1>Как Олжас ведет урок?</h1>
                <div class="flex items-center mr-2">
                    <input type="radio" name="first" class="mx-2" @click="first = 1, setFirst()">
                    <p>превосходно</p>
                    <!-- true -->
                </div>
                <div class="flex items-center mr-2">
                    <input type="radio" name="first" class="mx-2" @click="first = 2, setFirst()">
                    <p>шикарно</p>
                </div>
                <div class="flex items-center mr-2">
                    <input type="radio" name="first" class="mx-2" @click="first = 3, setFirst()">
                    <p>угарно</p>
                </div>
                <div class="flex items-center mr-2">
                    <input type="radio" name="first" class="mx-2" @click="first = 4, setFirst()">
                    <p>я опоздал и не знаю</p>
                </div>
            </div>
            <div>
                <h1>Почему?</h1>
                <div class="flex items-center mr-2">
                    <input type="radio" name="second" class="mx-2" @click="second = 1, setSecond()">
                    <p>что почему?</p>
                </div>
                <div class="flex items-center mr-2">
                    <input type="radio" name="second" class="mx-2" @click="second = 2, setSecond()">
                    <p>покачену</p>
                </div>
                <div class="flex items-center mr-2">
                    <input type="radio" name="second" class="mx-2" @click="second = 3, setSecond()">
                    <p>потому что Тамила принесла швабру</p>
                    <!-- true -->
                </div>
                <div class="flex items-center mr-2">
                    <input type="radio" name="second" class="mx-2" @click="second = 4, setSecond()">
                    <p>вы кто? как я сюда попал?</p>
                </div>
            </div>
            <div>
                <h1>Зачем идти на бетмена?</h1>
                <div class="flex items-center mr-2">
                    <input type="radio" name="third" class="mx-2" @click="third = 1, setThird()">
                    <p>чтобы Олжас перестал агитировать</p>
                </div>
                <div class="flex items-center mr-2">
                    <input type="radio" name="third" class="mx-2" @click="third = 2, setThird()">
                    <p>по приколу</p>
                </div>
                <div class="flex items-center mr-2">
                    <input type="radio" name="third" class="mx-2" @click="third = 3, setThird()">
                    <p>чтобы потом всем спойлерить</p>
                </div>
                <div class="flex items-center mr-2">
                    <input type="radio" name="third" class="mx-2" @click="third = 4, setThird()">
                    <p>чтобы поспать</p>
                    <!-- true -->
                </div>
            </div>
                <div>
                    <h1>Как зовут мою кошку?</h1>
                    <div class="flex items-center mr-2">
                        <input type="radio" name="fourth" class="mx-2" @click="fourth = 1, setFourth()">
                        <p>Тося</p>
                    </div>
                    <div class="flex items-center mr-2">
                        <input type="radio" name="fourth" class="mx-2" @click="fourth = 2, setFourth()">
                        <p>Засранка</p>
                        <!-- true -->
                    </div>
                    <div class="flex items-center mr-2">
                        <input type="radio" name="fourth" class="mx-2" @click="fourth = 3, setFourth()">
                        <p>Мысық-гүл</p>
                    </div>
                    <div class="flex items-center mr-2">
                        <input type="radio" name="fourth" class="mx-2" @click="fourth = 4, setFourth()">
                        <p>Саб-зиро</p>
                    </div>
                </div>
            <p v-if="first != 0 && second != 0 && third != 0 && fourth != 0">Правильных ответа: {{ result }} из 4.</p>
        </div>
    </div>
</template>

<script>
export default {
    name: "test",
    data() {
        return {
            first: 0,
            second: 0,
            third: 0,
            fourth: 0,
            result: 0,
            firstBool: false,
            secondBool: false,
            thirdBool: false,
            fourthBool: false
        };
    },
    methods: {
        setFirst() {
            if (this.first === 1 && this.firstBool === false) {
            this.result = this.result + 1;
            this.firstBool = true;
            } else if (this.first === 1 && this.firstBool === true) {
                this.result = this.result;
            } else if (this.first != 1 && this.firstBool === true) {
                this.result = this.result - 1;
                this.firstBool = false;
            }
        },
        setSecond() {
            if (this.second === 3 && this.secondBool === false) {
            this.result = this.result + 1;
            this.secondBool = true;
            } else if (this.second === 3 && this.secondBool === true) {
                this.result = this.result;
            } else if (this.second != 1 && this.secondBool === true) {
                this.result = this.result - 1;
                this.secondBool = false;
            }
        },
        setThird() {
            if (this.third === 4 && this.thirdBool === false) {
            this.result = this.result + 1;
            this.thirdBool = true;
            } else if (this.third === 2 && this.thirdBool === true) {
                this.result = this.result;
            } else if (this.third != 1 && this.thirdBool === true) {
                this.result = this.result - 1;
                this.thirdBool = false;
            }
        },
        setFourth() {
            if (this.fourth === 2 && this.fourthBool === false) {
            this.result = this.result + 1;
            this.fourthBool = true;
            } else if (this.fourth === 2 && this.fourthBool === true) {
                this.result = this.result;
            } else if (this.fourth != 1 && this.fourthBool === true) {
                this.result = this.result - 1;
                this.fourthBool = false;
            }
        },
    }
};
</script>
