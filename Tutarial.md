CHƯƠNG I: Javascript có thể làm gì?
a, Code Frontend: React JS, Vue, Angular
b, Code Backend (NodeJS, Express)
c, Code App mobile (React Native, Flutter)
d, Code Game (Cocos, BabylonJS)

JS là ngôn ngữ bất đồng bộ, khác so với các nn đồng bộ như Java, C++, PHP,... ở chỗ nó không chạy lần lượt code từ trên xuống dưới mà sẽ chạy toàn bộ code cùng lúc nên sẽ đem lại trải nghiệm liền lạc hơn trên web, giúp web không phải load lại trang mà vẫn update được nội dung. Ngoài ra, các câu lệnh chạy mất thời gian nhưng đứng trên vẫn sẽ trả lại kết quả sau những câu lệnh phía dưới, khác so với các ngôn ngữ đồng bộ là phải chờ lệnh trên chạy xong thì mới đến lệnh dưới. Vì thế JS cho tốc độ xử lý trên web nhanh hơn.

CHƯƠNG II: Javascript cơ bản
1. Biến
- Hằng: const
- Biến thay đổi đc: Let, Var
    + Let: biến cục bộ, giá trị trong 1 vòng lặp hoặc function,... chỉ có tác dụng trong đó, ra ngoài sẽ biến mất
    + Var: Biến toàn cục, giá trị áp dụng cho toàn bộ.
2. Kiểu dữ liệu
- Number: 5,4,6,3.2,...
- String: `Đây là dữ liệu`
- Boolean: true/fail
3. String Methods
- str.length 
//Tính độ dài chuỗi
- str.slice(7,10) 
//cắt chữ tù ký tự thứ 7-10
- text.replace("Microsoft", "OK luôn") 
//Thay thế Microsoft thành OK luôn
- text1.toUpperCase() 
//In hoa
- text1.toLowerCase() 
//Phản in hoa
...

- In ra giá trị biến trong chuỗi: ${a}
4. Object
- Khởi tạo:
let a = {
    name: `babc`,
    age: 23,
    sing: function() {
        console.log(`La la la`)
    }
}
- Lấy giá trị:
a.name; a.age; a.sing;
- Thêm key: a[address]

5. Array
- Khởi tạo:
let arr = [1,2,3,4,5]
- Lấy giá trị: arr[index]

6. Các control Flow Basics
// For loop
for(let i=0, i<5, i++)
{
    console.log(i);
}
// While do
let i=0
while (i<5) {
    console.log(`La la la`);
    i++;
}
// If else
if (i=0) {
    console.log(`La la la`);
}
else {console.log(`La la la`);}
// Switch case
switch (a){
    case 0: console.log(a); break;
    case 1: console.log(a); break;
    case 2: console.log(a); break;
}

7. Function & methods
- Khởi tạo:
function sum(a,b) {
    return a+b;
}
- Arrow function: 
let sum = (a,b) => {
    return a+b;
}
- Callback:
let sum = (a,b) => {
    let tong= a+b;
    print(tong);
}
let print =(a) => {console.log(a);}
sum(23,2,print);

- setTimeout: thực thi lệnh sau 1 khoảng thời gian
setTimeout (() => {
    console.log(`OK luôn`);
}, 500);

- setInterval: thực thi lệnh vô hạn sau 1 khoảng thời gian
let i=0;
let timer = setInterval(() => {
    console.log(`OK luôn`);
    i++;
    if (i===5) {
        clearInterval(timer) //Xóa timer
    }
}, 500);

8. Array methods
- Filter/Find: filter trả lại 1 mảng, find trả lại 1 phần tử
 let filter = arr.filter((item, index) => {
    return item && item.age === 25;
 })

 let find = arr.find((item, index) => {
    return item && item.age === 25;
 })

 - Map: duyệt 1 mảng, thực hiện lệnh và tạo thành 1 mảng mới
 let mapArr = arr.map((item, index) => {
    item = item*2;
    return item;
 })

 - Sort: sắp xếp mảng
 arr.sort((item1, item2) => {
    return item1 - item2;
 }) 
 //sắp xếp mảng tăng dần

9. Các kiến thức khác: