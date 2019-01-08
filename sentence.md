Let's pick up right where we left off last time 
#让我们继续上次的内容

whether or not to ask the server 
#是否询问服务器

We'll spruce this up later with a nice loading icon 
#稍后我们将用一个漂亮的加载图标来美化它

Now we have the logic necessary to authenticate users, but we still need a way for them to log in and out in the UI
#现在我们有了认证用户所需的逻辑，但是我们仍然需要一种方法让用户在UI中登录和退出

It'd be a good idea to change the name of this rule so we can see at a glance what it does
#更改这个规则的名称是个好主意，这样我们就可以一眼看出它的作用

This should never be done on the client-side alone. Always ensure that API routes are protected as well, as we've done in the API middleware section above.
#这绝不应该只在客户端完成。始终确保API路由也受到保护，就像我们在上面的API中间件部分中所做的那样。

It's vitally important to plan an application's data structure before diving straight into writing endpoints and business logic
#在直接编写端点和业务逻辑之前，计划应用程序的数据结构非常重要

Let's consider our RSVP app's intended features at a high level, then we'll extrapolate what our database schema models should look like in order to bring these features to life
#让我们从更高的层次考虑RSVP应用程序的预期功能，然后我们将推断数据库模式模型应该是什么样子的，以便使这些功能发挥作用

First we'll create the necessary schema to leverage our database.
#首先，我们将创建必要的结构来利用数据库。

There are a couple of ways we could do this: either through ... or ... 
#有几种方法可以做到这一点

It's a handy tool to have at your disposal for any MongoDB project, and particularly useful if you need to work with a database that is not hosted on your local machine
#对于任何MongoDB项目，它都是一种方便的工具，如果您需要使用本地机器上没有托管的数据库，那么它尤其有用.

We now have some seed documents to work with so we can get our API and Angular app up and running with data available right off the bat.
#现在我们有了一些种子文档来使用，这样我们就可以立即启动API和Angular应用，并在数据可用的情况下运行它们。

In the next part of the tutorial series, we'll tackle fetching data from the database with a Node API and displaying data with Angular, complete with filtering and sorting
#在本系列教程的下一部分中，我们将使用节点API从数据库中获取数据，并使用Angular显示数据，完成过滤和排序。

You raise an excellent point and this has now been updated, thanks for the great catch! Cheers! 
#你提出了一个很好的观点，现在已经更新了，谢谢你的精彩捕捉!干杯!

The third installment in the series covers fetching data from MongoDB with a Node API and displaying and filtering the data with Angular 
#本系列的第三部分将介绍如何使用节点API从MongoDB获取数据，以及如何使用Angular显示和过滤数据。

Projections state which fields we want returned in the documents that match our query 
#投影表示我们希望在匹配查询的文档中返回哪些字段

In the callback, we'll handle errors and iterate over any results. 
#在回调中，我们将处理错误并遍历所有结果

Pretty straightforward! 
#非常简单

It's worthwhile to note that this endpoint is simply for admin display purposes.
#值得注意的是，这个端点只是用于管理显示目的. 

Since we'll be making asynchronous API calls, it's ideal to also have a loading state. 
#由于我们将进行异步API调用，所以最好也有一个加载状态。

Alternatively, we could use route resolve to prevent routes from loading until the necessary API data has been returned, but this can give an app the appearance of sluggishness while navigating. Instead, we'll show a loading icon with a very simple component.
#或者，我们可以使用route resolve来防止在返回必要的API数据之前加载路由，但这可能会让应用程序在导航时显得迟缓。相反，我们将显示一个带有非常简单的组件的加载图标。

efore we start building out our components, let's make a utility service that we can build on throughout development.
#在开始构建组件之前，让我们先创建一个可以在整个开发过程中构建的实用程序服务。

Open the app.module.ts file and make the following updates 
#打开app.module.ts文件，并作出以下更新:

Angular uses pipes to transform data, but no longer provides out-of-the-box pipes for filtering or sorting for reasons cited here. 
#Angular使用管道来转换数据，但不再提供开箱即用的管道来过滤或排序，原因如下。

There are no equivalents in Angular.This isn't an oversight.
#在Angular中没有等价的,这不是疏忽

If these performance and minification considerations don't apply to you, you can always create your own such pipes 
#如果这些性能和简化考虑不适用于您，您总是可以创建自己的此类管道

In the template, we'll use the structural directive NgIf to dynamically load only the parts of the UI that should be revealed at a particular state of the component. 
#在模板中，我们将使用结构指令NgIf动态加载UI中在组件特定状态下应该显示的部分。

We'll now take measures to protect authorized routes on the front end and manage access to components utilizing protected API routes. 
#现在我们将采取措施保护前端的授权路由，并使用受保护的API路由管理对组件的访问。

Route guards are for the UI only. They don't confer any security when it comes to accessing an API 
#路由守卫仅用于UI。在访问API时，它们不提供任何安全性。

Route guards operate on returning true or false based on a condition that has to be fulfilled to permit navigation.
#路由守卫根据允许导航的条件返回true或false。

It will then clear the redirect from local storage to ensure no lingering data is left behind.
#然后，它将清除本地存储的重定向，以确保没有遗留数据。

Even if a user was somehow able to circumvent the front end protection, the Node API would not return the events data without the correct admin role concealed in the access token.
#即使用户能够绕过前端保护，如果访问令牌中没有隐藏的正确管理角色，节点API也不会返回事件数据。

However, feel free to explore this approach on your own if you prefer. 
#但是，如果您愿意，也可以自己探索这种方法。
