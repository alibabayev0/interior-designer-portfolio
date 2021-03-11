<template>
  <div
    :class="[
      'cursor',
      { cursor_hover: hover },
      { cursor_hide: hideCursor },
      { cursor_click: clickCursor }
    ]"
  >
    <div :style="cursorCircle" class="cursor_circle"></div>
    <div class="cursor_point" ref="point" :style="cursorPoint"></div>
    <!--   @mousedown="clickCursor = true"
    @mouseup="clickCursor = false" 
     @mouseover="this.$root.hover = true" 
          @mouseout="this.$root.hover = false"
          -->
  </div>
  <Header />
  <router-view />
  <Footer />
</template>

<script>
import Header from './components/Header'
import Footer from './components/Copyright'
export default {
  data() {
    return {
      miniDotX: 0,
      miniDotY: 0,
      bigDotX: 0,
      bigDotY: 0,
      hover: false,
      hideCursor: true,
      clickCursor: false
    }
  },
  components: {
    Header,
    Footer
  },
  computed: {
    cursorCircle() {
      return `transform: translateX(${this.bigDotX}px) translateY(${this.bigDotY}px) translateZ(0) translate3d(0, 0, 0);`
    },
    cursorPoint() {
      return `transform: translateX(${this.miniDotX - 3}px) translateY(${this
        .miniDotY - 3}px) translateZ(0) translate3d(0, 0, 0);`
    }
  },
  methods: {
    moveCursor(e) {
      this.miniDotX = e.clientX
      this.miniDotY = e.clientY
      setTimeout(() => {
        this.bigDotX = e.clientX - 15
        this.bigDotY = e.clientY - 15
      }, 75)
      this.hideCursor = false
    }
  },
  mounted() {
    document.addEventListener('mousemove', this.moveCursor)

    document.addEventListener('mouseleave', function() {
      this.hideCursor = true
    })

    document.addEventListener('mouseenter', function() {
      this.hideCursor = false
    })
  }
}
</script>

<style lang="css">
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;500;700;800&display=swap');
* {
  cursor: none !important;
}

html,
body {
  margin: 0px !important;
  padding: 0px !important;
  background-color: #eeece5;
}

button,
a {
  outline: none;
}
::-webkit-scrollbar {
  width: 20px;
}

::-webkit-scrollbar-track {
  background-color: transparent;
}

::-webkit-scrollbar-thumb {
  background-color: #1c1c1d;
  border-radius: 20px;
  border: 6px solid transparent;
  background-clip: content-box;
}

p {
  font-family: Poppins, sans-serif;
}

.cursor_hide {
  display: none;
  opacity: 0;
  width: 60px;
  height: 60px;
  transition: width 0.6s ease, height 0.6s ease, opacity 0.6s ease;
}
.cursor_circle {
  pointer-events: none;
  user-select: none;
  top: 0;
  left: 0;
  position: fixed;
  width: 30px;
  height: 30px;
  border: 2px solid #b8b8b8;
  border-radius: 100%;
  z-index: 10000;
  backface-visibility: hidden;
  transition: width 0.6s ease, height 0.6s ease, opacity 0.6s ease,
    margin-top 0.6s ease, margin-left 0.6s ease;
}

.cursor_point {
  top: 0;
  left: 0;
  position: fixed;
  width: 10px;
  height: 10px;
  pointer-events: none;
  user-select: none;
  border-radius: 100%;
  background: #1c1c1d;
  z-index: 1000000;
  backface-visibility: hidden;
  will-change: transform;
  transition: width 0.2s ease, height 0.2s ease, opacity 0.2s ease,
    margin-top 0.2s ease, margin-left 0.2s ease;
}

.cursor_hover .cursor_circle {
  opacity: 0;
  width: 60px;
  height: 60px;
  margin-top: -15px;
  margin-left: -15px;
  transition: width 0.4s ease, height 0.4s ease, opacity 0.4s ease,
    margin-top 0.4s ease, margin-left 0.4s ease;
}

.cursor_click .cursor_point {
  width: 20px;
  height: 20px;
  margin-top: -5px;
  margin-left: -5px;
  transition: width 0.4s ease, height 0.4s ease, margin-top 0.4s ease,
    margin-left 0.4s ease;
}

@media (pointer: none), (pointer: coarse) {
  .cursor {
    display: none;
  }
}
</style>
