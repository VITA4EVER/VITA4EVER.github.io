<template>
    <div class="section bg-[url('assets/pictures/bg.png')]">
        <div class="drk-rect"></div>
        <div class="absolute w-screen min-h-screen flex flex-col justify-center items-center pt-[5%] gap-12 text-center">
            <h2 class="font-bold text-2xl md:text-3xl text-center m-4">All articles here are in a chronical way, the newest ones are on the top</h2>
                <div id="main-articles-container" class="flex flex-col gap-8 md:gap-12"> <!-- Articles container -->
                                        
                    <a class="w-full p-6 border-accent border-4 rounded-2xl text-center self-center text-emerald-50 m-2 md:m-6 lg:m-12" v-for="article_page in article_pages" :key="article_page.path" :href="'/feed' + article_page.path">
                        <h2 class="font-bold text-3xl mt-4">{{ article_page.title }}</h2>
                    </a>
                    <KZButton @click="fetchInitArticlePage">Load All</KZButton>
                </div>
            </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            article_pages: null
        }
    },
    methods: {
        async fetchInitArticlePage() {
            const { data: docs } = await useAsyncData('articles-list', () => {
            return queryCollection('feed')
                .order('date', 'DESC')
                .select('title', 'path')
                .all()
            })

            this.article_pages = docs
        },
    },
}
</script>