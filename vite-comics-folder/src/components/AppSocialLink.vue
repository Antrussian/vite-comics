<template>
  <footer class="row">
    <section class="col-12 social-links">
      <div class="d-flex container-footer">

      <div class="container-social-link">      
        <a href="#" class="btn text-uppercase align-center">Sign-Up Now!</a>
     </div>

      <div> <span class="text-uppercase">Follow Us</span></div>
      <div> 
         <ul class="d-flex">
                <li v-for="socialLink in socialLinks"><a href="#"><img :src="getImgPath(socialLink.url)"
                            :alt="socialLink.description + '\'s icon'" :title="socialLink.description + '\'s icon'"></a>
                </li>
            </ul>
      </div>

    </div>
    </section>
  </footer>
</template>

<script>
export default {
    name: 'FooterSocialLinks',

    data() {
        return {
            path: './src/assets/img/footer-',
            socialLinks: [
                {
                    url: 'facebook',
                    description: 'Facebook',
                },


                {
                    url: 'twitter',
                    description: 'Twitter',
                },


                {
                    url: 'youtube',
                    description: 'Youtube',
                },


                {
                    url: 'pinterest',
                    description: 'Pinterest',
                },


                {
                    url: 'periscope',
                    description: 'Google Maps',
                },
            ]
        }
    },

    methods: {
        getImgPath(imgPath) {
            return new URL('../assets/img/footer-' + imgPath + '.png', import.meta.url).href
        }
    }
}
</script>




<style scoped lang="scss">
@use '../styles/partials/variables' as *;

.container-footer {
  width: 100%;
  padding: 1rem 2rem 1rem 2rem;
  justify-content: center;
  align-items: center;
}


.container-social-link {
  width: 50%;
}
.social-links {
    background-color: $lighter--secondary--color;


    a {
        color: $primary--color;
    }

    ul li {
      margin-top: 1rem;
        margin-left: 1rem;

        a:hover {
            filter: brightness(2);
        }
    }

    span {
        font-weight: bold;
        color: $complementary--color;
    }

    .btn {
        padding: 0.7rem;
        border: 2px solid $complementary--color;
        font-size: 0.9rem;
    }
}
</style>