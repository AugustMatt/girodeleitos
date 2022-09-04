<template>
    <div class="header-left-bottom">
        <form action="#" method="post">
            <div class="icon1">
                <span class="fa fa-user"></span>
                <input type="email" placeholder="Email" required />
            </div>
            <div class="icon1">
                <span class="fa fa-lock"></span>
                <input type="password" placeholder="Senha" required />
            </div>
            <div class="login-check">
                <label class="checkbox"><input type="checkbox" name="checkbox" checked><i> </i> Mantenha-me Logado</label>
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