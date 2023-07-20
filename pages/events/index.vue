

<template>
    <div class="container px-3 py-3 mx-auto">
        <h1 class="text-teal-500">events page</h1>
    </div>
    <Alert />
    <Profile />
    <IconsNasa />
</template>


<script>

export default{
    data(){
        return{
            greetings: "hello from options API"
        }
    },

    methods: {
        say_hello(){
            console.log(this.greetings)
        }
    },

    beforeCreate(){
        console.log("hello from options API beforeCretate")
    },

    created(){
        this.say_hello()
    },

    setup(){

        const { sayHello } = useUtils()


        onMounted(() => {
            console.log("Hello from composition API on Mounted")
        }
        )
        sayHello()
    }
}
</script>
