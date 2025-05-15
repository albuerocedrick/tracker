<template>
    <div
      class="bg-black/50 fixed inset-0 flex justify-center items-center"
      @click.self="$emit('NavModalClose')">
        <div :class="['box', 'w-1/4', 'h-2/5', theme.cardBg, theme.border]">
            <form class="w-full h-full flex flex-col justify-center  items-center gap-4" action="">
                <h1
                  class="font-bold text-4xl"
                  :class="[theme.textColor]">Log In</h1>
                <div class="sign-container">
                    <label
                      class="sign-label"
                      :class="[theme.textColor]"
                      for="">Email</label>
                    <input
                      class="sign-input"
                      :class="[theme.textColor]"
                      type="email">
                </div>
                <div class="sign-container">
                    <label
                      class="sign-label"
                      :class="[theme.textColor]"
                      for="">Password</label>
                   <input
                      class="sign-input"
                      :class="[theme.textColor]"
                      type="password">
                </div>
                <button
                  class="sign-submit"
                  type="submit"
                  @click="$emit('OpenMainPage')">Log In</button>
            </form>
        </div>
    </div>
</template>

<script>
    export default {
        props: ['theme'],
        emits: ['NavModalClose', 'OpenMainPage']
    }
</script>