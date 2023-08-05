<template>
<div class="container-fluid">
   <div class="row">
    <nav class="navbar navbar-expand-lg navbar-light bg-light">
        <div class="container-fluid">
            <NuxtLink to="/" :class="'navbar-brand'">
                NuxtJS Gtag / meta
            </NuxtLink>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav">
                    <li class="nav-item">
                        <NuxtLink to="/" :class="'nav-link'" :active-class="'active'">
                            Home
                        </NuxtLink>
                    </li>
                    <li class="nav-item">
                        <NuxtLink :class="'nav-link'" to="/about" :active-class="'active'">About</NuxtLink>
                    </li>
                </ul>
            </div>
        </div>
    </nav>
    <slot />
   </div>
</div>
</template>