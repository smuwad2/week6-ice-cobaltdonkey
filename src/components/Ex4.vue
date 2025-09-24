<script>
    // commit 2
    export default { 
        data() {
            return {
                // Add code here
                id: "demo1",
                isActive: false
            }
        },
        methods: { 
   			// Add code here
            changeColour() {
                this.isActive = !this.isActive;
            }
		}
    }
</script>

<template>
    
    <!-- Modify code here -->
    <div class="container">
        <div id="demo1" class="m-2" :class="{ blueBox: !isActive, redBox: isActive }"> 
            div ID : demo1
        </div>

        <button type="button" class="btn" 
        :class="{ 'btn-primary': !isActive, 'btn-danger': isActive }"
        @click="changeColour">
            Change Color
        </button>
    </div>

</template>

<style scoped>
    .redBox {
        background-color: red;
    }
    .blueBox {
        background-color: blue;
    }
    #demo1 {
        color: white;
    }
</style>
