<template>
    <div>
        <!-- prints title from data -->
        <h1>{{title}}</h1>
        <ul>
            <!-- loops through array of books from data and prints title and author -->
            <!-- :book passes book to book item as a prop -->
            <book-item v-for='book in books' :book='book'></book-item>
        </ul>
    </div>
</template>

<script>
// import child component
import BookItem from './BookItem';
export default {
    name: 'BookList',
    // sets value of components to object containing child comp.
    components: {
        BookItem
    },
    data: () => {
        // stores list of books
        return {
            title:"All Books",
            books: [
                {title: 'Self-Reliance', author: 'Ralph Waldo Emerson'},
                {title: 'American Gods', author: 'Neil Gaiman'},
                {title: 'Amusing Ourselves to Death', author: 'Neil Postman'},
            ]
            
        }
    }
}
</script>

<style>
h1, h2 {
    font-weight: normal;
}
ul {
    list-style-type: none;
    padding: 0;
}
</style>