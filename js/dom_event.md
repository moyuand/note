## 代码示例

```html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>动态表格</title>
	<style>
		.btns {
			margin-bottom: 5px;
		}
		.btn {
			display: inline-block;
			padding: .5em 2em;
			background-color:teal;
			border-top: 3px;
			color: #fff;
			cursor: pointer;
		}
		table.table{
			box-sizing: border-box;
			width: 100%;
			border-collapse: collapse;
		} 
		table.table th,
		table.table td {
			border:1px solid #ccc;
			line-height: 2em;
			text-align: center;  
		}
		.none {
			display: none;
		}
	</style>
</head>
<body>
	<div class="btn" id="btn_add">添加</div>
	<div class="btn">批量导入</div>
	<div class="btn">批量删除</div>
	<table class="table">
		<thead>
			<tr>
				<td width="60px">编号</td>
				<td width="200px">姓名</td>
				<td>性别</td>
				<td>手机</td>
				<td width="100px">操作</td>
			</tr>
		</thead>
		<tbody>
			<tr class="none">
				<td><input type="checkbox"></td>
				<td></td>
				<td></td>
				<td></td>
				<td>
					<a href="javascript:void(0)" class="btn_del" >删除</a>
					<a href="javascript:void(0)" class="btn_upd">修改</a>
				</td>
			</tr>
		</tbody>
	</table>
	<script>
		// function handle() {
		// 	// body...
		// 	alert(1);
		// }
		var btn_add = document.getElementById('btn_add');
		var tbody = document.getElementsByTagName('tbody')[0];
		// var btn_dels = document.getElementByClassName('btn_del');
		//为删除按钮绑定事件处理函数
		tbody.onclick = function(event){
			var target = event.target;
			console.log(event);
			console.log(target);
			if (target.nodeName ==="A") {
				if (target.className === "btn_del") {
					alert("确定删除吗？");
					tbody.removeChild(target.parentNode.parentNode);
				}
				if (target.className === "btn_upd") {
					alert("确定新增吗？");
				}
			}
			console.log(event)
		}
		// for(var key;key<btn_dels.length;i++){
		// 	var btn_del = 
		// }
		// console.log(tbody.firstElementChild);
		//为添加按钮绑定时间
		 btn_add.onclick = function(){
		 	//产生一个tr
		 	var newTr = tbody.firstElementChild.cloneNode(true);
		 	newTr.children[1].innerHTML = "<strong>"+Math.random()+"</strong>";
		 	newTr.className = "";
		 	tbody.appendChild(newTr);
		 	console.log(newTr);
		 }
	</script>
</body>
</html>
```

