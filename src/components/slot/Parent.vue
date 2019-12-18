<template>
  <div>
    <BaseModal>
      <template #header="slotProps"> <!-- #으로 단축해서 사용 -->
        <h1>모달 제목</h1>
        <button @click="slotProps.close">닫기</button>
        {{ slotProps }} <!-- { hello: 'hello' } -->
      </template>
      <template #[slotProps]> <!-- 동적인 슬롯명 사용  slotProps 사용시 자식의 것, slotName 사용시 부모의 내용이 나온다?? -->
        <p>모달의 컨텐츠입니다.</p>
      </template>
    </BaseModal>
  </div>
</template>
<script>
import BaseModal from "@/components/slot/BaseModal.vue"
export default {
	name : "parent",
	components : {
		BaseModal
	},
	data(){
		return {
			slotName: 'content'
		}
	}
}
</script>
<style scoped>

</style>