
<template>
  <div id="travel">
    <Loading v-show="loading"></Loading>
    <div class="travel" v-show="!loading">
      <h3>今までの旅行先</h3>
      <div v-for="country in countries" :key="country.index">
        <hr />
        Abroad: {{ country.name }}
        <br />
        Date: {{ country.date }}
        <br />
        Purpose: {{ country.purpose }}
        <br />
        {{ country.companion }}
      </div>
      <hr />
    </div>
  </div>
</template>

<script>
import Loading from "../components/Loading.vue";

export default {
  data: function() {
    return {
      loading: true,
      countries: [
        {
          name: "Australia",
          date: "2010",
          purpose: "School Trip",
          companion: "School",
          index: "T0001"
        },
        {
          name: "Bangladesh",
          date: "2016",
          purpose: "Volunteer",
          companion: "Contingent",
          index: "T0002"
        },
        {
          name: "China",
          date: "2017",
          purpose: "Sight Seeing",
          companion: "Friends",
          index: "T0003"
        },
        {
          name: "Philliphine",
          date: "2018",
          purpose: "International Meeting",
          companion: "Contingent",
          index: "T0004"
        },
        {
          name: "India",
          date: "2019",
          purpose: "Academic Conference",
          companion: "Assisstant Professor",
          index: "T0005"
        },
        {
          name: "Thailand",
          date: "2019",
          purpose: "Sight Seeing",
          companion: "Alone",
          index: "T0006"
        }
      ]
    };
  },
  mounted() {
    this.loading = false;
  },
  components: {
    Loading
  }
};
</script>
