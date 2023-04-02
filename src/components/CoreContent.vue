<template>
    <div class="container">
        <video id="myvideo" :src="vList[curr]" class="Video" controls preload="auto" muted="muted">
            <!-- <source src="" type='video/mp4' />  -->
        </video>
        <div class="flavr-container modal center shown" style="display:none">
            <div class="flavr-overlay"></div>
            <div class="flavr-fixer">
                <div class="flavr-outer">
                    <div class="flavr-content">
                        <div class="flavr-icon"><img src="../img/股权出质.png"></div>
                        <h1 class="flavr-title">请输入您的出资及占股意愿</h1>
                        <div class="flavr-message">
                            <form class="flavr-form" method="post">
                                <div class="form-row"> 出资金额(0-100万): <input type="text" name="money" placeholder="Money">
                                </div>
                                <div class="form-row"> 占股比例(0-100%): <input type="text" name="holding"
                                        placeholder="Holding">
                                </div>
                                <div class="form-row"> </div>
                            </form>
                        </div>
                    </div>
                    <div class="flavr-toolbar inline"><a href="#" class="flavr-button danger" rel="btn-submit">提交</a><a
                            href="#" class="flavr-button default" rel="btn-cancel">重新输入</a></div>
                </div>
            </div>
        </div>
    </div>
</template>

<style>
.Video{
    margin-top: -30px;
    width: 900px;
    height: 630px;
}
.container {
    width: 910px;
    height: 645px;
    margin-top: 10px;
    border: 1px solid #DFDEDE;
    box-shadow: #DFDEDE 1px 1px 5px 1px;
}
.flavr-container {
            /* display: none; */
            position: fixed;
            text-align: center;
            left: 0;
            right: 0;
            top: 0;
            bottom: 0;
            z-index: 999;
            overflow: hidden;
            -webkit-transform: translateZ(0);
            -moz-transform: translateZ(0);
            -ms-transform: translateZ(0);
            -o-transform: translateZ(0);
            transform: translateZ(0)
        }

        .flavr-container *,
        .flavr-container *:before,
        .flavr-container *:after {
            -webkit-box-sizing: border-box;
            -moz-box-sizing: border-box;
            -ms-box-sizing: border-box;
            box-sizing: border-box
        }

        .flavr-container .flavr-overlay {
            position: fixed;
            top: 0;
            right: 0;
            bottom: 0;
            left: 0;
            visibility: inherit;
            background: rgba(0, 0, 0, 0.4)
        }

        .flavr-container .flavr-fixer {
            position: relative;
            margin: 12% auto 0;
            display: inline-block;
            width: auto;
            pointer-events: auto;
            -webkit-transition: margin .3s;
            -moz-transition: margin .3s;
            -o-transition: margin .3s;
            transition: margin .3s
        }

        .flavr-container .flavr-fixer .flavr-outer {
            background: #2e3846;
            min-width: 300px;
            height: auto;
            text-align: center;
            font-family: Helvetica, Arial, sans-serif;
            -webkit-border-radius: 3px;
            -moz-border-radius: 3px;
            border-radius: 3px;
            -webkit-background-clip: padding-box;
            -moz-background-clip: padding-box;
            background-clip: padding-box;
            -webkit-box-shadow: 0 2px 4px 0 rgba(0, 0, 0, 0.3);
            -moz-box-shadow: 0 2px 4px 0 rgba(0, 0, 0, 0.3);
            box-shadow: 0 2px 4px 0 rgba(0, 0, 0, 0.3)
        }

        .flavr-container .flavr-fixer .flavr-outer .flavr-content {
            font-size: 14px;
            color: #fff;
            padding: 20px 30px 8px
        }

        .flavr-container .flavr-fixer .flavr-outer .flavr-content .flavr-icon {
            margin-top: 10px;
            margin-bottom: 10px
        }

        .flavr-container .flavr-fixer .flavr-outer .flavr-content .flavr-icon img {
            max-height: 40px;
            max-width: 40px
        }

        .flavr-container .flavr-fixer .flavr-outer .flavr-content .flavr-title {
            margin: 0;
            margin-bottom: 6px;
            font-size: 1.3em;
            line-height: 1.5
        }

        .flavr-container .flavr-fixer .flavr-outer .flavr-content .flavr-message {
            margin-top: 6px;
            color: inherit;
            text-shadow: 2px 2px rgba(0, 0, 0, 0.1);
            line-height: 1.5
        }

        .flavr-container .flavr-fixer .flavr-outer .flavr-content .flavr-message form .form-row {
            text-align: left;
            margin-top: 8px
        }

        .flavr-container .flavr-fixer .flavr-outer .flavr-content .flavr-message form input {
            display: block;
            width: 100%;
            border: 0;
            padding: 8px 6px 7px 15px;
            background-color: #f6f6f6;
            outline: none;
            height: 35px
        }

        .flavr-container .flavr-fixer .flavr-outer .flavr-toolbar {
            white-space: nowrap;
            padding: 0 30px 20px
        }

        .flavr-container .flavr-fixer .flavr-outer .flavr-toolbar .flavr-button {
            outline: none;
            display: block;
            text-decoration: none !important;
            padding: 7px 12px;
            margin-top: 8px;
            margin-bottom: 4px;
            font-size: 13px;
            font-weight: normal;
            line-height: 1.428571429;
            color: #fff;
            background-color: #795aac;
            text-align: center;
            white-space: nowrap;
            vertical-align: middle;
            cursor: pointer;
            background-image: none;
            border: none;
            -webkit-border-radius: 3px;
            -moz-border-radius: 3px;
            border-radius: 3px;
            -webkit-background-clip: padding-box;
            -moz-background-clip: padding-box;
            background-clip: padding-box;
            -webkit-touch-callout: none;
            -webkit-user-select: none;
            -khtml-user-select: none;
            -moz-user-select: none;
            -ms-user-select: none;
            user-select: none;
            -webkit-transition: all ease .3s;
            -moz-transition: all ease .3s;
            -o-transition: all ease .3s;
            transition: all ease .3s
        }

        .flavr-container .flavr-fixer .flavr-outer .flavr-toolbar .flavr-button:hover,
        .flavr-container .flavr-fixer .flavr-outer .flavr-toolbar .flavr-button:focus {
            outline: none;
            background-color: #3e4b5d;
            color: #fff
        }

        .flavr-container .flavr-fixer .flavr-outer .flavr-toolbar .flavr-button.danger {
            background-color: #f44a56
        }

        .flavr-container .flavr-fixer .flavr-outer .flavr-toolbar .flavr-button.danger:hover,
        .flavr-container .flavr-fixer .flavr-outer .flavr-toolbar .flavr-button.danger:focus {
            background-color: #3e4b5d
        }

        .flavr-container .flavr-fixer .flavr-outer .flavr-toolbar.inline .flavr-button {
            display: inline-block;
            width: auto;
            min-width: 120px;
            margin-left: 6px;
            margin-top: 2px
        }

        .flavr-container .flavr-fixer .flavr-outer .flavr-toolbar.inline .flavr-button:first-child {
            margin-left: 0
        }
</style>
<script>
export default {
    name: 'CoreContent',
    data() {
        return {
            vList : ['/media/试玩1.fcc3846f.mp4', '/media/试玩2.4acc0394.mp4', '/media/试玩3.409c92ad.mp4','/media/试玩4.bc04ac39.mp4','/media/试玩5.f4038adc.mp4','/media/试玩6.0d1e0881.mp4','/media/试玩7.85186844.mp4'], // 初始化播放列表
            vLen: 7,
            curr:0,
        }
    },
    methods: {
        videoplay() {
            
            if (this.curr == 2) {
                let flavr_container = document.querySelector('.flavr-container');
                flavr_container.style.display = "block";
            }
            this.curr++;
            console.log("this.play");
            console.log(this.curr);
            
            if (this.curr >= this.vLen) {
                this.curr = 0; //重新循环播放
            }
        }
    },
    mounted: function(){
        let myvideo = document.querySelector('#myvideo');
        // console.log(video.src);
        // console.log(this.$refs.vueMiniPlayer.pause());
        
        				//video 为jq对象，原生对象把video[0]换成原生对象即可 
        myvideo.play();

        

        let that = this;
        myvideo.addEventListener('ended', function () {//监听事件
            console.log("nextvedio");
            that.videoplay();
        });
        console.log(this.curr);
    }
}



</script>
