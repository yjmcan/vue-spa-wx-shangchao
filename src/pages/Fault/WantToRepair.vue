// '故障报修' - '我要报修'页
<template lang="pug">
#wantToRepair.Fault--module
    // 多行文本输入框( 限制500字 )
    <!--MtextBox.auto&#45;&#45;moduleMarginBottom( v-bind:setMtextBoxObj="setMtextBox" )-->

    // 图片上传(  )
    //#upload
    //div.ftp
    //    span 您最多可上传
    //    span.dll 5
    //    span 张图片，单张照片最大2M

    // 单行文本
    FortForm( v-bind:FortInputArr="fortInputText" )
</template>

<script>
import FortForm     from '../../components/common/FortForm'
// import MtextBox     from '../../components/common/MtextBox'
// import tinyImgUpload from '../../../static/js/tinyImgUpload'

const components = { FortForm }

export default {
    name: 'WantToRepair',
    mothods: {

    },
    data() {
        return {
            // 多行文本 基本配置
            setMtextBox: {
                maxLength: 500,
                placeholder: '请输入问题详情, 以便我们更好地处理'
            },
            // Fort.js 文本框内容
            fortInputText: [
                {
                    inputName: 'userName',
                    inputType: 'text',
                    maxlength: '10',
                    title: '报修人',
                    placeholder: '您的称呼'
                }, {
                    inputName: 'phone',
                    inputType: 'number',
                    maxlength: '13',
                    title: '电话',
                    placeholder: '您的手机号'
                }
            ]
        }
    },
    mounted: function() {
        // 在这配置一下 options => 基本参数
//        let options = {
//            path: '/',
//            // 成功时
//            onSuccess: function( res ) {
//                console.log( res )
//                console.log( '成功' )
//            },
//            onFailure: function( res ) {
//                console.log( res )
//                console.log( '失败' )
//            }
//        }
//
//        tinyImgUpload( '#upload', options ) // 执行 上传事件
    },
    components: components
}
</script>

<style lang="sass">
@import "../../sass/main"
.addimg
/*.ftp*/
    /*color: rgb( 178,178,178 )*/
    /*font-size: 14px*/
    /*margin-left: 15.5px*/
    /*padding-bottom: 15.5px*/
    /*padding-top: 15.5px*/
    /*.dll*/
        /*color: rgb( 35,210,150 )*/
#wantToRepair

</style>

