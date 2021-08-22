<template>
    <div class="container">
        <nav class="breadcrumb breadcrumb-style mt-5 text-center bg-light rounded neo-shadow">
            <p class="text-center my-2 breadcrumb-item active">Developed by <span class="text-primary"> Unitech </span> &copy; copyright 2021</p>
        </nav>
    </div>
</template>

<script>
export default {
    name : "Footer"
}
</script>

<style  scoped>
.breadcrumb-style{
    width : fill-available;
    width: -moz-fill-available;
    width :-webkit-fill-available;
    position : static !important;
    display : block !important;
    text-align : center !important;
    bottom :0 !important;
    margin-bottom:0;
}
.neo-shadow{
border: 0 !important;
background-color: #e0e5ec !important;
box-shadow: -7px -7px 20px 0px #fff9, -4px -4px 5px 0px #fff9, 7px 7px 20px 0px #0002, 4px 4px 5px 0px #0001, inset 0px 0px 0px 0px #fff9, inset 0px 0px 0px 0px #0001, inset 0px 0px 0px 0px #fff9, inset 0px 0px 0px 0px #0001;
border-radius: 15px;
/* padding: 20px 0px!important; */
}
</style>