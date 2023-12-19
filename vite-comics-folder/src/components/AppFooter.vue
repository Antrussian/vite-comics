<template>
  <div class="row">

  <section class="navbar-container d-flex col-12 ">

      <nav class="d-flex wrap column container col-10">
          <div class="nav-item" v-for="navSection in navSections">
              <span class="text-uppercase title">{{ navSection.title }}</span>
              <ul class="col-12 text-start m-0 p-0">
                  <li v-for="navItem in navSection.navItems"><a href="#" :alt="navItem">{{ navItem }}</a></li>
              </ul>
          </div>
          <div class="img-container d-flex">
          <img class="img-footer" src='../assets/img/dc-logo-bg.png' alt="img-footer">
        </div>
      </nav>



  </section>
</div>
</template>
  
  <script>
  
  export default {
    name: 'AppFooter',
    data() {
        return {
            navSections: [
                {
                    title: 'Dc Comics',
                    navItems: [
                        'Characters',
                        'Comics',
                        'Movies',
                        'TV',
                        'Games',
                        'Videos',
                        'News',
                    ]
                },

                {
                    title: 'Shop',
                    navItems: [
                        'Shop DC',
                        'Shop DC Collectibles',
                    ]
                },

                {
                    title: 'DC',
                    navItems: [
                        'Terms of Use',
                        'Privacy policy(new)',
                        'Ad Choices',
                        'Advertising',
                        'Jobs',
                        'Subscriptions',
                        'Talent Workshops',
                        'CPSC Certificates',
                        'Ratings',
                        'Shop Help',
                        'Contact Us',
                    ]
                },

                {
                    title: 'Sites',
                    navItems: [
                        'DC',
                        'MAD Magazines',
                        'DC Kids',
                        'DC Universe',
                        'DC Power Visa',
                    ]
                },
            ]
        }
    }
}



  </script>
  
  <style scoped lang="scss">
@use '../styles/partials/variables' as *;




.navbar-container {
    background-image: url('../assets/img/footer-bg.jpg');
    background-repeat: no-repeat;
    background-size: cover;
   
    width: 100%;
    


    &.container {
        padding-top: 0;
        padding-bottom: 0;
    }

    .img-footer {

        background-repeat: no-repeat;
        background-size: contain;
        background-position: left;
        width: 60%;
        height: 500px;
       

        

    }

    .img-container{
      display: flex;
      width: 100%;
      height: 300px;
      justify-content: center;
      align-items: center;
    }

    nav {
        padding: 2rem 1rem 2rem 1rem;
    
     

        .nav-item {
            margin: 1rem 0;
            text-align: start;
            width: 200px;

           

            .title {
                font-weight: bold;
             
            }

            li {
                font-size: 0.5rem;
                padding-bottom: 0.2rem;
                

                &:first-of-type {
                    padding-top: 0.7rem;
                }

                a {
                    color: $icon--bg-color;

                    &:hover {
                        color: $primary--color;
                    }
                }
            }
        }
    }
}
</style>