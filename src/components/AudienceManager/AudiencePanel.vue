<template>
	<div class="audiencePanel">
		<div class="audiencePanel__arrows">
			<font-awesome-icon icon="angle-double-left" style="font-size: 18px;"/>
		</div>
		<div class="audiencePanel__nodata">
			Looks like you don't have any campuses in your audience yet.
			You can add campuses by selecting them from your search list on the left.
		</div>
		<div class="audiencePanel__header">
			<div class="audiencePanel__header--title">My Audience</div>
			<div class="audiencePanel__header--control">
				<input class="control__input" placeholder="Name your audience"/>
				<font-awesome-icon icon="pen" style="font-size: 14px;"/>
			</div>
		</div>
		<div class="audiencePanel__content">
			<Stats/>
		</div>
	</div>
</template>

<script>
  import Stats from './Stats.vue';

  export default {
    name:       'AudiencePanel',
    components: {
      Stats
    },
    props:      {
      msg: String
    }
  };
</script>

<style scoped>
	.audiencePanel {
		display: flex;
		flex-direction: column;
		height: 100%;
		padding: 2rem;
		position: relative;
	}

	.audiencePanel__arrows {
		background: #fff;
		color: #CDD4E3;
		cursor: pointer;
		margin-left: calc(-2rem - 10px);
		position: absolute;
		transition: color .5s ease;
	}

	.audiencePanel__arrows:hover {
		color: #788193;
	}

	.audiencePanel__nodata {
		color: #CDD4E3;
		position: absolute;
		margin: 55% 2rem 0 0;
		text-align: center;
	}

	.audiencePanel__header--title {
		color: #333;
		font-weight: bold;
	}

	.audiencePanel__header--control {
		align-items: center;
		border-bottom: 1px solid #CDD4E3;
		color: #CDD4E3;
		display: flex;
		justify-content: space-between;
		padding: 1rem .5rem .125rem 0;
	}

	.control__input {
		border: none;
		padding: .5rem 0;
		width: 90%;
	}

	.control__input:focus {
		outline: none;
	}

	.control__input::placeholder {
		color: #CDD4E3;
	}


</style>
