<template>
  <button type="button" class="btn btn-warning negotiator-btn" data-toggle="tooltip" data-placement="bottom"
          title="Send to the negotiator" @click="sendToNegotiator" :disabled="disabled">
          REQUEST SAMPLES
  </button>
</template>

<style>
  .negotiator-btn {
    margin-bottom: 1rem;
  }
</style>

<script>
  import { SEND_TO_NEGOTIATOR } from '../../store/actions'

  export default {
    name: 'negotiator',
    props: {
      disabled: {
        type: Boolean,
        required: false,
        default: true
      }
    },
    methods: {
      sendToNegotiator () {
        this.$store.dispatch(SEND_TO_NEGOTIATOR)
      }
    }

  }
</script>
