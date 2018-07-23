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
                                
                                    <nuxt-link :to='"/login"' v-if="statActive<3">
                                        <el-button style="float: right; padding: 3px 0" type="text">
                                            Log In
                                        </el-button>
                                    </nuxt-link>
                                
                            </div>
                            <el-steps :active="statActive" align-center finish-status="success">
                                <el-step title="Step 1" description="Email">
                                </el-step>
                                <el-step title="Step 2" description="Personal Details">
                                </el-step>
                                <el-step title="Step 3" description="Profile Photo">
                                </el-step>
                                <el-step title="Step 4" description="Finish">
                                </el-step>
                            </el-steps>
                            <br>
                            <el-form ref="form" :model="form" label-width="">
                                <div v-if="statActive==0" class="block">
                                    <el-form-item label="Email">
                                        <el-input type="email" v-model="email"></el-input>
                                    </el-form-item>
                                </div>
                                <div v-if="statActive==1" class="block">
                                    <el-form-item label="Full Name">
                                        <el-input type="text" v-model="name"></el-input>
                                    </el-form-item>
                                    <el-form-item label="Password">
                                        <el-input type="password" v-model="password"></el-input>
                                    </el-form-item>
                                </div>
                                <div v-if="statActive==2" class="block">
                                    <el-upload
                                        class="upload-demo"
                                        drag
                                        action="https://jsonplaceholder.typicode.com/posts/"
                                        :on-preview="handlePreview"
                                        :on-remove="handleRemove"
                                        :file-list="fileList"
                                        multiple>
                                        <i class="el-icon-upload"></i>
                                        <div class="el-upload__text">Drop file here or <em>click to upload</em></div>
                                        <div class="el-upload__tip" slot="tip">jpg/png files with a size less than 500kb</div>
                                    </el-upload>
                                </div>
                                <div v-if="statActive==3" class="block">
                                    <h1 style="text-align:center;color:green"><i class="el-icon-check"></i> You are all set</h1>
                                    <center>
                                        <nuxt-link :to='"/mypage"'>
                                            <el-button type="primary">Get Started</el-button>
                                        </nuxt-link>
                                    </center>
                                </div>
                            </el-form>
                            <el-button v-if="statActive<3" @click="statActive++%4" type="text" style="float:right">Next <i class="el-icon-arrow-right el-icon-right"></i></el-button>
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
            statActive:0,
            email:'',
            name:'',
            password:''
        }
    }
}
</script>

<style>

</style>
