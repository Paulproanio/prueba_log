<template>
<div>
    <v-container>
        <v-card-text class="mt-5"></v-card-text>

        <v-card elevation="15" width="600" class="mx-auto">

            <v-layout wrap>
                <v-card-text></v-card-text>
                <v-flex>
                    <v-img class="mx-auto" src="@/assets/logo.png" width="170"></v-img>
                </v-flex>
                <v-flex sm12 mx-auto>
                    <v-card-title class="ml-5">BIENVENIDO</v-card-title>
                    <v-card-text>
                        <v-flex>
                            <v-text-field class="font-weight-medium ml-5 mr-5" label="Usuario.." type="text" v-model="usuario" solo dense height="70"></v-text-field>
                        </v-flex>
                        <v-flex>
                            <v-text-field class="font-weight-medium ml-5 mr-5" label="Contraseña.." type="text" v-model="contrasenia" solo dense height="70"></v-text-field>
                        </v-flex>

                    </v-card-text>
                    <v-card-actions>
                        <v-btn @click="login(usuario,contrasenia)" class="font-weight-medium  success" block>Login</v-btn>
                    </v-card-actions>

                </v-flex>

            </v-layout>
        </v-card>
    </v-container>
</div>
</template>

<script>
export default {
    name: 'Home',
    data() {
        return {
            usuario: '',
            contrasenia: ''

        }
    },
    components: {

    },
    methods: {
        login(usuario, contrasenia) {
            if (usuario == '' || contrasenia == '') {
                alert("Los campos no pueden quedar vacios!!");

            } else {
                console.log(usuario);
                console.log(contrasenia);

            }

        }
    },
}
</script>
