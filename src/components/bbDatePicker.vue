<template>
    <section class="datepicker-container">
        <div class="datepicker-wrapper">
            <h2 class="datepicker-title">Plan je bezoek</h2>
            <h3 class="datepicker-subtitle">Wanneer wil je langskomen?</h3>
            <hr />
            <table aria-labelledby="defaulPicker-month" aria-multiselectable="true" class="datepicker-table" role="grid">
                <caption class="datepicker-caption--title">{{ currentDate }} </caption>
                <thead>
                    <tr>
                        <th scope="col">
                            <abbr class="datepicker-day--title" title="Zondag">Zo</abbr>
                        </th>
                        <th scope="col">
                            <abbr class="datepicker-day--title" title="Maandag">Ma</abbr>
                        </th>
                        <th scope="col">
                            <abbr class="datepicker-day--title" title="Dinsdag">Di</abbr>
                        </th>
                        <th scope="col">
                            <abbr class="datepicker-day--title" title="Woensdag">Wo</abbr>
                        </th>
                        <th scope="col">
                            <abbr class="datepicker-day--title" title="Donderdag">Do</abbr>
                        </th>
                        <th scope="col">
                            <abbr class="datepicker-day--title" title="Vrijdag">Vr</abbr>
                        </th>
                        <th scope="col">
                            <abbr class="datepicker-day--title" title="Zaterdag">Za</abbr>
                        </th>
                    </tr>
                </thead>
                <tbody>
                    <tr>
                        <td role="gridcell">
                            <span class="datepicker-day--inactive">27</span>
                        </td>
                        <td role="gridcell" tabindex="0">
                            <span class="datepicker-day--inactive">28</span>
                        </td>
                        <td role="gridcell">
                            <span class="datepicker-day--inactive">29</span>
                        </td>
                        <td role="gridcell">
                            <span class="datepicker-day--inactive">30</span>
                        </td>
                        <td role="gridcell">
                            <span class="datepicker-day--active">1</span>
                        </td>
                        <td role="gridcell">
                            <span class="datepicker-day--deselected">2</span>
                        </td>
                        <td role="gridcell">
                            <span class="datepicker-day--active">3</span>
                        </td>
                    </tr>
                    <tr>
                        <td role="gridcell">
                            <span class="datepicker-day--deselected">4</span>
                        </td>
                        <td role="gridcell">
                            <span class="datepicker-day--active">5</span>
                        </td>
                        <td role="gridcell">
                            <span class="datepicker-day--selected">6</span>
                        </td>
                        <td role="gridcell">
                            <span class="datepicker-day--active">7</span>
                        </td>
                        <td role="gridcell">
                            <span class="datepicker-day--active">8</span>
                        </td>
                        <td role="gridcell">
                            <span class="datepicker-day--active">9</span>
                        </td>
                        <td role="gridcell">
                            <span class="datepicker-day--active">10</span>
                        </td>
                    </tr>
                    <tr>
                        <td role="gridcell">
                            <span class="datepicker-day--active">11</span>
                        </td>
                        <td role="gridcell">
                            <span class="datepicker-day--deselected">12</span>
                        </td>
                        <td role="gridcell">
                            <span class="datepicker-day--active">13</span>
                        </td>
                        <td role="gridcell">
                            <span class="datepicker-day--active">14</span>
                        </td>
                        <td role="gridcell">
                            <span class="datepicker-day--active">15</span>
                        </td>
                        <td role="gridcell">
                            <span class="datepicker-day--active">16</span>
                        </td>
                        <td role="gridcell">
                            <span class="datepicker-day--active">17</span>
                        </td>
                    </tr>
                    <tr>
                        <td role="gridcell">
                            <span class="datepicker-day--active">18</span>
                        </td>
                        <td role="gridcell">
                            <span class="datepicker-day--active">19</span>
                        </td>
                        <td role="gridcell">
                            <span class="datepicker-day--active">20</span>
                        </td>
                        <td role="gridcell">
                            <span class="datepicker-day--active">21</span>
                        </td>
                        <td role="gridcell">
                            <span class="datepicker-day--deselected">22</span>
                        </td>
                        <td role="gridcell">
                            <span class="datepicker-day--active">23</span>
                        </td>
                        <td role="gridcell">
                            <span class="datepicker-day--active">24</span>
                        </td>
                    </tr>
                    <tr class="">
                        <td role="gridcell">
                            <span class="datepicker-day--active">25</span>
                        </td>
                        <td role="gridcell">
                            <span class="datepicker-day--active">26</span>
                        </td>
                        <td role="gridcell">
                            <span class="datepicker-day--deselected">27</span>
                        </td>
                        <td role="gridcell">
                            <span class="datepicker-day--active">28</span>
                        </td>
                        <td role="gridcell">
                            <span class="datepicker-day--active">29</span>
                        </td>
                        <td role="gridcell">
                            <span class="datepicker-day--active">30</span>
                        </td>
                        <td role="gridcell">
                            <span class="datepicker-day--active">31</span>
                        </td>
                    </tr>
                </tbody>
            </table>
        </div>
    </section>
</template>

<script>
export default {
    name: 'bbDatePicker',
    data() {
        return {
            currentDate: 'Juli 2020'
        }
    }
}
</script>

<style lang="scss" scoped>
@import url('https://fonts.googleapis.com/css2?family=Open+Sans:wght@700&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Open+Sans:wght@600;700&display=swap');

$calendar-date: #50B6FF;
$calendar-bgc: #ffffff;
$calendar-divider: #4FB5FF;
$calendar-inactive: #818181;
$calendar-active: #B1D5FF;
$calendar-title: #009CFF;
$calendar-subtitle: #818181;
$calendar-deselected: #0089FF;
$calendar-deselected-border: #009CFF;;
$calendar-selected: #ffffff;
$calendar-selected-bgc: #0064FF;

table {
    font-family: 'Open Sans', sans-serif;
    table-layout: fixed;
    border-collapse: collapse;
    text-align: center;
    & td {
        height: 30px;
        width: 30px;
    }
}

hr {
    display: block;
    height: 1px;
    border: 0;
    border-top: 1px solid $calendar-divider;
    margin: 10px 0 0 0;
    padding: 0;
}

.datepicker {
    &-container {
        width: 100%;
        background-color: $calendar-bgc;
        border-top-left-radius: 45px;
    }

    &-wrapper {
        margin-left: 40px;
        height: 361px;
    }

    &-title {
        font-family: 'Palanquin Bold', sans-serif;
        font-size: 20px;
        color: $calendar-title;
        margin-bottom: 0;
    }

    &-subtitle {
        font-family: 'Open Sans', sans-serif;
        font-weight: 600;
        font-size: 13px;
        margin: 0;
        color: $calendar-subtitle;
    }

    &-table {
        height: 196px;
    }

    &-caption--title {
        color: $calendar-date;
        font-weight: bold;
        font-size: 14px;
        margin: 10px 0;
    }

    &-day--deselected {
        display: flex;
        justify-content: center;
        align-items: center;
        height: 30px;
        width: 30px;
        color: $calendar-deselected;
        border: 1px solid $calendar-deselected-border;
        border-radius: 50%;
    }

    &-day--selected {
        display: flex;
        justify-content: center;
        align-items: center;
        height: 30px;
        width: 30px;
        color: $calendar-selected;
        background-color: $calendar-selected-bgc;
        border-radius: 50%;
    }

    &-day--active {
        color: $calendar-active;
    }

    &-day--inactive {
       color: $calendar-inactive;
       opacity: 40%; 
    }

    &-day--title {
        color: $calendar-title;
        text-decoration: none;
    }
}
</style>
