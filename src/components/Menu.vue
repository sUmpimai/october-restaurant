<template>
    <div>
      <div class="text-center py-3">
        <h4 class="text-sm font-['Playfair'] italic text-[#777] pb-2">Genuine and delicious</h4>
        <h2 class="text-4xl font-extrabold uppercase pb-6">Our Menu</h2>
        <div class="tab">
            <div class="tab-nav">
                <div class="tab-nav-tab"
                    v-for="(item, index) in items"
                    :class="[index === active ? 'active' : '']"
                    @click="activate(index)"
                    >
                    Tab {{ index + 1 }} 
                </div>
                <div class="tabs-content">
                    {{ content }}
                </div>
            </div>
        </div>
      </div>
    </div>
</template>

<script>
import { ref } from 'vue'
const active = ref(1);

const items = ref([
  {
    content: '1'
  },
  {
    content: '2'
  },
  {
    content: '3'
  }
])

const activate = (index) => {
 return active = index
}
</script>