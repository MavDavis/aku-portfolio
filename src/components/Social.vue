<script lang="ts">
import { defineComponent } from "vue";
import { IMAGE } from "../assets/Image";
interface Item {
  id: number;
  child: string;
  href: string;
  icon:string
  style: string;
}

export default defineComponent({
  name: "ItemList",
  data() {
    return {
      links: [
        {
          id: 1,
          child: "LinkedIn ",
            icon:'fa fa-linkedin',
          href: "https://www.linkedin.com/in/rahmath-irshad-74781988/",
          style: "rounded-tr-md",
        },
        {
          id: 2,
          child: "Github",
          icon:'fa fa-github',

          href: "https://www.linkedin.com/in/rahmath-irshad-74781988/",
          style: "rounded-tr-md",
        },
        {
          id: 3,
          child: "Mail",
          icon:'far fa-envelope',

          href: "https://www.linkedin.com/in/rahmath-irshad-74781988/",
          style: "rounded-br-md",
        },
        {
          id: 5,
          child: "Resume",
          icon:'fas fa-user',

          href: "https://www.linkedin.com/in/rahmath-irshad-74781988/",
          style: "rounded-tr-md",
        },
      ] as Item[],
    };
  },
});
</script>
<template>
      <div class="hidden lg:flex flex-col top-[35%] left-0 fixed">
      <ul v-for="item in links">
          <li
            :key=item.id
            class=
              "flex justify-between items-center w-40 h-14 px-4 ml-[-100px] hover:ml-[-10px] hover:rounded-md duration-300 bg-gray-500 hover:bg-sky-500" 
             
          >
            <a
              :href=item.href
              class="flex justify-between items-center w-full text-white"
              download={download}
              target="_blank"
              rel="noreferrer"
            >
            {{item.child}}
            <i :class="item.icon"></i>
            </a>
          </li>
     
      </ul>
    </div>
</template>