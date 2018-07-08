<template>
  <div class="panel space-4">
    <div v-if="panelTitle" class="panel-title">
      {{ panelTitle }}
    </div>
    <div class="panel-content">
      <slot name="panel-content"></slot>
    </div>
  </div>  
</template>
<script>
  export default {
    props: {
      panelTitle: {
        type: String,
        default: ''
      }
    }
  }
</script>

<style lang="less" scoped>
.panel {
  border: 1px solid #dce0e0;
  background-color: #fff;
  -webkit-border-radius: 0;
  -moz-border-radius: 0;
  border-radius: 0;
}

.panel-title {
  background-color: #edefed;
  color: #484848;
  font-size: 16px;
  border-bottom: 1px solid #dce0e0;  
  position: relative;
  margin: 0;
  padding: 12px 20px;
  border-top: 1px solid #dce0e0;
}

.panel-content {
  border-top: none;
  position: relative;
  margin: 0;
  padding: 20px;
  border-top: 1px solid #dce0e0;

  &:last-child {
    margin-bottom: 0;
  }

  &:first-child {
    margin-top: 0;
  }
}

.list-unstyled {
  padding-left: 0;
  list-style-type: none;
}

.checked-icon {
  font-style: normal;
  font-weight: normal;
  line-height: 1;
  font-size: 24px;
}
</style>