<template>
  <div class="w-full">
    <div
      :class="[showClaimModal ? 'z-0' : '']"
      class="px-3 w-full h-screen sticky top-0 overflow-y-auto md:px-14 py-6 space-y-10 bg-slate-50"
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
        class="md:flex md:justify-between md:flex-row flex flex-col-reverse md:items-center bg-white rounded-lg py-4 space-y-6 md:space-y-0"
      >
        <div class="pl-10 space-y-2 py-6 md:py-0">
          <h1 class="font-bold text-gray-400 text-2xl">Make Claim</h1>
          <p class="text-sm text-gray-500 font-light">
            Select a product to make claim on
          </p>
        </div>
        <div class="pl-6 md:pl-0">
          <img src="@/assets/img/claimOffer.svg" alt="" />
        </div>
      </div>

      <div class="md:flex justify-between items-center space-y-6 md:space-y-0">
        <div
          class="border border-gray-100 lg:w-9/12 py-3 rounded-lg bg-white relative"
        >
          <input
            type="search"
            placeholder="Search product"
            class="w-full placeholder-gray-400 outline-none pl-10 text-sm font-medium"
          />
          <img
            class="absolute top-4 left-4"
            src="@/assets/img/searchIcon.svg"
            alt=""
          />
        </div>

        <div
          class="flex px-4 py-3 justify-center md:justify-start items-center border border-gray-400 rounded-lg"
        >
          <label for="SortBy" class="block text-sm font-medium text-gray-700">
            Filters by :
          </label>

          <select
            id="SortBy"
            class="mt-1 rounded border-gray-300 text-sm border-none outline-none font-medium"
          >
            <option class="font-medium text-sm">All products</option>
            <option class="font-medium text-sm" value="All time">
              Latest products
            </option>
            <option class="font-medium text-sm" value="Recent">
              Recent products
            </option>
          </select>
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
                  Product Name
                </th>
                <th
                  class="whitespace-nowrap px-4 py-2 text-left font-medium text-gray-900"
                >
                  Product Category
                </th>
                <th
                  class="whitespace-nowrap px-4 py-2 text-left font-medium text-gray-900"
                >
                  Provider
                </th>
                <th
                  class="whitespace-nowrap px-4 py-2 text-left font-medium text-gray-900"
                >
                  Distributor
                </th>

                <th
                  class="whitespace-nowrap px-4 py-2 text-left font-medium text-gray-900"
                >
                  Product I.D
                </th>

                <th
                  class="whitespace-nowrap px-4 py-2 text-left font-medium text-gray-900"
                >
                  No. customer
                </th>

                <th
                  class="whitespace-nowrap px-4 py-2 text-left font-medium text-gray-900"
                >
                  Date added
                </th>

                <th
                  class="whitespace-nowrap px-4 py-2 text-left font-medium text-gray-900"
                >
                  Policy status
                </th>

                <th
                  class="whitespace-nowrap px-4 py-2 text-left font-medium text-gray-900"
                >
                  Actions
                </th>
              </tr>
            </thead>

            <tbody class="divide-y divide-gray-100">
              <tr v-for="(claim, index) in claims" :key="index" class="py-6">
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
                    v-if="claim.imageUrl == 'flexiCare'"
                    class="rounded-full"
                    src="@/assets/img/flexiCare.svg"
                    alt=""
                  />

                  <img
                    v-if="claim.imageUrl == 'thirdParty'"
                    class="rounded-full"
                    src="@/assets/img/thirdParty.svg"
                    alt=""
                  />

                  <img
                    v-if="claim.imageUrl == 'creditLife'"
                    class="rounded-full"
                    src="@/assets/img/creditLife.svg"
                    alt=""
                  />
                  <p class="font-semibold">{{ claim.productName }}</p>
                </td>
                <td
                  class="whitespace-nowrap px-4 py-4 text-gray-500 text-xs font-light text-center"
                >
                  {{ claim.productCategory }}
                </td>
                <td
                  class="whitespace-nowrap px-4 py-4 text-gray-500 text-sm font-light text-center"
                >
                  {{ claim.productProvider }}
                </td>
                <td
                  class="whitespace-nowrap px-4 py-4 text-gray-500 text-xs font-light text-center"
                >
                  {{ claim.distributor }}
                </td>
                <td
                  class="whitespace-nowrap px-4 py-4 text-gray-500 text-xs font-light text-center"
                >
                  {{ claim.productId }}
                </td>
                <td
                  class="whitespace-nowrap px-4 py-4 text-gray-500 text-xs font-light text-center"
                >
                  {{ claim.customerCount }}
                </td>
                <td
                  class="whitespace-nowrap px-4 py-4 text-gray-500 text-xs font-light text-center"
                >
                  {{ claim.dateAdded }}
                </td>
                <td
                  class="whitespace-nowrap px-4 py-4 text-gray-500 text-xs text-center"
                >
                  <div
                    :style="[
                      claim.policyStatus === 'active'
                        ? 'background-color: #d8eee9'
                        : claim.policyStatus === 'inactive'
                        ? 'background-color: #FFFAEB'
                        : claim.policyStatus === 'deactivated'
                        ? 'background-color: #FEF3F2'
                        : '',
                    ]"
                    class="py-2 px-3 rounded-full flex items-center justify-center space-x-1 text-xs font-medium"
                  >
                    <div
                      :style="[
                        claim.policyStatus === 'active'
                          ? 'background-color: #12B76A'
                          : claim.policyStatus === 'inactive'
                          ? 'background-color: #F79009'
                          : claim.policyStatus === 'deactivated'
                          ? 'background-color: #F04438'
                          : '',
                      ]"
                      class="h-2 w-2 rounded-full"
                    ></div>
                    <div
                      :class="[
                        claim.policyStatus === 'active'
                          ? 'text-green-600'
                          : claim.policyStatus === 'inactive'
                          ? 'text-yellow-600'
                          : claim.policyStatus === 'deactivated'
                          ? 'text-red-600'
                          : '',
                      ]"
                      class="text-xs"
                    >
                      {{ claim.policyStatus }}
                    </div>
                  </div>
                </td>

                <td class="whitespace-nowrap px-4 py-4 text-gray-500 text-xs">
                  <span
                    style="background-color: #d8eee9"
                    class="py-2 px-3 rounded-lg text-xs font-medium text-green-600 cursor-pointer"
                    @click="handleClaim"
                  >
                    Claim</span
                  >
                </td>
              </tr>
            </tbody>
          </table>
        </div>
      </div>
    </div>

    <div
      v-if="showClaimModal"
      class="backdrop backdrop-blur-sm overflow-x-hidden overflow-y-auto fixed inset-0 z-50 outline-none focus:outline-none justify-center items-center flex"
    >
      <div class="absolute top-10 right-0 md:ml-32">
        <img
          src="@/assets/img/close.svg"
          class="cursor-pointer"
          @click="showClaimModal = !showClaimModal"
          alt=""
        />
      </div>

      <div
        :class="[showClaimModal ? 'z-50' : '']"
        class="w-11/12 md:w-5/12 absolute top-0 right-0 h-screen bg-white p-5 md:p-10 shadow-md"
      >
        <img
          src="@/assets/img/close.svg"
          class="cursor-pointer"
          @click="showClaimModal = !showClaimModal"
          alt=""
        />
        <div class="flex justify-between items-center bg-white rounded-lg pb-6">
          <div class="space-y-2">
            <h1 style="color: #1e1f20" class="font-bold text-3xl">
              Claim /
              <span class="text-green-400" style="color: #3baa90"
                >Credit Life</span
              >
            </h1>
            <p class="text-sm text-gray-500 font-light">
              Select the Customer you are making claim on
            </p>
          </div>
        </div>

        <hr />

        <div
          class="md:flex justify-between items-center py-10 space-y-6 md:space-y-0"
        >
          <div
            class="border border-gray-200 md:w-8/12 py-3 rounded-lg bg-white relative shadow-sm"
          >
            <input
              type="search"
              placeholder="Search Customer"
              class="w-full placeholder-gray-400 outline-none pl-10 text-sm font-medium"
            />
            <img
              class="absolute top-4 left-4"
              src="@/assets/img/searchIcon.svg"
              alt=""
            />
          </div>

          <div
            class="flex px-4 py-3 justify-center md:justify-start items-center border border-gray-400 shadow-sm rounded-lg"
          >
            <label for="SortBy" class="block text-sm font-medium text-gray-700">
              Filters by :
            </label>

            <select
              id="SortBy"
              class="mt-1 rounded border-gray-300 text-sm border-none outline-none font-medium"
            >
              <option class="font-medium text-sm">All</option>
              <option class="font-medium text-sm" value="All time">
                Latest
              </option>
            </select>
          </div>
        </div>

        <div>
          <div class="overflow-x-auto">
            <table class="min-w-full divide-y-2 divide-gray-200 text-sm">
              <thead>
                <tr>
                  <th
                    class="whitespace-nowrap px-4 py-2 text-left text-sm text-gray-500"
                  >
                    <span class="text-xs font-medium"> Customer name</span>
                  </th>
                  <th
                    class="whitespace-nowrap px-4 py-2 text-left text-sm text-gray-500"
                  >
                    <span class="text-xs font-medium">Policy No.</span>
                  </th>
                  <th
                    class="whitespace-nowrap px-4 py-2 text-left text-sm text-gray-500"
                  >
                    <span class="text-xs font-medium">Total Claimed</span>
                  </th>
                  <th
                    class="whitespace-nowrap px-4 py-2 text-left text-sm text-gray-500"
                  >
                    <span class="text-xs font-medium">Status</span>
                  </th>

                  <th
                    class="whitespace-nowrap px-4 py-2 text-left text-sm text-gray-500"
                  >
                    <span class="text-xs font-medium">Action</span>
                  </th>
                </tr>
              </thead>

              <tbody class="divide-y divide-gray-100">
                <tr
                  v-for="(claim, index) in singleClaims"
                  :key="index"
                  class="py-6"
                >
                  <td
                    class="whitespace-nowrap px-4 py-4 font-light text-gray-500 text-xs flex space-x-2"
                  >
                    <p>{{ claim.customerName }}</p>
                  </td>
                  <td
                    class="whitespace-nowrap px-4 py-4 text-gray-500 text-xs font-light"
                  >
                    {{ claim.policyNumber }}
                  </td>
                  <td
                    class="whitespace-nowrap px-4 py-4 text-gray-500 text-sm font-light"
                  >
                    {{ claim.totalClaimed }}
                  </td>
                  <td
                    class="whitespace-nowrap px-4 py-4 text-gray-500 text-xs font-light"
                  >
                    <div
                      :style="[
                        claim.status === 'Active'
                          ? 'background-color: #d8eee9'
                          : claim.status === 'Inactive'
                          ? 'background-color: #FFFAEB'
                          : claim.status === 'Expired'
                          ? 'background-color: #FEF3F2'
                          : '',
                      ]"
                      class="py-2 px-3 rounded-full flex items-center justify-center space-x-1 text-xs font-medium"
                    >
                      <div
                        :style="[
                          claim.status === 'Active'
                            ? 'background-color: #12B76A'
                            : claim.status === 'Inactive'
                            ? 'background-color: #F79009'
                            : claim.status === 'Expired'
                            ? 'background-color: #F04438'
                            : '',
                        ]"
                        class="h-2 w-2 rounded-full"
                      ></div>
                      <div
                        :class="[
                          claim.status === 'Active'
                            ? 'text-green-600'
                            : claim.status === 'Inactive'
                            ? 'text-yellow-600'
                            : claim.status === 'Expired'
                            ? 'text-red-600'
                            : '',
                        ]"
                        class="text-xs"
                      >
                        {{ claim.status }}
                      </div>
                    </div>
                  </td>
                  <td
                    class="whitespace-nowrap px-4 py-4 text-xs text-center font-bold text-green-700 cursor-pointer"
                  >
                    Select
                  </td>
                </tr>
              </tbody>
            </table>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      showClaimModal: false,
      claims: [
        {
          imageUrl: "flexiCare",
          productName: "Flexicare",
          productCategory: "Health",
          productProvider: "Hygeia",
          distributor: "Fincra",
          productId: "PR23456",
          customerCount: "30",
          dateAdded: "12th Jan 2020",
          policyStatus: "active",
        },
        {
          imageUrl: "thirdParty",
          productName: "3rd Party",
          productCategory: "Auto",
          productProvider: "AIICO",
          distributor: "Blackcopper",
          productId: "PR23456",
          customerCount: "20",
          dateAdded: "PR23456",
          policyStatus: "deactivated",
        },
        {
          imageUrl: "creditLife",
          productName: "Credit life",
          productCategory: "Credit life",
          productProvider: "Arm life Plc",
          distributor: "Payday",
          productId: "PR23456",
          customerCount: "10",
          dateAdded: "12th Jan 2020",
          policyStatus: "inactive",
        },
      ],

      singleClaims: [
        {
          customerName: "Ajayi Ibrahim",
          policyNumber: "IN - 123455",
          totalClaimed: "0",
          status: "Active",
        },
        {
          customerName: "Chuks Alex",
          policyNumber: "IN - 123455",
          totalClaimed: "1",
          status: "Expired",
        },
        {
          customerName: "Ajayi Ibrahim",
          policyNumber: "IN - 123455",
          totalClaimed: "0",
          status: "Active",
        },
        {
          customerName: "Chuks Alex",
          policyNumber: "IN - 123455",
          totalClaimed: "1",
          status: "Expired",
        },
      ],
    };
  },
  methods: {
    handleClaim() {
      this.showClaimModal = !this.showClaimModal;
    },
  },
};
</script>

<style scoped>
.backdrop {
  background-color: rgba(0, 0, 0, 0.5);
  height: 100vh;
  width: 100vw;
}
</style>