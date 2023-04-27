<template>
  <div class="particles">
    <div id="particles-js"></div>
  </div>
</template>

<script>
import 'particles.js'

export default {
  name: 'ParticlesComponent',
  mounted() {
    this.initParticles()
  },
  methods: {
    initParticles() {
      window.particlesJS("particles-js",
        {
          "particles": {
            "number": {
              "value": 50,
              "density": {
                "enable": true,
                "value_area": 800
              }
            },
            "color": {
              "value": "#ffffff"
            },
            "shape": {
              "type": "circle",
              "stroke": {
                "width": 0,
                "color": "#000000"
              },
              "polygon": {
                "nb_sides": 5
              },
              "image": {
                "src": "img/github.svg",
                "width": 100,
                "height": 100
              }
            },
            "opacity": {
              "value": 0.24051180912982842,
              "random": false,
              "anim": {
                "enable": false,
                "speed": 1,
                "opacity_min": 0.1,
                "sync": false
              }
            },
            "size": {
              "value": 3,
              "random": true,
              "anim": {
                "enable": false,
                "speed": 40,
                "size_min": 0.1,
                "sync": false
              }
            },
            "line_linked": {
              "enable": true,
              "distance": 150,
              "color": "#ffffff",
              "opacity": 0.3,
              "width": 1
            },
            "move": {
              "enable": true,
              "speed": 4,
              "direction": "none",
              "random": false,
              "straight": false,
              "out_mode": "out",
              "bounce": false,
              "attract": {
                "enable": false,
                "rotateX": 600,
                "rotateY": 1200
              }
            }
          },
          "interactivity": {
            "detect_on": "canvas",
            "events": {
              "onhover": {
                "enable": false,
                "mode": "repulse"
              },
              "onclick": {
                "enable": true,
                "mode": "repulse"
              },
              "resize": true
            },
            "modes": {
              "grab": {
                "distance": 194.89853095232286,
                "line_linked": {
                  "opacity": 1
                }
              },
              "bubble": {
                "distance": 828.318756547372,
                "size": 93.3888794146547,
                "duration": 0,
                "opacity": 0.13805312609122866,
                "speed": 3
              },
              "repulse": {
                "distance": 121.81158184520177,
                "duration": 0.4
              },
              "push": {
                "particles_nb": 4
              },
              "remove": {
                "particles_nb": 2
              }
            }
          },
          "retina_detect": true
        }
      )
    }
  }
}
</script>

<style scoped>
#particles-js {
  position: absolute;
  background: #050513;
  height: 100%;
  width: 100%;
}
</style>
