<template>
  <div id="calendar">
    <!-- 연도, 달, 요일, 달력 -->
    <!-- <div class="year">년도</div>
    <div class="month">월</div> -->
    <div class="container">
      <!-- <div>시각</div> -->
      <div class="week" v-for="weeks in week" :key="idx">{{ weeks }}</div>
      <div class="calender"></div>
    </div>
    <!-- 오늘날짜, 요일, 달 변경 버튼 -->
    <div class="controller">
      <h3>Today is ...</h3>
      <div class="thisDate">{{ viewDate }} 일</div>
      <div class="day">{{  }}</div>
      <div class="btn">
        <div>previous</div>
        <div>next</div>
      </div>
    </div>
    <!-- 배경화면 전환 -->
    <div class="backImg">
      <div class="imgView" id="1"></div>
      <div class="imgView" id="2"></div>
      <div class="imgView" id="3"></div>
      <div class="imgView" id="4"></div>
      <div class="imgView" id="5"></div>
      <div class="imgView" id="6"></div>
      <div class="imgView" id="7"></div>
      <div class="imgView" id="8"></div>
      <div class="imgView" id="9"></div>
      <div class="imgView" id="10"></div>
      <div class="imgView" id="11"></div>
      <div class="imgView" id="12"></div>
    </div>
  </div>
</template>

<script setup>
// 현재 날짜 및 시간
const today = new Date();
// [get은 반환, set은 대입의 역할]
// 현재 날짜 가져오기
const viewDate = today.getDate();
// 현재 년도 가져오기
const viewYear = today.getFullYear();
// 현재 월 가져오기 (0 부터 시작함으로 이번달을 구하려면 + 1)
const viewMonth = today.getMonth() + 1;
// 현재 요일 가져오기
const viewDay = today.getDay();

const week = ["SUN", "MON", "TUE", "WED", "THU", "FRI", "SAT"];
</script>

<style lang="less" scoped>
#calendar {
  width: 100%;
  padding-top: 30px;
  padding-bottom: 30px;
  background-color: violet;
  display: flex;
  justify-content: space-evenly;
  .container {
    display: flex;
    width: 40%;
    background-color: yellowgreen;
    .year {
      background-color: violet;
    }
    .week {
      width: 100%;
      text-align: center;
    }
  }
  .controller {
    display: flex;
    width: 30%;
    background-color: yellow;
  }
}
</style>