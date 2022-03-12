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
        <q-img src="../assets/logo2.png" width="400px" />
      </q-card-section>

      <q-card-section>
        <div class="text-h5">Login</div>
      </q-card-section>

      <q-card-section class="q-pt-none full-width">
        <q-input
          class="full-width"
          filled
          v-model="login.email"
          label="E-mail"
          color="dark"
        />
        <q-input
          class="q-mt-sm"
          v-model="login.password"
          filled
          label="Password"
          :type="login.isPwd ? 'password' : 'text'"
          color="dark"
        >
          <template v-slot:append>
            <q-icon
              :name="login.isPwd ? 'visibility_off' : 'visibility'"
              class="cursor-pointer"
              @click="login.isPwd = !login.isPwd"
            />
          </template>
        </q-input>
      </q-card-section>
      <q-card-actions class="full-width">
        <q-btn
          class="q-mx-sm"
          color="dark"
          label="ENTRAR"
          @click="$router.push({ name: 'home' })"
          style="width: 100%"
        />
        <q-btn
          class="q-mx-sm"
          color="dark"
          label="ESQUECI SENHA"
          @click="$router.push({ name: 'esqueciSenha' })"
          style="width: 100%"
        />
      </q-card-actions>
    </q-card>
  </q-page>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  data() {
    return {
      login: {
        email: "",
        password: "",
        isPwd: true,
      },
    };
  },
});
</script>
