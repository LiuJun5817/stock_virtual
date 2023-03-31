<template>
    <div id="info_box">
        <div class="text_info">
            <a>用户操作时间：</a>
        </div>
        <div class="clock">
            <div class="top">
                <div class="t1 btn"></div>
                <div class="t2 btn"></div>
                <div class="t3 btn"></div>
            </div>
            <div class="inside">
                <div class="hour screen">{{timeh}}h</div>
                <div class="minute screen">{{ timef }}m</div>
                <div class="second screen">{{ times }}s</div>
            </div>
        </div>
        <div class="text_info">
            <a>企业运营时间：{{timeyear}}年</a>
        </div>
        <div class="text_info">
            <a>初创团队人数：{{teamNum}}人</a>
        </div>
        <div class="text_info">
            <a>正式实验次数：{{testNum}}次</a>
        </div>
    </div>    
</template>

<script>
export default {
    name: 'Info',
    data() {
        return {
            timeh: '0',
            timef: '0',
            times: '0',
            timeyear: 0,
            teamNum: 5,
            testNum:0,
        }
    },
    methods: {
        
    },
    created() {
        setInterval(() => {
            this.times++;
            if (this.times == 60) {
                this.times = 0;
                this.timef++;
            }
            if (this.timef == 60) {
                this.timef = 0;
                this.timeh++;
            }
        }, 1000);
    }
}

</script>

<style>
#info_box {
    width: 240px;
    height: 645px;
    margin-top: 10px;
    border: 1px solid #DFDEDE;
    box-shadow: #DFDEDE 1px 1px 5px 1px;
    position: relative;
}
#info_box a{
    font-size: 18px;
    text-align:left;
}
.inside,
.screen {
    display: flex;
    justify-content: center;
    align-items: center;
}

.clock {
    display: block;
    width: 220px;
    height: 105px;
    background-color: #2b3430;
    margin-left: 10px;
    margin-top: 10px;
    margin-bottom: 20px;
    border-radius: 10px;
}

.inside {
    width: 100%;
    height: 100%;
    flex-direction: row;
    margin-top: -50px;
}

.screen {
    width: 45%;
    margin: 0 6px;
    border-radius: 7px;
    height: 90%;
    background-color: #3c3d3a;
    color: white;
    font-size: 40px;
}

.top {
    width: 100%;
    height: 50px;
}

.btn {
    position: absolute;
    width: 20px;
    height: 6px;
    background-color: #3c3d3a;
    top: 28px;
}

.t1 {
    left: 21px;
}

.t2 {
    left: 53px;
}

.t3 {
    left: 125px;
}

.text_info{
    margin-left: 10px;
    margin-bottom: 10px;
}
</style>