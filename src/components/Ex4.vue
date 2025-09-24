<script>
    // commit
    export default { 
        data() {
            return {
                // Add code here
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
        <div v-bind:id="id" class="m-2">
            div ID : {{id}} 
        </div>
        
        <button type="button" class="btn" 
        :class="{ 
            'btn-secondary': !isActive, 'btn-danger': isActive, 
            'blueBox': !isActive, 'redBox': isActive
        }" 
        @click="changeColour">Change Color</button>
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
