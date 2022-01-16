<template lang="pug">
.home.flex.justify-center.items-center.h-screen.flex-col.p-20
  .container.w-28.mb-1
    img.w-28(alt="Vue logo", src="../assets/icon.png")
    .font-bold.mb-2 Missing App
  img.w-28.mb-20(
    src="@/assets/apple.png",
    @click="window.open('https://apps.apple.com/tw/app/missing-%E8%A6%93%E5%BF%83/id1546452918https://apps.apple.com/tw/app/missing-%E8%A6%93%E5%BF%83/id1546452918', '_blank')"
  )
  .flex.flex-col.justify-self-end
    .font-bold.mb-2 Missing App Support
    .contact
      .font-medium 聯絡我們
      .cursor-pointer.rounded-md.bg-red-400.text-white.px-7.py-2.min-w-min.flex.items-center(
        @click="copied = true; navigator.clipboard.writeText('missingappofficial@gmail.com')"
      )
        i.far.fa-envelope.mr-2 
        .text missingappofficial@gmail.com
      .text-gray-600.text-sm.clicked(v-if="copied") 已複製！
</template>

<script>
// @ is an alias to /src

export default {
  name: "Home",
  components: {},
  data() {
    return {
      copied: false,
    };
  },
};
</script>
