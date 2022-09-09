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
                
                Sexo(){    
                    var myHeaders = new Headers();

                    myHeaders.append("Content-Type", "application/json");
                    myHeaders.append("Accept", "application/json");
    
                    var myInit = {
                        method: 'GET',
                        headers: myHeaders,
                        mode: 'cors',
                        cache: 'default',
                    };
    
                    fetch('http://127.0.0.1:8000/api/user/sexo/MiaKhalifa', myInit)
                    .then(function(response) {
                        return response.json();
                    }).then(this.handleErrors)
                    .then(function(data) {
                        console.log(data);
                    
                    }).catch(function(error) {
                        alert(error.message);
                    });
    
                },
                
                handleErrors(response){
                    if(response.error != undefined){
                        throw Error(response.error);
                    }
                    return response;
                },

                getCookie(cname) {
                    let name = cname + "=";
                    let decodedCookie = decodeURIComponent(document.cookie);
                    let ca = decodedCookie.split(';');
                    for(let i = 0; i <ca.length; i++) {
                        let c = ca[i];
                        while (c.charAt(0) == ' ') {
                        c = c.substring(1);
                        }
                        if (c.indexOf(name) == 0) {
                        return c.substring(name.length, c.length);
                        }
                    }
                    return "";
                }
            }, 
            beforeMount(){
                this.Sexo()
            }
        }
    
    </script>