<template>
  <div class="container">
    <img id="avatar" alt="avatar" src="https://pic.downk.cc/item/5e23ae452fb38b8c3c6bb5fb.jpg" />
    <h1>XXXX</h1>
    <h2>🙆‍♂️ 👨‍💻 🙋‍♂️</h2>

    <p>A Level在读 / ‘Apple Device’精神用户 / 情怀文学家</p>
    <p>
      * he is also a Developer of Apple
      <a href="https://developer.apple.com"> 'Develop Program' </a>
    </p>

    <hr id="top-hr" />
    <h3>🎉 Where to find me:</h3>
    <div id="card-container">
      <Card
        msg="博客 Blog"
        backgroundColor="#d62438"
        description="📒 从头开始"
        textColor="#FFFFFF"
        icon="Blog.png"
        link="https://www.patrickzhu.club"
      />
      <Card
        msg="GitHub"
        backgroundColor="#24292E"
        description="📦 我做过的项目都在这里"
        textColor="#FFFFFF"
        icon="github.png"
        link="https://github.com/OOXXXX"
      />
      <Card
        msg="知乎 Zhihu"
        backgroundColor="#2b8bde"
        description="📱 打发闲暇"
        textColor="#FFFFFF"
        icon="zhihu.png"
        link="https://www.zhihu.com/people/stay-alive-31/activities"
      />
    </div>

    <div id="others">
      <hr />
      <h3>你还可以在这些地方偶尔发现一只我：</h3>
      <div class="social-media">
        <div class="social-media-card">
          <img class="media-icon" src="@/assets/CN_bilibiliB.png" alt="bilibili" />
          <span>
            BiliBili:
            <a href="https://space.bilibili.com/284808882">@Zhupx</a>
          </span>
        </div>
        <div class="social-media-card">
          <img class="media-icon" src="@/assets/twitter.png" alt="twitter" />
          <span>
            Twitter:
            <a href="https://twitter.com/Patrick97786517">@Patrick97786517</a>
          </span>
        </div>
      </div>

      

      
      <a href="https://github.com/spencerwooo/portfolio">
        <img src="https://flat.badgen.net/badge/Designed%20by/@SpencerWoo/red" alt="copyright" />
      </a>
    </div>
  </div>
</template>

<script>
import Card from '@/components/Card.vue'

export default {
  components: {
    Card
  }
}
</script>
