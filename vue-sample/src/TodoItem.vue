<script>
export default {
    props : {
        todo: Object
        // 그냥 이렇게 객체하나 들어온다고 해놓고 받아서 쓸 수도 있구나.
    }
}
</script>

<template>
    <li>{{ todo.text }}</li>
</template>