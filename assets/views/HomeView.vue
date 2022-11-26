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
    <article class="photo web">
      <img loading="lazy" src="https://ucb8fdffb35da97b677bd86ce209.previews.dropboxusercontent.com/p/thumb/ABr1Sqpv1TTTpBPsB4pr6ceqnAi1IO2HGJCyvP4IpkdF4gEVCl0SuWh-AVqIYWpuh_5hVI2MUJ6bKEXg7HnG5cZ-8VQ82JKs9fTbuikXDbH9Hdwgq-1bLxg4qsK7ZpQ8MdtDFxrSCq_M2bDTTfc4mfhBz2OBCxC3t-9faJAlIgnrID_2--FWePKYZD9y4OWP1VjbvsVeSSJJZSSdRmMjezxj_2WMcdWgvEmNkpcuEFHWc67fa2gmJ6vmi7zI5n9mBHImUHFqmeHm5sxeEutY1fkQ1VErJw3M8VHG2Y1gxnL6gC8p3LyzuhRdlX5Z4zppF-Px4YzlWPmhhNJ6F5KKbNyGXYecAOAfINZYYpzG2U8kVnis3kIhkEmTpc2B3zXA2Sw/p.jpeg" alt="">
    </article>
    <article class="album print">
      <img loading="lazy" src="https://ucff2fa7b5b79bcd9ec3901fa093.previews.dropboxusercontent.com/p/thumb/ABoGNU7FE2h_M94YVxq1094OuMK7LA0jxFgn16XVAQETu1nf7ZQmVvV915cDkg_yF1rbwylCira3a_Ahnm5sVzc7VDZSvfkdHcHClXLG-okMFbZrYtsV18K3g3MPpdfX4IPvzOj2ZaBh34SfTSJyRnQqHlNz8uJZg_YMvFjcM3zC9UsTMxl3xkAbFEKj7yLbqlatwqTCerTULqQCxquhDiDKTX92rPxMHSMQC2n7sBlokpYm_BTtgLM3zPBqEg6vGEyImLSSt0MtSuhxaohIMUTesFJBbilxsh22xC6atkvG0VxNNDxAsT7X4qrMKNhGU3y5DySBVnZXRA-gGx4dkfh0888keIvhuEHXFJKr163imjoYmXUcxvIOonP2E48cwZw/p.jpeg" alt="">
    </article>
    <article class="video">
      <video src="https://www.dropbox.com/s/54cod9y08lsuk7c/SCENE.mp4?dl=1" autoplay muted loop></video>
      <div class="desc">
        <h1>LE CAMEMBERT</h1>
        Lorem, ipsum dolor sit amet consectetur adipisicing elit. Nobis, harum laudantium odit ullam consequuntur voluptatem expedita nulla perspiciatis voluptates quis non accusantium. Ducimus eligendi assumenda nulla architecto. Nemo voluptatum reprehenderit, quam laboriosam aperiam mollitia earum. Ab beatae libero assumenda tempore error ea omnis quis sapiente non ex neque, facere repellendus magnam. Dignissimos, at alias, molestias quidem placeat aliquam obcaecati odio quod labore sed est eligendi omnis accusamus optio assumenda asperiores atque tempore. Accusantium numquam commodi autem odit quam, placeat dolore molestias aliquam nam temporibus ratione cupiditate recusandae obcaecati veritatis debitis qui minima ipsa neque asperiores atque alias quis. Aliquam quibusdam facere neque, vero repellendus repellat corrupti ipsa modi laborum libero? Totam saepe, commodi eligendi iure placeat consectetur sit fuga, obcaecati corrupti ad consequatur molestiae voluptate veniam culpa doloremque repellat officia, alias ipsum! Numquam, vel iusto mollitia quibusdam corrupti corporis nostrum. Quod nesciunt eaque cupiditate minus ipsa quas id quia dignissimos, fugiat laboriosam consectetur quasi ratione repudiandae facere tenetur! Eos repellendus facilis reprehenderit obcaecati ipsam, est possimus quia, eligendi labore suscipit dignissimos excepturi, assumenda iste! Neque ratione itaque dicta hic quidem debitis, eligendi magni quam aut recusandae, amet nobis numquam fuga placeat similique. Nam nostrum amet perspiciatis reiciendis accusamus atque voluptatibus magni! Voluptas nisi est repudiandae dolores, dolor accusantium. Laboriosam possimus assumenda dignissimos commodi expedita totam quis, in placeat temporibus ad iusto soluta ea esse animi qui magnam. Asperiores, ullam saepe nemo dolorem aperiam provident adipisci, est harum praesentium nihil nobis sunt placeat laboriosam ab? Natus, tempore? Et architecto impedit nostrum necessitatibus facere, voluptatibus rem? Placeat officiis quisquam alias? Deleniti possimus repellendus eius voluptas consequuntur quam error dicta magnam. Iste possimus soluta sequi eligendi doloremque veniam id, rem quod minus impedit ipsam provident iusto est in tenetur esse facere laudantium! Laborum vel consequatur error, reprehenderit optio accusantium fugit laudantium obcaecati tenetur excepturi nulla neque dicta inventore. In repellendus laudantium odio, quod, suscipit sint quas provident aut a non dicta quam pariatur maxime id quia tempora fuga eos, distinctio ipsa quasi. Iusto a minima necessitatibus aut voluptate quis reprehenderit rem impedit in ratione quo provident atque commodi debitis minus excepturi, nemo voluptas distinctio itaque voluptatibus autem! Odio ut unde voluptatum obcaecati officiis eaque facere ipsum, labore animi quisquam dolores est non corporis rem, laborum deleniti expedita beatae. Aut itaque illo expedita dicta? Odit quas aperiam delectus quod sequi. Quaerat eaque ex magni exercitationem. Suscipit, nemo sed eveniet fuga perferendis placeat, doloremque amet nisi similique expedita ea explicabo a cupiditate iste officia modi molestias delectus facilis autem impedit ipsam pariatur aperiam nesciunt esse. Repellat quidem ullam veritatis obcaecati optio accusamus omnis vel odio consectetur voluptatibus laboriosam perspiciatis alias rerum eaque minima accusantium, quod ab neque ut cupiditate voluptate? Ducimus, dolores tempora quam voluptates facilis, pariatur inventore consequuntur dignissimos libero laborum non error quibusdam eveniet cupiditate officia esse eius tempore sit? Consequatur, autem consequuntur voluptatum accusamus tempora nostrum officia voluptate quos nihil earum blanditiis. Natus, impedit perferendis hic animi earum necessitatibus? Soluta sint repellendus eius in a iusto enim odit vero deserunt voluptatibus molestias unde, est culpa numquam sed ipsa, cumque necessitatibus optio, consequatur adipisci quia ullam. Maxime enim officia similique nihil quasi ducimus, sequi, placeat excepturi ab autem ipsum. Autem non aliquam eum, nobis eligendi repellat temporibus animi necessitatibus, impedit alias quae neque, laboriosam consectetur totam explicabo nam? Optio inventore et excepturi quae minus temporibus quos corporis iusto, porro officia ratione reprehenderit modi ipsa dolor esse quasi recusandae dolores delectus, iure rem consequuntur veritatis fugiat atque magni. Ut maxime quaerat numquam unde rerum tempora debitis modi veritatis a repellat. Iure cumque tenetur voluptate sit tempora cum. Corporis, voluptas? Sint tempore accusamus commodi at quidem iusto architecto aliquam quo. Saepe odio rerum nemo ducimus beatae. Odit, eos fugiat illum ipsum, id esse ut et quis corrupti quos, provident unde praesentium ipsa. Accusantium obcaecati odit eaque fugit, nesciunt eligendi nulla ut, ex aperiam nihil beatae exercitationem. Dicta repellat tenetur iste molestias eveniet impedit non unde eum, hic itaque ab culpa alias numquam voluptatum pariatur perspiciatis assumenda delectus, officiis quod laborum ut consequuntur excepturi. Amet labore, ad fuga deleniti vero nobis. Dolorum vitae itaque officiis sit fugit cupiditate. Saepe error adipisci tenetur esse, recusandae blanditiis nisi debitis quam asperiores dignissimos accusantium exercitationem cum molestias enim unde assumenda modi natus ipsa explicabo quaerat non eligendi. Molestiae quasi dolores cumque aliquid repudiandae necessitatibus. Beatae, obcaecati perspiciatis. Ipsam ab facere fuga nisi natus? Accusamus voluptatibus dolore officia corrupti, quam asperiores iusto quos provident porro eaque et inventore dolorem repellat, ipsum quis ad fuga rerum error hic ex at est nihil perspiciatis autem! Praesentium iste facilis, pariatur necessitatibus laboriosam harum vel libero nemo ut sit asperiores error amet magnam accusantium voluptas, sint dolorem animi quo doloremque. Quod quaerat sint aliquid, velit, consequatur corporis esse dolores ea, temporibus voluptatem placeat magnam dolorem dolore aut rerum maiores odit cumque dolor laudantium in commodi? Voluptate nesciunt fuga temporibus, aliquid ipsa doloremque tenetur ex harum nostrum nihil suscipit molestiae nulla? Vitae porro ipsa ipsum hic, magnam assumenda ad odit veniam excepturi voluptate praesentium animi repellat id quia cupiditate in atque, labore aspernatur necessitatibus vel maiores quae neque ipsam. Illo, incidunt. Odit, necessitatibus! Mollitia, esse! Harum aspernatur expedita incidunt deleniti id odit necessitatibus corporis ipsa. Consequatur incidunt quod qui dolore fugiat illo vero placeat, velit quibusdam necessitatibus nobis officia corrupti sit sunt tenetur ipsam recusandae libero dolorum natus eligendi blanditiis dolores. Natus blanditiis labore praesentium similique quis fugiat, tempora doloremque error quaerat sint repellat, asperiores nihil minus necessitatibus nostrum eveniet ut a dolores quisquam nemo ea porro. Distinctio sint hic corporis consequatur, culpa quas deleniti rem iste minima vitae doloremque libero quaerat aut cupiditate nemo aliquam consectetur illo odio quibusdam, asperiores iusto vel? Quaerat illo nisi veniam est impedit fuga amet, nesciunt cumque odit, molestias, excepturi ipsa sit nulla assumenda laudantium rerum! Molestias rerum eligendi nulla velit aperiam sequi consequuntur incidunt ullam dolores qui, nemo magnam labore omnis atque cumque, alias nesciunt, veniam nostrum earum fugit mollitia provident voluptatem quam. Veniam saepe unde, perspiciatis maxime repellat, labore necessitatibus totam aperiam quibusdam id provident, obcaecati dolor!
      </div>
    </article>
    <article></article>
    <article></article>
    <article></article>
    <article></article>
    <article></article>
    <article></article>
    <article></article>
    <article></article>
    <article></article>
    <article></article>
    <article></article>
    <article></article>
    <article></article>
    <article></article>
    <article></article>
    <article></article>
    <article></article>
    <article></article>
    <article></article>
    <article></article>
    <article></article>
    <article></article>
    <article></article>
    <article></article>
    <article></article>
    <article></article>
    <article></article>
    <article></article>
    <article></article>
    <article></article>
    <article></article>
    <article></article>
    <article></article>
    <article></article>
    <article></article>
    <article></article>
  </section>
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
header button.active::before, header button.active::after{
  width: 100%;
  transition: width .3s;
}

section{
  width: 70%;
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
  background: #AAA;
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
  content: '';
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  z-index: 2;
  width: 100%;
  height: 100%;
  background: #CD3341;
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
</style>
