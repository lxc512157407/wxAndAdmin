<template>
  <div>
    <KInput
      v-model="inputCardValue"
      label="卡号"
      placeholder="填写本人卡号"
      clearable
    />
    <KInput
      v-model="inputNickName"
      label="昵称"
      placeholder="填写信号的昵称"
      clearable
    />
    <KButton
      type="primary"
      style="width: 100%;"
      @click="diaBtnOption.isShow=true"
    >
      页面主要操作
    </KButton>
    <KDialog
      v-model="diaBtnOption.isShow"
      :buttons="diaBtn"
      :title="diaBtnOption.title"
      desc="弹窗内容，告知当前状态、信息和解决方法，描述文字尽量控制在三行内"
    />
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator'
@Component({
  name: 'test',
  components: {}
})
export default class extends Vue {
  private inputCardValue='';
  private inputNickName='';
  // 声明成对象类型的值，便于按钮点击时修改其展示的状态。
  private diaBtnOption: any= { isShow: false, title: '零度的田' };
  private diaBtn: any[] =[
    {
      text: '确定',
      click: () => {
        this.diaBtnOption.isShow = false
        this.diaBtnOption.title = 'lala'
      }
    }
  ];
}
</script>

<style lang="scss" scoped>

</style>
