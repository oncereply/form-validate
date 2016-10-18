form-validate
=============

# 使用示例
引入js文件
```html
<script src=".../form-validate/form-validate.js"></script>
```
HTML
```html
<input type="text" id="username" name="username" placeholder="用户名" value=""
       form-pattern=".{6,50}" form-classtarget="#group-username"
       form-correctclass="has-success" form-errorclass="has-error"
       form-msgtarget="#msg-username" form-msg="请输入6~50位的字符">
```
javascript
```javascript
$('form').formValidate({
    success: function () {
        // Do ajax request
        $.post(this.action, $(this).serializeArray()).done(function (data) {

        });
        return false;
        // If you return true, do normal form submit.
    }
});
```
