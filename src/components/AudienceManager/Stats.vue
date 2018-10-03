<template>
	<div class="stats" :class="statsClass">
		<div class="stats__item">
			<div class="stats__item--count">0</div>
			<div class="stats__item--label">Campuses</div>
		</div>
		<div class="stats__item">
			<div class="stats__item--count">0</div>
			<div class="stats__item--label">Students</div>
		</div>
		<div class="stats__item">
			<div class="stats__item--count">0</div>
			<div class="stats__item--label">States</div>
		</div>
	</div>
</template>

<script>
  export default {
    name:     'Stats',
    props:    {
      isHorizontal: Boolean
    },
    computed: {
      statsClass () {
        return {'is-horizontal': this.isHorizontal};
      }
    }
  };
</script>

<style scoped lang="scss">

	.stats {
		display: flex;
		justify-content: space-around;
		padding: 1.5rem 0;
		.stats__item {
			align-items: center;
			display: flex;
			flex-direction: column;

			.stats__item--count {
				color: #5FAEE1;
				font-size: 1.5rem;
			}
		}

		&.is-horizontal {
			& > .stats__item {
				flex-direction: row;
			}
		}
	}


</style>
