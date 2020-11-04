<template>
  <div id="app" class="flex container h-screen w-full">
    <div class="w-1/5 border-r-2 px-8 py-12 flex flex-col justify-between">
      <div>
        <button class="h-12 w-12 hover:bg-blue-300 text-4xl text-blue-500">
          <i class="fab fa-twitter"></i>
        </button>
        <button
          v-for="tab in tabs"
          :key="tab"
          @click="id = tab.id"
          :class="`focus:outline-none hover:text-blue-100 flex items-center py-2 px-4 hover:bg-blue-300 rounded-full mr-auto mb-3 ${
            id === tab.id ? 'text-blue-300' : ''
          }`"
        >
          <i :class="`${tab.icon} text-2xl mr-4 text-left`"></i>
          <p class="text-lg font-semibold text-left">{{ tab.title }}</p>
        </button>
        <button
          class="text-black-900 bg-blue-500 rounded-full font-semibold focus:outline-none w-full p-3 hover:bg-blue-700"
        >
          Tweet
        </button>
      </div>
      <div class="w-full relative">
        <button class="flex items-center w-full rounded-full focus:outline-none hover:bg-gray-300 p-2">
          <img
            src="https://steamcdn-a.akamaihd.net/steamcommunity/public/images/avatars/c4/c4d5255374aeca6369da7d068c5eb6dce9299002_full.jpg"
            class="w-12 h-12 rounded-full"
          />
          <div class="ml-4">
            <p class="text-sm font-bold">Emmanuel</p>
            <p class="text-sm">@SakuragiDev</p>
          </div>
          <i class="fas fa-angle-down text-dark-900 ml-auto"></i>
        </button>
        <div class="absolute bottom-0 left-0 w-64 rounded-lg shadow-md mb-16 bg-white-900">
          <button class="flex items-center w-full rounded-full focus:outline-none hover:bg-gray-300 p-2">
          <img
            src="https://steamcdn-a.akamaihd.net/steamcommunity/public/images/avatars/c4/c4d5255374aeca6369da7d068c5eb6dce9299002_full.jpg"
            class="w-12 h-12 rounded-full"
          />
          <div class="ml-4">
            <p class="text-sm font-bold">Emmanuel</p>
            <p class="text-sm">@SakuragiDev</p>
          </div>
          <i class="fas fa-check ml-auto text-blue-500"></i>
        </button>
        </div>  
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      tabs: [
        { icon: "fas fa-home", title: "Home", id: "home" },
        { icon: "fas fa-hashtag", title: "Explore", id: "explore" },
        { icon: "far fa-bell", title: "Notifications", id: "notifications" },
        { icon: "far fa-envelope", title: "Messages", id: "messages" },
        { icon: "far fa-bookmark", title: "Bookmarks", id: "bookmarks" },
        { icon: "fas fa-clipboard-list", title: "Lists", id: "lists" },
        { icon: "far fa-user", title: "Profile", id: "profile" },
        { icon: "fas fa-ellipsis-h", title: "More", id: "more" },
      ],
      id: "home",
    };
  },
};
</script>


