# this 绑定的四种规则

- 默认绑定
    - 独立函数调用
- 隐式绑定
    - 对象的属性调用
- 显示绑定
    - call ...
    - apply []
    - bind 返回一个函数
- new 绑定
    - 1. 创建一个空对象
    - 2. this 指向这个空对象
    - 3. 执行函数代码
    - 4. 如果函数没有显示的返回非空对象，默认返回这个空对象

# 内置函数的 this

# setTimeout
    - function
        - window
    - () => {}
        - 作用域链找 this

# DOM 事件
    - function
        - DOM Element
    - () => {}
        - window

# forEach
    - function
        - window
    - () => {}
        - window
    - 指定
        - function 指定的对象
        - () => {} window

# 绑定规则的优先级

- new > 显示 > 隐式 > 默认

# 其他情况

- apply/call 传入 null/undefined
    - 使用 默认绑定
- 间接函数引用
    - 直接调用函数 window
