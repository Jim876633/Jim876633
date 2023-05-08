<script src="https://code.jquery.com/jquery-3.6.0.min.js"></script>
<script src="https://cdn.jsdelivr.net/npm/jquery.hover3d"></script>

<div class="card-content">
  <div class='card'> 
    <a href="https://app.daily.dev/jim_huang" >
      <img id='my-image'src="https://api.daily.dev/devcards/3c097dbfcea84f16854da704c6315805.png?r=phw" width="400" alt="Jim's Dev Card"/>
    </a>
  </div>
</div>
<!-- <div class='card-content'>
  <img src='https://picsum.photos/200/300' id='my-image' class='card'/>
</div> -->

<style>
.card-content{
  perspective: 1000px;
  transform-style: preserve-3d;
  width: 100vw;
  height: 100vh;
  padding: 10rem;
}
.card {
  transform: translateZ(0);
  transform-style: preserve-3d;
  backface-visibility: hidden;
  box-shadow: 0 0 5px rgba(0, 0, 0, 0.1);
  position: relative;
}
</style>

<script>
  const card = $(".card");
  const cardContent = $(".card-content");

  cardContent.on("mousemove", function (e) {
      var ax = -($(window).innerWidth() / 2 - e.pageX) / 20;
      var ay = ($(window).innerHeight() / 2 - e.pageY) / 10;
      card.attr(
          "style",
          "transform: rotateY(" +
          ax +
          "deg) rotateX(" +
          ay +
          "deg);-webkit-transform: rotateY(" +
          ax +
          "deg) rotateX(" +
          ay +
          "deg);-moz-transform: rotateY(" +
          ax +
          "deg) rotateX(" +
          ay +
          "deg)"
      );
  });
</script>
