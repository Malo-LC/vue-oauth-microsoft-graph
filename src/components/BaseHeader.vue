<template>
  <div class="bigNav">
    <div class="insideNav">
      <button class="leftSide primary">
        <img src="../assets/HomeIcon.png" class="homeicon" />
        <p class="homeText">Home</p>
      </button>
      <button class="rightSide primary">
        <p class="LogText">Not logged in yet</p>
        <img src="../assets/AvatarIcon.png" class="avataricon" />
      </button>
    </div>
  </div>
</template>

<style>
.homeText {
  color: black;
  font-weight: 700;
  font-size: large;
  margin-left: 10px;
}
.LogText {
  color: black;
  font-weight: 700;
  font-size: large;
  margin-right: 10px;
}
.bigNav {
  width: 100vw;
  height: 10vh;
  background-color: #29b883;
  margin: 0;
  padding: 0;
}
.insideNav {
  height: 100%;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
}
.leftSide {
  display: flex;
  align-items: center;
  height: 100%;
}
.rightSide {
  height: 100%;
  display: flex;
  justify-content: right;
  align-items: center;
}
.homeicon {
  height: 80%;
  margin-left: 10px;
}
.avataricon {
  height: 80%;
  margin-right: 10px;
}
</style>
