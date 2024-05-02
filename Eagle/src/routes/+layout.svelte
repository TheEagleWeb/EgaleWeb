<script>
    import "../app.css";
    import Navbar from '../Components/Navbar.svelte';
    import Gallery_Team from '../Components/Gallery_Team.svelte'
    import TestimonialCard from '../Components/TestimonialCard.svelte'
    import Footer from '../Components/Footer.svelte'
    import Contact from '../Components/Contact.svelte'
    import Hero from '../Components/hero_sec.svelte'
    import Service from '../Components/Service.svelte'
  </script>
  
  <slot />
  <Navbar />
  <Hero />
  <Service />
  <Gallery_Team />
  <TestimonialCard />
  <Contact />
  <Footer />
