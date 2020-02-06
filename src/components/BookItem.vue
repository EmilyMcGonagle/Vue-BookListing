<template>
    <li v-for='book in books'>{{book.title}}:((book.author))</li>
</template>
    

<script>
export default {
    data: () => {
        name: 'BookItem';
        props: [
            'book',
        ]
    }
}
</script>

<style>

</style>
