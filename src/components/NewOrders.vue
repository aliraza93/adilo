<template>
    <div class="col-3">
        New Orders
        <div class="card" v-for="(value, index) in newOrders" :key="index" style="margin-top: 15px;">
            <div class="dropup">
                <div class="menu">
                    <span><i class="fas fa-bars"></i></span>
                </div>
                <div class="menu-content">
                    <a href="#" @click="remove(index)">Remove item</a>
                </div>
            </div>
            <div class="main-content">
                <div class="column-6">
                <img src="https://hips.hearstapps.com/hmg-prod.s3.amazonaws.com/images/yucca-cane-plant-in-a-pot-on-a-white-background-royalty-free-image-1580856558.jpg?crop=0.91771xw:1xh;center,top&resize=480:*" alt="Test Image">
                </div>
                <div class="column-6">
                <span class="badge" style="margin-top: 40%;">{{ value.title }}</span><br>
                <span class="delivery">5 days left</span><br>
                <div style="display: flex;">
                    <span class="time">20 hrs</span>
                    <span class="pipe">|</span>
                    <span class="budget">$320</span>  
                </div>
                </div>
            </div>
            <div class="main-content" style="border-top: 1px solid lightgray;">
                <div class="column-6" style="margin-top: 12px;">
                <span style="color: gray; font-size: 13px;">View Order</span>
                </div>
                <div class="column-6" style="margin-top: 7px;">
                <img style="float: right; width: 30px; height: 30px; border-radius: 50%;" src="https://images.unsplash.com/flagged/photo-1570612861542-284f4c12e75f?ixid=MnwxMjA3fDB8MHxzZWFyY2h8Mnx8cGVyc29ufGVufDB8fDB8fA%3D%3D&ixlib=rb-1.2.1&w=1000&q=80" alt="">
                </div>
            </div>
        </div>

        <div v-if="!newOrders.length > 0" style="margin-top: 10px;">
            <span style="color: red;">Oops, no items found</span>
        </div>

    </div>
</template>

<script>
export default {
    name: 'new-orders',
    data() {
        return {
            newOrders: [
                { title: 'New Order'},
                { title: 'New Order' }
            ]
        }
    },

    methods: {
        remove(index) {
            this.newOrders.splice(index, 1);
            alert('Item removed successfully.')
        }
    }

}
</script>