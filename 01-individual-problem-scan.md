## 01 — Individual Problem Scan
## Scan rộng

| # | Lăng kính | Problem quan sát được | Ai đang đau? | Dấu hiệu thật |
|---|---|---|---|---|
| 1 | Lặp lại | Học viên trái ngành không load kịp kiến thức khi học lab buổi chiều do lượng kiến thức tăng quá nhanh | Học viên trái ngành | 5-10 người/buổi phải hỏi lại mentor, nhiều người không hoàn thành lab đúng giờ |
| 2 | Tốn thời gian | Tài liệu học tập mở quá sát giờ học nên không kịp ôn trước | Học viên | Nhiều người vào lớp mới đọc slide nên bị mất nhịp từ đầu buổi |
| 3 | AI có thể tốt hơn | Không có AI tutor hỗ trợ recap kiến thức nền hoặc giải thích nhanh thuật ngữ | Học viên trái ngành | Mentor bị hỏi lại cùng một dạng câu hỏi nhiều lần mỗi buổi |
| 4 | AI có thể tốt hơn | Thiếu API key hoặc môi trường thực hành khiến việc học bị gián đoạn | Học viên | Có người không chạy được lab trong 30-60 phút đầu buổi |
| 5 | Pain từ người khác | App điểm danh khó sử dụng ở thời gian đầu | Học viên | Nhiều câu hỏi lặp lại trên group/chat trong tuần đầu |
| 6 | Pain từ người khác | Team project mất cân bằng kỹ năng | Học viên | Team nhiều tech, ít non-tech, một vài người phải làm phần lớn project |
| 7 | Pain từ người khác | Không có cam kết hoặc định hướng rõ ràng về cơ hội việc làm sau khóa học | Học viên | Câu hỏi “học xong làm được gì?” xuất hiện nhiều trong Q&A/group chat |
| 8 | Pain từ người khác | Bài test đầu vào quá đơn giản so với độ khó thực tế khi vào học | Học viên | Nhiều người bị “shock” sau 1-2 buổi đầu và không theo kịp tiến độ |
| 9 | AI có thể tốt hơn | Không có hệ thống cá nhân hóa tốc độ học cho người nền tảng yếu/mạnh khác nhau | Học viên | Người yếu bị quá tải, người mạnh phải chờ tiến độ chung của lớp |

## Top 3
| Rank | Problem | Vì sao chọn | Điều còn chưa chắc |
|---|---|---|---|
| 1 | Tài liệu học tập mở quá sát giờ học nên không kịp ôn trước | Đây là pain xảy ra thường xuyên, ảnh hưởng nhiều người và tác động trực tiếp tới khả năng theo kịp buổi học | Chưa chắc việc mở tài liệu sớm có giúp cải thiện hiệu quả học rõ rệt không |
| 2 | Học viên trái ngành không load kịp kiến thức khi học lab buổi chiều do lượng kiến thức tăng quá nhanh | Pain lớn và thực tế với nhiều học viên trái ngành, có dấu hiệu thật rõ ràng | Chưa xác định được nguyên nhân chính là do nền tảng yếu hay tốc độ dạy quá nhanh |
| 3 | Không có AI tutor hỗ trợ recap kiến thức nền hoặc giải thích nhanh thuật ngữ | Có tiềm năng AI rõ ràng, giảm tải mentor và hỗ trợ học viên học chủ động hơn | Chưa chắc học viên sẽ dùng thường xuyên thay vì hỏi mentor trực tiếp |

## Problem Card #1 

**Problem 1 câu:**  
Học viên  không có đủ thời gian ôn trước vì tài liệu thường được mở quá sát giờ học, dẫn đến mất nhịp và khó theo kịp lab.

**Actor:**  
Học viên

**Thời điểm / bối cảnh:**  
Trước buổi học vài giờ hoặc ngay khi buổi học bắt đầu
Đặc biệt ở các buổi lab kiến thức mới/chuyên sâu

**Current workflow:**

```text
1. Giảng viên có tài liệu
2. Tài liệu được publish sát giờ học
3. Học viên vào lớp mới bắt đầu đọc
4. Học viên gặp nhiều thuật ngữ/concept mới
5. Trong lúc lab phải vừa học lý thuyết vừa thực hành
6. Mentor phải hỗ trợ nhiều câu hỏi cơ bản
7 Một số học viên không hoàn thành lab đúng giờ
```

**Bottleneck:**  
Không có thời gian chuẩn bị kiến thức nền trước buổi học
Kiến thức mới xuất hiện quá nhiều trong thời gian ngắn

**Impact:**  
Học viên bị quá tải
Không theo kịp tiến độ, giảm chất lượng đầu ra
Mentor mất nhiều thời gian support câu hỏi lặp lại
Một số học viên mất động lực vì không theo kịp

**Success metric:**  
Tài liệu được mở trước ít nhất 1 ngày
Tăng số học viên hoàn thành lab đúng giờ
Học viên self-report hiểu bài tốt hơn
**Non-AI alternative:**  
Publish tài liệu sớm hơn
Có checklist prerequisite trước mỗi buổi
Gửi video/tóm tắt kiến thức nền trước giờ học

**AI hypothesis:**  
AI có thể tự động tạo recap/prerequisite ngắn từ slide hoặc lab
AI recommend phần cần đọc trước dựa trên trình độ học viên
AI chatbot giải thích nhanh thuật ngữ trước buổi học
**Quick gut:**  
[x] Workflow
[x] Agent
[ ] No AI / process fix
[ ] Rule
[ ] Chưa biết


### Draft current workflow

```text
[Trước buổi học]
       |
       v
[Mentor chuẩn bị slide / lab]
       |
       v
[Tài liệu được mở sát giờ]
       |
       v
[Học viên vào lớp mới đọc]
       |
       v
[Gặp nhiều thuật ngữ / kiến thức mới]
       |
       v
[Vừa học lý thuyết + vừa làm lab]
       |
       v
[Không hiểu / bị chậm nhịp]
       |
       +----------------------+
       |                      |
       v                      v
[Hỏi mentor nhiều]     [Không hoàn thành lab]
       |                      |
       +----------+-----------+
                  v
        [Mentor quá tải support]
                  |
                  v
        [Chất lượng buổi học giảm]
```
# Problem 2

Problem :
Học viên trái ngành không load kịp kiến thức khi học lab do tốc độ học và độ khó tăng quá nhanh.

**Actor:**

* Học viên trái ngành


Thời điểm / bối cảnh:

* Trong các buổi lab chiều hoặc các buổi kiến thức chuyên sâu
* Đặc biệt sau 1-2 tuần đầu của khóa học

Current workflow 3-7 bước:

1. Học viên học kiến thức nền cơ bản
2. Vào buổi lab chuyên sâu
3. Mentor giải thích nhanh workflow/concept mới
4. Học viên chưa hiểu context nhưng phải tiếp tục theo flow lớp
5. Trong lúc code phát sinh thêm lỗi/tool mới
6. Học viên bị mất nhịp
7. Phải hỏi mentor liên tục hoặc bỏ dở lab

Bottleneck:

* Chênh lệch lớn giữa kiến thức đầu vào và độ khó thực tế
* Người trái ngành thiếu context IT/workflow thực tế

Impact:

* Học viên bị quá tải
* Không hoàn thành lab đúng giờ
* Mentor bị overload support
* Một số học viên mất động lực hoặc bỏ cuộc

Success metric:

* Tăng số học viên hoàn thành lab đúng giờ
* Giảm số câu hỏi cơ bản lặp lại
* Giảm số học viên bị “mất flow” giữa buổi
* Tăng self-report confidence của học viên

Non-AI alternative:

* Chia lớp theo level
* Có lớp foundation trước khóa chính
* Giảm tốc độ hoặc chia nhỏ lab

AI hypothesis:

* AI detect học viên đang “kẹt” ở bước nào
* AI giải thích lại concept theo level người học
* AI generate roadmap/prerequisite cá nhân hóa

Quick gut:
[ ] No AI / process fix
[ ] Rule
[x] Workflow
[x] Agent
[ ] Chưa biết

ASCII Flow:

```text
[Học kiến thức nền cơ bản]
              |
              v
      [Vào buổi lab]
              |
              v
 [Kiến thức/workflow mới xuất hiện]
              |
              v
 [Học viên chưa hiểu context]
              |
              v
 [Vẫn phải tiếp tục code theo lớp]
              |
              v
       [Bị mất nhịp]
              |
      +-------+--------+
      |                |
      v                v
[Hỏi mentor]    [Không hoàn thành lab]
      |                |
      +--------+-------+
               v
      [Mất động lực học]
```
# Problem 3

Problem 1 câu:
Không có AI tutor hỗ trợ recap kiến thức nền hoặc giải thích nhanh thuật ngữ khiến mentor phải trả lời lặp lại nhiều lần.

Actor:

* Học viên trái ngành
* Mentor

Thời điểm / bối cảnh:

* Trong lúc học lab
* Khi gặp thuật ngữ mới hoặc lỗi kỹ thuật
* Sau giờ học khi tự học lại

Current workflow 3-7 bước:

1. Học viên gặp thuật ngữ/concept mới
2. Không hiểu nhưng flow lớp vẫn tiếp tục
3. Học viên pause để Google hoặc hỏi mentor
4. Mentor trả lời thủ công
5. Các học viên khác tiếp tục hỏi các câu tương tự
6. Mentor bị phân tán thời gian support
7. Học viên vẫn khó hiểu nếu giải thích quá technical

Bottleneck:

* Không có hệ thống hỗ trợ giải thích theo trình độ người học
* Mentor phải trả lời lặp lại nhiều câu giống nhau

Impact:

* Mentor quá tải support
* Học viên phụ thuộc mentor
* Flow lớp học bị gián đoạn
* Người yếu ngày càng chậm hơn

Success metric:

* Giảm số câu hỏi lặp lại cho mentor
* Tăng tốc độ tự giải quyết vấn đề của học viên
* Tăng completion rate của lab
* Học viên phản hồi hiểu bài tốt hơn

Non-AI alternative:

* FAQ/document tổng hợp
* Video recap kiến thức nền
* Session phụ đạo ngoài giờ

AI hypothesis:

* AI tutor có thể explain concept theo nhiều level
* AI trả lời dựa trên context bài lab hiện tại
* AI recap nhanh kiến thức prerequisite khi học viên bị kẹt

Quick gut:
[ ] No AI / process fix
[ ] Rule
[ ] Workflow
[x] Agent
[ ] Chưa biết

ASCII Flow:

```text
 [Học viên gặp thuật ngữ mới]
                |
                v
        [Không hiểu concept]
                |
       +--------+--------+
       |                 |
       v                 v
 [Google thủ công]   [Hỏi mentor]
       |                 |
       v                 v
 [Thông tin rời rạc] [Mentor trả lời]
       |                 |
       +--------+--------+
                v
     [Nhiều người hỏi lặp lại]
                |
                v
      [Mentor bị overload]
                |
                v
      [Flow lớp bị chậm]
```
