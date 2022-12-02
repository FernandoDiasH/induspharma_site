<template>
    <div>
        <nav>
            <ul>
                <li><NuxtLink to="/">Home</NuxtLink></li>
                <li><NuxtLink to="/about">about</NuxtLink></li>
                <li><NuxtLink to="/products">produtos</NuxtLink></li>
            </ul>
        </nav>
        <div>
            <slot />
        </div>
    </div>
</template>