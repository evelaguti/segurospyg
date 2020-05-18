<template>
  <div>
    <navbar></navbar>
    <whatsapp></whatsapp>
    <jumbotron></jumbotron>
    <motto title="Nuestro compromiso es proteger lo mas valioso de tu vida."/>
    <carousel/>
    <services v:on:childToParent="onClickService"/>
    
    <contact/>
    <futer/>
  </div>
</template>

<script>
import Navbar from "../components/navbar.vue";
import Jumbotron from "../components/jumbotron.vue";
import Whatsapp from "../components/whatsapp.vue";
import Motto from "../components/motto.vue";
import Carousel from "../components/carousel.vue";
import Services from "../components/services.vue";
import Detail from "../components/detail.vue";
import Contact from "../components/contact.vue";
import Futer from "../components/futer.vue";
export default {
  name: "app",

  data() {
    return {
      desdeServicio: {}
    };
  },

  components: {
    Navbar,
    Jumbotron,
    Whatsapp,
    Motto,
    Carousel,
    Services,
    Contact,
    Detail,
    Futer,
  },
  methods: {
    onClickService(value) {
      this.desdeServicio = value;
    },
  },
};

function iframeAutoScale() {
  "use strict";

  var iframes = document.getElementsByTagName("iframe"),
    index = 0;

  if (iframes.length > 0) {
    for (index = 0; index < iframes.length; index++) {
      var iframe = iframes[index],
        parent = iframe.parentElement,
        parentPadding =
          parseInt(
            window
              .getComputedStyle(parent, null)
              .getPropertyValue("padding-left")
          ) +
          parseInt(
            window
              .getComputedStyle(parent, null)
              .getPropertyValue("padding-right")
          ),
        parentWidth = parent.clientWidth - parentPadding,
        ratio = 0.75, // default ratio (4:3)
        width = iframe.clientWidth,
        height = iframe.clientHeight;

      // overwrite default ratio if width and height attributes are not set
      if (width !== undefined && height !== undefined) {
        ratio = height / width;
      }

      iframe.setAttribute("width", parentWidth);
      iframe.setAttribute("height", parentWidth * ratio);
    }
  }
}
// onload
document.addEventListener(
  "DOMContentLoaded",
  function() {
    iframeAutoScale();
  },
  false
);
// on window resize
window.onresize = function(event) {
  iframeAutoScale();
};

$(document).ready(function() {
  // Add smooth scrolling to all links in navbar + footer link
  $(".navbar a, footer a[href='#myPage']").on("click", function(event) {
    // Make sure this.hash has a value before overriding default behavior
    if (this.hash !== "") {
      // Prevent default anchor click behavior
      event.preventDefault();

      // Store hash
      var hash = this.hash;

      // Using jQuery's animate() method to add smooth page scroll
      // The optional number (900) specifies the number of milliseconds it takes to scroll to the specified area
      $("html, body").animate(
        {
          scrollTop: $(hash).offset().top,
        },
        900,
        function() {
          // Add hash (#) to URL when done scrolling (default click behavior)
          window.location.hash = hash;
        }
      );
    } // End if
  });

  $(window).scroll(function() {
    $(".slideanim").each(function() {
      var pos = $(this).offset().top;

      var winTop = $(window).scrollTop();
      if (pos < winTop + 600) {
        $(this).addClass("slide");
      }
    });
  });
});
</script>
