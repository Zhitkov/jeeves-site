<template>
  <v-layout class="full-screen contact" row wrap>
    <v-img cover class="parallax-screen change" dark :lazy-src="bg" cover :src="bg">
      <div class="static">
      <v-flex mx-3>
        <img style="padding-bottom: 42px;" :src="logo">
      </v-flex>
      </div>
    </v-img>
      <v-flex offset-md2 md8 offset-xs1 xs10>
        <p style="font-size: 36px; margin: 50px auto 30px auto" class="neue">Контактная информация</p>
      </v-flex>
    <v-flex offset-md2 md3 offset-xs1 xs10 style="padding-bottom: 20px"> 
      <v-flex xs12 class='contact-container'>
        <div class="vector">
        <svg width="21" height="21" viewBox="0 0 21 21" fill="none" xmlns="http://www.w3.org/2000/svg">
          <path d="M17.0853 11.7299C16.6941 11.3227 16.2224 11.1049 15.7224 11.1049C15.2264 11.1049 14.7506 11.3186 14.3433 11.7259L13.0691 12.9961C12.9643 12.9396 12.8594 12.8872 12.7586 12.8348C12.6135 12.7622 12.4764 12.6937 12.3594 12.6211C11.1659 11.863 10.0812 10.8751 9.04085 9.59685C8.53681 8.95975 8.1981 8.42345 7.95213 7.87909C8.28278 7.57667 8.58923 7.26215 8.88762 6.95973C9.00053 6.84683 9.11343 6.72989 9.22634 6.61699C10.0731 5.7702 10.0731 4.67342 9.22634 3.82664L8.12552 2.72582C8.00052 2.60082 7.87148 2.47179 7.75051 2.34275C7.50858 2.09275 7.25454 1.83468 6.99244 1.59275C6.60131 1.20565 6.13356 1 5.64162 1C5.14969 1 4.67387 1.20565 4.27064 1.59275C4.26661 1.59678 4.26661 1.59678 4.26258 1.60081L2.8916 2.98389C2.37547 3.50002 2.08111 4.12906 2.01659 4.85891C1.91982 6.03634 2.26659 7.13312 2.53273 7.85087C3.18596 9.61298 4.16177 11.2461 5.61743 12.9961C7.38358 15.105 9.5086 16.7703 11.936 17.9437C12.8635 18.3832 14.1014 18.9034 15.4845 18.9921C15.5691 18.9961 15.6578 19.0002 15.7385 19.0002C16.67 19.0002 17.4522 18.6655 18.0651 18.0002C18.0692 17.9921 18.0772 17.9881 18.0813 17.98C18.2909 17.726 18.5329 17.4961 18.7869 17.2501C18.9603 17.0848 19.1377 16.9114 19.3111 16.73C19.7103 16.3147 19.92 15.8308 19.92 15.3348C19.92 14.8348 19.7063 14.355 19.299 13.9517L17.0853 11.7299ZM18.5288 15.9759C18.5248 15.9759 18.5248 15.98 18.5288 15.9759C18.3716 16.1453 18.2103 16.2985 18.0369 16.4679C17.7748 16.7179 17.5087 16.98 17.2587 17.2743C16.8514 17.7098 16.3716 17.9155 15.7425 17.9155C15.682 17.9155 15.6175 17.9155 15.557 17.9114C14.3594 17.8348 13.2465 17.3671 12.4118 16.9679C10.1296 15.863 8.12552 14.2945 6.46018 12.3066C5.08517 10.6493 4.16581 9.11701 3.55693 7.47183C3.18193 6.46779 3.04483 5.68553 3.10531 4.94762C3.14563 4.47584 3.32709 4.08471 3.66177 3.75002L5.03678 2.37501C5.23436 2.18953 5.44404 2.08872 5.64969 2.08872C5.90372 2.08872 6.10937 2.24195 6.2384 2.37098C6.24244 2.37501 6.24647 2.37904 6.2505 2.38308C6.49647 2.61292 6.73034 2.85082 6.97631 3.10486C7.10132 3.23389 7.23035 3.36292 7.35938 3.49599L8.4602 4.59681C8.88762 5.02423 8.88762 5.41939 8.4602 5.84682C8.34326 5.96375 8.23036 6.08069 8.11342 6.19359C7.77471 6.54037 7.45213 6.86296 7.10132 7.17747C7.09325 7.18554 7.08519 7.18957 7.08115 7.19764C6.73438 7.54441 6.79889 7.88313 6.87147 8.11297C6.87551 8.12506 6.87954 8.13716 6.88357 8.14926C7.16986 8.84281 7.57309 9.49604 8.186 10.2743L8.19004 10.2783C9.30295 11.6493 10.4763 12.7178 11.7707 13.5364C11.936 13.6412 12.1054 13.7259 12.2667 13.8066C12.4118 13.8791 12.5489 13.9477 12.6659 14.0203C12.682 14.0283 12.6981 14.0404 12.7143 14.0485C12.8514 14.1171 12.9804 14.1493 13.1135 14.1493C13.4481 14.1493 13.6578 13.9396 13.7264 13.8711L15.1054 12.492C15.2425 12.3549 15.4603 12.1896 15.7143 12.1896C15.9643 12.1896 16.1699 12.3469 16.2949 12.484C16.299 12.488 16.299 12.488 16.303 12.492L18.5248 14.7138C18.9401 15.1251 18.9401 15.5485 18.5288 15.9759Z" fill="#136CE2"/>
        </svg>
      </div>
        <p class="thin contacts">8 800 550 39 34</p>
      </v-flex>
      <v-flex xs12 class='contact-container'>
        <div class="vector">
        <svg width="18" height="18" viewBox="0 0 18 18" fill="none" xmlns="http://www.w3.org/2000/svg">
          <g clip-path="url(#clip0)">
            <path d="M15.8026 2.15039H2.20112C0.986965 2.15039 0 3.13736 0 4.35151V13.6476C0 14.8618 0.986965 15.8487 2.20112 15.8487H15.7989C17.013 15.8487 18 14.8618 18 13.6476V4.35523C18.0037 3.14108 17.0168 2.15039 15.8026 2.15039ZM16.9981 13.6476C16.9981 14.3068 16.4618 14.8431 15.8026 14.8431H2.20112C1.5419 14.8431 1.00559 14.3068 1.00559 13.6476V4.35523C1.00559 3.69601 1.5419 3.1597 2.20112 3.1597H15.7989C16.4581 3.1597 16.9944 3.69601 16.9944 4.35523V13.6476H16.9981Z" fill="#136CE2"/>
            <path d="M11.3522 8.88425L15.7544 4.9364C15.9593 4.75018 15.9779 4.4336 15.7917 4.22504C15.6054 4.02019 15.2889 4.00157 15.0803 4.18779L9.00953 9.63658L7.82518 8.57885C7.82145 8.57513 7.81773 8.5714 7.81773 8.56768C7.79166 8.54161 7.76559 8.51926 7.73579 8.49692L2.91642 4.18407C2.70786 3.99785 2.39128 4.01647 2.20506 4.22504C2.01884 4.4336 2.03747 4.75018 2.24603 4.9364L6.70041 8.91777L2.26465 13.0705C2.06354 13.2604 2.05236 13.577 2.24231 13.7818C2.34287 13.8861 2.47694 13.942 2.61102 13.942C2.73393 13.942 2.85683 13.8973 2.95367 13.8079L7.45646 9.59561L8.67806 10.6869C8.7749 10.7725 8.89408 10.8135 9.01326 10.8135C9.13244 10.8135 9.25534 10.7688 9.34845 10.6831L10.6036 9.55837L15.0803 13.8116C15.1771 13.9047 15.3038 13.9494 15.4267 13.9494C15.5607 13.9494 15.6911 13.8973 15.7917 13.793C15.9816 13.5919 15.9742 13.2716 15.773 13.0816L11.3522 8.88425Z" fill="#136CE2"/>
          </g>
          <defs>
            <clipPath id="clip0">
              <rect width="18" height="18" fill="white"/>
            </clipPath>
          </defs>
        </svg>
      </div>

        <p class="thin contacts">E-mail: info@slv24.ru</p>
      </v-flex>
      <v-flex xs12 class='contact-container'>
        <div class="vector">
        <svg width="18" height="18" viewBox="0 0 16 18" fill="none" xmlns="http://www.w3.org/2000/svg">
  <path fill-rule="evenodd" clip-rule="evenodd" d="M7.00118 0.000603042C6.98739 -7.2142e-05 6.97345 -0.000184691 6.9594 0.000287265C4.12172 0.0955983 2.37059 1.32302 1.33849 2.78723C0.32417 4.22621 0.0264506 5.85894 0.00123974 6.78404C-0.0201531 7.56904 0.238392 8.47651 0.538774 9.25588C0.843646 10.0469 1.21508 10.7649 1.46878 11.1916L1.48492 11.2188L1.50436 11.2437L6.62856 17.8113C6.79843 18.029 7.11262 18.0678 7.33034 17.8979C7.39202 17.8498 7.43933 17.7901 7.47162 17.7242L12.4945 11.2424L12.5134 11.2181L12.5291 11.1916C12.7828 10.7649 13.1542 10.0469 13.4591 9.25588C13.7595 8.47651 14.018 7.56905 13.9966 6.78404C13.9713 5.85544 13.6604 4.22266 12.6344 2.78487C11.592 1.32406 9.83296 0.0982587 7.00118 0.000603042ZM7.015 16.6809L11.6849 10.6546C11.9126 10.2679 12.2495 9.61381 12.526 8.89625C12.8134 8.15069 13.0129 7.39377 12.997 6.81128C12.9757 6.03052 12.7044 4.60444 11.8204 3.36573C10.956 2.15441 9.485 1.08926 6.97565 1.00032C4.46682 1.08924 3.00842 2.15385 2.15584 3.36337C1.28353 4.60089 1.02224 6.02702 1.00087 6.81128C0.984994 7.39377 1.18452 8.15069 1.47187 8.89625C1.74826 9.61337 2.08489 10.2671 2.31254 10.6539L7.015 16.6809Z" fill="#136CE2"/>
  <path d="M9.12752 6.5395C9.12752 7.76443 8.09414 8.787 6.78227 8.787C5.4704 8.787 4.43701 7.76443 4.43701 6.5395C4.43701 5.31457 5.4704 4.29199 6.78227 4.29199C8.09414 4.29199 9.12752 5.31457 9.12752 6.5395Z" stroke="#136CE2"/>
  </svg>
        </div>
        <p style="width: 282px; line-height: 25px;" class="thin contacts">Главный офис  <span class='blue-text'>JEEVES</span>
  Ул. Заозерная, д. 8, кор. 2 Санкт-Петербург, 196084</p>
      </v-flex>
    </v-flex>
      <v-flex offset-md1 offset-xs1 md1 xs5 class='blue-text'>
        <p class="thin contacts">Клиентам:</p>
        <p class="thin contacts">Партнерам:</p>
        <p class="thin contacts">Маркетинг:</p>
      </v-flex>
      <v-flex md4 xs4>
        <p class="thin contacts">hello@slv24.ru</p>
        <p class="thin contacts">partners@slv24.ru</p>
        <p class="thin contacts">oko@servisvip.ru</p>
      </v-flex>
<v-flex offset-xs2 xs10>
  
      <v-dialog
      v-model="dialog"
      width="500"
    >
        
        <p slot="activator" class="black-underline thin">Оставить отзыв о работе мобильного приложения.</p>
        <p slot="activator" class="black-underline thin">Оставить отзыв об уровне нашего сервиса.</p>

      <v-card>
        <v-card-title
          class="headline lighten-2"
          primary-title
          style="display: flex; justify-content: center;"
        >
          <span class="neue" style="font-size: 38px !important;">Отзыв</span>
           <v-icon @click="dialog = false" class="clear">clear</v-icon>
           <b style="font-size: 20px; text-align: center;">Ваше мнение очень важно для нас, чтобы сделать наш сервис лучше для вас.</b>
        </v-card-title>

        <v-card-text>
            <v-flex xs12 >
              <v-text-field
              class="form-white"
              label="Как к Вам обращаться?"
              outline
              ></v-text-field>
          </v-flex>
            <v-flex xs12 >
              <v-text-field
              class="form-white"
              label="Обратная связь"
              outline
              ></v-text-field>
          </v-flex>
            <v-flex xs12 >
              <v-textarea
          outline
          label="Текст"
        ></v-textarea>
          </v-flex>
        </v-card-text>

        <v-card-actions>
          <v-spacer></v-spacer>
      <v-dialog
              v-model="dialog2"
              width="500"
              >
          <v-btn
            color="primary"
            @click="dialog = false"
            slot="activator"
          >
            Отправить
          </v-btn>




<v-card>
        <v-card-title
          class="headline lighten-2"
          primary-title
          style="display: flex; justify-content: center;"
        >
          <span class="neue" style="font-size: 38px !important;">Спасибо</span>
           <b style="font-size: 21px; line-height: 25px; text-align: center; font-weight: 500;">Давно выяснено, что при оценке дизайна и композиции читаемый текст мешает сосредоточиться.</b>
        </v-card-title>

        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn
            color="primary"
            @click="dialog2 = false"
            slot="activator"
          >
            Завершить
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>




        </v-card-actions>
      </v-card>
    </v-dialog>
</v-flex>



  </v-layout>
</template>

<script>

  export default {
    components: {

    },
    data () {
      return {
        logo: require('../../static/logos/logo2.svg'),
        bg: require('../../static/Contacts/bg.png'),
        dialog: false,
        dialog2: false,
        on: true

      }
    },
  }
</script>

<style lang="stylus" scoped>
.clear
  position absolute 
  right 10px
  top 10px
.blue-text 
  color: #136CE2;
  p 
    color: #136CE2;
  // border-bottom #136CE2 solid 1px
.black-underline
  color #000
  box-shadow: inset 0 0px 0 white, inset 0 -1px 0 black
  display: inline-flex;
  margin-bottom 5px
  display: block;
  &:first-child
    margin-top: 30px
  &:last-child
    margin-bottom: 50px
.contact-container
  display flex
  align-items center
  .vector
    display flex
    align-self end
    justify-self center
    width 20px
    svg
      align-self end
      margin-top 5px
.contacts
  margin-left: 10px;
  margin-bottom: 0
.thin
  font-weight 100 
  font-size 21px
.full-screen
  width 100vw
.parallax-screen
  width 100vw
  height 57vh !important
.container
  align-content: center
  align-items: center
  align-self: center
  display: flex
</style>
<style scoped>
.v-card__actions{
    display: grid;
    justify-items: center;
}
@media screen and (max-width: 900px){
  .First-text{
    font-size: 20px; 
    margin: 5% 10% 1%;
  }
  .parallax-screen{
    height: 100vh !important;
  }
}
</style>
<style>
div[data-v-6a7bb5d0] .v-responsive__content {
  display: flex;
  justify-content: center;
}
.contact .v-image__image{
  box-shadow: inset 10px -30px 150px 30px #000 !important;
}
</style>


