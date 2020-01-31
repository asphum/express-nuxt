<template>
  <div>
    <div id="mainmenu">
      <div class="uk-container uk-container-xlarge">
        <nav class="uk-navbar-container" uk-navbar>
          <div class="uk-navbar-left">
            <ul class="uk-navbar-nav">
              <NuxtLink
                v-for="(item, i) in items"
                :key="i"
                :to="item.to"
                class="menulink"
                ><li>
                  <i :class="item.icon" style="padding-right: 3px;"></i>
                  {{ item.title }}
                </li></NuxtLink
              >
            </ul>
          </div>

          <div class="uk-navbar-right">
            <ul class="uk-navbar-nav">
                <NLink class="menulink nav-item nav-link" to="/user/login"><li>
                  <i class="fas fa-sign-in-alt" style="padding-right: 5px;"></i
                  >เข้าสู่ระบบ</li>
                </NLink>
                <NLink class="menulink nav-item nav-link" to="/user/register"><li>
                  <i class="fas fa-user-plus" style="padding-right: 5px;"></i
                  >สมัครสมาชิก</li>
                </NLink>
            </ul>
          </div>
        </nav>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      toolbar: '#toolbar',
      items: [
        {
          icon: 'fas fa-home',
          title: 'หน้าแรก',
          to: '/'
        },
        {
          icon: 'fas fa-book',
          title: 'เอกสาร',
          to: '/docs'
        },
        {
          icon: 'fas fa-headphones',
          title: 'เสียง',
          to: '/audios'
        },
        {
          icon: 'fas fa-film',
          title: 'วิดีโอ',
          to: '/videos'
        },
        {
          icon: 'fas fa-image',
          title: 'รูปภาพ',
          to: '/albums'
        },
        {
          icon: 'fas fa-pen-alt',
          title: 'เว็บบอร์ด',
          to: '/boards'
        }
      ]
    }
  }
}
</script>
<style scoped>
#mainmenu {
  background-color: #323232 !important;
  color: #fff;
  padding: 0px;
  z-index: 100;
  box-shadow: 0 1px 3px 0 rgba(0,0,0,.1), 0 1px 2px 0 rgba(0,0,0,.06);
}
.menulink {
  color: #fff !important;
  font-size: 1.2rem;
  font-weight: 700;
  padding: 5px 10px;
  display: inline-block;
  transition: 0.3s;
  text-decoration: none;
  text-shadow: 1px 1px 1px rgba(0, 0, 0, 0.8);
  margin: 5px;
  box-shadow: 0 1px 3px 0 rgba(0,0,0,.1), 0 1px 2px 0 rgba(0,0,0,.06);
}
.menuicon {
  color: #fff !important;
  margin-right: 5px !important;
}
.menulink:hover,
.nuxt-link-exact-active {
  background-color: #eb622c;
  border-radius: 4px;
}
.uk-navbar-container {
  background: none !important;
  height: 50px !important;
}
.navbar-toggler {
  border: none;
  padding: 0.25rem 0.75rem;
  font-size: 2rem;
  line-height: 1;
  background-color: transparent;
  border-radius: 0.25rem;
}
</style>
