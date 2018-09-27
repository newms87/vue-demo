<template>
  <div class="audienceManager">
    <PageHeader title="Audience Manager"/>
    <div class="audienceManager__content">
        <div class="audienceManager__content--search">
          <div class="audienceManager__title search">Search</div>
          <div class="search__content">
            <FilterPanel/>
            <div class="search__content--results">
              <div class="results__header">
                <div class="results__header--title">Search Results</div>
                <div class="results__header--right">
                  <font-awesome-icon icon="search" style="font-size: 16px;"/>
                </div>
              </div>
              <div class="results__stats">
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
              <Table :results="results"/>
              <div class="results__footer">
                  <Button label="Add to Audience"/>
              </div>
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
import Button from '../../components/Button.vue'
import FilterPanel from './FilterPanel.vue'
import PageHeader from '../../components/PageHeader.vue'
import Table from './Table.vue'

const results = [
  {
    campus: 'University of Colorado',
    city: 'Boulder',
    state: 'CO',
    studentCount: 30000,
    mediaOffered: [1, 0, 0, 1],
    relevance: 3
  },
  {
    campus: 'University of Colorado',
    city: 'Boulder',
    state: 'CO',
    studentCount: 30000,
    mediaOffered: [1, 0, 0, 1],
    relevance: 3
  },
  {
    campus: 'University of Colorado',
    city: 'Boulder',
    state: 'CO',
    studentCount: 30000,
    mediaOffered: [1, 0, 0, 1],
    relevance: 3
  },
  {
    campus: 'University of Colorado',
    city: 'Boulder',
    state: 'CO',
    studentCount: 30000,
    mediaOffered: [1, 0, 0, 1],
    relevance: 3
  }
]

export default {
  name: 'AudienceManager',
  components: {
    AudiencePanel,
    Button,
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
    padding: 2rem;
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

  .search__content--results {
    display: flex;
    flex-direction: column;
    height: 100%;
    padding: 2rem;
    width: 100%;
  }

  .results__header {
    align-items: center;
    color: #788193;
    display: flex;
    flex: 0 0 2%;
    justify-content: space-between;
    padding-bottom: 1rem;
  }

  .results__footer {
    display: flex;
    justify-content: flex-end;
  }

  .results__header--title {
    color: #333;
    font-weight: bold;
  }

  .results__stats {
    align-items: center;
    display: flex;
    flex: 0 0 5%;
    justify-content: flex-start;
  }

  .stats__item {
    align-items: center;
    display: flex;
    padding-right: 1rem;
  }

  .stats__item--count {
    color: #5FAEE1;
    font-size: 2rem;
    padding-right: .25rem;
  }
</style>
