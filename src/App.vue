<template>
  <div id="app" class="min-h-screen bg-gray-200 antialiased xl:flex xl:flex-col xl:h-screen">
    <SiteHeader class="xl:flex-shrink-0" />
    <div class="xl:flex-1 xl:flex xl:overflow-y-hidden">
      <SearchFilters />
      <main class="py-6 xl:flex-1 xl:overflow-x-hidden">
        <div class="px-4">
          <h3 class="text-gray-900 text-xl">Los Angeles</h3>
          <p
            class="text-gray-600"
          >Live like the stars in these luxurious Southern California estates.</p>
        </div>
        <div class="mt-6 sm:overflow-x-auto">
          <div class="px-4 sm:inline-flex sm:pb-8">
            <div
              v-for="(property, i) in properties"
              :key="i"
              :class="{'mt-10 sm:ml-4': i > 0}"
              class="sm:mt-0 sm:w-80 sm:flex-shrink-0"
            >
              <PropertyCard :property="property" />
            </div>
          </div>
        </div>
      </main>
    </div>
  </div>
</template>

<script>
import SiteHeader from "./components/SiteHeader";
import SearchFilters from "./components/SearchFilters";
import PropertyCard from "./components/PropertyCard";

export default {
  name: "App",
  components: { SiteHeader, SearchFilters, PropertyCard },
  data() {
    return {
      properties: [
        {
          imageUrl:
            "https://images.unsplash.com/photo-1512917774080-9991f1c4c750?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=500&q=60",
          beds: 3,
          baths: 2,
          title: "Modern home in city center",
          price: 140000,
          reviewCount: 34,
          rating: 4,
        },
        {
          imageUrl:
            "https://images.unsplash.com/photo-1512917774080-9991f1c4c750?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=500&q=60",
          beds: 4,
          baths: 2,
          title: "Modern home in city center",
          price: 160000,
          reviewCount: 45,
          rating: 4,
        },
        {
          imageUrl:
            "https://images.unsplash.com/photo-1512917774080-9991f1c4c750?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=500&q=60",
          beds: 5,
          baths: 3,
          title: "Modern home in city center",
          price: 320000,
          reviewCount: 1,
          rating: 4,
        },
        {
          imageUrl:
            "https://images.unsplash.com/photo-1512917774080-9991f1c4c750?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=500&q=60",
          beds: 2,
          baths: 1,
          title: "Modern home in city center",
          price: 210000,
          reviewCount: 21,
          rating: 4,
        },
      ],
    };
  },
};
</script>

<style src='./assets/css/tailwind.css'>
</style>
