# battle-of-pens
## 永远的“弹笔”
此仓库为神岛地图“弹笔”开源代码，按MIT协议提供。该地图目前已不再更新。

本仓库更新日期：2025年5月25日
## server
### index.js
```javascript
/*
world.onTick(()=>{world.say(`世界人数:${world.querySelectorAll("player").length}`)})
world.onPlayerJoin(p=>p.entity.player.canFly = 1)
*/
require("./main.js");
/*挂机括号(  )
todo{
    
    足球赛
    重构比赛系统
    笔筒 不采纳
    MVP得到更多小橡皮 已完成
    ui封装与缓存 已完成
    观战自由视角(Daniel林子) 不采纳
    订书机(云里雾里) 已有模型 已完成
    音乐火影RISE(L-342) 不采纳
    取消打开盲盒(wccwcc) 已完成
    单笔模式(某只咕咕小鸽子) 不采纳
    PVP(诗仙李白打老虎) 不采纳
    小橡皮固定时间(鼠窝中的笨鼠) 已完成
    萝卜刀(云里雾里) 不采纳
    戒尺(鼠窝中的笨鼠) 已有模型 已完成
    黑板擦(ZiganotosaurusSpinosaurusTyrar)
    量角器(洒脱的小蓝t1z4) 已完成
    召唤班主任技能(名字真难) 不采纳
    转笔技能(洒脱的小蓝t1z4) 不采纳
    生化模式{
        教室门口传来了一阵脚步声……
        笔，不是玩具，是文具！
        我的办公室里有一个袋子用来统一保管你们的玩具！
        学生，就应该干学生该干的事！
        xxx被没收
    }(一只果蒋吖) 不采纳
    右键蓄力技能 已改为长按蓄力，已完成
    夹子(越打力度越小)(洒脱的小蓝t1z4) 不采纳
    神龙摆尾技能(机灵的神射手) 不采纳
    盲盒空盒(U.S.S尛黍諟) 已完成
    美工刀(叛腻der泥) 不采纳
    涂卡笔(mzaa但是暂退) 不采纳
    水笔(一颗红小豆) 不采纳
}
转移测试:
storage.getDataStorage("main").set("13033456",{items:["重重的橡皮"],boxes:[["超级文具盲盒",null]],joinTimes:10,totalScore: 54145,smallErasers: 54145,bestScore: 145})
145:寒假更新{
    pen.js 凑活
    match 实现了一半，放弃
    ui和匹配机制 凑活，鸽了吧
    用item实现的blindbox 鸽
}
145:{
段位 已完成
}
145:游乐场化{
引导报名 已完成
}
脚本喵：签到
万嘉麒：签到
145:todo{
测试新文具稀有度显示 已完成
修复神秘的盲盒不关闭bug
测试一遍游戏
}
万嘉麒：e，那个时候我代码写的太繁琐了
145:没事，我也看不懂大多数商业大陆代码。对话框背景改成透明了。
万嘉麒：地图一会黑屏选择框，一会屏幕一亮。我认为选择框背景色可以不调
万嘉麒：你的代码非常好，虽然我看不懂大部分代码。这个原因可能是我的能力不行或我的编程涉及面不够广
145:广告词{
    万物皆可弹4来啦！这是令人兴奋的万物皆可弹系列第四个地图！我们打破常规，引领创新的风潮！
    这个地图的独特之处在于，它并不依赖华丽的模型和复杂的代码，而只运用了纯色方块和不到1000行的代码，呈现出独特而奇妙的弹笔世界。我们和你一样在平板上敲代码一敲一卡，苦苦等待着编辑器对移动端创作的支持。我们没有使用官方未公开的api接口，如http和rtc，我们唯一使用的未公开api是借鉴了社区用户“145a”的gui代码。
    我们并非遥不可及的大佬，而是与你一样，怀揣梦想的普通岛民。我们热衷于探索、创新和分享。我们与你一起在首页地图中寻找灵感，梦想着成为地图制作的大佬。
    在社区论坛中，我们与你一同浏览、借鉴开源代码，分享我们的发现，共同解决其中的bug。我们希望通过这种方式，与您共同探索、学习和成长。
    在创作端，我们与你并肩作战，消掉一个又一个todo，为地图注入新的生命力。我们坚信，你的每一次游玩、点赞、分享、收藏、评论、issue，甚至是模型和代码的贡献，都对我们至关重要。
    为了回馈您的支持，我们承诺以下几点：首先，我们将永远不会推出氪金；其次，我们将免费向创作的你开放地图内广告位，与你共享成功的喜悦；最后，我们会向你开源所有代码，让你能够深入探索和继续创新。
    让我们携手共进，共同创造更多精彩！万物皆可弹4期待您的参与，让我们一起在这个奇妙的地图中探险、创新和成长！
}
万嘉麒：签到
145:模型任务:粉笔、毛笔
145:地图开始内测
简介{
万物皆可弹4全新启航啦！
这是全岛第五个弹笔地图，万物皆可弹系列的第四个作品。
}
145:第二阶段计划 已完成{
    1.(60/15)种文具 已完成
    2.总分排行榜 已完成
    3.单局排行榜 已完成
    4.盲盒提示(先把盲盒拆出来) 已完成
    5.Squads 已完成{
        先做一个队伍系统
        1.队伍属性 已完成
        2.npc索敌规则 已完成
        3.击杀判定规则 已完成
        4.击杀播报、计分规则 已完成
        5.队伍颜色 已完成
        6.分队 已完成
    }
    6.盲盒系统优化 已完成{
        1.BlindBoxConfigData类 已完成
        2.盲盒开启时间 已完成
    }
}
145:第一阶段已结束，现在地图完全适配Arena。
145:刺客，能帮我修个bug吗，我尽力了。就是main.js报名之后会加入游戏，创造笔实体后笔不知道为什么突然被destroy了。我查过了所有的destroy()，没找到问题在哪
145:遇到了难修的bug
145:爆肝一上午，gui初具雏形
145:有人吗
145:可恶的闪退
145:吉吉什么时候修一下bug
145:我试试
万嘉麒：其实我对这个一点都不懂...你完全可以自己写的...
145:还要更简单些，我之前写过一个简单的显示，可以用Promise封装一下，就像原生的对话框那样使用，还要一个全屏的背景 https://shequ.codemao.cn/mobile/community/549165
万嘉麒：经过两坤时的修改测试，GUI文本框函数已构建完成，详情请见文件“GUI测试专用”中的“dingyiGUI”函数以及文件第一行使用函数参照数组
145:主要是这个要展示大量内容，就是相当于重写对话框，这个新的对话框要全屏展示
万嘉麒：GUI函数经过一坤时修改测试有进展，勿动【2023/7/24/21:33:19】
万嘉麒：...关键我不知道GUI的输入框和选择框怎么写...
145:有人吗 有人做任务吗 ……
145:还有什么比修改自己一年前的破代码更加痛苦的？啊啊啊啊啊啊啊啊啊啊
145:我要让代码易扩展度和易维护度对标瓶盖人,我要挑战首页!!
145:没事慢慢来(有时间)
万嘉麒：只是告知...这是我搜到的，将要修改的内容
145:别写在index.js
万嘉麒：收到，GUI不会用...
145:代码规范{
    命名按照这个
    https://juejin.cn/post/7076259548872310814
    所有变量可修改可访问，易于调试
    //todo 待测试
    //tofix 待修复的bug
    //totest 待测试(自己写的totest可以让别人消)
    //patch 补丁，不需要时再移除
    //toremove 在每次大整理之后统一移除的无用代码
}
145:代码任务来了[
    一位大佬刚刚研究出来了一种GUI新技术 https://shequ.codemao.cn/community/552330
    代码任务是写一个GUI系统(写在main.js合适的位置(我也不知道哪里合适))
    需要提供三个快速显示GUI对话框的函数(跟官方对话框一样都是异步
    能兼容各种屏幕大小(手表除外)
    可以指定标题、选项、content、
    (文字、选项、输入(输入框))
    最后我来包装一下
]
万嘉麒：每天晚上我都会来，代码可以做什么任务呢
145:快来做任务啊!发布前一周会踢掉贡献最少的人，留下五个人{
    1.各式各样的笔模型(可以用Vobi)
    2.修正带模型(现在这个不行)
    3.地图宣传片(这个发布前10天开始做，有人领吗)（有jscode我领！！！！！！我会剪视频）
}
145:地图重启，重构代码!!!!{
    1.数据库 已完成
    2.大拆分计划(把所有代码拆成函数和多个文件 进行中
    (3).换模型(自制的模型)
    4.把不清楚的变量命名都改了，修改不合适的位置，按规范修改全部代码 进行中
    4.目标是确保所有数据都可访问可修改 进行中

以下内容暂缓，优先执行大拆分

    5.补丁系统(简)
    6.弹笔方向控制(待定)
    6.更换场景(建筑) 已完成
    7.笔的技能(待定)
    8.实时排行榜(待定)
    9.交易
    9.gui(如果可以) 已完成
    10.参加创作节(ye)
}
*/
```
### main.js
```javascript
/*main.js*/
require("./ui.js");
require("./145player.js");
require("./145match.js");
const { PenTeamType, PenConfigData } = require("./pen.js");

console.log("main.js开始运行");

const ADMIN_LIST = ["145a", "TQ.YFT.MOSS", "万嘉麒"];
let END_COUNDDOWN_TIME = 10;
let MIN_PLAYER_NUM = 10;
let MAX_ENEMY_BOT_NUM = 5;
let PEN_CLICK_COOL_DOWN_TIME = 1000;
const SPAWN_POS = new GameVector3(64, 10, 64);
const GameModeConfig = {

}
const GameModeType = {
    FFA: "自由混战赛",
    TDM: "团队淘汰赛",
    SIEGE: "无尽挑战赛"
};
const PEN_ENHANCE_SCALE_CONFIG = {
    "大大的": {
        scale: 1.5
    },
    "小小的": {
        scale: 0.8
    },
    "重重的": {
        mass: 1.5
    },
    "轻轻的": {
        mass: 0.8
    }
}
const PEN_CONFIG = {
    "铅笔": new PenConfigData("谁能借个削笔刀qwq，，", 4, 0.2, 0.3, 0),
    "蜡笔": new PenConfigData("不粘手()", 4, 0.2, 0.2, 0),
    "尺子": new PenConfigData("还带这么玩的？", 4, 0.2, 0.3, 1),
    "自动铅笔": new PenConfigData("借根铅芯呗)", 6, 0.2, 0.1, 1),
    "圆规": new PenConfigData("小心，它很尖。", 8, 0.1, 0.3, 3, 2),
    "剪刀": new PenConfigData("不带这么玩的！", 8, 0.1, 0.12, 3, 3),
    "橡皮": new PenConfigData("Q弹。", 6, 0.3, 0.2, 3),
    "马克笔": new PenConfigData("又轻又大。", 4, 0.1, 0.2, 1),
    "修正带": new PenConfigData("小心，别摔坏了。", 4, 0.1, 0.2, 1, 2),
    "口香糖": new PenConfigData("小又粘。", 4, 0.3, 0.1, 2, 2),
    "钢笔": new PenConfigData("好沉啊……", 8, 0.1, 0.2, 3),
    "订书机": new PenConfigData("没钉了:(", 7, 0.2, 0.05, 3),
    "圆珠笔": new PenConfigData("又细又黑。", 6, 0.2, 0.2, 2),
    "胶带": new PenConfigData("轻，但是上面有点胶。", 2, 0.3, 0.06, 1),
    "量角器": new PenConfigData("还带这么玩的？！", 4, 0.2, 0.4, 2, 2)
}
Object.keys(PEN_CONFIG).forEach((pen) => {
    PEN_CONFIG[pen].mesh = `mesh/${pen}.vb`;
    Object.keys(PEN_ENHANCE_SCALE_CONFIG).forEach((enchancement) => {
        PEN_CONFIG[enchancement + pen] = PEN_CONFIG[pen].toEnhanced(PEN_ENHANCE_SCALE_CONFIG[enchancement]);
    });
});
class BossConfigData extends PenConfigData {
    constructor(scale) {
        return super("Boss", 12, 0.5, scale, 1);
    }
}
const BOSS_CONFIG = {
    "水壶": new BossConfigData(0.2),
    "笔盒": new BossConfigData(0.4),
    "字典": new BossConfigData(0.4),
    "笔记本": new BossConfigData(0.5),
    "瓶子": new BossConfigData(0.4),
    "作业本": new BossConfigData(0.2),
    "戒尺": new BossConfigData(0.1)
};
Object.keys(BOSS_CONFIG).forEach((boss) => {
    BOSS_CONFIG[boss].mesh = `mesh/${boss}.vb`;
});
class BlindboxConfigData {
    constructor(stationeryNum, openingTimeNeedHour) {
        this.stationeryNum = stationeryNum;
        this.openingTimeNeed = openingTimeNeedHour * 60 * 60 * 1000;
    }
}
const BLINDBOX_CONFIG = {
    "普通文具盲盒": new BlindboxConfigData(1, 1),
    "幸运文具盲盒": new BlindboxConfigData(2, 2),
    "巨型文具盲盒": new BlindboxConfigData(4, 8),
    "超级文具盲盒": new BlindboxConfigData(8, 48)
};
let SCORE_PER_LEVEL = 10;
const LEVEL_DISPLAY_NAME = [
    "新手上桌",
    "江湖新秀",
    "技巧高手",
    "运笔大师",
    "控笔专家",
    "桌上传奇"
];
class CameraViewTypeData {
    constructor(setup) {
        this.setup = setup;
    }
}
const CameraViewType = {
    "第三人称跟随": new CameraViewTypeData((entity) => {
        entity.player.cameraMode = "follow";
        entity.player.cameraDistance = 50 * entity.screenAspectRatio;
        entity.player.swapInputDirection = false;
        entity.player.reverseInputDirection = GameInputDirection.NONE;
        entity.player.cameraFreezedAxis = GameCameraFreezedAxis.NONE;
        entity.player.freezedForwardDirection = null;
    }),
    "俯视": new CameraViewTypeData((entity) => {
        entity.player.cameraMode = GameCameraMode.RELATIVE;
        entity.player.cameraPosition = new GameVector3(-0.01, 70 * entity.screenAspectRatio, 0);
        entity.player.swapInputDirection = true;
        entity.player.reverseInputDirection = GameInputDirection.HORIZONTAL;
        entity.player.cameraFreezedAxis = GameCameraFreezedAxis.Y;
        entity.player.freezedForwardDirection = new GameVector3(0, 0, 1);
    })
}
function displayTimeMsNum(num) {
    const hourMs = 1000 * 60 * 60;
    const minMs = 1000 * 60;
    const secondMs = 1000;
    const hour = Math.floor(num / hourMs);
    const min = Math.floor(num % hourMs / minMs);
    const second = Math.floor(num % hourMs % minMs / secondMs);
    return `${hour}时${min}分${second}秒`;
}

function randomPos() {
    return new GameVector3(10 + Math.round(Math.random() * 107), 5, 10 + Math.round(Math.random() * 107));
}
function randomPen() {
    const s = Object.keys(PEN_CONFIG)[Math.floor(Math.random() * Object.keys(PEN_CONFIG).length)];
    let index = PEN_CONFIG[s].rarity + 1;
    if (1 / index < Math.random()) return randomPen();
    return s;
}

let endCountDownStarted = null;
let endCountdownStartSecond = null;
let gameModeVoteList = [];
let seigeCurrentWave = 0;

let gameMode = null;
let topContent = "弹笔";
const broadcastContent = [];
let bestScoreRank = "加载中，请稍后再试";
let totalScoreRank = "加载中，请稍后再试";

world.maxFog = 1;
world.fogHeightFalloff = 1;
world.fogHeightOffset = -5;
world.useOBB = true;
world.addCollisionFilter("player", "*");

function broadcast(content) {
    //world.say(content);
    broadcastContent.unshift(content);
    sleep(10000).then(() => broadcastContent.pop());
}

function setupPlayer(entity) {
    //转移和修复代码
    if (entity.stationery.length === 0 && entity.items?.length > 0) {
        try {
            entity.stationery = [...entity.items];
            entity.items = {};
        } catch (e) {
            entity.textDialog("数据库故障", `${e}\n请务必在评论区向我们反馈这些信息`);
            entity.stationery = [randomPen(), randomPen()];
            entity.items = {};
        }
    }
    entity.stationery = Array.from(new Set(entity.stationery));

    entity.isInGame = false;
    entity.pen = null;
    entity.watchGlobalPos = new GameVector3(64, 165, 64);
    entity.isCharging = false;
    entity.action0PressTime = null;
    Object.defineProperties(entity, {
        level: {
            get() {
                return LEVEL_DISPLAY_NAME[Math.floor(this.totalScore / SCORE_PER_LEVEL)] ?? LEVEL_DISPLAY_NAME[LEVEL_DISPLAY_NAME.length - 1];
            }
        },
        isControllingPen: {
            get() {
                return this.isInGame && this.pen;
            }
        },
        action0PressTimePassed: {
            get() {
                return Date.now() - this.action0PressTime;
            }
        },
        clickCoolDownTimeLeft: {
            get() {
                return Math.max(0, PEN_CLICK_COOL_DOWN_TIME - (Date.now() - entity.pen.lastClickTime));
            }
        },
        chargeScale: {
            get() {
                return (Math.sqrt(Math.sqrt(this.action0PressTimePassed)) / 2).toFixed(2);
            }
        },
        hasBlindboxOpening: {
            get() {
                return this.blindboxOpening.type !== null;
            }
        },
        blindboxOpeningTimeNeed: {
            get() {
                return BLINDBOX_CONFIG[this.blindboxOpening.type].openingTimeNeed
            }
        },
        blindboxOpeningTimePassed: {
            get() {
                return Date.now() - this.blindboxOpening.startTime;
            }
        },
        blindboxOpeningTimeLeft: {
            get() {
                return this.blindboxOpeningTimeNeed - this.blindboxOpeningTimePassed;
            }
        },
        blindboxOpeningCanOpen: {
            get() {
                return this.blindboxOpeningTimeLeft <= 0;
            }
        },
        speedupBlindboxPrice: {
            get() {
                return Math.max(1, Math.floor(this.blindboxOpeningTimeLeft / 1000 / 60 / 60));
            }
        },
        blindboxDisplay: {
            get() {
                if (!this.hasBlindboxOpening) {
                    return `待打开 ${entity.blindboxes.length} 盲盒`;
                } else if (this.blindboxOpeningCanOpen) {
                    return `${this.blindboxOpening.type} 已打开`;
                } else {
                    return `${this.blindboxOpening.type} 打开中\n剩余${displayTimeMsNum(this.blindboxOpeningTimeLeft)}`;
                }
            }
        },
        menuContent: {
            get() {
                return `[${this.level}] ${this.player.name}\n最高单局分数: ${this.bestScore}\n累计分数: ${this.totalScore}\n${this.blindboxDisplay}\n小橡皮: ${this.smallErasers}`;
            }
        }
    });
    entity.getBlindbox = function (BoxLv = 0) {
        this.blindboxes.push(Object.keys(BLINDBOX_CONFIG)[BoxLv]);
    };
    entity.joinGame = async function () {
        this.isInGame = true;
        this.player.cancelDialogs();
        for (let n = 0; n < 3; n++)
            await world.nextTick();
        this.position.copy(randomPos());
        this.pen = createPen(this.usePenType, `${this.player.name} 的 ${this.usePenType}`, this.position.clone());
        this.pen.owner = this;
        this.player.cameraEntity = this.pen;
        CameraViewType[this.cameraView].setup(this);
    };
    entity.exitGame = async function () {
        this.isInGame = false;
        if (this.isCharging) {
            this.isCharging = false;
        }
        const score = this.pen.currentRoundScore;
        let extra = `本局分数为${score}`;
        this.totalScore += score;
        if (score > 0) {
            let boxLv = Math.min(Math.floor(Math.random() * score), Object.keys(BLINDBOX_CONFIG).length);
            if (boxLv > 0) {
                boxLv -= 1;
                extra += `，你获得了${Object.keys(BLINDBOX_CONFIG)[boxLv]}\n${this.viewAd()}`;
                this.getBlindbox(boxLv);
            }
        }
        this.pen.currentRoundScore = 0;
        if (!this.pen.destroyed)
            this.pen.destroy();
        this.player.cancelDialogs();
        if (score > this.bestScore) {
            extra += "\n恭喜你创造了新纪录！";
            this.bestScore = score;
        }
        await this.textDialog(
            `比赛结束`,
            `${!game.ended ? `${this.pen.id} 被 ${this.pen.attacker?.id ?? "你"} 弹下了桌面。` : "恭喜你成为了最后的赢家！"}\n${extra}`
        );
        this.player.cameraEntity = this;
        this.pen = null;
        await this.menu();
    };
    entity.chooseCameraView = async function () {
        await this.selectDialog(
            "选择视角",
            "请选择你希望使用的视角",
            Object.keys(CameraViewType)
        );
        if (!this.dialogResult) return;
        this.cameraView = this.dialogResult.value;
    };
    entity.choosePenType = async function () {
        await this.selectDialog(
            "选择文具",
            `请选择你要使用的文具`,
            this.stationery
        );
        if (!this.dialogResult) return;
        this.usePenType = this.dialogResult.value;
    };
    entity.signUpGame = async function () {
        await this.selectDialog(
            "报名参加比赛",
            `请选择你想参加的比赛模式`,
            Object.values(GameModeType)
        );
        if (!this.dialogResult) return;
        const voteValue = this.dialogResult.value;
        while (!this.usePenType) {
            await this.choosePenType();
        }
        while (!this.cameraView) {
            await this.chooseCameraView();
        }
        while (true) {
            await this.selectDialog(
                "报名参加游戏",
                `游戏模式: ${voteValue}\n文具: ${this.usePenType}\n视角: ${this.cameraView}\n开始时将扣除1分数`,
                ["确认报名", "选择文具", "选择视角"]
            );
            if (!this.dialogResult) return;
            switch (this.dialogResult.value) {
                case "确认报名":
                    gameModeVoteList.push(voteValue);
                    this.addTag("joinGame");
                    return;
                case "选择文具":
                    await this.choosePenType();
                    break;
                case "选择视角":
                    await this.chooseCameraView();
                    break;
            }
        }
    }
    entity.stationeryHandbook = async function () {
        while (true) {
            await this.selectDialog(
                `我的文具`,
                `文具收集进度 ${this.stationery.length}/${Object.keys(PEN_CONFIG).length}`,
                this.stationery
            );
            if (!this.dialogResult || typeof this.dialogResult === "string") break;
            const config = PEN_CONFIG[this.dialogResult.value];
            await this.textDialog(
                this.dialogResult.value,
                config.toString()
            );
        }
    };
    entity.openBlindbox = async function () {
        await this.selectDialog(
            "打开盲盒",
            `选择一个盲盒开始打开`,
            this.blindboxes
        );
        if (!this.dialogResult) return;
        const type = this.dialogResult.value;
        const index = this.dialogResult.index;
        const config = BLINDBOX_CONFIG[type];
        this.blindboxOpening.type = type;
        this.blindboxOpening.startTime = Date.now();
        this.blindboxes.splice(index, 1);
    };
    entity.getStationeryFromBlindbox = async function () {
        let content = "";
        const config = BLINDBOX_CONFIG[this.blindboxOpening.type];
        for (let l = 0; l < config.stationeryNum; l++) {
            let p = randomPen();
            if (Math.random() > 0.3) {
                if (this.stationery.includes(p)) {
                    content += `你开出了 ${p} ，但已拥有，转化为1小橡皮。`;
                    this.smallErasers += 1;
                } else {
                    content += `恭喜！你开出了 ${p} 。`;
                    this.stationery.unshift(p);
                }
            } else {
                content += `盲盒的这一格没有任何文具。`;
            }
        }
        const type = this.blindboxOpening.type;
        this.blindboxOpening.type = null;
        await this.textDialog(type, content);
    };
    entity.speedupBlindboxOpening = async function () {
        this.smallErasers -= this.speedupBlindboxPrice;
        this.getStationeryFromBlindbox();
    };
    entity.displayLeaderbroad = async function () {
        while (true) {
            await this.selectDialog("排行榜", "查看排行榜", ["累计分数排行榜", "最高单局分数排行榜"]);
            if (!this.dialogResult) break;
            switch (this.dialogResult.value) {
                case "累计分数排行榜":
                    await this.textDialog("累计分数排行榜", totalScoreRank);
                    break;
                case "最高单局分数排行榜":
                    await this.textDialog("最高单局分数排行榜", bestScoreRank);
                    break;
            }
        }
    };
    entity.moreOptions = async function () {
        while (true) {
            await this.selectDialog(
                "更多",
                void 0,
                ["捐助", "关于地图", "个人数据管理"]
            );
            if (!this.dialogResult) break;
            switch (this.dialogResult.value) {
                case "捐助":
                    this.player.openMarketplace([283435159560112, 0]);
                    break;
                case "个人数据管理":
                    await this.manageData();
                    break;
                case "关于地图":
                    this.player.link("https://dao3.fun/exp/experience/detail/100029019", { isNewTab: true, isConfirm: false });
                    break;
            }
        }
    };
    entity.menu = async function () {
        let currentSeedupBlindboxPrice = 0;
        const exit = this.watchGlobal(this.watchGlobalPos);
        this.position.copy(SPAWN_POS);
        do {
            if (this.hasTag("joinGame")) {
                await this.textDialog(
                    void 0,
                    `你已报名参加比赛，请等待下轮比赛开始。\n${this.viewTip()}`
                );
            } else {
                const opt = ["开始", `文具(${this.stationery.length})`, "帮助", "排行榜", "更多"];
                if (this.hasBlindboxOpening) {
                    if (this.blindboxOpeningCanOpen) {
                        opt.splice(1, 0, "获取盲盒中的文具");
                    } else {
                        currentSeedupBlindboxPrice = this.speedupBlindboxPrice;
                        opt.splice(1, 0, "取消打开盲盒");
                        if (this.smallErasers >= currentSeedupBlindboxPrice) {
                            opt.splice(1, 0, `加速打开盲盒(${currentSeedupBlindboxPrice}小橡皮)`);
                        }
                    }
                } else if (this.blindboxes.length > 0) {
                    opt.splice(1, 0, "打开盲盒");
                }
                await this.selectDialog(
                    void 0,
                    void 0,
                    opt
                );
            }
            if (!this.dialogResult?.value) {
                if (entity.isInGame) break;
                else continue;
            }
            switch (this.dialogResult.value) {
                case "帮助":
                    await this.viewHelp();
                    break;
                case "排行榜":
                    await this.displayLeaderbroad()
                    break;
                case "更多":
                    await this.moreOptions();
                    break;
                case "开始":
                    await this.signUpGame();
                    break;
                case `文具(${this.stationery.length})`:
                    await this.stationeryHandbook();
                    break;
                case "打开盲盒":
                    await this.openBlindbox();
                    break;
                case "获取盲盒中的文具":
                    await this.getStationeryFromBlindbox();
                    break;
                case `加速打开盲盒(${currentSeedupBlindboxPrice}小橡皮)`:
                    await this.speedupBlindboxOpening();
                    break;
                case "取消打开盲盒":
                    this.blindboxes.push(this.blindboxOpening.type);
                    this.blindboxOpening.type = null;
                    break;
            }
        } while (!this.isInGame)
        exit();
    };
}

function createPen(penType, id, position) {
    const config = PEN_CONFIG[penType];
    const pen = world.createPen(config, id, position);
    return pen;
}
/*
async function autoOrientateAllPen() {
    for (const pen of world.querySelectorAll(".pen")) {
        if (!pen.velocity.exactEquals(new GameVector3(0, 0, 0))) {
            pen.meshOrientation.copy(pen.meshOrientation.rotateY(Math.PI / 20 * pen.rotateDirection));
        }
        await sleep(1);
    }
}
*/
function buildCarpet(voxName) {
    for (let x = 0; x < 128; x++) {
        for (let z = 0; z < 128; z++) {
            voxels.setVoxel(x, 0, z, voxName);
        }
    }
}
let onRegisterToken = remoteChannel.onServerEvent(async ({ entity, args }) => {
    if (args.name !== "register") return;
    await sleep(1000);
    await world.setup145player(entity);
    setupPlayer(entity);
    entity.id = entity.player.name;
    if (!entity.player.userId) {
        entity.player.kick();
        return;
    }
    entity.player.spectator = true;
    entity.player.invisible = true;
    entity.player.showName = false;
    const exit = entity.watchGlobal(entity.watchGlobalPos);
    entity.position.copy(SPAWN_POS);
    entity.addTag("playing");
    if (entity.joinTimes === 0) {
        await entity.textDialog(
            "新手引导",
            `欢迎来到 弹笔`,
        );
        do {
            await entity.selectDialog("新手引导",
                "请选择你的初始笔\n你可以通过盲盒获得更多笔",
                Object.entries(PEN_CONFIG).filter(v => v[1].rarity === 0).map(v => v[0])
            );
        } while (!entity.dialogResult);
        entity.stationery.push(entity.dialogResult.value);
    }
    entity.joinTimes += 1;
    exit();
    await entity.menu();
});
let onPlayerLeaveToken = world.onPlayerLeave(async ({ entity }) => {
    if (entity.pen) {
        entity.pen.attacker = entity;
        entity.pen.destroy();
    }
});
let onChatToken = world.onChat(async ({ entity, message }) => {
    //broadcast(`${entity.player.name}: ${message}`);
    switch (message) {
        case "管理个人数据":
            await entity.manageData();
            break;
        case "$":
            if (!ADMIN_LIST.includes(entity.player.name)) return;
            entity.player.cancelDialogs();
            await entity.inputDialog("调试", `欢迎你，管理员 ${entity.player.name}`, void 0, "执行");
            if (!entity.dialogResult) break;
            const code = entity.dialogResult;
            let result;
            try {
                result = eval(code);
            } catch (e) {
                result = e;
            } finally {
                await entity.textDialog("调试", result);
            }
            break;
    }
});
let onEntityContactToken = world.onEntityContact(async ({ entity, other }) => {
    if (!(entity.hasTag("pen") && other.hasTag("pen"))) return;
    entity.attacker = other;
});
let onPressToken = world.onPress(({ entity, button }) => {
    if (button === "action0") {
        if (entity.isInGame && entity.clickCoolDownTimeLeft === 0) {
            entity.action0PressTime = Date.now();
            entity.isCharging = true;
        }
    }
    if (button === "action1") {
        if (entity.isInGame) {
            entity.isCharging = false;
        }
    }
});
let onRealeaseToken = world.onRelease(async ({ entity, button, raycast }) => {
    /*if (button === "action1") {
    }*/
    if (button === "action0") {
        if (entity.isInGame && entity.isCharging) {
            entity.pen.click(entity.player.facingDirection, entity.chargeScale);
            entity.isCharging = false;
        }
    }
});
const gameZone = world.addZone({
    selector: ".pen",
    bounds: {
        lo: new GameVector3(-100, -20, -100),
        hi: new GameVector3(228, 30, 228)
    },
});
let gameZoneOnLeaveToken = gameZone.onLeave(async ({ entity }) => {
    entity.destroy();
});
let onEntityDestroyToken = world.onEntityDestroy(({ entity }) => {
    if (!entity.hasTag("pen")) return;
    if (!game.ended) {
        let extra = "";
        if (gameMode !== GameModeType.SIEGE) {
            if (entity.team && entity.attacker.team) {
                let scoreTeam = null;
                if (entity.attacker.team !== entity.team) {
                    scoreTeam = entity.attacker.team;
                }
                world.querySelectorAll(".pen").filter(p => scoreTeam ? (p.team === scoreTeam) : (p.team !== entity.team)).forEach(e => e.currentRoundScore += 1);
                extra = `${scoreTeam ?? "敌方"}全体+1分`;
            } else {
                const scoreGet = entity.currentRoundScore + 1;
                entity.attacker.currentRoundScore += scoreGet;
                extra = `+${scoreGet}分共${entity.attacker.currentRoundScore}分`;
            }
        }
        broadcast(`${entity.attacker.team ?? ""} ${entity.attacker.id} 击败 ${entity.team ?? ""} ${entity.id} ${extra}`);
    }
    if (!entity.owner || entity.owner.destroyed) return;
    entity.owner.exitGame();
});
let onTickToken = world.onTick(async ({ tick }) => {
    world.querySelectorAll(".uiClient").forEach(entity => {
        entity.uiDiaplay.left = entity.isControllingPen ? `${entity.pen.id}\n本局分数 ${entity.pen.currentRoundScore}` : entity.menuContent;
        entity.uiDiaplay.top = [topContent, ...broadcastContent.slice(0, 2)].join("\n");
        entity.uiDiaplay.bottom = entity.isControllingPen ? (entity.isCharging ? `蓄力 ${entity.chargeScale}×` : `冷却 ${(entity.clickCoolDownTimeLeft / 1000).toFixed(2)}秒`) : "";
    });
});
function createBoss(name) {
    name ??= Object.keys(BOSS_CONFIG)[Math.floor(Object.keys(BOSS_CONFIG).length * Math.random())];
    buildCarpet("red");
    sleep(5000).then(async () => {
        buildCarpet("black");
    });
    const boss = world.createPen(
        BOSS_CONFIG[name],
        `[boss]${name} `,
        randomPos().add(new GameVector3(0, 2, 0)),
        true
    );
    boss.addTag("npc");
    return boss;
}
function createNPC() {
    const penName = randomPen();
    const npc = createPen(penName, `npc 的 ${penName}`, randomPos());
    npc.target = null;
    npc.addTag("npc");
    return npc;
}
async function refreshRank() {
    totalScoreRank = await storage.userDataStorage.getRank("totalScore", "累计分数", 100, false);
    bestScoreRank = await storage.userDataStorage.getRank("bestScore", "最佳单局分数", 100, false);
}
function seigeWave() {
    const spawnNum = MAX_ENEMY_BOT_NUM - world.querySelectorAll(".npc").length;
    if (spawnNum < MAX_ENEMY_BOT_NUM / 2) return;
    seigeCurrentWave += 1;
    topContent = `${gameMode}第${seigeCurrentWave}波`;
    for (let i = 0; i < spawnNum; i++) {
        const npc = i === 0 && Math.random() > 0.5 ? createBoss() : createNPC();
        npc.joinTeam(PenTeamType.RED);
    }
    if (seigeCurrentWave > 1) {
        for (const pen of world.querySelectorAll(".pen")) {
            pen.currentRoundScore += 1;
        }
    }
}
async function startGame() {
    broadcast("新一局比赛即将开始");
    buildCarpet("black");
    world.fogColor = new GameRGBColor(1, 0, 0);
    await sleep(10000);
    if (gameModeVoteList.length === 0) {
        gameMode = GameModeType.FFA;
    } else {
        let gameModeList = Object.values(GameModeType);
        let gameModeVoteResult = gameModeVoteList.reduce(
            (p, v) => {
                p[v] += 1;
                return p;
            },
            gameModeList.reduce(
                (p, v) => {
                    p[v] = 0;
                    return p;
                },
                {}
            )
        );
        gameModeList.sort((a, b) => gameModeVoteResult[b] - gameModeVoteResult[a]);
        gameMode = gameModeList[0];
    }
    gameModeVoteList = [];
    endCountDownStarted = false;
    endCountdownStartSecond = null;
    broadcast(`${gameMode}开始`);
    if (gameMode !== GameModeType.SIEGE) {
        for (let l = 0; l < (MIN_PLAYER_NUM - world.querySelectorAll(".joinGame").length); l++) {
            let npc = await createNPC();
        }
    }
    world.querySelectorAll(".joinGame").forEach(async entity => {
        if (entity.totalScore > 0) entity.totalScore -= 1;
        await entity.joinGame();
        if (gameMode === GameModeType.SIEGE)
            entity.pen.joinTeam(PenTeamType.BLUE);
        entity.removeTag("joinGame");
    });
    await sleep(1000);
    if (gameMode === GameModeType.TDM) {
        world.querySelectorAll(".pen").forEach(e => {
            e.joinRandomTeam();
        });
    }
}
async function endGame() {
    let players = world.querySelectorAll(".pen");
    players.sort((a, b) => {
        return b.currentRoundScore - a.currentRoundScore;
    });
    let extra = "";
    switch (gameMode) {
        case GameModeType.FFA:
            if (players.length == 0) break;
            const mvpScore = players[0].currentRoundScore;
            extra = `MVP ${players[0].id} ${mvpScore}分`;
            if (players[0].owner) {
                players[0].owner.smallErasers += mvpScore;
                extra += ` 获得${mvpScore}小橡皮`;
            }
            break;
        case GameModeType.SIEGE:
            extra = `最终波数:${seigeCurrentWave}`;
            break;
    }
    topContent = `${gameMode}结束 ${extra}`;
    buildCarpet("white");
    world.fogColor = new GameRGBColor(1, 1, 1);
    refreshRank();
    players.forEach(p => p.destroy());
    if (gameMode === GameModeType.SIEGE) {
        seigeCurrentWave = 0;
    }
}
function canEndGame(second) {
    return (
        world.querySelectorAll(".pen").length < 2
        ||
        world.querySelectorAll(".pen").map(v => v.team).every((v, i, a) => v && v === a[0])
        ||
        (endCountDownStarted && second - endCountdownStartSecond >= END_COUNDDOWN_TIME && gameMode !== GameModeType.SIEGE)
    );
}
const game = world.createMatch(
    startGame,
    async (second) => {
        if (gameMode !== GameModeType.SIEGE) {
            const pens = world.querySelectorAll(".pen");
            if (pens.length < 3) {
                if (!endCountDownStarted) {
                    endCountDownStarted = true;
                    endCountdownStartSecond = second;
                }
                topContent = `${gameMode}决赛剩余${END_COUNDDOWN_TIME - (second - endCountdownStartSecond)}秒`;
            } else {
                topContent = `${gameMode}剩余${pens.length}选手`;
            }
        }
        if (gameMode === GameModeType.FFA && second === 20) {
            const boss = createBoss();
            broadcast(`${boss.id} 出现`);
        }
        if (gameMode === GameModeType.SIEGE) {
            seigeWave();
        }
        if (second % 3 === 0) {
            const a = Math.floor(3000 / world.querySelectorAll(".npc").length);
            if (second > 0) {
                for (const npc of world.querySelectorAll(".npc")) {
                    await npc.autoClick();
                    await sleep(a);
                }
            }
        }
    },
    canEndGame,
    endGame
);
async function main() {
    buildCarpet("black");
    world.fogColor = new GameRGBColor(0, 0, 0);
    while (true) {
        await sleep(5000);
        await game.play();
        await sleep(5000);
    }
}
main();
//请勿删除最后一行
```
### pen.js
```javascript
/*
*/
const PenTeamType = {
    RED: "红队",
    BLUE: "蓝队"
};
const PenColor = {
    RED: new GameRGBAColor(1, 0.1, 0.1, 1),
    BLUE: new GameRGBAColor(0.1, 0.1, 1, 1)
};
const PenRarityType = ["普通", "稀有", "罕见", "史诗", "传奇"];
class PenConfigData {
    constructor(description, mass, friction, scale, rarity, scaleY = 1) {
        this.description = description;
        this.mass = mass;
        this.friction = friction;
        this.scale = scale;
        this.rarity = rarity;
        this.scaleY = scaleY;
        this.mesh = null;
    }
    toEnhanced(scaleConfig) {
        const result = new PenConfigData(this.description, this.mass, this.friction, this.scale, this.rarity + 1, this.scaleY);
        Object.keys(scaleConfig).forEach((k) => {
            result[k] = result[k] * scaleConfig[k];
        });
        result.mesh = this.mesh;
        return result;
    }
    toString() {
        return `“${this.description}”\n重量: ${this.mass}\n摩擦力: ${this.friction}\n稀有度: ${PenRarityType[this.rarity]} `
    }
}
world.createPen = function (config, id, position, isboss = false) {
    let pen = world.createEntity({
        id: id,
        mesh: config.mesh,
        meshScale: new GameVector3(config.scale, config.scale * config.scaleY, config.scale),
        meshOrientation: new GameQuaternion(0, 0, 0, 1).rotateY(Math.random() * Math.PI * 2),
        meshEmissive: 1,
        position: position,
        mass: config.mass,
        friction: config.friction,
        collides: true,
        restitution: 1
    });
    pen.addTag("pen");
    pen.showId = true;
    //pen.interactHint = pen.id;
    pen.customName = pen.id;
    pen.target = null;
    //pen.interactRadius = 300;
    //pen.interactColor = new GameRGBColor(0.3, 0.9, 1);
    //pen.enableInteract = true;
    pen.showEntityName = true;
    pen.nameRadius = 300;
    pen.target = null;
    pen.currentRoundScore = 0;
    pen.lastClickTime = 0;
    pen.team = null;
    pen.attacker = {
        id: pen.id,
        team: null,
        currentRoundScore: 0
    };
    if (isboss) {
        pen.addTag("boss");
    }
    pen.joinTeam = function (teamName) {
        this.team = this.attacker.team = teamName;
        switch (teamName) {
            case PenTeamType.RED:
                this.meshColor.copy(PenColor.RED);
                break;
            case PenTeamType.BLUE:
                this.meshColor.copy(PenColor.BLUE);
                break;
        }
    }
    pen.joinRandomTeam = function () {
        const redNum = world.querySelectorAll(".pen").filter(e => e.team === PenTeamType.RED).length;
        const blueNum = world.querySelectorAll(".pen").filter(e => e.team === PenTeamType.BLUE).length;
        if (redNum > blueNum) {
            this.joinTeam(PenTeamType.BLUE);
        }
        if (blueNum > redNum) {
            this.joinTeam(PenTeamType.RED);
        }
        if (blueNum === redNum) {
            this.joinTeam(Math.random() > 0.5 ? PenTeamType.RED : PenTeamType.BLUE);
        }
    }
    pen.click = function (direction, force = 3/*, rotateDirection = Math.round(Math.random() + 0.5) * (Math.random() > 0.5 ? 1 : -1)*/) {
        this.lastClickTime = Date.now();
        direction.y = 0;
        this.velocity.addEq(direction.scale(1 / direction.mag()).scale(force));
        //this.rotateDirection = rotateDirection;
    };
    pen.autoClick = async function () {
        if (!this.target || this.target.destroyed || this.target.position.distance(this.position) > 50) {
            let players = world.querySelectorAll(".pen").filter(p => p !== this && (!p.team || p.team !== this.team));
            this.target = players.sort((a, b) => {
                return a.position.distance(this.position) - b.position.distance(this.position)
            })[0];
            if (!this.target) return;
        }
        let direction;
        if (this.position.x > 122 || this.position.x < 5 || this.position.z > 115 || this.position.z < 12) {
            direction = new GameVector3(64, this.position.y, 64).sub(this.position);
        } else {
            direction = this.target.position.sub(this.position);
        }
        await this.click(direction, Math.ceil(Math.random() * 3 + 1));
    };

    return pen;
}
module.exports = { PenTeamType, PenRarityType, PenConfigData };
//请勿删除最后一行
```
### 145player.js
```javascript
/** 
 * !Info {Module} -来自145a
 * 145player 4.0
 * 145player是145lab的一部分
 */
"use strict";
const { DEFAULT_USER_DATA, TIPS, ADS } = require("./145playerConfig.js");
require("./145storage.js");
/*config*/
const HELP = TIPS.join("\n");
/*storage*/
storage.userDataStorage = storage.get145DataStorage("main", DEFAULT_USER_DATA);
/*setup*/
world.setup145player = async function (entity) {
    /*dialog*/
    entity.dialogResult = null;
    entity.basicDialog = async function (params) {
        Object.assign(params, {
            titleTextColor: new GameRGBAColor(1, 1, 1, 1),
            titleBackgroundColor: new GameRGBAColor(0, 0, 0, 0.2),
            contentBackgroundColor: new GameRGBAColor(0, 0, 0, 0.2)
        });
        return this.dialogResult = await this.player.dialog(params);//await gui.dialog(this, params.title, params.content, params.options, gui.DialogPositionType.FULL_SCREEN);
    };
    entity.textDialog = async function (title, content) {
        return await this.basicDialog({
            type: "text",
            title: title,
            content: content
        });
    };
    entity.selectDialog = async function (title, content, options) {
        return await this.basicDialog({
            type: "select",
            title: title,
            content: content,
            options: options
        });
    };
    entity.inputDialog = async function (title, content, placeholder, confirmText) {
        return this.dialogResult = await this.player.dialog({
            type: "input",
            title: title,
            content: content,
            placeholder: placeholder,
            console: confirmText
        });
    };
    entity.cancelDialog = async function () {
        this.player.cancelDialogs();
    };
    /*debug*/
    entity.debugBridgeRun = function (input) {
        let output;
        try {
            output = eval(input);
        } catch (e) {
            output = e;
        }
        return output
    };
    entity.debugBridgeConsole = async function () {
        while (true) {
            await this.inputDialog("145lab", "145lab Debug Bridge", "命令", "执行");
            if (!this.dialogResult) break;
            await this.textDialog("145lab", this.debugBridgeRun(this.dialogResult));
        }
    };
    /*tips*/
    entity.viewTip = function () {
        return "Tips：" + TIPS[Math.floor(Math.random() * TIPS.length)];
    };
    /*ad*/
    entity.viewAd = function () {
        return `[广告]${ADS[Math.floor(Math.random() * ADS.length)]}`;
    };
    /*help*/
    entity.viewHelp = async function () {
        await this.textDialog("帮助", HELP);
    };
    /*camera*/
    GamePlayer.prototype.enable
    entity.watchGlobal = function (cameraPos) {
        const previousMode = this.player.cameraMode;
        const previousPosition = this.player.cameraPosition.clone();
        const previousTarget = this.player.cameraTarget.clone();
        const previousUp = this.player.cameraUp.clone();
        const previousDisableInputDirection = this.player.disableInputDirection;
        const previousEnableAction0 = this.player.enableAction0;
        const previousEnableAction1 = this.player.enableAction1;
        this.player.cameraMode = "fixed";
        this.player.cameraPosition.copy(cameraPos);
        this.player.cameraTarget.copy(cameraPos.sub(new GameVector3(0, 100, 0)));
        this.player.cameraUp.set(1, 0, 0);
        this.player.disableInputDirection = GameInputDirection.BOTH;
        this.player.enableAction0 = false;
        this.player.enableAction1 = false;
        return () => {
            this.player.cameraMode = previousMode;
            this.player.cameraTarget.copy(previousTarget);
            this.player.cameraPosition.copy(previousPosition);
            this.player.cameraUp.copy(previousUp);
            this.player.disableInputDirection = previousDisableInputDirection;
            this.player.enableAction0 = previousEnableAction0;
            this.player.enableAction1 = previousEnableAction1;
        };
    };
    /*items*/
    Object.defineProperties(entity, {
        displayItems: {
            enumerable: true,
            get() {
                return Object.entries(entity.items).map(([k, v]) => `${k} * ${v}`);
            }
        },
        totalItemsNum: {
            enumerable: true,
            get() {
                return Object.values(entity.items).reduce((p, v) => p + v, 0);
            }
        }
    });
    entity.addItem = function (name, num = 1) {
        if (entity.items[name]) {
            entity.items[name] += num;
        } else {
            entity.items[name] = num;
        }
        if (entity.items[name] < 1) {
            delete entity.items[name];
        }
    };
    /*storage*/
    entity.manageData = async function () {
        await this.selectDialog("管理145lab储存的个人数据", `userId:${this.player.userId}\n已储存的数据:${JSON.stringify((await storage.userDataStorage.get(this.player.userId)).value)}`, ["删除个人数据"]);
        switch (this.dialogResult?.value) {
            case "删除个人数据":
                await this.selectDialog("删除个人数据", "是否要删除您的个人数据？此操作不可逆", ["删除个人数据"]);
                if (!this.dialogResult) break;
                entity.player.kick();
                storage.userDataStorage.remove(entity.player.userId);
                break;
        }
    };
    await storage.userDataStorage.setupUser(entity);
};
//请勿删除最后一行
```
### 145playerConfig.js
```javascript
//config
const DEFAULT_USER_DATA = {
    joinTimes: 0,//默认进入次数统计
    items: {},//默认背包
    stationery: [],
    totalScore: 0,
    smallErasers: 0,
    blindboxes: [],
    blindboxOpening: {
        type: null,
        startTime: 0
    },
    bestScore: 0,
    cameraView: "",
    usePenType: ""
};
const TIPS = [
    "欢迎来到 弹笔",
    "在 dao3.fun 搜索“弹笔”可以快速找到这张地图",
    "掉下平台边缘淘汰",
    "使用手机等较小屏幕的设备时，建议横屏并全屏",
    "电脑建议选择第三人称视角",
    "使用第三人称视角时，调整面对方向确定方向",
    "移动端推荐横屏并选择俯视视角",
    "使用俯视视角时，左下角摇杆(WASD)确定方向",
    "长按A键(鼠标左键)蓄力，B键(鼠标右键)取消蓄力",
    "比赛结束时概率获得盲盒，得分越高概率越大",
    "开启盲盒可以解锁更多文具",
    "如果你有疑问，请将你的问题写在地图评论区"
];
const ADS = [
    "把繁琐交给145lab，专注于地图本身",
    "在dao3.fun搜索“静谧之森”"
];
module.exports = { DEFAULT_USER_DATA, TIPS, ADS };
//请勿删除最后一行
```
### 145storage.js
```javascript
/**
 * !Info {Module} -来自145a
 * 145storage 4.0
 * 145storage是145lab的一部分
 */
/**
 * 缓冲时间
 * @type {number}
 */
const REQUEST_MIN_INTERVAL = 1000;
class DeepProxy {
    /**
     * @param {object} target
     * @param {object} handler
     */
    constructor(target, handler) {
        const deepHandler = Object.assign({}, handler);
        deepHandler.get = (target, property) => {
            const value = Reflect.get(target, property);
            if (typeof (value) === "object" && value !== null) {
                return new DeepProxy(value, handler);
            } else {
                if (handler.get) {
                    return handler.get(target, property);
                } else {
                    return value;
                }
            }
        };
        return new Proxy(target, deepHandler);
    };
}
/**
 * @param {object} host
 * @param {string} key
 * @param {any} defaultValue
 * @param {function(JSONValue)} updater
 */
storage.setupCloudVariable = async function (host, key, defaultValue, updater) {
    const cacheKey = `_${key}_cache_`;
    const objectCacheKey = `_${key}_object_cache_`;
    const isWaitingKey = `_${key}_isWaiting_`;
    const scheduleUpdateKey = `_${key}_scheduleUpdate_`;
    host[cacheKey] = typeof defaultValue === "object"?Object.assign({},defaultValue):defaultValue;
    host[isWaitingKey] = false;
    host[scheduleUpdateKey] = async function () {
        if (host[isWaitingKey]) return;
        host[isWaitingKey] = true;
        await sleep(REQUEST_MIN_INTERVAL);
        host[isWaitingKey] = false;
        updater(host[cacheKey]);
    }
    Object.defineProperty(host, key, {
        get() {
            return host[cacheKey];
        },
        set(value) {
            host[cacheKey] = value;
            host[scheduleUpdateKey]();
            return true;
        }
    });
    if (typeof defaultValue === "object" && defaultValue !== null) {
        host[objectCacheKey] = defaultValue;
        host[cacheKey] = new DeepProxy(host[objectCacheKey], {
            set(target, property, value) {
                Reflect.set(target, property, value);
                host[scheduleUpdateKey]();
                return true;
            }
        });
    }
}
/**
 * @param {String} name
 * @param {JSONValue} defaultUserData 用户默认属性和数据类型，其中name自带
 * @returns {GameDataStorage}
 */
storage.get145DataStorage = function (name, defaultUserData) {
    let host = storage.getDataStorage(name);
    Object.assign(defaultUserData, {
        name: "游客"
    });
    /**
     * @param {GamePlayerEntity} user
     */
    host.setupUser = async function (user) {
        if (!user || !user.isPlayer) throw `setupUser的参数不对`;
        if (!user.player.userId) return;
        let dataStorage = this;
        const data = await dataStorage.get(user.player.userId);
        if (!data) {
            await dataStorage.set(user.player.userId, defaultUserData);
            return await dataStorage.setupUser(user);
        }
        user._isPreparingUpdate_ = false;
        user._storageUpdateCache_ = {};
        Object.keys(defaultUserData).forEach(key => {
            if (data.value[key] === null || typeof data.value[key] !== typeof defaultUserData[key]) {
                data.value[key] = defaultUserData[key];
            }
            user._storageUpdateCache_[key] = data.value[key];
            storage.setupCloudVariable(user, key, data.value[key], async (value) => {
                user._storageUpdateCache_[key] = value;
                if (user._isPreparingUpdate_) return;
                user._isPreparingUpdate_ = true;
                await sleep(REQUEST_MIN_INTERVAL);
                dataStorage.set(user.player.userId, user._storageUpdateCache_);
                user._isPreparingUpdate_ = false;
            });
        });
        user.name = user.player.name;
    }
    /**
     * @param {string} name
     * @param {string} displayName
     * @param {number} num
     * @param {boolean} ascending
     * @returns {string}
     */
    host.getRank = async function (name, displayName, num = 100, ascending) {
        const data = (await this.list({
            cursor: 0,
            pageSize: num,
            constraintTarget: name,
            ascending: ascending
        })).getCurrentPage().map(v => ({
            key: v.key,
            value: v.value
        }));
        let result = `用户名 ${displayName}\n` + data.map((v) => `${v.value.name} ${v.value[name]}`).join("\n");
        return result;
    }
    return host;
}
//请勿删除最后一行
```
### 145match.js
```javascript
/**
 * !Info {Module} -来自145a
 * 145match 1.0
 * 145match是145lab的一部分
 */
"use strict";
class Match {
    /**
     * @param {function} onStart
     * @param {function(number)} onSecond
     * @param {function():boolean} canEnd
     * @param {function} onEnd
     */
    constructor(onStart, onSecond, canEnd, onEnd) {
        this.ended = null;
        this.timeSecond = 0;
        this.onStart = onStart;
        this.onSecond = onSecond;
        this.canEnd = canEnd;
        this.onEnd = onEnd;
    }
    async play(...params) {
        this.ended = false;
        await this.onStart(...params);
        this.timeSecond = 0
        do {
            this.timeSecond += 1;
            this.onSecond(this.timeSecond);
            await sleep(999);
        } while (!this.canEnd(this.timeSecond))
        this.ended = true;
        await this.onEnd(this.timeSecond);
        this.timeSecond = 0;
    }
}
world.createMatch = function (...params) {
    return new Match(...params);
}
//请勿删除最后一行
```
### ui.js
```javascript
/**
 * !Info {Module} -来自145a
 * ui模板 0.5
 * ui模板是145lab的一部分
 * ui.js
 */
let onRegisterToken = remoteChannel.onServerEvent(async ({ entity, args }) => {
    switch (args.name) {
        case "register":
            entity.uiDiaplayCache = {};
            Object.assign(entity, args.data);
            entity.screenAspectRatio = entity.screenHeight / entity.screenWidth;
            entity.uiDiaplay = new Proxy(entity.uiDiaplayCache, {
                set(target, property, value) {
                    if (Reflect.get(target, property) !== value) {
                        let data = {};
                        Reflect.set(data, property, value);
                        Reflect.set(target, property, value);
                        remoteChannel.sendClientEvent(entity, {
                            name: "display",
                            data: data
                        });
                    }
                    return true;
                }
            });
            entity.addTag("uiClient");
            break;
            case "resize":
                        Object.assign(entity, args.data);
                        entity.screenAspectRatio = entity.screenHeight / entity.screenWidth;
            break;
    }
});
//请勿删除最后一行
```
## client
## clientIndex.js
```javascript
/**
 * !Info {Project} -来自145a
 * ui模板 0.5
 * ui模板是145lab的一部分
 * clientIndex.js
 */
console.clear();

let DEFAULT_TOP_DISPLAY_CONTENT = "正在连接服务器……"
let getBasicFontSize = () => Math.max(15, Math.floor(screenWidth / 60));
let basicFontSize = getBasicFontSize();

function setupTextColor(node) {
    node.textColor.copy({ r: 255, g: 255, b: 255 });
    node.backgroundColor.copy({ r: 0, g: 0, b: 0 });
    node.backgroundOpacity = 0.2;
}

const permanent = UiScreen.create();
/*permanent.position.offset.copy({x:0,y:0});
permanent.size.offset.copy({x:0,y:0});
permanent.parent = UiScreen.create();*/

const leftDisplay = UiText.create();
leftDisplay.name = "left";
leftDisplay.autoResize = "XY";
leftDisplay.textXAlignment = "Left";
leftDisplay.textYAlignment = "Center";
setupTextColor(leftDisplay);
leftDisplay.textContent = "";
leftDisplay.parent = permanent;

const topDisplay = UiText.create();
topDisplay.name = "top";
topDisplay.anchor.x = 0.5;
topDisplay.autoResize = "XY";
topDisplay.textXAlignment = "Center";
topDisplay.textYAlignment = "Bottom";
setupTextColor(topDisplay);
topDisplay.textContent = DEFAULT_TOP_DISPLAY_CONTENT;
topDisplay.parent = permanent

const bottomDisplay = UiText.create();
bottomDisplay.name = "bottom";
bottomDisplay.anchor.copy({ x: 0.5, y: 1 });
bottomDisplay.autoResize = "XY";
bottomDisplay.textXAlignment = "Center";
bottomDisplay.textYAlignment = "Bottom";
setupTextColor(bottomDisplay);
bottomDisplay.textContent = "";
bottomDisplay.parent = permanent;
function resize() {
    basicFontSize = getBasicFontSize();

    leftDisplay.position.offset.copy({ x: screenWidth / 100, y: 16 });
    leftDisplay.size.offset.copy({ x: 0, y: 0 });

    topDisplay.position.offset.copy({ x: screenWidth / 2, y: screenHeight / 20 });
    topDisplay.size.offset.copy({ x: screenWidth / 3, y: 0 });

    bottomDisplay.position.offset.copy({ x: screenWidth / 2, y: screenHeight - screenHeight / 20 });
    bottomDisplay.size.offset.copy({ x: 0, y: 0 });
    leftDisplay.textFontSize = basicFontSize;
    topDisplay.textFontSize = basicFontSize;
    bottomDisplay.textFontSize = basicFontSize;

}
sleep(20000).then(() => {
    if (topDisplay.textContent !== DEFAULT_TOP_DISPLAY_CONTENT) return;
    topDisplay.textContent = "服务器连接超时，请重试";
});

input.uiEvents.on("pointerup", (args) => {
    if (args?.target?.name) {
        remoteChannel.sendServerEvent({
            name: "click",
            data: args.target.name
        });
    }
});
remoteChannel.events.on("client", (args) => {
    switch (args.name) {
        case "display":
            for (const name of Object.keys(args.data)) {
                permanent.findChildByName(name).textContent = args.data[name];
            }
            break;
    }
});
remoteChannel.sendServerEvent({
    name: "register",
    data: {
        screenHeight: screenHeight,
        screenWidth: screenWidth
    }
});
screen.events.add("resize", ({ screenWidth, screenHeight }) => {
    resize();
    remoteChannel.sendServerEvent({
        name: "resize",
        data: {
            screenHeight: screenHeight,
            screenWidth: screenWidth
        }
    });
});
resize();
//请勿删除最后一行
```