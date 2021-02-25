<template>
<div class="points">

  <div v-for="el in info" :key="el.id">

    
     <div class="si-tRow">
            <div class="si-tCel si-Pos"><span>{{el.position}}</span></div>
            <div class="si-tCel si-teamFlag" ><span></span></div>
            <div class="si-tCel si-teamName">
                <span class="si-fullName">{{el.name}}</span>
                <span class="si-shortName">{{el.short_name}}</span>
            </div>
            <div class="si-tCel si-Pld"><span>{{el.sport_specific_keys.events_played}}</span></div>
            <div class="si-tCel si-stnd-won"><span>{{el.sport_specific_keys.wins}}</span></div>
            <div class="si-tCel si-stnd-lost"><span>{{el.sport_specific_keys.lost}}</span></div>
            <div class="si-tCel si-stnd-tied"><span>{{el.sport_specific_keys.tied}}</span></div>
            <div class="si-tCel si-NR"><span>{{el.sport_specific_keys.no_result}}</span></div>
            <div class="si-tCel si-Netrr"><span>{{el.sport_specific_keys.net_run_rate}}</span></div>
            <div class="si-tCel si-Pts"><span>{{el.sport_specific_keys.points}}</span></div>
        </div>
    
  </div>
</div>

</template>

<script>
export default {
  name: "pointsTable",
  props: ["info"],
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>



.si-standingWrap {
 background: blue;
  
}
.si-tCel {
  color: red;
  background: grey;

}



/* @keyframes logo-rotate {
    0% {
      transform: skewY(0deg) rotateY(0deg);
    }
    25% {
      transform: skewY(10deg) rotateY(30deg);
    }
    50% {
      transform: skewY(0deg) rotateY(0deg);
    }
    75% {
      transform: skewY(-10deg) rotateY(-30deg);
    }
    100% {
      transform: skewY(0deg) rotateY(0deg);
    }
  } */

/*# sourceMappingURL=kingsPunjab-mc-common.css.map */
</style>
