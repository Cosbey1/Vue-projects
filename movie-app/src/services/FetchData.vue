<script>
export default {
  data() {
    return {
      data: null,
    };
  },
  methods: {
    async fetchData() {
      const response = await fetch('http://www.omdbapi.com/?i=tt3896198&apikey=f119b9f9');
      this.data = await response.json();
    },
  },
  mounted() {
    this.fetchData();
  },
};
</script>