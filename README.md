# Leolord的个人站点

原本将博客放到了阿里云上，用Koa 2东拼西凑写了一个博客，还用到了MongoDB、Nginx、Redis、PM2等一堆实际上并不需要的东西。期间甚至还因为Node.js对于ES6的支持增强而做过一次改版。之后悲剧的发现，自己的懒惰是无可救药的。不但很久没有写过任何东西，站点上的Bug也懒得修复。

最终决定把博客先放到Github上吧，万一我那天彻底忘记去阿里云续费呢。

我本身是个前端工程师，后端代码也偶尔写写。工作三年多点了，PHP、Node.js、Java、Python啥乱七八糟的都写过一点，但是除了本行，别的还是啥都不会。

即使单纯前端方向的话，我也很少有非常深入研究的话题。 同事说这是缺乏方法论。我甚至不知道啥叫方法论。


## 最近的博客

{% assign all_posts = site.posts %}

<ul class="post-list">
	{% for item in all_posts %}
		<li>
			<div>
				<h3>
					<a href="{{ item.url }}">{{ item.title }} ({{ item.date | date: "%Y年%m月%d日" }})</a>
				</h3>
				<p>{{ item.excerpt }}</p>
			</div>
		</li>
	{% endfor %}
</ul>
