<template>
    <article>
        <slot name="default">
            <div class="">
                <a :href="link">
                    <Img :src="imgUrl" :alt="alt" format="avif, webp"
                        class="object-cover object-center h-40 xl:h-64 w-full box-border" />
                    <div class="glass-border w-full">
                        <div class="flex justify-between p-4">
                            <h2 class="text-zinc-500 dark:text-zinc-200">
                                {{ title }}
                            </h2>
                            <time :datetime="date" class="text-gray-400 dark:text-zinc-300">
                                {{ date }}
                            </time>
                        </div>

                    </div>
                </a>
            </div>
        </slot>
        <slot name="not-found"></slot>
    </article>
</template>

<script setup>
defineProps({
    title: {
        type: String,
        required: true
    },
    date: {
        type: String,
        required: true
    },
    imgUrl: {
        type: String,
        required: true
    },
    alt: {
        type: String,
        required: true
    },
    link: {
        type: String,
        required: true
    },

})
</script>
