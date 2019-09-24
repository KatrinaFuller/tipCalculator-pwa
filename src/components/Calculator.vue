<template>
  <div class="calculator container-fluid">
    <div class="row title-row align-items-center">
      <div class="col-12 text-center">
        <h1>Tip Calculator</h1>
      </div>
    </div>

    <div class="row info-row align-items-center">
      <!-- total bill -->
      <div class="col-sm-2 col-md-3">
        <h5>Total bill:</h5>
      </div>
      <div class="col-sm-10 col-md-9">
        <div class="input-group mb-3">
          <div class="input-group-prepend">
            <span class="input-group-text">$</span>
          </div>
          <input type="number" class="form-control" aria-label="Amount" id="total-bill" />
        </div>
      </div>

      <!-- tip percentage -->
      <div class="col-sm-2 col-md-3">
        <h5 id="tipAmount">Tip:--</h5>
      </div>
      <div class="col-sm-10 col-md-9 slidecontainer">
        <input
          type="range"
          min="1"
          max="30"
          value="20"
          class="slider"
          id="tipRange"
          oninput="tipPercent()"
        />
      </div>

      <!-- number of people to split between -->
      <div class="col-sm-2 col-md-3">
        <h5 id="peopleAmount">Number of People:</h5>
      </div>
      <div class="col-sm-10 col-md-9 slidecontainer">
        <input
          type="range"
          min="1"
          max="20"
          value="1"
          class="slider"
          id="peopleRange"
          oninput="peopleRange()"
        />
      </div>

      <!-- horizontal line -->
      <hr />

      <!-- new bill per person -->
      <div class="col-sm-2 col-md-3">
        <h5>New Bill (per person):</h5>
      </div>
      <div class="col-sm-10 col-md-9">
        <h5 id="bill-per-person">$ 0</h5>
      </div>

      <!-- tip amount per person -->
      <div class="col-sm-2 col-md-3">
        <h5>Tip Amount (per person):</h5>
      </div>
      <div class="col-sm-10 col-md-9">
        <h5 id="tip-per-person">$ 0</h5>
      </div>
      <div class="row bottom-row align-items-center">
        <div class="col-6 text-center">
          <button type="button" class="btn reset-button" onclick="calculate()">Calculate</button>
        </div>
        <div class="col-6 text-center">
          <button type="button" class="btn reset-button" onclick="reset()">Reset</button>
        </div>
      </div>
    </div>
  </div>
</template>


<script>
export default {
  name: "calculator",
  data() {
    return {};
  },
  computed: {},
  methods: {},
  components: {}
};
</script>


<style scoped>
</style>