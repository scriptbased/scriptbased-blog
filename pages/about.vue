<template>
  <div id="about-page" class="page-wrapper about-page content-page">
    <site-hero
      title="[about this blog]"
      subtitle="use at your own risk"
      image="/uploads/about-hero.jpg"
    ></site-hero>
    <main-section theme="sidebar-right">
      <template v-slot:default>
        <div class="content">
          <h3>about this site</h3>
          <p>
            The TL;DR version of what you can expect to find on this site:
			<ul>
			<li>My ramblings and musings about automation, scripting and coding</li>
			<li>Cool things I’ve built, things I’ve “stolen” & modified/enhanced or new things I learned about</li>
			<li>Things I find online from others about scripting and automation</li>
			<li>Memes</li>
			</ul>
			<br>
			The full background in all its glory about why I started this site please read my first post <a href = https://www.scriptbased.com/welcome-to-script-based>here</a> 
          </p>

          <h3>about me</h3>
          <p>
            Little blurb about me here.
          </p>
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
