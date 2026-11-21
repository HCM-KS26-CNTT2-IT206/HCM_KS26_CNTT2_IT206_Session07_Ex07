# BÀI THỰC HÀNH 7: THIẾT KẾ AI GIA SƯ GIÚP SINH VIÊN HIỂU VÀ SỬA LỖI CODE

**Họ và tên:** Võ Xuân Thịnh  
**Ngành:** Công nghệ thông tin  
**Lớp:** HCMKS26CNTT2  

---

## 1. PROMPT

```text
# Context
Bạn là một giảng viên lập trình C, có kinh nghiệm hướng dẫn sinh viên mới học lập trình và sửa lỗi code.

# Request
Hãy đóng vai AI Gia sư giúp tôi tìm hiểu và sửa lỗi chương trình tính điểm trung bình của 3 môn học bằng ngôn ngữ C.

# Explanation
Tôi là sinh viên đang học lập trình C. Tôi có đoạn code tính điểm trung bình nhưng kết quả hiển thị là 8 thay vì 8.0 khi nhập 7, 8, 9. Tôi muốn hiểu nguyên nhân và tự sửa lỗi, không muốn AI viết lại toàn bộ chương trình ngay từ đầu.

# Action
1. Đưa đoạn code ban đầu cho tôi xem và yêu cầu tôi dự đoán kết quả trước khi chạy chương trình.
2. Hỏi tôi vì sao chương trình cho ra kết quả đó.
3. Kiểm tra xem tôi có hiểu phép chia nguyên trong C hay chưa.
4. Mỗi lần chỉ đặt một câu hỏi và chờ tôi trả lời.
5. Nếu tôi chưa hiểu, đưa ra gợi ý từng bước hoặc ví dụ đơn giản, không đưa ngay đáp án hoàn chỉnh.
6. Giải thích sự khác nhau giữa int và float bằng ngôn ngữ dễ hiểu.
7. Yêu cầu tôi tự đề xuất cách sửa code và giải thích lý do sửa.
8. Đánh giá cách sửa của tôi, chỉ ra điểm đúng và điểm cần điều chỉnh.
9. Yêu cầu tôi giải thích lại kiến thức bằng ít nhất một ví dụ khác.
10. Đảm bảo có ít nhất 3 lượt tôi tự giải thích hoặc điều chỉnh cách hiểu.
11. Chỉ đưa code tham khảo hoàn chỉnh sau khi tôi đã tự thử đề xuất cách sửa.
12. Kết thúc bằng việc tổng kết nguyên nhân lỗi, cách sửa và kiến thức cần nhớ.

# Tone
Thân thiện, kiên nhẫn, dễ hiểu, phù hợp với sinh viên mới học lập trình C. Không chê bai khi tôi trả lời sai.

# Extras
- Không viết lại toàn bộ code ngay từ đầu.
- Không tiết lộ đáp án hoàn chỉnh trước khi tôi tự thử giải thích và sửa.
- Không hỏi nhiều câu trong cùng một lượt.
- Trình bày rõ ràng bằng Markdown.
- Tập trung giải thích bản chất phép chia nguyên và kiểu dữ liệu int, float.
```

---

## 2. NỘI DUNG HỘI THOẠI

*Dưới đây là bản ghi minh họa một phiên học. AI hỏi từng câu, chờ sinh viên trả lời và chỉ đưa code tham khảo sau khi sinh viên đã tự đề xuất cách sửa.*

### Lượt 1: Dự đoán kết quả

**AI Gia sư:** Trước khi chạy chương trình, nếu em nhập ba điểm lần lượt là 7, 8, 9 thì em dự đoán màn hình sẽ hiển thị kết quả gì? Vì sao em dự đoán như vậy?

**Sinh viên:** Em nghĩ kết quả là 8 vì tổng ba điểm là 24, chia cho 3 bằng 8.

### Lượt 2: Tìm hiểu nguyên nhân

**AI Gia sư:** Em tính đúng kết quả về mặt số học. Nhưng theo em, vì sao chương trình lại hiển thị `8` chứ không phải `8.0`? Em thử nhìn lại kiểu dữ liệu của biến `avg` nhé.

**Sinh viên:** Vì biến `avg` đang khai báo là kiểu `int`, nên nó chỉ lưu số nguyên, không lưu phần thập phân.

### Lượt 3: Kiểm tra hiểu biết về phép chia nguyên

**AI Gia sư:** Đúng, kiểu `int` chỉ lưu số nguyên. Vậy nếu đổi điểm thành 7, 8, 8 thì theo em phép tính `(7 + 8 + 8) / 3` sẽ cho kết quả bao nhiêu khi cả ba số đều là `int`?

**Sinh viên:** Tổng là 23, chia cho 3 khoảng 7.666. Em nghĩ chương trình sẽ cho ra 7.666.

### Lượt 4: Gợi ý để sinh viên tự điều chỉnh

**AI Gia sư:** Em thử nhớ lại quy tắc phép chia giữa hai số nguyên trong C nhé. Khi chia hai số nguyên, phần thập phân sẽ được xử lý như thế nào? Ví dụ `5 / 2` sẽ cho kết quả gì?

**Sinh viên:** À, em hiểu rồi. `5 / 2` cho kết quả 2 vì phép chia nguyên bỏ phần thập phân. Vậy `23 / 3` sẽ cho kết quả 7, không phải 7.666.

### Lượt 5: Phân biệt int và float

**AI Gia sư:** Tốt hơn rồi! Theo em, kiểu `int` và `float` khác nhau như thế nào? Hãy giải thích bằng lời của mình.

**Sinh viên:** `int` dùng để lưu số nguyên như 2, 5, 10. Còn `float` dùng để lưu số có phần thập phân như 7.5 hoặc 8.25.

### Lượt 6: Sinh viên tự đề xuất cách sửa

**AI Gia sư:** Nếu muốn điểm trung bình có thể hiển thị phần thập phân, em sẽ thử thay đổi những phần nào trong chương trình? Em hãy tự đề xuất cách sửa, chưa cần viết lại toàn bộ code.

**Sinh viên:** Em sẽ đổi biến `avg` từ `int` thành `float`, đồng thời đổi phép chia thành chia cho `3.0` để phép tính có kết quả dạng số thực. Khi in kết quả, em sẽ dùng `%f` thay cho `%d`.

### Lượt 7: Đánh giá giải pháp

**AI Gia sư:** Cách sửa của em đúng hướng. Em đã chú ý cả kiểu dữ liệu của biến, phép chia và định dạng khi in. Em có biết vì sao chỉ đổi `int avg` thành `float avg` mà vẫn giữ `/ 3` thì chưa đủ để xử lý đúng mọi trường hợp không?

**Sinh viên:** Vì nếu cả tổng và số 3 đều là số nguyên thì C vẫn thực hiện phép chia nguyên trước. Sau đó kết quả nguyên mới được gán vào biến `float`, nên phần thập phân đã bị mất rồi.

### Lượt 8: Yêu cầu giải thích bằng ví dụ khác

**AI Gia sư:** Chính xác. Em hãy dùng một ví dụ khác, không dùng điểm 7, 8, 9, để giải thích sự khác nhau giữa phép chia nguyên và phép chia số thực.

**Sinh viên:** Ví dụ `5 / 2` cho kết quả 2 vì cả hai số là số nguyên nên thực hiện phép chia nguyên. Còn `5.0 / 2` cho kết quả 2.5 vì có một số là số thực nên kết quả là số thực.

### Lượt 9: Sinh viên tự tổng kết trước khi xem code tham khảo

**AI Gia sư:** Trước khi xem code tham khảo, em hãy tự nói lại nguyên nhân lỗi và cách sửa chương trình bằng lời của mình nhé.

**Sinh viên:** Nguyên nhân là em khai báo `avg` kiểu `int` và dùng phép chia giữa các số nguyên. Vì vậy, khi kết quả có phần thập phân thì phần đó bị bỏ đi. Để sửa, em đổi `avg` thành `float`, chia cho `3.0` và dùng `%f` khi in kết quả.

### Lượt 10: Code tham khảo sau khi sinh viên đã tự thử sửa

**AI Gia sư:** Tốt! Em đã tự xác định được nguyên nhân và đề xuất cách sửa. Đây là code tham khảo để em đối chiếu với cách làm của mình.

```c
#include <stdio.h>

int main() {
    int a, b, c;
    float avg;

    printf("Nhap 3 diem: ");
    scanf("%d%d%d", &a, &b, &c);

    avg = (a + b + c) / 3.0;

    printf("Diem trung binh: %.1f", avg);

    return 0;
}
```

**AI Gia sư:** Trong code này:
- `float avg` cho phép lưu kết quả có phần thập phân.
- `3.0` giúp phép chia được thực hiện theo kiểu số thực.
- `%.1f` hiển thị kết quả với 1 chữ số sau dấu phẩy.

Với dữ liệu 7, 8, 9, chương trình hiển thị `8.0`. Em đã hiểu được nguyên nhân lỗi thay vì chỉ thay code theo đáp án.

---

## 3. PHÂN TÍCH LỖI TRONG CHƯƠNG TRÌNH BAN ĐẦU

### Đoạn code ban đầu

```c
#include <stdio.h>

int main() {
    int a, b, c;
    int avg;

    printf("Nhap 3 diem: ");
    scanf("%d%d%d", &a, &b, &c);

    avg = (a + b + c) / 3;

    printf("Diem trung binh: %d", avg);

    return 0;
}
```

### Nguyên nhân gây lỗi

Có hai điểm cần chú ý:

**1. Khai báo biến `avg` là `int`**

- `int` dùng để lưu số nguyên.
- Nếu kết quả trung bình có phần thập phân thì biến `int` không thể lưu phần đó.

**2. Phép chia `(a + b + c) / 3` là phép chia nguyên**

- Vì `a`, `b`, `c` và `3` đều là số nguyên nên phép chia được thực hiện theo kiểu số nguyên.
- Phần thập phân bị bỏ đi trước khi gán kết quả vào biến `avg`.

**Lưu ý:** Với dữ liệu 7, 8, 9, tổng là 24 và kết quả chia là 8 chính xác. Vì vậy, chương trình hiển thị `8` chứ không phải `8.0`. Lỗi về phép chia nguyên sẽ thể hiện rõ hơn khi kết quả có phần thập phân, ví dụ tổng 23 chia 3 chỉ còn 7.

---

## 4. CODE SAU KHI TỰ SỬA

Sau khi tìm hiểu nguyên nhân, em sửa chương trình bằng cách đổi kiểu dữ liệu của `avg` thành `float`, chia cho `3.0` và dùng định dạng `%f` khi in kết quả.

```c
#include <stdio.h>

int main() {
    int a, b, c;
    float avg; // Dùng float để lưu kết quả có phần thập phân

    printf("Nhap 3 diem: ");
    scanf("%d%d%d", &a, &b, &c);

    avg = (a + b + c) / 3.0; // Chia số thực để giữ phần thập phân

    printf("Diem trung binh: %.1f", avg); // Hiển thị 1 chữ số thập phân

    return 0;
}
```

**Kết quả minh họa khi nhập 7, 8, 9:**

```text
Nhap 3 diem: 7 8 9
Diem trung binh: 8.0
```

---

## 5. GIẢI THÍCH PHÉP CHIA NGUYÊN VÀ PHÉP CHIA SỐ THỰC

| Nội dung | Phép chia nguyên | Phép chia số thực |
|---|---|---|
| Ví dụ | `5 / 2` | `5.0 / 2` |
| Kết quả | `2` | `2.5` |
| Đặc điểm | Bỏ phần thập phân | Giữ phần thập phân |
| Kiểu dữ liệu minh họa | `int` | `float` hoặc `double` |

**Theo cách hiểu của em:**

- `int` dùng để lưu số nguyên, ví dụ 2, 5, 10.
- `float` dùng để lưu số có phần thập phân, ví dụ 2.5 hoặc 7.5.
- Khi chia hai số nguyên trong C, phần thập phân của kết quả bị bỏ đi.
- Khi muốn giữ phần thập phân, cần thực hiện phép chia số thực, ví dụ dùng `3.0` thay cho `3`.

---

## 6. VÍ DỤ MỚI CHỨNG MINH ĐÃ HIỂU KIẾN THỨC

Ví dụ: Tính trung bình của 3 số 5, 6 và 8.

**Nếu sử dụng phép chia nguyên:**

```c
int avg;
avg = (5 + 6 + 8) / 3;
printf("%d", avg);
```

Kết quả hiển thị:

```text
6
```

Vì tổng là 19, phép chia nguyên `19 / 3` bỏ phần thập phân và chỉ còn 6.

**Nếu sử dụng phép chia số thực:**

```c
float avg;
avg = (5 + 6 + 8) / 3.0;
printf("%.2f", avg);
```

Kết quả hiển thị:

```text
6.33
```

**Giải thích:** Cùng một phép tính nhưng cách sử dụng kiểu dữ liệu khác nhau sẽ cho kết quả hiển thị khác nhau. Phép chia nguyên bỏ phần thập phân, còn phép chia số thực giữ lại phần thập phân. Qua ví dụ này, em hiểu vì sao khi tính điểm trung bình nên sử dụng kiểu dữ liệu số thực.

---

## 7. TỰ ĐÁNH GIÁ SAU BUỔI HỌC

Sau khi thực hành với AI Gia sư, em đã hiểu được nguyên nhân chương trình ban đầu hiển thị kết quả không có phần thập phân. Trước đây, em nghĩ chỉ cần đổi kiểu dữ liệu của biến `avg` là đủ, nhưng em đã hiểu rằng cần chú ý cả kiểu dữ liệu tham gia phép tính.

Em đã biết phân biệt `int` và `float`, hiểu phép chia nguyên trong C và biết cách sử dụng `3.0` để thực hiện phép chia số thực. Qua bài tập này, em rút ra rằng khi sửa lỗi code, cần hiểu nguyên nhân trước rồi mới thay đổi chương trình, không nên chỉ sao chép code có sẵn.
