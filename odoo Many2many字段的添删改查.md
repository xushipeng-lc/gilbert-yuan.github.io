## odoo Many2many字段的添删改查
many2many

(0,0,{values}) 根据values里面的信息新建一个记录。

(1,ID,{values})更新id=ID的记录（写入values里面的数据）

(2,ID) 删除id=ID的数据（调用unlink方法，删除数据以及整个主从数据链接关系）

(3,ID) 切断主从数据的链接关系但是不删除这个数据

(4,ID) 为id=ID的数据添加主从链接关系。

(5) 删除所有的从数据的链接关系就是向所有的从数据调用(3,ID)

(6,0,[IDs]) 用IDs里面的记录替换原来的记录（就是先执行(5)再执行循环IDs执行（4,ID））

例子[(6, 0, [8, 5, 6, 4])] 设置 many2many to ids [8, 5, 6, 4]

