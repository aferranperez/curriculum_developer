<template>
    <!-- Skills -->
    <div class="flex flex-col gap-10 lg:flex-row">
        <div class="px-3 w-full lg:flex-1">
            <h4 class="py-5 text-3xl">From <span class="underline bg-gradient-to-r from-primary-600 to-success-500 bg-clip-text text-transparent">self-taught</span> to graduate. <span class="bg-gradient-to-r from-primary-600 to-success-500 bg-clip-text text-transparent">Still passionate.</span></h4>
            <div class="grid grid-cols-6 gap-5">
                <nuxt-icon name="technologies/tailwind" filled />
                <nuxt-icon name="technologies/typescript" filled />
                <nuxt-icon name="technologies/nuxt" filled />
                <nuxt-icon name="technologies/vue" filled />
                <nuxt-icon name="technologies/tailwind" filled />
                <nuxt-icon name="technologies/typescript" filled />
                <nuxt-icon name="technologies/nuxt" filled />
                <nuxt-icon name="technologies/vue" filled />
            </div>
        </div>
        <div class="w-full flex flex-col px-3 gap-1 lg:flex-1">
            <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Veritatis assumenda earum non expedita! Quasi eaque sed amet commodi voluptatibus quidem.</p>
            <br/>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Voluptates modi magnam repellat quas suscipit doloribus vero ratione omnis error numquam! Ipsum minima iure eveniet?</p>
            <br>
            <p>Lorem ipsum, dolor sit amet consectetur adipisicing elit. Nam, alias!</p>

            <div class="flex justify-center my-5">
                <a class="mb-2 inline-block rounded bg-success-500 px-12 pt-4 pb-3.5 text-sm font-medium uppercase leading-normal text-white shadow-[0_4px_9px_-4px_#3b71ca] transition duration-150 ease-in-out hover:bg-primary-600 hover:shadow-[0_8px_9px_-4px_rgba(59,113,202,0.3),0_4px_18px_0_rgba(59,113,202,0.2)] focus:bg-primary-600 focus:shadow-[0_8px_9px_-4px_rgba(59,113,202,0.3),0_4px_18px_0_rgba(59,113,202,0.2)] focus:outline-none focus:ring-0 active:bg-primary-700 active:shadow-[0_8px_9px_-4px_rgba(59,113,202,0.3),0_4px_18px_0_rgba(59,113,202,0.2)] dark:shadow-[0_4px_9px_-4px_rgba(59,113,202,0.5)] dark:hover:shadow-[0_8px_9px_-4px_rgba(59,113,202,0.2),0_4px_18px_0_rgba(59,113,202,0.1)] dark:focus:shadow-[0_8px_9px_-4px_rgba(59,113,202,0.2),0_4px_18px_0_rgba(59,113,202,0.1)] dark:active:shadow-[0_8px_9px_-4px_rgba(59,113,202,0.2),0_4px_18px_0_rgba(59,113,202,0.1)] md:mr-2 md:mb-0"
                data-te-ripple-init data-te-ripple-color="light" href="#!" role="button">Learn More</a>
            </div>

        </div>
    </div>
</template>

<style>
.nuxt-icon svg{
    width: 2.5em;
    height: 2.5em;
    margin-bottom: 0;
}
</style>