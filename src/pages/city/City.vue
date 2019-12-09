<template>
  <div class="city">
    <city-header></city-header>
    <city-hot :hot="hotCities"></city-hot>
    <city-letter :cities="cities"></city-letter>
    <city-list 
      :cities="cities" 
      @change="handleLetterChange"
    ></city-list>
  </div>
</template>

<script>
import axios from 'axios'
import CityHeader from './components/Header'
import CityList from './components/List'
import CityHot from './components/Hot'
import CityLetter from './components/Letter'
export default {
  name: 'City',
  components: {
    CityHeader,
    CityHot,
    CityLetter,
    CityList,
  },
  data () {
    return {
      cities: {},
      hotCities: []
    }
  },
  methods: {
    getCityInfo () {
      axios.get('api/city.json')
        .then(this.handleGetCityInfoSucc)
    },
    handleGetCityInfoSucc (res) {
      res = res.data
      if (res.ret && res.data) {
        const data = res.data
        this.cities = data.cities
        this.hotCities = data.hotCities
      }
    },
    handleLetterChange (letter) {
      this.letter = letter
    }
  },
  mounted () {
    this.getCityInfo()
  }
}
</script>

<style lang="stylus" scoped>
  .city
    background: #f5f5f5
</style>
