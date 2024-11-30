<template>
    <div class="production">

        <div class="production-actions">
            <div class="filters">
                <div class="btn-filter active">
                    Текущий месяц
                </div>
                <div class="btn-filter">
                    Квартал
                </div>
                <div class="btn-filter">
                    Год
                </div>
                <div class="btn-filter">
                    Все время
                </div>
                <div class="btn-filter">
                    Выбор периода
                </div>
            </div>
            <div class="btn-filter active">
                Добавить запись
            </div>
        </div>

        <div class="production-tabs">
            <div class="tab-item active">Сводка</div>
            <div class="tab-item">Статистика</div>
        </div>
        <div class="search">
            <div class="input-search">
                <img src="@/assets/Union.svg" alt="searchlogo">
                <!-- <span class="input-group-text" id="basic-addon1">@</span> -->
                <input placeholder="Введите поисковый запрос" type="text">
            </div>
            <div class="btn-filter active">Искать</div>
        </div>

    </div>
</template>

<script>
export default {
    data() {
        return {
            count: 0
        }
    },
    methods: {
        increment() {
            this.count++
        }
    },
    computed: {
        currentRouteName() {
            return this.$route.name;
        }
    },
    mounted() {
        console.log(`The initial count is ${this.count}.`)
    }
}
</script>

<style>
.production {
    /* background: blue; */
}

.production-actions {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 25px;
}

.filters {
    display: flex;
    flex-direction: row;
}

.btn-filter {
    border: 1px solid #1308171A;
    border-radius: 10px;
    padding: 10px 15px;
    color: #130817B2;
    font-size: 15px;
    margin-right: 10px;
}

.btn-filter.active {
    background: #6E3794;
    color: #fff;
}

.production-tabs {
    background: #fff;
    border-radius: 15px;
    padding: 10px 25px;
    display: flex;
    margin-bottom: 25px;
}

.tab-item {
    color: #13081766;
    padding: 20px 0;
    font-size: 14px;
    font-weight: 400;
    margin-right: 20px;
}

.tab-item.active {
    border-bottom: 3px solid #130817B2;
    color: #130817E5;
    font-weight: 600;
}

.search {
    display: flex;
    flex-direction: row;
    align-items: center;
}

.input-search {
    display: flex;
    flex-direction: row;
    align-items: center;
    border: 1px solid #1308171A;
    border-radius: 15px;
    padding: 10px;
    width: 40%;
    margin-right: 30px;
    background-color: #fff
}

.input-search input {
    border: none;
    outline: none;
    margin-left: 10px;
    background: #fff;
}
</style>
