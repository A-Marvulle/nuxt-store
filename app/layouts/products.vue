<template>
  <div>
    <header>
      <nav>
        <ul>
          <li><NuxtLink to="/">Home</NuxtLink></li>
        </ul>
      </nav>
    </header>

    <!-- ? START PAGE CONTENT -->
    <div>
      <slot />
    </div>
    <!-- ? END PAGE CONTENT -->

    <header>
      <nav>
        <ul>
          <li><NuxtLink to="/about">About</NuxtLink></li>
          <li><NuxtLink to="/products">Products</NuxtLink></li>
        </ul>
      </nav>
    </header>
  </div>
</template>
