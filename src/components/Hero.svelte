<script>
  import SectionWrap from "./SectionWrap.svelte";
  import Header from "./Header.svelte";
  import Cta from "./Cta.svelte";
</script>

<SectionWrap>
  <Header />
  <div
    class="flex flex-col gap-10 flex-1 items-center justify-center pb-10 md:pb-14"
  >
    <h2
      class="text-5xl sm:text-6xl md:text-7xl lg:text-8xl max-w-[1200px] mx-auto w-full text-center font-semibold"
    >
      <span class="text-indigo-400">Gym</span> Training Is
      <span class="text-slate-600 line-through">Hard</span><br />
      Just Got
      <span class="text-indigo-400">Easier</span>
    </h2>
    <p
      class="text-xl sm:text-2xl md:text-3xl text-center max-w-[1000px] mx-auto w-full"
    >
      Less think & more doing. Do <span class="italic"
        >workouts, exercise, analytic</span
      > and much more.
    </p>
    <Cta />
    <div class="flex items-center justify-center gap-2 text-base">
      <p>4.8</p>
      {#each [0, 1, 2, 3, 4] as i}
        <div class="grid place-items-center relative">
          <i class="fa-solid fa-star opacity-0"></i>
          <div
            class={"absolute top-0 left-0 grid place-items-center " +
              (i === 4 ? " w-[80%] overflow-hidden" : " ")}
          >
            <i class="fa-solid fa-star text-amber-400"></i>
          </div>
        </div>
      {/each}
      <p>5000+</p>
    </div>
  </div>
</SectionWrap>
