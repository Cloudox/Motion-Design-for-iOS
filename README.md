# Motion-Design-for-iOS
翻译自《Motion Design for iOS》，讲解iOS动画设计指南

## <a name="Catalogue"/>目录
* [SECTION 1](#SECTION 1)
* [SECTION 2](#SECTION 2)
* [SECTION 3](#SECTION 3)
* [SECTION 4](#SECTION 4)
* [SECTION 5](#SECTION 5)
* [SECTION 6](#SECTION 6)

## <a name="SECTION 1"/>SECTION 1
在2013年六月，苹果推出了iOS 7，并与iOS 6大相径庭，让设计师回归本初。曾经代表漂亮iOS设计的现实主义拟物化离去了，而一个更加平面、光滑，更加“计算机真实”的美学到来了。这种向平面设计专项的一个重大影响就是在Photoshop（或者任何可选的设计工具）中进行一个设计变得更简单、花费更少的时间、并且不再有差异。创建一个有着漂亮现实渐变色、阴影和高亮的app界面是一件很艰苦的事情。而创建一个根本没有渐变色和阴影并且主要由大块相同颜色组成的app界面明显更简单。

平面设计让app更难从其他app中在视觉上脱颖而出。

现在，在这个iOS 7的世界，很多iOS app分享了类似的视觉设计美学。类似的颜色，类似的字体，类似的空白。iOS 7app设计中渐变色、阴影和其他视觉装饰的缺失降低了竞争（可以这么说！），并且现在设计师和开发者意识到不得不与他们的竞争对手通过使用`动作`和`动画`来区分创意。

这意味着什么？在iOS 7之前app中也有动画，有什么改变吗？改变的是如今提升app用户体验的动作设计的重要性和意义。曾经被认为后续再添加的东西（在你设计全拟物化和渲染3D界面之后）现在是你的客户体验你的app的焦点和关键方面。动画不再是最后的附属品，他们现在在整个设计过程中被设计和思考。

所以你现在准备好添加一些可爱的动画到你的app中了，那么从何处开始呢？在哪里并且如何添加动画呢？什么类型的动画是引人注目且自然的，什么动画是无聊且平凡的呢？

让我们开始吧！

### 流动的现实动画的起源
在1981年，迪士尼长期动画师Ollie Johnston 和 Frank Thomas（迪士尼九大元老的成员——1920年代和1930年代迪士尼的原始动画团队）写了一本名为《Disney Animation: The Illusion of Life》的书，概括了他们在迪士尼早期卡通工作中倡导人物动画的基本原则。

这12个基本动画原则在《Disney Animation: The Illusion of Life》一书中被详细的描述，并且这本书现在被工作于此领域的艺术家和动画师广泛地认为是“动画界的圣经”。即使这些原则是将近80年前的手绘卡通动画师所提出的，它们至今依然使用。

----------

![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%201/illusion.jpg)

----------

重印版颠倒了标题，将“The Illusion of Life”印在了前面

这些基本的原则是：挤压和拉伸(Squash and stretch)、预备动作 (Anticipation)、演出布局 (Staging)、连续运动和姿态对应 (Straight-Ahead Action and Pose-to-Pose)、跟随和重叠动作 (Follow Through and Overlapping Action)、缓入缓出 (Slow In and Slow Out)、弧线运动 (Arc)、次要动作 (Secondary Action)、时间节奏 (Timing)、夸张手法 (Exaggeration)、扎实的描绘 (Solid drawing)、吸引力 (Appeal)。

设计师Cento Lodigiani创建了一个很棒的video来演示这12个原则，用于一个有魅力的弹性立方体的简单对象。他也将这些例子转换成了一系列的GIF动图。

这些原始的动画原则创建了1920年代到1930年代精心制作的动画的框架。Ollie Johnston 和 Frank Thomas是新的卡通动画时代的先锋，所以我们如何运用这些基本的动画原则来设计现代软件交互呢？在进入这些细节之前，让我们先来谈谈为什么动画应该被用到你的产品中以及一般该如何考虑动画。

### 过渡，焦点和乐趣

当SDK第一次发布时我就开始思考设计和构建iOS app的动画。经过这次思考和所有这些app，我意识到有三个我要为一个iOS app（或者任何数字产品）想象、设计和构建一个动画的关键原因：

1. `过渡：`在两个视觉状态之间突出一个平滑的运动，让用户适应新界面而不是被推进去。像这样的平滑过渡可以减轻对于不熟悉的界面的精神负担。

2.  `焦点：`引导用户关注界面上的一个重要的或者最近更新的特殊部分，尤其是那些需要用户立即操作的元素。

3.  `乐趣：`通过使用奇思妙想或意料之外的动作让一个平凡的交互更加吸引人且有趣。

让我们看一些动画的例子并仔细剖析它们存在的原因以及它们使用这三类动画的目的。

----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%201/calendar.gif)

iOS 7日历app的动画


----------
苹果给iOS的日历app为iOS 7彻底重新构想了一遍。查看一年和单个月份之间的动画是一个很好的过渡的例子，在两个视觉状态直接引导用户。因为过渡不只是一个简单的导航栏控制器push，而是动画地放大一个更深细节的层次，用户能明确地感知到他们正在深入这个数据。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%201/call.gif)

iOS 7.1 通话界面和关机动画


----------
从iOS 7.1开始通过界面动画变得彻底精致了，并且现在比以前有了更加一致的设计。当接电话时，绿色的接通按钮会旋转并过渡成红色的，这样就可以变成挂断按钮。一个相似的过渡也发生在你点击绿色的拨通按钮发起一次通话的时候。带锁的关机滑动条现在变得更加易懂，并且整个屏幕（除了你在滑动的关机按钮）都会淡出来暗示如果你继续滑动它的话界面接下来将会进入什么状态——一部关机了的手机。

----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%201/speedometer.gif)

----------
上面显示的界面使用了一个内置的效果来从空白状态过渡到信息填充的屏幕。通过每个元素单独的动画，它迫使用户在其动画出现在屏幕上时一次只关注一个元素。内置的一步一步类型的动画让设计师可以调整用户使用过程中每一秒的的视觉焦点。这也比简单没有任何动画地显示这个界面或者一次对整个界面进行动画要更加有视觉吸引力。这种类型动画不好的一个方面是它展示界面和信息给用户花费了太多时间。这会引起反感，特别是当它一次次地发生的时候。动画时间和迟缓感知会在之后进行讨论。

----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%201/map.gif)


----------
这是一个很好的关于动画如何让用户适应并帮助他们理解app背后更大的逻辑模型的例子。当动画渐出主界面以及动画渐入地图时保持图标不动让地图图标看起来像两个面板之间的视觉支点。当用户点击地图图标时，地图会承接上一页，之前的界面收缩到背后但依然可见。用户不会觉得他们在移动时迷失在应用之中并且能够理解主要特性是如何工作的。

----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%201/paper.gif)


----------
Facebook Paper中所有的过渡和新展现的信息都使用了很多2D和3D动画效果。在第一个面板中，当点击地球图标时，Notifacations表单会从图标下方滑出，给用户一种它总是折起在地球图标下方，等待被显示的印象。还有，通过图标，它加强了一种特定的心理模型给用户，暗示这个额外的界面总是可以通过地球图标获取，无论他们在应用的那个地方。

在第三个面板中，当你从底部滚动视图中滑出一块占据整个屏幕的内容时，它会滑到当前内容的顶部来提醒用户他们可以通过一次简单的点击回到他们之前的地方。当整个界面淡出并且文章详细视图淡入时，用户可能忘记他们之前在app中的位置，所以Paper的多种过渡总是用来在用户的脑中定位导航流。

Paper使用了非常棒的动画框架Pop，Facebook将其发布为开源工程供所有开发者来使用。我们之后会深入研究Pop。

----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%201/iwatch.gif)


----------
在这个概念下Apple手环的动画，你可以看到每个界面之间的过渡都是流动性的，并且物体在内物体出现在界面上之前移出。每个物体移动得好像被之前运动中的物体拖出了屏幕。因为显示区域太小了，并且在水平方向上，使用动作来建立用户对app的心理模型非常重要。这里你可以看到音乐控件在时钟的左边并且在其下方是更改歌曲的功能区。在时钟的右边是一系列的app。所以即使在屏幕的左边没有任何导航线索（比如返回按钮），过渡动画也给了你关于产品及其界面的整体信息结构的感觉。

----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%201/menu.gif)


----------
就像之前手环的例子一样，这是另一个在视觉上解释应用数据层级的整体架构的动画。这个动画从一个简单的中心对齐文本菜单开始，当点击My Files的时候，文件夹图标会扩展开来显示那些文件。用户会得到一种菜单就在文件列表背后的感觉，并且觉得他们可以在任何时候点击右下角的菜单按钮回到列表。当点击菜单按钮时，收缩整个文件列表进入之前的文件夹图标然后再次显示菜单。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%201/music.gif)


----------
这是另一个Jakub Autalik设计的非常有趣的动画，之前的里程计东湖也是他创建的。每个界面都使用了多种内置的效果来错开每个视觉元素的显示。歌曲列表动画进入的方式比起简单地使用iOS导航栏push的动画进入来说是一种非常好看的方式。这个动画的关键不同点在于屏幕不是一次性移动的，界面上每一个独立的元素都在移动。为了达到这种效果，每个元素的开始时间都需要与之前的元素又一些错开，好像它们都被拖进来一样。这种类型的拖动效果会在之后作为编码示例来展示。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%201/skull.gif)


----------
这个下拉刷新的骷髅头动画是一个很好的介绍一些古怪而有趣的，容易被忽视并且构建非常简单（而且廉价！）不需要任何复杂动画的界面元素的例子。在下拉手势中发生了一系列事情，首先，组成骷髅头图片的元素会旋转，让它像是在向下旋转一样。然后，有两个默认状态下界面上不可见的动画人物在下拉的时候出现。最后，这些动画人物不是简单的在用户下拉的时候出现，它们的一部分也会在手势过程中旋转和移动。这是一个包含多个不同元素的非常复杂的动画，但是你可以想象用户可能会一次次地下拉界面，因为它实在是太有趣了。这是让他们记住这个app的地方，而在用户的主屏幕上凸现出来是非常重要的。

如果你在寻找其他人创建的非常棒的app动画例子，我高度推荐你浏览[CAPPTIVATE.co](http://capptivate.co)和[Dribbble](https://dribbble.com/search?q=animation)里的动画标签。

寻找动画并讨论它们为什么棒是很好的事，但是这不会让我们接近并充分分解它们做了什么从而自己创建惊艳的动画。让我们继续本指南的下一节来学习动画的结构和性能。

## <a name="SECTION 2"/>SECTION 2
### 动画属性
回头看看上一节显示的动画，它们是如何从一个空白的画布或白班变成一个复杂、漂亮的动画的？这些动画是怎么产生的？在变化过程中改变的特殊属性是什么？在回忆中摇晃你的手来表明一些物体应该移动或拉伸是不够的：如果你想要动画脱离你的手进入界面，你需要仔细思考在每一步中会发生什么以及哪些值被操作了。

如果你看一下上一节展示的动画GIF图，以及像[CAPPTIVATE.co](http://capptivate.co)和其他网站展示的多种动画，并且你对发生了什么观察得非常仔细，你就会开始在视觉效果中看出一些模式来。这些模式是设计师和开发者在他们的动画中一次又一次改变的特定属性，而且这还不是全部。事实上我认为如果你简单地操作下面三个属性就可以创建一个充满了世界级动画的完整app：

1. `位置：`界面上一个物体的精确的X和Y坐标。
2.  `透明度：`一个物体的透明度，从0.0（不可见）到1.0。
3.  `比例：`一个物体对比于其原始尺寸的尺寸。1.0的比例意味着物体被设置为其原始大小的高和宽。0.5的比例意味着物体是一半的宽度和高度。0.0的尺寸意味着物体的宽度和高度都是0，但依然存在于界面上一个特定的坐标。2.0的比例意味着物体的高度和宽度是原始的两倍。

这三个属性是人们设计iOS app的动画时三个可动画化的值。你可以通过简单地单独或结合使用这些属性实现惊人数量的好动画。

所以通过位置、透明度和比例这三个属性，你能做什么？怎样做才能操作这些属性来在屏幕上实现？

`位置。`如果你想要让一个物体在屏幕上移动，你只需要操纵它的位置。将一个向屏幕的下方移动意味着你在增加其Y坐标，因为（X:0, Y:0）在iOS app中表示屏幕的左上角。如果你想要将一个物体从屏幕的底部移动到中央，你首先需要将Y坐标设为比屏幕的垂直分辨率大（道屏幕底部），然后将Y坐标动画移动到一个较小的数值来放置在屏幕的中央。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%201/xy.gif)

`320*568是iPhone 5屏幕的一倍分辨率。iPhone 6的屏幕是375*667。然而全部真实的像素总数是这个的两倍，但你放置UI对象到屏幕上时不需要考虑这个。`

----------
`透明度。`将一个界面元素从100%不透明改成透明一些意味着你在调整它的透明度，或者alpha值。动画改编一个物体的透明度可能是最常见的属性，这可以在与背景混合到100%不透明地显露在前端之间做一个很好的过渡。而且如果你在缓慢地从屏幕上移除一些东西，动画淡出将其alpha设为0通常不会有错。一般你会看到透明度动画和其他属性的动画同时出现，比如说，将一些东西从屏幕底部移动到屏幕上（位置），同时将其透明度从0.0（透明）动画变成1.0（不透明）。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%201/alpha.gif)


----------
`比例。`如果你想要让一个物体变大或变小（一次变化两个方向来保持其比例，或一次只变化一个方向），有一个简单的属性可以调整，那就是物体的比例。想要创建一个看起来和iOS 7的警告框视图一样的模态警告框么？那是一个依托于改变比例的视觉效果的很简单的动画。将比例初始设为大概1.3倍（比原始尺寸要大），然后将其动画变为1.0倍（原始尺寸），同时改变透明度（从0开始变成1.0），这就是它的全部。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%201/scale.gif)


----------
现在我们已经描述了在设计动画是经常用到的三个属性，让我们回到之前我展示的动画例子并精确地拆分它们哪里用了位置、透明度和比例动画来创建它们的视觉效果。

----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%201/map.gif)


----------
在Jeff的地图动画中，他同时使用了所有位置、透明度和比例动画的组合。

* 初始的面板稍微缩小并且透明度降低，所以它很好地淡出到应用的背景中去了。
* 地图面板从一个比1.0倍稍微大一点的比例（可能是1.1倍之类的）以及0.0的透明度开始。然后动画减小到1.0倍以及1.0的透明度。它还有一个轻微的位置动画来上移一些像素。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%201/iwatch.gif)


----------
记得这个手表的界面和它光滑的动作么？真的没有什么秘诀，这个动画设计唯一的属性就是元素的位置。没有比例或者透明度的调节，元素仅仅是在屏幕上通过改变他们的位置来移入移出。每个动画的开始时间会比前一个元素稍微错开一点来给出一种“拖拽”的感觉，但是唯一用到动画里的就只有位置。

动画一个元素的位置、透明度和比例可以让你走的很远，但当然也有其他你可以在动画中操作的属性。这里是三个在更高级的动画中经常用到的元素属性。

`颜色。`就如CSS动画中一样，你可以在两个值之间过渡颜色。这可以是你界面中一些文本的颜色或形状和面板的背景色。你可以在一次点击或者介绍一个新界面给用户的时候过渡颜色。或者可以在用户首次体验一个滑动的时候在颜色之间缓慢地切换。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%201/color.gif)


----------
`旋转。`你界面中的物体可以旋转，从初始的0度到360度的旋转状态到360度的整体旋转并回到0度。当你在代码中创建动画的时候旋转通常使用弧度来表示（0到2π）。轻微的旋转动画可以增加非常灵巧有趣的元素到原本平凡的动作中去，尤其是和之后会讨论的跳跃动画曲线组合的时候。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%201/rotate.gif)


----------
`3D。`在你的界面中以3D的方式变化一个物体意味着在第三个方向上操作它，并且当你在动画中使用3D的时候，通常要么是3D旋转回屏幕，要么是旋转向用户。这个旋转的数量也是像2D平面旋转一样用弧度来表示的，但3D动画的另一个关键因素是你想使用多少透视程度。通过改变透视值，你可以有限地描述元素会被放置在视觉上离屏幕前端多远的地方。这取决于3D变化过程中变形的数值。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%201/3D.gif)


----------
一个精细的3D效果的例子是Clear中捏的动画。这个视觉效果是任务条目行视觉上折了一半，其中每一半都向屏幕里面旋转（在3D空间上）。旋转的数值和行的上下两半的位置都被仔细的控制，所以在中间没有缝隙去影响效果。还有，为了让它看上去确实像一个三维物体，要让行的上半部分比下半部分暗来显示一个阴影。这类似于Paper中的弹起动画：新闻在打开的时候使用了一个3D变化来旋转向用户。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%201/clear.png)

Clear中的捏交互


----------

### 计划动画
如果把动画比作一个房子，你现在至少已经在熟悉造房子的工具了：锤子、扳手和螺丝刀。你熟悉的动画的工具也就是你在创建一个动画的时候操作的特定属性。但这还不是你考试思考动画和设计动作需要知道的全部。

现在是时候开始布局动画的蓝图了。这是指准确描述动画中每一步将会发生什么的说明。如我之前提到的，你不能在开会的时候仅仅挥舞你的手臂来解释当用户点击一个按钮的时候会发生什么，你需要一个语言来描述和拆分你在想想一个界面元素运动时头脑中发生的事情。在你创建之前，你的下一步应该是思考将其化为细粒度并且写下动画的各个部分的细节。这就是动画的计划。

对于每个动画化的元素，在我开始写代码之前我喜欢思考以下几点。

1. `元素的初始属性是什么？`只是在屏幕的底部？是完全透明的吗？它会缩小的微观尺度吗？它是巨大的吗？
2. `元素的最终属性是什么？`元素现在是在屏幕的中间吗？现在是对用户完全可见的吗？它是不是被旋转到一个特定的角度了？他是不是有了一个不同的背景色？
3. `动画应该持续多长时间？`在这个初始阶段要知道动画的准确时间是很难的，所以我喜欢把时间转化为我打响指的时间长度。一个响指？三个响指？因为要在结束移动前进行弹跳所以是五个响指？
4. `元素动画的时候会发生什么？`通常你会同时动画很多事情，时间上一个个错开。作为整体的一部分来思考这些次级动画很重要。
5. `元素结束动画的时候会发生什么？`当你的动画结束的时候应该移除元素吗？或者也许在结束动画三个响指之后你想要它从另一个方向上离开？或者当这完成后，另一个元素会开始它的动画？

像这样组织你的思路会很有帮助。首先，它会强制你将一个抽象的动画概念模型转化为你可以跟他人描述的具体事物。然后，通过这个步骤你可能会发现一些在宏观视角下没有发现的需要处理的问题。元素2适合元素1同时开始动画吗？还是稍微错开一些？错开的时间应该多长？我应该将元素3移动多少距离来和元素4对齐？在我将元素5缩回到1.0倍大小前应该将它置为多大？我是应该将元素6淡出还是仅仅将它的比例减小到0？你一开始往往不会有这些问题的答案，但当你开始创建和运行你的动画的时候就会很快得到的。

### 如同生活一样，时间就是一切
有一个我至今没提到的动画的关键成分，但它确实是创建一个非常棒的、自然的动画最重要的一块拼图。时间。在一个动作发生和一个动画开始之间的时间。一个动画持续的时间。在两个动画开始之间的时间。

当然还有的是，你的动画元素的属性如何随着时间改变，只是动画的本质。

最简单的可视化说明时间以及属性随着时间改变的效果的方式如下所示。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%202/linear.gif)

一个线性动画的时间曲线


----------
图像代表了一个动画。垂直坐标轴表示你在动画的属性值，在这个例子中是元素的比例。对于这个动画，我们会从比例值为0.0开始（对用户不可见）并以1.0的比例值结束（元素的初始尺寸）。

水平轴表示动画开始（经过0秒）到你的动画完成的时间，在这个例子中，是一个1秒长的动画周期。橙色的线准确地表示了在某个特定的时间点属性值会变得怎样。如你所见，橙色的线是完全笔直的，这意味着值随着时间改变的比率是一个定值。对于这个动画，比例值随着一秒的时间以一个不变的变更比率从0.0到1.0变化。

这种特殊的时间曲线说明了一个线性动画，例如一个球在一秒时间内从比例0到比例1的线性动画。

这个球的比例随着时间以固定的速度持续增长，因为这个动画有一个线性的时间曲线。为什么要称一个直线为曲线呢？因为你很少让动画处于线性的时间下，大多数的动画时间图看起来都是曲线。下面的四个图形表示了一些典型的动画时间。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%202/easing.png)


----------
垂直轴表示你动画的属性值，例如元素的比例或位置（如上面的图形所讨论的）。垂直轴的底部表示属性的开始值，也就是为0的Y坐标，垂直轴的顶部是属性的结束值，也就是为100的Y坐标。水平轴表示你的动画从开始到结束的时间，整个轴长表示动画的周期。线准确地指示了在特定的时间点属性值会变成什么样。

曲线的动画时间看起来是什么样的？例如一个小球，以1秒的周期动画，但这次，我们要将其放在一个缓入缓出动画的球的旁边，看看有什么不同。

缓入缓出动画的小球的时间曲线大致如下。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%202/easeinout.gif)


----------
一个缓入缓出的曲线在很多地方都和线性时间曲线不同。首先，它确实是一个曲线，所以在0.25秒的时候比例不是0.25，值改变的速率不是恒定的。然后，最容易注意到的，它产生了一种不同的动画动作，即慢慢地开始动作（好像落后了一点）并且慢慢地结束（就好像接近最终比例的时候缓慢地变成最终值）。

线性动画曲线意味着你的属性值随着时间的流动以恒定的步伐改变，而各种迟缓的图形表示属性值会缓慢地开始改变，或者缓慢地结束改变，或者两者都有。

现在来添加第三个球的动画。这第三个球，会在开始的时候动作的很快，然后归于正常，不断变慢最终停止在最终值。这是一个淡出动作的例子。

下面是淡出动作的时间曲线。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%202/easeout.gif)


----------
一个视觉化这种曲线的方式是想象餐厅里的服务员给你拿来了你的食物。他们不会快速地突然将盘子放在你的面前，他们会慢慢地最终把盘子停放在桌子上。

最后一种更加常见的时间曲线是淡入动作，这意味着非常缓慢地开始动画，然后快速地结束。

下面大致就是这种动画曲线的样子。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%202/easein.gif)


----------
观察淡入动画曲线，你可以看到在0.5秒的时候（动画时间的一半）比例值仅仅才到最终值的1/4。这创建了一种动画开始得非常缓慢迟钝，然后在最后的时间里迅速地跑到最终值的感觉。

线性，淡入淡出，淡出，淡入动画曲线是四种大部分界面系统默认提供的内置的时间选项，比如说，在CSS3动画中就默认提供这些时间曲线。在iOS的动画框架——Core Animation中也是默认提供的。

类似Core Animation和CSS3中提供的缓慢曲线在数学上由Bezier曲线定义，就如你在Sketch、Illustrator或者其他矢量绘图工具中绘制的一样。要定义在缓慢动画中使用的Bezier曲线类型，你需要选择曲线端点的位置。Core Animation和CSS3执行缓慢动画使用的特定曲线类型是一种三维的Bezier曲线，意味着有四个控制点来定义。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%202/cubic.gif)

移动控制点是如何影响曲线形状的。


----------
下一节我们会开始学习漂亮动画背后的真实魔法，它创建了自然感觉的动作。

## <a name="SECTION 3"/>SECTION 3
### 自然的动作
标准的动画时间曲线是好用的，但还可以更好，而且它们不足以让你的用户觉得对你的界面感到惊奇和愉悦，因为它们仍然是机器人的感觉，而不是如人类或受外力驱动的物体般完全流动性和自然。如果我们想要让动画变得真正的自然，我们就需要去观察自然世界以及真实的物体的行为，这样我们就可以模仿其动作。这就是软件中迷人、自然的动画的秘密本质：让你的物体动作符合物理法则，这样你界面中的元素就仿佛有了质量和动量，就如在屏幕上滑动或就在你的用户手指下方一般。

所以自然的动作时怎样的呢？符合物理法则的移动例子是什么？好吧，就如下面这个一般。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%203/spring.gif)

弹簧的阻尼


----------
一个挂着方块的弹簧。它就如你所期望弹簧上的方块一样移动，因为你之前已经看过或体验过类似的弹簧运动很多次了。它的运动和之前说的简单动画时间曲线有很大的不同。让我们看一下弹簧上物体的动画曲线。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%203/damped.png)

阻尼的震荡运动


----------
这个曲线表示了挂在弹簧上的物体的运动，有很多的属性（例如拉力、摩擦力和阻力）都影响了其动作。如果你观察上图中的深蓝色曲线，它表示欠阻尼的系统，意味着物体在到达最终稳定位置前会来回震荡（反弹）。这就是让动画如上面的例子一般感觉像弹簧上挂着的方块一样需要的动画曲线类型。这种欠阻尼的弹簧动作可以让动画变得有弹性，很多app都在界面动画中采用了这种类型的动作。比如说，Facebook Paper几乎对所有界面动作使用了这种弹簧动作。

上图中中间的蓝色曲线也显示了一个欠阻尼的系统（在稳定前反弹过最终点），但它是一个反弹较少的更加平滑的动作类型。这会导致一个更精细的感觉，而过度反弹的动画会让你的界面变得太丰富或热情。

红色曲线描述了一个很少反弹而且只在到达最终位置前越过一点点的动作。如果物体一点都不震荡和反弹，只是缓慢地到达最终位置，这种弹簧就叫欠阻尼。

让我们看看类似弹簧动作的物体。红色的圆仿佛附有非常有弹性的弹簧一般在移动。绿色的圆带着稍微平滑一些的弹性移动。蓝色的不带有弹性，但会在接近终点值时以指数级衰退速度的动画变得非常的缓慢。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%203/threeballs.gif)


----------
第三个球实际上并没有弹性，但它的动画依然被现实世界的弹簧物理法则所管理，是怎么回事呢？弹簧不是应该有弹性么？如我之前所说，附有弹簧的物体的动作实际上由弹簧的特性决定。想象一个弹簧，组成弹簧的线非常的细。这个弹簧的拉力是非常的松额，如果你在其底部挂上一个小物体，并松开它，你就会看到如红球演示的弹性动作。比较一个拥有更多线圈和更大拉力的更加高强度类型的弹簧。挂在这种类型弹簧上的物体动作会很没有弹性，因为弹簧的属性非常不同。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%203/springs.jpg)


----------
类似弹簧动作的动画曲线和简单类型动作的动画曲线可能看起来相似（至少他们都是曲线！），但是它们背后的数学运算是非常不同的。如前所说，简单曲线通过三维贝塞尔函数来定义绘制曲线控制点的位置。不幸的是，很多高级类型的曲线不能用贝塞曲线来描述。其中一种曲线就是阻尼弹簧系统。

使用好的拥有弹簧感觉动画的动作类型一般模仿阻尼谐振，其可以调整弹簧末端方块质量、弹簧的刚度、阻尼强度等不同值。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%203/damped.gif)


----------
`质量`是指挂在弹簧末端物体的质量。`刚度`是指拉伸弹簧的难度，一般由弹簧的厚度和盘绕的密度决定。`阻尼强度`是指抵抗力度或者摩擦力，就如你尝试在水中快速拖动你的手时受到的阻力。这些是定义一个弹簧动作的关键属性。

如果你想要从头构建起你对web、iOS或其他平台的动画库，并且想要支持类似弹簧的动画，你就需要理解弹簧系统背后大量的数学知识才能正确地实现它。幸运的是，对于iOS，有很多已经存在的优秀的动画框架（由苹果公司或其他人创建）可以用来创建自然的、类似弹簧的动画。

在我们投入动画编码之前，让我们从头开始讨论开发iOS app的基本原则，然后进入界面开发和iOS动画。

### 开始iOS开发
如果你已经踏入原生iOS app开发之中，你可以跳过这一节去看Core Animation入门。但如果你刚开始iOS app的开发，抓住其基本就很重要，这样你就可以完全理解事物工作的原理。

#### Xcode
Xcode是Mac和iOS开发者用来创建原生应用的IDE（集成开发环境）。它不仅仅是一个像你可能用过的Sublime Text之类的代码编辑器，它是设计、编程、测试、调试和分发Mac和iOS应用的整个一套功能。有一些编写Mac和iOS app的替代方式，但是大部分的开发者都使用Xcode。要开始接下来的编程实例，你需要有从Mac App Store上下载的最近版本的Xcode。

#### iOS模拟器
iOS模拟器让你可以在你的Mac上测试你的iOS app，其提供一个窗口让它看起来像是你正在iPhone或者iPad上运行它们。如果你安装了最新版本的Xcode，它会包含iOS模拟器而且可以模拟所有当前的（以及大部分以前的）iOS设备，例如iPhone 4、5、6、6Plus、iPad、iPad retina、iPad mini等等。因为新iPhone的真实分辨率太高了，在第一次运行模拟器的时候你可能会惊讶，因为窗口非常巨大，可能会超过你屏幕的顶部和底部！幸运的是你可以在一个小一些的尺寸上显示模拟器窗口这样就方便看一些。重要的是要记住模拟器不是测试你app的完美方式，唯一获取性能和app感觉的方式是在你的设备上运行它，你可以在Xcode开着的时候将设备连接Mac，跟随指令在你的手机上运行它。

#### Objective-C
Objective-C是一种编程语言，于1980年代首次出现，并作为编写NeXT计算机的主要语言受到欢迎。当苹果公司买下NeXT后，他们使用了NeXTSTEP操作系统下的技术并用它创建了Mac OS X，从此Mac app和iOS app都使用Objective-C开发。 苹果公司使用Objective-C编写OS X和iOS的所有软件。在最近几年，苹果公司作出了显著的改善让Objective-C更适合新的程序员。

#### Swift
在2014年夏天的苹果开发者大会，苹果公司宣布他们正在致力于一种新的编程语言，名为Swift，此语言从Objective-C、Rust、Haskell、Ruby、Python和其他语言中获取灵感，创建出他们称为“不要C的Objective-C”的语言。Swift被设计为和已经存在的Cocoa和Cocoa Touch框架协作（苹果公司提供给开发者来创建应用的API库）而且可以和Objective-C在同一个app中共存，但不能在同一个源代码文件中。部分的WWDC app是用Swift编写的，但苹果仍未任何完全用Swift编写的主要软件。当2014年九月初发布iOS 8时，苹果宣布Swift发布了1.0版本并可以安全地使用于发布到App  Store的app中。

我对于Objective-C和Swift的立场是：Swift太新了，而且在走向黄金时代生产app开发前依然有问题需要解决。然而，它的语法比起Objective-C无处不在的的方括号[和]，看起来和JavaScript更为接近，因此它对新的iOS开发者更为诱人。我依然使用Objective-C编写我的app，但随着时间流逝，我会至少在新的工程中部分使用Swift。我对Swift中的一些Objective-C没有的高级语言特性非常期待。本书中的全部动画示例代码都会有Objective-C和Swift两种编写方式，因此你可以理解和观察其区别并自行选择哪一种语言对你的使用更有意义。

如果Objective-C对你来说是全新的，我推荐你阅读我对Objective-C的介绍以及Big Nerd Ranch的[Objective-C Programming book](https://www.bignerdranch.com/we-write/objective-c-programming/)。如果Swift对你来说是全新的（除了苹果公司以外每个人都是这样！）你应该看看iBooks上500页的[Swift Programming Language](https://itunes.apple.com/us/book/swift-programming-language/id881256329?mt=11) 指南，这是免费的。在苹果开发者中心也有一个非常好的[Swift引导](https://developer.apple.com/library/ios/documentation/Swift/Conceptual/Swift_Programming_Language/GuidedTour.html#//apple_ref/doc/uid/TP40014097-CH2-XID_1)。

现在你队iOS开发工具和语言都有了一些接触，让我们开始一些关于iOS app界面是如何创建的以及让它们显示在屏幕上的过程的细节。

##从UIKit和CoreAnimation开始
通常情况下，iOS app中屏幕上的物体都是`UIView`对象。它们是矩形的并且有坐标和大小来定义它们在屏幕上的位置和尺寸。`UIView`是用来构建你的界面的UIKit Framework中基本的界面对象。每个视图都可能伴随着文本、形状或图片绘制。比如说，iOS app中的状态栏是一个长且瘦的视图，处于屏幕的顶端，并且状态栏目中的每个物体（时间、电池指示器、信号强度指示器等等）都是状态栏视图中的其它视图。

这些是为某些功能或特性特定的特殊的`UIView`对象。包括作为界面按钮的`UIButton`、用来显示图片的`UIImageView`、显示文本的`UILabel`和显示列表的`UITableView`。你也可以通过绘制任何你想要的东西来完全自定义`UIView`。

这是我的app Interesting for iPhone的截屏和界面中一些视图的分解。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%203/header.png)


----------
1. 运营商图像视图（苹果控制）
2. wifi信号强度视图（苹果控制）
3. 当前时间视图（苹果控制）
4. 电池等级视图（苹果控制）
5. “汉堡包”菜单按钮
6. 标题栏中的标题标签
7. 改变子板的按钮
8. 一个`UITableViewCell`视图，用来包含`UITableView`中一行的元素
9. `UILabel`中的帖子标题
10. 评论数量`UIButton`，由一个评论气泡图和评论的数量组成
11. 显示帖子URL的`UILable`
12. `UILabel`中显示帖子的点值和子板

如果你不熟悉iOS用户界面开发，看看一些你喜欢的app，看能不能找出界面中所有的视图，以此作为分解你自己设计的练习，这样你就可以学习在代码中构建它们。

`UIView`对象有很多的职责，其中之一就是事件处理，即响应触摸事件。如果你想的话你界面中的所有视图都可以响应触摸事件，或者你可以指定只有特定的视图会在用户触摸它们时响应。

一个`UIView`本质上是一个包含内部图形的矩形。在屏幕上布局，靠近或在其他视图的顶部，还可能会有高级的透明效果来整合到一起或者快速绘制。像你想象的一样，让大量的视图在屏幕上移动确实是一个挑战，尤其是在一个小的，低功率的设备上。

`这就是为什么苹果公司开发了Core Animation。`

Core Animation是一个动画和图形合成框架，用于提高速度和效率。虽然在名字中有动画的单词，不要让它误导你以为它只能做这个；它实际上负责屏幕上显示的所有视图的整体渲染体系结构，可以非常快速地进行透明度计算、图像过滤和视觉效果。它是为iOS创造的，但从OS X10.5开始，也可以在Mac上应用。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%203/calogo.png)


----------
要通过GPU管理渲染在屏幕上的图像内容，Core Animation使用`CALayer`对象作为主力。`CALayer`负责界面渲染，实际上，`UIView`对象只是`CALayer`的简单封装，而Core Animation在苹果公司内部最初名为Layer Kit！当你在屏幕上操作一个`UIView`的布局或方向的时候，你实际上在移动它的`CALayer`。Core Animation在硬件层面管理合成并操作你app的界面内容，与显卡对话并精简你界面的渲染，让它变得快速而不迟缓。iOS中所有的动画性能都是由Core Animation框架实现的。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%203/ca.png)


----------
图层可以像视图一样被层级安排来在屏幕上创建一个完整的用户界面。你不是非得要用`UIView`对象来构建你的界面，也可以使用`CALayer`对象来代替，像视图一样将它们按照父视图-子视图的类型放置，只不过替换成父图层-子图层。

虽然你可以只是用`CALayer`不用视图来实现一个app的界面，大部分的iOS开发者仍然都会使用`UIView`对象而不是直接使用`CALayer`对象来构建app界面，除非他们在做一些严肃的图形处理或者一次性布局成百上千的图形。如果你需要直接更改图层属性的话随时都可以获取一个视图的图层，比如说，设置一个视图的圆角弧度就是通过操作视图的`CALayer`属性来完成的。

### 简单动画
是时候写一些代码了。让我们先添加一个简单的`UIView`对象到屏幕上并设置它的圆角。我们要把它添加到我们的主窗口上时因为它是一个快速的例子，但在真实的app界面中你需要添加到管理当前界面的视图控制器中。

```objective-c
UIView *redBall = [[UIView alloc] initWithFrame:CGRectMake(50, 50, 100, 100)];
redBall.backgroundColor = [UIColor redColor];
redBall.layer.cornerRadius = 50;
[self.window addSubview:redBall];
```

我们创建了一个新的`UIView`对象并设置了它的框架来定义它在屏幕上的的X和Y坐标，以及它的宽和高，然后将其添加到屏幕中。我们还将它的背景颜色属性设为了红色。如我前面所说，要让一个视图的角变为圆角，你需要获取它的layer，所以我们设置它的layer.cornerRadius值为50，这是宽度的一半。如果你在你的app的delegate类的-application:didFinishLaunchingWithOptions方法中添加这个代码，就可以在运行后的屏幕上看到它。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%203/ball.png)


----------
这里是和上面一样的功能，但是是Swift而不是Objective-C写的。你可以打开Balls In Swift Xcode工程导出这个例子的Swift版本。

```swift
var redBall = UIView(frame: CGRect(x: 50, y: 50, width: 100, height: 100))
redBall.backgroundColor = UIColor.redColor()
redBall.layer.cornerRadius = 50
view.addSubview(redBall)
```

我们在屏幕上有了一个红色的球！很激动，我知道。现在我们让它动起来。

iOS提供了一些内置的技术来创建动画：创建并添加一个`CAAnimation`到我们之后要讨论的layer中，或者使用简单的基于block的动画方法来动画化`UIView`的值。让我们创建一个基于block的动画来将圆从1.0扩大到2.0倍，这会让它变成原来的两倍大。

```objective-c
UIView *redBall = [[UIView alloc] initWithFrame:CGRectMake(50, 50, 100, 100)];
redBall.backgroundColor = [UIColor redColor];
redBall.layer.cornerRadius = 50;
[self.window addSubview:redBall];

[UIView animateWithDuration:.5 delay:0
    options:UIViewAnimationOptionCurveEaseInOut animations:^{
    redBall.transform = CGAffineTransformMakeScale(2.0, 2.0);
} completion:NULL];
```

这个`UIView`上称为 +animateWithDuration:delay:options:animations:completion: 的类方法时`UIView`提供的多种动画方法之一。第一个安排，持续时间（duration），被设为半秒，第二个安排，延迟（delay），被设为0。

选项（options）参数让我们设置想要使用的动画类型（它还允许你设置一大串其他选项例如在动画完成后自动反转），所以这个简单的测试中我们选择`UIViewAnimationOptionCurveEaseInOut`来将时间设为简单的淡入淡出时间曲线。其他的时间曲线选项还有线性、淡入和淡出。

接下来，动画（animations）安排使用了一个block代码作为值，在block中你可以设置你要动画的视图的最终状态。Core Animation会自动在球的当前尺寸值和你的最终值之间更改来产生一个平滑的动画。这一次，我希望动画能最终让球变成两倍大，所以我设置了球的transform属性为一个新值。transform是一个表述了视图中每个像素根据一些线性代码应该改变的值的矩阵。有很多方式来操作一个视图的transform（尺寸、旋转、位置），所以苹果提供了很多函数来改变你感兴趣的值，在我们的例子中，是尺寸。将transform属性设为`CGAffineTransformMakeScale(2.0, 2.0)意味着我们想要其他所有的值都保持不变，除了尺寸，我们想让尺寸变为原来的两倍。

最后，我们不需要在动画完成后运行任何代码，所以我么你设置完成（completion）的安排为NULL。这里是你再次运行代码后会看到的样子。GIF会回到原始的样子但实际上球并不会。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%203/ballanim1.gif)


----------
这里是Swift下同样的代码：

```swift
UIView.animateWithDuration(0.5, delay: 0,
    options: UIViewAnimationOptions.CurveEaseInOut, animations: {
    redBall.transform = CGAffineTransformMakeScale(2.0, 2.0)
}, completion: nil)
```

在block代码块中我们可以改变很多视图相关的属性，它们会在同一个持续时间内一起动画。现在让我们再添加一些值的改变到动画block中来丰富你使用基于block的动画可以操作的内容。

```objective-c
UIView *redBall = [[UIView alloc] initWithFrame:CGRectMake(50, 50, 100, 100)];
redBall.backgroundColor = [UIColor redColor];
redBall.layer.cornerRadius = 50;
[self.window addSubview:redBall];

[UIView animateWithDuration:.5 delay:0
    options:UIViewAnimationOptionCurveEaseInOut animations:^{
    redBall.backgroundColor = [UIColor greenColor];
    redBall.transform = CGAffineTransformConcat(
        CGAffineTransformMakeScale(2.0, 2.0),
        CGAffineTransformMakeTranslation(75, 0));
} completion:NULL];
```

在我们现在的动画block中，我们做了很多事情。首先，我们将视图的背景色从原始的红色改成了绿色。Core Animation会帮我们修改它并处理中间的颜色。接下来，我们改变了两个关于视图的transform的内容：它的尺寸和平移。平移的更改会将视图上、下、左、右移动。在我们的例子中，我们会将它右移75个像素。我们使用了`CGAffineTransformConcat()`函数来将两个更改操作合成了一个，这样就可以分配一个简单矩阵转化给视图。你可以手动构建转变矩阵来包含尺寸和平移更改到一个数据结构中，但我发现让iOS来帮我们结合多个单独的转变到一个最终转变会容易一些。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%203/ballanim2.gif)


----------
到目前为止有意义吗？围绕转变矩阵的数学有一点复杂和困难，但是苹果让它变得亲近，即使你没有线性代数的背景。动画一个视图的转变矩阵是发动动画最有效的方式之一。

##从iOS 7中的弹簧动画开始
从iOS 7开始，苹果在他现有的一套动画方法中添加了类弹簧的动画能力。实际上，他们还添加了很多东西；他们的UIKit Dynamics 框架是一个整合到了UIKit中的完整的物理引擎，允许你添加地心引力、弹簧附着、动力等到你的界面元素中。

让我们看看一个iOS 7中介绍的更改了的基于block的动画方法，它现在增加了一些额外的参数来实现类弹簧动画。这个是我们动画代码的更改。

```objective-c
UIView *redBall = [[UIView alloc] initWithFrame:CGRectMake(50, 50, 100, 100)];
redBall.backgroundColor = [UIColor redColor];
redBall.layer.cornerRadius = 50;
[self.window addSubview:redBall];

[UIView animateWithDuration:3 delay:0 usingSpringWithDamping:.3
    initialSpringVelocity:0 options:0 animations:^{
    redBall.transform = CGAffineTransformMakeTranslation(300, 0);
} completion:NULL];
```

哇，这是一个长方法！如你所见，有一些我们之前的例子里没有的额外的参数在方法中调用了。参数包括弹簧阻尼和初始弹簧速度。弹簧阻尼是一个0到1之间的值，1模仿一个没有震荡的过阻尼弹簧系统，0表示很有弹力的欠阻尼系统。速度参数用来定义物体开始的快慢，当你使用手势用于用户在屏幕上滑动手指持续一个物体的移动的时候会非常有用。

在我们的例子中我们设置阻尼为0.3（有点弹性），因为我们是用物体静止开始的所以速度为0。因为弹动会使时间变长所以我们也增加了持续时间。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%203/redspringy.gif)


----------
就我个人来说，我不认为iOS 7中使用了新block方法的弹簧动画如我所愿地平滑移动，当你想要完善动作时他们也没有提供足够的弹簧属性来操作。还有，如果你在创建一个地图app并想要使用这些UIKit Dynamics中的弹簧动作将是不幸的。如果你的app还需要支持iOS 7之前的版本怎么办？你也是不幸的，因为UIKit Dynamics直到iOS 7才出现并且不能用于之前的版本中。

所以还有什么别的方式可以创建自然的动作、类弹簧的动画呢？其他的可选项是什么？幸运的是，我认为有两个非常好的UIKit Dynamics的替代方式可以解决我上面列出的关于调整属性和不修改太多就能在iOS 6以及Mac OS X上工作的所有问题。我是下面给两个框架的铁杆粉丝，并且在我已发布和未来开发的app上广泛地使用它们。

这两个框架是`JNWSpringAnimation`和`Pop by Facebook`。

##JNWSpringAnimation
JNWSpringAnimation是Jonathan Willing，一个Mac和iOS开发者，写的一个很棒的动画框架。要理解它为什么棒，让我们先回过头再一次谈谈Core Animation。

如我之前所说，Core Animation的时间曲线是由三维贝塞尔曲线定义的。你可以告诉一个动画去使用线性、淡入、淡入淡出或者淡出时间曲线，或者你可以手动设置曲线的控制点，就如你可以在CSS动画中使用三维贝塞尔动画时间函数。

然而，你不能用这种方式定义弹簧动作动画曲线，因为他们的形状太高级了。所以你可以怎么做呢？我们可以创建类似这个的其他什么动作吗？


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%203/linespring.png)

这种类型的弹簧动画曲线无法通过简单的三维贝塞尔曲线来创建。

----------
苹果还给开发者提供了一种称为`CAKeyframeAnimation`的特殊的动画类别，用来代替无忧的像我们之前讨论的动画（你定义开始和结束值并让Core Animation为你计算中间值）

关键帧动画是指你给系统提供一系列的值（用来改变物体的位置、旋转、比例等等。）然后它会根据你定义的时间间隔一步步地改变你列出来的值。你可以使用关键帧动画来创建多重部分的动画，其中一些物体在开始的几秒移动到一个位置，然后移动到另一个方向。你还可以改变每段的时间曲线。

JNWSpringAnimation工作的方式就是定义你的弹簧的关键属性，例如阻尼、刚度和质量，然后告诉它你要动画的属性是什么，JNWSpringAnimation就会为你创建一个包含你的动画的大量值的`CAKeyframeAnimation`，在到达最终值前弹簧动作曲线中的每1/60秒都有值。接着，你要做的只是将这个关键帧动画添加到你想要动画的`CALayer`中去，（可以是它自己的layer，或者是一个`UIView`的layer属性），Core Animation会一步步地执行每个关键帧，每秒60次，直到它到达最终位置动画就结束了。系统不需要知道你是如何生产关键帧列表中的所有值的，也不需要知道它会产生什么类型的动作，它只是盲目地在每一步按照你想要的方式改变动画属性。

详细地说的话，JNWSpringAnimation获取你给它的用来描述你想要在动作中模仿的弹簧的值，并用代码绘制真实的弹簧曲线。然后生成所有的动画关键帧值，它本质上在曲线上每次只走非常小的一步来定义曲线上每1/60秒的值。那就是为物体移动过程中每个位置的值。完成这个过程会非常快，因为要在动画开始前就全部准备好。

让我们看一些使用JNWSpringAnimation来使用不同类型的弹簧动作并有不同属性的动画的例子。在我们的第一个例子中，我们还是要动画之前同样的红色的球，使用我们定义的弹簧管理的弹簧效果将它的尺寸从1提升到2.0倍。

```objective-c
JNWSpringAnimation *scale =
    [JNWSpringAnimation animationWithKeyPath:@"transform.scale"];
```

首先，我们定义我们的`JNWSpringAnimation`对象，一个动画的新实例，命名为scale。我们使用定义的初始化器并将关键路径置为“transform.scale”，不过这表示什么呢？这个关键路径就是指我们想要动画的属性或值。它是视图下的`CALayer`对象的一个属性，也就是我们实际打算使用关键帧动画的动画。还记得`CALayer`是Core Animation中真正的主力么？这是因为当使用类似关键帧动画的动画时，你会将其放置到你想要动画的layer上，而且一般这个layer是`UIView`对象的组成部分。想要动画一个展示照片的`UIImageView`？动画它的layer。想要动画一个`UIButton`？动画它的layer。

基于此我们有一个知道它要作用的属性是什么的`JNWSpringAnimation`对象。是时候通过调整一些弹簧的属性来调整这个动画的动作了。

```objective-c
JNWSpringAnimation *scale =
    [JNWSpringAnimation animationWithKeyPath:@"transform.scale"];
scale.damping = 9;
scale.stiffness = 100;
scale.mass = 2;
```

阻尼、刚度和质量是我们要调整获得我们的球动画的完美的动作的三个重要的弹簧属性。我如何触碰这些值呢？很简单！JNWSpringAnimation也包含了一个Mac app让你交互式地处理这三个值并直接看到结果。

还有一个要注意的重点是你没有在JNWSpringAnimation中像之前在基于block的`UIView`动画中一样设置持续时间。阻尼、刚度和质量三个属性或产生一个一旦系统的力学到达最终值就会在最终值安定下来的弹簧动作。如果你想要缩短你动画的持续时间，就需要调整弹簧的属性才能快一点到达最终值，一般来说会增加弹簧的阻尼属性。通过非人工地操作弹簧动作的整体持续时间，就可以让你在动画的物体想在自然世界中伴随真实弹簧管理其整个动作和持续时间一样移动。这就是JNWSpringAnimation创建的动画看起来非常自然和有趣的原因。

我们刚才将一个红色的球作为动画示例，弹簧的动作并不是关键的，我们何时开始用下一节中定义的动作动画实际的界面元素，以及我们想要实现什么才是关键。这就是为什么一个类似JNWSpringAnimation提供的交互式的弹簧定义的app很重要，当你创建你的动画时它节省了大量的时间。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%203/jnwdemo.gif)

----------
一旦你完成你动画的完美动作，你只需要插入阻尼、刚度和质量值到你的动画代码中，然后无论你动画什么都会和你之前正确的值的动作一样。

我们也需要让`JNWSpringAnimation`对象知道我们想要动画属性的开始和结束值是什么。这是用来绘制弹簧和关键帧值的。

```objective-c
JNWSpringAnimation *scale =
    [JNWSpringAnimation animationWithKeyPath:@"transform.scale"];
scale.damping = 9;
scale.stiffness = 100;
scale.mass = 2;
scale.fromValue = @(1.0);
scale.toValue = @(2.0);
```

现在我们的`JNWSpringAnimation`对象知道了它的开始值和结束值，以及我们想要模仿的弹簧的准确属性，我们现在可以把它添加到我们想要移动的`CALayer`上去了。在我们的例子中，我们要将它添加到redBall上去。

```objective-c
JNWSpringAnimation *scale =
    [JNWSpringAnimation animationWithKeyPath:@"transform.scale"];
scale.damping = 9;
scale.stiffness = 100;
scale.mass = 2;
scale.fromValue = @(1.0);
scale.toValue = @(2.0);

[redBall.layer addAnimation:scale forKey:scale.keyPath];
```

这个名为scale的动画现在根据给定的关键路径（又称为我们想要在layer上改变的值）被添加到redBall.layer中了。我们可以将“transform.scale”传入到forkey:的参数中，但我们也可以只传入准确的我们创建的动画关键路径，这样我们就不会混淆`JNWSpringAnimation`的关键路径和我们要协调动画时使用的关键路径。在这个例子中，我们创建动画使用的关键路径“transform.scale”可以直接写成scale.keyPath.

如果我们创建并运行我们的代码，这就是产生的动画。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%203/jnwdemo2.gif)


----------
现在如果你想要在Swift工程中使用`JNWSpringAnimation`，由于你是使用一个Objective-C框架，你需要使用一些称为“桥街头”的东西让Xcode知道你想要在你的Swift代码中使用非Swift的框架。所以首先，我拖动称为JNWSwift的我需要使用`JNWSpringAnimation`的.h和.m文件到Xcode中的我的Swift工程中（包含到Xcode工程文件中）。Xcode就会询问是否要创建一个桥街头，我选择要，这就是哪个特殊文件的内容。

```objective-c
// This is within the JNWSwift-Bridging-Header.h file
// that was automatically created for me

#import "JNWSpringAnimation.h"
#import "NSValue+JNWAdditions.h"
```

任何添加到这个特殊的桥街头文件中的Objective-C头文件都会被设为Swift可见，这样你就可以使用Swift来交互它们的Objective-C函数。酷的地方在于当你想要在你的Swift代码中使用它们时，你不需要有任何`import`说明，Xcode会处理它。

当设置好桥街头之后，你就可以进入你的Swift代码中并开始处理你想要操作的对象，在这个例子中，就是`JNWSpringAnimation`。这里是我用Swift写的创建与上面的例子一样的动画的代码，依然是使用`JNWSpringAnimation`。

```objective-c
let scale = JNWSpringAnimation(keyPath: "transform.scale")
scale.damping = 9.0
scale.stiffness = 100
scale.mass = 2
scale.fromValue = NSNumber(float: 1.0)
scale.toValue = NSNumber(float: 2.0)

redBall.layer.addAnimation(scale, forKey: scale.keyPath)
```

它看起来和上面的Objective-C代码非常接近，但是当然没有包含调用方法的方括号，并且如果你写过JavaScript的话，它看起来与其非常相似。

这就是Swift代码和Objective-C代码会创建的一样的动画。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%203/jnwdemo2.gif)

----------

球的动画是从其原始尺寸增加到两倍大然后立即跳回其原始尺寸。这确实是我们上面所写代码的准确行为，但球在动画完成后跳回到起原始尺寸的原因却是需要重点理解的。

Core Animation在任何给出的时间内会维持三个你的层的集合或者树。每个层树都会在你的界面显示过程中扮演一个重要的角色。

1. `模型层树。`模型层树反映了一个layer静止不动画时的所有属性。比如说，当我们设置redBall.layer.cornerRadius到50来让它变成球时，我们就是在模型层上设置属性。模型层上的值是你的app交互的最多的。任何时候你改变一个layer的值时，都在更新它的模型层。模型层上的值不会在动画过程中改变，并会持续反应你添加动画前的值。
2.  `表现层树。`表现层树反映了动画时layer上的属性，并包含了运行动画时的变化值。你不应该在这个层树上设置任何值，通常都是在想要准确了解一个layer在哪或是其在动画过程中的行为时通过查看当前的动画值来与表现层树交互。
3.  `渲染树。`渲染树时苹果的私有值集合，用来执行渲染到屏幕上的实际绘制。你不需要与其交互或知道这些值。

当我们添加一个动画到layer的时候，动画会在layer 的表现树上操作这些值，当动画完成的时候，动画会自动从layer移除，并且表现树的值会变回模型树的值，因为这些值反映了真实、静止的layer属性。

如果我们想要layer 的属性更新为动画的最终值，我们需要明确地说明。对，我知道折痕奇怪，但因为Core Animation允许开发者构建非常多类型的动画，它们需要支持有些时候你确实想要你的动画被移除然后layer回到其原始位置的使用案例。

这里是在末尾添加了决定性的一行后的代码示例。

```objective-c
JNWSpringAnimation *scale =
    [JNWSpringAnimation animationWithKeyPath:@"transform.scale"];
scale.damping = 9;
scale.stiffness = 100;
scale.mass = 2;
scale.fromValue = @(1.0);
scale.toValue = @(2.0);

[redBall.layer addAnimation:scale forKey:scale.keyPath];
redBall.transform = CGAffineTransformMakeScale(2.0, 2.0);
```

通过手动地设置redBall的transform属性为两倍比例，并匹配动画的最终值，动画会在移除的时候将实际的layer上的transform值无缝更新为匹配动画的最终值。现在球就会维持在2倍大小了。GIF依然会回到起始位置，不过在代码中球不会。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%203/jnwdemo3.gif)


----------

你可能会想，我们使用基于block的UIView动画时并不需要处理这些，完全正确。`UIView`上基于block的动画方法是一个创建简单动画的更方便的方式，因为它们会自动保留最终值而无需去设置。当然了，你会被默认的过渡动作或者iOS 7提供的简单的弹簧动作所限制。如果你想要完整控制你的动画并想要细致地调整你的弹簧属性，你就需要奔向真实的`CAAnimation`对象，`JNWSpringAnimation`就是其中之一。

使用类似JNWSpringAnimation弹簧动画框架的真实诱惑是你可以获得对你弹簧力学的精确控制，所以让我们看看更多使用不同弹簧动作的红球的例子。

```objective-c
JNWSpringAnimation *scale =
    [JNWSpringAnimation animationWithKeyPath:@"transform.scale"];
scale.damping = 13;
scale.stiffness = 540;
scale.mass = 11;

scale.fromValue = @(1.0);
scale.toValue = @(2);

[redBall.layer addAnimation:scale forKey:scale.keyPath];
redBall.transform = CGAffineTransformMakeScale(2.0, 2.0);
```

这些弹簧属性产生了一个更慢、更深的移动。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%203/jnwdemo4.gif)


----------
下一个例子没有任何弹性，但有一个指数衰减动作来慢慢地到达最终值。这是模仿过阻尼的弹簧系统。这个动作类似于简单的淡出动作，但到达最终值时会更加的轻缓。我们也可以通过操作阻尼和刚度属性来调整其到达最终值的速度。

```objective-c
// 所有其他部分的代码都是一样的
scale.damping = 6;
scale.stiffness = 6;
scale.mass = 1;
```


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%203/jnwdemoexpo.gif)


----------
这里是三个并排的球，第一个的阻尼为6、刚度为6、质量为1。第二个阻尼为15、刚度为15、质量为1。第三个阻尼为30、刚度为30、质量为1。他们都是指数衰减型的动作，但他们到达最终值的速度不同。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%203/jnwdemo3balls.gif)


----------

我大部分展示的比例变更动画，但这不意味着你不能动画layer的更多属性！这里就是使用JNWSpringAnimation来使用弹簧动作旋转一个layer的示例。

```objective-c
JNWSpringAnimation *scale =
    [JNWSpringAnimation animationWithKeyPath:@"transform.rotation"];
scale.damping = 10;
scale.stiffness = 100;
scale.mass = 3;

scale.fromValue = @(0);
scale.toValue = @(M_PI_2);

[redBall.layer addAnimation:scale forKey:scale.keyPath];
redBall.transform = CGAffineTransformMakeRotation(M_PI_2);
```

由于这是一个旋转动画，开始和结束值是由弧度定义的角度。我们使用便利的函数`CGAffineTransformMakeRotation()`来设置模型层的最终值为2π。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%203/jnwdemorotate.gif)


----------
接下来我们要设置弹簧的阻尼和刚度为如之前展示的3个层示例一般会导致指数衰减类型动作的类似值。我们会动画其位置，而不是layer的比例。

```objective-c
JNWSpringAnimation *scale = [JNWSpringAnimation
    animationWithKeyPath:@"transform.translation.x"];
scale.damping = 7;
scale.stiffness = 7;
scale.mass = 1;

scale.fromValue = @(0);
scale.toValue = @(400);

[redBall.layer addAnimation:scale forKey:scale.keyPath];
redBall.transform = CGAffineTransformMakeTranslation(400, 0);
```

我们要动画的位置关键路径为“transform.translation.x”，是从左到右的位置——x坐标。我们会将其向右移动400个像素，所以toValue是400，要设置最终值并保持球在我们动画的地方，我们需要设置球的transform到`CGAffineTransformMakeTranslation(400, 0)`。这个函数是一个改变视图的变化矩阵的平移组件的简单方式，它接收两个参数，x和y的变化。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%203/jnwdemobrown.gif)


----------
当然，我们可以一次性动画很多属性。这里是一个同时动画比例和旋转的代码。看你能不能发现与单个属性动画的区别。

```objective-c
JNWSpringAnimation *scale = [JNWSpringAnimation
    animationWithKeyPath:@"transform.scale"];
scale.damping = 9;
scale.stiffness = 9;
scale.mass = 1;
scale.fromValue = @(1);
scale.toValue = @(4.0);

[redBall.layer addAnimation:scale forKey:scale.keyPath];
redBall.transform = CGAffineTransformScale(redBall.transform, 4.0, 4.0);

JNWSpringAnimation *rotate = [JNWSpringAnimation
    animationWithKeyPath:@"transform.rotation"];
rotate.damping = 9;
rotate.stiffness = 9;
rotate.mass = 1;
rotate.fromValue = @(0);
rotate.toValue = @(M_PI);

[redBall.layer addAnimation:rotate forKey:rotate.keyPath];
redBall.transform = CGAffineTransformRotate(redBall.transform, M_PI);
```

第一个动画是一个比例变化，从1.0到4.0变成四倍大小。与之前的例子的代码相比第一个不同是当我们在添加动画后设置模型层的实际变化值时（所以它才能保持最终值。）不是使用`CGAffineTransformMakeScale()`函数来进入新的比例，而是使用了名称相似容易混淆的`CGAffineTransformScale()`函数并接收了三个参数。`CGAffineTransformMakeScale()`（包含make在其中）假设你想改变到的变化矩阵是常规、默认、未触摸的恒等变换的变化矩阵，其刚刚创建了此时的视图。

另一方面接收三个参数的`CGAffineTransformScale()`，第一个参数是你想要改变的起始的变化矩阵。这可以是恒等变化或者一个已经有了一些操作的变形，比如已经被旋转了、伸缩了、平移了等等。我们使用这个函数并且将视图当前的变形作为第一个参数的原因是我们正在添加两个动画到其中并且它们都会操作layer的变形矩阵。如果我们使用`CGAffineTransformMakeScale()`，就会影响所有的第二个动画的变形调整，使用开始的恒等变换，而不是最近更新的第二次动画设置的layer变形。通过引入当前的变形值，我们可以确保对我们的操作使用最近的值，而这就会包含第二个动画的最终值。

第二个动画会旋转我们的对象π的角度。让我们看看包含比例和旋转变形的动画看起来什么样。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%203/jnwdemo5.gif)


----------
很酷对吧，我们不需要对每个动画设置同样的时间曲线；因为这是两个单独的动画对象，我们可以单独地控制每个弹簧的属性。这里是一个比例和旋转动画的例子，其比例弹簧使用了一个指数衰减类型的弹簧动作（没有弹性），而旋转动画动作非常有弹性。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%203/jnwdemo6.gif)


----------
这里是另一个同时添加两个动画的例子。这次它组合了一个位置（平移）动画和一个比例变形。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%203/jnwdemo7.gif)


----------
我不知道你如何，但我对于仅仅动画这些色块已经有点无聊了。我认为是时候进入一些使用JNWSpringAnimation来实现弹簧动作动画的真实世界、真实app的例子了。


----------

## <a name="SECTION 4"/>SECTION 4
现在我们已经了解了Core Animation的基础并且使用了优秀的框架JNWSpringAnimation来模仿弹簧系统，是时候来开始写一些真实的示例代码了。

###仿制一个iOS AlertView
重现一个熟悉的界面元素是一个很好的熟悉动画开发的方式。首先，让我们创建我们自己的标准iOS警告视图。这是内置的警告视图的样子。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%204/ios7alert.gif)


----------
在本指南之前的章节中，我解释了分解一个动画的各个组成部分有多么重要，这样你就可以准确地构建它。仅仅说“警告框动画进入屏幕”是不够的，你需要准确地知道发生了什么。让我们来分解这个动画。

1. 屏幕随着渐入的一层半透明灰覆盖变暗。
2. 警告框从完全透明以及比1.0倍大的大小开始，并动画至100%不透明和1.0倍大小。
3. 消失的时候，它会淡出为完全透明并且比例会动画减小到比1.0要小。
4. 阴暗的覆盖层淡出并消失。

在我们进入详细的代码之前，让我们看看我们要完成的警告框是什么样子的。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%204/alertfinal.gif)


----------
首先让我们创建一个简单的有白色背景的应用窗口。这是在应用的delegate类中，并且代码会在app完成启动的时候就立即运行。你可以在Alert View 1 Xcode工程中参考代码。

```objective-c
- (BOOL)application:(UIApplication *)application
    didFinishLaunchingWithOptions:(NSDictionary *)launchOptions {
	
    // Construct the main window for this application
    self.window = [[UIWindow alloc] initWithFrame:[[UIScreen mainScreen] bounds]];

    // All additional code in this example will go right here

    self.window.backgroundColor = [UIColor whiteColor];
    [self.window makeKeyAndVisible];
    return YES;
}
```

在这一步，我们有一个`UIWindow`，其位置和方向可以准确地填充屏幕，并且背景色被设为了白色。如果我们现在立马运行它，它只会在模拟器中（或者你的手机，如果连接了的话）运行一个空的、白色的应用屏幕。现在来创建我们的覆盖层，将其添加到屏幕上，并将透明度设为0.0，因为我们现在不想显示它。

```objective-c
UIView *overlayView = [[UIView alloc] initWithFrame:self.window.bounds];
overlayView.backgroundColor = [UIColor blackColor];
overlayView.alpha = 0.0f;
[self.window addSubview:overlayView];
```

这个覆盖层是一个简单的`UIView`，填充了整个主窗口对象。这意味着它会被放置在窗口的左上角，并且其宽和高会匹配窗口，从而覆盖所有的内容。为了显示我现在有的内容，如果我提高覆盖层的不透明度，这就是看起来的样子。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%204/alert1.png)


----------

现在让我们着手我们的警告框界面，为了便于在这个demo中实现，会仅仅是一个简单的图片而不是一个有label和按钮的纯代码的界面。让我们开始创建这个界面。

```objective-c
CGFloat alertDimension = 250;
CGRect alertViewFrame = CGRectMake(
    self.window.bounds.size.width/2 - alertDimension/2,
    self.window.bounds.size.height/2 - alertDimension/2,
    alertDimension, alertDimension);
UIView *alertView = [[UIView alloc] initWithFrame:alertViewFrame];
```

首先，我们需要创建一个`UIView`对象来作为我们的虚拟警告框，并将其位置设为屏幕的正中央。这是通过将全屏幕的宽和高除以2并减去警告框的宽和高的一半完成的。我喜欢设置一个对象的frame到它完成动画后的最终位置，然后通过操作它的transform属性来调整它的大小或者位置。通过这种方式，当添加动画时，比起重新计算它的`CGRect`frame，我可以移除transform上已完成的操作。这也是为什么如果我想要它变成1.5倍，比起动画它的整个frame，不得不计算在像素层面它的位置和大小是多少，我更喜欢以好的、简单的增加来动画一个视图的transform.scale，而前一种方式是很痛苦的。保持简单。

是时候设置一些关键属性了。

```objective-c
alertView.backgroundColor = [UIColor colorWithPatternImage:
    [UIImage imageNamed:@"alert_box"]];
alertView.alpha = 0.0f;
alertView.transform = CGAffineTransformMakeScale(1.2, 1.2);
alertView.layer.cornerRadius = 10;
```

在这段代码中我们做了四件事：

1. 设置backgroundColor属性为一个图片，这是我创建的看起来像是一个好看、简单的警告框视图的图片。
2. 设置alpha为0，这样警告框就不会立马可见，直到我们想要它动画进入。
3. 通过`CGAffineTransformMakeScale()`函数在变换矩阵中仅仅操作比例值来设置它的transform属性来让比例更大些。
4. 通过设置视图layer的cornerRadius属性来形成圆角。

让我们给它加一点阴影来完成我们警告框的配置。

```objective-c
alertView.layer.shadowColor = [UIColor blackColor].CGColor;
alertView.layer.shadowOffset = CGSizeMake(0, 5);
alertView.layer.shadowOpacity = 0.3f;
alertView.layer.shadowRadius = 10.0f;
[self.window addSubview:alertView];
```

如果我将alpha值调回1.0并移除比例增加的变换然后截屏，这就是它看起来的样子。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%204/alert2.gif)


----------

是时候添加一些动画了。为了警告框的显示，如我之前所说，我们想要覆盖层从完全透明（不可见）变成半透明。我们还想要添加两个动画到警告框中：将不透明度从0.0动画到1.0，以及将比例从大于1.0动画到1.0。这就是iOS 7的警告框做的事情，所以我们要模仿它。

首先让我们处理两个不透明度的动画（覆盖层和警告框视图），因为不透明度动画一般不需要任何高级的弹簧动作，让我们使用一些简单的基于block的`UIView`动画。

```objective-c
// 淡入灰色的封盖层和警告框视图
[UIView animateWithDuration:.3 delay:0 options:UIViewAnimationOptionCurveEaseInOut
    animations:^{
    overlayView.alpha = 0.3f;
    alertView.alpha = 1.0f;
} completion:NULL];
```

我们同时在一个block中动画覆盖层和警告框视图的不透明度。这是因为我想要覆盖层和警告框在同一个动画和同样的时间中呈现给用户，所以为什么不一起动画它们呢？我将持续时间调整到比三分之一秒略少。我是通过尝试很多时间、运行动画、并做出对这个类型动画合适的选择来得出这个时间的。当显示一个重要的信息给用户时，比如警告框，使用一个柔和的动画时间是比较好的，这样实际的过渡会显得更重要。不要太快地显示出来，一个稍缓慢的时间会让信息显得更有分量和势头，且用户应该关注。

现在是时候动画警告框的比例了。这次我确实想用一个更加高级的弹簧动作来让进入比起上面例子中基于block的简单的淡入动画更有趣。在标准iOS警告款视图中，苹果公司没有弹动警告框，而是使用了一个缓慢衰减的动画来慢慢到达最终值。我们会协调弹簧动画的damping和stiffness属性来达到这样的效果。

```objective-c
// Scale-animate in the alert view
JNWSpringAnimation *scale = [JNWSpringAnimation animationWithKeyPath:@"transform.scale"];
scale.damping = 14;
scale.stiffness = 14;
scale.mass = 1;
scale.fromValue = @(1.2);
scale.toValue = @(1.0);

[alertView.layer addAnimation:scale forKey:scale.keyPath];
alertView.transform = CGAffineTransformMakeScale(1.0, 1.0);
```

这个动画的关键路径是“transform.scale”，因为这就是layer上我们想要操作的属性。还记得我们第一次创建这个`UIView`并设其transform属性为`CGAffineTransformMakeScale(1.2, 1.2)`么？这就是我们开始的的fromValue，即当前的比例尺寸，我们要将其动画回1.0的比例，这是正常的尺寸和大小。

这就是现在动画看起来的样子。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%204/alert4.gif)


----------

很好，警告框已经准确地处于屏幕的中间，并且有我想要的动画。现在让我们开发消失的动画。

就如我们起初显示警告框并且确保它不会出现的太快一样，当警告框消失时我们需要思考一下时间应该是什么样的。我不知道你怎么想，但当我关闭一个警告框时，我想要立即回到我之前被打断的内容里去，所以基于此，我总是喜欢以比显示它更快的速度来清楚它。没必要让动画两端的时间保持对称，如果对用户有意义的话，可以调整动画的时间。

```objective-c
// 淡出覆盖层和警告框
[UIView animateWithDuration:.15 delay:0 options:UIViewAnimationOptionCurveEaseInOut
    animations:^{
    overlayView.alpha = 0.0f;
    alertView.alpha = 0.0f;
} completion:NULL];
```

因为我们在回转我们的初始动画，我们现在需要将覆盖层和警告框视图的不透明度退回到0。同样，因为我想要这两个同时动画，所以我将它们放到同一个基于block动画中。注意这个淡出动画的时间只有淡入动画的一般长。我们想要让警告框离开屏幕的时候显得很爽利，让持续时间变短则可以完成这一需求。

接下来我们需要在其淡出到0不透明度的同时缩小警告框。

```objective-c
// 警告框的缩小动画
JNWSpringAnimation *scaleOut = [JNWSpringAnimation
    animationWithKeyPath:@"transform.scale"];
scaleOut.damping = 11;
scaleOut.stiffness = 11;
scaleOut.mass = 1;
scaleOut.fromValue = @(1.0);
scaleOut.toValue = @(0.7);

[alertView.layer addAnimation:scaleOut forKey:scaleOut.keyPath];
alertView.transform = CGAffineTransformMakeScale(0.7, 0.7);
```

内置的iOS警告框会在淡出时缩小一点点，所以我们在这里也做同样的事情。比例值0.7只是我观察内置的警告框后得出的，并且看起来还不错。

这里是完整的动画：


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%204/alertfinal.gif)


----------

### 构建更有想象力的警告框视图

现在我们基本重现了标准的iOS 7警告框视图，让我们娱乐一下，构建一些有不同类型动作的自定义的警告框视图。这里是一个警告框的例子，有着位置和比例的动画，并且其出现和消失的动画都是在屏幕的底部。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%204/alertfrombottom.gif)


----------
为了完成这个动画，支撑警告框的`UIView`和我们之前的例子的设置基本一致，但这一次我们需要更新它的transform属性来进行translation和scale的更改。

```objective-c
alertView.transform = CGAffineTransformMakeScale(.25, .25);
alertView.transform = CGAffineTransformTranslate(alertView.transform, 0, 600);
```

这会设置transform在X和Y方向上都变为0.25的比例，接着会对translation进行更变，将其放置到屏幕的底部。你也可以这样做来达到同样的效果。

```objective-c
CGAffineTransform viewTransform = CGAffineTransformConcat(
    CGAffineTransformMakeScale(.25, .25), CGAffineTransformMakeTranslation(0, 600));
alertView.transform = viewTransform;
```

现在`UIView`就已经被设为在动画开始前比例变小并且处于屏幕的底部了，我们可以开始下一步了。我们会将警告框的比例拉回1.0，并将其位置改回开始的位置，即屏幕的中央。我们依然会同时淡出覆盖层、淡入警告框。

```objective-c
// 同时处理覆盖层和警告框
UIView animateWithDuration:.3 delay:0 options:UIViewAnimationOptionCurveEaseInOut
    animations:^{
    overlayView.alpha = 0.2f;
    alertView.alpha = 1.0f;
} completion:NULL];

// 将警告框的比例动画从0.25变为1.0
JNWSpringAnimation *scale =
    [JNWSpringAnimation animationWithKeyPath:@"transform.scale"];
scale.damping = 12;
scale.stiffness = 12;
scale.mass = 1;
scale.fromValue = @(.25);
scale.toValue = @(1.0);

[alertView.layer addAnimation:scale forKey:scale.keyPath];
alertView.transform = CGAffineTransformScale(CGAffineTransformIdentity, 1.0, 1.0);

// 将Y方向的位置从600动画回0
// 将其放回原来的位置
JNWSpringAnimation *translate = [JNWSpringAnimation
    animationWithKeyPath:@"transform.translation.y"];
translate.damping = 15;
translate.stiffness = 15;
translate.mass = 1;
translate.fromValue = @(600);
translate.toValue = @(0);

[alertView.layer addAnimation:translate forKey:translate.keyPath];
alertView.transform = CGAffineTransformTranslate(alertView.transform, 0, 0);
```

如果你细心的话就会发现这两个动画的弹簧属性非常的相似。它们都有匹配damping的stiffness，意味着它是一种没有弹性的指数衰减类型的动作。然而scale动画的值比translation动画的值要低，意味着scale会慢一点点。这是因为我想要所有的动画大致在同时结束，因为translation动画比scale动画移动更多的值，所以它需要移动的快一点点来匹配scale动画的速度。这只会略微被注意到，但如果某个动画比另一个结束得早，绝对会看起来很奇怪。

对于收回的动画，警告框会收缩并且跳回屏幕的底部。如其他例子一样，我想要警告框有一个比起显示到用户面前时更快的动作。

```objective-c
// 一起淡化覆盖层和警告框
[UIView animateWithDuration:.2 delay:0 options:UIViewAnimationOptionCurveEaseInOut
    animations:^{
    overlayView.alpha = 0.0f;
    alertView.alpha = 0.0f;
} completion:NULL];

// 动画将警告框的比例从1.0变为0.5
JNWSpringAnimation *scale =
    [JNWSpringAnimation animationWithKeyPath:@"transform.scale"];
scale.damping = 17;
scale.stiffness = 17;
scale.mass = 1;
scale.fromValue = @(1.0);
scale.toValue = @(0.5);

[alertView.layer addAnimation:scale forKey:scale.keyPath];
alertView.transform = CGAffineTransformScale(CGAffineTransformIdentity, 0.5, 0.5);

// 动画将位置从0变回屏幕底部
JNWSpringAnimation *translate = [JNWSpringAnimation
    animationWithKeyPath:@"transform.translation.y"];
translate.damping = 4;
translate.stiffness = 4;
translate.mass = 1;
translate.fromValue = @(0);
translate.toValue = @(600);

[alertView.layer addAnimation:translate forKey:translate.keyPath];
alertView.transform = CGAffineTransformTranslate(alertView.transform, 0, 600);
```

警告框消失的动画速度和之前非常的不一样：translation动画比scale动画要慢很多。原因是当translation动画移动得scale动画慢时，你会在警告框落回屏幕底部前看到更多的scale动画。我认为这种方式是一个很好的视觉效果，因为我加强了警告框退出的效果。

如果我们加快translation动画，使其damping和stiffness值和scale动画一样，这就是它看起来的样子。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%204/alert2fast.gif)


----------
与慢一点的过渡相比较...


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%204/alertfrombottom.gif)


----------

现在让我们为我们的警告框视图创建一个不同类型的动作，从屏幕的中央出来并带有一些弹性动画来获取用户的注意。这就是它看起来的样子。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%204/alert3center.gif)


----------
这是一个更简单的动画，因为我们只动画了警告框transform的一个属性，即scale。我们设置它的初始scale为0来建立我们的警告框视图。

```objective-c
lofter 2016/6/30 9:15:45
alertView.transform = CGAffineTransformMakeScale(0, 0);
```

和之前一样，我们想要给覆盖层和警告框一个淡化的动画，不过这一次我们会用弹性的出现来动画警告框的scale。

```objective-c
JNWSpringAnimation *scale = [JNWSpringAnimation
    animationWithKeyPath:@"transform.scale"];
scale.damping = 32;
scale.stiffness = 450;
scale.mass = 2.4;
scale.fromValue = @(0);
scale.toValue = @(1.0);

[alertView.layer addAnimation:scale forKey:scale.keyPath];
alertView.transform = CGAffineTransformScale(CGAffineTransformIdentity, 1.0, 1.0);
```

这里的弹簧的damping、stiffness和mass属性和我们用来创建平稳衰减到最终值的动作的属性非常不同。这些值会一直使用JNWSpringAnimation Mac app直到它们有了正确地弹性，不太快也不太强力。

觉得使用JNWSpringAnimation和自然的动作来构建动画界面和棒吗？非常好，是时候开始构建一些在第一节里显示的动画例子了。


## <a name="SECTION 5"/>SECTION 5
### 创建Jeff Broderick的地图动画
在本指南的前面，我提到了一些Jeff Broderick设计并发布到Dribbble的很棒的动画。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%205/map.gif)


----------
如我所说，这里有一些不懂得动画。首先，当地图的图标被点击时，应用的主界面（包括导航栏）同时有不透明度和比例的动画来让其淡出到黑色的背景中并且有一点点缩小。同时，地图伴随着不透明度和比例的动画显著地显现到界面的前面来。地图还会向屏幕上方移动一点，就像过度动画一样。地图图标会保持在原位。

在我们编码重现Jeff的动画前，先看一眼我们创建的最终的动画效果。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%205/map2.gif)


----------
我们通过一些简单的`UIImageView`和`UIButton`来重新开发这个动画，因为它们可以准确地得到动画的感觉，但在真实的地图中这会是一个真实的可伸缩的地图视图。

首先，让我们添加代表app主界面的图片。

```objective-c
// 添加app的主背景图片
self.appBackground = [[UIImageView alloc] initWithFrame:CGRectMake(0, 20,
    self.window.bounds.size.width, 548)];
self.appBackground.image = [UIImage imageNamed:@"app-bg"];
[self.window addSubview:self.appBackground];
```

我们添加了一个图片属性为“app-bg@2x.png”的简单的`UIImageView`。app的运行时很聪明，你只用写“app-bg”它就会在app包的图片资源中找到“app-bg@2x.png”。这个视图被添加为类的@property了，这样我们就可以在之后的代码中引用它。这里显示了如何声明一个@porperty。

```objective-c
@property (assign) UIImageView *appBackground;
```

这个@property既可以定义在类的.h文件的@interface中，也可以定义在.m实现文件的@interface块中来让其私有。在苹果的开发者网站的Objective-C指南中可以阅读更多关于程序的属性的内容。

最后，我们将`UIImageView`作为主屏幕的一个子视图添加进去。这是一个快速的模型，否则我会创建另一个`UIViewController`的子类来装载我们的UI代码。

如果我构建并运行，这就是app目前看起来的样子。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%205/map1.png)


----------
非常棒！现在让我们添加地图，它会是透明的，并且会伴随着变化开始。我们会在主应用图片后立即添加它，因为我们想要最后添加图标按钮，这样它就会使z轴上最高的，也就是在其他视图的顶部。

```objective-c
// 添加地图视图
self.mapView = [[UIImageView alloc] initWithFrame:CGRectMake(0, 62,
    self.window.bounds.size.width, 458)];
self.mapView.image = [UIImage imageNamed:@"map-arrow"];
self.mapView.alpha = 0.0f;
self.mapView.transform = CGAffineTransformMakeTranslation(0, 30);
self.mapView.transform = CGAffineTransformScale(self.mapView.transform, 1.1, 1.1);
[self.window addSubview:self.mapView];
```

想在Swift下开发这些例子么？这里就是Swift下的上面Objective-C的代码。

```swift
self.mapView =
    UIImageView(frame: CGRectMake(0, 62, self.window!.bounds.size.width, 458))
self.mapView!.image = UIImage(named: "map-arrow")
self.mapView!.alpha = 0.0
self.mapView!.transform = CGAffineTransformMakeTranslation(0, 30)
self.mapView!.transform = CGAffineTransformScale(self.mapView!.transform, 1.1, 1.1)
self.window!.addSubview(self.mapView!)
```

地图视图的frame开始会在左上角，但会距离顶部62像素，这样就会正好位于我们要添加的地图按钮的下方一点点。图片属性被设为“map-arrow”，这只是一个地图图片，我将其和一个箭头放在一起，来模仿Jeff在他的动画中所涉及的样子。

一开始，这个视图会是完全透明的，所以alpha属性被设为0。有两个变换添加到视图中：第一个将视图往下移动30像素，第二个将其从正常尺寸拉伸到1.1倍。

这里是它现在看起来的样子，我注视了alpha那一行，这样我们就可以看到地图在哪。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%205/map2.png)


----------
这看起来是动画开始的准确位置了。

现在让我们添加我们的图标按钮。

```objective-c
// 添加图标
UIButton *icon = [UIButton buttonWithType:UIButtonTypeCustom];
[icon setImage:[UIImage imageNamed:@"map-icon"] forState:UIControlStateNormal];
[icon addTarget:self action:@selector(didTapMapIcon:)
    forControlEvents:UIControlEventTouchUpInside];
[icon setFrame:CGRectMake(self.window.bounds.size.width - 49, 19, 49, 44)];
[self.window addSubview:icon];
```

这是一个非常典型的添加图标按钮的方式。`UIButton`类有一个便利的方式来构建一个按钮：+buttonWithType:类方法。我将按钮类型设为`UIButtonTypeCustom`，意味着没有默认的风格会被设置，完全取决于我。这是一种实用的简单图标按钮，没有边界和其他怪异的风格需要移除。有点类似于CSS中对按钮进行重置。

接下来我设置按钮的图片为我app包中的“map-icon”图片。参数`UIControlStateNormal`意味着这个图标会在常规、默认状态下为显示按钮的图片。你可以用多种图片多次设置这个值，只要你想要改变图标，比如`UIControlStateHighlighted`状态。默认情况下，当一个`UIButton`被点击时，iOS会自动暗化图片。

最后，我让按钮可被点击并且会调用我定义的一个方法。`self`参数值意味着我想要这个按钮调用其被点击时所在的类，而`@selector(didTapMapIcon:)`是我想要调用的Objective-C方法。接下来我通过设置frame将按钮放置在准确的位置。

让我们看看现在app的样子，地图的alpha值被设为了0，所以它是不可见的。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%205/map3.png)


----------
好，现在我们将动画的所有主要部件都添加到界面上了，是时候在地图图标被点击时添加一些动画了。

首先，我们需要实现按钮被点击时被调用的方法。这里是不含任何内容的方法看起来的样子。

```objective-c
- (void)didTapMapIcon:(id)sender {
    // 暂时没有任何内容!
}
```

它会在用户点击地图按钮时被调用，因为我们之前通过 -addTarget:action:forControlEvents:方法进行了设置。

所以，按照逻辑，当你点击按钮时，下面两种事件之一会发生：将地图动画到界面上，或者如果地图已经可见了，则将地图动画出界面。我们可以检查我们的界面元素并查看它们的位置来决定我们应该做什么，但那太麻烦了，所以让我们通过一个简单的作为类@property的 BOOL 变量来跟踪状态。在这个文件的顶部我添加了一个名为mapShowing的BOOL变量来管理我们是需要打开还是关闭地图视图。这个属性会放置在我们按钮方法的下面，而我们添加的其他属性是我们界面的主视图。

```objective-c
@interface DTCAppDelegate ()

- (void)didTapMapIcon:(id)sender;

@property (assign) BOOL mapShowing;

@property (strong) UIImageView *appBackground;
@property (strong) UIImageView *mapView;

@end
```

现在，回到我们的按钮点击方法，我们需要在这里添加一些逻辑，来检查地图是显示还是不显示，然后将变量设为相反的。

```objective-c
- (void)didTapMapIcon:(id)sender {
	
if (self.mapShowing) {	
    self.mapShowing = NO;

    // 当地图已经可见时要运行的代码
} else {
    self.mapShowing = YES;

    // 当地图不可见时要运行的代码
}
```

让我们从`else`的情况开始，此时地图未显示，我们需要进行不透明度的动画。我们需要做的是淡出主app背景一点点然后淡入地图。主app背景的淡出速度会比地图的淡入速度慢一点点，这样地图会更显眼。

```objective-c
[UIView animateWithDuration:.5 delay:0 
    options:UIViewAnimationOptionCurveEaseInOut|UIViewAnimationOptionBeginFromCurrentState 
    animations:^{
    self.appBackground.alpha = 0.3f;
} completion:NULL];
		
[UIView animateWithDuration:.15 delay:0
    options:UIViewAnimationOptionCurveEaseInOut|UIViewAnimationOptionBeginFromCurrentState 
    animations:^{
	self.mapView.alpha = 1.0f;
} completion:NULL];
```

你可能注意到了放置在这个基于block的`UIView`动画方法总的options依据里的巨大的参数。这实际上是两个选项通过二进制 | 操作组合在一起的：`UIViewAnimationOptionCurveEaseInOut`用来定义动画的淡入淡出，`UIViewAnimationOptionBeginFromCurrentState `会从其alpha的当前值开始动画，这样即使动画被打断了，它也不会跳回开始动画前的初始值。这对像这样被用户动作管理的动画非常重要，因为你不知道用户会不会在动画发生后不停点击按钮，而且你肯定不想在动画完成后都没做任何事。

当然，调整主app界面和地图的不透明度并没有准确地完成我们的动画，因为我们还需要动画地图的比例和位置，这样它才能够到达它最终的位置和尺寸。对于主app界面，我们只会稍微动画其比例。

即使这些动画可以通过一个淡出动画曲线来完成，我也想使用含有相同damping和stiffness值得弹簧动画，这样我就可以减缓速度。这里不会有弹性，只是非常平滑的过渡。

```objective-c
CGFloat dampingStiffness = 16.0f;

// 主app背景的比例动画
JNWSpringAnimation *scale =
    [JNWSpringAnimation animationWithKeyPath:@"transform.scale"];
scale.damping = dampingStiffness;
scale.stiffness = dampingStiffness;
scale.mass = 1;
scale.fromValue = @([[self.appBackground.layer.presentationLayer
    valueForKeyPath:scale.keyPath] floatValue]);
scale.toValue = @(0.9);

[self.appBackground.layer addAnimation:scale forKey:scale.keyPath];
self.appBackground.transform =
    CGAffineTransformScale(CGAffineTransformIdentity, .9, .9);

```

我将damping和stiffness值设为一个`CGFloat`变量，这样我就可以更简单地调整它们而不用一次更新两个值。

这个block代码中的一个主要的与其他例子不同的改变是比例动画的fromValue没有被设为一个常量，而是设为[[self.appBackground.layer.presentationLayer valueForKeyPath:scale.keyPath] floatValue]。这是什么意思呢？如果你一块块拆开，这些事要发生的事：

* 我会使用self.appBackground来访问这个类的appBackground属性
* 我会获取到这个视图的`CALayer`对象
* 我在layer上获取presentationLayer属性，通过它来获取特殊的presentation model layer，让我们看到动画改变时的值
* 当我有了presentationLayer后，我会调用 -valueForKeyPath: 来取得变换的比例部分的当前值。（scale.keyPath = @"transform.scale"）
* 当我最后有了当前的比例值后，它不是JNWSpringAnimation需要的数据格式，所以我使用了floatValue。

记得之前我提到过在动画中layer上的很多属性值都不会改变么？以及presentation model layer是Core Animation用来存储动画发生过程中精确的变更值的？我们需要获取比例变换的当前值，这样就可以在当前任何点开始动画（记住如果用户很开心地不停点击，我们不想要动画重新开始！）。我们需要获取特殊的显示层来查看值。然后我们使用它作为我们动画的fromValue，这样他就能始终正常工作，无论fromValue是我们为视图设置的正常的、未触摸的比例值，还是动画中的某个值。如果我们不通过presentationLayer获取它，这个值在动画中就始终不会正确，直到动画结束。

我们不仅仅需要动画主app背景，还需要动画地图，将比例降回1.0,，并且通过过渡移动到屏幕上。让我们现在做。

```objective-c
// 地图有两个分开的动画，一个用于位置，一个用于比例
JNWSpringAnimation *mapScale =
    [JNWSpringAnimation animationWithKeyPath:@"transform.scale"];
mapScale.damping = dampingStiffness;
mapScale.stiffness = dampingStiffness;
mapScale.mass = 1;
mapScale.fromValue =
    @([[self.mapView.layer.presentationLayer valueForKeyPath:mapScale.keyPath] floatValue]);
mapScale.toValue = @(1.0);

[self.mapView.layer addAnimation:mapScale forKey:mapScale.keyPath];
self.mapView.transform = CGAffineTransformScale(CGAffineTransformIdentity, 1, 1);

JNWSpringAnimation *mapTranslate =
    [JNWSpringAnimation animationWithKeyPath:@"transform.translation.y"];
mapTranslate.damping = dampingStiffness;
mapTranslate.stiffness = dampingStiffness;
mapTranslate.mass = 1;
mapTranslate.fromValue =
    @([[self.mapView.layer.presentationLayer valueForKeyPath:mapTranslate.keyPath] floatValue]);
mapTranslate.toValue = @(0);

[self.mapView.layer addAnimation:mapTranslate forKey:mapTranslate.keyPath];
self.mapView.transform = CGAffineTransformTranslate(self.mapView.transform, 0, 0);
```

这里没有什么很复杂的，除了获取当前变化的值来从其开始，如前面的动画一样。我在这也使用了damping和stiffness变量，这样所有的动画都感觉是同一个类型的动作。

锁着这是一块正统的代码，好在其非常简单，而且现在你应该习惯了JNWSpringAnimation代码块的样子。这是目前动画看起来的样子。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%205/map3.gif)


----------

现在是时候添加这个界面的其他动画了，即当用户点击地图图标且地图可见时，我们想要将其淡出并且将主app背景放回到前面。因为它和我们刚才展示的动画除了开始和结束值外完全一样，这里就直接放一个大块来解释发生了什么。

```objective-c
if (self.mapShowing) {
		
    self.mapShowing = NO;

    // 再次使用这些动画相同的damping和stiffness
    // 这样我们就可以获取CGFloat形式的值。注意这个值会高一点
    // 意味着动画会花费更少的时间（在匹配此damping和stiffness的弹簧动画下）。
    // 少时间是好的，因为我们要回到界面的默认状态，而此时用户只想让地图赶紧消失。
    CGFloat dampingStiffnessOut = 24.0f;

    // 再说一次，从当前状态开始很重要，这样用户点击按钮时就不会抽动
    [UIView animateWithDuration:.5 delay:0 
        options:UIViewAnimationOptionCurveEaseInOut|UIViewAnimationOptionBeginFromCurrentState
        animations:^{
    	self.appBackground.alpha = 1.0f;
    } completion:NULL];

    [UIView animateWithDuration:.3 delay:0
        options:UIViewAnimationOptionCurveEaseInOut|UIViewAnimationOptionBeginFromCurrentState 
        animations:^{
    	self.mapView.alpha = 0.0f;
    } completion:NULL];

    // 地图有两个分开的动画，一个是位置一个是比例。
    // 我们通过presentationLayer获取@“transform.scale”的变化的值，如之前的例子一样
    JNWSpringAnimation *mapScale =
        [JNWSpringAnimationanimationWithKeyPath:@"transform.scale"];
    mapScale.damping = dampingStiffnessOut;
    mapScale.stiffness = dampingStiffnessOut;
    mapScale.mass = 1;
    mapScale.fromValue =
        @([[self.mapView.layer.presentationLayer
        valueForKeyPath:mapScale.keyPath] floatValue]);
    mapScale.toValue = @(1.1);

    [self.mapView.layer addAnimation:mapScale forKey:mapScale.keyPath];
    self.mapView.transform =
        CGAffineTransformScale(CGAffineTransformIdentity, 1.1, 1.1);

    JNWSpringAnimation *mapTranslate =
        [JNWSpringAnimation animationWithKeyPath:@"transform.translation.y"];
    mapTranslate.damping = dampingStiffnessOut;
    mapTranslate.stiffness = dampingStiffnessOut;
    mapTranslate.mass = 1;
    mapTranslate.fromValue =
        @([[self.mapView.layer.presentationLayer
        valueForKeyPath:mapTranslate.keyPath] floatValue]);
    mapTranslate.toValue = @(30);

    [self.mapView.layer addAnimation:mapTranslate forKey:mapTranslate.keyPath];
    self.mapView.transform = CGAffineTransformTranslate(self.mapView.transform, 0, 30);

    // 主app背景的比例动画。我们将其动画回1.0倍
    JNWSpringAnimation *scale =
        [JNWSpringAnimation animationWithKeyPath:@"transform.scale"];
    scale.damping = dampingStiffnessOut;
    scale.stiffness = dampingStiffnessOut;
    scale.mass = 1;
    scale.fromValue =
        @([[self.appBackground.layer.presentationLayer
        valueForKeyPath:@"transform.scale.x"] floatValue]);
    scale.toValue = @(1.0);

    [self.appBackground.layer addAnimation:scale forKey:scale.keyPath];
    self.appBackground.transform =
        CGAffineTransformScale(CGAffineTransformIdentity, 1.0, 1.0);

}
```

这里是完整的、最终的动画的样子。如果你想一个疯子一样点击，会发现它确实是从当前值开始动画的，而且不会抽动。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%205/map4.gif)


----------
这很有意思！现在让我们去转眼有些断断续续的动画。

### 构建Jakub Antalik的音乐播放器
Jakub是斯洛伐克的一名出色的设计师，已经设计了一些经常发布到Dtibbble去的非常有创造力的界面。其中一个作品非常打动我，那是一个很有趣的例子，证明了界面上每次操作一个元素的断断续续的动画是如何抓住用户的眼球的。在本指南的早期我展示了一个他设计的音乐播放器，含有一些很酷的内置动画，这里我们再看一下。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%205/music.gif)


----------
所以这里他明显使用到的技术是什么？他操纵了动画的开始时间。通过让每个元素比另一个元素慢一点动画到屏幕上的位置，并按照行的顺序操作屏幕上的每一个元素，就形成了一个非常整齐的波浪效果，感觉就像每个元素都被前一个元素用橡皮筋带动的一样。

让我们重建他音乐播放器概念的第二个屏幕：歌曲列表。

首先，我们需要重建设计来切片元素并且尽可能整齐地分开动画它们。我拉出我选择的设计工具：Photoshop，然后开始工作。musicplayer.psd文件是放置该设计文件的地方，如果你喜欢的话可以打开来检出它。我不会详细说明如何用Photoshop创建这个设计，但文件和设计都足够简单和直接。

这里是我重建的第二个屏幕的歌曲列表。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%205/musicplayer.png)


----------

如果你仔细观察原始的动画，会发现有8个分开动画的不同元素。

1. 黑色箭头和“Dance Club”文本
2. “Ministry of Fun”文本
3. “Add a Song”按钮
4. 五首歌对应的五行

这8个元素（或元素组，因为箭头和“Dance Club”文本是一起动画的）是通过不同的开始时间递进进入视图的，这就是我们要在动画中获取的非常酷的波浪感效果。

首先我们整理一下计划。我需要做的是分开添加这些元素到界面上，这样我就可以分开动画它们了。如果这是一个真实的app，有着真实流入的数据，这个界面最可能是一个`UITableView`或者`UICollectionView`来获取一个好的、结构化的展示行的方式。从高层面来概括这两个视图类型的话，就是你实现你需要定义的它们的接口方法，来返回一些数据到界面上，比如返回行高的方法，或者返回一个只有一行的视图的方法。因为我们没有数据，而且我的主要目的是演示如何构建动画，我就仅仅是保存一些Photoshop里设计的图片并手动将这些图片添加到界面上去，从顶部的箭头和“Dance Club”文本开始。

```objective-c
// 定义一个变量来获取屏幕的宽度，我们会经常用到这个值。
CGFloat windowWidth = self.window.bounds.size.width;

// 将背景添加到界面上
UIImageView *backgroundView = [[UIImageView alloc] initWithFrame:self.window.bounds];
backgroundView.image = [UIImage imageNamed:@"background"];
[self.window addSubview:backgroundView];

// 添加箭头和文本
UIImageView *arrowView =
    [[UIImageView alloc] initWithFrame:CGRectMake(0, 0, windowWidth, 45)];
arrowView.image = [UIImage imageNamed:@"arrow"];
[self.window addSubview:arrowView];
```

这里没什么特别的，只是简单地添加一些视图到我们原型的主屏幕上。名为@“background”的图片是大的渐变的图片，作为其他视图的背景。@“arrow”图片是用Photoshop做出来的包含箭头和“Dance Club”文本的图片，因为我会同时动画它们，所以将它们简单地放在一个图片里。

这里是目前界面看起来的样子。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%205/music1.png)


----------
现在让我们添加更多的视图！

```objective-c
// “Ministry of Fun”图片
UIImageView *ministryView =
    [[UIImageView alloc] initWithFrame:CGRectMake(0, 57, windowWidth, 28)];
ministryView.image = [UIImage imageNamed:@"ministry"];
[self.window addSubview:ministryView];

// 添加一个歌曲按钮
UIButton *addButton = [UIButton buttonWithType:UIButtonTypeCustom];
[addButton setImage:[UIImage imageNamed:@"add-button"] forState:UIControlStateNormal];
[addButton setImage:[UIImage imageNamed:@"add-button-pressed"]
    forState:UIControlStateHighlighted];
[addButton setFrame:CGRectMake(0, 102, windowWidth, 45)];
[self.window addSubview:addButton];
```

我添加“Ministry of Fun”图片视图（使用我用Photoshop分割出来的PNG图片）到界面上然后为“Add a Song”按钮创建一个`UIButton`。我本可以懒一点，不将按钮做成一个真的`UIButton`，而是使用一个`UIImageView`，但我想演示如何为一个自定义的`UIButton`设置点击的和普通的图片。只需要调用同样的一个 -setImage:forState:方法，但给它传输不同的属性。你可以随便调用它来设置不同的状态属性，来覆盖用户对按钮的每一个可能的操作。接着我设置按钮的位置并将它添加到界面上。

这里是目前状态的界面，以及点击按钮时不同状态的演示。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%205/musicbutton.gif)


----------
我们`UIControlStateHighlighted`状态的图片只是将白色边框换成了白色的填充。

现在让我们添加我们的行。它们也都是`UIImageView`，所以也只用直接在背景图片上放置就可以了。

```objective-c
// Katy Perry 行
UIImageView *firstRow =
    [[UIImageView alloc] initWithFrame:CGRectMake(0, 170, windowWidth, 80)];
firstRow.image = [UIImage imageNamed:@"1st-row"];
[self.window addSubview:firstRow];

// Shakira 行
UIImageView *secondRow =
    [[UIImageView alloc] initWithFrame:CGRectMake(0, 170+80, windowWidth, 80)];
secondRow.image = [UIImage imageNamed:@"2nd-row"];
[self.window addSubview:secondRow];

// Pitbull 行
UIImageView *thirdRow =
    [[UIImageView alloc] initWithFrame:CGRectMake(0, 170+160, windowWidth, 80)];
thirdRow.image = [UIImage imageNamed:@"3rd-row"];
[self.window addSubview:thirdRow];

// Lana del Rey 行
UIImageView *fourthRow =
    [[UIImageView alloc] initWithFrame:CGRectMake(0, 170+240, windowWidth, 80)];
fourthRow.image = [UIImage imageNamed:@"4th-row"];
[self.window addSubview:fourthRow];

// HEX 行
UIImageView *fifthRow =
    [[UIImageView alloc] initWithFrame:CGRectMake(0, 170+320, windowWidth, 80)];
fifthRow.image = [UIImage imageNamed:@"5th-row"];
[self.window addSubview:fifthRow];
```

你可能注意到每一行frame的Y坐标（垂直位置）都有一个小方程式。每一行都是80px高，所以放置它们每一行的时候我都在Y坐标上加了80。我也可以使用Auto Layout来做，但对这个例子来说就有点过于复杂了。

这里是在添加动画前的样子。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%205/music2.png)


----------
但等一下，我们并不想要在第一次进入的看到这样的界面。这次练习的目的在于让每个元素都动画到它们的位置上，也就是说它们不应该立即出现在它们的最终位置。我要做的是从屏幕的右边开始每一个元素，然后我会让每个元素的左边动画到屏幕的左边，来到最终的位置。

让我们回到我们的视图设置代码并修改每个元素的frame，这样它们的X轴坐标就不再是0了，而是屏幕的宽度。这样就会让每个元素的左边界并齐屏幕的右边界，用户就看不到了。

```objective-c
// 添加箭头和顶部的文字
UIImageView *arrowView =
   [[UIImageView alloc] initWithFrame:CGRectMake(windowWidth, 0, windowWidth, 45)];
arrowView.image = [UIImage imageNamed:@"arrow"];
[self.window addSubview:arrowView];

// Ministry of Fun 文字
UIImageView *ministryView =
    [[UIImageView alloc] initWithFrame:CGRectMake(windowWidth, 57, windowWidth, 56/2)];
ministryView.image = [UIImage imageNamed:@"ministry"];
[self.window addSubview:ministryView];

// Add a Song 按钮
UIButton *addButton = [UIButton buttonWithType:UIButtonTypeCustom];
[addButton setImage:[UIImage imageNamed:@"add-button"]
    forState:UIControlStateNormal];
[addButton setImage:[UIImage imageNamed:@"add-button-pressed"]
    forState:UIControlStateHighlighted];
[addButton setFrame:CGRectMake(windowWidth, 102, windowWidth, 45)];
[self.window addSubview:addButton];

// Katy Perry 行
UIImageView *firstRow =
    [[UIImageView alloc] initWithFrame:CGRectMake(windowWidth, 170, windowWidth, 80)];
firstRow.image = [UIImage imageNamed:@"1st-row"];
[self.window addSubview:firstRow];

// Shakira 行
UIImageView *secondRow =
    [[UIImageView alloc] initWithFrame:CGRectMake(windowWidth, 170+80, windowWidth, 80)];
secondRow.image = [UIImage imageNamed:@"2nd-row"];
[self.window addSubview:secondRow];

// Pitbull 行
UIImageView *thirdRow =
    [[UIImageView alloc] initWithFrame:CGRectMake(windowWidth, 170+160, windowWidth, 80)];
thirdRow.image = [UIImage imageNamed:@"3rd-row"];
[self.window addSubview:thirdRow];

// Lana del Rey 行
UIImageView *fourthRow =
    [[UIImageView alloc] initWithFrame:CGRectMake(windowWidth, 170+240, windowWidth, 80)];
fourthRow.image = [UIImage imageNamed:@"4th-row"];
[self.window addSubview:fourthRow];

// HEX 行
UIImageView *fifthRow =
    [[UIImageView alloc] initWithFrame:CGRectMake(windowWidth, 170+320, windowWidth, 80)];
fifthRow.image = [UIImage imageNamed:@"5th-row"];
[self.window addSubview:fifthRow];
```

你可以想象一下现在所有元素都移动到屏幕的右边去的界面样式，现在只显示了背景图片。

现在所有内容都在屏幕外并且准备好动画了，策略是让每个元素都动画到左边，一次一个，每个都有所延迟，这样就会产生一种波浪的感觉。为了好玩，我们试试使用基于block的`UIView`动画方法来让我们的元素动画到屏幕上。

这里是第一个动画block，我们会将箭头和“Dance Club”图片滑动到左边。

```objective-c
[UIView animateWithDuration:1.1 delay:0 usingSpringWithDamping:0.3
    initialSpringVelocity:0 options:0 animations:^{
    [arrowView setFrame:CGRectMake(0, 0, windowWidth, 45)];
} completion:NULL];
```

这个基于block的动画有1.1秒的持续时间和0.3的弹簧阻尼。持续时间是动画完成需要的时间，而阻尼是iOS 7在`UIView`动画方法中提供的一个弹簧属性，用来控制弹簧的弹力。JNWSpringAnimation提供了三个属性来控制弹簧的物理性质，但Apple值提供了一个，即damping属性。damping需要时一个0到1之间的值，越接近0，弹簧动作就越有弹性，越接近1，就越没有弹性，直到完全没有弹性，变成一个平滑的淡入。

让我们看看这个duration和damping值产生的动作。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%205/musicbutton2.gif)


----------
恩，有点不太对。动画太快也太跳跃了。这种类型的弹性动画带来了一些焦虑。这是一个关于仅仅使用一个弹簧动画并不能提升你的app整体用户体验的很好的例子。每种类型的动画都给你的用户带来了一些感受，而这个带来了错误地感受。

让我们将持续时间提升到2.1秒并看看感觉。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%205/musicbutton3.gif)


----------
比起Jakub的原始动画，这个又太弹了，我们的damping值也需要调整。让我们将damping从0.3提升到0.6，如我之前所说，它更靠近1这个不弹的值。我们还是需要一点弹性，现在让我们来看看它怎么样了。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%205/musicbutton3.gif)


----------
好了，不是太坏。你可以发现当你使用iOS 7提供的弹簧动画方法时，它直接提供了一些值来获取你想要的感觉。NSWSpringAnimation给出的弹簧属性更容易理解，至少对我来说是这样，因为它们都操作了弹簧动作方程的不同属性。iOS 7的基于block的动画中的damping值实际上是一个解释值，这意味着苹果无论获取到你输入的什么值，都会做一些复杂的计算来操作这个值并将其放入弹簧动作方程式中。你可以说苹果操作了这个值，因为它在0和1之间改变弹性。而在实际的弹簧动作方程中，动作的时间（它到达平衡点或者最终位置的时间）是由弹簧的其他属性决定的，它不是你去设置然后强制弹簧遵循的。苹果的动画方法有一个你需要设置的持续时间，所以你在以一种并非完全遵循物理法则管理下的弹簧动作。这就是为什么我倾向于用JSWSpringAniamtion（或者Facebook Pop，我会马上提及），因为它们有着更加自然、逼真的弹簧动画。

现在，让我们从上到下动画屏幕上的其他元素。每个都需要比前一个开始得稍微慢一点。同时我想要控制app启动后动画开始的时间，来看看我如何管理。

```objective-c
CGFloat initialDelay = 1.0f;
CGFloat stutter = 0.3f;

// 动画箭头图片
[UIView animateWithDuration:2.1 delay:initialDelay
    usingSpringWithDamping:0.6 initialSpringVelocity:0 options:0 animations:^{
    [arrowView setFrame:CGRectMake(0, 0, windowWidth, 45)];
} completion:NULL];

// 动画Ministry of Fun文字
[UIView animateWithDuration:2.1 delay:initialDelay + (1 * stutter)
    usingSpringWithDamping:0.6 initialSpringVelocity:0 options:0 animations:^{
    [ministryView setFrame:CGRectMake(0, 57, windowWidth, 28)];
} completion:NULL];

```

我设置了两个`CGFloat`变量，一个initialDelay值来存储延迟时间，一个stutter来存储每个动画之间细微的延迟。这个数字对我们动画效果整体的感觉和流动感都非常重要。动画之间太长的延时会让他们觉得不连贯，太短就不足以形成我们想要构建的波浪效果。

回到代码：第一个动画的delay属性就是initialDelay变量的值，因为这是来到屏幕上的第一个动画。第二个动画block的delay值为initialDelay+（1*stutter）。这表示它会等待开始的延迟时间，然后会等待stutter值乘以1的时间。接下来的所有动画都会遵循这个公式作为延时，并且每次都会加1倍stutter。这可以确保他们的动画之间都是同样的延时。

这里是现在看起来的样子。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%205/musicbutton5.gif)


----------

我觉得这个看起来不错。老实说，只动画两个元素很难看出波浪效果是不是好的，因为你无法获取一个整体的真实感受，除非动画一系列的元素。所以让我们动画屏幕上的其他元素。

```objective-c
[UIView animateWithDuration:2.1 delay:initialDelay + (2 * stutter)
    usingSpringWithDamping:0.6 initialSpringVelocity:0 options:0 animations:^{
    [addButton setFrame:CGRectMake(0, 102, windowWidth, 45)];
} completion:NULL];

[UIView animateWithDuration:2.1 delay:initialDelay + (3 * stutter)
    usingSpringWithDamping:0.6 initialSpringVelocity:0 options:0 animations:^{
    [firstRow setFrame:CGRectMake(0, 170, windowWidth, 80)];
} completion:NULL];

[UIView animateWithDuration:2.1 delay:initialDelay + (4 * stutter)
    usingSpringWithDamping:0.6 initialSpringVelocity:0 options:0 animations:^{
    [secondRow setFrame:CGRectMake(0, 170+80, windowWidth, 80)];
} completion:NULL];

[UIView animateWithDuration:2.1 delay:initialDelay + (5 * stutter)
    usingSpringWithDamping:0.6 initialSpringVelocity:0 options:0 animations:^{
    [thirdRow setFrame:CGRectMake(0, 170+160, windowWidth, 80)];
} completion:NULL];

[UIView animateWithDuration:2.1 delay:initialDelay + (6 * stutter)
    usingSpringWithDamping:0.6 initialSpringVelocity:0 options:0 animations:^{
    [fourthRow setFrame:CGRectMake(0, 170+240, windowWidth, 80)];
} completion:NULL];

[UIView animateWithDuration:2.1 delay:initialDelay + (7 * stutter)
    usingSpringWithDamping:0.6 initialSpringVelocity:0 options:0 animations:^{
    [fifthRow setFrame:CGRectMake(0, 170+320, windowWidth, 80)];
} completion:NULL];
```

现在我们动画了所有的元素到位置上了，让我们看看效果。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%205/musicbutton7.gif)


----------
对我来说感觉还不太对。动画的延时还是有点太长了，破坏了想要的波浪感。看起来一点也没有流动感。让我们降低延时，把stutter变量的值从0.3降为0.15来看看效果。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%205/musicbutton8.gif)


----------
很接近了，但我认为我们可以再缩小一点点延迟时间来让它更有天然的流动感，就像每个元素都牵引了下一个。让我们将stutter变量降为0.6。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%205/musicbutton9.gif)


----------
现在我们有些成果了。我认为它看起来很棒并且有非常好的波浪动作。让我们和Jakub原始的动作做一些比较。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%205/music.gif)


----------
看起来我们匹配得很接近！所以从这个例子中学到了什么呢？

* 基于block的`UIView`动画方法中的弹簧的damping值是一个抽象值，对获取一个好的感觉并没有什么用。这就是为什么我喜欢用真实的弹簧动作（不需要设置持续时间的），比如JSWSpringAnimation提供的那种。
* 当实现一个像这个一样内置的动画时，调整动画之间的延时是得到一个好的波浪形动作的关键点。

我在我自己的iPhone app Interesting中也使用了波浪形的动画。来看看我的app的动画并构建它。

### 动画Interesting的Stories Into Position
当我的新闻app Interesting首次打开时，我会发起一个网络请求来拉取最近的文章。当请求返回时，我需要用`UITableView`来放置文章数据，每行一篇文章。一些app选择在数据返回时淡入列表，一些会将行一行行地滑动到位置上，而其他的则立即显示行，没有任何动画。我选择使用一个内置的类似我们刚刚构建的音乐播放器的效果，但不是水平地动画它们，我从底部垂直地动画它们。这就是我的加载动画的样子。


----------
![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%205/int.gif)


----------
要完成它，先来一步步地分解我做了什么。

1. 如果数据返回了并且我调用了[self.tableView reloadData]，它会立即出现并且对用户可见。所以我首先让列表的透明度变为0，这样我就可以操作它，不让用户看到任何东西，直到我想让他们看见。
2. 然后我会调用[self.tableView reloadData]将数据加载到列表行中去，这时候所有的行都在它们正常的位置上，但因为整个列表透明度为0并且是隐藏的，屏幕上什么都看不见。
3. 我遍历现在屏幕上可见的行并且移动`UITableView`将行都放到屏幕底部。我通过改变列表的位置，将其移动到整个列表高度的下方来达到目的，这样每行都会藏在屏幕的底部了。
4. 现在所有的行都在屏幕的底部了，我将alpha改回1.0来让列表变得可见。现在列表是可见的了，但素有的行都在屏幕底部所以看不到任何文章。
5. 最后，我再次遍历所有的行将其推离屏幕底部，通过移除我初始设置的变换将其动画到原本的位置上。

这个看上去相当简单的效果有这么多的步骤！这里是完成这些步骤的代码。

```objective-c
// 将列表变为不可见，重载数据
self.tableView.alpha = 0.0f;
[self.tableView reloadData];

// 存储一个时间变量，这样我就可以调整每行动画之间的延迟时间
CGFloat diff = .05;
CGFloat tableHeight = self.tableView.bounds.size.height;
NSArray *cells = [self.tableView visibleCells];

// 遍历行并将它们移动到屏幕底部
for (NSUInteger a = 0; a < [cells count]; a++) {
    UITableViewCell *cell = [cells objectAtIndex:a];
    if ([cell isKindOfClass:[UITableViewCell class]]) {

        // 通过变换cell的Y坐标来讲其移动到屏幕底部
        cell.transform = CGAffineTransformMakeTranslation(0, tableHeight);
    }
}

// 现在所有的行都在屏幕底部了，将列表设为可见
self.tableView.alpha = 1.0f;

// 将每行动画回位置
for (NSUInteger b = 0; b < [cells count]; b++) {
    UITableViewCell *cell = [cells objectAtIndex:b];
	
    [UIView animateWithDuration:1.6 delay:diff*b usingSpringWithDamping:0.77
        initialSpringVelocity:0 options:0 animations:^{
        cell.transform = CGAffineTransformMakeTranslation(0, 0);
     } completion:NULL];
}
```

如果你注意第二个循环，在动画的block中，我的延迟值设为了diff*b。因为我在一个循环中，我可以同步地使用循环次数变量b来保持动画的时间，只需要操作每行的动画时间间隔即可。这可以确保每一行的动画之间都是同样的时间，来达到一个好的波浪形动作。这就是全部了！


----------
是时候换挡了。

至此，我们使用了Core Animation来创建我们的动画界面。无论我们是使用iOS 7的基于block的动画方法及其弹簧属性，还是使用很棒的为我们创建了`CAKeyframeAnimation`的JNWSpringAnimation框架，我们都还在Core Animation的范围内，苹果有众多的框架管理了iOS繁多的界面表现。

但有很多种方法可以解决问题，也就是说，还有其他的不使用苹果的Core Animation框架的方式可以在iOS app的屏幕上创建动作。

其中一个创建动画的方法最近获取了很多的关注。它实在是iOS动画框架界的一股清流，而且已经在世界上一些最常用的app中被用来构建了非常棒的动画。

我说的当然就是Facebook创建的杰出的Pop框架。

你准备好学习一些新东西了吗？开始吧！

## <a name="SECTION 6"/>SECTION 6
### 介绍Facebook的Pop
在2014年4月，Facebook的工程师Kimon Tsinteris发布了Pop，Facebook构建用来支撑他们app Paper的一个弹簧动画框架。这个框架的起源其实早于Facebook，Kimon构建了其中的大部分用来支撑他被Facebook于2011年收购的电子书公司Push Pop Press。你可能记得Push Pop Press，它获得了苹果的设计奖，作为iPad的电子书，为被称为“Our Choice”的AI Gore所构建。

![](https://github.com/Cloudox/Motion-Design-for-iOS/blob/master/SECTION%206/pop.gif)

[点击观看AI Gore's 'Our Choice' - an iPad app视频](https://www.youtube.com/watch?v=U-edAGLokak)

“Our Choice”在2011年确实很有开创性。它是最早的有完整的基于手势来操作界面内容的iOS app之一。屏幕上的每个视觉元素都是弹簧动画的，有着很好的弹性和响应，这是从所未见的。

时间快进到2014年早期，来介绍一些Facebook的Paper。Paper同样包含基于手势的控制和弹簧动画，并且可以发现，它全部基于Al Gore三年前的电子书的工作。对我们开发者来说幸运的是，Facebook认为他们的动画框架Pop值得公开到社区中去，这样其他人也能构建酷的基于弹簧动画的app了。

### Pop VS Core Animation
当我们在本书前面讨论Core Animation的时候，以及它是如何在一个基本的水平上工作的，我结识了model layer和presentation layer的不同。模型层表示已知的准确的CALayer预加到动画上的属性。如果你添加一个动画到layer上，然后在动画进行到一半时问模型层它的属性是什么，答案是不会反映任何动画当前的内容的。如果你想要知道动画中实时的、运动中的layer的值，你就得去看表现层。而一旦动画完成后，表现层就会消失，所以如果你不想你的layer回到开始的位置，你就需要设置模型层的属性来匹配动画的最终状态。

这就是Core Animation的工作。这是苹果为了构建一个iPhone上用的动画框架在很多年前做出的一个基本的实现选择。而因为JNWSpringAnimation简单地为我们开发了一个依然是Core Animation对象的`CAKeyframeAnimation`，我们还是需要设置动画模型层的最终值来在完成时保持住。

Pop是完全不同的！

Pop不使用Core Animation来执行任何它提供的动画功能。不同之处在于它设置了一个特殊的时间对象来每1/60秒执行一次。那个每秒执行60次的代码会直接基于下一个你在弹簧动作中定义的位置更新任何你想要的属性。没有什么特别的、额外的layer添加到你的元素中去，Pop直接在`UIView`或者`CALayer`上改变属性，或者，有趣地在任何你想要的对象类型上改变。这意味着在动画中的任何时候，你都可以直接接触改变的属性的当前值而不用跳到任何表现层。并且更好的是，你不需要单独设置最终值让动画在那逗留，因为动画始终在实际的真实值上工作。

这个Pop用来支撑整个框架的时间对象是`CADisplayLink`，它可以看做是`NSTimer`的一个更高级版本，NSTimer是Mac游戏开发者常年用来在他们的Mac和iOS游戏中一帧帧运行代码的。`NSTimer`可以在你想要的任何时候调用任何你想调用的代码，不断地重复或者只调用一次。如果你想每5秒钟调用一次代码就可以使用`NSTimer`来做。或者如果你想要每秒调用代码60次，也可以用`NSTimer`来做，但当这么快地调用代码的时候（比如每次运动一点点像素，一步步地动画一个界面元素），这个时间对象就会失去准确的同步刷新频率，你可能会丢失一些帧，从而导致一些奇怪的短暂跳跃。

这就是`CADisplayLink`施展之处。`CADisplayLink`就是设计来避免这个问题的，因为它不是设置时间间隔，它一遍遍地调用你的方法的速率完全取决于屏幕的刷新频率。它随着屏幕的刷新来启动你的代码，这样你就有了最好的机会来每秒更新你的界面60次（平滑感知动作的时间）。这就是Pop用来将动画一像素一像素、1/60秒一次推动的方法。

让我们看一些简单的Pop动画时如何工作的。

```objective-c
// 添加我们的红球到界面上
UIView *redBall = [[UIView alloc] initWithFrame:CGRectMake(300, 300, 75, 75)];
redBall.backgroundColor = [UIColor redColor];
redBall.layer.cornerRadius = 75/2; // Half the width
[self.window addSubview:redBall];

POPSpringAnimation *scale =
    [POPSpringAnimation animationWithPropertyNamed:kPOPViewScaleXY];
scale.toValue = [NSValue valueWithCGPoint:CGPointMake(2, 2)];
scale.springBounciness = 20.0f; // Between 0-20
scale.springSpeed = 1.0f; // Between 0-20
[redBall pop_addAnimation:scale forKey:@"scale"];
```

这就是这个代码产生的动画。


----------
![](http://img.blog.csdn.net/20160811090316583)


----------
很有弹性！我们已经谈论了很多关于如何用JNWSpringAnimation和Core Animation创建弹簧动画的内容，现在来看看Pop的方法。

```objective-c
POPSpringAnimation *scale =
    [POPSpringAnimation animationWithPropertyNamed:kPOPViewScaleXY];
scale.toValue = [NSValue valueWithCGPoint:CGPointMake(2, 2)];
scale.springBounciness = 20.0f; // Between 0-20
scale.springSpeed = 1.0f; // Between 0-20
[redBall pop_addAnimation:scale forKey:@"scaleAnimation"];
```

首先，我们创建了一个新的POPSpringAnimation对象。它被设计用 +animationWithPropertyNamed: 方法来初始化，获取参数来告诉Pop你想要动画什么属性。这非常像我们在JNWSpringAnimation中添加的关键路径值，但不是一个简单的字符串，Pop设计了很多值，这样你就不需要记住字符串。这里是一小部分Pop随时可以动画的属性。

* kPOPViewAlpha——视图的透明度
* kPOPViewFrame——视图的整体框架
* kPOPViewScaleXY——视图的拉伸（X和Y轴）
* kPOPViewBackgroundColor——视图的背景色
* kPOPLayerCornerRadius——layer的角的度数
* kPOPLayerRotation——layer的旋转度
* kPOPLayerShadowRadius——layer下阴影的尺寸

所有的属性列表可以在Pop的GitHub找到。那是一个很长很长的清单，并且由于开发者一直在贡献，清单还在不断增长。

你可能注意到这些属性的命名有一些有趣的地方。我们有一个名为kPOPViewAlpha的属性，而另一个又名为kPOPLayerRotation。Pop酷的地方在于基于你传入的属性，你可以操作`UIView`的属性，也可以操作`CALayer`的属性。这完全取决于你，你只需要让Pop知道那一长串它支持的属性清单中你想要动画的是哪一个，无论它是一个view属性、layer属性或者任何类型的属性。Pop允许你更新任何你想要的类型的变量，甚至是与界面动画无关的。

我们设置了 toValue为 [NSValue valueWithCGPoint:CGPointMake(2, 2)] ，看起来可能会有点奇怪。为什么我们要将{2,2}这个点（我们的X和Y拉伸值）放到一个`NSValue`对象中去？好吧，这就是Pop工作的方式，它期待传到toValue参数中的是一个准确类型的值。而这个值得类型取决于我们添加的类型。它总是期待一个对象，在这个例子中，它想要一个`CGPoint`转化成的`NSValue`对象。不幸的是Pop的这个部分在文档中有点难懂，但随着开发者的贡献它也在变得更好。

至于要考虑的fromValue，我们在这个例子中没有设置它，因为Pop做了一些很酷的事情：如果你不设置它，它就会自动计算当前的开始值，并从这里开始。太赞了！


----------
更多更新内容参见[我的博客](http://blog.csdn.net/column/details/cloudox-column3.html)  
[回到目录](#Catalogue)
