<template>
  <div class="h-screen w-screen">
    <div
      id="header"
      class="flex items-center justify-center bg-black w-full"
      style="height: 12%"
    >
      <!--start of logo-->
      <div class="w-1/5 h-full flex items-center justify-center">
        <div class="w-3/4 flex items-center justify-end mx-1">
          <img src="@/assets/logo.svg" class="w-1/3" />
        </div>
        <div class="w-1/4 flex items-center justify-center">
          <img
            src="@/assets/telegram.svg"
            class="w-1/3"
            @click="toggleDropdownTel"
          />
          <div class="relative">
            <div
              v-show="isOpenTel"
              class="absolute bg-gray-200 top-full mt-3 left-full text-black"
            >
              <ul>
                <li>
                  <a
                    href="#"
                    class="block px-1 py-2 hover:bg-gray-200"
                    @click="toggleDropdownTel"
                    >Group</a
                  >
                </li>
                <li>
                  <a
                    href="#"
                    class="block px-1 py-2 hover:bg-gray-200"
                    @click="toggleDropdownTel"
                    >Support</a
                  >
                </li>
              </ul>
            </div>
          </div>
        </div>
      </div>
      <!--end of logo-->

      <!--start of text-->
      <div class="w-2/5 h-full flex items-center justify-center">
        <div class="w-2/3 h-full text-white flex">
          <div class="flex-1 mx-1 flex items-center justify-center">О нас</div>
          <div class="flex-1 mx-1 flex items-center justify-center">
            Сообщество
          </div>
          <div class="flex-1 mx-1 flex items-center justify-center">FAQ</div>
        </div>
      </div>
      <!--end of text-->

      <!--start of register-len-->
      <div class="w-1/5 h-full flex items-center justify-start">
        <div
          class="w-3/4 h-full flex items-center justify-start"
          style="margin-right: 1%"
        >
          <div class="w-1/4 text-white mx-2">Вход</div>
          <button
            class="w-3/4 text-black px-4 py-2 rounded-lg mx-2 md:py-3 md:px-6 lg:py-2 lg:px-4"
            style="background-color: #fff72c"
          >
            Регистрация
          </button>
        </div>

        <div class="w-1/4 h-full flex items-center justify-start">
          <div class="w-1/3 h-full text-white flex items-center justify-center">
            RU
          </div>
          <div class="w-2/3 h-full text-white flex items-center justify-start">
            <img
              class="w-1/2"
              src="@/assets/expand.svg"
              @click="toggleDropdownLan"
            />
            <div class="relative">
              <div
                v-show="isOpenLan"
                class="absolute bg-gray-200 top-full mt-3 right-full text-black"
              >
                <ul>
                  <li>
                    <a
                      href="#"
                      @click="toggleDropdownLan"
                      class="block px-2 py-2 hover:bg-gray-200"
                      >RU</a
                    >
                  </li>
                  <li>
                    <a
                      href="#"
                      @click="toggleDropdownLan"
                      class="block px-2 py-2 hover:bg-gray-200"
                      >EN</a
                    >
                  </li>
                </ul>
              </div>
            </div>
          </div>
        </div>
      </div>
      <!--end of register-len-->
    </div>
  </div>
</template>

<script>
import { ref } from "vue";
export default {
  name: "App",
  setup() {
    const isOpenLan = ref(false);
    const toggleDropdownLan = () => {
      isOpenLan.value = !isOpenLan.value;
    };

    const isOpenTel = ref(false);
    const toggleDropdownTel = () => {
      isOpenTel.value = !isOpenTel.value;
    };
    return {
      isOpenLan,
      isOpenTel,
      toggleDropdownTel,
      toggleDropdownLan,
    };
  },
};
</script>
