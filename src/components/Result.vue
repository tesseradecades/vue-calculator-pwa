<template>
    <div>
        <table>
            <tr class="table-head">
                <th class="name">Name</th>
                <th class="value">Value</th>
            </tr>
            <tr
                v-for='result in results'
                :key="result.label"
            >
                <td>{{result.label}}</td>
                <td class="value">{{result.value}}</td>
            </tr>
        </table>
        <button
            v-on:click="handleClickback"
            class="btn-back"
        >
        Back
        </button>
    </div>
</template>

<script>
export default {
  name: "Result",
  props: {
      results: Object
  },
  methods: {
      handleClickback: function(){
          this.$emit("clearCalculations");
      }
  }
};
</script>

<style lang="scss" src="../assets/styles/Result.scss"/>