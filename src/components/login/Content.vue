<script>
import { onErrorCaptured } from 'vue';

    export default{
        email: 'AddInformation',
        data(){
            return{
                email: '',
                senha: '',
                remember: false,
            }
        },
        methods:{
            onSubmit(e){

                e.preventDefault();

                if(!this.email.trim() || this.email.length < 5 || !this.email.includes('@')){
                    alert('Digite um email valido');
                    return;
                } 

                var myHeaders = new Headers();

                var myInit = { method: 'POST',
                            headers: myHeaders,
                            mode: 'cors',
                            cache: 'default',
                            body: new FormData(document.getElementById('formLogin'))
                         };

                fetch('http://127.0.0.1:8000/api/users/sexo', myInit)
                .then(function(response) {
                    return response.json();
                })
                .then(this.handleErrors)
                .then(function(data) {

                    alert('ok');
                
                }).catch(function(error) {
                    alert(error.message);
                });

            },
            handleErrors(response){
                if(response.error != undefined){
                    throw Error(response.error);
                }
                return response;
            }
        }
    }

</script>

<template>
    <div class="header-left-bottom">
        <form id="formLogin" @submit="onSubmit" method="post">
            <div class="icon1">
                <span class="fa fa-user"></span>
                <input name="email" v-model="email" type="email" placeholder="Email" required />
            </div>
            <div class="icon1">
                <span class="fa fa-lock"></span>
                <input name="senha" v-model="senha" type="password" placeholder="Senha" required />
            </div>
            <div class="login-check">
                <label class="checkbox"><input v-model="remember" type="checkbox" name="checkbox"><i> </i> Mantenha-me Logado</label>
            </div>
            <div class="bottom">
                <button class="btn">Log In</button>
            </div>
            <div class="links">
                <p><a href="#">Esqueceu a senha?</a></p>
                <p class="right"><a href="#">Cadastre-se</a></p>
                <div class="clear"></div>
            </div>
        </form>
    </div>

    <div class="social">
        <ul>
            <li>Ou faça login com : </li>
            <li><a href="#" class="facebook"><span class="fa fa-facebook"></span></a></li>
            <li><a href="#" class="twitter"><span class="fa fa-twitter"></span></a></li>
            <li><a href="#" class="google"><span class="fa fa-google-plus"></span></a></li>
        </ul>
    </div>
</template>