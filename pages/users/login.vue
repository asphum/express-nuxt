<template>
  <div class="uk-padding-small">
    
    <div class="bg-head"><h3>#เข้าสู่ระบบ</h3></div>
    <div class="bg-content">
      <form class="uk-form-stacked uk-text-center">

        <div class="uk-margin">
          <label class="uk-form-label" for="form-stacked-text">อีเมล</label>
          <div class="uk-form-controls">
            <div class="uk-inline">
              <span class="uk-form-icon" uk-icon
                ><i class="fas fa-envelope"></i
              ></span>
              <input
                class="uk-input uk-form-width-auto"
                name="email"
                type="email"
              />
            </div>
          </div>
        </div>

        <div class="uk-margin">
          <label class="uk-form-label" for="form-stacked-text">รหัสผ่าน</label>
          <div class="uk-form-controls">
            <div class="uk-inline">
              <span class="uk-form-icon" uk-icon
                ><i class="fas fa-key"></i
              ></span>
              <input
                class="uk-input uk-form-width-auto"
                name="password"
                type="password"
              />
            </div>
          </div>
        </div>

        <button class="uk-button uk-button-1waan">
          <i class="fas fa-sign-in-alt" style="padding-right: 5px;"></i
          >เข้าสู่ระบบ
        </button>
      </form>
    </div>
  </div>
</template>
<script>
export default {
    head: {
    title: "สมัครสมาชิก"
  }
}
</script>