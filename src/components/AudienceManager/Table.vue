<template>
  <div class="table">
    <div class="table__header">
      <div class="cell width__xsmall">
        <div class="cell__checkbox">
          <!-- checkmark toggles here -->
        </div>
      </div>
      <div class="cell width__large">Campus</div>
      <div class="cell width__small">Stdnts</div>
      <div class="cell width__medium">City</div>
      <div class="cell width__small">State</div>
      <div class="cell width__medium">Media Offered</div>
      <div class="cell width__medium relevance">Relevance</div>
    </div>
    <div class="table__row">
      <div class="cell width__xsmall">
        <div class="cell__checkbox">
          <!-- checkmark toggles here -->
        </div>
      </div>
      <div class="cell width__large">University of Alabama</div>
      <div class="cell width__small">93k</div>
      <div class="cell width__medium">Tuscaloosa</div>
      <div class="cell width__small">AL</div>
      <div class="cell width__medium">
        <font-awesome-icon icon="newspaper" style="font-size: 20px;" class="cell__mediaIcon"/>
        <font-awesome-icon icon="desktop" style="font-size: 16px;" class="cell__mediaIcon"/>
        <font-awesome-icon icon="comment" style="font-size: 20px;" class="cell__mediaIcon"/>
        <font-awesome-icon icon="tree" style="font-size: 18px;" class="cell__mediaIcon"/>
      </div>
      <div class="cell width__medium">
          <div class="cell__relevance">
            <div class="cell__relevance--bar blue"/>
            <div class="cell__relevance--bar blue"/>
            <div class="cell__relevance--bar blue"/>
            <div class="cell__relevance--bar"/>
            <div class="cell__relevance--bar"/>
            <font-awesome-icon icon="info-circle" style="font-size: 14px;" class="cell__infoIcon"/>
          </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Table',
  props: {
    msg: String
  }
}
</script>

<style scoped>
.table {
  height: 75%;
  padding-top: 1rem;
}

.table__header,
.table__row {
  align-items: center;
  border-bottom: 1px solid #CDD4E3;
  display: flex;
  font-size: .85rem;
  width: 100%;
}

.table__header {
  font-weight: bold;
}

.table__row {
  cursor: pointer;
  padding: .5rem 0;
}

.cell {
  align-items: center;
  color: #788193;
  display: flex;
  flex-direction: row;
  padding: .25rem .5rem;
}

.cell.width__small {
  width: 20px;
}

.cell.width__small {
  flex: 1 1;
}

.cell.width__medium {
  flex: 2 1;
}

.cell.width__large {
  flex: 3 1;
}

.cell__checkbox {
  border: 1px solid #788193;
  border-radius: 3px;
  box-shadow: inset 1px 1px 1px #788193;
  height: 14px;
  width: 14px;
}

.cell__mediaIcon {
  color: #788193;
  padding-right: .5rem;
}

.cell__relevance {
  align-items: center;
  display: flex;
}

.cell__relevance--bar {
  background: #CDD4E3;
  height: 24px;
  margin-right: .25rem;
  width: 8px;
}

.cell__relevance--bar.blue {
  background: #5FAEE1;
}

.cell__infoIcon {
  color: #CDD4E3;
  margin-left: .5rem;
}
</style>
