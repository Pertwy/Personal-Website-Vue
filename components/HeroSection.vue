<template>
    <section class="grid-half">
        <div class="justify-left introduction">
          <h3>Hi, my name is John</h3>
          <p>I’m a Frontend Javascript Web Developer with a background in aerospace engineering.</p>
        </div>
        
        <div>
          <img class="profile-img" src="https://i.pinimg.com/originals/69/20/fc/6920fc266ea0a8bfbb02561dfdd18f1c.png" />
        </div>
      </section>
</template>

<script>
    export default {
        
    }
</script>

<style scoped>
.introduction h1{
  font-size: 28px;
  line-height: 28px;
  margin-bottom: 30px;
  color: #0d0c22;
  font-weight: 500;
}
.introduction p{
  font-size: 36px;
  line-height: 42px;
  margin: 10px 0;
}
.profile-img{
  -webkit-transform: scaleX(-1);
  transform: scaleX(-1);
  opacity: 1;
  border: 0;
  max-width: 100%;
  vertical-align: middle;
  display: inline-block;
}
.grid-half{
  display: grid;
  gap: 20px;
  grid-gap: 30px;
  height: 100%;
  grid-template-columns: 1fr 1fr;
}
@media (max-width: 768px) {
  .grid-half, .grid-three-one, .grid-one-one-one
{
    grid-template-columns: 1fr;
    grid-template-rows: 1fr;
  }
  .grid-one-one-one-one{
    grid-template-columns: 1fr 1fr;
  }

}
</style>