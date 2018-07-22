<template>
    <div>
        <el-container>
            <el-main>
                <el-row>
                    <el-col :span=8>&nbsp;</el-col>
                    <el-col :span=8>
                        <h1 style="margin:0; font-family:'Schoolbell';text-align:center;font-size:5em">TravelPost</h1>
                        <el-card class="box-card">
                            <div slot="header" class="clearfix">
                                <span>Sign Up</span>
                                
                                    <nuxt-link :to='"/login"'>
                                        <el-button style="float: right; padding: 3px 0" type="text">
                                            Log In
                                        </el-button>
                                    </nuxt-link>
                                
                            </div>
                            <el-steps :active="statActive" align-center>
                                <el-step title="Step 1" description="Email" status="success">
                                    a
                                </el-step>
                                <el-step title="Step 2" description="Personal Details">
                                    v
                                </el-step>
                                <el-step title="Step 3" description="Profile Photo">
                                    h
                                </el-step>
                                <el-step title="Step 4" description="Finish">
                                    j
                                </el-step>
                            </el-steps>
                        </el-card>
                    </el-col>
                    <el-col :span=8>&nbsp;</el-col>
                </el-row>
            </el-main>
        </el-container>
    </div>
</template>

<script>
export default {
    data(){
        return {
            statActive:0
        }
    }
}
</script>

<style>

</style>
