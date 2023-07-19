<script lang="tsx">
import { defineComponent, ref } from 'vue'
import TestComp from './TestComp.vue'

export default defineComponent({
    name: 'TsxComp',
    setup() {
        const msg = ref('ni hao')

        return () => (
            // ts error 2322 
            // 不能将类型“{ "v-model": string; }” 分配给类型“IntrinsicAttributes & { readonly modelValue: string ...
            // but it works
            <TestComp v-model={msg.value} />
        )
    }
})

</script>
