#配置安装以及开发文档
--------------------
* 简介
* 控制器
* ORM
* 标签

##简介
----

##标签
----
* 对象
* if-else
* 循环
* 嵌套循环
* 循环嵌套 if-else

```PHP
###对象
----
//对象成员变量
{#value['title']}

###if-else
-------

{if @value['is_private'] == 1}
{else}
{/if}
支持的比较运算操作符:==、!=、>、<、<=、>=

###循环
----

//循环变量
{foreach $articles(key,value)} 
		{@value}
{/foreach}

//循环对象成员变量
{foreach $articles(key,value)} 
		{@value['title']}
{/foreach}



###嵌套循环
--------
//嵌套循环变量
{foreach $articles(key,value)} 
	{foreach #value(v_key,v_value)} 
		{@v_value}
	{/foreach}
{/foreach}

//嵌套循环对象成员变量
{foreach $articles(key,value)} 
	{foreach #value(v_key,v_value)} 
		{@v_value['title']}
	{/foreach}
{/foreach}



###嵌套循环if-else
---------------
{foreach $articles(key,value)} 
		{if @value['title'] }
		{else}
		{/if}
{/foreach}


```
