# Đề bài Clean Code & Fix Bug

**Tổng điểm:** 80 điểm + 20 điểm làm việc nhóm = 100 điểm
**Thời gian:** 40 phút

## Phần 1: Nhận diện và Sửa lỗi cơ bản (5 câu, 8 điểm/câu = 40 điểm)

### 1. Đặt tên có ý nghĩa
**Vấn đề:** Tên hàm và tham số chưa mô tả rõ mục đích sử dụng.
```javascript
function calc(x, y) {
    return x + y;
}
```

### 2. Sử dụng hằng số thay vì số cụ thể
**Vấn đề:** Hàm `getCirc` sử dụng một giá trị số cụ thể thay vì dùng hằng số có sẵn.
```javascript
function getCirc(d) {
    return d * 3.14159;
}
```

### 3. Kiểm tra điều kiện logic
**Vấn đề:** Hàm `evalNum` có thể trả về kết quả không đúng với mục đích.
```javascript
function evalNum(val) {
    if (val % 2 !== 0) {
        return "Chẵn";
    } else {
        return "Lẻ";
    }
}
```

### 4. Lựa chọn toán tử so sánh phù hợp
**Vấn đề:** Hàm `compVals` đang sử dụng toán tử so sánh có thể gây nhầm lẫn.
```javascript
function compVals(v1, v2) {
    if (v1 == v2) {
        return true;
    } else {
        return false;
    }
}
// Ví dụ: compVals(5, "5") sẽ trả về true, nhưng nên là false.
```

### 5. Sử dụng comment hiệu quả
**Vấn đề:** Hàm `checkSign` có comment không cần thiết.
```javascript
function checkSign(num) {
    // Kiểm tra xem số có lớn hơn 0 không
    if (num > 0) {
        return true;
    } else {
        return false;
    }
}
```

## Phần 2: Thực hành Viết Code Sạch (5 câu, 8 điểm/câu = 40 điểm)

### 6. Áp dụng nguyên tắc DRY (Don't Repeat Yourself)
**Vấn đề:**
1. Hai hàm `gMorn` và `gEve` có cấu trúc tương tự nhau.
2. Cách nối chuỗi có thể được cải thiện.
```javascript
function gMorn(n) {
    return "Chào buổi sáng, " + n + "! Chúc bạn một ngày tốt lành.";
}

function gEve(n) {
    return "Chào buổi tối, " + n + "! Chúc bạn ngủ ngon.";
}
```

### 7. Nguyên tắc trách nhiệm đơn lẻ
**Vấn đề:** Hàm `handleData` đang thực hiện nhiều nhiệm vụ khác nhau.
```javascript
function handleData(name, age) {
    // Kiểm tra tuổi
    let adultFlag = false;
    if (age >= 18) {
        adultFlag = true;
    }

    // In thông tin
    console.log("Tên: " + name);
    console.log("Tuổi: " + age);
    if (adultFlag) {
        console.log("Đây là người lớn.");
    } else {
        console.log("Đây là trẻ em.");
    }
}
```

### 8. Cải thiện cấu trúc điều kiện
**Vấn đề:** Điều kiện trong hàm `canView` khó đọc và hiểu.
```javascript
function canView(usr) {
    // Người dùng có quyền xem nếu là 'admin' HOẶC (là 'editor' VÀ đã 'active')
    if (usr.r === 'admin' || (usr.r === 'editor' && usr.s === 'active')) {
        return true;
    }
    return false;
}
```

### 9. Cú pháp hàm hiện đại
**Vấn đề:** Hàm `timesTwo` có thể được viết ngắn gọn hơn với cú pháp hiện đại.
```javascript
// Hàm này nhận một số và trả về gấp đôi số đó
function timesTwo(val) {
    return val * 2;
}
```

### 10. Quản lý phạm vi biến
**Vấn đề:**
1. Code thiếu một chỉ thị để đảm bảo an toàn.
2. Biến trong hàm `showMsg` được khai báo không đúng cách.
```javascript
// (Không có 'use strict';)

function showMsg() {
    gMsg = "Chào mừng bạn đến với trang web của chúng tôi!"; // Biến toàn cục không khai báo
    console.log(gMsg);
}

showMsg();
```