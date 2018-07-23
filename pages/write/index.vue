<template>
    <div>
        <Head />
        <el-container>
            <el-main>
                <el-row>
                    <el-col :span=8>&nbsp;</el-col>
                    <el-col :span=8>
                        <el-card class="box-card" v-loading="clicked">
                            <div slot="header" class="clearfix">
                                <span>{{ title==''?'New Post':title }}</span>
                            </div>
                            <el-form ref="form" :model="form" label-width="120px">
                                <el-form-item label="Title">
                                    <el-input v-model="title"></el-input>
                                </el-form-item>
                                <el-form-item label="Activity zone">
                                    <div class="block">
                                        <el-date-picker
                                        v-model="date"
                                        type="daterange"
                                        range-separator="To"
                                        start-placeholder="Start date"
                                        end-placeholder="End date" style="width:100%">
                                        </el-date-picker>
                                    </div>
                                </el-form-item>
                                <el-input
                                    type="textarea"
                                    :rows="10"
                                    placeholder="Tell your story"
                                    v-model="textarea">
                                </el-input>
                                <br>
                                <br>
                                <br>
                                <el-form-item style="float:right">
                                    <el-button><i class="el-icon-document"></i> Save as Draft</el-button>
                                    <el-button type="danger" plain><i class="el-icon-delete"></i> Discard</el-button>
                                    <el-button type="primary" @click="onSubmit"><i class="el-icon-check"></i> Create</el-button>
                                </el-form-item>
                            </el-form>
                        </el-card>
                    </el-col>
                    <el-col :span=8>&nbsp;</el-col>
                </el-row>
            </el-main>
        </el-container>
    </div>
</template>

<script>
import Head from '@/components/Head.vue'
export default {
    components:{
        Head
    },
    data() {
      return {
          title:'',
          date:'',
          clicked:false,
        form: {
          name: '',
          region: '',
          date1: '',
          date2: '',
          delivery: false,
          type: [],
          resource: '',
          desc: ''
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
