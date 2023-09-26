---
theme: dracula
class: text-center
highlighter: shiki
lineNumbers: false
info: 
drawings:
  persist: false
transition: slide-up
title: EDU SSR series SSG
fonts: 
 serif: 'Poppins'
---
# Hi! Thanks for joining.

<v-click>

Today our topic is...

</v-click>

<v-click>

## Unlocking the Power of SSG

</v-click>


---
preload: false
clicks: 4
src: ./pages/plan.md
---
---

<img src="/sponge-bob-sleep.jpeg" class="img-blog" />

---
---

<section class='conditions'>
<div>

# What he want

<v-clicks>

- *SEO* support
- We need *green metrics* for certain pages
- Flexibility that can't be achieved without modern frameworks

</v-clicks>

</div>

<div>

# What he has

<v-clicks>

- Bright mind and enthusiasm <img src="sponge-imagine.webp" class="krabs sponge" />
- Low money budget <img src="Mr._Krabs.svg" class="krabs" />
- Knowledge from this meetup :)<img src="edu_logo.png" class="krabs" />

</v-clicks>

</div>
</section>

<section class="render-options">
  <div class="blalbe">
    <figure class="figure">
      <figure v-click class="red_cross">
        <img src="/Red_X.svg">
        <figcaption>Bad SEO</figcaption>
      </figure>
      <img class="imagessss" src="/React.svg"/>
      <figcaption>Plain CSR framework</figcaption>
    </figure>
  </div>
  <div class="blalbe">
    <figure class="figure">
      <figure v-click class="red_cross">
        <img src="/Red_X.svg">
        <figcaption>Server costs</figcaption>
      </figure>
      <img class="imagessss" src="/Next.svg"/>
      <figcaption>SSR</figcaption>
    </figure>
  </div>
  <div class="blalbe">
    <figure class="figure">
      <figure v-click class="red_cross">
        <img src="/green-check.svg">
        <figcaption>All cool</figcaption>
      </figure>
      <img class="imagessss" src="/Next_SSG.svg"/>
      <figcaption>SSG</figcaption>
    </figure>
  </div>
</section>

<style>
  .conditions{
    display: flex;
    align-items: flex-start;
    justify-content: space-around;
  }
  .render-options {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    gap: 5px;
  }
  .blalbe {
    width: 100%;
    height: 100%;
  }
  .red_cross {
    position: absolute;
    width: 100%;
    height: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 15px; 
  }
  .red_cross img { 
    width: 200px;
    height: 200px;
  }
  .red_cross figcaption { 
    text-align: center;
    width: 200px;
    background: hsl(231, 15%, 18%);
  }
  .figure {
    position: relative;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 15px; 
    margin-top: 15px;
  }
  .imagessss {
    width: 200px;
    height: 200px;
  }
  .krabs {
    width: 30px;
    height: 30px;
    float: right;
  }
  .sponge {
    width: 40px;
  }
</style>

---
clicks: 4
---

# What is it "SSG"? 

<v-click>

Static-site generation(*SSG*) is the process of creating web-pages by pre-generating each page, resulting in really good performance and UX. 

</v-click>

<v-click>
  <ServerGeneration/> 
</v-click>


---
clicks: 12
---

# What Sponge will get from SSG

<v-clicks>

- *SEO* support ✅
- *Green metrics* for certain pages ✅
- No SSR ✅

</v-clicks>

<Crawler v-click></Crawler>

---
preload: false
clicks: 9
src: ./pages/basicFlow.md
---

---
clicks: 17
---

# What we need for SSG

<v-clicks>

- Server to generate HTML
- Framework of choice

</v-clicks>

<Frameworks v-click></Frameworks>

---
clicks: 1
---

<AstroPart pageToRun=9>Astro</AstroPart>

---

# ASTRO

<AstroSell>Want some Islands?</AstroSell>

---

# ASTRO

<AstroSell2>A new web architecture for building faster websites.</AstroSell2>

---
clicks: 1
---

<AstroPart pageToRun=12>Islands</AstroPart>

---
---

# Typical page
<section class="page-with-islands">
  <p>Page</p>
    <Island type="react" class="react" v-click>
			<template v-slot:icon>
				<img class="logo-img" src="/React.svg" alt="">
			</template>
			<template v-slot:title>React</template>
		</Island>
</section>

<style lang='css' scoped>
  .page-with-islands {
    width: 100%;
    height: 93%;
    padding: 15px;
    border-radius: 8px;
    border: 1px solid white;
    text-align: center;
  }
  .page-with-islands p {
    margin: 0;
  }
  .logo-img {
	width: 40px;
	height: 40px;
}
.react {
  height: 95%;
}
</style>

---

# What are Islands
<section class="page-with-islands">
  <p>Page</p>
  <section class="wrapper-islands" v-click>
    <Island type="react" class="react">
			<template v-slot:icon>
				<img class="logo-img" src="/React.svg" alt="">
			</template>
			<template v-slot:title>React</template>
		</Island>
    <Island type="vue" class="vue">
			<template v-slot:icon>
				<img class="logo-img" src="/Vue.svg" alt="">
			</template>
			<template v-slot:title>Vue</template>
	  </Island>
    <Island type="svelte" class="svelte">
	  	<template v-slot:icon>
				<img class="logo-img" src="/Svelte.svg" alt="">
			</template>
			<template v-slot:title>Svelte</template>
		</Island>
    <Island type="html" class="html">
			<template v-slot:icon>
				<img class="logo-img" src="/Html.svg" alt="">
			</template>
			<template v-slot:title>HTML</template>
		</Island>
  </section>
</section>

<style lang='css' scoped>
  .page-with-islands {
    width: 100%;
    height: 93%;
    padding: 15px;
    border-radius: 8px;
    border: 1px solid white;
    text-align: center;
  }
  .page-with-islands p {
    margin: 0;
  }
  .wrapper-islands {
    width: 100%;
    height: 100%;
    padding: 15px;
    gap: 5px;
    display: grid;
    grid-template-areas: "header  header"
                         "sidebar main  "
                         "sidebar footer";
    grid-template-rows: repeat(3, 110px);
    grid-template-columns: repeat(2, 1fr);
  }
  .react {
    grid-area: header;
  }
  .vue {
    grid-area: main;
  }
  .svelte {
    grid-area: sidebar;
  }
  .html {
    grid-area: footer;
  }
  .logo-img {
	width: 40px;
	height: 40px;
}
</style>

---
---

# Is there a reason?

<img class="brando" src="/raynolds.jpeg" v-click />

<style lang="css" scoped>
.raynolds {
  margin: 0 auto;
}
</style>
---

# There is!

<img class="brando" src="/Brando.png" v-click />

<style lang="css" scoped>
.brando {
  margin: 0 auto;
}
</style>
---
clicks: 1
---

<AstroPart pageToRun=17>Directives</AstroPart>

---

<v-click>

```tsx
// fancy react Island

export const FancyReact = (blabla: Props)=>{
  return (
    <SomeJSX/>
  )
}

```

</v-click>

<v-click>

```tsx
// Astro app entrypoint

import ReactPart from "**/*/index.tsx";
---

<Layout title="Welcome React-haters">
  <main>
    <ReactPart/>
  </main>
</Layout>
```

</v-click>

<div class="diff">
<v-click>
<img src="/load-me-js.png" />
</v-click>
<v-click>

```tsx
<ReactPart client:idle />
```

✅ Done
</v-click>
</div>

<style lang="css" scoped>
.diff {
  display: flex;
  align-items: center;
  justify-content: flex-start;
  gap: 10px;
  margin-top: 15px;
}

.diff img {
  width: 200px;
}
</style>
---
clicks: 9
---

<Directives  pageToRun=19 />

---
---

# What to remember with SSG

<v-clicks>

- You build time will increase. 
- You should use SSG only for pages that are not changing too often and not depend on concrete user.
- You JS is still works. Parts of page can be rendered on client and be interactive.
- Use Timers, LocalStorage, SessionStorage and onther browser-specific APIs with caution.
- After user get his SSGed page hydration process happens and after it you will have CSA where everything else rendered by Client.
- If you don't need SPA-like user experience but need good speed check out Astro. 

</v-clicks>

<v-click>

<h2 style="margin-top: 55px"> Now lets talk how our page get updates </h2>

</v-click>

---
---

# Types of revalidation

By default generated page will be updated only when we rebuild or app.

But we have 2 options to update it without entire rebuilding.

<div class="options">
  <div v-click class="option">
    <h2>Time-based revalidation</h2>
    <p>Simple pattern where we just specify timer and after time passes page concidered outdated. And for all outdated pages rebuild process begins. <br/>
    Usefull if we want to update something like reviews.</p>
  </div>
    <div v-click class="option">
    <h2>On-demand revalidation</h2>
    <p>Bit more complex pattern. We create invalidation-handler which receives request that will trigger rebuild process.
    For example after we get new post in our blog, CMS responsible for it will sent request that will invalidate page with posts.
    </p>
  </div>
</div>

<style>
  .options {
    display: grid;
    grid-template-columns: 1fr 1fr;
    align-items: center;
    justify-content: center;
    gap: 25px;
  }
  .option {
    border-radius: 8px;
    border: white 2px solid;
    padding: 10px;
    height: 220px;
  }
</style>

---
layout: iframe

url: https://ssgm-etup.vercel.app/timeISR
---
---
layout: iframe

url: https://ssgm-etup.vercel.app/onDemandISR
---
---

# Conclusion


<v-click>

Static-site generation is a very powerfull approach when you have web-pages that doesn't need to be user-specific, but it has some limitations. 

</v-click>

<v-click>

SSG gives us following benefits

</v-click>


<v-clicks>

- Your web-page performance will be <span class="blazingly-fast">Blazingly fast</span>. 
- Under heavy loads your page will remain <span class="cons-perf">Consistently performant</span>.
- You won't spend a lot of time to decide how to serve you site because SSG-pages are <span class="easy-deploy">Easy to deploy</span>.

</v-clicks>

<div class="cons">

<v-click>

<img src="/great-power.webp" class="h-40 mt-5" />

</v-click>

<div>

<v-click>

So with SSG you also got some limitations

</v-click>


<v-clicks>

- Expect your <span class="long-build">build time to take longer then ever before</span>. 
- Get ready to add some checks where you code is running. <span class="no-dynamic">Browser-speific API call will break build</span>.
- Prepare yourself <span class="hard-updates">Complex invalidations</span> if your pages updates frequently.

</v-clicks>

</div>
</div>

<style>
  .blazingly-fast {
    background: linear-gradient(90deg, rgba(255,248,0,1) 0%, rgba(255,154,0,1) 40%, rgba(255,0,0,1) 100%);
    background-clip: text;
    -webkit-background-clip: text;
    color: transparent;
  }
  .cons-perf {
    background: linear-gradient(90deg, rgba(86,149,255,1) 0%, rgba(65,65,203,1) 23%, rgba(176,51,51,1) 100%);
    background-clip: text;
    -webkit-background-clip: text;
    color: transparent;
  }
  .easy-deploy {
    background: linear-gradient(90deg, rgba(0,255,248,1) 0%, rgba(21,175,103,1) 45%, rgba(84,218,20,1) 100%);
    background-clip: text;
    -webkit-background-clip: text;
    color: transparent;
  }

  .cons {
    display: flex;
    flex-direction: row;
    align-items: flex-start;
    justify-content: flex-start;
    gap: 35px;
  }

  .long-build {
    background: linear-gradient(90deg, rgba(66,112,110,1) 0%, rgba(124,58,28,1) 45%, rgba(168,0,0,1) 100%);
    background-clip: text;
    -webkit-background-clip: text;
    color: transparent;
  }

  .no-dynamic {
    background: linear-gradient(90deg, rgba(93,71,138,1) 0%, rgba(61,14,105,1) 45%, rgba(129,7,77,1) 100%);
    background-clip: text;
    -webkit-background-clip: text;
    color: transparent;
  }

  .hard-updates {
    background: linear-gradient(90deg, rgba(137,138,124,1) 0%, rgba(83,85,26,1) 48%, rgba(124,150,34,1) 100%);
    background-clip: text;
    -webkit-background-clip: text;
    color: transparent;
  }

</style>
---
clicks: 1
---

<AstroPart pageToRun=25>Thanks</AstroPart>

---