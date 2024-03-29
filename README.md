  _此仓库中文件为阅读APP书源配置文件_ 
<b>阅读APP下载：</b>[https://www.90pan.com/o138704](https://www.90pan.com/o138704)
#  :fa-list: 全网搜书用法
###  :fa-search: 搜索格式定向搜索目标书籍
###  :fa-film: [搜索格式定向搜索目标书籍示范视频](https://m.weibo.cn/6893627530/4583477582760192)
```
───搜索格式───

完全格式　　书名#作者$网站
简化格式1　 书名$网站
简化格式2　 书名#作者
简化格式3　 书名
简化格式4　 #作者(仅夸克支持)

注：仅夸克搜书 支持“#作者”指定作者搜索，这种方式得到的书籍与普通搜索最大的不同在于，借助了夸克官方的数据直接获取相关作者的书籍，然后从链接到的结果页中筛选出小说网站重定向过去直接观看
```
![搜索格式定向搜索目标书籍](https://images.gitee.com/uploads/images/2021/0130/070417_dcc50bd0_8324729.jpeg "搜索格式.jpg")


###  :fa-cogs: 加前缀或修改简介操控书源
```
──────🇨🇳前缀设置全体🇨🇳───────

用法：“转单跳逆原动静字图”等字后跟“^”再跟“搜索关键字”，可实现这些字对应的功能。

范围：本次搜索到的所有书籍都会执行指定的功能。

示例：“图^斗破苍穹”、“逆静^斗破苍穹#天蚕土豆”、“跳^斗破苍穹$www.qidian.com”。

补充：谷歌搜书既设置域名又指定功能时，先设置域名再指定功能，如“0单^我的天国”。
─────⤵
转：尽量考虑将链接转化为电脑版，争取获得目录不分页的电脑版链接

跳：允许目录自动跳转，目录标题说点击跳转时可如此做。

逆：设置书籍目录章节逆向排序，配合指定网站的搜索方式针对小说全是逆向排序的网站比较方便。

原：设置书籍不进行净化替换，优点是加载正文快速且不会被误删内容，缺点是需要自己写“替换净化”规则并在正文中启用才能净化网站推广文本。

动：强制设置正文动态加载(正文默认会进行需要动态加载还是静态加载的判断，然后自动切换模式，若判断失误导致本应切换成动态加载却未切换时，可强制设置正文动态加载)。

静：强制设置正文静态加载(正文默认会进行需要动态加载还是静态加载的判断，然后自动切换模式，若判断失误导致本应保持静态加载却切换成动态加载而使正文加载时间变长时，可强制设置正文静态加载)。

图：设置成看图模式(不设置则默认图文模式)，只显示图片，不显示文字。

字：设置成纯字模式(不设置则默认图文模式)，只显示文本，不显示图片。
─────⤴

──────🇨🇳书籍变量设置🇨🇳───────

用法：
将“单直跳全逆原图字动静”中任意多个字
或“[目录url]”或“[正文尾页url]单”
或“数字#第二页链接#”
或“[目录尾页url]录”
放在详情页右上角的书籍变量中，
确认后点刷新就能触发这些字段对应的功能。

范围：只控制当前书籍执行指定功能。

书籍变量格式示范：[http://m.biquku.la/0/425/]全字

─────⤵
[注：前面`前缀设置全体`哪里列出的所有指令这里也能用]

直：不做目录识别，直接将详情页作为目录页，或以“[目录链接]”格式直接指定目录链接，目录识别错误时可这种做。

全：直接显示查询到的所有章节，跳过章节筛选环节，因为筛选机制导致章节不全时可这样做。
─────⤴

──🇨🇳目录有分页却无翻页按钮或书籍无目录🇨🇳──

单：无目录打开即正文但有尾页或下一页按钮的书籍，必须设置为单向模式，这样书源会直接将入口页作为正文第一页，并将第一页及其所有下一页共同构造生成“正文1”、“正文2”…的目录形式来阅读，搜索前缀“单^”、书籍变量“单”。

录：有目录分页但无目录下一页按钮的书籍，可在书籍变量中直接指定复制到的最后目录页链接为目录链接并添加指令“录”，即可自动生成所有目录分页。
书籍变量：“[https://m.zuizaoxiaoshuo.com/ml/33280_13]录”
对于通用书源，还可复制最后那个目录页链接并在其后加“?录”进行“添加网址”，从而自动生成补全所有目录分页。
示范链接：“https://m.zuizaoxiaoshuo.com/ml/33280_13/?录”

辅助生成──无目录打开即正文也无尾页和下一页按钮的书籍，需指定章节数量并用第二页链接作为参考链接生成所有分页。
书籍变量──220#https://wap.yqshuwang.com/2021n/02/14972_2.html#
效果说明──根据第二页链接“https://wap.yqshuwang.com/2021n/02/14972_2.html”生成220条章节的目录列表。

单个章节──目录仅一个章节且这个章节正文中无下一页按钮时，可复制那个章节的正文尾页链接并用指令“单”，便可将所有正文分页构造成章节列表。
书籍变量──[http://www.yulinzhanye.la/20/20733/532447_9.html]单

──────🇨🇳通用书源用法🇨🇳───────

在导入的书籍链接后加“?”，然后跟着“单直跳全逆原图字动静”中任意多个字或“[目录url]”或“[正文尾页url]单”或“数字#第二页链接#”或“[目录尾页url]录”，也能实现功能增强中描述的效果。

如：“https://m.30sy.com/book/wonengtingjiannidexitongyin0weichuanshu0/?跳”，会将“https://m.30sy.com/book/wonengtingjiannidexitongyin0weichuanshu0/”对应的书籍加入书架，并设置其目录动态加载。

添加指令的链接后也可跟URL参数，如“https://m.qubook.net/read.php?id=115393&txt=/TXT/%CA%F5%D0%DE%B4%F3%CE%D7.txt?1051#https://m.qubook.net/read.php?id=115393&txt=/TXT/%CA%F5%D0%DE%B4%F3%CE%D7.txt&yeshu=1#,{"webView":true}”这种写法也是可行的。

```
![书籍变量](https://images.gitee.com/uploads/images/2021/0913/202128_5c04c7fc_8324729.jpeg "IMG_20210913_200637.jpg")

```
───搜索引擎的通用搜索───

比如“玄幻小说”直接搜索玄幻小说

比如“斗破苍穹 site:www.qidian.com”采用搜索引擎技巧搜索，等同于“斗破苍穹$www.qidian.com”

比如“武神 塔读”

比如“忘语 大梦主”
```
```
───混用搜索引擎式和全网搜书式───

简言：`<前缀>书名#作者$域名`中，
书名前后的关键字都只能是文字描述的模样
作者处只能填作者，域名处只能填域名，前缀处只能填前缀
但书名处则可以完全套用“搜索引擎的通用搜索格式”，自由发挥，浏览器能怎么搜这里就能怎么填

例子：“字^我的 玄幻小说$www.qidian.com”

含义：在“www.qidian.com”中搜名称含“我的”的玄幻小说，设置搜到的书籍正文都只查询文字
```
<br><br/>
# 搜索条目较少
现象：搜索到相关性高的条目少，只有一两条相关性高的。
<br><br/>
原因：同一书源的同一书名结果只显示一条(无论实际结果是多少)，书源的剔除书名中额外文本能力越强，搜索显示相关性高的条目就会越少(被合并了)。
<br><br/>
办法：详情页点进换源列表，就能看到本次搜索到的其它所有与当前书名相同的书籍。
<br><br/>
下页：如果都还没有符合要求的结果，退回搜索界面，上拉刷出下一页，会有更多结果，总之搜索引擎的所有结果页都能通过上拉全部刷出来。
<br><br/>
<br><br/>
# 搜索没有结果
原因一：阅读APP版本太低，不支持书源使用到的新API，请下载最新版
<br><br/>
原因二：搜索分组勾选了“精确搜索”，搜索结果被软件屏蔽
<br><br/>
<br><br/>
# 书源相关链接
源库订阅：http://no-mystery.gitee.io/shuyuan/%E6%96%B0%E7%89%88%E6%BA%90%E4%BB%93%E5%BA%93%E8%AE%A2%E9%98%85.json
<br><br/>
精校书源：http://no-mystery.gitee.io/shuyuan/%E7%B2%BE%E6%A0%A1%E4%B9%A6%E6%BA%90%E5%90%88%E9%9B%86.json
<br><br/>
[:fa-film:通用书源](https://m.weibo.cn/detail/4607771884653947)
[:fa-film:全网搜书](https://m.weibo.cn/detail/4583477582760192)
全网通用：http://no-mystery.gitee.io/shuyuan/%E5%85%A8%E7%BD%91%E9%80%9A%E7%94%A8.json
<br><br/>
<br><br/>

# :fa-magic: 全网搜书思路

1. 把搜索引擎做成书源，借助搜索引擎全网搜书。

2. 搜索有多种方式(`书名#作者$网站`、`书名$网站`、`书名#作者`、`书名`、`#作者(仅夸克支持)`)，具体用法见书源编辑界面首页的“源注释”和[用法展示视频](https://m.weibo.cn/6893627530/4583477582760192)。
<br><br/>
其中夸克支持“#作者”指定作者搜索，这种方式得到的书籍与普通搜索最大的不同在于，借助了夸克官方的数据直接获取相关作者的书籍，然后从链接到的结果页中筛选出小说网站重定向过去直接观看。

3. 发现采用夸克官方分类排行榜，书籍链接指向夸克搜索结果页面，书源从中筛选出小说网站重定向过去直接观看，不满意的话，过段时间点详情页的刷新会重新定向到新的小说网站。

4. 书名采用关键字切割法，先获得初级书名，然后根据各种条件以及搜索页及详情页获取到作者名，进一步识别删除那种书名跟着的作者名或其它无关内容，然后对比网站提供的元数据和author相关标签，存在包含关系时选择其中最短的。

5. 分类、作者、最新章节规则优先识别网站元数据，网站相应元数据时改用最近文本识别法，用正则表达式进行内容抓取，先定位关键字，再查找是否仅跟冒号或处于标签末尾，然后排除一些常见错误定位，然后识别最近的下个文本。

6. 简介规则优先识别网站元数据，网站无相应元数据时改用内容识别法，通过各种判定规则先移除无用标签，避免无关文本被当做简介识别，再通过文本特征精确定位识别简介。

7. 目录链接采用“链接构造正则->正则识别链接”这种正则关联上下级链接的思想根据上级链接精确识别下级链接，并辅以一些目录识别关键字、目录链接关键字识别或排除相关链接，从而构造出专门识别目录链接的正则表达式去识别目录链接。

8. 章节链接优先使用从目录链接处传来的参考链接识别章节(目录链接处尽可能识别最新章节链接或书籍首章，若有则将其作为参考链接)，若不成功则退而求其次采用与目录链接相似的识别方式，根据目录链接构造出专门识别章节链接的正则表达式去识别章节链接。

9. 正文规则：采用无用标签移除思想，使用各种判定规则找出所有不可能存在正文内容的标签并全部移除，从而避免获取到与正文无关的文字。
<br><br/>
然后剔除链接及其环绕文字，以及网站插入的带有负数编号的宣传文本，再对正文中的`章节名、书名、页尾、未缩进文本(仅在正文存在缩进段落时对未缩进段落进行标记)`施加不同标记。
<br><br/>
而且，自动判定正文是否需要动态加载，需要的会自动动态加载，不需要的继续保持静态加载。不需要动态加载的网页不会因为动态加载而变慢，需要动态加载的网站不会因为只静态加载而获取不到内容，两全其美。

10. 替换规则：结合正文添加的`章节名、书名、页尾、未缩进文本`四大标记的相互位置以及标记环绕文本，能快速安全的剔除绝大部分网站宣传文本，而且能根据网站强行切断点识别方法判断出这种网站强行切断段落的位置，并绕开不删被网站强行切断到下一页的未缩进正文重新将网站强行切断的内容合并。
<br><br/>
此外：对英文、全角字符、拼音字符串、数字、图片标签、非中英文字符进行标记，然后结合上下文判断出疑似广告的字符串并施加`特殊标记`，然后再结合上下文其它条件谨慎判断标记成广告的字符串是真广告还是小说内容
<br><br/>
可指定为“图片模式”，采用专门识别图片的jsoup表达式识别img标签，排除网站图标、过渡动画等无关图片。且会自动跳过不执行只针对文字的替换规则。
<br><br/>
可指定为“文字模式”，采用专门识别文字的jsoup表达式识别文本标签，排除图片及图片环绕文本的影响，识别正文更加干净。

11. 书中净化规则特意避开了img标签，净化的同时不会破坏图片显示，所以不仅可以搜书，还可以搜漫画。

12. 单页文章自动构造目录：当某个文章中不存在目录时，自动为将构造目录，从而可以浏览没有目录的单页网页
<br><br/>
<br><br/>
# 更新日志
```
通用书源V32、全网搜书Pro V49

───────

1、修复书籍页链接以“//”结尾时，试图找出参考章节链接会出现语法错误的问题。

2、修复正文链接以“/”结尾时，预先转义意外造成语法出错的问题。

3、对必应搜书的搜索结果进行判断，获取结果不正确时将会重复请求。

4、上调百度搜书的搜索结果不正确时重新请求的次数。

5、以前需要在简介中设置的指令，现在全改成在详情页右上角菜单中的“书籍变量”中设置，最新用法见“源注释”。

6、谷歌改成逐个访问域名直到返回正确结果，可把可用域名放在“源变量”中(格式类似https:/✘/www.google.com/search?q=)，放置多个域名请用换行分隔，不设置源变量则使用默认域名列表。

7、夸克通过发现看书会自动生成当前书籍链接在“书籍变量”中，清空变量刷新后会重定向到新网站，不清空则一直访问生成的网站。

8、夸克发现采用新的排版方式，保证显示不同手机的显示一致。

```
```
通用书源V26、全网搜书Pro V43

─────

优化目录URL规则中的参考链接识别规则，避免将目录“第1页”错当做参考链接，导致章节列表除了正常章节外混入目录分页的问题。

优化目录列表规则，调整首条章节列表识别规则，更进一步避免识别无关链接。

修正目录下一页规则中链接排除规则中的正则预处理部分，避免符合预处理规则的链接未被排除而被错当做下一页链接的情况发生。

优化正文下一页规则，原来仅末尾章节判断下一页是否指向目录页，现在每章都进行这种判断，避免有些网站每章之后都浪费时间去加载不必要的链接。

优化正文下一页规则，将“a.match(c)”形式的写法改为“~a.indexOf(c)”，解决正则冲突导致下一页包含“?”时正则出错的问题。
```
```
通用书源V25、全网搜书Pro V42
────────

增强正文下一页规则：没有下一页按钮，但有正文分页链接列表的书籍，也能识别到所有正文下一页了！

优化详情页作者识别：增强正则净化能力，无关字符剔除更干净

增强正文页替换规则：识别能力更强大
```
```
通用书源V24、全网搜书Pro V41
─────

目录存在下一页但没有下一页按钮时，需复制最后一个目录分页链接。

通用书源可在复制到的最后目录页链接后加“?录”，从而自动生成所有目录分页。如“https:/✘/m.zuizaoxiaoshuo.com/ml/33280_13/?录”。

全网搜书书源则需在简介中直接指定复制到的最后目录页链接为目录链接并添加指令“录”，也能自动生成所有目录分页。即：{[https:/✘/m.zuizaoxiaoshuo.com/ml/33280_13]录}。
```
```
通用书源V23-3、全网搜书Pro V40-3
─────

①目录URL规则中，修复某次优化正则时，将字串格式的正则表达式改成标准正则时，忘将“\\”改成“\”，从而意外将目录链接移除，导致未识别到目录链接的问题。如“https:/✘/m.5atxt.com/wapbook/55770.html”

②优化封面规则，新增一种常见封面识别方法，弥补原规则的不足

③优化正文规则中图片识别方法，新增一种常见src格式的图标排除写法
```
```
通用书源V23、全网搜书Pro V40
─────

①修复正文规则在特定情况下错将body标签移除，导致部分书籍出现正文内容为空的问题！

②精确识别目录首尾分页，将首目录页结果直接跨越式传递到尾目录页处进行对比，用subList方法选中清除前端相同部分。

从而解决每个目录分页都有最新章节列表的书籍最后一页最新章节列表大于正常章节列表时，出现的局部章节逆向排序这个顽固问题！！！

③优化正文规则，当内容识别不到采用兜底识别规则时，优先查找图片，其次查找文本。

若内容满足兜底规则要求但同时正式内容只是文字却有无关图片干扰时，请设置成“纯文字”模式获取正确内容！

若内容为图片，设置成图片模式时，因为图片标签存在多个src或存在data-src而在阅读中显示不出来时，可将图片模式改为动态模式(“?图”->“?动”)，因为非图片模式下替换规则会对图片标签进行格式化处理且动态模式能保证图片标签已写入，能解决一部分图片无法显示的问题，如“https:/✘/www.shenglifubang.cn/book/webBookDetail/1936?动”
```
```
通用书源V22、全网搜书Pro V39
─────

①优化详情页书名规则，上个版本书名有可能会获取成列表，导致详情页加载失败，现在修复。

②优化正文规则与替换规则，上个版本去掉了标记书名、章节名的语句，原因是容易误删。
现在重新对章节名进行标记，并在替换规则中预排除部分典型的错误标记，并将内容分为“首、体、尾”三部分，去掉文“体”部分的标记，然后合并内容再做进一步的替换净化。
这样做能净化正文首尾出现章节名的同时，还能有效降低章节名标记导致的误删！

③优化详情页封面规则，发现页得到的书籍优先采用发现页得到的封面图！

④优化目录Url规则，上个版本屏蔽“下一页”链接的同时也屏蔽了部分链接中带有“page”的目录链接，这次优化后这条规则将只会屏蔽非目录链接，如“https:/✘/m.aoyuge.com/35/35838/”也能识别到目录链接了！

⑤优化目录列表规则，优化废话章节屏蔽方法，屏蔽更精准
```
```
全网搜书Pro V38、通用书源V21
───────

⓪删除目录下一页规则(改为在目录列表规则中获取)。

①删除目录Url规则中试图获取正向目录链接的规则(目录列表规则已加强，无需再试图获取正向目录链接)，加快目录链接获取速度。

②章节列表及目录下一页皆放在目录列表规则中获取！！

这样做的的好处是，可以对比不同分页获取到的章节列表，实现目录的整体操控。

　如：(一) 对比不同目录分页的章节列表，删除不同分页前后相同的所有链接！
　　解决每个目录分页都有最新章节列表的书籍，最后一页出现局部章节倒序的问题。
　　实现意外获取到非章节链接时，可通过对比不同目录分页排除非章节链接的功能！！

　如：(二) 所有目录分页集中获取，解决设置目录逆向时，列表出现“7、8、9、4、5、6、1、2、3”这样局部正向排序而分页依然逆向排序的问题。

```
```
通用书源V17、全网搜书Pro V34
───────

◉【解决最近更新导致大量网站书籍正文变空白的问题】

如：“http:/✘/m.lssin.com/bookinfo/206651.html”

◉【修复详情页最新章节规则】

◉【优化替换规则】

解决作者随意拿某个符号当成引号用而被误删的问题。

解决网站两段推广宣传内容相连，前段以句号结束时，导致替换规则只净化了上一段，未将两段都净化的问题。
```
```
通用书源V16、全网搜书Pro V33
───────
⓪优化分类规则，排除将表情符号识别成分类的可能

①优化简介识别规则，进一步排除无关文本。

②优化目录列表规则，上个版本不小心把规则弄成了，详情页和目录页不一致时才移除“javascript:”开头的标签，现在改回无条件移除。

③优化目录列表规则，上个版本将vip章节识别方法改得过于严格，导致有些网站vip章节识别不到了，现在放宽规则。

④简化目录url规则

⑤简化并增强正文规则识别精确度

```
```
通用书源V14-2、全网搜书Pro V31-2
───────
⓪增强参考链接抓取规则，目录识别更精确

①目录列表规则新增一种从script标签中直接抓取目录列表的方法(加上原有方法一共有两种从script中抓取元素的方法了)，让一部分原来需要设置目录跳转的书籍不设置目录跳转也能得到目录。
```
```
通用书源V14、全网搜书Pro V31
───────

⓪优化纯图模式正文加载速度

①“全网搜书”前缀改为“转单跳逆原动静字图”等字后跟“^”再跟“搜索关键字”的方式指定，原来的指定方式将不再有效。

②新增指定书源不执行替换规则的功能，只需在将“{原}”插入简介前端保存刷新即可指定。
“通用书源”可在添加网址时在网址后加“?原”的方式实现同样效果。
“全网搜书”可在搜索书籍时加前缀“原^”指定本次搜到的所有书籍都不执行替换规则。

③增强单页模式，设置为单页模式的书籍，书源将尝试自动构造目录。

添加网址
“https://wap.yqshuwang.com/2021n/02/14972.html?静字单”
的效果与
“https://wap.yqshuwang.com/2021n/02/14972.html?静字220#https://wap.yqshuwang.com/2021n/02/14972_2.html#”
一致。

对于那种没法自动构造目录的书籍，依然需要采用类似“https://wap.yqshuwang.com/2021n/02/14972.html?静字220#https://wap.yqshuwang.com/2021n/02/14972_2.html#”的方式人工设置目录如何生成。

否则，只能通过不断加载下一页的方式加载所有目录，几百页的书籍大概10多分钟才能加载完目录，几千页的书消耗的时间更是不可想象。

而自动生成目录或人工设置生成目录的只需要几分钟。
```
```
通用书源V13-3、全网搜书Pro V30-3
───────
①全面加强正文规则，旧版本存在正文内容过少而正文内容之外某个元素中所有a标签文本累积超过正文字数时，虽然不会将a文本作为正文，但会将包含a标签的父元素的其它标签中的文本当做正文一部分，导致正文出现额外内容的问题。

现对这种情况进行分析处理，以后同样现象再也不会出现了。

②针对那种有些章节正文全是文字没有图片而有些章节正文全是图片没有文字的书籍。

旧版本为了加速正文获取而将首次查询表达式向后传递，导致书籍要么只能看图片章节，要么只能看文字章节。

现改为根据首次得到的正文元素反向构造出专门识别正文所在元素的jsoup表达式，构造不出表达式或构造出的表达式不够精确时才会用内置的识别法进行识别。

从而使得那种有些章节正文全是文字没有图片而有些章节正文全是图片没有文字的书籍中两种章节都能正常阅读了。

③目录列表规则，增强屏蔽那种纯粹感谢书友的章节的能力，既然感谢内容又有正文的不会被屏蔽

④针对个别以图片形式显示文字的网站的识别能力，避免有些章节有内容有些章节无内容的问题。
```
```
通用书源V12-5、全网搜书Pro V29-5
───────
⓪“通用书源”添加网址时，链接后可先跟指令再跟URL参数，如“https:/✘/m.qubook.net/read.php?id=115393&txt=/TXT/%CA%F5%D0%DE%B4%F3%CE%D7.txt?1051#https:/✘/m.qubook.net/read.php?id=115393&txt=/TXT/%CA%F5%D0%DE%B4%F3%CE%D7.txt&yeshu=1#,{"webView":true}”。

①优化正文规则的内容筛选机制，少数依然会获取到正文标签之外标签的网站，现在也能精确识别了。如“m.qubook.net”网站的小说。

②鉴于夸克搜书通过发现看书时，有可能访问到被墙或已经挂了的网站，导致加载目录失败，故对得到的链接进行是否能访问的检测，若检测失败就替换成另一个网址。
```
```
通用书源V12-3，全网搜书Pro V29-3
───────
⓪优化“目录url规则”中参考链接规则，新增对类似于“read?id=123456”、“book?bid=aya”这类网址的识别，将正确的参考链接传递到目录列表规则处，有利于排除无关链接只识别到章节链接。

①优化“正文下一页”规则，当上下章都是类似于上面那种网址时，旧版书源对这种链接会直接当做下一页链接而不做判断，会使正文一直加载不出来。

现将下一页规则更改为，当上下章链接都是类似上面那种链接时，依然需要进行包含性判断，从而避免无限加载下一页导致正文一直处于加载中的问题。
```
```
通用书源V12，全网搜书Pro V29
───────
⓪优化“通用书源”详情页书名规则，获取更准、执行更快

①将“全网搜书”三个书源搜索页的分类规则调整到书名处执行，减少不必要的变量传递，并优化相应规则，获取更准、执行更快

②优化“全网搜书”三个书源搜索页的书名规则，获取更准、执行更快。

──⤵
至此版本，所有书源终于从头到尾又完全优化了一遍，所有可以加载更快的地方均以优化成所能想到的最快执行写法。

经过最近几个版本的连续更新后，可以明显发现书籍整体加载速度快了很多很多。

向后回溯四个版本对比现在的版本，一本六千多章的书，原来加载到正文时需要消耗36秒以上，现在只需要12秒左右。
──⤴
```
```
通用书源V11-3，全网搜书Pro V28-3
───────
①由于操作失误，导致`通用书源V9、全网搜书Pro V26`不是在`通用书源V8-1、全网搜书Pro V25-1`基础上进行更新，而是在前个版本上进行了更新，导致已修正的问题未能延续到之后的版本，现重新进行相关问题的修正。

②多次优化正文规则，不断加快正文获取速度，快一点是一点，精益求精。

```
```
通用书源V11，全网搜书Pro V28
───────
⓪重构“目录列表规则”，更改执行方式！

当目录有分页时，将在目录第一页执行所有规则并试探出能查询到章节链接的jsoup表达式；

剩下的目录分页将跳过“试探出能查询到章节链接的jsoup表达式”的所有语句，直接用目录第一页传递来的jsoup表达式获取章节链接。

加载目录分页很多又没找到参考链接的书籍时，目录整体加载速度比上个版本快无数倍。

①重构“正文规则”，更改执行方式！

当正文有分页时，将在正文第一页执行所有规则并试探出能精确定位到内容元素的jsoup表达式，以及判断出当前书籍正文需要动态加载还是静态加载；

剩下的正文分页将跳过“试探出能精确定位到内容元素的jsoup表达式”及“判断出当前书籍正文需要动态加载还是静态加载”的所有语句，直接用正文第一页传递来的变量来决定是否动态加载和定位内容元素。

全书正文整体加载速度大大提高！

②优化正文动态加载机制，减少正文内容不全的情况。
```
```
通用书源V10，全网搜书Pro V27
───────
①优化“目录url规则”中查找参考链接put到后面的相关代码，传递更准确。

②优化“目录列表规则”首个查找章节链接的规则，避免获取到无关链接。

③优化“正文规则”，解决chapter.url为相对网址而baseUrl为绝对网址时，上个版本的逻辑判断机制不够完善，导致判断正文需要动态加载，却未执行动态加载导致正文不全的问题。
```
```
通用书源V9-2，全网搜书Pro V26-2
───────
⓪修正select结果为空时，后跟remove()方法触发try语句捕获错误，导致其中变量未执行而使后面访问未定义变量时正文加载失败的问题。

①将“正文下一页规则”中一条语句提前到“章节url规则”处执行，避免每次加载下一页时都重复执行同样的语句，提升正文加载速度。
```
```
通用书源V9，全网搜书Pro V26
───────
⓪修正网站标签错误，导致内容错乱和缺失的问题。

比如网站存在“<img&nbsp;src="image/niaojpg">”或“</a&nbsp;>”这样的标签导致的内容错乱缺失。

①修正同时选中父元素和子元素导致的内容重复问题

②完全改变“正文规则”动态加载机制，加快正文执行速度！！

上个版本在加载每个正文分页时都会重复进行是否要动态加载的判断，整体下来凭空消耗了太多时间，现在改为只在正文第一页时判断需要动态还是静态加载。

然后将判断结果通过“正文下一页规则”和“正文规则”相关逻辑代码间接告诉正文第二页、第三页、第…页，不再重复执行不必要的判断。

注意：下次阅读APP更新后(2月19日之后的版本)，这次更改的“正文规则”动态加载机制才会完全发挥效果(现在，只有正文第一页、第三页及其之后的分页效果正常，正文第二页始终静态加载)，请谨慎升级！
```
```
通用书源V8-6，全网搜书Pro V25-6
───────
⓪预先替换result中的特定内容，解决org.jsoup.Jsoup.parse()方法解析特定字符串出现错乱导致内容缺失的问题

①优化作者名获取规则，获取作者名的能力加强，原来获取不到的现在有些也能获取了；获取作者名更准确，原来识别错成其它文字的现在有些修正回来了。

②大幅度增强优化封面获取规则，原来获取不到的现在能获取到，原来获取错成其它封面的现在也基本修正回来。

③净化规则加强，新增一种情况的识别与净化

④“通用书源”的书名规则加强，比原来获取更精确
```
```
通用书源V8，全网搜书Pro V25
───────
重要提示：有些书籍获取到了非章节链接不是因为书源出了问题，而是因为网站转移到新的地址，导致目录下一页定位到了旧网站首页，所以获得了非章节链接。比如https://m.18xs.org/book_14120/all.html，像这种请到新网站复制书籍链接。

⓪修正设置获取到的链接尽可能转化为电脑版链接的相关逻辑判断，因为最近几个版本改变了相关处理流程，但判断是否需要尝试转化为电脑链接的逻辑却未跟着修改，现在发现这个问题并进行了修正！

①全面优化“目录url规则”和“目录列表规则”中那种即可以是英文又可以是汉语拼音的屏蔽关键词写法，解决有些以汉语拼音作为书名编号的网址个别书籍链接被屏蔽的问题。

②优化“目录url规则”，屏蔽链接中包含“mulu”但不是书籍目录而是分类的链接，避免目录识别出现偏差，解决www.aixswx.com这种网站的目录识别问题。

③优化“目录url规则”，解除对“//”开头的链接的屏蔽，并对涉及到这种链接的规则进行优化，解决少数网站目录以“//”开头而被屏蔽后识别不到的问题。

④优化“目录列表规则”，预先移除“link”和“meta”标签，剩下与“href”相关的查询表达式都不用再加“a”来精确定位了，解决上个版本会获取到的一些目录杂项的问题，如起点中文。

⑤优化“目录列表规则”，优化查询十六进制书籍编号的规则，排除十六进制编号后接“=”的情况(如“subCateId=”这种容易被错当做书籍编号)，避免分类、书库、排行链接被识别成章节链接的可能，解决上个版本会获取到的一些目录杂项的问题，如起点中文。

⑥通用书源获取有些网站书籍的书名时，在经过净化处理后依然存在很多冗余内容(比如https://m.qzleyang.com/bk/16030.html)，针对这种网站会考虑识别简介，若简介以“《”开头，则尝试提取其中书名。
```
```
通用书源V7，全网搜书Pro V24
───────
⓪章节脚本：

尝试从script中直接抓取章节链接数组，解决有些网站需要点击特定按钮才会通过js加载完整目录的问题。
并尝试将其中utf-8编码字串还原为字符。

例如：http://m.lssin.com/bookinfo/206651.html

①目录生成：

制作原因──没有目录且正文分页特别多的书籍，一页页的加载下一页会非常非常的慢，根据参考链接生成所有分页组成目录列表则只需加载一两页的时间内就可生成数百数千章大小的目录列表。

举例说明──插入{220#https://wap.yqshuwang.com/2021n/02/14972_2.html#}，则能参考“https://wap.yqshuwang.com/2021n/02/14972_2.html”生成220条章节的目录列表。

重点突出──其中“##”之间是第二页链接，是生成目录必不可少的参考内容。

通用书源──添加形如：“https://wap.yqshuwang.com/2021n/02/14972.html?220#https://wap.yqshuwang.com/2021n/02/14972_2.html#”的网址也能达到修改简介同样的效果。
```
```
通用书源V6-1，全网搜书Pro V23-1
───────
增强章节逆向排序功能：

增强前，只能正确处理单页目录的逆向排序，面对多分页的目录时会出现每个分页都做好了逆向排序纠正，但分页本身也是逆向却未纠正的问题。

增强后，设置逆向排序时(设置方法见书源的源注释)，会自动加载目录首个分页，并在其中查找正向排序链接，查到后直接将目录链接替换为正向排序的链接，查不到则采用人工排序实现逆向排序。


比如：https://m.zhaishulou.com/166849/?[https://m.zhaishulou.com/dir/166849/?page=1&sort=desc]逆
```
```
通用书源V6，全网搜书Pro V23
───────
①将“正文规则”中的“while(c--)”替换成“for(;c;c--)”，修复动态加载未执行的问题。

旧版问题追踪：

由于js中“while(c--)”与“for(;c;c--)”不等效，导致动静态判断机制判断正文需要动态加载时，虽判断成功却未执行动态加载的问题。

②全面增强“目录url规则”的判断机制，目录链接识别准确度更进一步！

增强部分描述：

由于网站分类、网站推广、网站其它与书籍无关链接大多数字数通常都是固定的二到四个字，故根据此点移除只包含一至四个字又不包含特定关键字的其它链接，避免非目录链接被识别成目录链接的可能。

根据当前baseUrl构造出可大致匹配当前书籍章节链接的正则识别表达式，并将符合此正则表达式的链接移除，避免章节链接被误当成目录链接识别。

根据当前baseUrl构造出可大致匹配当前网站其它书籍详情页链接、目录页链接的正则识别表达式，并将符合此正则表达式又非当前书籍链接的其它链接移除，避免其它书籍的链接被误当成当前书籍的目录链接识别。
```
```
通用书源V5-2，全网搜书Pro V22-2
───────
①优化“目录url规则”，屏蔽链接包含“list”且是分类的链接，避免目录识别偏差。
②修正“目录url规则”中储存目录链接的变量与向后传递带书籍编号的网址前端的变量同名导致当两者不一致时访问目录失败的错误。
③修正上个版本调整章节筛选规则后把“javascript”开头的链接识别成章节链接的错误。
```
```
通用书源V5，全网搜书Pro V22
───────
①改进“目录URL规则”处，用于识别章节参考链接的元素查询表达式，原来识别不到参考章节的有些网站现在也能识别了。

②改进“目录列表规则”中元素筛选规则里按结构屏蔽无关链接的写法，避免有些漫画网站的正常章节被屏蔽导致识别章节出现偏差的问题。

③优化正文规则，指定为看“图”模式时，屏蔽封面图。

④优化正文下一页规则，避免同时得到多个下一页链接时，正则判断出现误判导致下一页的数量明明超过两页却只加载了两页的问题，这种情况常见于漫画网站
```
```
通用书源V4，全网搜书Pro V21
───────
⓪由于章节筛选规则比较浪费时间，所以不到兜底规则生效时，就不执行章节筛选规则了。
兜底规则之前的识别规则都比较精确，识别成功时一般不会混入无关链接；识别失败后再做章节筛选并执行兜底规则。
此举将大大加快大部分网站的目录列表加载速度。

①加“!”搜到的书籍将被设置成单页模式，这种书籍会跳过不执行目录链接识别规则、跳过不执行章节链接识别规则(旧版的单页模式跳过得不彻底，这次将是彻底跳过)。直接将入口页作为正文第一页，并将第一页及其所有下一页共同构造成“正文1”、“正文2”…的目录形式来阅读。

②向简介前端插入“{单}”也能设置当前书籍为单页模式，这种模式适用于那种没有目录故只能从正文首页开始并通过点击下一页连续阅读的书籍，也适用于只有一页的单页文章/网页。

③导入通用书源的，可在书籍链接后加“?单”设置书籍为单页模式。如：“https:/删/wap.yqshuwang.com/2021n/02/14972.html?单”
```
```
通用书源V3，全网搜书Pro V20
───────
⓪鉴于谷歌搜索结果的元素布局经常变动，故换种不容易受这些变动影响的书籍列表识别规则，修复最近谷歌搜书没有结果的问题

①新增动态加载的指定方式，跳过动态静态判断切换程序，强行指定正文动态加载，正文的程序没有自动切换成动态时可强行指定为动态加载，解决偶尔有些网站内容不全的问题。

②新增静态加载的指定方式，跳过动态静态判断切换程序，强行指定正文静态加载。

③将修改简介、设置前缀、书籍链接后缀三种方式指定书源功能的相关代码统一处理，涉及到此逻辑的其它代码全部精简。

④替换规则中，优化冒号后跟着链接这种规则的识别，避免单独的“:”也被标记，导致误删正文正常内容。

⑤将替换规则中，一条替换规则中的“☯.☯”更正为“☯\.☯”，避免这条规则错误的标记了不应该标记的段落，导致误删正文正常内容。
```
```
通用书源V2，全网搜书Pro V19
───────
①目录url规则中，屏蔽仅含“追书”两个字的链接，解决类似“m.30sy.com/book/zaguomaitiequshangxue/”这种追书链接包含“chapterlist”而被误当做目录链接，从而导致目录定位出错的问题。


②目录url规则中，新增“showchapter”识别关键字，并将候补规则中排除“chapter”改为排除“/chapter”，纵横中文网等几个正版网站的目录终于不会识别出现偏差了。

③优化目录列表规则，屏蔽关键字的写法更严格，尽可能避免屏蔽到正常章节。

④目录下一页链接优化，当设置目录跳转时，所有目录分页的都动态加载，避免章节识别不全的问题。

⑤正文规则，新增当内容包含“内容未加载完成|关闭小说模式|关闭阅读模式”时自动动态加载的逻辑
```
```
Pro V18
──────
百度搜书：

重写三个(最新章节规则、详情页url规则、书名规则)与书籍来源网址相关的规则

搜索页最新章节规则：优先获取直接链接，其次获取文本中不包含“...”的快照链接的文本，再其次获取快照链接，再再其次获取标题链接，尽量获取到最接近原网站的网址。

详情页url规则：在搜索页最新章节规则处处理后向后传递变量，优先获取直接链接，其次获取快照链接，再其次获取标题链接

详情页书名规则：设置baseUrl，优先以直接链接设置，否则以base标签文本设置，否则以快照链接的文本设置(不是快照链接，是快照链接的文本)

像“www.cnoz.org”这样的网站，百度搜书终于也能看了。

所有书源：优化正文下一页规则网址以method=get方式加载时的处理方式
```
```
更新到Pro V5
────
一、简介精确识别上线！！

上个版本偷懒只用“[property$=description]”识别简介，现在则借用“正文的精准识别规则”，并在其基础上进行增删调整使其适用于识别简介内容。

目前为止，效果完美(识别能力强、识别到简介外文本的几率低)

二、正文内容识别规则升级：①能识别的网站更多②识别更加精确。

一直以来，不存在包含关系的并列元素，想判断紧挨着的两个都直接包含几十上百个文字的元素，那个是正文，那个不是正文一直都是个大难题，把规则搞严格了识别不到内容，把规则放松了又会识别到正文之外的文字。

经过我一天的研究测试后，终于想办法解决了这个难题。这个办法就是新增的“分解对比法”，先调整规则将上个版本无法识别到的内容识别到，然后按是否包含换行、是否是块元素、或都不是但包含文字的方式分为五组，不按长度逐一选取元素，而是按照分组中所有元素长度之后选取长度最长的分组。

现在，像“www.hetushu.com”、“www.6ks.net”这样的网站内容也能精确识别到了。
```
```
更新到Pro V4-2
────
优化章节名标记方法，识别删除插入内容中的章节名更加精确有效
优化目录URL规则中目录链接的父元素定位规则
```
```
更新到Pro V4(精简优化)
───
1、把阅读提供的变量都利用起来，删除所有不必要的java.put语句，避免无意间获取到空字符串。

2、加强最新章节规则，能识别更多情况。

3、加强正文规则，彻底消除旧规则用java.put传递变量为空时正文标记全文删除的现象。

4、把详情页的书名、作者、分类、最新章节规则合并起来写，避免一大堆无意义的相互转化和重复查询代码。
```
```
更新到Pro V3-3
────
1、综合测试书源设置{转直跳全逆动字}，发现并修复一些错误。
①修复目录URL规则中未将book.customIntro转化为String，导致设置{直}时目录加载出错。
②修复目录列表规则中，设置{全}时使用了未定义变量b有问题，导致目录加载出错。

2、精简优化目录列表规则，代码更少，效果更好。

3、优化搜索页书名规则，解决一些网站识别到的书名包含额外文字的问题。

4、优化改进正文下一页规则：旧规则屏蔽了href="?page=2"这种下一页，现在不再屏蔽只有一段的链接。

───
专业版终于画上了句号
```
```
更新到Pro V3

────
综合测试书源设置：{转直跳全逆动字}、{转直跳全逆动图}，发现两个错误。

1、修复目录URL规则中未将book.customIntro转化为String，导致设置{直}时目录加载出错。

2、修复目录列表规则中，设置{全}时使用了未定义变量b有问题，导致目录加载出错。

3、优化精简目录URL规则。
───
专业版终于画上了句号
```
```
更新到Pro V2-1
───
终于实现了“百度搜书”的“尽可能转化链接为电脑版”的功能。
这样一来，谷歌搜书、百度搜书、夸克搜书(原夸克原网、夸克电脑合二为一)都可以通过前缀和修改简介启动这个功能了。
```
```
更新到Pro V2
───
0、移除夸克原网用于测试的详情页链接，无论怎么搜目录都一样的现象不会发生了。

1、将夸克电脑并入夸克原网，以后两者的功能都用夸克搜书实现。

2、同时采用关键字加前缀和修改简介的方式控制书源的执行效果。

注：两者的区别是，加前缀搜索影响所有书籍，修改简介再点刷新只影响当前书籍。
```
```
更新到Pro V1-2
───
优化目录识别规则：旧规则中，识别到的目录链接为以“javascript:”开头时，会直接将当前页作为目录页，新规则新增排除一种情况，链接即使以“javascript:”开头，只要元素包含“最新”字段时，依然会继续查找其它目录链接。
```
```
更新到Pro V1-1
───

功能：将特定字段插入简介保存后，点刷新可实现目录跳转、正文动态加载、目录逆向排序、目录链接指定等多种功能。

位置：插入到简介最前端

格式：在“{}”中包含以下文字就会触发相应功能
─────⤵
直：不做目录识别，直接将详情页作为目录页，或以“直[目录链接]”格式直接指定目录链接，目录识别错误时可这种做。

跳：允许目录自动跳转，目录标题说点击跳转时可如此做。

全：直接显示“预览正文”和查询到的所有章节，跳过章节筛选环节，单页文章和部分筛选后章节不全的小说网站可这样做。

逆：设置目录章节逆向排序。

动：正文动态，设置正文动态加载，内容为空时可如此做。

图：设置成看图模式(默认为图文模式)，只显示图片，不显示文字。

字：设置成纯字模式(默认为图文模式)，只显示文本，不显示图片。
─────⤴

示例：{直[http://m.biquku.la/0/425/]全动字}

效果：①直接将“http://m.biquku.la/0/425/”作为小说目录链接②显示元素查询得到的全部章节列表，不做章节筛选③以纯文字模式查找正文内容，避免图片干扰。④动态加载正文内容
```
```
更新到V60，改头换面

────
1、完全重构“百度搜书”详情页所有规则。

解决由于java.getElement漏洞导致获取内容缺失，使得详情页所有规则都有一定几率无法获取到有效信息的难题。

解决由于java.getElement获取的内容缺失误导目录链接识别机制，导致将非目录链接当做目录链接的难题，如“www.wujiuwenxue.com”。

重构前，有快照时用快照，此时一切正常。无快照时，目录章节为相对链接时会拼接出错，导致正文获取失败。

重构后，有快照时用快照，无快照时自动跳转并将baseUrl设置成跳转后的网站，不管有无快照都能正确拼接章节链接。

2、所有书源详情全部改为先预处理剔除不必要的内容，再用java.setContent格式化设置内容。
设置内容之后出现的规则全部简化，原来用于剔除不必要内容的规则全部删除，因为已不需要。

3、目录链接规则：章节链接的父元素识别方法从“:not(:matchesOwn(\S),:has(:not(a):matchesOwn(\S)+:has(a:only-child):only-child,:not(a):matchesOwn(\S)+a:only-child))”简化为“matchesOwn(^$)”，效果更好，代码更少。

4、去除详情页“────”分隔的内容，因为阅读已经支持详情页复制URL了，这个设计的作用就不大了，故将用于获取额外内容的所有代码全部删除。

5、优化正文未缩减段落标记，避免有些网站会变得全成一段，且由此导致误删部分内容。

6、改进目录链接无文本时的识别方法，为这种链接的识别关键字添加前后字段限制，并屏蔽“hot|sort|top”三个关键字，避免把分类排行当做目录。

7、优化夸克搜书详情页规则，避免执行不必要的语句，删除不必要的变量。

8、删除“夸克电脑”的发现页：
①因为和“夸克原网”得到的结果一样，重复没有意义。
②删除发现页后，详情页可去除大量不必要的判断语句，加载详情页变快。

9、重构夸克电脑所有界面中链接的处理方式，争取让夸克原网和夸克电脑具有明显的区别，各展所长。

这次更新后，夸克原网与夸克电脑将有如下区别

────夸克原网────
特点：进退自如

⓪有发现

①搜索页加载快(不考虑转化链接为电脑版)

②关键字加“@”前缀，可允许目录链接自动跳转

③关键字加“$”前缀，可指定章节链接动态加载(不指定时静态加载)。
静态加载比动态加载快很多，但指定动态加载后能读取到需要异步加载才能显示的网页正文，比如大多数漫画网站以及部分正版小说网站。

────夸克电脑────
特点：懒人专属

①无发现，且搜索页加载慢(优先考虑转化链接为电脑版，争取获得目录不分页的电脑版链接)

②取消关键字加“@”前缀的设定，因为需要目录链接自动跳转的情况很少

③取消关键字加“$”前缀的设置，对所有章节都采用动态加载。

正文加载等同于“夸克原网”加“$”前缀的效果，好处是不用考虑内容需不需要动态加载，坏处是对于不需要动态加载就能显示内容的网站来说，凭白无故降低了加载正文的速度。

PS：更多相关信息，源注释都有介绍
```
<br><br/>
# 使用示范图片
──────────────────────────────────
## 夸克官方排行榜
![夸克官方排行榜](https://images.gitee.com/uploads/images/2020/1117/123309_71237217_8324729.jpeg "夸克官方排行榜.jpg")
<br><br/>
## 玄幻热搜榜
![玄幻热搜榜](https://images.gitee.com/uploads/images/2020/1117/123336_328dbb72_8324729.jpeg "玄幻热搜榜.jpg")
<br><br/>
## 详情页
![详情页](https://images.gitee.com/uploads/images/2020/1117/123415_2b823f53_8324729.jpeg "牧神记.jpg")
<br><br/>
## 换源列表
![换源列表](https://images.gitee.com/uploads/images/2020/1117/123446_b9a64883_8324729.jpeg "换源列表.jpg")
<br><br/>
## 搜索格式：书名#作者$网站
![书名#作者$网站](https://images.gitee.com/uploads/images/2020/1117/123703_552ce92d_8324729.jpeg "完整搜索格式.jpg")
<br><br/>
## 搜索格式：书名#作者
![书名#作者](https://images.gitee.com/uploads/images/2020/1117/123753_edec8a71_8324729.jpeg "无限轮回#陌白.jpg")
<br><br/>
## 搜索格式：书名$网站
![书名$网站](https://images.gitee.com/uploads/images/2020/1117/123913_71a0d10d_8324729.jpeg "大奉打更人$www.jpg")
<br><br/>
## 搜索格式：#作者
![#作者](https://images.gitee.com/uploads/images/2020/1117/123952_2d591b35_8324729.jpeg "指定作者搜索.jpg")
<br><br/>
<br><br/>
<br><br/>
<br><br/>
# 净化前后对比
<br><br/>
# 示范一
──────────────────────────────────
<br><br/>
## 净化前
![内容1：净化前a](https://images.gitee.com/uploads/images/2020/1117/124039_c6ec22f1_8324729.jpeg "内容1：净化前A.jpg")
![内容1：净化前b](https://images.gitee.com/uploads/images/2020/1117/124102_f8a0df41_8324729.jpeg "内容1：净化前B.jpg")
<br><br/>
## 净化后
![内容1：净化后](https://images.gitee.com/uploads/images/2020/1117/124110_a4d53c2e_8324729.jpeg "内容1：净化后.jpg")
<br><br/>
<br><br/>
# 示范二
──────────────────────────────────
<br><br/>
## 净化前
![内容2：净化前a](https://images.gitee.com/uploads/images/2020/1117/124411_a625ae75_8324729.jpeg "内容2：净化前A.jpg")
![内容2：净化前b](https://images.gitee.com/uploads/images/2020/1117/124443_77ec94d0_8324729.jpeg "内容2：净化前B.jpg")
<br><br/>
## 净化后
![内容2：净化后](https://images.gitee.com/uploads/images/2020/1117/124509_235546f1_8324729.jpeg "内容2：净化后.jpg")
<br><br/>
<br><br/>
# 示范三
──────────────────────────────────
<br><br/>
## 净化前
![内容3：净化前](https://images.gitee.com/uploads/images/2020/1117/124538_1fe0a1f4_8324729.jpeg "内容3：净化前.jpg")
<br><br/>
## 净化后
![内容3：净化后](https://images.gitee.com/uploads/images/2020/1117/124557_8bc4bb67_8324729.jpeg "内容3：净化后.jpg")
<br><br/>
<br><br/>
# 示范四
──────────────────────────────────
<br><br/>
## 净化前
![内容4：净化前a](https://images.gitee.com/uploads/images/2020/1117/124619_cd5966d9_8324729.jpeg "内容4：净化前A.jpg")
![内容4：净化前b](https://images.gitee.com/uploads/images/2020/1117/124642_ed466262_8324729.jpeg "内容4：净化前B.jpg")
<br><br/>
## 净化后
![内容4：净化后](https://images.gitee.com/uploads/images/2020/1117/124703_10fad736_8324729.jpeg "内容4：净化后.jpg")
