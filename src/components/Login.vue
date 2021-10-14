<template>
  <form>
      ID :   <input type="text"><br/><br/>
      PWD : <input type="text">
      <input type="submit" @click="findId" value="로그인">
      <br/><br/>
  </form>
  <button type="button" @click="findId">
      아아디 찾기
  </button>
  <button type="button" @click="findPwd">
      비밀번호 찾기
  </button>

    <div class="modal_background" v-if="findIdCount==1">
        <div class="modal_box">
            <button class="modal_close" @click="findId">X</button>
            아이디 찾기
        </div>
    </div>

    <div class="modal_background" v-if="findPwdCount==1">
        <div class="modal_box">
            <button class="modal_close" @click="findPwd">X</button>
            비밀번호 찾기
        </div>
    </div>

</template>

<script>

export default {
    data() {
        return {
            findIdCount : 0,
            findPwdCount : 0,
        }
    },
    methods : {
        findId(){
            if (this.findIdCount==0) {
                this.findIdCount = 1;
            } else {
                this.findIdCount = 0;
            }
        },
        findPwd(){
            if (this.findPwdCount==0) {
                this.findPwdCount = 1;
            } else {
                this.findPwdCount = 0;
            }
        },

    }

}
</script>

<style>
/* 모달창의 배경을 만든다 */
.modal_background{
  position: fixed;
  top:0; left: 0; bottom: 0; right: 0;
  background: rgba(0, 0, 0, 0.8);
}
 
/* 모달창 영역을 꾸민다 */
.modal_box{
  position: absolute;
  top: calc(50vh - 100px); left: calc(50vw - 200px);
  background-color: white;
  display: flex; justify-content: center;
  align-items: center;
  border-radius: 10px;
  width: 400px;
  height: 200px;
}

</style>