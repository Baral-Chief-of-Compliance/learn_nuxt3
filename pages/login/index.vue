<template>
    <div>
        <div>
            <form class="grid grid-rows-3 gap-4 py-10">
                 <div class="grid grid-flow-col gap-10">
                    <div></div>
                        <input v-model="login" class="text-black" placeholder="Логин">
                    <div></div>
                 </div>
                
                 <div class="grid grid-flow-col gap-10">
                    <div></div>
                        <input v-model="password" class="text-black border-2 px-4 py-2 border-blue-500 rounded-full focus:ring-blue-700 focus:border-blue-700" placeholder="Пароль">
                    <div></div>
                 </div>
                
                 <div class="grid grid-flow-col gap-10">
                    <div></div>
                    <button @click="enter()" class="bg-blue-500 hover:bg-blue-700 py-2  rounded-full" type="submit">Вход</button>
                    <div></div>
                 </div>
                
                <div></div>
            </form>

            {{ this.login }}

            {{ this.password }}

        </div>
    </div>
</template>

<script>
export default{
    data(){
        return{
            login: "",
            password: ""
        }
    },

    methods: {
        enter(){
            localStorage.setItem('login', this.login)
            localStorage.setItem('password', this.password)

            const router = useRouter()

            router.push({ path: "/"})
        }
    }
}
</script>