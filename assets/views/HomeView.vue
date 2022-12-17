<script>
export default {
  mounted() {
    document.querySelectorAll('header > button').forEach((button) => {
      button.addEventListener('click', () => {
        if(document.querySelector('.active')){
          document.querySelector('.active').classList.remove('active')
        }
        button.classList.add('active')
        document.querySelectorAll('section > article').forEach((article) => {
          if(article.classList.contains(button.textContent.toLowerCase())){
            article.classList.remove('hidden')
          }else if(button.textContent.toLowerCase() == 'voir tout'){
            article.classList.remove('hidden')
          }else{
            article.classList.add('hidden')
          }
        })
      })
    })

    let dialog = document.querySelector('dialog');
    let testArray = {url: 'https://www.dropbox.com/s/54cod9y08lsuk7c/SCENE.mp4?dl=1', desc: 'LE CAMEMBERT'}

    document.querySelectorAll('section > article').forEach((article) => {
      article.addEventListener('click', () => {
        dialog.innerHTML = '<video src="'+ testArray.url +'" loop controls></video><p>' + testArray.desc + '</p>'

        dialog.showModal()
        document.querySelector('body').style.overflowY = 'hidden'
      })
    })
    dialog.addEventListener('click', (event) => {
      if(event.target === dialog){
        dialog.close()
        document.querySelector('body').style.overflowY = 'scroll'
      }
    })
  },
}
</script>


<template>
  <header>
    <button class="active">Voir tout</button>
    <button>Print</button>
    <button>Web</button>
    <button>Video</button>
    <button>Illustrations</button>
    <button>3D</button>
    <button>Photos</button>
  </header>
  <section>
    <article class="photo web" style="--text: ''">
      <img loading="lazy" src="https://i.imgur.com/O7X0ZED.gif" alt="">
    </article>
    <article class="album print" style="--text: ''">
      <img loading="lazy" src="https://ucff2fa7b5b79bcd9ec3901fa093.previews.dropboxusercontent.com/p/thumb/ABoGNU7FE2h_M94YVxq1094OuMK7LA0jxFgn16XVAQETu1nf7ZQmVvV915cDkg_yF1rbwylCira3a_Ahnm5sVzc7VDZSvfkdHcHClXLG-okMFbZrYtsV18K3g3MPpdfX4IPvzOj2ZaBh34SfTSJyRnQqHlNz8uJZg_YMvFjcM3zC9UsTMxl3xkAbFEKj7yLbqlatwqTCerTULqQCxquhDiDKTX92rPxMHSMQC2n7sBlokpYm_BTtgLM3zPBqEg6vGEyImLSSt0MtSuhxaohIMUTesFJBbilxsh22xC6atkvG0VxNNDxAsT7X4qrMKNhGU3y5DySBVnZXRA-gGx4dkfh0888keIvhuEHXFJKr163imjoYmXUcxvIOonP2E48cwZw/p.jpeg" alt="">
    </article>
    <article class="video" style="--text: 'LE CAMEMBERT';">
      <video src="https://www.dropbox.com/s/54cod9y08lsuk7c/SCENE.mp4?dl=1" autoplay muted loop></video>
    </article>
    <article style="--text: ''"></article>
    <article style="--text: ''"></article>
    <article style="--text: ''"></article>
    <article style="--text: ''"></article>
    <article style="--text: ''"></article>
    <article style="--text: ''"></article>
    <article style="--text: ''"></article>
    <article style="--text: ''"></article>
    <article style="--text: ''"></article>
    <article style="--text: ''"></article>
    <article style="--text: ''"></article>
    <article style="--text: ''"></article>
    <article style="--text: ''"></article>
    <article style="--text: ''"></article>
    <article style="--text: ''"></article>
    <article style="--text: ''"></article>
    <article style="--text: ''"></article>
    <article style="--text: ''"></article>
    <article style="--text: ''"></article>
    <article style="--text: ''"></article>
    <article style="--text: ''"></article>
    <article style="--text: ''"></article>
    <article style="--text: ''"></article>
  </section>
  <dialog>

  </dialog>
</template>

<style scoped>
header{
  padding: 1rem 3rem;
  /* background: #FFFFFF50; */
  margin-bottom: 5rem;
}
header button{
  position: relative;
  padding: 1rem 2rem;
  background: none;
  border: none;
  color: var(--color-text);
  border-left: 1px solid currentColor;
}
header button:first-child{
  border: none;
}
/* header button:hover{
  TROUVER ANIMATION
} */
header .active + button{
  border-left: none;
}
header button.active{
  color: var(--color-active);
  border-right: 1px solid currentColor;
}
header button:last-child{
  border-right: none;
}
header button.active::before, header button.active::after{
  width: 100%;
  transition: width .3s;
}

section{
  width: 70%;
  padding-bottom: 2rem;
  display: grid;
  grid-template-columns: 2, 1fr;
  grid-auto-rows: 35rem;
  grid-auto-flow: dense;
  grid-gap: 2rem;
}
article{
  position: relative;
  isolation: isolate;
  width: calc(35vw - 1.5rem);
  position: relative;
  background: var(--color-logo);
  overflow: hidden;
}
article.hidden{
  display: none;
}
article:nth-child(6n+1){
  grid-column: 2;
  grid-row: span 2;
}
article:nth-child(6n+4) {
  grid-column: 1;
  grid-row: span 2;
}

/* article:not(.active){
  display: none;
} */

article::after{
  content: var(--text);
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  z-index: 2;
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  color: #000;
  font-size: 50px;
  font-weight: 700;
  background: #FFA200;
  opacity: 0;
  transition: .3s linear;
}
article::before{
  position: absolute;
  top: 10px;
  right: 10px;
  z-index: 1;
  padding: 8px;
  width: 40px;
  height: 40px;
  background: #00000050;
  transition: opacity .3s linear;
}
article::before, article::after{
  pointer-events: none;
}
article:hover::before{
  opacity: 0;
  transition: opacity .3s linear;

}
article:hover::after{
  width: calc(100% - 5rem);
  height: calc(100% - 5rem);
  opacity: .7;
  transition: .3s linear;
}

article img, article video{
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: scale .1s linear;
}

article:hover img, article:hover video{
  scale: 1.05;
  transition: scale .1s linear;
}

.album::before{
  content: url(@/img/album.svg);
}
.image::before{
  content: url(@/img/image.svg);
}
.video::before{
  content: url(@/img/video.svg);
  padding-left: 9.5px;
  padding-right: 6.5px;
}

.video.active{
  position: absolute;
  top: 0;
  left: 0;
  transition: 1s ease-in-out;
  background: none;
  z-index: 99;
  width: 100%;
  height: auto;
}
.desc{
  display: none;
  padding-inline: 150px;
  color: var(--color-active);
  text-align: justify;
}

.active .desc{
  display: block;
}
.active::after, .active::before{
  display: none;
}
h1{
  font-size: 50px;
  color: currentColor;
}

dialog{
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: max-content;
  height: max-content;
  max-width: 50vw;
  max-height: 50vh;
  padding: 0;
  border: 0;
  overflow: visible;
  background: none;
}
dialog::backdrop{
  background: #00000050;
  backdrop-filter: blur(20px);
}
</style>
