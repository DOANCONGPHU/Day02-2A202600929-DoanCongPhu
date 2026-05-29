# 02 — Group Problem Statement

## Group convergence

## Bước 2.1 — Trình bày top 3

| # | Người đưa ra | Candidate problem | Người gặp vấn đề | Điểm nghẽn (Bottleneck) | Cảm nhận nhanh (Quick gut) |
|:---|:---|:---|:---|:---|:---|
| 1 | [Đoàn Công Phú] | Tài liệu học tập mở quá sát giờ học nên không kịp ôn trước. | Học viên | Không có đủ thời gian để đọc trước, dẫn đến không theo kịp tốc độ bài giảng. | Quy trình (Process fix) |
| 2 | [Đoàn Công Phú] | Học viên trái ngành không load kịp kiến thức khi học lab buổi chiều do lượng kiến thức tăng quá nhanh. | Học viên trái ngành | Bị choáng ngợp thông tin, tốc độ nạp kiến thức chậm hơn tốc độ dạy. | AI Agent (Tutor cá nhân) |
| 3 | [Đoàn Công Phú] | Không có AI tutor hỗ trợ recap kiến thức nền hoặc giải thích nhanh thuật ngữ. | Học viên | Tốn thời gian tự tra cứu thủ công, dễ hiểu sai lệch thuật ngữ chuyên môn. | RAG Agent |
| 4 | [Vũ Quang Vinh] | Học viên nhiều nhưng trợ giảng ít dẫn đến việc thắc mắc nhưng không được giải đáp kịp thời. | Học viên | Thời gian chờ đợi TA quá lâu gây "đóng băng" tiến độ thực hành code. | Agent (Virtual TA) |
| 5 | [Vũ Quang Vinh] | Các học viên đều có thắc mắc giống nhau (cài đặt môi trường, hỏi đường...). | Trợ giảng (TA) | Trợ giảng bị quá tải, phải lặp lại thao tác copy/paste câu trả lời như một cái máy. | Agent / Rule-based FAQ |
| 6 | [Vũ Quang Vinh] | Khó nắm bắt được các thông tin do có quá nhiều kênh thông báo (Zalo, Teams, Discord). | Học viên | Phải lướt dò thủ công nhiều app, dễ trôi tin và lỡ deadline quan trọng. | Workflow + AI (Gom luồng) |
| 7 | [Hoàng Đức Dũng] | Xử lý hồ sơ hoàn tiền công tác phí chậm và tốn công. | Kế toán / Hành chính | Khâu đối chiếu hóa đơn với quy chế công ty phải làm hoàn toàn bằng mắt thường. | AI Workflow (OCR + LLM) |
| 8 | [Hoàng Đức Dũng] | Trích xuất và kiểm duyệt hồ sơ dịch vụ công tốn nhiều thời gian. | Nhân viên xử lý hồ sơ | Phải gõ lại dữ liệu thủ công từ các form giấy tờ cũ, dễ bị mờ/nhòe. | Workflow (OCR) |
| 9 | [Hoàng Đức Dũng] | Đánh giá chất lượng cuộc gọi CSKH chỉ đạt tỷ lệ rất thấp (dưới 5%). | QA / Quản lý CSKH | Phải nghe lại từng file ghi âm thủ công, không đủ sức người để cover 100% cuộc gọi. | AI (Speech-to-Text) |


## Bước 2.2 — Gom trùng / cluster

| Cluster | Candidates included | Pattern chung | Ghi chú |
| :--- | :--- | :--- | :--- |
| *A (Hỗ trợ học tập)* | #3, #4, #5 | *Sự thiếu hụt nguồn lực giải đáp Real-time:* Học viên có nhu cầu hỏi đáp cao (về thuật ngữ, lỗi code, quy trình) nhưng số lượng TA/Mentor có hạn, dẫn đến tình trạng "đóng băng" tiến độ thực hành và lãng phí thời gian của đôi bên. | Đây là *"Mỏ vàng"* để xây dựng Virtual TA / RAG Agent. Tính khả thi cao và tác động cực kỳ rõ rệt trong môi trường Bootcamp. |
| *B (Tiếp thu kiến thức)* | #1, #2 | *Độ trễ trong việc nạp kiến thức:* Tốc độ cung cấp tài liệu hoặc tốc độ giảng dạy đang nhanh hơn khả năng tiêu hóa thông tin của học viên (đặc biệt là nhóm trái ngành hoặc khi tài liệu mở quá sát giờ). | Vấn đề này thiên về tối ưu *quy trình sư phạm (Process fix)* hơn là dùng AI, trừ khi kết hợp dùng AI để tóm tắt trước tài liệu. |
| *C (Giao tiếp & Thông báo)* | #6 | *Phân mảnh luồng thông tin:* Dữ liệu, thông báo và deadline nằm rải rác ở quá nhiều nền tảng khác nhau gây nhiễu loạn, tâm lý FOMO và sót việc. | Đứng độc lập thành một cụm riêng. Phù hợp nhất với giải pháp *Automation Workflow (Gom luồng)* kết hợp AI trích xuất deadline. |
| *D (Vận hành B2B)* | #7, #8, #9 | *Xử lý dữ liệu phi cấu trúc thủ công:* Quy trình vận hành back-office (kế toán, hành chính, CSKH) đang dùng sức người (mắt, tai) để xử lý dữ liệu thô (ảnh hóa đơn, form giấy, file ghi âm) vô cùng tốn thời gian. | Cụm bài toán *Doanh nghiệp (Enterprise)*, sử dụng OCR hoặc Speech-to-Text. Hơi "lạc quẻ" so với bối cảnh học thuật của các cụm trên. |

## Bước 2.3 — Shortlist

| Candidate | Vì sao vào shortlist | Rủi ro / điều chưa rõ |
| :--- | :--- | :--- |
| Cluster A — Hỗ trợ học tập: Virtual TA / AI tutor trong lab (#3, #4, #5) | Đây là cụm mạnh nhất vì nhóm hiểu workflow thật từ bối cảnh bootcamp: học viên gặp thuật ngữ, lỗi code, setup môi trường hoặc câu hỏi lặp lại rồi phải chờ TA/mentor. Actor cụ thể gồm học viên và TA/mentor. Bottleneck là bước giải đáp thắc mắc real-time khi nguồn lực support không đủ. Impact đo được bằng thời gian chờ TA, số câu hỏi lặp lại, số lượt hỏi mentor và tỷ lệ hoàn thành lab đúng giờ. Before/after workflow rất rõ: trước là hỏi thủ công và chờ support, sau là hỏi Virtual TA trước, chỉ escalates cho mentor khi câu hỏi khó. Dễ so sánh Rule / Workflow / Agent: FAQ rule-based cho câu hỏi cố định, workflow gom tài liệu-lab-FAQ, agent RAG trả lời theo context bài lab. Phạm vi vừa sức lab nếu giới hạn vào một bài lab và 1-2 nhóm câu hỏi phổ biến. | Cần nguồn tri thức đủ tốt như slide, lab guide, FAQ hoặc log câu hỏi cũ. Rủi ro AI trả lời sai nếu không giới hạn nguồn hoặc không có cơ chế báo "không chắc". Cần chốt rõ prototype hỗ trợ phần nào trước: thuật ngữ, lỗi code, hay setup môi trường. |
| Cluster B — Tiếp thu kiến thức: học viên không kịp nạp kiến thức trước/trong lab (#1, #2) | Cụm này có actor rõ là học viên, đặc biệt học viên trái ngành. Nhóm cũng hiểu workflow học tập thật: tài liệu mở sát giờ, vào lab gặp nhiều concept mới, vừa học lý thuyết vừa thực hành nên bị mất nhịp. Bottleneck là bước chuẩn bị kiến thức nền và tiêu hóa concept trước khi làm lab. Impact có thể đo bằng tỷ lệ đọc tài liệu trước buổi học, tỷ lệ hoàn thành lab đúng giờ, số câu hỏi cơ bản trong buổi, mức tự tin self-report. Before/after workflow vẽ được: trước là vào lớp mới đọc và bị quá tải, sau là có prerequisite checklist, recap ngắn hoặc AI tóm tắt cá nhân hóa trước buổi học. Có thể so sánh Rule / Workflow / Agent: rule gửi checklist cố định, workflow tự tạo recap từ tài liệu, agent cá nhân hóa phần cần ôn theo level học viên. | Có thể nghiêng về process fix hơn là AI nếu chỉ cần mở tài liệu sớm. Cần làm rõ nhóm có đo được việc học viên đọc trước hay không. Nếu làm AI cá nhân hóa quá rộng thì vượt phạm vi lab hôm nay; nên giới hạn vào recap/prerequisite cho một buổi học cụ thể. |
| Cluster C — Giao tiếp & thông báo: gom luồng thông tin nhiều kênh (#6) | Actor cụ thể là học viên phải theo dõi Zalo, Teams, Discord. Bottleneck là bước lướt dò thủ công nhiều kênh để tìm thông báo, deadline và việc cần làm. Impact đo được bằng số deadline bị lỡ, thời gian kiểm tra thông báo mỗi ngày, số lần hỏi lại thông tin đã được thông báo. Before/after workflow rõ: trước là mở từng app và tự lọc tin, sau là một luồng tổng hợp có deadline/action item. Dễ so sánh Rule / Workflow / Agent: rule theo keyword deadline, workflow gom tin định kỳ, agent tóm tắt và phân loại mức quan trọng. Phạm vi lab vừa nếu dùng dữ liệu mẫu thay vì tích hợp API thật. | Có thể chưa có quyền truy cập dữ liệu thật từ các kênh chat. Rủi ro bài toán bị trôi sang phần tích hợp kỹ thuật. Cần xác định nguồn chính, loại thông báo quan trọng nhất và cách đánh giá "tin quan trọng". |
| Cluster D — Vận hành B2B: xử lý dữ liệu phi cấu trúc thủ công bằng OCR/STT + AI (#7, #8, #9) | Cụm này có ROI rõ vì actor là kế toán/hành chính, nhân viên xử lý hồ sơ, QA/CSKH; bottleneck đều là bước con người phải đọc, nghe, gõ lại hoặc đối chiếu dữ liệu phi cấu trúc. Impact đo được tốt: thời gian xử lý hồ sơ/cuộc gọi, tỷ lệ lỗi nhập liệu, tỷ lệ hồ sơ bị trả lại, tỷ lệ cuộc gọi được QA. Before/after workflow dễ vẽ: trước là kiểm tra thủ công bằng mắt/tai, sau là OCR hoặc speech-to-text, AI trích xuất/chấm điểm, con người duyệt lại. Có thể so sánh Rule / Workflow / Agent rõ: rule kiểm tra điều kiện cố định, workflow trích xuất và đối chiếu, agent hỏi lại khi thiếu dữ liệu hoặc đề xuất xử lý. | Cụm này hơi lạc khỏi bối cảnh học tập của nhóm và có thể thiếu người hiểu workflow thật đủ sâu. Cần dữ liệu mẫu, quy chế/rubric kiểm duyệt và tiêu chí thành công cụ thể. Nếu chọn cả cụm thì quá rộng cho lab; cần chọn một use case đại diện như hoàn tiền công tác phí hoặc chấm transcript CSKH. |

## Bước 2.4 — Score để đồng thuận

Chấm 1-5. Điểm không cần tuyệt đối; mục tiêu là ép nhóm nói rõ lý do.

| Candidate | Actor rõ | Workflow rõ | Pain có evidence | Impact đo được | Làm trong lab | So sánh R/W/A được | Nhóm hiểu domain | Tổng |
| :--- | ---: | ---: | ---: | ---: | ---: | ---: | ---: | ---: |
| Cluster A — Hỗ trợ học tập: Virtual TA / AI tutor trong lab (#3, #4, #5) | 5 | 5 | 4 | 5 | 5 | 5 | 5 | 34 |
| Cluster B — Tiếp thu kiến thức: học viên không kịp nạp kiến thức trước/trong lab (#1, #2) | 5 | 4 | 4 | 4 | 4 | 4 | 5 | 30 |
| Cluster C — Giao tiếp & thông báo: gom luồng thông tin nhiều kênh (#6) | 5 | 4 | 3 | 4 | 4 | 5 | 4 | 29 |
| Cluster D — Vận hành B2B: xử lý dữ liệu phi cấu trúc thủ công bằng OCR/STT + AI (#7, #8, #9) | 4 | 5 | 3 | 5 | 2 | 5 | 2 | 26 |

Candidate nhóm chọn:

```text
Cluster A — Hỗ trợ học tập: Virtual TA / AI tutor trong lab (#3, #4, #5)
```

Vì sao chọn:

```text
Cluster A có điểm cao nhất vì nhóm hiểu domain học lab rõ nhất, actor và bottleneck cụ thể, impact đo được, và có thể triển khai prototype nhỏ trong lab hôm nay. Bài toán cũng cho phép so sánh rõ giữa Rule-based FAQ, Workflow gom tài liệu/FAQ, và Agent RAG trả lời theo context bài lab.
```

Vì sao không chọn các candidate còn lại:

```text
Cluster B liên quan trực tiếp đến học tập nhưng có nguy cơ là process fix nhiều hơn AI, ví dụ chỉ cần mở tài liệu sớm hoặc gửi checklist trước buổi học.

Cluster C có workflow rõ và phù hợp automation, nhưng cần dữ liệu từ nhiều kênh chat; nếu không có dữ liệu thật thì prototype dễ bị giả lập nhiều.

Cluster D có impact doanh nghiệp rõ, nhưng nhóm chưa chắc hiểu sâu workflow kế toán/hồ sơ/CSKH và phạm vi hơi rộng cho lab nếu chọn cả cụm.
```

Nếu có disagreement, nhóm xử lý thế nào:

```text
Nhóm ưu tiên candidate có người hiểu workflow thật, có thể vẽ before/after ngay và làm prototype nhỏ trong thời gian lab. Nếu còn phân vân giữa Cluster A và B, chọn Cluster A vì bottleneck nằm ở một bước cụ thể hơn: giải đáp thắc mắc real-time trong lúc làm lab.
```

