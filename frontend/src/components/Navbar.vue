<template>
    <div>
        <nav class="navbar is-info" role="navigation" aria-label="main naviation" style="min-height: rem">
            <div class="navbar-brand">
                <a class="navbar-item is-size-4">Funzwa</a>
            </div>

            <div id="navbar-item" class="navbar-menu">
                <div class="navbar-start">
                    <a href="/" class="navbar-item">Home</a>
                     <a href="/about" class="navbar-item">About</a>
                </div>

                <div class="navbar-end">
                    <div class="navbar-item">
                        <div class="buttons">
                            <a href="/sign-up" class="button is-primary"><strong>Sign up</strong></a>
                            <a href="/log-in" class="button is-light">Log in</a>
                        </div>  

                    </div>

                </div>
            </div>

        </nav>
    </div>
</template>

<script>
export default {
    name: 'Navbar'
}
</script>

