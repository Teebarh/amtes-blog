---
showDate: false
showReadingTime: false
showWordCount: false
type: custom
layout: centered
---

<div class="container">
    <h1>Welcome to</h1>
    <h2>the AMTES Blog</h2>
</div>

Explore the latest updates, research, and projects from the Mechatronics Engineering Department at FUNAAB. Stay informed and engaged with our community.

{{< button href="about" target="_self" >}}
About Us
{{< /button >}}

---

<div class="pro-section">
    <div class="pro-title">
        <h1>Check Out<br>Our Projects</h1>
    </div>
    <div class="pro-desc">
        <p>
            Explore cutting-edge innovations like robotic arms, drones, and more. Discover the latest advancements and get inspired by the projects that are shaping the future.
        </p>
        <a class="!rounded-md bg-primary-600 px-4 py-2 !text-neutral !no-underline hover:!bg-primary-500 dark:bg-primary-800 dark:hover:!bg-primary-700">See More →</a>
    </div>  
</div>

---

<div id="apply" class="container">
    <h2>Become a Student Blogger</h2>
</div>

Do you have a flair for writing? Want to share your eye-catching ideas with the world? We’ve got you covered!

Join our dynamic student blogging team and let your voice be heard!

<a class="!rounded-md bg-primary-600 px-4 py-2 !text-neutral !no-underline hover:!bg-primary-500 dark:bg-primary-800 dark:hover:!bg-primary-700">Apply Now!</a>

---

<div class="container">
    <h2>FAQ</h2>
</div>

**Q: How can I contribute to the blog?**

A: You can apply to become a student blogger by clicking the "[Apply Now!](#apply)" button above.

**Q: What topics can I write about?**

A: We welcome a wide range of topics related to Mechatronics, engineering, and pretty much anything.

**Q: How can I bring that flair to my writing?**

A: No worries! Check out our comprehensive [writing guide]({{< ref "how-to-write" >}}) for tips and inspiration to elevate your content.

<style>
    .pro-section {
        display: flex;
        justify-content: space-between;
        align-items: flex-start; /* Aligns items at the start */
    }

    .pro-title {
        flex: 1;
    }

    .pro-title > h1 {
        font-size: 4rem;
        text-align: left;
        font-weight: bold;
        margin-right: 30px;
        transform: rotate(-5deg);
    }

    .pro-title > h2 {
        font-size: 3rem;
        text-align: left;
        font-weight: bold;
        margin: 0;
        transform: translateY(-30px) rotate(-10deg); /* Slight upward shift for effect */
    }

    .pro-desc {
        flex: 1; /* Allows the description to take more space */
        margin-right: 20px; /* Adjust for desired whitespace */
    }
</style>
