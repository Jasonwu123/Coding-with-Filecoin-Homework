#### 1.尽管 IPFS 网络已经达到相当大的规模，为什么我们还要构造 Filecoin 这样一个网络？

```
IPFS是互联网的底层协议，而filecoin是一种通证，是一种代币。Filecoin是运行在IPFS上面的一个激励层。
filecoin是去中心化存储网络，中心化存储无法永久保存人类的文明；
ipfs网络只是提供了存储存储，但没有激励难以商业化；
filecoin网络通过经济模型和证明机制来实现存储市场。
```

#### 2. 为什么 Filecoin 要引入 tipset 机制？

```
  tipset机制保证Filecoin在同一高度的可以存在多个区块，其中多个Block都可以获得奖励。引入该机制保证存储提供商都能获取收益，进而维护Filecoin网络健康发展。
```

#### 3. Filecoin 在复制证明的过程中引入了哪些参数和过程来防止女巫攻击，生成攻击和外包攻击？

```
  女巫攻击：是指存储提供商利用N个身份，承诺会存储N份数据，但实际上存储小于N份数据，并谎报自己存储了N份数据。通过加入扇区参数（SectorID）可以确保每一份数据都是独立的，进而防止女巫攻击。
  
生成攻击：是存储提供商利用某种方式生成数据，当系统要求验证时用生成的数据完成攻击。实际并没有存储数据。引入参数（replica_id）是为了生成replica_id的复杂性，这部分工作是不可加速的，是一个比较缓慢的过程，保证了复制的工作量，防止了生成攻击。

外包攻击：当系统要求存储提供山提供存储证明的时候，利用别人存储的数据提供证明，实际自己并没有存储数据。引入身份ID（minerID）是为了使存储的每一份数据都是跟存储提供商绑定的，防止外包攻击。

```

#### 4. Filecoin 是怎么使存储服务商提供稳定的服务的？

```
 复制证明：存储提供商提供存储可以获得代币奖励；
 时空证明：通过时空证明可以验证存储提供商是否真正存储了数据，若没有存储则会损失代币奖励。
```

#### 5. Filecoin 为什么要各种语言/架构实现的版本？这给整个网络带来了哪些好处？

```
每种语言都会有一定的局限性，使用多种语言可以更好的保证整个网络的稳定，维护存储提供商的利益。

吸引更多的开发人员加入Filecoin生态，来对软件进行不同层面的优化，探索不同的软件架构来满足不同的应用场景。
```
