<template>
    <div class="backdrop">
        <div class="modal">
            <h1>Modal Title</h1>
            <p>Modal content here</p>
        </div>
    </div>
</template>

<style scoped>
    .backdrop {
        top: 0;
        position: fixed;
        background: rgba(0,0,0,0.5);
        width: 100%;
        height: 100%;
    }
    .modal {
        width: 400px;
        padding: 20px;
        margin: 100px auto;
        background: white;
        border-radius: 10px;
    }
    h1 {
        color: aquamarine;
        border: none;
        padding: 0
    }
    .modal h1 {
        color: aquamarine;
        border: none;
        padding: 0;
    }
    .modal p {
    font-style: normal;
    }
</style>