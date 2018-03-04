---
title: 矿池的意义在哪里？
tags:
  - bitcoincash
  - mining
  - pool
  - satoshi
date: 2018-03-04 18:21:10
---
问：您好，我想问您一个技术问题，看了好多文章说法都不一样，您看看我理解的对不对。关于矿工挖矿有两种理解：1.白皮书规定谁计算出哈希值，挖出的矿归谁，因为现在算力太高，普通旷工很难有收益，所以某个矿池算力高，挖出来的几率大，但是一个区块也只有一个矿池能获得全部币，矿池内部根据算力贡献度平分这些币。2.白皮书就是说的大家一起算哈希，只要哈希算出来了，大家自动按算力平分挖矿所得。

我自己倾向于认为1是对的，因为白皮书是这么写的，但是这里有个逻辑问题就是如果1对，那个人矿工几乎不会有收益，好像与事实不符。中本聪希望看到的就是这样专业矿池取代小作坊吧，因为花费了大量成本，所以利益上是一体的。但是我不太能理解既然要这样设计，为什么要矿池内按算力分利益，而不是直接全网按算力平分呢？矿池的意义在哪里？
<!--more-->

### 1、去中心化
其实你和对方的理解都是对的，只是去中心化有程度之分，有3个节点是去中心化，有3万个节点也是去中心化，程度不同而已。

去中心化是防止有单一中央节点垄断，因为这就变成了央行。但去中心化不是没有代价的，就是效率降低。过于去中心化，会使得统筹协调、数据同步变得困难，所以要找一个平衡点，这个平衡点应该是市场去自动寻找，而不是像Core开发组那样人为强行限制。实际上，即使有1M的人为限制，也没拦住比特大陆这样的“垄断”矿工出现，所以限制区块来遏制“垄断”，其实是没什么效果的。

长期来说，这个比例应该是恒定的，太低则网络不够安全，太高则网络太昂贵而让大众难以承受，最终市场会给出这个比例应该是多少。

### 2、矿池
中本聪不是希望而是预期未来矿工必然会聚集在一起形成矿池以降低收益的不确定性，甚至中本聪本人就协助过早期的矿池诞生（这个我不确定，但多次听挖矿的专业矿工提起）。

中本聪最开始时对矿工的看法[如下](http://satoshi.nakamotoinstitute.org/emails/cryptography/2/#selection-67.0-83.14)：

> Long before the network gets anywhere near as large as that, it would be safe
for users to use Simplified Payment Verification (section 8) to check for double spending, which only requires having the chain of block headers, or about 12KB per day. Only people trying to create new coins would need to run network nodes. At first, most users would run network nodes, but as the network grows beyond a certain point, it would be left more and more to specialists with server farms of specialized hardware. A server farm would only need to have one node on the network and the rest of the LAN connects with that one node.

建立矿池的目的主要不是利益一致，主要是降低矿工收益的起伏。大致类似于大家凑份子买彩票，也类似于买基金，都是降低不确定性，目的就是让自己的收益能够尽量稳定，比如把“3年间偶然挖到一个块，一个块就赚50个币” 改为 “3年里每个星期都必然能有0.333个币的收益，连续挖3年，一共赚取50个币”。

### 3、全网为何不能每次按算力平分

因为去中心化的全网不能统计矿工的算力比例，这个统计工作必须由一个中心化的矿池来完成（我估计是通过矿池的权力中心，依据分配任务的多少来统计每个矿工的算力多少，具体方法要问运营矿池的人），然后按算力比例来把挖到的50个币切碎了分配。

之所以统计工作必须由一个中心节点来做，是因为POW的工作量证明是计算一个随机函数来实现的，即究竟哪个矿工能率先完成计算是随机的，即算力小的也可能战胜大算力在某一次胜出，所以凭着单次出块是无法知道其他那些没出块的矿工到底有多大算力的，某个矿工能胜出可能不是算力大，而只是运气好。

所以单次出块，全网无法根据挖矿结果获知全网算力比例，但是中心化的矿池可以根据任务分配量来统计算力比例。

https://www.weibo.com/hxsl0622?refer_flag=0000015012_&from=feed&loc=nickname&is_all=1#1520156103254
