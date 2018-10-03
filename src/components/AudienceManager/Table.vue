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
		<TableRow v-for="row in rows" :row="row" :key="'tr-' + row.id"/>
	</div>
</template>

<script>
  import TableRow from './TableRow.vue';
  import rows from '../../resources/publishers';

  export default {
    name:       'Table',
    components: {
      TableRow
    },
    data () {
      return {
        rows
      };
    }
  };
</script>

<style scoped>
	.table {
		height: 75%;
		padding-top: 1rem;
	}

	.table__header {
		align-items: center;
		border-bottom: 1px solid #CDD4E3;
		display: flex;
		font-size: .85rem;
		width: 100%;
	}

	.table__header {
		font-weight: bold;
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
</style>
