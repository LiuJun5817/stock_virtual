<template>
    <div class="flow_box">
        <div class="process_box">
            <div class="process_num">
                <a>1</a>
            </div>
            <div class="line"></div>
            <div class="process_name">
                <a>试玩</a>
            </div>
        </div>
        <div class="process_box">
            <div class="process_num">
                <a>2</a>
            </div>
            <div class="line"></div>
            <div class="process_name">
                <a>MVP迭代预算</a>
            </div>
        </div>
        <div class="process_box">
            <div class="process_num">
                <a>3</a>
            </div>
            <div class="line"></div>
            <div class="process_name">
                <a>团队选择</a>
            </div>
        </div>
        <div class="process_box">
            <div class="process_num">
                <a>4</a>
            </div>
            <div class="line"></div>
            <div class="process_name">
                <a>出资占股决策</a>
            </div>
        </div>
        <div class="process_box">
            <div class="process_num">
                <a>5</a>
            </div>
            <div class="line"></div>
            <div class="process_name">
                <a>股权激励规则设置</a>
            </div>
        </div>
        <div class="process_box">
                <div class="process_num">
                    <a>6</a>
                </div>
                <div class="line"></div>
                <div class="process_name">
                    <a>股权转让</a>
                    <a>规则设置</a>
                </div>
            </div>
        <div class="process_box">
                <div class="process_num">
                    <a>7</a>
                </div>
                <div class="line"></div>
                <div class="process_name">
                    <a>股东退出规则设置</a>
                </div>
            </div>
        <div class="process_box">
                <div class="process_num">
                    <a>8</a>
                </div>
                <div class="line"></div>
                <div class="process_name">
                    <a>公司运营</a>
                </div>
            </div>
        <div class="process_box">
                    <div class="process_num">
                        <a>9</a>
                    </div>
                    <div class="line"></div>
                    <div class="process_name">
                        <a>产品估值</a>
                    </div>
                </div>  
        <div class="process_box">
                    <div class="process_num">
                        <a>10</a>
                    </div>
                    <div class="process_name">
                        <a>实验得分</a>
                    </div>
                </div>          
    </div>
</template>

<script>
export default {
    name: 'FlowChart',
}
</script>

<style>
.flow_box {
    width: 240px;
    height: 645px;
    margin-top: 10px;
    border: 1px solid #DFDEDE;
    box-shadow: #DFDEDE 1px 1px 5px 1px;
}

.process_box {
    /* border-left: 4px solid #EFB82E; */
    /* border: 1px solid black; */
    margin-left: 30px;
    
    height: 65px;
}

.line{
    width: 0;
    height: 33px;
    float: left;
    margin-left: -18px;
    margin-top: 44px;
    /* border-left: 4px solid #EFB82E; */
    border-left: 4px solid #51545D;

}

.process_num{
    width: 35px;
    height: 35px;
    background-color: #51545D;
    /* background-color: #EFB82E; */
    border-radius: 50%;
    margin-left: -20px;
    margin-top: 10px;
    float: left;
    /* margin: 0 auto; */
}

.process_num a{
    color: white;
    font-size: 22px;
    line-height: 35px;
    text-align: center;
}

.process_name{
    float: left;
    /* margin-top: 20px; */
    margin-left: 10px;
    width: 170px;
    height: 50px;
    background-color: #FBFAF4;
    border: 1px solid #DFDEDE;
    box-shadow: #DFDEDE 1px 1px 5px 1px;
    
}

.process_name a{
    font-size: 18px;
    line-height: 50px;
    text-align: center;
}
</style>