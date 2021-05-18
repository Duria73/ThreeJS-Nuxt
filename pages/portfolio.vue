<template>
  <!-- content -->
  <div class="overflow-hidden">
    <nav class="bg-white-800 navBar">
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
                  >Contact</a
                >
              </div>
            </div>
          </div>
          <div>
            <a
              href="#"
              class="w-full flex items-center justify-center px-2 py-2 border border-transparent rounded-md text-base font-medium text-black nav-logo"
            >
              <img class="w-12" src="../assets/linkedin.svg" alt="LinkedIn" />
            </a>
          </div>
          <div>
            <a
              href="#"
              class="w-full flex items-center justify-center px-2 py-2 border border-transparent rounded-md text-base font-medium text-black nav-logo"
            >
              <img class="w-12" src="../assets/github.svg" alt="GitHub" />
            </a>
          </div>
          <div>
            <a
              href="#"
              class="w-full flex items-center justify-center px-2 py-2 border border-transparent rounded-md text-base font-medium text-black nav-logo"
            >
              <img class="w-12" src="../assets/resume.png" alt="Resume" />
            </a>
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
            >Resume</a
          >

          <a
            href="#"
            class="text-gray-300 hover:bg-gray-700 hover:text-white block px-3 py-2 rounded-md text-base font-medium"
            >Contact</a
          >
        </div>
      </div>
    </nav>

    <div
      class="bars relative flex items-center justify-center bg-gray-900 overflow-y-hidden overflow-x-hidden"
    >
      <!-- grid background -->
      <div
        class="grid-background absolute inset-0 p-2 grid grid-cols-12 gap-2 transform -skew-y-12 scale-125 "
      >
        <!-- row 1 -->
        <div class="col-span-2 bg-gray-800 rounded animate-pulse"></div>
        <div class="col-span-5 bg-gray-800 rounded animate-pulse"></div>
        <div class="col-span-1 bg-gray-800 rounded animate-pulse"></div>
        <div class="col-span-4 bg-gray-800 rounded animate-pulse"></div>

        <!-- row 2 -->
        <div class="col-span-5 bg-gray-800 rounded animate-pulse"></div>
        <div class="col-span-3 bg-gray-800 rounded animate-pulse"></div>
        <div class="col-span-2 bg-gray-800 rounded animate-pulse"></div>
        <div class="col-span-2 bg-gray-800 rounded animate-pulse"></div>

        <!-- row 3 -->
        <div class="col-span-4 bg-gray-800 rounded animate-pulse"></div>
        <div class="col-span-7 bg-gray-800 rounded animate-pulse"></div>
        <div class="col-span-1 bg-gray-800 rounded animate-pulse"></div>

        <!-- row 4 -->
        <div class="col-span-2 bg-gray-800 rounded animate-pulse"></div>
        <div class="col-span-4 bg-gray-800 rounded animate-pulse"></div>
        <div class="col-span-6 bg-gray-800 rounded animate-pulse"></div>

        <!-- row 5 -->
        <div class="col-span-5 bg-gray-800 rounded animate-pulse"></div>
        <div class="col-span-5 bg-gray-800 rounded animate-pulse"></div>
        <div class="col-span-2 bg-gray-800 rounded animate-pulse"></div>

        <!-- row 6 -->
        <div class="col-span-3 bg-gray-800 rounded animate-pulse"></div>
        <div class="col-span-5 bg-gray-800 rounded animate-pulse"></div>
        <div class="col-span-4 bg-gray-800 rounded animate-pulse"></div>
      </div>

      <!--About Section -->
      <div
        class="py-12 relative flex justify-items-center align-items-center landing sm:h-auto"
      >
        <div
          class="innerLanding lg:my-32 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 bg-white bg-opacity-100 border-2 rounded-md py-6 lg:h-3/5 mx-4 intro-bg"
        >
          <div class="lg:text-center border-b-2 border-gray-400 m-auto">
            <p
              class="mt-2 text-3xl leading-8 font-extrabold tracking-tight text-gray-900 sm:text-4xl heading"
            >
              About
            </p>

            <p
              class="mt-4 max-w-2xl text-xl text-gray-500 lg:mx-auto mb-6 description"
            >
              I'm a Full-Stack Developer currently located in Toronto, CA. I
              have serious passion for UI effects, animations and creating
              intuitive, dynamic user experiences. Let's make something special.
            </p>
          </div>

          <div class="mt-10">
            <div class="lg:text-center mb-6">
              <h2
                class="text-base text-indigo-600 font-semibold tracking-wide uppercase languages"
              >
                Languages, Frameworks & Libraries
              </h2>
            </div>
            <div
              class="flex flex-wrap overflow-hidden xl:-mx-1 rounded-md justify-content-center align-items-center text-white md:grid sm:grid lg:grid-cols-10 sm:grid-cols-4 md:grid-cols-4 md:gap-x-8 md:gap-y-10"
            >
              <img
                class="flex h-16 w-auto m-4 lang-icon up"
                src="../assets/html5.svg"
                alt="HTML5"
              />
              <img
                class="flex h-16 w-auto m-4 lang-icon down"
                src="../assets/css3.svg"
                alt="CSS3"
              />
              <img
                class="flex h-16 w-auto m-4 lang-icon up"
                src="../assets/js.png"
                alt="JAVASCRIPT"
              />
              <img
                class="flex h-16 w-auto m-4 lang-icon down"
                src="../assets/python.svg"
                alt="PYTHON"
              />
              <img
                class="flex h-16 w-auto m-4 lang-icon react up"
                src="../assets/react.png"
                alt="REACT"
              />
              <img
                class="flex h-16 w-auto m-4 lang-icon down"
                src="../assets/nodejs.svg"
                alt="NODEJS"
              />
              <img
                class="flex h-16 w-auto m-4 lang-icon up"
                src="../assets/mongo.png"
                alt="MONGODB"
              />

              <img
                class="flex h-16 w-auto m-4 lang-icon down"
                src="../assets/sass.svg"
                alt="SASS"
              />
              <img
                class="flex h-16 w-auto m-4 lang-icon up"
                src="../assets/sqlite.svg"
                alt="SQLITE"
              />
              <img
                class="flex h-16 w-auto m-4 lang-icon down"
                src="../assets/gatsby.png"
                alt="GATSBYJS"
              />
            </div>
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

        <div
          class="mt-16 mx-4 grid grid-cols-1 md:grid-cols-1 lg:grid-cols-3 gap-6"
        >
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
              <h3 class="font-bold text-2xl">ThreeJS Portfolio</h3>
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
        </div>
      </div>
    </div>
    <!--Contact Section -->
    <section class="text-white-700 body-font relative contact">
      <div class="max-w-6xl mx-auto text-center mt-20 mb-10">
        <h1 class="text-6xl font-bold text-gray-800 underline">Contact Me</h1>
        <p class="lg:w-2/3 mx-auto leading-relaxed text-base mt-4">
          Alex.duria@outlook.com
        </p>
      </div>
      <div class="lg:w-1/2 md:w-2/3 mx-auto">
        <div class="flex flex-wrap -m-2">
          <div class="p-2 w-1/2">
            <input
              class="w-full bg-gray-100 rounded border border-gray-400 focus:outline-none focus:border-indigo-500 text-base px-4 py-2"
              placeholder="Name"
              type="name"
            />
          </div>
          <div class="p-2 w-1/2">
            <input
              class="w-full bg-gray-100 rounded border border-gray-400 focus:outline-none focus:border-indigo-500 text-base px-4 py-2"
              placeholder="Email"
              type="email"
            />
          </div>
          <div class="p-2 w-full">
            <input
              class="w-full bg-gray-100 rounded border border-gray-400 focus:outline-none h-48 focus:border-indigo-500 text-base px-4 py-2"
              placeholder="Enter Message"
              type="text"
            />
          </div>
          <div class="p2 w-full mt-4">
            <button
              class="flex mx-auto text-white bg-indigo-500 border-0 py-2 px-8 focus:outline-none hover:bg-indigo-600 rounded text-lg"
            >
              Submit
            </button>
          </div>
        </div>
      </div>
    </section>

    <!--Footer-->
    <footer class="footer text-gray-100 bg-gray-800 h-50">
      <div class="max-w-3xl mx-auto mt-24 py-6 sm:mt-12">
        <div class="flex justify-center mt-6">
          <div class="bg-gray rounded-md">
            <div class="flex flex-wrap justify-between md:flex-row">
              <a href="" class="m-6">
                <img class="w-12" src="../assets/linkedin.svg" alt="LinkedIn" />
              </a>
              <a href="" class="m-6">
                <img class="w-12" src="../assets/github.svg" alt="GitHub" />
              </a>
              <a href="" class="m-6">
                <img class="w-12" src="../assets/resume.png" alt="Resume" />
              </a>
            </div>
          </div>
        </div>

        <hr class="h-px mt-6 bg-gray-700 border-none mt-4" />

        <div
          class="flex flex-col items-center justify-between mt-4 md:flex-row"
        >
          <div>
            <a
              href="#"
              class="text-xl font-bold text-gray-100 hover:text-gray-400"
              >Alexander Duria 2021</a
            >
          </div>

          <div class="flex mt-4 md:m-0">
            <div class="-mx-4">
              <a
                href="#"
                class="px-4 text-sm text-gray-100 font-medium hover:text-gray-400"
                >About</a
              >
              <a
                href="#"
                class="px-4 text-sm text-gray-100 font-medium hover:text-gray-400"
                >Portfolio</a
              >
              <a
                href="#"
                class="px-4 text-sm text-gray-100 font-medium hover:text-gray-400"
                >Contact</a
              >
            </div>
          </div>
        </div>
      </div>
    </footer>
  </div>
</template>

<script>
import gsap from "gsap";
export default {
  mounted() {
    gsap.from("nav", { duration: 1, y: -80, delay: 1 });
    //Animations headers landing-page
    gsap.from(".innerLanding", { duration: 2, y: 1000 });
    gsap.from(".heading", { duration: 1.5, x: -400 });
    gsap.fromTo(".heading", { opacity: 0 }, { opacity: 1, duration: 2 });
    gsap.from(".description", { duration: 1.5, x: -500 });
    gsap.fromTo(".description", { opacity: 0 }, { opacity: 1, duration: 2 });

    gsap.from(".languages", { duration: 1, x: -400, delay: 1 });
    gsap.fromTo(
      ".languages",
      { opacity: 0 },
      { opacity: 1, duration: 2, delay: 1 }
    );
    //Icon SVGs
    gsap.from(".up", { duration: 1, y: -200, delay: 1 });
    gsap.fromTo(".up", { opacity: 0 }, { opacity: 1, duration: 3, delay: 1 });
    gsap.from(".down", { duration: 1, y: 200, delay: 1 });
    gsap.fromTo(".down", { opacity: 0 }, { opacity: 1, duration: 3, delay: 1 });

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
      const duration = getRandomInt(3, 5);

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

nav {
  z-index: 10;
}

nav.scrolled {
  @apply shadow-2xl;
  border-bottom: 0px;
}

.nav-logo:hover {
  transform: scale(1.01);
  transition: ease-in 0.1s;
}

.landing {
  height: calc(100vh - 80px) !important;
}

.lang-icon:hover {
  transform: scale(1.1);
  transition: ease-in 0.1s;
  border: 1px solid black;
  border-radius: 5px;

  padding: 5px;
}

.react {
  -webkit-animation: spin 12s linear infinite;
  -moz-animation: spin 12s linear infinite;
  animation: spin 12s linear infinite;
}

@-moz-keyframes spin {
  100% {
    -moz-transform: rotate(360deg);
  }
}
@-webkit-keyframes spin {
  100% {
    -webkit-transform: rotate(360deg);
  }
}
@keyframes spin {
  100% {
    -webkit-transform: rotate(360deg);
    transform: rotate(360deg);
  }
}

@media only screen and (max-width: 415px) {
  .landing {
    height: auto !important;
  }
}

.portfolio-item:hover {
  transform: scale(1.01);
  transition: ease-in-out 0.3s;
}

.footer {
  background: #1b242f;
}

.contact {
  height: calc(100vh - 293px) !important;
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
