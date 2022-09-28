<script lang="ts" setup>
  import {ElAvatar, ElIcon} from 'element-plus';
  import { House, Collection, Guide, Avatar } from '@element-plus/icons-vue';
  import { DefineComponent } from 'vue';
  interface NAV_MENU {
    text: string;
    icon: DefineComponent;
    link?: string;
  }
  type NAV_JSON_TYPE = NAV_MENU[];
  const nav_json: NAV_JSON_TYPE = [
    { text: '主页', icon: House },
    { text: '标签', icon: Guide },
    { text: '存档', icon: Collection },
    { text: '关于', icon: Avatar }
  ]
</script>
<template>
  <div w-60 flex items-center flex-col pt-12>
    <div class="border-[#979797]" border-b-1px p-10px>
      <el-avatar :size="100" src="/assets/images/idea.png"/>
      <div class="color-[#666]" text-center font-light mt-2 mb-3 italic>十号</div>
    </div>
    <ul px-0 my-25px>
      <li v-for="nav in nav_json" :key="nav.text" class="color-[#999]" cursor-pointer text-sm my-5 flex items-center list-none>
        <el-icon size="20px">
          <component :is="nav.icon" />
        </el-icon>
        <span ml-1>{{nav.text}}</span>
      </li>
    </ul>
  </div>
</template>
