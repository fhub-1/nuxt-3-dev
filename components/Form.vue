<template>
    <form class="text-gray-600 body-font">
        <div class="container px-5 py-24">
            <div class="lg:w-3/5 md:w-1/2">
                <h1 class="text-gray-900">
                    Subscribe to my newsletter
                </h1>
                <p class="leading-relaxed mt-4">
                    I send out a weekly newsletter with tips and tricks for web
                    development.
                </p>
            </div>
            <div class=" lg:w-2/6 md:w-1/2 bg-gray-100">
                <h2 class="text-gray-900 text-lg font-medium title-font mb-5">
                    Subscribe
                </h2>

                <div class="relative mb-4">
                    <label for="email" class="leading-7 text-sm text-gray-600">Email</label>
                    <input type="email" id="email" name="email" class="w-full bg-white rounded" />
                </div>
                <button class="text-white bg-indigo-500">
                    Subscribe
                </button>
            </div>
        </div>
    </form>
</template>