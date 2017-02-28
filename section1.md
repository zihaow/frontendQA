<h1>前端面试题</h1>

<ul>
	<li><strong>1.在浏览器地址访问一个url 发生了什么事情</strong>
		<p>当输入URL地址时，浏览器首先会请求DNS服务器，通过DNS查询获取相应的域名所对应的IP地址，然后通过这个映射的IP地址找到IP对应的服务器，并建立连接，等浏览器发送完HTTP Request包后，服务器接送到请求包才开始处理，返回HTTP Response（响应）包后，客户端浏览器收到服务器响应后就开始渲染Response包的主体（body）部分，等收到全部内容后断开与该服务器之间的连接。
		</p>
		<p>参考文章:
			http://www.ruanyifeng.com/blog/2016/08/http.html
			http://www.qixing318.com/article/the-http-protocol-handling-process.html
			http://www.liaoxuefeng.com/wiki/001374738125095c955c1e6d8bb493182103fac9270762a000/001386832653051fd44e44e4f9e4ed08f3e5a5ab550358d000
		</p>		
	</li>
	<li><strong>2.HTML页面的渲染过程？（可以引出第3题）</strong>
		<p>
			需了解关键呈现路径（CRP）
			DOM => CSSDOM => Render Tree => Layout => Paint
			<img src="/resource/img/CRP.jpg" alt="">			
			当用户请求页面时，浏览器会抓取HTML同时生成DOM，然后抓取CSS并建立CSS对象模型，最后通过匹配DOM和CSS对象生成渲染树。在需要处理的JavaScript文件被解决之前，浏览器不会开始对页面进行渲染。作为开发者，我们要明确的告诉浏览器不要等待，直接开始渲染。具体方法是使用HTML中的defer和async两个属性。(defer和async两个属性区别？)
			async指的异步脚本，即脚本异步加载，加载的过程不会造成阻塞，但是async的脚本的执行时机是不确定的，而且执行的顺序也是不确定的，因此使用async的脚本应该是不依赖于任何代码的脚本(比如第三方统计代码或广告代码)，否则就会导致执行出错。          
		</p>
		<p>参考文章:
			https://gold.xitu.io/entry/582492025bbb5000590ef04d/		
			http://www.jb51.net/article/93004.htm   
		</p>		
	</li>
	<li>3.<strong>前端性能优化方式，在实际项目中的优化例子</strong>
		<p>
		</p>		
	</li>
	<li><strong>前端缓存相关知识点</strong>
		<p>
		</p>
		<p>参考文章:

		</p>		
	</li>
	<li><strong>解释一下CSS盒子对象，什么情况下可以使盒子的宽度等于宽度+边框+padding？以及什么情景下需要这样做？</strong>
		<p>
			使用box-sizing:border-box属性。要一个元素的宽度严格是其父元素的某个百分比，但是又要给其子元素周边留出点空白
		</p>
		<p>参考文章:
		</p>	
	</li>
	
	<li><strong>跨域相关知识点，如何实现跨域？跨域时会发送多少个请求？JSONP的实现以及为何它能解决跨域问题？</strong>
		<p>
		</p>
		<p>参考文章:

		</p>		
	</li>
	<li><strong>你对JS面向对象编程的理解？如何创建对象？子类父类继承等相关知识</strong>
		<p>
		Way 1
		function person(fname,lname,age,eyecolor)
		{
		   this.firstname=fname;
		   this.lastname=lname;
		   this.age=age;
		   this.eyecolor=eyecolor;
		}

		myFather=new person("John","Doe",50,"blue");
		document.write(myFather.firstname + " is " + myFather.age + " years old.");
		</p>
		<p>
		Way 2
		var Robot =
		{
		    metal: "Titanium",
		    killAllHumans: function()
		    {
			alert("Exterminate!");
		    }
		};
		Robot.killAllHumans();
		</p>
		<p>
		var NewObject = {};
		NewObject['property1'] = value;
		NewObject['property2'] = value;
		NewObject['method'] = function(){ /* function code here */ }
		</p>
		<p>
		Use way 1 if you want to create several similar objects. In your example, Person (you should start the name with a capital 		  letter) is called the constructor function. This is similar to classes in other OO languages.
		</p>
		<p>
		Use way 2 if you only need one object of a kind (like a singleton). If you want this object to inherit from another one, 		then you have to use a constructor function though.
		</p>
		<p>
		Use way 3 if you want to initialize properties of the object depending on other properties of it or if you have dynamic 		property names.
		</p>
		<p>参考文章:

		</p>		
	</li>
	<li><strong>JS事件机制，当点击页面一个元素时发生了什么，事件捕获过程？</strong>
		<p>
		</p>
		<p>参考文章:
		</p>		
	</li>
	
	<li><strong>RESTFUL API的理解</strong>
		<p>
		</p>
		<p>参考文章: http://stackoverflow.com/questions/6843951/which-way-is-best-for-creating-an-object-in-javascript-is-var-necessary-befor
		</p>		
	</li>
	<li><strong>微信JSSDK如何授权和调用API，实际应用例子？</strong>
		<p>
		</p>
		<p>参考文章:
		</p>		
	</li>
</ul>
