<template>
  <div class="navbar bg-primary border-b-2 border-red-600">
    <div class="navbar-start">
      <div class="dropdown">
        <div tabindex="0" role="button" class="btn btn-ghost lg:hidden">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            class="h-5 w-5"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor">
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M4 6h16M4 12h8m-8 6h16" />
          </svg>
        </div>
        <ul tabindex="0" class="menu menu-sm dropdown-content glass rounded-box z-[1] mt-3 w-32 p-2 shadow"> <!-- Start of mobile dropdown -->

          <RouterLink to="/" class="btn bg-white text-black m-1">Home</RouterLink>
          <RouterLink to="/credits" class="btn bg-red-600 text-white m-1">Credits</RouterLink>
          <RouterLink to="/devlogs" class="btn bg-indigo-500 text-white m-1">Devlogs</RouterLink>
          <a href="https://discord.gg/ZrGP7hG65n" class="btn bg-blue-500 text-black m-1">Discord</a>
          <a href="https://github.com/VITA4EVER/" class="btn bg-gray-400 text-black m-1">Github</a>
          <RouterLink to="/rss" class="btn bg-orange-600 text-black m-1 ">RSS</RouterLink>
          <RouterLink to="/project-status" class="btn bg-cyan-400 text-cyan-950 m-1">Project Status</RouterLink>
          <RouterLink to="/code-of-conduct" class="btn bg-red-500 text-white m-1">COC</RouterLink>

        </ul> <!-- End of mobile dropdown -->
      </div>
      <RouterLink to="/" class="btn btn-ghost text-xl">VITA4EVER</RouterLink>
    </div>
    <div class="navbar-center hidden lg:flex">
      <ul class="menu menu-horizontal px-1 gap-2"> <!-- Start of the center navbar -->
        <li class="border-2 rounded-xl"><RouterLink to="/">Home</RouterLink></li>
        <li class="border-2 rounded-xl border-red-600"><RouterLink to="/credits">Credits</RouterLink></li>
        <li class="border-2 rounded-xl border-indigo-500"><RouterLink to="/devlogs">Devlogs</RouterLink></li>
        <li class="border-2 rounded-xl border-blue-500"><a href="https://discord.gg/ZrGP7hG65n">Discord</a></li>
        <li class="border-2 rounded-xl border-gray-400"><a href="https://github.com/VITA4EVER/">Github</a></li>
        <!--<li class="border-2 rounded-xl border-emerald-700"><RouterLink to="/status/kzv">KZV Status</RouterLink></li>-->
        <li class="border-2 rounded-xl border-orange-600"><RouterLink to="/rss">RSS</RouterLink></li>
        <li class="border-2 rounded-xl border-cyan-400"><RouterLink to="/project-status">Project Status</RouterLink></li>
        <li class="border-2 rounded-xl border-x-red-600 border-y-indigo-500"><RouterLink to="/code-of-conduct">Code Of Conduct</RouterLink></li>
      </ul> <!-- End of the center navbar -->
    </div>
    <div class="navbar-end">
      <!-- No need for anything here yet. -->
    </div>
  </div>
</template>

<script>
export default {
  name: 'HeaderComponent'
}
</script>
