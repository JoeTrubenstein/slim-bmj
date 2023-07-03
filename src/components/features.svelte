<script>


  let features = [
  {
    title: "Design",
    description:
      "Polish an existing project or start from scratch. All you need is a basic idea",
    icon: "fa-solid fa-compass-drafting",
  },
  {
    title: "Develop",
    description:
      "Hand-coding means having complete control over every moving part. I use the highest-rated web frameworks available to achieve what page builders can't.",
    icon: "bx:bxs-window-alt",
  },
  {
    title: "Deploy",
    description:
      "Send your idea out in the world with managed and reliable hosting. Utilize advanced SEO and analytic tools to take a data-driven approach to growing your online presence. ",
    icon: "bx:bxs-data",
  }
];
</script>

<section class="md:pt-6 md:pb-24 lg:px-12  px-4 pt-2">
  <div class="mt-16 md:mt-0">
    <h2 class="text-4xl lg:text-5xl font-bold lg:tracking-tight text-primary-500 dark:text-white">
      Everything you need to build an online presence
    </h2>
    <p class="text-lg mt-4">
      A data-driven approach that favors speed, security, and simplicity.
    </p>
  </div>
  
  <div class="grid sm:grid-cols-2 md:grid-cols-3 mt-16 gap-16">

    {#each features as item}
    <div class="flex gap-4 items-start">
        <div class="mt-1 bg-primary-500 dark:bg-white rounded-full p-2 w-8 h-8 shrink-0 flex items-center justify-center">
          <i class={`${item.icon} text-white`}></i>
        </div>
        <div>
          <h3 class="font-semibold text-lg">{item.title}</h3>{" "}
          <p class="mt-2 leading-relaxed">{item.description}</p>
        </div>
      </div>
    {/each}

  </div>
</section>
