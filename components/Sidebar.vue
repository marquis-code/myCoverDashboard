<template>
  <main class="">
    <div
      style="background-color: #070707"
      class="hidden lg:flex h-screen flex-col justify-between border-r top-10 overflow-y-auto"
    >
      <div class="px-6 py-5">
        <div class="h-10 pt-3">
          <div class="">
            <img
              src="@/assets/img/logo_white.svg"
              @click="$router.push('/')"
              class="cursor-pointer"
              alt=""
            />
          </div>
        </div>

        <nav aria-label="Main Nav" class="flex flex-col space-y-4 pt-10">
          <router-link
            :class="[$route.name === 'index' ? 'text-green-400' : 'text-white']"
            to="/"
            class="flex items-center gap-2 rounded-lg py-2 space-x-3"
          >
            <img src="@/assets/img/get_started.svg" alt="" />

            <span class="text-sm font-semibold"> Get Started </span>
          </router-link>
        </nav>

        <nav aria-label="Dashboard Nav" class="flex flex-col space-y-4 pt-10">
          <p style="color: #98a2b3" class="uppercase text-xs font-light">
            Dashboard
          </p>
          <router-link
            :class="[
              $route.name === 'analytics' ? 'text-green-400' : 'text-white',
            ]"
            to="/analytics"
            class="flex items-center gap-2 rounded-lg py-2 space-x-3"
          >
            <img src="@/assets/img/analytics.svg" alt="" />

            <span class="text-sm font-semibold"> Analytics </span>
          </router-link>
        </nav>

        <nav aria-label="Admin Nav" class="flex flex-col space-y-4 pt-10">
          <p style="color: #98a2b3" class="uppercase text-xs font-light">
            Admin
          </p>

          <router-link
            :class="[$route.name === 'sales' ? 'text-green-400' : 'text-white']"
            to="/sales"
            class="flex items-center gap-2 rounded-lg py-2 space-x-3"
          >
            <img src="@/assets/img/sales.svg" alt="" />

            <span class="text-sm font-semibold"> Sales </span>
          </router-link>

          <router-link
            :class="[
              $route.name === 'policies' ? 'text-green-400' : 'text-white',
            ]"
            to="/policies"
            class="flex items-center gap-2 rounded-lg py-2 space-x-3"
          >
            <img src="@/assets/img/policies.svg" alt="" />

            <span class="text-sm font-semibold"> Policies </span>
          </router-link>

          <router-link
            :class="[
              $route.name === 'products' ? 'text-green-400' : 'text-white',
            ]"
            to="/products"
            class="flex items-center gap-2 rounded-lg py-2 space-x-3"
          >
            <img src="@/assets/img/products.svg" alt="" />

            <span class="text-sm font-semibold"> Products </span>
          </router-link>

          <router-link
            :class="[
              $route.name === 'customers' ? 'text-green-400' : 'text-white',
            ]"
            to="/customers"
            class="flex items-center gap-2 rounded-lg py-2 space-x-3"
          >
            <img src="@/assets/img/customer.svg" alt="" />

            <span class="text-sm font-semibold"> Customer </span>
          </router-link>

          <router-link
            :class="[$route.name === 'users' ? 'text-green-400' : 'text-white']"
            to="/users"
            class="flex items-center gap-2 rounded-lg py-2 space-x-3"
          >
            <img src="@/assets/img/users.svg" alt="" />

            <span class="text-sm font-semibold"> Users </span>
          </router-link>

          <router-link
            :class="[
              $route.name === 'claims' ? 'text-green-400' : 'text-white',
            ]"
            to="/claims"
            class="flex items-center gap-2 rounded-lg py-2 space-x-3"
          >
            <img src="@/assets/img/claims.svg" alt="" />

            <span class="text-sm font-semibold"> Claim </span>
          </router-link>
        </nav>

        <nav aria-label="Transaction Nav" class="flex flex-col space-y-4 pt-10">
          <p style="color: #98a2b3" class="uppercase text-xs font-light">
            Transactions
          </p>
          <router-link
            :class="[
              $route.name === 'wallet' ? 'text-green-400' : 'text-white',
            ]"
            to="/wallet"
            class="flex items-center gap-2 rounded-lg py-2 space-x-3"
          >
            <img src="@/assets/img/wallet.svg" alt="" />

            <span class="text-sm font-semibold"> Wallet </span>
          </router-link>

          <router-link
            :class="[
              $route.name === 'transactionHistory'
                ? 'text-green-400'
                : 'text-white',
            ]"
            to="/transactionHistory"
            class="flex items-center gap-2 rounded-lg py-2 space-x-3"
          >
            <img src="@/assets/img/transactionHistory.svg" alt="" />

            <span class="text-sm font-semibold"> Transaction History </span>
          </router-link>
        </nav>

        <nav aria-label="Dashboard Nav" class="flex flex-col space-y-4 pt-10">
          <p style="color: #98a2b3" class="uppercase text-xs font-light">
            Others
          </p>
          <router-link
            :class="[
              $route.name === 'provider' ? 'text-green-400' : 'text-white',
            ]"
            to="/provider"
            class="flex items-center gap-2 rounded-lg py-2 space-x-3"
          >
            <img src="@/assets/img/users.svg" alt="" />

            <span class="text-sm font-semibold"> Provider </span>
          </router-link>

          <router-link
            :class="[
              $route.name === 'distributors' ? 'text-green-400' : 'text-white',
            ]"
            to="/distributors"
            class="flex items-center gap-2 rounded-lg py-2 space-x-3"
          >
            <img src="@/assets/img/users.svg" alt="" />

            <span class="text-sm font-semibold"> Distributors </span>
          </router-link>
        </nav>

        <nav aria-label="Service Nav" class="flex flex-col space-y-4 pt-10">
          <p style="color: #98a2b3" class="uppercase text-xs font-light">
            Service
          </p>
          <router-link
            :class="[
              $route.name === 'inspection' ? 'text-green-400' : 'text-white',
            ]"
            to="/inspection"
            class="flex items-center gap-2 rounded-lg py-2 space-x-3"
          >
            <img src="@/assets/img/inspection.svg" alt="" />

            <span class="text-sm font-semibold"> Inspection </span>
          </router-link>

          <!-- <router-link
            :class="[
              $route.name === 'claims' ? 'text-green-400' : 'text-white',
            ]"
            to="/claims"
            class="flex items-center gap-2 rounded-lg py-2 space-x-3"
          >
            <img src="@/assets/img/claims.svg" alt="" />

            <span class="text-sm font-semibold"> Claim </span>
          </router-link> -->
        </nav>

        <nav aria-label="Service Nav" class="flex flex-col space-y-4 pt-10">
          <router-link
            :class="[
              $route.name === 'settings' ? 'text-green-400' : 'text-white',
            ]"
            to="/settings"
            class="flex items-center gap-2 rounded-lg py-2 space-x-3"
          >
            <img src="@/assets/img/settings.svg" alt="" />

            <span class="text-sm font-semibold"> Settings </span>
          </router-link>
        </nav>
      </div>

      <img src="@/assets/img/spiral.svg" alt="" />
    </div>

    <div class="relative">
      <div
        v-if="showSidebar"
        :class="[showSidebar ? 'w-16 z-50' : '']"
        style="background-color: #070707"
        class="lg:hidden flex h-screen absolute flex-col justify-between border-r bg-white"
      >
        <div>
          <div class="inline-flex h-16 w-16 items-center justify-center">
            <span
              class="grid h-10 w-10 place-content-center rounded-lg bg-gray-100 text-xs text-gray-600"
            >
            </span>
          </div>

          <div class="border-t border-gray-100">
            <nav aria-label="Main Nav" class="flex flex-col p-2">
              <div class="py-4">
                <router-link
                  :class="[
                    $route.name === 'index'
                      ? 'text-green-700 bg-green-500'
                      : 'text-white',
                  ]"
                  to="/"
                  class="t group relative flex justify-center rounded px-2 py-1.5 text-blue-700"
                >
                  <img src="@/assets/img/get_started.svg" alt="" />

                  <span
                    class="absolute left-full top-1/2 ml-4 -translate-y-1/2 rounded bg-gray-900 px-2 py-1.5 text-xs font-medium text-white opacity-0 group-hover:opacity-100"
                  >
                    Get Started
                  </span>
                </router-link>
              </div>

              <ul class="border-t space-y-6 border-gray-100 pt-4">
                <li>
                  <router-link
                    :class="[
                      $route.name === 'analytics'
                        ? 'text-green-700 bg-green-500'
                        : 'text-white',
                    ]"
                    to="/analytics"
                    class="t group relative flex justify-center rounded px-2 py-1.5 text-blue-700"
                  >
                    <img src="@/assets/img/analytics.svg" alt="" />
                    <span
                      class="absolute left-full top-1/2 ml-4 -translate-y-1/2 rounded bg-gray-900 px-2 py-1.5 text-xs font-medium text-white opacity-0 group-hover:opacity-100"
                    >
                      Analytics
                    </span>
                  </router-link>
                </li>
                <li>
                  <router-link
                    :class="[
                      $route.name === 'sales'
                        ? 'text-green-700 bg-green-500'
                        : 'text-white',
                    ]"
                    to="/sales"
                    class="t group relative flex justify-center rounded px-2 py-1.5 text-blue-700"
                  >
                    <img src="@/assets/img/sales.svg" alt="" />
                    <span
                      class="absolute left-full top-1/2 ml-4 -translate-y-1/2 rounded bg-gray-900 px-2 py-1.5 text-xs font-medium text-white opacity-0 group-hover:opacity-100"
                    >
                      Sales
                    </span>
                  </router-link>
                </li>
                <li>
                  <router-link
                    :class="[
                      $route.name === 'policies'
                        ? 'text-green-700 bg-green-500'
                        : 'text-white',
                    ]"
                    to="/policies"
                    class="t group relative flex justify-center rounded px-2 py-1.5 text-blue-700"
                  >
                    <img src="@/assets/img/policies.svg" alt="" />
                    <span
                      class="absolute left-full top-1/2 ml-4 -translate-y-1/2 rounded bg-gray-900 px-2 py-1.5 text-xs font-medium text-white opacity-0 group-hover:opacity-100"
                    >
                      Policies
                    </span>
                  </router-link>
                </li>
                <li>
                  <router-link
                    :class="[
                      $route.name === 'products'
                        ? 'text-green-700 bg-green-500'
                        : 'text-white',
                    ]"
                    to="/products"
                    class="t group relative flex justify-center rounded px-2 py-1.5 text-blue-700"
                  >
                    <img src="@/assets/img/products.svg" alt="" />
                    <span
                      class="absolute left-full top-1/2 ml-4 -translate-y-1/2 rounded bg-gray-900 px-2 py-1.5 text-xs font-medium text-white opacity-0 group-hover:opacity-100"
                    >
                      Products
                    </span>
                  </router-link>
                </li>
                <li>
                  <router-link
                    :class="[
                      $route.name === 'customers'
                        ? 'text-green-700 bg-green-500'
                        : 'text-white',
                    ]"
                    to="/customers"
                    class="t group relative flex justify-center rounded px-2 py-1.5 text-blue-700"
                  >
                    <img src="@/assets/img/customer.svg" alt="" />

                    <span
                      class="absolute left-full top-1/2 ml-4 -translate-y-1/2 rounded bg-gray-900 px-2 py-1.5 text-xs font-medium text-white opacity-0 group-hover:opacity-100"
                    >
                      Customers
                    </span>
                  </router-link>
                </li>
                <li>
                  <router-link
                    :class="[
                      $route.name === 'users'
                        ? 'text-green-700 bg-green-500'
                        : 'text-white',
                    ]"
                    to="/users"
                    class="t group relative flex justify-center rounded px-2 py-1.5 text-blue-700"
                  >
                    <img src="@/assets/img/users.svg" alt="" />
                    <span
                      class="absolute left-full top-1/2 ml-4 -translate-y-1/2 rounded bg-gray-900 px-2 py-1.5 text-xs font-medium text-white opacity-0 group-hover:opacity-100"
                    >
                      Users
                    </span>
                  </router-link>
                </li>

                <li>
                  <router-link
                    :class="[
                      $route.name === 'claims'
                        ? 'text-green-700 bg-green-500'
                        : 'text-white',
                    ]"
                    to="/claims"
                    class="t group relative flex justify-center rounded px-2 py-1.5 text-blue-700"
                  >
                    <img src="@/assets/img/claims.svg" alt="" />

                    <span
                      class="absolute left-full top-1/2 ml-4 -translate-y-1/2 rounded bg-gray-900 px-2 py-1.5 text-xs font-medium text-white opacity-0 group-hover:opacity-100"
                    >
                      Claims
                    </span>
                  </router-link>
                </li>

                <li>
                  <router-link
                    :class="[
                      $route.name === 'wallet'
                        ? 'text-green-700 bg-green-500'
                        : 'text-white',
                    ]"
                    to="/wallet"
                    class="t group relative flex justify-center rounded px-2 py-1.5 text-blue-700"
                  >
                    <img src="@/assets/img/wallet.svg" alt="" />

                    <span
                      class="absolute left-full top-1/2 ml-4 -translate-y-1/2 rounded bg-gray-900 px-2 py-1.5 text-xs font-medium text-white opacity-0 group-hover:opacity-100"
                    >
                      Wallet
                    </span>
                  </router-link>
                </li>

                <li>
                  <router-link
                    :class="[
                      $route.name === 'transactionHistory'
                        ? 'text-green-700 bg-green-500'
                        : 'text-white',
                    ]"
                    to="/transactionHistory"
                    class="t group relative flex justify-center rounded px-2 py-1.5 text-blue-700"
                  >
                    <img src="@/assets/img/transactionHistory.svg" alt="" />

                    <span
                      class="absolute left-full top-1/2 ml-4 -translate-y-1/2 rounded bg-gray-900 px-2 py-1.5 text-xs font-medium text-white opacity-0 group-hover:opacity-100"
                    >
                      Transaction History
                    </span>
                  </router-link>
                </li>

                <li>
                  <router-link
                    :class="[
                      $route.name === 'provider'
                        ? 'text-green-700 bg-green-500'
                        : 'text-white',
                    ]"
                    to="/provider"
                    class="t group relative flex justify-center rounded px-2 py-1.5 text-blue-700"
                  >
                    <img src="@/assets/img/users.svg" alt="" />

                    <span
                      class="absolute left-full top-1/2 ml-4 -translate-y-1/2 rounded bg-gray-900 px-2 py-1.5 text-xs font-medium text-white opacity-0 group-hover:opacity-100"
                    >
                      Provider
                    </span>
                  </router-link>
                </li>

                <li>
                  <router-link
                    :class="[
                      $route.name === 'distributors'
                        ? 'text-green-700 bg-green-500'
                        : 'text-white',
                    ]"
                    to="/distributors"
                    class="t group relative flex justify-center rounded px-2 py-1.5 text-blue-700"
                  >
                    <img src="@/assets/img/users.svg" alt="" />

                    <span
                      class="absolute left-full top-1/2 ml-4 -translate-y-1/2 rounded bg-gray-900 px-2 py-1.5 text-xs font-medium text-white opacity-0 group-hover:opacity-100"
                    >
                      Distributors
                    </span>
                  </router-link>
                </li>

                <li>
                  <router-link
                    :class="[
                      $route.name === 'inspection'
                        ? 'text-green-700 bg-green-500'
                        : 'text-white',
                    ]"
                    to="/inspection"
                    class="t group relative flex justify-center rounded px-2 py-1.5 text-blue-700"
                  >
                    <img src="@/assets/img/inspection.svg" alt="" />

                    <span
                      class="absolute left-full top-1/2 ml-4 -translate-y-1/2 rounded bg-gray-900 px-2 py-1.5 text-xs font-medium text-white opacity-0 group-hover:opacity-100"
                    >
                      Inspection
                    </span>
                  </router-link>
                </li>

                <!-- <li>
                  <a
                    href=""
                    class="group relative flex justify-center rounded px-2 py-1.5 text-gray-500 hover:bg-green-500 hover:text-gray-700"
                  >
                    <img src="@/assets/img/claims.svg" alt="" />

                    <span
                      class="absolute left-full top-1/2 ml-4 -translate-y-1/2 rounded bg-gray-900 px-2 py-1.5 text-xs font-medium text-white opacity-0 group-hover:opacity-100"
                    >
                      Claims
                    </span>
                  </a>
                </li> -->

                <li>
                  <router-link
                    :class="[
                      $route.name === 'settings'
                        ? 'text-green-700 bg-green-500'
                        : 'text-white',
                    ]"
                    to="/settings"
                    class="t group relative flex justify-center rounded px-2 py-1.5 text-blue-700"
                  >
                    <img src="@/assets/img/settings.svg" alt="" />

                    <span
                      class="absolute left-full top-1/2 ml-4 -translate-y-1/2 rounded bg-gray-900 px-2 py-1.5 text-xs font-medium text-white opacity-0 group-hover:opacity-100"
                    >
                      Settings
                    </span>
                  </router-link>
                </li>
              </ul>
            </nav>
          </div>
        </div>

        <div
          class="sticky inset-x-0 bottom-0 border-t border-gray-100 bg-white p-2"
        >
          <form action="/logout">
            <button
              type="submit"
              class="group relative flex w-full justify-center rounded-lg px-2 py-1.5 text-sm text-red-500 hover:bg-gray-50 hover:text-gray-700"
            >
              <svg
                xmlns="http://www.w3.org/2000/svg"
                class="h-5 w-5 opacity-75"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
                stroke-width="2"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  d="M17 16l4-4m0 0l-4-4m4 4H7m6 4v1a3 3 0 01-3 3H6a3 3 0 01-3-3V7a3 3 0 013-3h4a3 3 0 013 3v1"
                />
              </svg>

              <span
                class="absolute left-full top-1/2 ml-4 -translate-y-1/2 rounded bg-gray-900 px-2 py-1.5 text-xs font-medium text-red-600 opacity-0 group-hover:opacity-100"
              >
                Logout
              </span>
            </button>
          </form>
        </div>
      </div>
      <div class="pl-6 z-50 absolute top-6 md:hidden">
        <svg
          v-if="!showSidebar"
          @click="toggleSidebar"
          xmlns="http://www.w3.org/2000/svg"
          width="22"
          height="22"
          viewBox="0 0 24 24"
          fill="none"
          stroke="#000000"
          stroke-width="3"
          stroke-linecap="round"
          stroke-linejoin="round"
          class="cursor-pointer"
        >
          <line x1="3" y1="12" x2="21" y2="12"></line>
          <line x1="3" y1="6" x2="21" y2="6"></line>
          <line x1="3" y1="18" x2="21" y2="18"></line>
        </svg>
        <svg
          v-if="showSidebar"
          @click="toggleSidebar"
          xmlns="http://www.w3.org/2000/svg"
          width="22"
          height="22"
          viewBox="0 0 24 24"
          fill="none"
          stroke="#000000"
          stroke-width="4"
          stroke-linecap="round"
          stroke-linejoin="round"
          class="cursor-pointer"
        >
          <line x1="18" y1="6" x2="6" y2="18"></line>
          <line x1="6" y1="6" x2="18" y2="18"></line>
        </svg>
      </div>
    </div>
  </main>
</template>

<script>
export default {
  data() {
    return {
      showSidebar: false,
    };
  },
  mounted() {
    console.log(this.$route.name);
  },
  methods: {
    toggleSidebar() {
      this.showSidebar = !this.showSidebar;
    },
  },
};
</script>