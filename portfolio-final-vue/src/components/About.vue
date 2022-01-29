<template>
    <section id="About">
    <div class="About">
        <h2>About Me</h2>
        <div class="about-box">
            <div class="about-box-left">
                <img src="https://i.postimg.cc/C55wj67F/closeup-bg.jpg" alt="">
            </div>
            <div class="about-box-right">
                <p>I am servant-hearted, so I'm always looking to help those in need. I'm a people's person and also love working with children. When I set my mind to something, I never give up on it, regardless of how challenging it is. I have a bubbly personality and can often bring life and positive energy to the environments I'm placed in. </p>
                <p>I was always inquisitive as a child, so naturally I wanted to know how everything works, and that's where my interest in building websites and seeing how every function works visually and practically grew from. I also know that technology is the future, as it will always be the most dominant industry, as almost everything in this world revolves around technology.
                </p>
            </div>
        </div>

    </div>
    </section>
</template>

<script>
export default {
  name: 'About',
  components: {

  }
}
</script>

<style>
#About {
    height: 100vh;
    text-align: center;
}

.About h2{
    padding-bottom: 20px;
}

.about-box{
    display: flex;
    flex-wrap: wrap ;
}

.about-box-left{
    width: 50%;
}

.about-box-left img{
    width: 350px;
    height: 350px;
    clip-path: polygon(60% 0, 58% 0, 23% 76%, 61% 0, 49% 85%, 63% 0, 74% 92%, 0 68%);
    object-position: -50px 10px;
}

.about-box-right {
    width: 50%;
    text-align: left;
}
</style>