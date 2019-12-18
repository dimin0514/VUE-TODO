<template>
<div>
  <header>
    <slot name="header" :hello="childData" :close="close">
      <strong>기본 타이틀</strong>
      <button>기본 버튼</button>
    </slot>
  </header>
  <div>
    <slot name="content">
      <p>이것은 자식의  콘텐츠</p>
    </slot>
  </div>
</div>
</template>
<script>
export default {
	name:"baseModal",
	data(){
		return {
			childData : "hello",
			active : false
		}
	},
	methods: {
		colse(){
			this.active = false
		}
	}
}
</script>
<style scoped></style>