
<h2> Clean Architecture</h2>

<div align="center">
<img height="400" src="https://github.com/kimTH65/cs/blob/main/img/CleanArchitecture.jpg">
<h6>source : https://blog.cleancoder.com/</h6>
</div>

<br>
<h4>円の内側に向かってのみ依存し、外側の円は内側の円に影響を与えてはならない。
</h4>
<h6>
<a>　　</a>- Entity : データ構造、関数集合、コアワークルールをカプセル化、最も変わらず影響を受けない
<br><br>
<a>　　</a>- Use Cases : ビジネスルール、業務ルール、データの流れを定義
<br><br> 
<a>　　</a>- Interface Adapters : mvp の presenter, mvvm の view model など、純粋なビジネスロジック
<br><br> 
<a>　　</a>- Frameworks & Drivers : フレームワーク、データベース、UI など
</h6> 
<br>

<h4>長所</h4>
<h5>
 - 理解/開発/維持/配布をより簡単に -> より柔軟でスムーズに
</h5>
<h6>
 - 各階層を明確に分離し、テストとメンテナンスが容易になる
<br><br> - インターフェイスへの依存性がなくなり、インターフェイスが変わってもクライアントは影響なし
<br><br> - 基調階層型アーキテクチャが持っていたデータベースへの依存性がなくなり、データベースなしでも他の部分を開発可能
</h6> 
<br>


<div align="center">
<h4>アンドロイド+クリーンアーキテクチャ構造
</h4>
<img src="https://github.com/kimTH65/cs/blob/main/img/cleanAnd.png">
<h6>source : https://qiita.com/koutalou/items/07a4f9cf51a2d13e4cdc</h6>
 </div>
