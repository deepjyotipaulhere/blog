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
                            <el-steps :active="statActive" align-center finish-status="success">
                                <el-step title="Step 1" description="Email">
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
                            <div v-if="statActive==0" class="block">
                                a
                            </div>
                            <div v-if="statActive==1" class="block">
                                d
                            </div>
                            <div v-if="statActive==2" class="block">
                                hg
                            </div>
                            <div v-if="statActive==3" class="block">
                                hj
                            </div>
                            <el-button @click="statActive++%4" type="text" style="float:right">Next <i class="el-icon-arrow-right el-icon-right"></i></el-button>
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
