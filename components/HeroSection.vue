<template>
    <div v-bind:class="$style.container">
        <h2 v-bind:class="$style.mainHeadline">Create.</h2>
        <p v-bind:class="$style.mainIntro">Passionate purpose-driven Web Developer & Designer based in
        Houston, Texas with an emphasis on making online experiences memorable.</p>
    </div>
</template>

<style lang="scss" module>

    .container {
        @apply flex flex-col mt-10 m-auto w-full;
        max-width: 75%;
    }

    .mainHeadline {
        @apply font-black;
        font-size: 10rem;
    }

    .mainIntro {
        @apply font-thin leading-loose max-w-md mt-2 tracking-wide text-grey-darkest;
        font-size: .9rem;
    }

</style>
