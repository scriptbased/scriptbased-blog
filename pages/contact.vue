<template>
  <div id="contact-page" class="page-wrapper contact-page content-page">
    <site-hero
      title="[contact me]"
      subtitle="places where you can find me"
      image="/uploads/contact-hero.jpg"
    ></site-hero>
    <main-section theme="sidebar-right">
      <template v-slot:default>
        <div class="tile is-ancestor">
          <div class="tile is-parent">
            <article class="tile is-child box">
              <p class="title">
                Hello!
              </p>
              <figure class="image is-1by1">
                <opti-image
                  :src="require('~/assets/uploads/contact-person.jpg').src"
                  :srcset="
                    require('~/assets/uploads/contact-person.jpg').srcSet
                  "
                />
              </figure>
              <br />
              <div class="content">
                <p>
                  If you have any questions about the contents of this site, the easiest way to connect with me is through DM on Twitter, or LinkedIn. Click how you want to connect.
                </p>
              </div>
            </article>
          </div>
          <div class="tile is-parent is-8">
            <article class="tile is-child box">
               <div class="tile is-ancestor">
          <div class="tile is-parent">
            <article class="tile is-child box">
              <p class="title">
                Twitter
              </p>
              <a v-bind:href="https:/twitter.com/joelinthecloud"><p class="subtitle">
                @joelinthecloud
              </p>
              <figure class="image is-1by1">
			                  <opti-image 
                  :src="require('~/assets/uploads/twitter.png').src"
                  :srcset="
                    require('~/assets/uploads/twitter.png').srcSet
                  "
                />
              </figure>
			  </a>
            </article>
          </div>
          <div class="tile is-parent">
            <article class="tile is-child box">
              <p class="title">
                Twitter
              </p>
              <p class="subtitle">
                @scriptbased
              </p>
              <figure class="image is-1by1">
                <opti-image width="500" height="500" />
              </figure>
            </article>
          </div>
          <div class="tile is-parent">
            <article class="tile is-child box">
              <p class="title">
                LinkedIn
              </p>
              <p class="subtitle">
                joelstocker
              </p>
              <figure class="image is-1by1">
                <opti-image width="500" height="500" />
              </figure>
            </article>
          </div>
        </div>
            </article>
          </div>
        </div>
      </template>
      <template v-slot:sidebar>
        <h3 class="subtitle is-4">
          Latest Posts
        </h3>
        <!-- Latest Posts -->
        <posts-grid :per-row="1" :number="2" />
      </template>
    </main-section>
  </div>
</template>
<script>
import ContactForm from '~/components/ContactForm'
export default {
  head() {
    return {
      title: `Contact | ${this.$siteConfig.siteName}`
    }
  },
  components: { ContactForm }
}
</script>
