<script setup>
  const items = ref([
    {
        title:"Dashboard",
        path:"/home",
        icon:"pixelarticons:dashboard"
    },
    {
        title:"Transaction",
        path:"/transactions",
        icon:"healthicons:money-bag-negative"
    },
    {
        title:"Account",
        path:"/services",
        icon:"ri:account-box-fill"
    },
    {
        title:"Contacts",
        path:"/about",
        icon:"mdi:contacts"
    },
    {
        title:"Settings",
        path:"/services",
        icon:"ic:baseline-settings"
    }

  ]);
</script>

<template>
    <div>
        <header class="flex items-center gap-2 p-4 hover:scale-[101%] transition cursor-pointer">
            <Logo />
            <p class="font-bold">Shipping Management</p>
        </header>
        <div class="px-4 grow">
            <div class="grid gap-2">
                <NuxtLink :href="item.path" v-for='(item,index) in items' :key="index" class="flex items-center gap-2 px-2 py-1 rounded transition cursor-pointer hover:bg-neutral-100">
                    <Icon size="20" :name="item.icon" color="black" />
                    <span>{{ item.title }}</span>
                </NuxtLink>
            </div>
        </div>
    </div>
</template>