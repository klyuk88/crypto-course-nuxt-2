<template>
  <div>
    <!-- INTRO -->
    <section class="intro" id="intro">
      <div class="container-lg">
        <div
          class="intro__baner bg-set"
          :style="{ backgroundImage: `url('${mainBannerBg}')` }"
        >
        <!-- вставить ссылку на видео -->
        <!-- <video src="~/assets/ocean .mp4" class="intro-video" autoplay muted crossorigin playsinline></video> -->
          <div class="intro__shadow">
            <div class="intro__offer">
              <div class="intro__video-btn course">
                <img src="~/assets/img/intro/video-btn.svg" alt="video-btn" />
              </div>
              <h1 class="intro__title section-title">Не повторяйте действия<br> крупного игрока, а станьте им
</h1>
              <span class="intro__subtitle"
                >Место для тех, кто готов выйти на совершенно иной уровень
              </span>
              <!-- <div class="intro__btns">
                <a href="#register" class="intro__btn btn"
                  ><span>Вступить</span></a
                >
              </div> -->
            </div>
          </div>
        </div>
      </div>
    </section>
    <!-- //INTRO -->

    <!-- ADVANTAGES -->
    <section class="advantages" id="advantages">
      <div class="container">
        <h2 class="advantages__title section-title">PRIVATE CLUB <br>Что вы получите</h2>
        <TheCards :triggers="triggers"/>
        <div class="private-lines">
          <nuxt-link to="/profile"><button class="connect-btn">
            <span>ПРИСОЕДИНИТСЯ</span> 
          </button></nuxt-link>
        </div>
      </div>
      <!-- //container -->

      <div class="advantages__star">
        <img
          src="~/assets/img/advantages/advantages-img2.svg"
          alt="right-icon"
        />
      </div>
      <div class="advantages__rhombus">
        <img
          src="~/assets/img/advantages/advantages-img1.svg"
          alt="left-icon"
        />
      </div>
    </section>
    <!-- //ADVANTAGES -->

    <TheInstruction/>


  </div>
</template>

<script>
import mainBannerBg from "~/assets/img/private-club-img.jpg";
export default {
  data() {
    return {
      mainBannerBg,
      triggers: [
        {
          title: "Live Trading",
          about:
            "Приватный канал с реал-тайм трейдингом, торговой системой и чатом практиков. Это экосистема активного извлечения прибыли из рыночных неэффективностей.",
        },
        {
          title: "Academy",
          about:
            "Курс обучения прогрессивному трейдинга с дополнительными привелегиями - своевременной обратной связью от наставника и поддержкой в выполнении домашних заданий.",
        },
        {
          title: "Аналитика",
          about:
            "Долгосрочные инвестидеи, сбор портфелей, pre-sale проекты, diamond монеты на ранних стадиях. Общение и обмен опытом с трейдерами и крупными инвесторами.",
        },
        {
          title: "Эксклюзив",
          about:
            "Возможность тестирования наших передовых разработок в области алгоритмических торговых систем, ботов и копитрейдинга, а также участие в оффлайн мероприятиях.",
        },
      ],
    };
  },
};
</script>