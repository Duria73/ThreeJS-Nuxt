<template>
  <!-- content -->
  <div>
    <nav class="bg-white-800">
      <div class="max-w-7xl mx-auto px-2 sm:px-6 lg:px-8">
        <div class="relative flex items-center justify-between h-20">
          <div
            class="hamburger absolute inset-y-0 left-0 flex items-center sm:hidden"
          >
            <!-- Mobile menu button-->
            <button
              type="button"
              class="inline-flex items-center justify-center p-2 rounded-md text-gray-400 hover:text-white hover:bg-gray-700 focus:outline-none focus:ring-2 focus:ring-inset focus:ring-white"
              aria-controls="mobile-menu"
              aria-expanded="false"
            >
              <span class="sr-only">Open main menu</span>
              <!--
            Icon when menu is closed.

            Heroicon name: outline/menu

            Menu open: "hidden", Menu closed: "block"
          -->
              <svg
                class="block h-6 w-6"
                xmlns="http://www.w3.org/2000/svg"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
                aria-hidden="true"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M4 6h16M4 12h16M4 18h16"
                />
              </svg>
              <!--
            Icon when menu is open.

            Heroicon name: outline/x

            Menu open: "block", Menu closed: "hidden"
          -->
              <svg
                class="hidden h-6 w-6"
                xmlns="http://www.w3.org/2000/svg"
                fill="none"
                viewBox="0 0 24 24"
                stroke="currentColor"
                aria-hidden="true"
              >
                <path
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="M6 18L18 6M6 6l12 12"
                />
              </svg>
            </button>
          </div>
          <div
            class="flex-1 flex items-center justify-center sm:items-stretch sm:justify-start"
          >
            <div class="flex-shrink-0 flex items-center">
              <img
                class="block lg:hidden h-8 w-auto"
                src="../assets/logo.png"
                alt="Workflow"
              />
              <img
                class="hidden lg:block h-8 w-auto"
                src="../assets/logo.png"
                alt="Workflow"
              />
            </div>
            <div class="hidden sm:block sm:ml-6">
              <div class="flex space-x-6">
                <!-- Current: "bg-gray-900 text-white", Default: "text-gray-300 hover:bg-gray-700 hover:text-white" -->
                <a
                  href="/"
                  class="bg-gray-900 text-white px-3 py-2 rounded-md text-sm font-medium"
                  aria-current="page"
                  >Home</a
                >

                <a
                  href="#"
                  class="text-black-400 hover:bg-gray-700 hover:text-white px-3 py-2 rounded-md text-medium font-medium"
                  >About</a
                >

                <a
                  href="#"
                  class="text-black-400 hover:bg-gray-700 hover:text-white px-3 py-2 rounded-md text-medium font-medium"
                  >Projects</a
                >

                <a
                  href="#"
                  class="text-black-400 hover:bg-gray-700 hover:text-white px-3 py-2 rounded-md text-medium font-medium"
                  >Blog</a
                >
                <a
                  href="#"
                  class="text-black-400 hover:bg-gray-700 hover:text-white px-3 py-2 rounded-md text-medium font-medium"
                  >Contact</a
                >
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- Mobile menu, show/hide based on menu state. -->
      <div class="sm:hidden hidden" id="mobile-menu">
        <div class="px-2 pt-2 pb-3 space-y-1">
          <!-- Current: "bg-gray-900 text-white", Default: "text-gray-300 hover:bg-gray-700 hover:text-white" -->
          <a
            href="#"
            class="bg-gray-900 text-white block px-3 py-2 rounded-md text-base font-medium"
            aria-current="page"
            >About</a
          >

          <a
            href="#"
            class="text-gray-300 hover:bg-gray-700 hover:text-white block px-3 py-2 rounded-md text-base font-medium"
            >Projects</a
          >

          <a
            href="#"
            class="text-gray-300 hover:bg-gray-700 hover:text-white block px-3 py-2 rounded-md text-base font-medium"
            >Blog</a
          >

          <a
            href="#"
            class="text-gray-300 hover:bg-gray-700 hover:text-white block px-3 py-2 rounded-md text-base font-medium"
            >Contact</a
          >
        </div>
      </div>
    </nav>

    <!--overflow-hidden absolute top-56 right-0 left-0 -->
    <!--About Section -->
    <div
      class="py-12 flex justify-items-center align-items-center bg-black landing sm:h-auto"
    >
      <div
        class="lg:my-32 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 bg-white bg-opacity-100 border-2 rounded-md py-6 lg:h-3/5"
      >
        <div class="lg:text-center border-b-2 border-gray-400 m-auto">
          <p
            class="mt-2 text-3xl leading-8 font-extrabold tracking-tight text-gray-900 sm:text-4xl"
          >
            About
          </p>
          <p class="mt-4 max-w-2xl text-xl text-gray-500 lg:mx-auto mb-6">
            I'm a Full-Stack Developer currently located in Toronto, CA. I have
            serious passion for UI effects, animations and creating intuitive,
            dynamic user experiences. Let's make something special.
          </p>
        </div>

        <div class="mt-10">
          <div class="lg:text-center mb-6">
            <h2
              class="text-base text-indigo-600 font-semibold tracking-wide uppercase"
            >
              Languages, Frameworks & Libraries
            </h2>
          </div>
          <div
            class="flex flex-wrap overflow-hidden xl:-mx-1 rounded-md justify-content-center align-items-center text-white md:grid sm:grid lg:grid-cols-10 sm:grid-cols-4 md:grid-cols-4 md:gap-x-8 md:gap-y-10"
          >
            <img
              class="flex h-16 w-auto m-4"
              src="../assets/html5.svg"
              alt="HTML5"
            />
            <img
              class="flex h-16 w-auto m-4"
              src="../assets/css3.svg"
              alt="CSS3"
            />
            <img
              class="flex h-16 w-auto m-4"
              src="../assets/js.png"
              alt="JAVASCRIPT"
            />
            <img
              class="flex h-16 w-auto m-4"
              src="../assets/python.svg"
              alt="PYTHON"
            />
            <img
              class="flex h-16 w-auto m-4"
              src="../assets/react.png"
              alt="REACT"
            />
            <img
              class="flex h-16 w-auto m-4"
              src="../assets/nodejs.svg"
              alt="NODEJS"
            />
            <img
              class="flex h-16 w-auto m-4"
              src="../assets/mongo.png"
              alt="MONGODB"
            />

            <img
              class="flex h-16 w-auto m-4"
              src="../assets/sass.svg"
              alt="SASS"
            />
            <img
              class="flex h-16 w-auto m-4"
              src="../assets/sqlite.svg"
              alt="SQLITE"
            />
            <img
              class="flex h-16 w-auto m-4"
              src="../assets/gatsby.png"
              alt="GATSBYJS"
            />
          </div>
        </div>
      </div>
    </div>
    <!--Projects -->
    <div
      class="md:flex py-12 flex justify-items-center align-items-center bg-white-700"
    >
      <div class="max-w-6xl mx-auto">
        <div class="text-center">
          <h1 class="text-6xl font-bold text-gray-800 underline">Portfolio</h1>
        </div>

        <div class="mt-16 grid grid-cols-1 md:grid-cols-1 lg:grid-cols-3 gap-6">
          <div
            class="bg-white rounded-md shadow-xl lg:col-span-1 portfolio-item"
          >
            <img
              src="../assets/chatapp.jpg"
              alt="chatapp"
              class="object-cover w-full h-80"
            />
            <div class="p-8">
              <h3 class="font-bold text-2xl">React Chat App</h3>
              <p class="pt-3">
                A real-time chat app built using React and Socket.io. TODO: use
                MongoDB for user list + room list; use Passport for user
                login/authentication; fix sign-in/out message layout.
              </p>
              <div class="h-50 w-100 border-t-2 border-b-2 border-black">
                <p>
                  Hello Div
                </p>
              </div>
              <a
                href="#"
                class="inline-block mt-4 px-6 py-2 bg-gradient-to-r from-cyan-400 to-emerald-400 rounded-md shadow-md text-sm font-bold text-black"
                >View More</a
              >
            </div>
          </div>
          <div class="bg-white rounded-md shadow-lg portfolio-item">
            <img
              src="../assets/mashup.jpg"
              alt=""
              class="object-cover w-full h-80"
            />
            <div class="p-8">
              <h3 class="font-bold text-2xl">Google Maps + News Mashup</h3>
              <p class="pt-3">
                Lorem ipsum dolor sit amet consectetur adipisicing elit.
              </p>
              <a
                href="#"
                class="inline-block mt-4 px-6 py-2 bg-gradient-to-r from-cyan-400 to-emerald-400 rounded-md shadow-md text-sm font-bold text-black"
                >View More</a
              >
            </div>
          </div>
          <div class="bg-white rounded-md shadow-lg portfolio-item">
            <img
              src="../assets/finance.jpg"
              alt=""
              class="object-cover w-full h-80"
            />
            <div class="p-8">
              <h3 class="font-bold text-2xl">Stock Trading Simulator</h3>
              <p class="pt-3">
                Lorem ipsum dolor sit amet consectetur adipisicing elit.
              </p>
              <a
                href="#"
                class="inline-block mt-4 px-6 py-2 bg-gradient-to-r from-cyan-400 to-emerald-400 rounded-md shadow-md text-sm font-bold text-black"
                >View More</a
              >
            </div>
          </div>
          <div
            class="bg-white rounded-md shadow-lg lg:col-span-2 portfolio-item"
          >
            <img
              src="images/work4.jpg"
              alt=""
              class="object-cover w-full h-80"
            />
            <div class="p-8">
              <h3 class="font-bold text-2xl">Work Title</h3>
              <p class="pt-3">
                Lorem ipsum dolor sit amet consectetur adipisicing elit.
                Repellat sequi minima vero sunt perferendis.
              </p>
              <a
                href="#"
                class="inline-block mt-4 px-6 py-2 bg-gradient-to-r from-cyan-400 to-emerald-400 rounded-md shadow-md text-sm font-bold text-white"
                >View More</a
              >
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  mounted() {
    const mobileButton = document.querySelector(".hamburger");
    const mobileMenu = document.getElementById("mobile-menu");

    function mobileToggle() {
      mobileMenu.classList.toggle("hidden");
    }

    mobileButton.addEventListener("click", mobileToggle);

    // grab everything we need
    const gridItems = document.querySelectorAll(".grid-background > div");

    // loop over grid items and create a random duration + delay for each
    gridItems.forEach(item => {
      // calculate random number for delay
      const delay = getRandomInt(0, 5);

      // calculate random number for duration
      const duration = getRandomInt(3, 6);

      // set both
      item.style.animationDelay = `${delay}s`;
      item.style.animationDuration = `${duration}s`;
    });

    function getRandomInt(min, max) {
      min = Math.ceil(min);
      max = Math.floor(max);
      return Math.floor(Math.random() * (max - min + 1)) + min;
    }
  }
};
</script>

<style>
* {
}

.landing {
  height: calc(100vh - 80px) !important;
}

@media only screen and (max-width: 415px) {
  .landing {
    height: auto !important;
  }
}

.portfolio-item:hover {
  transform: scale(1.01);
  transition: ease-in-out 0.5s;
}

@keyframes slideInFromLeft {
  0% {
    transform: translateX(-100%);
  }
  100% {
    transform: translateX(0);
  }
}

@keyframes slideInFromRight {
  0% {
    transform: translateX(100%);
  }
  100% {
    transform: translateX(0);
  }
}

.left {
  animation: 1s ease-out 0s 1 slideInFromLeft;
}

.right {
  animation: 1s ease-in 0s 1 slideInFromRight;
}
</style>
