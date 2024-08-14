# 前言

> Hello，各位好，我是面包！
>
> 这篇文档集合了面包的电赛失败经历与教训总结。



​		在电子设计竞赛中，我意识到找到合适的队友和成为一个合格的队长至关重要。我承认在电赛期间，我没有很好地履行队长的职责，没有激发队友的积极性，也没有平衡地分配任务，结果导致许多任务落在了我身上，而队友们只能提供辅助。我没有根据每个队员的特长来分配任务，这导致我在本应专注于视觉任务的同时，不得不承担PCB电路板绘制、硬件布局思路、MSPM0电控任务等额外工作，以及与学院保持信息流通等杂乱任务。这些因素最终使我们只获得了广东省省赛的三等奖。

​		7月29日，我向硬件队友提供了硬件布局的初步思路，并在当天下午成功完成了PCB板的设计，随后委托嘉立创进行打板。与此同时，另一位电控队友正在着手编写任务执行的代码。在浏览B站时，我偶然发现了一个潜在的实现方案——惯导系统。我以为到电控队友应该能够迅速完成基础方案的编写，我决定利用这段时间学习更高级的惯导方案。

​		7月30日，由于电控队友在通信方面遇到了问题，我不得不在紧张的比赛期间紧急移植蓝牙调试器软件的MSPM0代码，这项工作本应在比赛前完成。由于我对MSPM0配置不够熟悉，直到第二天凌晨才完成代码编写。同时，我还要验证并修改电控队友编写的代码，以及对惯导方案的可行性进行评估。到了晚上，地图送达后，虽然小车能够进行基本的直线行驶和巡线，但表现并不稳定。

​		7月31日，我仅在宿舍短暂地休息了两个小时，便匆匆返回实验室继续我的编程任务。此时，我们的项目进度已经严重滞后于原计划，我对电控队友编写的代码感到担忧，因为它充斥着死循环，完全没有体现出伪实时系统和有限状态机应有的特性。面对这种情况，我不得不亲自接手，从头开始编写代码，以确保我们能够在电赛中顺利完成比赛。尽管我忘记了具体花费了多少小时，但最终我成功地完成了这项艰巨的任务。由于之前分身乏术，我未能深入学习和掌握惯导方案。在深思熟虑后，我决定放弃这一方案，因为我意识到，如果没有我的直接参与和指导，硬件和软件团队可能无法达到预期的效果。下午时分，嘉立创的PCB板如期送达学校，我不禁感叹他们的效率。在夜幕降临之前，我迅速完成了PCB板的焊接工作。然而，在准备验证拓展板的可用性时，我们遭遇了MSPM0板锁死的意外。幸运的是，我在之前加入的电赛学习群中找到了解锁的方法，这才避免了灾难的发生。随后，我们开始了紧张的任务代码验证工作。第一和第二问通过角度PID控制顺利解决，但第三问在对角线连接时小车出现了严重的抖动和寻迹误识别问题。我们通过不断调整角度偏差和参数，虽然勉强解决了问题，但第四问的稳定性仍然不尽人意。面对这种情况，我感到有些无奈，但同时也意识到了团队协作和技术准备的重要性。

​		8月1日，随着电控队友意外发现电机接线错误，我们的比赛进程再次遭遇挫折。经过一番紧急调整，我们勉强完成了12问的任务，但此时的我已感到身心俱疲，几乎想要放弃。时间紧迫，下午我们得知另一支队伍可能会来取走小车地图，这让我们的处境更加艰难。面对这种情况，我决定立即整理代码，准备封箱，以确保我们至少能够完成比赛。到了晚上8点，我们在匆忙中完成了封箱工作。封箱的那一刻，我感到了一丝解脱，终于可以从这四天三夜几乎不眠不休的高压状态中暂时逃离。然而，我也清楚地意识到，按照目前的进度，我们最多只能获得省赛三等奖，甚至可能一无所获。面对这样的结果，我不禁感到失落，同时也在思考如何向指导老师交代。

​		8月3日，我踏上了前往华南理工大学的测评之旅，心情却异常平静，因为早已预料到电赛的结果可能不尽人意。在前往华工的大巴上，我接到了组委会志愿者的电话，告知我们的测评时间已经到来。我向他解释了我们的实际情况，并请求调整测评时间。电话那头，我的声音平静而坚定。当我们终于抵达测评现场，我惊讶地发现，这里并没有我想象中的紧张和严肃，而是一种轻松平常的氛围。这让我的心情也稍微放松了一些。我们的测评过程就像顺水推舟，没有太多的波折。然而，正如我所预料的，我们的小车在测评中只完成了前两问。

​		8月5日，随着电赛结果的揭晓，我们团队获得了省赛三等奖。当我看到这一成绩时，内心涌上的第一感觉是松了一口气——至少我们有了一个可以向指导老师交代的结果。然而，紧随其后的是一种深深的失望。我不禁反思，如果我们在封箱前能更加冷静地处理问题，或许能够成功恢复第三问的代码，这样我们的成绩可能会有所提升。但现实已无法改变，再多的"如果"也只是徒增遗憾。

​		在反思中，我深刻认识到作为队长，关键不在于个人技术能力，而是要根据每位队员的特长合理分配任务，并施加适当的压力以促进他们完成任务。我未能充分发挥这一角色，选择了视觉任务，认为它最具挑战性，却忽视了电控在执行比赛任务中的核心地位。在选题上，我们本有两道控制题可供选择——小车和三子棋，但因电控队友不熟悉STM32 HAL库，我们不得不放弃三子棋。尽管我有HAL库的开发经验，但如果这样，我不确定如何给他分配任务。同时，硬件队友的电路板绘制能力和焊接能力也不过关，这可能会使任务完全变成我一个人的负担，因此我们选择了小车题目。此外，我们与另一队共用一张地图的决定也是错误的，这严重影响了我们的调试效率。
