<template>
    <div>
        <Head />
        <nuxt-link :to='"/write"'>
        <el-container>
            <el-main>
                <el-button type="primary" icon="el-icon-plus">
                    Create
                </el-button>
            </el-main>
        </el-container>
        </nuxt-link>
    </div>
</template>

<script>
import Head from '@/components/Head.vue'
export default {
    components:{
        Head
    }
}
</script>

<style>

</style>
