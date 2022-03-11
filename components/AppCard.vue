<template>
    <div class="card">
        <slot name="media"></slot>
        <div class="card__content">
            <slot></slot>
        </div>
    </div>
</template>




<style>
.card{
	width: 90%;
	margin: 20px;
	border-radius: 10px;
	overflow: hidden;
	background: #173F58;
	box-shadow: 0px 1px 10px rgha(0,0,0,0.2);
	cursor: default;
}

.card:hover{
	box-shadow: 5px 5px 10px rgba(0, 0, 0, 4);
	
}

.card img{
	width: 100%;
	height: 200px;
}

.card {
	padding:15px;
	text-align:center;
    font-family: Helvetica;

}
.card .card__content h3{
    color:#fff;
	font-weight: 400;
	margin-bottom: 15px;

}
.card .card__content p{
	line-height: 1.5;
	color: #fff;
}

.card .card__content a{
	text-decoration: none;
	display: inline-block;
    padding: 10px;
    margin-top: 10px;
    color:#fff;
    border-radius: 10px;
    background: #05A053;
    
}
</style>
