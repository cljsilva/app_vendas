<template>
  <q-page class="flex flex-center bg-grey">
    <q-card
      style="
        width: 410px;
        height: auto;
        display: flex;
        flex-direction: column;
        align-items: center;
      "
    >
      <q-card-section>
        <div class="text-h5">Recuperação de senha</div>
      </q-card-section>

      <q-card-section class="q-pt-none full-width">
        <q-input
          class="full-width"
          filled
          v-model="email"
          label="E-mail"
          color="dark"
        />
      </q-card-section>
      <q-card-actions class="full-width">
        <q-btn
          class="q-mx-sm"
          color="dark"
          label="RECUPERAR SENHA"
          @click="$router.push({ name: 'login' })"
          style="width: 100%"
        />
      </q-card-actions>
    </q-card>
  </q-page>
</template>

<script>
export default {
  data() {
    return {
      email: "",
    };
  },
};
</script>
