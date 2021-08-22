<template>
  <div class="card mb-1" style="width: 18rem;">
    <img :src="pais.flag" class="card-img-top" :alt="`bandera-${pais.name}`" />
    <div class="card-body">
      <h5 class="card-title text-center">{{ pais.name }}</h5>
      <p class="card-text">
        <span class="badge badge-primary d-block mb-1">
          nativeName: {{ pais.nativeName }}
        </span>
        <span class="badge badge-info p-3 d-block mb-1">
          population: {{ numeroFormato(pais.population) }}
        </span>
        <span class="badge badge-primary d-block mb-1">
          capital: {{ pais.capital }}
        </span>
        <span class="badge badge-primary d-block mb-1">
          region: {{ pais.region }}
        </span>
      </p>
      <!-- <a href="#" class="btn btn-primary">Go somewhere</a> -->
    </div>
  </div>
</template>

<script>
export default {
  props: ["pais"],
  setup() {
    const numeroFormato = num => {
      return Intl.NumberFormat("de-DE").format(num);
    };

    return { numeroFormato };
  }
};
</script>
