<script>
    import 'iconify-icon'
    import contact from "$lib/content/contact.json";
</script>

<section class="section" id="contact">
    <div class="container is-max-desktop">
        <div class="columns">
            <div class="column is-6">
                <div class="block">
                    <h1 class="title is-1">
                        Get In Touch
                    </h1>
                </div>
                <div class="has-text-centered is-size-3">
                    <a href="mailto:{contact.email}">
                        {contact.email}
                    </a>
                </div>
            </div>
            <div class="column is-2">
            </div>
            <div class="column is-3">
                <div class="block">
                    <h1 class="title is-3 pt-5">
                        Socials
                    </h1>
                </div>
                <div class="buttons">
                            <a class="button is-flex is-justify-content-left my-1 is-fullwidth" href="mailto:{contact.email}">
                                <span class="icon pr-3 ml-0">
                                    <iconify-icon icon="line-md:email" height="auto"></iconify-icon>
                                </span>
                                <span>
                                    {contact.email}
                                </span>
                            </a>
                            <a class="button is-normal is-flex is-justify-content-left my-1 is-fullwidth" href="{contact.github.link}">
                                <span class="icon pr-3 ml-0">
                                    <iconify-icon icon="line-md:github" height="auto"></iconify-icon>
                                </span>
                                <span>
                                    {contact.github.handle}
                                </span>
                            </a>
                    <a class="button is-flex is-justify-content-left my-1 is-fullwidth" href="{contact.linkedin.link}">
                        <span class="icon pr-3 ml-0">
                            <iconify-icon icon="line-md:linkedin" height="auto"></iconify-icon>
                        </span>
                        <span>
                            {contact.linkedin.handle}
                        </span>
                    </a>
                </div>
            </div>
        </div>
</section>


<style>
</style>
