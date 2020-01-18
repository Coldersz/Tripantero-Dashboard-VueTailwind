<template>
  <div class="font-montserrat">
    <div class="px-10 py-12 bg-gray-100">
      <div class="flex justify-center">
        <h1 class="text-4xl font-montserrat text-center">Dashboard</h1>
      </div>
      <div class="flex justify-center">
        <table class="w-48">
          <tr>
            <td class>
              <div class="bg-gray-400 h-px leading-px">&zwnj;</div>
            </td>
          </tr>
        </table>
      </div>
      <div class="mt-20">
        <div class="rounded border-2 bg-white shadow-md">
          <div class="flex justify-end px-2 py-2">
            <button
              class="font-montserrat text-gray-600 focus:outline-none hover:bg-gray-200"
              @click="check = !check"
            >
              View Details
              <img src="/img/forward.svg" class="h-4 inline" alt="arrow" />
            </button>
          </div>
          <div class="px-3">
            <table class="w-full">
              <tr>
                <td class>
                  <div class="bg-gray-400 h-px leading-px">&zwnj;</div>
                </td>
              </tr>
            </table>
          </div>
          <div class="px-6 py-6 justify-center md:flex block">
            <div class="w-full md:w-1/3 rounded-lg block md:inline-block mx-2 my-2 shadow-md">
              <div class="bg-blue-500 rounded-lg">
                <div class="flex justify-between">
                  <div class="text-white px-5 py-5">
                    <p class="block text-base">Your Trips</p>
                    <p class="block text-4xl py-1">{{trips.length}}</p>
                  </div>
                  <div class="px-4 py-6">
                    <img src="/img/rocket.svg" alt="transport" class="h-20" />
                  </div>
                </div>
              </div>
              <div class="mx-3 my-3" v-show="check">
                <div class="text-base text-gray-600 bg-blue-100 rounded-lg py-1 mb-5">
                  <ul class="list-disc mx-6 text-justify">
                    <li class="mx-1" v-for="trip in trips" :key="trip.id">
                      <div class="text-blue-500">{{trip.spot}}</div>
                      <div class="text-right">{{trip.date}}</div>
                      <table class="w-full">
                        <tr>
                          <td class>
                            <div class="bg-gray-400 h-px leading-px">&zwnj;</div>
                          </td>
                        </tr>
                      </table>
                    </li>
                  </ul>
                </div>
              </div>
            </div>
            <div class="w-full md:w-1/3 rounded-lg block md:inline-block mx-2 my-2 shadow-md">
              <div class="bg-teal-400 rounded-lg">
                <div class="flex justify-between">
                  <div class="text-white px-5 py-5">
                    <p class="block text-base">Your Reservation</p>
                    <p class="block text-4xl py-1">5</p>
                  </div>
                  <div class="px-4 py-6">
                    <img src="/img/scheduling.svg" alt="transport" class="h-20" />
                  </div>
                </div>
              </div>
              <div class="mx-3 my-3" v-show="check">
                <div class="text-base text-gray-600 bg-teal-100 rounded-lg py-1 mb-5">
                  <ul class="list-disc mx-6 text-justify">
                    <li class="mx-1" v-for="reservation in reservations" :key="reservation.id">
                      <div class="text-teal-500">{{reservation.place}}</div>
                      <div class="text-right">{{reservation.date}}</div>
                      <table class="w-full">
                        <tr>
                          <td class>
                            <div class="bg-gray-400 h-px leading-px">&zwnj;</div>
                          </td>
                        </tr>
                      </table>
                    </li>
                  </ul>
                </div>
              </div>
            </div>
            <div class="w-full md:w-1/3 rounded-lg block md:inline-block mx-2 my-2 shadow-md">
              <div class="bg-yellow-500 rounded-lg">
                <div class="flex justify-between">
                  <div class="text-white px-5 py-5">
                    <p class="block text-base">Total Payments</p>
                    <p class="block text-4xl py-1">Rp 0,-</p>
                  </div>
                  <div class="px-4 py-6">
                    <img src="/img/business-and-finance.svg" alt="transport" class="h-20" />
                  </div>
                </div>
              </div>
              <div class="mx-3 my-3" v-show="check">
                <div class="text-base text-gray-600 bg-yellow-100 rounded-lg py-1 mb-5">
                  <ul class="list-disc mx-6 text-justify">
                    <li class="mx-1">
                      <div class="text-yellow-500">List</div>
                      <table class="w-full">
                        <tr>
                          <td class>
                            <div class="bg-gray-400 h-px leading-px">&zwnj;</div>
                          </td>
                        </tr>
                      </table>
                    </li>
                  </ul>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="my-12">
        <div class="xl:inline block w-full xl:flex">
          <div class="rounded border-2 bg-white shadow-md w-full xl:w-2/3 xl:mr-2">
            <div class="py-5">
              <h2
                class="text-center uppercase tracking-wider text-2xl text-gray-600"
              >time until your next trip</h2>
            </div>
            <div class="px-6 justify-center flex">
              <div class="sm:px-4 px-1 py-5 text-center w-1/3">
                <div class="text-5xl sm:text-6xl text-green-500">00</div>
                <div class="text-base text-gray-600">Years</div>
              </div>
              <div class="sm:px-4 px-1 py-5 text-center w-1/3">
                <div class="text-5xl sm:text-6xl text-green-500">00</div>
                <div class="text-base text-gray-600">Months</div>
              </div>
              <div class="sm:px-4 px-1 py-5 text-center w-1/3">
                <div class="text-5xl sm:text-6xl text-green-500">00</div>
                <div class="text-base text-gray-600">Days</div>
              </div>
            </div>
            <div class="py-2">
              <h3 class="text-center uppercase text-xl text-green-500">Trip to london</h3>
            </div>
            <div class="pb-6">
              <h3 class="text-center text-base text-gray-600">November 18, 2020</h3>
            </div>
          </div>
          <div class="rounded border-2 bg-white shadow-md w-full xl:w-1/3 xl:ml-2 my-12 sm:my-0">
            <div class="py-5">
              <h2 class="text-center uppercase tracking-wider text-2xl text-gray-600">upcoming trips</h2>
            </div>
            <div class="carousel relative shadow-2xl bg-white">
              <div class="carousel-inner relative overflow-hidden w-full">
                <!--Slide 1-->
                <input
                  class="carousel-open"
                  type="radio"
                  id="carousel-1"
                  name="carousel"
                  aria-hidden="true"
                  hidden
                  checked="checked"
                />
                <div class="carousel-item absolute opacity-0" style="height:50vh;">
                  <div
                    class="block h-full w-full bg-indigo-500 text-white text-5xl text-center font-montserrat"
                  >Slide 1</div>
                </div>
                <label
                  for="carousel-3"
                  class="prev control-1 w-10 h-10 ml-2 md:ml-10 absolute cursor-pointer hidden text-3xl font-bold text-black hover:text-white rounded-full bg-white hover:bg-blue-700 leading-tight text-center z-10 inset-y-0 left-0 my-auto"
                >‹</label>
                <label
                  for="carousel-2"
                  class="next control-1 w-10 h-10 mr-2 md:mr-10 absolute cursor-pointer hidden text-3xl font-bold text-black hover:text-white rounded-full bg-white hover:bg-blue-700 leading-tight text-center z-10 inset-y-0 right-0 my-auto"
                >›</label>

                <!--Slide 2-->
                <input
                  class="carousel-open"
                  type="radio"
                  id="carousel-2"
                  name="carousel"
                  aria-hidden="true"
                  hidden
                />
                <div class="carousel-item absolute opacity-0" style="height:50vh;">
                  <div
                    class="block h-full w-full bg-orange-500 text-white text-5xl text-center"
                  >Slide 2</div>
                </div>
                <label
                  for="carousel-1"
                  class="prev control-2 w-10 h-10 ml-2 md:ml-10 absolute cursor-pointer hidden text-3xl font-bold text-black hover:text-white rounded-full bg-white hover:bg-blue-700 leading-tight text-center z-10 inset-y-0 left-0 my-auto"
                >‹</label>
                <label
                  for="carousel-3"
                  class="next control-2 w-10 h-10 mr-2 md:mr-10 absolute cursor-pointer hidden text-3xl font-bold text-black hover:text-white rounded-full bg-white hover:bg-blue-700 leading-tight text-center z-10 inset-y-0 right-0 my-auto"
                >›</label>

                <!--Slide 3-->
                <input
                  class="carousel-open"
                  type="radio"
                  id="carousel-3"
                  name="carousel"
                  aria-hidden="true"
                  hidden
                />
                <div class="carousel-item absolute opacity-0" style="height:50vh;">
                  <div
                    class="block h-full w-full bg-green-500 text-white text-5xl text-center"
                  >Slide 3</div>
                </div>
                <label
                  for="carousel-2"
                  class="prev control-3 w-10 h-10 ml-2 md:ml-10 absolute cursor-pointer hidden text-3xl font-bold text-black hover:text-white rounded-full bg-white hover:bg-blue-700 leading-tight text-center z-10 inset-y-0 left-0 my-auto"
                >‹</label>
                <label
                  for="carousel-1"
                  class="next control-3 w-10 h-10 mr-2 md:mr-10 absolute cursor-pointer hidden text-3xl font-bold text-black hover:text-white rounded-full bg-white hover:bg-blue-700 leading-tight text-center z-10 inset-y-0 right-0 my-auto"
                >›</label>

                <!-- Add additional indicators for each slide-->
                <ol class="carousel-indicators">
                  <li class="inline-block mr-3">
                    <label
                      for="carousel-1"
                      class="carousel-bullet cursor-pointer block text-4xl text-white hover:text-blue-700"
                    >•</label>
                  </li>
                  <li class="inline-block mr-3">
                    <label
                      for="carousel-2"
                      class="carousel-bullet cursor-pointer block text-4xl text-white hover:text-blue-700"
                    >•</label>
                  </li>
                  <li class="inline-block mr-3">
                    <label
                      for="carousel-3"
                      class="carousel-bullet cursor-pointer block text-4xl text-white hover:text-blue-700"
                    >•</label>
                  </li>
                </ol>
              </div>
            </div>
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
      check: false,
      trips: [
        { spot: "Manchester", date: "February 16, 2019" },
        { spot: "Rio De Janeiro", date: "May 22, 2019" },
        { spot: "Istanbul", date: "October 3, 2019" },
        { spot: "Bali", date: "Januray 18, 2020" },
        { spot: "Singapore", date: "June 24, 2020" }
      ],
      reservations: [
        { place: "Jakarta", date: "February 7, 2019" },
        { place: "Jakarta", date: "February 7, 2019" },
        { place: "Jakarta", date: "February 7, 2019" }
      ]
    };
  }
};
</script>

<style scoped>
.carousel-open:checked + .carousel-item {
  position: static;
  opacity: 100;
}
.carousel-item {
  -webkit-transition: opacity 0.6s ease-out;
  transition: opacity 0.6s ease-out;
}
#carousel-1:checked ~ .control-1,
#carousel-2:checked ~ .control-2,
#carousel-3:checked ~ .control-3 {
  display: block;
}
.carousel-indicators {
  list-style: none;
  margin: 0;
  padding: 0;
  position: absolute;
  bottom: 2%;
  left: 0;
  right: 0;
  text-align: center;
  z-index: 10;
}
#carousel-1:checked
  ~ .control-1
  ~ .carousel-indicators
  li:nth-child(1)
  .carousel-bullet,
#carousel-2:checked
  ~ .control-2
  ~ .carousel-indicators
  li:nth-child(2)
  .carousel-bullet,
#carousel-3:checked
  ~ .control-3
  ~ .carousel-indicators
  li:nth-child(3)
  .carousel-bullet {
  color: #2b6cb0; /*Set to match the Tailwind colour you want the active one to be */
}
</style>