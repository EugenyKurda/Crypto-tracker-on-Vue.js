<template>
    <div>
        <header class="header">
            <h1 class="header-title">{{appName}}</h1>
        </header>
    </div>
</template>

<script>
export default {
    name: 'my-header',
    data() {
        return {
            appName: 'Cryptocurrency App'
        }
    }
}
</script>