# Cơ bản ban đầu #
1. ghi chú 
- Ghi chú trong Python được thể hiện bằng một dấu thăng (#), và bất kỳ thứ gì 
đứng sau dấu thăng trên dòng đó đều bị bỏ qua
2. Khoảng trắng 
- trong python khoảng trắng cũng có nghĩa: các khối mã được biểu thị bằng cách thụt lề.
- khoảng trắng trong cùng 1 dòng của đoạn mã Python
không quan trọng
- Biến Python là con trỏ: Gán biến trong Python rất dễ dàng chỉ bằng cách đặt tên biến bên trái dấu bằng 
(=): ví dụ: x=4
=>  các biến Python chỉ trỏ
đến các đối tượng khác nhau, nên không cần phải “khai báo” biến

## Data Type: ##
Các loại dữa liệu:
- Text Type:	str
- Numeric Types:	int, float, complex
- Sequence  (trình tự) Types:	list, tuple, range
- Mapping Type:	dict
- Set Types:	set, frozenset
- Boolean Type:	bool
- Binary (nhị phân) Types:	bytes, bytearray, memoryview

CỤ Thể:
|Kiểu dữ liệu| Ví dụ | Mô tả |  
|------------|-------|-------|
|int| x = 1 |nSố nguyên |
|float| x = 1.0 |Số thực dấu phẩy động|
|complex| x = 1 + 2j |Số phức (số có phần thực và phần ảo)|
|bool| x = True| Boolean: Đúng hoặc Sai|
|str |x = ‘abc’ |Chuỗi: ký tự và chữ số|
|NoneType| x = None |Biểu diễn đối tượng không có giá trị|

### Kiểu dữ liệu tích hợp ###
 - Bên cạnh những kiểu dữ liệu đơn giản như trên, Python cũng có một số kiểu dữ liệu hỗn hợp được tích hợp sẵn, hoạt động như những bình chứa cho các kiểu dữ liệu khác. Những kiểu hỗn hợp đó là:  

 |Kiểu dữ liệu| Ví dụ | Mô tả |  
 |------------|-------|-------|  
 |list|[1, 2, 3]|Tổ hợp có thứ tự|  
 | tuple|(1, 2, 3)  |Tổ hợp bất biến có thứ tự |  
|dict |{‘a’:1, ‘b’:2, ‘c’:3} |Tổ hợp không có thứ tự các cặp khóa, giá trị|  
|set |{1, 2, 3} |Tổ hợp không có thứ tự các giá trị duy nhất|  

Cụ thể
 - Danh sách (list): Danh sách là kiểu dữ liệu tổ hợp có thứ tự và có thể thay đổi cơ bản trong Python. Nó có thể được định nghĩa bằng cách đặt những giá trị được ngăn cách bằng dấu 
phẩy vào giữa cặp dấu ngoặc vuông
- trong 1 danh sách có thể chứa các đối tượng thuộc bất cứ kiểu dữ liệu nào.

- Tuple: Khá tương đồng với list nhưng được định nghĩa bằng cặp dấu ngoặc đơn thay vì ngoặc vuông. hoặc cũng có thể được định nghĩa mà không cần dấu ngoặc nào.  
Ví dụ:  
t = 1, 2, 3  
  print(t)
- Dictionary: Từ điển là tổ hợp cực kì linh hoạt thể hiện tương quan giữa các cặp khóa (key)
và giá trị (value)
- Set:  định nghĩa rất giống list và Tuple, ngoại trừ việc nó dùng cặp dấu ngoặc nhọn như Dictionary

## Control Flow ## 
### Câu lệnh điều kiện: if, elif và else ###
- Câu lệnh điều kiện, thường được gọi là câu lệnh if-then, cho phép thực thi các đoạn mã nhất định phụ thuộc vào một số điều kiện. Ví dụ: 
a = 200  
b = 33  
if b > a:  
  print("b is greater than a")  
elif a == b:  
  print("a and b are equal")  
else:  
  print("a is greater than b") 

Sử dụng dấu hai chấm (:) và khoảng trắng để biểu thị các 
khối mã riêng biệt.

- Vòng lặp for: Vòng lặp trong Python là cách để lặp lại việc thực thi một số câu lệnh. Ví dụ, nếu muốn in ra từng mục trong một danh sách, ta có thể sử dụng vòng lặp for:
for N in [2, 3, 5, 7]:  
  print(N, end=' ') 
  #in ra trên cùng 1 dòng
for N in [2, 3, 5, 7]:  
   print(N) #in ra trên mỗi dòng
for i in range(10):
   print(i, end=' ')

- Vòng lặp while: Một kiểu vòng lặp khác trong Python là vòng lặp while, nó sẽ tiến hành lặp cho đến khi thỏa mãn một số điều kiện:
i = 0  
   while i < 10:
     print(i, end=' ')
          i += 1

Tinh chỉnh vòng lặp với break và continue  
Có hai câu lệnh hữu ích được sử dụng trong vòng lặp để tinh chỉnh cách mà chúng 
thực thi:  
  - Câu lệnh break để thoát hoàn toàn khỏi vòng lặp
  - Câu lệnh continue để bỏ qua phần còn lại của lần lặp hiện tại và tiến đến lần lặp tiếp theo.
Chúng có thể sử dụng trong cả vòng lặp for và while.  
**Ví dụ** 
 - Break:  
  a, b = 0, 1  
  amax = 100  
  L = []  
  while True:  
    (a, b) = (b, a + b)  
    if a > amax:
       break  
    L.append(a)  
  print(L)  
- continue: 
                    for n in range(20):  
                    #kiểm tra xem n có chẵn không  
                      if n % 2 == 0:   
                      continue  
                    print(n, end=' ')
## Hàm ##
 - Hàm (Function) là những nhóm mã có tên và có thể gọi bằng cách sử dụng dấu 
ngoặc đơn
-  Trong Python, hàm được định nghĩa bằng câu 
lệnh def. 
  
x=int(input("Nhập số cần tính giai thừa:"))  
def fact(x):  
    if x == 0:  
      return 1  
    return x * fact(x - 1)  
print (fact(x))  
y = 2   
z = (x**y)   
print (z) 