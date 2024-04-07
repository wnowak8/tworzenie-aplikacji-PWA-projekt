<script setup lang="ts">
import { FontAwesomeIcon } from "@fortawesome/vue-fontawesome";
import {
   faFacebookSquare,
   faXTwitter,
   faSquareInstagram,
} from "@fortawesome/free-brands-svg-icons";
</script>

<template>
   <footer class="footer">
      <div class="content">
         <div class="footer-links">
            <FooterLinks
               title="poradnik zakupowy"
               :links="{
                  links: [
                     {
                        title: 'Metody płatności',
                        url: '/',
                     },
                     {
                        title: 'Formy dostawy',
                        url: '/',
                     },
                     {
                        title: 'Reklamacje',
                        url: '/',
                     },
                     {
                        title: 'Zwroty, wymiana',
                        url: '/',
                     },
                     {
                        title: 'Kontakt',
                        url: '/',
                     },
                  ],
               }"
            />
            <FooterLinks
               title="zasady i regulaminy"
               :links="{
                  links: [
                     {
                        title: 'Regulamin sklepu',
                        url: '/',
                     },
                     {
                        title: 'Regulamin karty stałego klienta',
                        url: '/',
                     },
                     {
                        title: 'Regulamin karty podarunkowej',
                        url: '/',
                     },
                     {
                        title: 'Saldo karty podarunkowej',
                        url: '/',
                     },
                  ],
               }"
            />
            <FooterLinks
               title="o nas"
               :links="{
                  links: [
                     {
                        title: 'Regulamin sklepu',
                        url: '/',
                     },
                     {
                        title: 'Regulamin karty stałego klienta',
                        url: '/',
                     },
                     {
                        title: 'Regulamin karty podarunkowej',
                        url: '/',
                     },
                     {
                        title: 'Saldo karty podarunkowej',
                        url: '/',
                     },
                  ],
               }"
            />
            <div class="social-box">
               <ul>
                  <li class="links-box-link">
                     <a href="https://www.facebook.com/" target="_blank"
                        ><FontAwesomeIcon size="4x" :icon="faFacebookSquare" />
                     </a>
                  </li>
                  <li class="links-box-link">
                     <a href="https://www.x.com/" target="_blank"
                        ><FontAwesomeIcon size="4x" :icon="faXTwitter" />
                     </a>
                  </li>
                  <li class="links-box-link">
                     <a href="https://www.instagram.com/" target="_blank"
                        ><FontAwesomeIcon size="4x" :icon="faSquareInstagram" />
                     </a>
                  </li>
               </ul>
            </div>
         </div>
      </div>
   </footer>
</template>

<style scoped lang="scss">
.content {
   @media (min-width: 1920px) {
      max-width: 1600px;
   }

   @media (min-width: 768px) {
      box-sizing: border-box;
      margin-left: auto;
      margin-right: auto;
      max-width: 1140px;
      padding-left: 40px;
      padding-right: 40px;
      width: auto;
   }
}

.footer {
   background-color: #fff;
}

.footer-links {
   padding-top: 62px;
   flex-wrap: wrap;
   display: flex;
   justify-content: space-between;
   margin-bottom: 0;
   flex-direction: row;
}

.social-box {
   flex: 1 0 25%;
   max-width: 25%;
   order: 2;
   align-items: flex-start;
   flex-direction: column;
   justify-content: flex-start;
   margin-bottom: 69px;
   padding-right: 0;
   display: flex;
}

.links-box-link {
   letter-spacing: 0.3px;
   font-size: 12px;
   line-height: 1.9;
   margin: 0 34px 0 0;
}

.links-box-link a {
   color: inherit;
}

.social-box ul {
   padding: 0;
   margin: 0;
   list-style: none;
   margin-top: 15px;
   justify-content: flex-start;
   max-width: none;
   margin: 20px 0 0;
   display: flex;
   width: 100%;
}
</style>
