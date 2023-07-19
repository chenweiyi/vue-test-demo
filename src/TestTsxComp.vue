<script lang="tsx">
import { computed, defineComponent } from 'vue';

export default defineComponent({
  name: 'TestTsxComp',
  props: {
    modelValue: {
      type: String,
      default: ''
    }
  },
  emits: {
    'update:modelValue': (value: string) => typeof value === 'string'
  },
  setup(props, { emit }) {
    
    const value = computed({
      get: () => props.modelValue,
      set: (val) => {
        emit('update:modelValue', val)
      }
    })
    return () => (
      <input v-model={value.value} />
    )
  }
})

</script>

