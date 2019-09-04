<template>
  <v-container>
    <v-row
      justify="center"
    >
        <v-col
          cols="12"
          sm="12"
          md="6"
          lg="4"
          xl="3"
          v-for="element in elements"
          :key="element.id"
        >
          <v-card
            hover
          >
            <v-card-title class="card-title">{{ element.name }}</v-card-title>
            <v-card-text class="card-intro">{{ element.introduction }}</v-card-text>
            <v-card-text>作者: {{ element.author }}</v-card-text>
            <v-btn
              text
              v-bind:href="element.url"
              target="_blank"
            >
              <v-icon>mdi-send</v-icon> 点击以访问
            </v-btn>
          </v-card>
        </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'Elementlist',
  components: {
  },
  data: () => ({
    elements: [
      {
        id: "20190904001",
        name: "SafeU",
        introduction: "一个能够快速、安全分享文件的网页应用。抛弃U盘，无需登录，只需要一个提取码，便可在世界范围内访问你的文件。快速访问地址: safeu.xyz",
        author: "A2OS SafeU 开发团队",
        url: "https://safeu.a2os.club"
      },
      {
        id: "20190904002",
        name: "御道助手",
        introduction: "囊括了全校大部分常用服务的微信小程序，包含课表等常用教务功能、消费统计功能、电费查询、校车时刻等。",
        author: "苏瑞辅",
        url: "https://nuaa.suruifu.com"
      },
      {
        id: "20190904003",
        name: "A2OS BlogRoll",
        introduction: "南京航空航天大学 Blog 收集计划，你可以在这里浏览校内外人士的博客，也可以提交自己的博客或个人网站。",
        author: "A2OS 团队",
        url: "https://blogroll.a2os.club/"
      },
      {
        id: "20190904004",
        name: "金工实习网站校外代理",
        introduction: "通过此网站，可以从校外网络访问金工实习网站，方便同学练习金工实习题目、提交作业。",
        author: "VVZERO",
        url: "https://nuaa.vvzero.com/ceping"
      },
      {
        id: "20190904005",
        name: "NUAA-BookCorner 共享图书",
        introduction: "由南京航空航天大学Asuri战队，微软学生俱乐部，A2OS等部门的各方大佬以及毕业离校的优秀学长们捐助的计算机技术类图书共享以及书单推荐计划。",
        author: "Kit4y",
        url: "https://github.com/NUAA-Open-Source/BookCorner"
      }
    ]
  }),
};
</script>

<style>
  .card-title
  {
    background-color: #00E5FF;
    color: black;
  }
  .card-intro
  {
    margin-top: 10px;
  }
</style>