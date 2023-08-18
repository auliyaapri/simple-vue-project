<template>
        Hello, ini adalah komponen student {{ nameStudent }}         
         <button @click="notification">Klik Detail Bro</button><br><br>

         <slot>Ini adalah slot</slot>

</template>

<script >
    export default {
        props : {
            nameStudent : String
        },
        emits: ['response'],
        // methods: {
        //     notification() { // Method notification akan dipanggil ketika tombol diklik.
        //         this.$emit('show-alert', `detail untuk siswa ${this.nameStudent}`)
        //         console.log(notification);
        //     }
        // },
        methods: {
            notification() { // Method notification akan dipanggil ketika tombol diklik.
                this.$emit('response', this.nameStudent)
                // console.log(this.$emit('response', this.nameStudent));
            }
        },
        
    }
    
</script>


