<template>
  <form>
      ID : <input type="text"><br/><br/>
      PWD : <input type="text"><br/><br/>
  </form>
  <button type="button" @click="findId">
      아아디 찾기
  </button>
  <button type="button" @click="findPwd">
      비밀번호 찾기
  </button>

    <div class="modal__background" v-if="findIdCount==1">
        <div class="modal__box">
            아이디 찾기
        </div>
    </div>

    <div class="modal__background" v-if="findPwdCount==1">
        <div class="modal__box">
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
            this.findIdCount = 1;
        },
        findPwd(){
            this.findPwdCount = 1;
        },

    }

}
</script>

<style>
/* 모달창의 배경을 만든다 */
.modal__background{
  position: fixed;
  top:0; left: 0; bottom: 0; right: 0;
  background: rgba(0, 0, 0, 0.8);
}
 
/* 모달창 영역을 꾸민다 */
.modal__box{
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