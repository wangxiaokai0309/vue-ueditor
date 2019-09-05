  <template>
  <div class="hello">
    <ueditor v-model="form.content" id="editor" ref="editor"></ueditor>
    <div class="button-group">
      <button class="button" @click="check">输出</button>
      <button class="button" @click="reset">重置</button>
      <button class="button" @click="setDisabled">不可编辑</button>
      <button class="button" @click="setEnabled">可编辑</button>
    </div>
  </div>
</template>

<script>
import ueditor from "./ueditor";
export default {
  name: "hello",
  data() {
    return {
      msg: "Welcome to Your Vue.js App",
      form: {
        content: ""
      }
    };
  },
  components: { ueditor },
  methods: {
    reset() {
      this.$refs.editor.editor.setContent(
        '<p style="text-align:left;line-height:36px"><span style="font-size:21px;font-family:黑体">&nbsp;</span></p><p style="text-align:center;line-height:36px"><span style="font-family: 方正小标宋简体; font-size: 29px;">&nbsp;区域节能审查受理单</span></p><p style="text-align:right;line-height:36px"><span style="font-size:20px;font-family:&#39;Times New Roman&#39;,serif">×</span><span style="font-size:20px;font-family:仿宋_GB2312">发改区受字第（</span><span style="font-size:20px;font-family:&#39;Times New Roman&#39;,serif">&nbsp;&nbsp; </span><span style="font-size:20px;font-family:仿宋_GB2312">）号</span></p><p style="text-align:left;line-height:37px"><br/></p><p style="text-align:left;line-height:37px"><span style="text-decoration:underline;"><span style="font-size:21px;font-family:仿宋_GB2312">&nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp;&nbsp;</span></span><span style="font-size:21px;font-family:宋体">：</span></p><p style="text-align:left;text-indent:43px;line-height:37px"><span style="font-size:21px;font-family:仿宋_GB2312">你（单位）于<span style="text-decoration:underline;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span>年<span style="text-decoration:underline;">&nbsp;&nbsp; </span>月<span style="text-decoration:underline;">&nbsp;&nbsp; </span>日提出的<span style="text-decoration:underline;">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span></span></p><p style="text-align:left;line-height:37px"><span style="text-decoration:underline;"><span style="font-size:21px;font-family:仿宋_GB2312">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span></span><span style="font-size:21px;font-family:仿宋_GB2312">申请收悉，经审查，决定予以受理。</span><span style="font-size:21px;font-family:仿宋_GB2312">本单位具体办理处（科）室为</span><span style="text-decoration:underline;"><span style="font-size:21px;font-family:仿宋_GB2312">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span></span><span style="font-size: 21px;font-family:仿宋_GB2312">处（科）。联系人：</span><span style="text-decoration:underline;"><span style="font-size:21px;font-family:仿宋_GB2312">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span></span><span style="font-size:21px;font-family:仿宋_GB2312">；</span> <span style="font-size:21px;font-family:仿宋_GB2312">联系电话：</span><span style="text-decoration:underline;"><span style="font-size:21px;font-family:仿宋_GB2312">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span></span><span style="font-size: 21px;font-family:仿宋_GB2312">。</span></p><p style="text-align:left;line-height:37px"><span style="font-size:21px;font-family:仿宋_GB2312">&nbsp;&nbsp;&nbsp; </span><span style="font-size:21px;font-family:仿宋_GB2312">特此通知。</span></p><p style="text-align:left;line-height:37px"><br/></p><p style="text-align:left;line-height:37px"><br/></p><p style="text-align: right; line-height: 37px;"><span style="font-size:21px;font-family:仿宋_GB2312">&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; </span><span style="font-size:21px;font-family:仿宋_GB2312">年&nbsp;&nbsp;&nbsp; 月&nbsp;&nbsp;&nbsp; 日</span></p>'
      );
    },
    check() {
      console.log(this.form.content);
    },
    setDisabled() {
      this.$refs.editor.editor.setDisabled("fullscreen");
    },
    setEnabled() {
      this.$refs.editor.editor.setEnabled("fullscreen");
    }
  }
};
</script>

  <!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
.button-group {
  position: absolute;
  top: 50px;
  right: 100px;
}
#editor {
  width: 600px;
  height: 500px;
  margin: 0 auto;
}
</style>
