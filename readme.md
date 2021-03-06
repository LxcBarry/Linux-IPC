# 测试文件格式
测试文件位于test/

```
n     //  音乐厅座位排数 
m     //  每排座位数 
k     //  代理个数 
r vt   //  预约的有效期（单位分钟） 
agent 1 
reserve reserve_time (单位秒) 
ticket ticket_time   (单位秒) 
cancel cancel_time   (单位秒) 
check_customer check_time (单位秒) 
  : 
有效的交易列表 
  :
```

有效交易格式
```
reserve <座位描述> name_of_customer  // 为某客户预订指定座位的票 
ticket <座位描述> name_of_customer   // 为某客户购买指定座位的票 
cancel <座位描述> name_of_customer   // 为某客户取消指定座位的预订 
show all name_of_customer            // 显示某客户的预订或购票情况 
```

有效地址格式

```
"A 2" // 第 A 行，第 2 座 
"A 4 7" // 第 A 行，第 4 到 7 座 
"A" // 第 A 行 
"A 2r" // 从第 A 行开始的 2 行 
"A 2c" // 第 A 行，2 个座位（不在意具体列） 
"6" // 6 个座位（不在意具体行和列）
```
# 运行方式

```sh
# 打开终端，先到项目目录下

# 编译
make clean
make

# 测试地址格式
./main test/different_type_pos.txt 

# 测试退票和预约
./main test/reserve_cancel.txt 

# 测试购票和显示
./main test/ticket_show.txt

# 示例运行文档
./main test/all_test.txt 
```

# 详细实验报告
[readme.pdf](./readme.pdf)

希望参考本代码的同学有所收获，如果能点击一下star就更好了:)
