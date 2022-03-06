<template>
  <ul class="sidenav app-sidenav" :class="{open: isOpen}">  

    <router-link
      v-for="link in links"
      :key="link.url"
      active-class="active"
      :to="link.url"
      :exact="link.exact"
    >
      <li>
        <a href="#" class="waves-effect waves-orane pointer">{{link.title}}</a>
      </li>
    </router-link>
    
  </ul>
</template>

<script>
export default {
  props: ['isOpen'],
  data: () => ({
    links: [
      {title: 'Счет', url: '/', exact: true},
      {title: 'История', url: '/history'},
      {title: 'Планирование', url: '/planning'},
      {title: 'Новая запись', url: '/record'},
      {title: 'Категория', url: '/categories'},
    ]
  })
}
</script>
