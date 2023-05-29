<template>
  <q-page class="constrain q-pa-md">

    <div class="row q-col-gutter-lg">
      <div class="col-12 col-sm-8"><q-card v-for="post in posts" :key="post.id" class="card-post q-mb-md" flat bordered>
          <q-item>
            <q-item-section avatar>
              <q-avatar>
                <img src="https://cdn.quasar.dev/img/boy-avatar.png">
              </q-avatar>
            </q-item-section>

            <q-item-section>
              <q-item-label class="text-bold">Lana__Banana</q-item-label>
              <q-item-label caption>
              {{ post.location }}
              </q-item-label>
            </q-item-section>
          </q-item>

          <q-separator />

          <q-img :src="post.imageUrl" />

          <q-card-section>
            <div >{{ post.caption }}</div>
            <div class="text-caption text-grey">{{ formatDate(post.date) }}</div>
          </q-card-section>

        </q-card>
      </div>
      <div class="col-4 large-screen-only">
        <q-item class="fixed">
          <q-item-section avatar>
            <q-avatar size="48px">
              <img src="https://cdn.quasar.dev/img/boy-avatar.png">
            </q-avatar>
          </q-item-section>

          <q-item-section>
            <q-item-label class="text-bold">Lana__Banana</q-item-label>
            <q-item-label caption>Lana Langlois</q-item-label>
          </q-item-section>
        </q-item>
      </div>
    </div>


  </q-page>
</template>

<script setup>
import { ref } from 'vue';
import { date } from 'quasar'

const posts = ref([
  {
    id: 1,
    caption: 'Rocheuses Canadienne',
    date: 1685323369903,
    imageUrl: 'https://cdn.quasar.dev/img/mountains.jpg',
    location: 'St-Donat, Québec'
  },
  {
    id: 2,
    caption: 'Rocheuses Canadienne',
    date: 1685323369903,
    imageUrl: 'https://cdn.quasar.dev/img/mountains.jpg',
    location: 'St-Donat, Québec'
  },
  {
    id: 3,
    caption: 'Rocheuses Canadienne',
    date: 1685323369903,
    imageUrl: 'https://cdn.quasar.dev/img/mountains.jpg',
    location: 'St-Donat, Québec'
  },
  {
    id: 4,
    caption: 'Rocheuses Canadienne',
    date: 1685323369903,
    imageUrl: 'https://cdn.quasar.dev/img/mountains.jpg',
    location: 'St-Donat, Québec'
  },
  {
    id: 5,
    caption: 'Rocheuses Canadienne',
    date: 1685323369903,
    imageUrl: 'https://cdn.quasar.dev/img/mountains.jpg',
    location: 'St-Donat, Québec'
  },
])

function formatDate(timeStamp){
  return date.formatDate(timeStamp, 'D MMM h:m a')
}

</script>

<style lang="scss">
 .q-card{
  .q-img{
    min-height: 200px;
  }
 }
</style>
