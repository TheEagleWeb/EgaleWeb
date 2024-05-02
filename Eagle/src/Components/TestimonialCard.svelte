<!-- TestimonialsSlider.svelte -->
<script>
  
  import Swiper from 'swiper';
  import { onMount } from 'svelte';

  const testimonials = [
    {
      name: 'Jane D',
      role: 'CEO',
      avatar: 'https://pagedone.io/asset/uploads/1696229969.png',
      testimonial: 'The user interface of this pagedone is so intuitive, I was able to start using it without any guidance.'
    },
    {
      name: 'Harsh P.',
      role: 'Product Designer',
      avatar: 'https://pagedone.io/asset/uploads/1696229994.png',
      testimonial: 'I used to dread doing my taxes every year, but pagedone has made the process so much simpler and stress-free.'
    },
    // Add more testimonials as needed
  ];

  let mySwiper;

  onMount(() => {
    mySwiper = new Swiper('.swiper-container', {
      loop: true,
      navigation: {
        nextEl: '.swiper-button-next',
        prevEl: '.swiper-button-prev',
      },
    });
  });
</script>

<div class="mx-auto max-w-7xl px-4 sm:px-6 lg:px-8 py-24">
  <div class="flex justify-center items-center gap-y-8 lg:gap-y-0 flex-wrap md:flex-wrap lg:flex-nowrap lg:flex-row lg:justify-between lg:gap-x-8 max-w-sm sm:max-w-2xl lg:max-w-full mx-auto">
      <div class="swiper-container">
          <div class="swiper-wrapper">
              {#each testimonials as testimonial (testimonial.name)} <!-- Here's the change -->
                  <div class="swiper-slide" key={testimonial.name}>
                      <TestimonialCard {...testimonial} />
                  </div>
              {/each}
          </div>
          <div class="swiper-button-prev"></div>
          <div class="swiper-button-next"></div>
      </div>
  </div>
</div>

<style>
  @import 'swiper/swiper-bundle.css';

  .swiper-button-prev,
  .swiper-button-next {
    width: 30px;
    height: 30px;
    background-color: white;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    z-index: 10;
    cursor: pointer;
  }

  .swiper-button-prev:hover,
  .swiper-button-next:hover {
    background-color: #4b5563;
  }
</style>
