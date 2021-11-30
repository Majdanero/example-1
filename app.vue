<template lang="pug">
div
	h1 Example page
	NuxtPage
</template>
<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Montserrat:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');
* {
	font-family: Montserrat,serif;
	background: none;
	color: #ffffff;
	box-shadow: none;
	border: none;
	outline: none;

}
body {
	background-color: #333333;
}
input {
	border: 1px solid #ffffff;
	border-radius: 5px;
	padding: 5px 10px;
	margin: 5px;
}
button {
	margin: 5px;
	border: 1px solid #ffffff;
	border-radius: 5px;
	padding: 5px 10px;
	background-color: rgba(#ffffff, 0.2);
	cursor: pointer;
	&:hover {
		background-color: rgba(#ffffff, 0.3);
	}
}
</style>
