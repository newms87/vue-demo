<template>
  <div class="audienceManager">
    <PageHeader title="Audience Manager"/>
    <div class="audienceManager__content">
        <div class="audienceManager__content--search">
          <div class="audienceManager__title search">Search</div>
          <div class="search__content">
            <FilterPanel/>
            <div class="search__content--results">
              <Table msg="table"/>
            </div>
          </div>
        </div>
        <div class="audienceManager__content--audience">
          <div class="audienceManager__title audience">Audience</div>
          <div class="audience__content">
            <AudiencePanel/>
          </div>
        </div>
    </div>
  </div>
</template>

<script>
import AudiencePanel from './AudiencePanel.vue'
import FilterPanel from './FilterPanel.vue'
import PageHeader from '../../components/PageHeader.vue'
import Table from './Table.vue'

export default {
  name: 'AudienceManager',
  components: {
    AudiencePanel,
    FilterPanel,
    PageHeader,
    Table
  },
  props: {
    title: String
  }
}
</script>

<style scoped>
  .audienceManager {
    display: flex;
    flex-direction: column;
    grid-row: 2/-1;
    grid-column: 2/-1;
    margin: 2rem;
  }

  .audienceManager__content {
    display: flex;
    flex: 0 0 93%;
    justify-content: space-between;
  }

  .audienceManager__content--search {
    display: flex;
    flex: 0 0 70%;
    flex-direction: column;
  }

  .audienceManager__title {
    font-size: 1.5rem;
    height: 35px;
    padding: 1rem 0;
  }

  .audienceManager__title.search {
    color: #5FAEE1;
  }

  .audienceManager__title.audience {
    color: #788193;
  }

  .audienceManager__content--audience {
    display: flex;
    flex: 0 0 28%;
    flex-direction: column;
  }

  .audience__content {
    border: 1px solid #CDD4E3;
    border-radius: 3px;
    height: calc(100% - 35px);
  }

  .search__content {
    border: 1px solid #cdd4e3;
    border-radius: 3px;
    display: flex;
    height: calc(100% - 35px);
    width: 100%;
  }
</style>
