<template>
      <div id="contact" class="container-fluid bg-grey">
      <h2 class="text-center">CONTACTO</h2>
      <div class="row">
        <div class="col-sm-4">
          <iframe
            width="600"
            height="600"
            src="https://maps.google.com/maps?q=Villa%20alemana&t=&z=15&ie=UTF8&iwloc=&output=embed"
            frameborder="0"
            scrolling="no"
            marginheight="0"
            marginwidth="0"
          ></iframe>
        </div>
        <div class="col-sm-3">
          <p>Contactanos y responderemos dentro de 24 horas.</p>
          <p>
            <span class="glyphicon glyphicon-map-marker"></span> Quinta Región, Chile
          </p>
          <p>
            <span class="glyphicon glyphicon-phone"></span> +5691087106
          </p>
          <p>
            <span class="glyphicon glyphicon-envelope"></span> myemail@something.com
          </p>
        </div>
        <div class="col-sm-5 slideanim">
          <div class="row">
            <div class="col-sm-6 form-group">
              <input
                class="form-control"
                id="name"
                name="name"
                placeholder="Nombre"
                type="text"
                required
              />
            </div>
            <div class="col-sm-6 form-group">
              <input
                class="form-control"
                id="email"
                name="email"
                placeholder="Email"
                type="email"
                required
              />
            </div>
          </div>
          <textarea
            class="form-control"
            id="comments"
            name="comments"
            placeholder="Comentario"
            rows="5"
          ></textarea>
          <br />
          <div class="row">
            <div class="col-sm-12 form-group">
              <button class="btn btn-default pull-right" type="submit">Enviar</button>
            </div>
          </div>
        </div>
      </div>
    </div>
</template>

<script>
export default {
    
}
</script>