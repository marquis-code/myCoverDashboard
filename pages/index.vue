<template>
  <div
    class="w-full px-3 md:w-10/12 h-screen sticky top-0 overflow-y-auto md:px-14 py-6 space-y-10 bg-slate-50"
  >
    <div
      class="md:flex md:justify-between md:items-center flex-col md:flex-row flex items-end justify-end pr-6 md:pr-0"
    >
      <div>
        <h1 style="color: #360040" class="font-bold text-xl">Claims</h1>
      </div>
      <div class="md:flex items-center md:space-x-6">
        <div class="hidden md:flex">
          <img
            class="h-10 w-10"
            src="@/assets/img/notificationBell.svg"
            alt=""
          />
        </div>
        <div class="hidden md:flex">
          <img
            src="@/assets/img/header_avatar.jpeg"
            class="rounded-full"
            alt=""
          />
        </div>
        <p style="color: #360040" class="lg:text-lg font-bold pb-0 mb-0">
          Hello Alexander
        </p>
      </div>
    </div>

    <div
      class="md:flex justify-end items-center md:space-x-5 md:space-y-0 space-y-6"
    >
      <div
        class="flex justify-center md:justify-start items-center border border-gray-400 space-x-3 px-3 py-3 rounded-lg"
      >
        <label for="SortBy" class="block text-sm font-medium text-gray-700">
          Filters by :
        </label>

        <select
          id="SortBy"
          class="mt-1 rounded border-gray-300 text-sm border-none outline-none"
        >
          <option>All time</option>
          <option value="All time">All time</option>
          <option value="Recent">Recent</option>
          <option value="Last year">Last year</option>
        </select>
      </div>

      <div
        style="background-color: #eaecf0"
        class="flex justify-center md:justify-start space-x-3 items-center border px-2 md:py-2 py-3 rounded-lg"
      >
        <p class="text-xs">12 July - 12 August</p>
        <div class="cursor-pointer">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            width="18"
            height="18"
            viewBox="0 0 24 24"
            fill="none"
            stroke="#000000"
            stroke-width="3"
            stroke-linecap="round"
            stroke-linejoin="round"
          >
            <line x1="18" y1="6" x2="6" y2="18"></line>
            <line x1="6" y1="6" x2="18" y2="18"></line>
          </svg>
        </div>
      </div>
    </div>

    <hr />

    <div class="lg:flex justify-between items-center space-y-6 lg:space-y-0">
      <div>
        <button
          style="background-color: #3baa90"
          class="text-white font-medium rounded-md px-6 py-3 w-full md:w-auto"
        >
          Make Claim
        </button>
      </div>

      <div
        class="md:flex items-center md:space-x-6 md:w-6/12 space-y-6 md:space-y-0"
      >
        <div
          class="lg:rounded-lg place-content-center py-6 rounded-md px-3 lg:py-4 h-26 md:w-3/12"
          style="background-color: #3baa90"
        >
          <p class="text-white font-light text-lg md:text-base">Total Claims</p>
          <h1 class="text-white font-extrabold">2,420</h1>
        </div>

        <div
          class="lg:rounded-lg place-content-center py-6 rounded-md px-6 lg:py-4 h-26 md:w-3/12"
          style="background-color: #7a5af8"
        >
          <p class="text-white font-light text-lg md:text-base">Settled</p>
          <h1 class="text-white font-extrabold">500</h1>
        </div>

        <div
          class="lg:rounded-lg place-content-center py-6 rounded-md px-3 lg:py-4 h-26 md:w-3/12"
          style="background-color: #f5b203"
        >
          <p class="text-white font-light text-lg md:text-base">In progress</p>
          <h1 class="text-white font-extrabold">300</h1>
        </div>

        <div
          class="lg:rounded-lg place-content-center py-6 rounded-md px-3 lg:py-4 h-26 md:w-3/12"
          style="background-color: #f97066"
        >
          <p class="text-white font-light text-lg md:text-base">Rejected</p>
          <h1 class="text-white font-extrabold">1,050</h1>
        </div>
      </div>
    </div>

    <div
      class="space-y-10 bg-white rounded-tr-lg rounded-tl-lg border p-3 md:p-6"
    >
      <div class="lg:flex items-center justify-between space-y-6 lg:space-y-0">
        <div
          class="grid grid-cols-4 divide-x lg:w-3/12 rounded-l-md rounded-r-md h-10 border"
        >
          <div
            class="font-medium text-white text-center flex justify-center items-center text-xs cursor-pointer bg-black hover:bg-black rounded-md hover:text-white"
          >
            All
          </div>
          <div
            class="font-medium text-gray-500 text-center flex justify-center items-center text-xs cursor-pointer hover:bg-black rounded-md hover:text-white"
          >
            Paid
          </div>
          <div
            class="font-medium text-gray-500 text-center flex justify-center items-center text-xs cursor-pointer hover:bg-black rounded-md hover:text-white"
          >
            Pending
          </div>
          <div
            class="font-medium text-gray-500 text-center flex justify-center items-center text-xs cursor-pointer hover:bg-black rounded-md hover:text-white"
          >
            Rejected
          </div>
        </div>

        <div class="lg:flex items-center lg:space-x-5 space-y-6 lg:space-y-0">
          <div class="relative">
            <div>
              <input
                type="search"
                placeholder="Search e.g insurance no. , pro.."
                class="rounded-md px-16 py-3 text-xs border w-full outline-none"
              />
            </div>
            <img
              src="@/assets/img/searchIcon.svg"
              class="absolute top-3 px-6"
              alt=""
            />
          </div>

          <div
            class="flex items-center justify-center lg:justify-start space-x-3 px-5 py-3 border rounded-md cursor-pointer"
          >
            <div><img src="@/assets/img/filterIcon.svg" alt="" /></div>
            <p class="font-medium text-sm">Filters</p>
          </div>

          <div
            style="background-color: #f2f4f7"
            class="flex justify-center lg:justify-start items-center space-x-3 px-5 py-3 border rounded-md cursor-pointer"
          >
            <div><img src="@/assets/img/exportIcon.svg" alt="" /></div>
            <p class="font-medium text-sm text-green-500">Export</p>
          </div>
        </div>
      </div>

      <div class="space-y-2">
        <h1 class="font-bold text-xl" style="color: #141518">All Claims</h1>
        <p class="text-gray-400">245 claims</p>
      </div>
    </div>

    <div>
      <div class="overflow-x-auto">
        <table class="min-w-full divide-y-2 divide-gray-200 text-sm">
          <thead>
            <tr>
              <th
                class="sticky inset-y-0 left-0 bg-gray-50 px-4 py-2 text-left"
              >
                <label for="SelectAll" class="sr-only">Select All</label>

                <input
                  type="checkbox"
                  id="SelectAll"
                  class="h-5 w-5 rounded border-gray-300"
                />
              </th>
              <th
                class="whitespace-nowrap px-4 py-2 text-left font-medium text-gray-900"
              >
                Customer name
              </th>
              <th
                class="whitespace-nowrap px-4 py-2 text-left font-medium text-gray-900"
              >
                Insurance No.
              </th>
              <th
                class="whitespace-nowrap px-4 py-2 text-left font-medium text-gray-900"
              >
                Email address
              </th>
              <th
                class="whitespace-nowrap px-4 py-2 text-left font-medium text-gray-900"
              >
                Phone no
              </th>

              <th
                class="whitespace-nowrap px-4 py-2 text-left font-medium text-gray-900"
              >
                Product
              </th>

              <th
                class="whitespace-nowrap px-4 py-2 text-left font-medium text-gray-900"
              >
                Policy I.D
              </th>

              <th
                class="whitespace-nowrap px-4 py-2 text-left font-medium text-gray-900"
              >
                All time claimed
              </th>

              <th
                class="whitespace-nowrap px-4 py-2 text-left font-medium text-gray-900"
              >
                Date submitted
              </th>
            </tr>
          </thead>

          <tbody class="divide-y divide-gray-100">
            <tr class="py-6">
              <td
                class="sticky inset-y-0 left-0 bg-bg-gray-50 text-sm px-4 py-4"
              >
                <label class="sr-only" for="Row1">Row 1</label>

                <input
                  class="h-5 w-5 rounded border-gray-300"
                  type="checkbox"
                  id="Row1"
                />
              </td>
              <td
                class="whitespace-nowrap px-4 py-4 font-light text-gray-500 text-xs flex items-center space-x-2"
              >
                <img
                  class="rounded-full"
                  src="@/assets/img/table_avatar.svg"
                  alt=""
                />
                <p>Alex Igwe</p>
              </td>
              <td
                class="whitespace-nowrap px-4 py-4 text-gray-500 text-xs font-light"
              >
                IN - 4567899
              </td>
              <td
                class="whitespace-nowrap px-4 py-4 text-gray-500 text-sm font-light"
              >
                alex@gmail.com
              </td>
              <td
                class="whitespace-nowrap px-4 py-4 text-gray-500 text-xs font-light"
              >
                090876542345
              </td>
              <td
                class="whitespace-nowrap px-4 py-4 text-gray-500 text-xs font-light"
              >
                Comprehensive Auto
              </td>
              <td
                class="whitespace-nowrap px-4 py-4 text-gray-500 text-xs font-light"
              >
                RTYUI-12
              </td>
              <td
                class="whitespace-nowrap px-4 py-4 text-gray-500 text-xs font-light text-center"
              >
                2
              </td>
              <td class="whitespace-nowrap px-4 py-4 text-gray-500 text-xs">
                12th Jan 2020
              </td>
            </tr>

            <tr class="py-6">
              <td class="sticky inset-y-0 left-0 bg-gray-50 text-sm px-4 py-4">
                <label class="sr-only" for="Row1">Row 1</label>

                <input
                  class="h-5 w-5 rounded border-gray-300"
                  type="checkbox"
                  id="Row1"
                />
              </td>
              <td
                class="whitespace-nowrap px-4 py-4 font-light text-gray-500 text-xs flex items-center space-x-2"
              >
                <img
                  class="rounded-full"
                  src="@/assets/img/table_avatar.svg"
                  alt=""
                />
                <p>Alex Igwe</p>
              </td>
              <td
                class="whitespace-nowrap px-4 py-4 text-gray-500 text-xs font-light"
              >
                IN - 4567899
              </td>
              <td
                class="whitespace-nowrap px-4 py-4 text-gray-500 text-sm font-light"
              >
                alex@gmail.com
              </td>
              <td
                class="whitespace-nowrap px-4 py-4 text-gray-500 text-xs font-light"
              >
                090876542345
              </td>
              <td
                class="whitespace-nowrap px-4 py-4 text-gray-500 text-xs font-light"
              >
                Comprehensive Auto
              </td>
              <td
                class="whitespace-nowrap px-4 py-4 text-gray-500 text-xs font-light"
              >
                RTYUI-12
              </td>
              <td
                class="whitespace-nowrap px-4 py-4 text-gray-500 text-xs font-light text-center"
              >
                2
              </td>
              <td class="whitespace-nowrap px-4 py-4 text-gray-500 text-xs">
                12th Jan 2020
              </td>
            </tr>

            <tr class="py-6">
              <td
                class="sticky inset-y-0 left-0 bg-bg-gray-50 text-sm px-4 py-4"
              >
                <label class="sr-only" for="Row1">Row 1</label>

                <input
                  class="h-5 w-5 rounded border-gray-300"
                  type="checkbox"
                  id="Row1"
                />
              </td>
              <td
                class="whitespace-nowrap px-4 py-4 font-light text-gray-500 text-xs flex items-center space-x-2"
              >
                <img
                  class="rounded-full"
                  src="@/assets/img/table_avatar.svg"
                  alt=""
                />
                <p>Alex Igwe</p>
              </td>
              <td
                class="whitespace-nowrap px-4 py-4 text-gray-500 text-xs font-light"
              >
                IN - 4567899
              </td>
              <td
                class="whitespace-nowrap px-4 py-4 text-gray-500 text-sm font-light"
              >
                alex@gmail.com
              </td>
              <td
                class="whitespace-nowrap px-4 py-4 text-gray-500 text-xs font-light"
              >
                090876542345
              </td>
              <td
                class="whitespace-nowrap px-4 py-4 text-gray-500 text-xs font-light"
              >
                Comprehensive Auto
              </td>
              <td
                class="whitespace-nowrap px-4 py-4 text-gray-500 text-xs font-light"
              >
                RTYUI-12
              </td>
              <td
                class="whitespace-nowrap px-4 py-4 text-gray-500 text-xs font-light text-center"
              >
                2
              </td>
              <td class="whitespace-nowrap px-4 py-4 text-gray-500 text-xs">
                12th Jan 2020
              </td>
            </tr>

            <tr class="py-6">
              <td
                class="sticky inset-y-0 left-0 bg-bg-gray-50 text-sm px-4 py-4"
              >
                <label class="sr-only" for="Row1">Row 1</label>

                <input
                  class="h-5 w-5 rounded border-gray-300"
                  type="checkbox"
                  id="Row1"
                />
              </td>
              <td
                class="whitespace-nowrap px-4 py-4 font-light text-gray-500 text-xs flex items-center space-x-2"
              >
                <img
                  class="rounded-full"
                  src="@/assets/img/table_avatar.svg"
                  alt=""
                />
                <p>Alex Igwe</p>
              </td>
              <td
                class="whitespace-nowrap px-4 py-4 text-gray-500 text-xs font-light"
              >
                IN - 4567899
              </td>
              <td
                class="whitespace-nowrap px-4 py-4 text-gray-500 text-sm font-light"
              >
                alex@gmail.com
              </td>
              <td
                class="whitespace-nowrap px-4 py-4 text-gray-500 text-xs font-light"
              >
                090876542345
              </td>
              <td
                class="whitespace-nowrap px-4 py-4 text-gray-500 text-xs font-light"
              >
                Comprehensive Auto
              </td>
              <td
                class="whitespace-nowrap px-4 py-4 text-gray-500 text-xs font-light"
              >
                RTYUI-12
              </td>
              <td
                class="whitespace-nowrap px-4 py-4 text-gray-500 text-xs font-light text-center"
              >
                2
              </td>
              <td class="whitespace-nowrap px-4 py-4 text-gray-500 text-xs">
                12th Jan 2020
              </td>
            </tr>
          </tbody>
        </table>
      </div>

      <div class="flex justify-end items-end">
        <ol class="flex justify-center gap-1 text-xs font-medium">
          <li>
            <a
              href="#"
              class="inline-flex h-8 w-8 items-center justify-center rounded border border-gray-100"
            >
              <span class="sr-only">Prev Page</span>
              <svg
                xmlns="http://www.w3.org/2000/svg"
                class="h-3 w-3"
                viewBox="0 0 20 20"
                fill="currentColor"
              >
                <path
                  fill-rule="evenodd"
                  d="M12.707 5.293a1 1 0 010 1.414L9.414 10l3.293 3.293a1 1 0 01-1.414 1.414l-4-4a1 1 0 010-1.414l4-4a1 1 0 011.414 0z"
                  clip-rule="evenodd"
                />
              </svg>
            </a>
          </li>

          <li>
            <a
              href="#"
              class="block h-8 w-8 rounded border border-gray-100 text-center leading-8"
            >
              1
            </a>
          </li>

          <li
            class="block h-8 w-8 rounded border-blue-600 bg-blue-600 text-center leading-8 text-white"
          >
            2
          </li>

          <li>
            <a
              href="#"
              class="block h-8 w-8 rounded border border-gray-100 text-center leading-8"
            >
              3
            </a>
          </li>

          <li>
            <a
              href="#"
              class="block h-8 w-8 rounded border border-gray-100 text-center leading-8"
            >
              4
            </a>
          </li>

          <li>
            <a
              href="#"
              class="inline-flex h-8 w-8 items-center justify-center rounded border border-gray-100"
            >
              <span class="sr-only">Next Page</span>
              <svg
                xmlns="http://www.w3.org/2000/svg"
                class="h-3 w-3"
                viewBox="0 0 20 20"
                fill="currentColor"
              >
                <path
                  fill-rule="evenodd"
                  d="M7.293 14.707a1 1 0 010-1.414L10.586 10 7.293 6.707a1 1 0 011.414-1.414l4 4a1 1 0 010 1.414l-4 4a1 1 0 01-1.414 0z"
                  clip-rule="evenodd"
                />
              </svg>
            </a>
          </li>
        </ol>
      </div>
    </div>
  </div>
</template>

<script>
useHead({
  title: "Dashboard",
  meta: [{ name: "description", content: "My cover amazing dashboard." }],
  bodyAttrs: {
    class: "test",
  },
  script: [{ innerHTML: "console.log('Hello world')" }],
});
export default {};
</script>

<style>
</style>