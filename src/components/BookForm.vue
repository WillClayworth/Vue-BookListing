<template>
    <form v-on:submit.prevent="bookSubmit(bookTitle, bookAuthor)" class="" action="#" method="post">
        <input v-model="bookTitle" type="text" name="title" placeholder="Book Title"/>
        <input v-model="bookAuthor" type="text" name="author" placeholder="Book Author"/>
        <button type="submit" name="button">Add Book</button>
    </form>
</template>

<script>
export default {
    name: 'BookForm',
    props: ['books'],
    data(){
        return {
            bookTitle: '',
            bookAuthor: ''
        }
    }
}
</script>

<style>
    h1, h2{
        font-weight: normal;
    }
    ul{
        list-style-type: none;
        padding: 0;
    }
</style>