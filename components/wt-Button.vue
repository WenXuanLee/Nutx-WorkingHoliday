<script>
export default {
  functional: true,
  props: {
    title: {
      type: String,
    },
    type: {
      type: String,
      default: 'button'
    },
    customClass: {
      type: String,
      default: 'btn'
    },
  },
  render(h, { props, listeners, children}) {
    const data = {
      staticClass: `${ props.customClass}`,
      attrs: {
        title: props.title,
        type: props.type,
      },
      on: listeners,
    }
    return h("button", data, children);
  }
}
</script>

<style lang="less">
 button {
    align-items: flex-start;
    text-align: center;
    cursor: default;
    color: buttontext;
    background-color: buttonface;
    box-sizing: border-box;
    padding: 2px 6px 3px;
    border-width: 2px;
    border-style: outset;
    border-color: buttonface;
    border-image: initial;
}
.btn-link {
  background: transparent;
  border: 0;
  color: #008489;
  display: inline;
  font-weight: normal;
  margin: 0;
  padding: 0;
  vertical-align: bottom;
}
.btn-link--reset {
  color: inherit;
}
</style>