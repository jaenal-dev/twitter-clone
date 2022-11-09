<template>
    <div class="flex flex-col">
        <!-- Card : What's Happening -->
        <SidebarRightCard title="What's Happening">
            <SidebarRightCardItem v-for="whatsHappening in whatsHappeningItems">
                <div>
                    <h2 class="font-bold text-gray-800 text-md dark:text-white">{{ whatsHappening.title }}</h2>
                    <p class="text-xs text-gray-400 ">{{ whatsHappening.count }}</p>
                </div>
            </SidebarRightCardItem>
        </SidebarRightCard>

        <!-- Card : Who to Follow -->
        <SidebarRightCard title="Who to Follow">
            <SidebarRightCardItem v-for="whoToFollow in whoToFollowItems">
                <div class="flex flex-row justify-between p-2">
                    <div class="flex flex-row">
                        <img class="w-10 h-10 rounded-full" :src="whoToFollow.image" :alt="whoToFollow.name">
                    </div>
                    <p>{{ whoToFollow.name }}</p>
                    <p>{{ whoToFollow.handle }}</p>
                </div>
            </SidebarRightCardItem>
        </SidebarRightCard>
    </div>
</template>

<script setup>
const whatsHappeningItems = ref([
    {
        title: 'SpaceX',
        count: '18.8k tweets'
    },
    {
        title: '#CodingIsFun',
        count: '8.8k tweets'
    },
    {
        title: '#artforall',
        count: '1.8k tweets'
    }
])

const whoToFollowItems = ref([
    {
        name: 'John Doe',
        handle: '@JohnDoe',
        image: 'https://picsum.photos/200/200'
    },
])
</script>