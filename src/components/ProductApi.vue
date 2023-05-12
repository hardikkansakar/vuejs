<template>
    <div>
        <h1>Get Product data using API</h1>
        
        <!-- <p>{{ products }}</p> -->
        <button @click="getAllProduct();">Call API</button>
    </div>
    <div v-for="elms in products">
        <ol>
        <li>ID : {{ elms.id }}</li>
        <li>Title : {{ elms.title }}</li>
        <li>Body : {{ elms.body }}</li>
        </ol>  
        
    </div>
</template>
<script>
    export default{
        name:'ProductApi',
        components:{},
        
        data(){
            return{
                products:[],
                
            }
            
        },
        methods:{
            async getAllProduct(){
                const productData =await fetch('https://jsonplaceholder.typicode.com/posts');
                this.products = await productData.json();
                console.log(this.products);
            }
        }

    };
</script>
