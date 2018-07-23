<template>
    <div style="background-color:aliceblue">
        <el-container>
            <el-main>
                <el-row>
                    <el-col :span=9>&nbsp;</el-col>
                    <el-col :span=6>
                        <h1 style="margin:0; font-family:'Schoolbell';text-align:center;font-size:5em">TravelPost</h1>
                        <el-card class="box-card">
                            <div slot="header" class="clearfix">
                                <span>Log In</span>
                                
                                    <nuxt-link :to='"/register"'>
                                        <el-button style="float: right; padding: 3px 0" type="text">
                                            Sign Up
                                        </el-button>
                                    </nuxt-link>
                                
                            </div>
                            
                            <el-form ref="form" :model="form" label-width="120px">
                                <el-form-item label="Email">
                                    <el-input type="email" v-model="form.email"></el-input>
                                </el-form-item>
                                <el-form-item label="Password">
                                    <el-input type="password" v-model="form.password"></el-input>
                                </el-form-item>
                                
                                <el-form-item>
                                    <el-button type="primary" @click="onSubmit">Sign In</el-button>
                                    <nuxt-link :to='"/"'>
                                        <el-button type="danger" plain>Exit</el-button>
                                    </nuxt-link>
                                </el-form-item>
                            </el-form>
                        </el-card>
                    </el-col>
                    <el-col :span=9>&nbsp;</el-col>
                </el-row>
            </el-main>
        </el-container>
    </div>
</template>

<script>
export default {
    data() {
      return {
        form: {
          email: '',
          password: '',
        }
      }
    },
    methods: {
      onSubmit() {
        console.log('submit!');
      }
    }
}
</script>

<style>

</style>
