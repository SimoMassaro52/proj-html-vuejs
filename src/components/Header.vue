<template>
  <header>

      <!-- TIMER SUB SECTION -->
      <section id="timer" class="d-flex justify-content-center">
          <div id="clock" class="d-flex align-items-center justify-content-between">
              <span>Starts TOMORROW! Our biggest event of the year...</span>
              <span class="mx-3"><i class="bi bi-clock"></i> 00 : 00 : 00 : 00</span>
          </div>
          <div class="d-flex align-items-center px-5">
              <div class="custom_btn">
                  <span>Get ticket</span>
              </div>
          </div>
      </section>

        <!-- NAV -->
      <nav class="d-flex align-items-center">
      </nav>
  </header>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
@import '@/assets/style/variables.scss';

/*TIMER SUB SECTION*/
#timer{
    background-color: $silver;
    height: 50px;
}

#clock{
    span:first-child{
        color: $boulder;
    }
}

.custom_btn{
    background-color: $button-orange;
    color: white;
    padding: 5px 30px;
    border-radius: 5px;
    font-weight: 700;
    cursor: pointer;
}

/*NAV*/



</style>