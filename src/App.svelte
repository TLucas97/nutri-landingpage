<script lang="ts">
  import Header from './lib/Header.svelte';
  import HomeBanner from './lib/content/HomeBanner.svelte';
  import HealthBeneficts from './lib/content/HealthBeneficts.svelte';
  import GetHealthy from './lib/content/GetHealthy.svelte';
  import ExpertVideo from './lib/content/ExpertVideo.svelte';
  import AboutMe from './lib/content/AboutMe.svelte';
  import FollowMe from './lib/content/FollowMe.svelte';
  import Plans from './lib/content/Plans.svelte';
  import Footer from './lib/Footer.svelte';
</script>

<main>
  <Header />
  <div class="mt-[6.5em] h-[700vh] flex flex-col space-y-15">
    <HomeBanner />
    <HealthBeneficts />
    <GetHealthy />
    <ExpertVideo />
    <AboutMe />
    <FollowMe />
    <Plans />
    <Footer />
    <div class="w-full h-[25px] bg-white text-center">
      <span class="text-gray-700">Todos os direitos reservados © 2023</span>
    </div>
  </div>
</main>
