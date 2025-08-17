<template>
    <Header />
        <div class="services">
            <h2>Destinos</h2>
            <p>Explore nossos destinos incríveis!</p>
            <ul>
                <li>Praia do Forte</li>
                <li>Chapada Diamantina</li>
                <li>Ilhéus</li>
                <li>Porto Seguro</li>
            </ul>
        </div>
    <Footer />
</template>
<script>
    import Header from '../components/Header.vue';   
    import Footer from '../components/Footer.vue';
    export default {
        name: 'Services',
        components: {
            Header,
            Footer
        }
    }
</script>
<style scoped>
    .services {
        padding: 20px;
        background-color: #f0f0f0;
    }
    .services h2 {
        color: #333;
    }
    .services p {
        font-size: 16px;
        color: #666;
    }
    .services ul {
        list-style-type: none;
        padding: 0;
    }
    .services ul li {
        background-color: #fff;
        margin: 5px 0;
        padding: 10px;
        border-radius: 5px;
        box-shadow: 0 2px 4px rgba(0, 0,    0, 0.1);
    }
    .services ul li:hover {
        background-color: #e9ecef;
    }
</style>