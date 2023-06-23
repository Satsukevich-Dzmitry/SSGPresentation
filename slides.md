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
---
# Hi! Thanks for joining.

<v-click>

Today we will talk about...

</v-click>

<v-click>

SSG!

</v-click>

---
preload: false
clicks: 4
src: ./pages/plan.md
---
---

# What is it? 

<v-click>

Static-site generation(*SSG*) is the process of creating web-pages by pre-generating each page, resulting in really good performance and UX. 

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
- No more highly dynamic or user-specific UI. <span class="no-dynamic">First S in SSG stands for Static</span>.
- Get ready to have <span class="hard-updates">Complex invalidations</span> if your pages updates frequently.

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
preload: false
clicks: 14
src: ./pages/basicFlow.md
---
---

# SEO

---
---

# What we need for SSG

---
---

# Lets compare tools (IMHO ALERT)

---
---

# ASTRO

---
---

# Types of revalidation

---
---
layout: iframe

url: https://ssgm-etup.vercel.app/timeISR
---
---
layout: iframe

url: https://ssgm-etup.vercel.app/onDemandISR
---
---

# About performance and metrics

---
---

# Conclusion

---