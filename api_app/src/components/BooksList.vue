<template>
    <section id=list-of-books>
        <ul class="books-list">
            <books-list-item v-for="(book, index) in books" :key="index" :book="book"></books-list-item>
        </ul>
    </section>
</template>

<script>
import BooksListItem from "@/components/BooksListItem.vue";

export default {
    name: "books-list",
    components: {
        "books-list-item": BooksListItem
    },
    props: ['books']
    
}
</script>

<style>
.books-list {
    display: flex;
    flex-flow: row wrap;
    justify-content: center;
}
</style>