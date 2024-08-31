<template>
    <view class="content">
      <view class="base">
        <view class="avatar-container">
            <image class="avatar" src="/static/logo.png"></image>
        </view>
        <view class="name">
            {{ name }}
        </view>
        <view class="que-name">
            {{ queName }} 
            <span>当月积分{{score}}</span>
        </view> 
      </view>
      <view class="list-container">
        <view class="list-item self-data" @click="goSelfData">
            <view class="icon-container">
                <image class="icon" src="../../static/data.png"></image>
                个人数据
            </view>
            <image class="arrow" src="../../static/arrow.jpg"></image>
        </view>
        <view class="list-item update-info">
            <view class="icon-container">
                <image class="icon" src="../../static/profile.png"></image>
                修改资料
            </view>
            <image class="arrow" src="../../static/arrow.jpg"></image>
            </view>
        <view class="list-item hate-value">
            <view class="icon-container">
                <image class="icon" src="../../static/hate.png"></image>
                仇恨值
            </view>
            <image class="arrow" src="../../static/arrow.jpg"></image>
            </view>
        <view class="list-item rank">
            <view class="icon-container">
                <image class="icon" src="../../static/rank.png"></image>
                雀庄当月排行
            </view>
            <image class="arrow" src="../../static/arrow.jpg"></image>
            </view>
      </view>
    </view>
  </template>
  
  <script>
  export default {
    data() {
      return {
        title: "Hello",
        name: "公式战昵称",
        queName: '雀庄1',
        score: 0
      };
    },
    onLoad() {
      console.log("onload");
    },
    methods: {
        goSelfData() {
            console.log("去个人数据页面")
            // uni.navigateTo('/pages/newPage/newPage')
        }
    },
  };
  </script>
  
  <style>
  .content {
    color: #333;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
  }
  .base {
    margin-top: 10px;
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  .base .avatar-container {
    width: 80px;
    height: 80px;
    border-radius: 50%;
    overflow: hidden;
  }
  .base .avatar {
    width: 100%;
    height: 100%;
  }
  .base .name {
    margin-top: 5px;
  }
  .list-container {
    width: 100%;
    padding: 12px 0;
  }
  .list-container .list-item {
    height: 45px;
    display: flex;
    align-items: center;
    border-bottom: 1px solid #eee;
    box-sizing: border-box;
    padding: 0 12px;
  }
  .list-item {
    display: flex;
    justify-content: space-between;
  }
  .list-item .icon-container {
   display: flex;
   align-items: center;
  }
  .list-item .icon {
    width: 20px;
    height: 20px;
    margin-right: 4px;
  }

  .list-item .arrow {
    width: 16px;
    height: 16px;
  }
  
  </style>
  