## HandsFree 故事和酒

> 2017.4.15 记

&emsp;&emsp;今天就是想和大家聊聊HandsFree。

&emsp;&emsp;[HandsFree](https://hands-free.github.io/)是一个开源的移动机器人开发平台，后来学长们把它做成了社区。

&emsp;&emsp;它怎么来的呢？

&emsp;&emsp;两年前，学校舞蹈机器人基地有个电子组学长，在基地电子组干了得有两年多，几乎把基地各个项目电子组的活儿都摸了个遍。有天他敲代码连续敲了有13个小时，突然发现自己的手累的都没办法抬起来了。

&emsp;&emsp;这学长懒啊，然后他就想，我特么一个电子组的整天在这儿这么苦逼的敲代码,不行啊,以后我要解放双手，去搞上层啊。以后一定要造一套轮子，不管要做啥机器人，都不用重新写一遍代码，不用重新调PID，自己就再也不用干这些底层的重复性民工活儿了,一定要实现HandsFree，那该多好。嗯，这还是一个伟大的梦想，一定会实现的。然后学长就坐那耷拉着手开始嘿嘿嘿笑起来了。。。。

&emsp;&emsp;没想到的是，他这么懒的一个人有了这样一个念头之后，真的就忘不了了。。。他想搞机器人啊，他真的觉得自己以后很有可能就天天搞机器人了，既然这样，他就一定要造一套好轮子，能够实现HandsFree，让自己专心做有前途的上层。于是，就在大三快放暑假的时候，在他刚刚感到有大把时间可以供自己自由分配的时候，他终于按捺不住了，开始没日没夜的写HandsFree，他就开始朝着自己那个能让自己嘿嘿嘿笑的梦想开始努力了。

&emsp;&emsp;其实这学长的学分积已经非常可怜了，80%，在基地厮混了这么久，哪里有时间想着照顾学分积呢。但他依然在那个时候，在准备考研的时候，疯狂的敲了一个暑假。开学之后，他本来准备忍痛放下HandsFree,复习考研。但没想到，那一年政策变化，80%的他居然也成功保研。。。听到这消息他立马就把考研书扔一边儿，屁颠儿屁颠儿又跑过去整HandsFree了。

&emsp;&emsp;第一版写完之后,学长非常开心的把HandsFree的嵌入式库分享给老学长,老学长看完之后说这玩意儿不错啊，我们还能用呢。他又很开心的分享给狗哥他们，狗哥他们也说好。后来就说，这么好的玩意儿咱别自己用了，咱整开源吧。起个好名字，就叫OpenRE（Open Robot Embedded）。然后狗哥刚好还和Exbot的管理员关系不错,易科就说你们这玩意儿也挺不错的,我们帮你们推广下吧。一推广就火了，大家建了个群，第二天就200人了。

&emsp;&emsp;后来啊，要不怎么说兄弟情深，要不怎么说情怀啊。基地他们那一届，A叔，狗哥，陈映冰学长，汪志康学长，邵琪杰学长都在呢，说你干吧，好不容易咱基地也整个开源项目，我们都帮你。从基地退役之后，没了经费，他们搞机器人也要生存啊，那就卖机器人吧，就卖HandsFree机器人。

&emsp;&emsp;以上这些,就是我对HandsFree历史的一些粗浅印象,可能有失实和夸张的部分。

&emsp;&emsp;问过学长之后,他给了我当时的一篇日记(2016.1.3)原文如下:

>*&emsp;&emsp;四个月前，我决定慢慢脱离底层，但是在这之前，我要把之前搞过的东西总结成一个库，方便以后再次使用时不需要再次研究底层的东西，并且这个库要具备强大的可移植性，可扩展性，完备精简，方便快捷，我大概花了一周的时间搭好一个基本框架，并使用ROS Package 和 Node的概念，以便于扩展各种功能包，并把所有MCU相关的代码有条理的封装成一个和MCU同名的文件夹，使用C++方式来封装每个功能包，同时把操作系统组件封装到一个文件夹，这样，即使一个不懂嵌入式的人，也可以很轻松的用这个库来开发。*

>*&emsp;&emsp;然而做到这一步，并没有我一开始想的那么轻松，我花了1个半月的时间，改了好几版，才写好一个仅仅支持STM32F1的库，这一个半月，让我痛苦不堪，每天一醒来就在写，写到着整层楼的人都睡了，天天如此，我当时唯一的念头就是，一旦写好，我就可以HANDS FREE了，并且全部开源的念头也是在这种情景上诞生的，我希望别人不要在干这种浪费生命的活，我把这第一个版本命名HANDS-FREE-V1.0发布在基地里，希望有人和我一起搞。*

>*&emsp;&emsp;可是现实并不美好，除了获得几个赞外，啥都没有，关键时刻还得靠基友啊，于是我去找陈映冰，把我的想法告诉他，正好那个时候，他在搞移动平台，并且正在着死画板子，敲着死代码，可以说是和我之前的情景一样，于是我们一拍即和，两个人精心配合一直到现在，在合作的两个月里，我们一起制定了HANDS-FREE-PCB的协议和统一的lib，一起完善制定开展了模块化PCB思想，一起精心设计ALL FOR ONE的主控的一代，二代，三代，他还设计了HANDS-FREE的电机驱动，并且一起完善了HANDS-FREE嵌入式框架在STM32 F4平台上的支持性，那段时间，我们基本天天通过语音来合作，也有好几次想要放弃，更要命的是，我们各自不满对方的想法，直接在QQ上开始撕逼大战，不过还好他脾气好，不然HANDS-FREE就夭折了，我和他也基本完成了硬件和嵌入式的框架，总而言之，没有他，我早就放弃了，他是我在HANDS-FREE项目中最给力的助攻。*

>*&emsp;&emsp;也是在和陈映冰搞了一个月后，我想到我毕设需要3个移动平台，于是我找到汪志康帮我设计机械部分，我的毕设和廖新一一起做，做了HANDS-FREE这么久，移动平台自然是要在HANDS-FREE的基础上完成的，于是建立机械标准的想法自然就诞生了，于是HandsFree就变成了一个以嵌入式框架为核心，机械，硬件为分之的平台了，汪志康很给力，虽然他不太懂硬件和嵌入式，不过他却很支持HANDS-FREE的理念，他定义HANDS-FREE机械标准和设计了,HANDS-FREE-Robot-3WD V1.0,也是他让我想到这个硬件平台是可以为更多人服务的。*

>*&emsp;&emsp;发布HANDS-FREE1.0后，我就把阵营搬到毕设教研室，也就是说后面的进程，我都是在教研室搞的，毕设是ROS,在这段时间里，我做了一个决策，让HANDS-FREE以ROS机器人开发的开源平台的形式推广出去，机器人越来越火，需要以机器人开发平台的人也越来越多，而国内基本没有一个好的开源平台，HANDS-FREE已经封装了机械，硬件，和嵌入式，而且廖新一在EXBOT上的影响力不小，所以我们具备了很多可以推广的条件，于是我开始规划HANDS-FREE的推广计划。*

>*&emsp;&emsp;后面的发展和一开始规划的差不多，我们和EXBOT达成了合作关系，只不过让我没想到的是，EXBOT先来找我，而不是我去找他，我更坚定了这个平台的需求，我们约定，1个月也就是2月1号之前，在EXBOT官网上推出HANDS-FREE-Robot-3WD，他们负责ROS教程编写和宣传HANDS-FREE，接着我说服了我的毕设导师，和教研室达成了合作，于是我们有了资金和后续技术支持，教研室负责视觉SLAM和机器学习的软硬件开发，接着找到邵琪杰，于是HANDS-FREE-Robot-人形也就加入进来了，后来在基地发布了HANDS-FREE-Robot-1.5，吸引了一些学长以及他们的创业团队和基地小伙伴们，HANDS-FREE的维护成员于是开始增长，我相信，随着越来越多的人加入进来，HANDS-FREE的目标很快就会实现。*
>


&emsp;&emsp;后来HandsFree团队内的人聚聚散散，车也是有空了造几台卖一把。16年上半年干的比较起劲，暑假还去了好多学校和公司讲了讲HandsFree。但是下半年研究生就开学了，大家都有课，都有一堆新的人在等着自己认识。发展速度就慢慢慢了下来。但是因为社区早已经建起来了，当时在我们这批还在基地服役的队员里面。。。HandsFree的名声还是神秘而装逼的。。。。

&emsp;&emsp;去年冬天的时候，学长跑到基地来拉皮条了。自己一个人带着个PPT。我就舔着脸认识了学长。我们一些人也就趁着比赛帮学长推广项目的名义加进了HandsFree。

&emsp;&emsp;大学，是每个人的青春。不甘寂寞的人总是会寻找各式各样的出路，来度过漫长四年。或者是学生会、社团，运动会，又或者是加基地，进实验室。我们把自己最黄金的两年多时间投入到里面，以至于很多年后回想大学生涯，这依然会是我们的谈资。有些人，很难能可贵的，就会在这个过程中找到自己想要的东西。

&emsp;&emsp;学长，就是这样的一个人。基地，就是这样的一个组织。我们在这里发现对机器人的热爱，很多人就从这里开始走上了一条以前从未想象过的道路。

&emsp;&emsp;至于我，现在正大三，过年前本来想的是这学期要放弃一切竞赛，准备安心学习复习的。本来参加比赛的时候想的就是帮学长打个宣传，宣传完也就没事了。。。但没想到真的越陷越深了。。。

&emsp;&emsp;一开始是在和学长有过一次快四个小时的长谈之后，真的是被他这种对机器人的热爱和开源精神打动了，我发现我们两个在很多理念上非常契合。开源精神，听起来像做公益，像做慈善。但是谁让我真的有这方面的愿望呢。一路走来，很多地方都曾受人恩惠，被人提携。我们每个人其实都是在社会成长，利用社会的资源，也要尽可能的回报社会。曾想着是等自己有大把大把的钱了，再回报社会。但随着自己在“马克思主义道路”（一本正经脸）上感触越来越深，思考的就慢慢的变了。何必非等到以后呢？所行就是所想，所做就是为人。真想回报社会，就不会找借口等到以后。你就从现在做起，从能摸得到的身边人做起，帮助他们，这就是回报社会。

&emsp;&emsp;更何况，HandsFree里面还寄托着一群人对机器人的梦想。想一想我们在搞的机器人，中国现在做智能机器人的核心青年力量，都是曾参加过中国机器人大赛，RoboCup的一批人。然而近几年随着一批顶尖高校的退水（转向国际赛放弃国内赛），和比赛本身生命周期的发展，真正甩着膀子在这个比赛上往前冲的人越来越少了。仔细想想，中国现在到底有多少机器人人才储备军啊？985高校的学生可能在本科生阶段会比较单纯的参与进去，但是到了大四或者研究生，被实验室的项目牵着走，转而追求一些其他的东西了。再加上有些实验室的保密氛围或者封闭性，除了发论文卖产品之外，能为这个社会机器人事业的发展贡献的力量就更少了。可是你看啊，中国未来对机器人的需求是多么巨大。现在行业对机器人人才的渴望是多么强烈。原先互联网时代那群人是多么希望跟上时代步伐也来开发机器人。现在的国内虽然有易科这样的机器人社区，但是对很多想入手机器人的人来说，还是缺少一个开放友好的机器人开发平台啊。

&emsp;&emsp;还有时代在发展,技术在迅速的进步。每一年顶会上发的论文趋势都在变化。你拼了命的学习，看代码，还不一定赶得上熟悉前沿技术，更别说投入那么长的时间调机器人了。

&emsp;&emsp;机械、电子、软件都在发展，仅就基地而言，软件组从三年前开始引入ROS,去年开始上深度学习FasterRcnn,三年前出去的人现在回来看都不一定跟的上了。有人说，你就一个本科生，比赛需求还那么低，搞那么多牛逼的东西干啥？基础的东西你都学完了吗？时代在发展啊，大兄弟。几百年前人们花几十年时间学习牛顿定律，但是当他发展成熟之后，今天我们一本初中课本就能让你学完最核心的知识。生产力发展的需求在推着时代往前走，不断的弃旧扬新。不断的压缩远离时代的知识的学习时间，把时间挤出来发展新技术，新应用，提高生产力。一代人有一代人的使命，上一代人搞好的东西，交到你手里，你就可以直接用，是让你来发展新东西的。07年别人拿PCA做个人脸识别，还是个挺新的玩意儿，今年你还拿他来做创新实践，得了吧，半天实验熟悉一遍就做完了。你要是时间充裕还行，别人已经造出来的东西，你就跑过去复现一遍，体会创造思想，但也仅此打住。不要再浪费时间了。时间是多么宝贵啊，你花时间学习旧的，是为了发展新的啊。这么多东西等着你学，你还守在过去的一个炕里面站不起来啊。

&emsp;&emsp;很多人说害怕未来人工智能机器人时代到来他们失业,但其实对我们这群搞机器人的人来说,这恰恰就是我们的事业啊,未来几十年内，这么好的机会就再等着我们呢。HandsFree把整个的嵌入式软硬件开发环境都移植到了Linux上，OpenRE还把一系列机器人开发过程中的嵌入式代码进行了封装，出于实际机器人开发经验的需要，丰富了很多接口（包括电源。通信，调试这些），而且实现了全开源。后来我们把它总结成叫：分布式架构设计、硬件资源预留以及软件开放性优化。她极大的方便了这群搞ROS的人根据任务需要进行底层DIY，以及一群以前玩儿电子的人进入ROS。她这么一套东西，是真的能省去大量的开发时间的，以前开发个机器人准备比赛可能需要六七个人从头花七八个月的时间，但是用HandsFree之后，可能三四个人三四个月就能整个差不多了。

&emsp;&emsp;也就是说，她这个东西是真的能推动一批人进入到机器人学习中来，推动开源机器人事业的发展，为社会带来贡献的。西工大好不容易能出来这么一个被社会评价很好的开源社区，为什么不扶一把呢，这也算是西工大学生的社会担当，西工大在机器人开源社区对社会的贡献。公为天下，即从今日始。报效祖国，就从手边干啊。这么说，可能有点太伟光正，但是为什么就不能伟光正一点，把我们的初衷表达出来呢？

&emsp;&emsp;想通了这一点之后，我就决定加入HandsFree了。我们啊，搞HandsFree，真的是出于我们在基地培养出来的对机器人事业的热爱，是看到中国机器人事业发展壮大的希望，是愿意从我们自身开始，推动中国机器人开源平台事业向前发展的愿景。是开源精神。是在互联网时代开放氛围下成长学习的我们，也愿意和别人，和走在同一条道路上的人，分享经验，共同成长的共享精神。这是HandsFree团队凝聚在一起的精神支柱。


&emsp;&emsp;说起来团队，HandsFree团队现在稳定的队员不到10人，都还是西工大上学的学生。团队内部机械、电子、ROS，视觉，运营干啥的人也有。鼎力支持我们的老师是航空学院的教授布树辉老师。他们实验室在搞的是视觉SLAM和无人机。和HandsFree有非常紧密的联系。HandsFree要干的事情也很多，技术开发，教程编写，开源产品设计，网站搭建，社区推广等等。。

&emsp;&emsp;为了技术开发,我们要赶紧把底层要完善发展的工作做完。然后赶紧开始视觉SLAM，机器学习的学习。

&emsp;&emsp;为了维持团队正常运行花费，我们还忙着运营卖小车赚经费，给团队添置一些材料设备。

&emsp;&emsp;为了让HandsFree能被更多的人知道,我们还要忙着参加重量级的比赛进行宣传,整理好网站和社区方便推广。

&emsp;&emsp;之前有人问我们有什么困难。想了半天想不出来。我们到现在一直都是很幸运的。布老师不遗余力，不求回报的帮助我们，师兄师姐也始终支持我们。每有一个人肯帮助我们，我们都感到万分幸运。团队现在能不定期的进行技术交流会，有自己的局域网千兆带宽服务器，能有钱买自己的VPN，能顺利的卖六七十台车，在开心的时候挤出一点钱去吃顿大餐。社区发展到500人多，使用者涉及全国30多家高校和科研院所跟公司。包括中科院，哈工大，厦大，电科里面好多好多人都在我们社区里面。我们等于是站在巨人的肩膀上，被大家一把一把扶着起来的。我们是真心的感谢那些帮助过我们的人，不管是给我们在技术上提供支持，还是在团队发展、宣传上给我们提建议，还是帮我们转发推送，真的真的感谢你们。真要说现在哪里困难，就是我们现在技术上的难题甘之如饴，但商业化问题十分头痛。缺少精通运营，推广的人来帮助我们。上次去珠海,感触最深的就是时代的发展.大西北太封闭了,不管是社会文化还是科技发展，到珠三角才是触摸时代的前沿,这里这么多机会等着你抓住,这么多资源等着人来用。机器人这么前沿的东西就在这里，你要不去攻占，明天就可能被别人占领。

&emsp;&emsp;现在几个人忙里忙外累死累活也能勉强维持前进，但是人无远虑，必有近忧。团队也是啊，团队现在有不少人都面临着就业上研或者考研的抉择，等我们走了之后，不想让HandsFree就这么没了,我们还是真心的希望能再找到一些人和我们一起走下去,能找到在各方面都有些特长，还能热爱机器人的人，来储备一批发展力量。

&emsp;&emsp;大学青春时光宝贵，能找到这样一个团队，大家一起喝酒吃肉，指点江山,这是多么荡气回肠的事啊！