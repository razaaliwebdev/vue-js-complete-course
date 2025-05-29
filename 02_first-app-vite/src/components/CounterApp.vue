<template>
    <div class="count-wrapper">
        <h1>Counter App Using Vue JS</h1>
        <div class="counter-box">
            <button @click="count--" class="btn">-</button>
            <div class="count-display">{{ count }}</div>
            <button @click="count++" class="btn">+</button>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            count: 0
        };
    }
}
</script>

<style>
.count-wrapper {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: 30vh;
    font-family: Arial, sans-serif;
    background: #f5f5f5;
}

h1 {
    margin-bottom: 20px;
    font-size: 28px;
    color: #333;
}

.counter-box {
    display: flex;
    align-items: center;
    gap: 20px;
    background: #fff;
    padding: 15px 30px;
    border-radius: 10px;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
}

.btn {
    background-color: #007bff;
    border: none;
    color: white;
    font-size: 22px;
    padding: 10px 20px;
    border-radius: 5px;
    cursor: pointer;
}

.btn:hover {
    background-color: #0056b3;
}

.count-display {
    font-size: 24px;
    width: 40px;
    text-align: center;
}
</style>
