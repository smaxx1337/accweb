<template>
    <div>
        <label>{{label}}</label>
        <input :type="type"
            :placeholder="placeholder"
            v-bind:value="value"
            v-on:input="$emit('input', $event.target.value)"
            :step="step" />
        <div class="error" v-show="error">{{error}}</div>
    </div>
</template>

<script>
export default {
    props: {
        value: null,
        type: {default: "text"},
        label: null,
        placeholder: null,
        step: null,
        error: null
    }
}
</script>
