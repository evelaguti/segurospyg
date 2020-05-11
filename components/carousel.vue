<template>
    
    <div id="myCarousel" class="carousel slide" data-ride="carousel">
      <!-- Indicators -->
      <ol class="carousel-indicators">
        <li data-target="#myCarousel" data-slide-to="0" class="active"></li>
        <li data-target="#myCarousel" data-slide-to="1"></li>
        <li data-target="#myCarousel" data-slide-to="2"></li>
      </ol>

      <!-- Wrapper for slides -->
      <div class="carousel-inner" role="listbox">
        <div class="item active">
          <img src="images/fam1.jpg" alt="Chania" />
          <div class="carousel-caption">
            <h3>Seguro Familia</h3>
            <p>familia</p>
          </div>
        </div>

        <div class="item">
          <img src="images/son.jpg" alt="Chania" />
          <div class="carousel-caption">
            <h3>Proteccion</h3>
            <p>Proteccion</p>
          </div>
        </div>

        <div class="item">
          <img src="images/teaching.jpg" alt="Flower" />
          <div class="carousel-caption">
            <h3>Seguro Escolar</h3>
            <h1
              style="color: #fff !important;"
            >Cubre hasta los años de universidad, según monto y años contratados.</h1>
            <h1 style="color: #fff !important;">Libre Elección 👏👏👍</h1>
          </div>
        </div>
      </div>

      <!-- Left and right controls -->
      <a class="left carousel-control" href="#myCarousel" role="button" data-slide="prev">
        <span class="glyphicon glyphicon-chevron-left" aria-hidden="true"></span>
        <span class="sr-only">Previous</span>
      </a>
      <a class="right carousel-control" href="#myCarousel" role="button" data-slide="next">
        <span class="glyphicon glyphicon-chevron-right" aria-hidden="true"></span>
        <span class="sr-only">Next</span>
      </a>
    </div>

</template>

<script>
export default {
    
}
</script>