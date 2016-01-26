
<h1>Dialogbox API</h1>

<a href="javascript:;" id="default">default</a>
<pre>
$('#default').on('click',function(){
  var data = '&lt;div style="padding:20px;"&gt;这是内容&lt;br /&gt;这是内容&lt;br /&gt;这是内容&lt;/div&gt;';
  $.dialogbox({
    type:'default',
    title:'标题',
    content:data,
    closeCallback:function(){
      $.dialogbox.prompt({
        content:'关闭了对话框',
        time:2000 
      });
    }
  });
});
</pre>
<br />
<a href="javascript:;" id="alert">alert</a>
<pre>
$('#alert').on('click',function(){
  $.dialogbox({
    type:'msg',
    title:'提示',
    icon:1,
    content:'图片已上传成功！',
    btn:['确定'],
    call:[
      function(){
        $.dialogbox.close(); 
      }
    ]
  });
});
</pre>
<br />
<a href="javascript:;" id="confirm">confirm</a>
<pre>
$('#confirm').on('click',function(){
  $.dialogbox({
    type:'msg',
    title:'提示',
    content:'您确定要删除图片吗？',
    closeBtn:true,
    btn:['确定','取消'],
    call:[
      function(){
        $.dialogbox.close(); 
      },
      function(){
        $.dialogbox.close(); 
      }
    ]
  });
});
</pre>
<br />
<a href="javascript:;" id="iframe">iframe</a>
<pre>
$('#iframe').on('click',function(){
  $.dialogbox({
    type:'iframe',
    title:'百度',
    content:'下面是百度首页',
    url:'http://www.baidu.com',
    width:900,
    height:650
  });
});
</pre>
<br />
<a href="javascript:;" id="prompt">prompt</a>
<pre>
$('#prompt').on('click',function(){
  $.dialogbox.prompt({
    content:'提交成功',
    time:2000 
  });
});
</pre>
