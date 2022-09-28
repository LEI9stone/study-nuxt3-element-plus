<template>
  <header h-11>
    我是头部UI
  </header>
  <div flex mx-auto justify-center >
    <Author />
    <div w-784px>
      <slot />
    </div>
  </div>
  <footer>
    我是底部友情链接
  </footer>
</template>