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
                  href="#about"
                  class="text-black-400 hover:bg-gray-700 hover:text-white px-3 py-2 rounded-md text-medium font-medium"
                  >About</a
                >

                <a
                  href="#projects"
                  class="text-black-400 hover:bg-gray-700 hover:text-white px-3 py-2 rounded-md text-medium font-medium"
                  >Projects</a
                >
                <a
                  href="#contact"
                  class="text-black-400 hover:bg-gray-700 hover:text-white px-3 py-2 rounded-md text-medium font-medium"
                  >Contact</a
                >
              </div>
            </div>
          </div>
          <div class="nav-logos">
            <a
              href="https://www.linkedin.com/in/alexander-duria-b4a20376/"
              class="w-full flex items-center justify-center px-2 py-2 border border-transparent rounded-md text-base font-medium text-black nav-logo"
            >
              <img class="w-12" src="../assets/linkedin.svg" alt="LinkedIn" />
            </a>
          </div>
          <div class="nav-logos">
            <a
              href="https://github.com/Duria73"
              class="w-full flex items-center justify-center px-2 py-2 border border-transparent rounded-md text-base font-medium text-black nav-logo"
            >
              <img class="w-12" src="../assets/github.svg" alt="GitHub" />
            </a>
          </div>
          <div class="nav-logos">
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
            href="#projects"
            class="text-gray-300 hover:bg-gray-700 hover:text-white block px-3 py-2 rounded-md text-base font-medium"
            >Projects</a
          >

          <a
            href="#"
            class="text-gray-300 hover:bg-gray-700 hover:text-white block px-3 py-2 rounded-md text-base font-medium"
            >Resume</a
          >
          <a
            href="https://github.com/Duria73"
            class="text-gray-300 hover:bg-gray-700 hover:text-white block px-3 py-2 rounded-md text-base font-medium"
            >GitHub</a
          >
          <a
            href="https://www.linkedin.com/in/alexander-duria-b4a20376/"
            class="text-gray-300 hover:bg-gray-700 hover:text-white block px-3 py-2 rounded-md text-base font-medium"
            >LinkedIn</a
          >

          <a
            href="#contact"
            class="text-gray-300 hover:bg-gray-700 hover:text-white block px-3 py-2 rounded-md text-base font-medium"
            >Contact</a
          >
        </div>
      </div>
    </nav>

    <!-- Grid Background -->
    <div class="bars relative flex items-center justify-center">
      <!-- grid background -->
      <div
        class="grid-background absolute inset-0 p-2 grid grid-cols-12 gap-2 transform -skew-y-12 scale-125 bg-gray-900 outer-landing"
      >
        <!-- row 1 -->
        <div
          class="col-span-2 bg-gray-800 rounded animate-pulse backdrop"
        ></div>
        <div class="col-span-5 bg-gray-800 rounded animate-pulse fade"></div>
        <div
          class="col-span-1 bg-gray-800 rounded animate-pulse backdrop"
        ></div>
        <div class="col-span-4 bg-gray-800 rounded animate-pulse fade"></div>

        <!-- row 2 -->
        <div class="col-span-5 bg-gray-800 rounded animate-pulse fade"></div>
        <div
          class="col-span-3 bg-gray-800 rounded animate-pulse backdrop"
        ></div>
        <div class="col-span-2 bg-gray-800 rounded animate-pulse fade"></div>
        <div
          class="col-span-2 bg-gray-800 rounded animate-pulse backdrop"
        ></div>

        <!-- row 3 -->
        <div class="col-span-4 bg-gray-800 rounded animate-pulse fade"></div>
        <div
          class="col-span-7 bg-gray-800 rounded animate-pulse backdrop"
        ></div>
        <div class="col-span-1 bg-gray-800 rounded animate-pulse fade"></div>

        <!-- row 4 -->
        <div
          class="col-span-2 bg-gray-800 rounded animate-pulse backdrop"
        ></div>
        <div class="col-span-4 bg-gray-800 rounded animate-pulse fade"></div>
        <div
          class="col-span-6 bg-gray-800 rounded animate-pulse backdrop"
        ></div>

        <!-- row 5 -->
        <div class="col-span-5 bg-gray-800 rounded animate-pulse fade"></div>
        <div
          class="col-span-5 bg-gray-800 rounded animate-pulse backdrop"
        ></div>
        <div class="col-span-2 bg-gray-800 rounded animate-pulse fade"></div>

        <!-- row 6 -->
        <div class="col-span-3 bg-gray-800 rounded animate-pulse"></div>
        <div
          class="col-span-5 bg-gray-800 rounded animate-pulse backdrop"
        ></div>
        <div class="col-span-4 bg-gray-800 rounded animate-pulse"></div>
      </div>

      <!--About Section -->
      <div
        class="py-12 relative flex justify-items-center align-items-center landing sm:h-auto"
        id="about"
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
              class="flex flex-wrap overflow-hidden xl:-mx-1 rounded-md justify-content-center align-items-center text-white md:grid sm:grid lg:grid-cols-10 sm:grid-cols-4 md:grid-cols-4 md:gap-x-8 md:gap-y-10 lg:mt-12"
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
      class="md:flex py-12 flex justify-items-center align-items-center bg-white-700 mt-28 scroll-container"
      id="projects"
    >
      <div class="max-w-6xl mx-auto">
        <div
          class="text-right mr-6 project-title  scroll-element js-scroll slide-left"
        >
          <h1 class="text-6xl font-bold text-gray-800 underline">
            Projects
          </h1>
        </div>

        <div
          class="mt-16 mx-4 grid grid-cols-1 md:grid-cols-1 lg:grid-cols-3 gap-6"
        >
          <!--Project 1 -->
          <div
            class="bg-white rounded-md shadow-xl lg:col-span-1 portfolio-item relative scroll-element js-scroll slide-left"
          >
            <img
              src="../assets/chatapp.jpg"
              alt="chatapp"
              class="object-cover w-full h-80"
            />
            <div>
              <h3 class="font-bold text-2xl px-8 py-4">React Chat App</h3>
              <p class="px-8 py-2 h-2/5">
                A real-time chat app built using React and Socket.io. TODO: use
                MongoDB for user list + room list; use Passport for user
                login/authentication; fix sign-in/out message layout.
              </p>
              <div class="h-50 w-100 lang-list">
                <ul class="flex flex-row justify-center py-0 px-6 mx-4">
                  <li>
                    <img
                      class="flex h-10 w-auto m-2 lang-icon up"
                      src="../assets/html5.svg"
                      alt="HTML5"
                    />
                  </li>
                  <li>
                    <img
                      class="flex h-10 w-auto m-2 lang-icon up"
                      src="../assets/html5.svg"
                      alt="HTML5"
                    />
                  </li>
                  <li>
                    <img
                      class="flex h-10 w-auto m-2 lang-icon up"
                      src="../assets/html5.svg"
                      alt="HTML5"
                    />
                  </li>
                </ul>
              </div>
              <div class="flex flex-row justify-between">
                <a
                  href="#"
                  class="inline-block m-4 px-6 py-2 bg-gradient-to-r from-cyan-400 to-emerald-400 rounded-md shadow-md text-sm font-bold text-black link-button"
                  >View Repo</a
                >
                <a
                  href="#"
                  class="inline-block m-4 px-6 py-2 bg-gradient-to-r from-cyan-400 to-emerald-400 rounded-md shadow-md text-sm font-bold text-black link-button"
                  >Live Site</a
                >
              </div>
            </div>
          </div>
          <!--Project 2 -->
          <div
            class="bg-white rounded-md shadow-xl lg:col-span-1 portfolio-item relative scroll-element js-scroll fade-in-bottom"
          >
            <img
              src="../assets/mashup.jpg"
              alt=""
              class="object-cover w-full h-80"
            />
            <div>
              <h3 class="font-bold text-2xl px-8 py-4">React Chat App</h3>
              <p class="px-8 py-2 h-2/5">
                A real-time chat app built using React and Socket.io. TODO: use
                MongoDB for user list + room list; use Passport for user
                login/authentication; fix sign-in/out message layout.
              </p>
              <div class="h-50 w-100 lang-list">
                <ul class="flex flex-row justify-center py-0 px-6 mx-4">
                  <li>
                    <img
                      class="flex h-10 w-auto m-2 lang-icon up"
                      src="../assets/html5.svg"
                      alt="HTML5"
                    />
                  </li>
                  <li>
                    <img
                      class="flex h-10 w-auto m-2 lang-icon up"
                      src="../assets/html5.svg"
                      alt="HTML5"
                    />
                  </li>
                  <li>
                    <img
                      class="flex h-10 w-auto m-2 lang-icon up"
                      src="../assets/html5.svg"
                      alt="HTML5"
                    />
                  </li>
                </ul>
              </div>
              <div class="flex flex-row justify-between">
                <a
                  href="#"
                  class="inline-block m-4 px-6 py-2 bg-gradient-to-r from-cyan-400 to-emerald-400 rounded-md shadow-md text-sm font-bold text-black link-button"
                  >View Repo</a
                >
                <a
                  href="#"
                  class="inline-block m-4 px-6 py-2 bg-gradient-to-r from-cyan-400 to-emerald-400 rounded-md shadow-md text-sm font-bold text-black link-button"
                  >Live Site</a
                >
              </div>
            </div>
          </div>
          <!--Project 3 -->
          <div
            class="bg-white rounded-md shadow-xl lg:col-span-1 portfolio-item relative scroll-element js-scroll slide-right"
          >
            <img
              src="../assets/mashup.jpg"
              alt=""
              class="object-cover w-full h-80"
            />
            <div>
              <h3 class="font-bold text-2xl px-8 py-4">React Chat App</h3>
              <p class="px-8 py-2 h-2/5">
                A real-time chat app built using React and Socket.io. TODO: use
                MongoDB for user list + room list; use Passport for user
                login/authentication; fix sign-in/out message layout.
              </p>
              <div class="h-50 w-100 lang-list">
                <ul class="flex flex-row justify-center py-0 px-6 mx-4">
                  <li>
                    <img
                      class="flex h-10 w-auto m-2 lang-icon up"
                      src="../assets/html5.svg"
                      alt="HTML5"
                    />
                  </li>
                  <li>
                    <img
                      class="flex h-10 w-auto m-2 lang-icon up"
                      src="../assets/html5.svg"
                      alt="HTML5"
                    />
                  </li>
                  <li>
                    <img
                      class="flex h-10 w-auto m-2 lang-icon up"
                      src="../assets/html5.svg"
                      alt="HTML5"
                    />
                  </li>
                </ul>
              </div>
              <div class="flex flex-row justify-between">
                <a
                  href="#"
                  class="inline-block m-4 px-6 py-2 bg-gradient-to-r from-cyan-400 to-emerald-400 rounded-md shadow-md text-sm font-bold text-black link-button"
                  >View Repo</a
                >
                <a
                  href="#"
                  class="inline-block m-4 px-6 py-2 bg-gradient-to-r from-cyan-400 to-emerald-400 rounded-md shadow-md text-sm font-bold text-black link-button"
                  >Live Site</a
                >
              </div>
            </div>
          </div>

          <!--Project 4 -->
          <div
            class="bg-white rounded-md shadow-lg lg:col-span-2 portfolio-item scroll-element js-scroll slide-left"
          >
            <img
              src="images/work4.jpg"
              alt=""
              class="object-cover w-full h-80"
            />
            <div>
              <h3 class="font-bold text-2xl px-8 py-4">ThreeJS Portfolio</h3>
              <p class="pt-3 px-8 py-2">
                Lorem ipsum dolor sit amet consectetur adipisicing elit.
                Repellat sequi minima vero sunt perferendis.
              </p>
              <div class="h-50 w-100 lang-list">
                <ul class="flex flex-row py-0 px-6 mx-4 justify-center">
                  <li>
                    <img
                      class="flex h-10 w-auto m-2 lang-icon up"
                      src="../assets/html5.svg"
                      alt="HTML5"
                    />
                  </li>
                  <li>
                    <img
                      class="flex h-10 w-auto m-2 lang-icon up"
                      src="../assets/html5.svg"
                      alt="HTML5"
                    />
                  </li>
                  <li>
                    <img
                      class="flex h-10 w-auto m-2 lang-icon up"
                      src="../assets/html5.svg"
                      alt="HTML5"
                    />
                  </li>
                </ul>
              </div>
              <div class="flex flex-row justify-between">
                <a
                  href="#"
                  class="inline-block m-4 px-6 py-2 bg-gradient-to-r from-cyan-400 to-emerald-400 rounded-md shadow-md text-sm font-bold text-black link-button"
                  >View Repo</a
                >
                <a
                  href="#"
                  class="inline-block m-4 px-6 py-2 bg-gradient-to-r from-cyan-400 to-emerald-400 rounded-md shadow-md text-sm font-bold text-black link-button"
                  >Live Site</a
                >
              </div>
            </div>
          </div>
          <!--Project 5 -->
          <div
            class="bg-white rounded-md shadow-lg portfolio-item scroll-element js-scroll fade-in-bottom"
          >
            <img
              src="../assets/finance.jpg"
              alt=""
              class="object-cover w-full h-80"
            />
            <div>
              <h3 class="font-bold text-2xl px-8 py-4">
                Stock Trading Simulator
              </h3>
              <p class="pt-3 px-8 py-2">
                Lorem ipsum dolor sit amet consectetur adipisicing elit.
              </p>
              <div class="h-50 w-100 lang-list">
                <ul class="flex flex-row justify-center py-0 px-6 mx-4">
                  <li>
                    <img
                      class="flex h-10 w-auto m-2 lang-icon up"
                      src="../assets/html5.svg"
                      alt="HTML5"
                    />
                  </li>
                  <li>
                    <img
                      class="flex h-10 w-auto m-2 lang-icon up"
                      src="../assets/html5.svg"
                      alt="HTML5"
                    />
                  </li>
                  <li>
                    <img
                      class="flex h-10 w-auto m-2 lang-icon up"
                      src="../assets/html5.svg"
                      alt="HTML5"
                    />
                  </li>
                </ul>
              </div>
              <div class="flex flex-row justify-between">
                <a
                  href="#"
                  class="inline-block m-4 px-6 py-2 bg-gradient-to-r from-cyan-400 to-emerald-400 rounded-md shadow-md text-sm font-bold text-black link-button"
                  >View Repo</a
                >
                <a
                  href="#"
                  class="inline-block m-4 px-6 py-2 bg-gradient-to-r from-cyan-400 to-emerald-400 rounded-md shadow-md text-sm font-bold text-black link-button"
                  >Live Site</a
                >
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!--Contact Section -->
    <section
      id="contact"
      class="text-white-700 body-font flex contact croll-element js-scroll fade-in-bottom"
    >
      <div class="m-auto">
        <div class="max-w-6xl mx-auto text-center mt-10 mb-10">
          <h1 class="text-6xl font-bold text-gray-800 underline">Contact Me</h1>
          <p class="lg:w-2/3 mx-auto leading-relaxed text-base mt-4">
            Alex.duria@outlook.com
          </p>
        </div>
        <div class="lg:w-full md:w-2/3 mx-auto">
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
      </div>
    </section>

    <!--Footer-->
    <footer class="footer text-gray-100 bg-gray-800 h-50">
      <div class="max-w-3xl mx-auto mt-24 py-6 sm:mt-12">
        <div class="flex justify-center mt-6">
          <div class="bg-gray rounded-md">
            <div class="flex flex-wrap justify-between md:flex-row">
              <a
                href="https://www.linkedin.com/in/alexander-duria-b4a20376/"
                class="m-6"
              >
                <img class="w-12" src="../assets/linkedin.svg" alt="LinkedIn" />
              </a>
              <a href="https://github.com/Duria73" class="m-6">
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
                href="#about"
                class="px-4 text-sm text-gray-100 font-medium hover:text-gray-400"
                >About</a
              >
              <a
                href="#projects"
                class="px-4 text-sm text-gray-100 font-medium hover:text-gray-400"
                >Projects</a
              >
              <a
                href="#contact"
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
import { ScrollTrigger } from "gsap/ScrollTrigger";

export default {
  mounted() {
    gsap.fromTo(".outer-landing", { opacity: 0 }, { opacity: 1, duration: 1 });
    gsap.fromTo(".backdrop", { x: -800 }, { x: 0, duration: 2 });
    gsap.fromTo(".fade", { x: 800 }, { x: 0, duration: 2 });
    gsap.from(".nav", { duration: 1, y: -80, delay: 1 });

    //Animations headers landing-page
    gsap.from(".innerLanding", { duration: 2, y: 1000 });
    gsap.from(".heading", { duration: 1.5, x: -400 });
    gsap.fromTo(".heading", { opacity: 0 }, { opacity: 1, duration: 2 });
    gsap.from(".description", { duration: 1.5, x: -500 });
    gsap.fromTo(".description", { opacity: 0 }, { opacity: 1, duration: 2 });

    gsap.from(".languages", { duration: 1.5, x: -400, delay: 1 });
    gsap.fromTo(
      ".languages",
      { opacity: 0 },
      { opacity: 1, duration: 2, delay: 1 }
    );
    //Icon SVGs
    gsap.from(".up", { duration: 1.5, y: -200, delay: 1.5 });
    gsap.fromTo(".up", { opacity: 0 }, { opacity: 1, duration: 3, delay: 2 });
    gsap.from(".down", { duration: 1.5, y: 200, delay: 1.5 });
    gsap.fromTo(".down", { opacity: 0 }, { opacity: 1, duration: 3, delay: 2 });

    //scroll trigger
    const scrollElements = document.querySelectorAll(".js-scroll");

    const elementInView = (el, dividend = 1) => {
      const elementTop = el.getBoundingClientRect().top;

      return (
        elementTop <=
        (window.innerHeight || document.documentElement.clientHeight) / dividend
      );
    };

    const elementOutofView = el => {
      const elementTop = el.getBoundingClientRect().top;

      return (
        elementTop >
        (window.innerHeight || document.documentElement.clientHeight)
      );
    };

    const displayScrollElement = element => {
      element.classList.add("scrolled");
    };

    //optional remove scrolled to replay animations

    // const hideScrollElement = element => {
    //   element.classList.remove("scrolled");
    // };

    const handleScrollAnimation = () => {
      scrollElements.forEach(el => {
        if (elementInView(el, 1.25)) {
          displayScrollElement(el);
        } else if (elementOutofView(el)) {
          hideScrollElement(el);
        }
      });
    };

    window.addEventListener("scroll", () => {
      handleScrollAnimation();
    });

    const mobileButton = document.querySelector(".hamburger");
    const mobileMenu = document.getElementById("mobile-menu");

    function mobileToggle() {
      mobileMenu.classList.toggle("hidden");
    }

    mobileButton.addEventListener("click", mobileToggle);

    //Navbar scroll w/ drop shadow
    let navBar = document.querySelector(".navBar");
    window.onscroll = function() {
      if(window.scrollY > 8) {
        navBar.classList.add("nav-scrolled"); 
      } else {
        navBar.classList.remove("nav-scrolled")
      }
    }

    // select grid divs
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
  scroll-behavior: smooth;
  scroll-snap-type: y mandatory;
}

.navBar {
  z-index: 10;
  transition: all 10ms ease-in;
}

.nav-scrolled {
  @apply shadow-2xl;
  border-bottom: 1px;
  position: fixed;
  width: 100%;
  background-color: #fff;
}


.nav-logo:hover {
  transform: scale(1.1);
  transition: ease-in 0.1s;
}

@media screen and (max-width: 800px) {
  .nav-logos {
    display: none;
  }
}

.landing {
  height: calc(100vh - 80px) !important;
}

.bars {
}

@media screen and (min-width: 900px) {
  .bars {
    clip-path: polygon(22.5% 0, 100% 0, 100% 90%, 0 136%, 0 91%, 0% 60%, 0 10%);
  }
}
@media screen and (max-width: 899px) {
  .bars {
    overflow-y: hidden;
    overflow-x: hidden;
  }
}

.lang-icon:hover {
  transform: scale(1.1);
  transition: ease-in 0.1s;
  border: 1px solid black;
  border-radius: 5px;

  padding: 5px;
}

.bottom-items {
  position: absolute;
  bottom: 0;
}

.react {
  -webkit-animation: spin 12s linear infinite;
  -moz-animation: spin 12s linear infinite;
  animation: spin 12s linear infinite;
}

@media only screen and (max-width: 730px) {
  .innerLanding {
    margin: 0px 12px;
  }
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

@media only screen and (max-width: 900px) {
  .project-title {
    text-align: center !important;
  }
}

@media only screen and (max-width: 900px) {
  .contact {
    margin: 0px 20px;
  }
}

.portfolio-item:hover {
  transform: scale(1.01);
  transition: ease-in-out 0.3s;
}

.lang-list {
  border-top: 1px solid rgba(0, 0, 0, 0.1);
  border-bottom: 1px solid rgba(0, 0, 0, 0.1);
}

ul,
li {
  list-style-type: none;
}

.gs_reveal {
  opacity: 0;
  visibility: hidden;
  will-change: transform, opacity;
}

.link-button:hover {
  cursor: pointer;
  background-color: black;
  transition: 0.3s ease-in-out;
  color: white;
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

/**Styling scrollable elements*/

.js-scroll {
  opacity: 0;
  transition: opacity 500ms;
}

.js-scroll.scrolled {
  opacity: 1;
}

.scrolled.fade-in {
  animation: fade-in 1s ease-in-out both;
}

.scrolled.fade-in-bottom {
  animation: fade-in-bottom 1s ease-in-out both;
}

.scrolled.slide-left {
  animation: slide-in-left 1s ease-in-out both;
}

.scrolled.slide-right {
  animation: slide-in-right 1s ease-in-out both;
}

/*Scroll Slides */

@keyframes slide-in-left {
  0% {
    -webkit-transform: translateX(-300px);
    transform: translateX(-300px);
    opacity: 0;
  }
  100% {
    -webkit-transform: translateX(0);
    transform: translateX(0);
    opacity: 1;
  }
}

@keyframes slide-in-right {
  0% {
    -webkit-transform: translateX(300px);
    transform: translateX(300px);
    opacity: 0;
  }
  100% {
    -webkit-transform: translateX(0);
    transform: translateX(0);
    opacity: 1;
  }
}

@keyframes fade-in-bottom {
  0% {
    -webkit-transform: translateY(50px);
    transform: translateY(50px);
    opacity: 0;
  }
  100% {
    -webkit-transform: translateY(0);
    transform: translateY(0);
    opacity: 1;
  }
}

@keyframes fade-in {
  0% {
    opacity: 0;
  }
  100% {
    opacity: 1;
  }
}
</style>
