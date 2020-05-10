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
			The full background in all its glory about why I started this site please read my first post <a href = https://www.scriptbased.com/welcome-to-script-based>here</a> 
          </p>
          <h3>about me</h3>
          <p>
The personal bit:<br> 
After being born and raised in The Netherlands, and living in London for a few years, moved to Florida in 2008. 
<br>
Some "trivia" about me:
<ul>
<li>I enjoy doing government paperwork (they're like complex puzzles and the challenge is to solve those... The rewards? Well...)</li>
<li>Almost all things in my home can be voice controlled or through a wall-mounted touch screen</li>
<li>Favorite movie: Back to the Future (trilogy)</li>
<li>Favorite color: orange</li>
<li>Random: you're never too old for Lego</li>
</ul>
The professional bit:
Professionally it has mostly been Citrix, since I spend the majority of my career there (close to 19 years). Mostly had roles in Sales Engineering or SE related as well as a few Product roles. I decided to leave Citrix in September, because I was missing the culture that you can really only find in smaller organizations: short lines of communication, less internal meetings, less rules and making a direct impact on the success of a company. And that eventually led me to ControlUp and I can't express how excited I am to get back into the field and do it with such a talented group of people!"
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
