<template>
  <div id="panolens-container" />
</template>

<script>
export default {
  name: 'panolens',
  props: {
    source: {
      type: String
    },
  },
  mounted() {
    // Load threejs
    let threejsScript = document.createElement('script')
    threejsScript.setAttribute('src', 'https:///cdnjs.cloudflare.com/ajax/libs/three.js/105/three.js')
    threejsScript.onload = () => {
      let panolensjsScript = document.createElement('script')
      panolensjsScript.setAttribute('src',"https:////cdn.jsdelivr.net/npm/panolens@0.11.0/build/panolens.min.js")
      panolensjsScript.onload = () => {
        const container = document.querySelector('#panolens-container')
        const panorama = new PANOLENS.ImagePanorama(this.source)
        const viewer = new PANOLENS.Viewer({ container: container })
        viewer.add( panorama )
      }
      document.head.appendChild(panolensjsScript) 
    }
    document.head.appendChild(threejsScript)
  }    
}
</script>
