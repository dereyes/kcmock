<template>
  <div class="reveal" id="exampleModal1" data-reveal>
    <h1>Filter songs</h1>
    <!-- <div class="grid-container">
      <div class="grid-x grid-padding-x">
        <div class="small-12 medium-6 cell">
          <label>
            Song name
            <input type="text" placeholder>
          </label>
        </div>
        <div class="small-12 medium-6 cell">
          <label>
            Artist name
            <input type="text" placeholder>
          </label>
        </div>
      </div>
    </div>-->
    <button class="close-button" data-close aria-label="Close modal" type="button">
      <span aria-hidden="true">&times;</span>
    </button>
  </div>
</template>

<script>
export default {
  name: "ModalFilter"
};
</script>