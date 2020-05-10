<template>
  <div id="about-page" class="page-wrapper about-page content-page">
    <site-hero
      title="[about this site]"
      subtitle="use at your own risk"
      image="/uploads/about-hero.jpg"
    ></site-hero>
    <main-section theme="sidebar-right">
      <template v-slot:default>
        <div class="content">
          <h3>about this site</h3>
          <p>
            Little blurb about the site here. Link to first post
          </p>

          <h3>about me</h3>
          <p>
            Little blurb about me here.
          </p>
          <quote-card />
        </div>
      </template>

      <template v-slot:sidebar>
        <h3 class="subtitle is-4">
          Latest Posts
        </h3>
        <posts-grid :per-row="1" :number="2" />
      </template>
    </main-section>
  </div>
</template>
<script>
import QuoteCard from '~/components/cards/QuoteCard'
export default {
  head() {
    return {
      title: `About | ${this.$siteConfig.siteName}`
    }
  },
  components: { QuoteCard }
}
</script>
