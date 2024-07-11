<template>
    <div class="about">
      <h1>HOME OF CHINESE PUGON-ROASTED ASADO</h1>
      <div>
        We take you back to the year 1936 when calesas clonked their way down the bustling streets and esquinitas of Binondo.
        On one of the narrow alleys stood a modest eatery called Panciteria Lido,
        owned by a Cantonese chef, known as Mr. Lido.

        The word panciteria originated from the term “pansit,” which was what Pinoys called noodles. It originated from “pian-sit,” a Hokkien phrase that means something quickly cooked.
      </div>
      <div>
        First known for its authentic Chinese food, the eatery soon became famous for its succulent and savory Pugon-Roasted Asado.
        Mr. Lido himself carefully basted the pork with precise proportions of Chinese herbs and spices.
        The marinated loin was roasted with the right amount of heat in an old-fashioned brick oven, called a pugon.
        The sweet and aromatic flavors were locked in from the delicately sweet marinade to the tender layer of white meat underneath.
        It was an ambrosial, unique creation and every bite was a gustatory experience.

        The Lido legacy continues until today. For more than 80 years, Lido has delivered legendary flavors using the freshest ingredients.
        This has given its patrons a reason to return time and again to take part in a tradition of quality that has been enjoyed by one generation after another.
      </div>
    </div>
  </template>

<script>
export default {
  name: 'About'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .about {
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 2rem;
    justify-content: center;
    padding: 5%;
  }

  @media (max-width: 700px) {
    .about h1 {
      font-size: 1.3rem;
    }

    .about {
      font-size: 12px;
    }
  }
</style>
