<template>
	<div>
		<Nav></Nav>
		시작하는 숫자 <input type="text" v-model="first" >
		끝나는 숫자 <input type="text" v-model="second" ><br>
		
		<button @click="sum" value="결과값 "> 합계? </button> {{sumvalue}} 
		<Footer></Footer>
	</div>
</template>
<script>
import Nav from "@/components/cmm/Nav.vue"
import Footer from "@/components/cmm/Footer.vue"
export default {
	name:'seqsum',
	components:{
		Nav, Footer
	},
	data(){
		return {
			sumvalue:0,
			first : '',
			second : ''
		}
	},
	methods: {
		sum(){
/* 			const first= parseInt(document.getElementById("first").value)
			const second= parseInt(document.getElementById("second").value) */
			// let start =0, end = 0
/* 			let _first = parseInt(this.fisrt)
			let _second = parseInt(this.second)
			let arr = [_first,_second] */
			// let arr = [Number(this.fisrt),Number(this.second)]
			/* if(_first<_second){
				start = _first
				end = _second
			}else{
				start = _second
				end = _first
			} */
		/* 	arr.sort()
			let sum = 0 */
			/* for(let i=start;i<end+1;i++){
				sum += i
			} */
	/* 		for(let i=arr[0];i<arr[1]+1;i++){
				sum += i
			}
			this.sumvalue= sum */
			

			let a = parseInt(this.first)
			let b = parseInt(this.second)
			alert(`a의 타입 ${typeof a} b의 타입 ${typeof b}`)
			const arr = [a, b]
			arr.sort(function(a, b){
				return a - b
			})
			let sum = 0
			let start = arr[0]
			let end = arr[1]+1
			for(let i=start; i< end; i++){
				sum += i
			}
			this.sumvalue = sum
		}
	}
}
</script>
<style scoped>

</style>