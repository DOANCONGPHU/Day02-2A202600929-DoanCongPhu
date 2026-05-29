# Phase 3 — Group Problem Statement

## Group convergence

## Bước 3.1 — Trình bày top 3

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


## Bước 3.2 — Gom trùng / cluster

| Cluster | Candidates included | Pattern chung | Ghi chú |
| :--- | :--- | :--- | :--- |
| *A (Hỗ trợ học tập)* | #3, #4, #5 | *Sự thiếu hụt nguồn lực giải đáp Real-time:* Học viên có nhu cầu hỏi đáp cao (về thuật ngữ, lỗi code, quy trình) nhưng số lượng TA/Mentor có hạn, dẫn đến tình trạng "đóng băng" tiến độ thực hành và lãng phí thời gian của đôi bên. | Đây là *"Mỏ vàng"* để xây dựng Virtual TA / RAG Agent. Tính khả thi cao và tác động cực kỳ rõ rệt trong môi trường Bootcamp. |
| *B (Tiếp thu kiến thức)* | #1, #2 | *Độ trễ trong việc nạp kiến thức:* Tốc độ cung cấp tài liệu hoặc tốc độ giảng dạy đang nhanh hơn khả năng tiêu hóa thông tin của học viên (đặc biệt là nhóm trái ngành hoặc khi tài liệu mở quá sát giờ). | Vấn đề này thiên về tối ưu *quy trình sư phạm (Process fix)* hơn là dùng AI, trừ khi kết hợp dùng AI để tóm tắt trước tài liệu. |
| *C (Giao tiếp & Thông báo)* | #6 | *Phân mảnh luồng thông tin:* Dữ liệu, thông báo và deadline nằm rải rác ở quá nhiều nền tảng khác nhau gây nhiễu loạn, tâm lý FOMO và sót việc. | Đứng độc lập thành một cụm riêng. Phù hợp nhất với giải pháp *Automation Workflow (Gom luồng)* kết hợp AI trích xuất deadline. |
| *D (Vận hành B2B)* | #7, #8, #9 | *Xử lý dữ liệu phi cấu trúc thủ công:* Quy trình vận hành back-office (kế toán, hành chính, CSKH) đang dùng sức người (mắt, tai) để xử lý dữ liệu thô (ảnh hóa đơn, form giấy, file ghi âm) vô cùng tốn thời gian. | Cụm bài toán *Doanh nghiệp (Enterprise)*, sử dụng OCR hoặc Speech-to-Text. Hơi "lạc quẻ" so với bối cảnh học thuật của các cụm trên. |

## Bước 3.3 — Shortlist

| Candidate | Vì sao vào shortlist | Rủi ro / điều chưa rõ |
| :--- | :--- | :--- |
| Cluster A — Hỗ trợ học tập: Virtual TA / AI tutor trong lab (#3, #4, #5) | Đây là cụm mạnh nhất vì nhóm hiểu workflow thật từ bối cảnh bootcamp: học viên gặp thuật ngữ, lỗi code, setup môi trường hoặc câu hỏi lặp lại rồi phải chờ TA/mentor. Actor cụ thể gồm học viên và TA/mentor. Bottleneck là bước giải đáp thắc mắc real-time khi nguồn lực support không đủ. Impact đo được bằng thời gian chờ TA, số câu hỏi lặp lại, số lượt hỏi mentor và tỷ lệ hoàn thành lab đúng giờ. Before/after workflow rất rõ: trước là hỏi thủ công và chờ support, sau là hỏi Virtual TA trước, chỉ escalates cho mentor khi câu hỏi khó. Dễ so sánh Rule / Workflow / Agent: FAQ rule-based cho câu hỏi cố định, workflow gom tài liệu-lab-FAQ, agent RAG trả lời theo context bài lab. Phạm vi vừa sức lab nếu giới hạn vào một bài lab và 1-2 nhóm câu hỏi phổ biến. | Cần nguồn tri thức đủ tốt như slide, lab guide, FAQ hoặc log câu hỏi cũ. Rủi ro AI trả lời sai nếu không giới hạn nguồn hoặc không có cơ chế báo "không chắc". Cần chốt rõ prototype hỗ trợ phần nào trước: thuật ngữ, lỗi code, hay setup môi trường. |
| Cluster B — Tiếp thu kiến thức: học viên không kịp nạp kiến thức trước/trong lab (#1, #2) | Cụm này có actor rõ là học viên, đặc biệt học viên trái ngành. Nhóm cũng hiểu workflow học tập thật: tài liệu mở sát giờ, vào lab gặp nhiều concept mới, vừa học lý thuyết vừa thực hành nên bị mất nhịp. Bottleneck là bước chuẩn bị kiến thức nền và tiêu hóa concept trước khi làm lab. Impact có thể đo bằng tỷ lệ đọc tài liệu trước buổi học, tỷ lệ hoàn thành lab đúng giờ, số câu hỏi cơ bản trong buổi, mức tự tin self-report. Before/after workflow vẽ được: trước là vào lớp mới đọc và bị quá tải, sau là có prerequisite checklist, recap ngắn hoặc AI tóm tắt cá nhân hóa trước buổi học. Có thể so sánh Rule / Workflow / Agent: rule gửi checklist cố định, workflow tự tạo recap từ tài liệu, agent cá nhân hóa phần cần ôn theo level học viên. | Có thể nghiêng về process fix hơn là AI nếu chỉ cần mở tài liệu sớm. Cần làm rõ nhóm có đo được việc học viên đọc trước hay không. Nếu làm AI cá nhân hóa quá rộng thì vượt phạm vi lab hôm nay; nên giới hạn vào recap/prerequisite cho một buổi học cụ thể. |
| Cluster C — Giao tiếp & thông báo: gom luồng thông tin nhiều kênh (#6) | Actor cụ thể là học viên phải theo dõi Zalo, Teams, Discord. Bottleneck là bước lướt dò thủ công nhiều kênh để tìm thông báo, deadline và việc cần làm. Impact đo được bằng số deadline bị lỡ, thời gian kiểm tra thông báo mỗi ngày, số lần hỏi lại thông tin đã được thông báo. Before/after workflow rõ: trước là mở từng app và tự lọc tin, sau là một luồng tổng hợp có deadline/action item. Dễ so sánh Rule / Workflow / Agent: rule theo keyword deadline, workflow gom tin định kỳ, agent tóm tắt và phân loại mức quan trọng. Phạm vi lab vừa nếu dùng dữ liệu mẫu thay vì tích hợp API thật. | Có thể chưa có quyền truy cập dữ liệu thật từ các kênh chat. Rủi ro bài toán bị trôi sang phần tích hợp kỹ thuật. Cần xác định nguồn chính, loại thông báo quan trọng nhất và cách đánh giá "tin quan trọng". |
| Cluster D — Vận hành B2B: xử lý dữ liệu phi cấu trúc thủ công bằng OCR/STT + AI (#7, #8, #9) | Cụm này có ROI rõ vì actor là kế toán/hành chính, nhân viên xử lý hồ sơ, QA/CSKH; bottleneck đều là bước con người phải đọc, nghe, gõ lại hoặc đối chiếu dữ liệu phi cấu trúc. Impact đo được tốt: thời gian xử lý hồ sơ/cuộc gọi, tỷ lệ lỗi nhập liệu, tỷ lệ hồ sơ bị trả lại, tỷ lệ cuộc gọi được QA. Before/after workflow dễ vẽ: trước là kiểm tra thủ công bằng mắt/tai, sau là OCR hoặc speech-to-text, AI trích xuất/chấm điểm, con người duyệt lại. Có thể so sánh Rule / Workflow / Agent rõ: rule kiểm tra điều kiện cố định, workflow trích xuất và đối chiếu, agent hỏi lại khi thiếu dữ liệu hoặc đề xuất xử lý. | Cụm này hơi lạc khỏi bối cảnh học tập của nhóm và có thể thiếu người hiểu workflow thật đủ sâu. Cần dữ liệu mẫu, quy chế/rubric kiểm duyệt và tiêu chí thành công cụ thể. Nếu chọn cả cụm thì quá rộng cho lab; cần chọn một use case đại diện như hoàn tiền công tác phí hoặc chấm transcript CSKH. |

## Bước 3.4 — Score để đồng thuận

Chấm 1-5. Điểm không cần tuyệt đối; mục tiêu là ép nhóm nói rõ lý do.

| Candidate | Actor rõ | Workflow rõ | Pain có evidence | Impact đo được | Làm trong lab | So sánh R/W/A được | Nhóm hiểu domain | Tổng |
| :--- | ---: | ---: | ---: | ---: | ---: | ---: | ---: | ---: |
| Cluster A — Hỗ trợ học tập: Virtual TA / AI tutor trong lab (#3, #4, #5) | 5 | 5 | 3 | 5 | 4 | 4 | 4 | 30 |
| Cluster B — Tiếp thu kiến thức: học viên không kịp nạp kiến thức trước/trong lab (#1, #2) | 5 | 4 | 4 | 4 | 4 | 4 | 5 | 30 |
| Cluster C — Giao tiếp & thông báo: gom luồng thông tin nhiều kênh (#6) | 5 | 4 | 3 | 4 | 4 | 5 | 4 | 29 |
| Cluster D — Vận hành B2B: xử lý dữ liệu phi cấu trúc thủ công bằng OCR/STT + AI (#7, #8, #9) | 4 | 5 | 5 | 5 | 2 | 5 | 5 | 31 |

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

---

# Phase 4 — Quick Validation + Research giải pháp

## Bước 4.1 — Quick validation

| Nguồn | Số người / số mẫu | Tín hiệu xác nhận | Tín hiệu phản bác | Nhóm sửa problem thế nào |
| :--- | ---: | :--- | :--- | :--- |
| Quan sát nội bộ nhóm / Problem Cards | 3 người đưa candidate | Các candidate #3, #4, #5 đều xoay quanh cùng một điểm đau: học viên bị kẹt khi gặp thuật ngữ, lỗi code, setup môi trường hoặc câu hỏi lặp lại; TA/mentor phải trả lời thủ công nhiều lần. | Chưa có số liệu chính thức về thời gian chờ TA và số câu hỏi lặp lại trên từng buổi. | Thu hẹp từ "AI tutor học mọi thứ" thành "Virtual TA hỗ trợ câu hỏi lặp lại và câu hỏi context bài lab trong lúc thực hành". |
| Quick interview đề xuất | 3-5 học viên + 1 TA | Cần hỏi: lần gần nhất bị kẹt trong lab là khi nào, chờ hỗ trợ bao lâu, câu hỏi thuộc nhóm setup/thuật ngữ/lỗi code/quy trình, có tự xử lý được không. | Nếu đa số học viên không hỏi vì thiếu động lực hoặc chưa đọc tài liệu, AI tutor không giải quyết gốc rễ. | Sau interview, ưu tiên 1-2 intent có tần suất cao nhất thay vì làm chatbot quá rộng. |
| Micro survey / Discord poll đề xuất | 5-10 học viên | Cần đo: tần suất bị kẹt trong lab, thời gian tự tra cứu, thời gian chờ mentor, mức độ sẵn sàng dùng Virtual TA trước khi hỏi người thật. | Nếu học viên vẫn thích hỏi trực tiếp TA hơn vì tin tưởng hơn, adoption sẽ thấp. | Thêm cơ chế "AI trả lời kèm nguồn" và nút escalates cho TA để tăng niềm tin. |
| Log / dấu hiệu thật từ scan cá nhân | Quan sát theo buổi học | Có dấu hiệu 5-10 người/buổi phải hỏi lại mentor, nhiều người không hoàn thành lab đúng giờ, mentor bị hỏi lại cùng dạng câu hỏi nhiều lần. | Log hiện tại là quan sát định tính, chưa tách rõ câu hỏi lặp lại với câu hỏi khó thật sự cần mentor. | Baseline cần đo trong 1 buổi: tổng câu hỏi, câu hỏi lặp lại, thời gian chờ, số câu AI có thể trả lời bằng tài liệu. |

Kết luận validation nhanh:

```text
Pain có tín hiệu thật và xuất hiện lặp lại trong bối cảnh lab. Tuy nhiên, trước khi rollout cần đo baseline tối thiểu trong 1 buổi học: số câu hỏi lặp lại, thời gian chờ TA/mentor, và tỷ lệ câu hỏi có thể trả lời bằng slide/lab guide/FAQ.
```

## Bước 4.2 — Research giải pháp đã có

| Nguồn / tool / case | Link | Họ giải quyết phần nào? | Điểm mạnh | Khoảng trống / rủi ro | Bài học cho nhóm |
| :--- | :--- | :--- | :--- | :--- | :--- |
| Khanmigo by Khan Academy | [khanmigo.ai](https://khanmigo.ai) | AI tutor và teaching assistant cho học tập; hướng người học suy nghĩ thay vì chỉ đưa đáp án. | Rất sát bối cảnh giáo dục, nhấn mạnh an toàn học tập và vai trò hỗ trợ giáo viên. | Không phải công cụ tùy biến trực tiếp cho lab/slide riêng của lớp; cần content và guardrail riêng. | Virtual TA không nên "làm hộ bài"; nên gợi ý, hỏi ngược, giải thích từng bước và khuyến khích học viên tự làm. |
| Coursera Coach | [coursera.org/explore/coach](https://www.coursera.org/explore/coach) | Hỗ trợ người học hiểu concept, nhận giải thích ngắn, tóm tắt và luyện tập trong ngữ cảnh khóa học. | Cho thấy nhu cầu AI học tập theo course context là có thật. | Bị giới hạn trong hệ sinh thái Coursera; không xử lý trực tiếp lỗi setup/lỗi code trong lab nội bộ. | Prototype nên bám context bài học hiện tại, không trả lời chung chung như chatbot ngoài lớp. |
| Intercom Fin AI Agent | [intercom.com/help](https://www.intercom.com/help/en/articles/7837535-fin-ai-agent-faqs) | AI support agent trả lời từ support content, biết thể hiện không chắc và handoff cho người thật khi không đủ thông tin. | Mẫu tốt cho bài toán câu hỏi lặp lại và giảm tải support tuyến đầu. | Là sản phẩm customer support, không phải tutor; nếu áp dụng vào học tập cần tránh trả lời như "đóng ticket". | Cần có knowledge base sạch, trả lời kèm nguồn, đo unresolved questions, và escalates sang TA khi không chắc. |
| RAG / Grounding pattern | [Azure AI Search RAG](https://learn.microsoft.com/en-us/azure/search/retrieval-augmented-generation-overview), [Google Vertex AI Grounding](https://docs.cloud.google.com/vertex-ai/generative-ai/docs/grounding/overview) | Kết nối model với dữ liệu riêng như tài liệu, website, PDF; giảm hallucination bằng truy xuất nguồn trước khi trả lời. | Phù hợp với bài toán slide/lab guide/FAQ vì câu trả lời phải dựa trên nguồn lớp học. | Chất lượng phụ thuộc mạnh vào chuẩn bị tài liệu, chunking, naming, versioning và kiểm thử câu hỏi. | Pilot nên bắt đầu bằng RAG workflow nhỏ: 1 lab guide + 1 FAQ + 10-20 câu hỏi mẫu, chưa cần agent phức tạp. |

Kết luận research:

```text
Các giải pháp hiện có xác nhận hướng Virtual TA là hợp lý, nhưng bài học chung là phải grounding vào tài liệu lớp học, có boundary rõ, có human handoff, và không để AI làm thay bài học viên. Với phạm vi lab hôm nay, chọn Workflow RAG nhỏ sẽ hợp lý hơn full Agent.
```

---

# Phase 5 — Workflow + Problem Statement

## Bước 5.1 — Current workflow bản nhóm

Dán workflow:

```text
CURRENT STATE — trong buổi lab

[Học viên gặp thuật ngữ/lỗi code/setup]
        |
        v
[Tự đọc lại slide/lab guide hoặc Google: 5-10']
        |
        v
[Vẫn chưa hiểu hoặc không biết áp dụng vào bài lab]
        |
        v
[Hỏi group/TA/mentor và chờ hỗ trợ: 5-20']
        |
        v
[TA/mentor hỏi lại context và trả lời thủ công]
        |
        +-------------------------------+
        |                               |
        v                               v
[Học viên tiếp tục lab]        [Câu hỏi tương tự lặp lại]
        |                               |
        v                               v
[Một số bạn hoàn thành chậm]   [TA/mentor bị phân tán]
```

| Bước | Actor | Input | Output | Thời gian/tần suất | Ghi chú |
| :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | Học viên | Lab task, slide, môi trường code | Phát hiện không hiểu thuật ngữ, lỗi setup hoặc lỗi code | Xảy ra trong lúc làm lab | Đây là điểm bắt đầu của pain, đặc biệt với học viên trái ngành. |
| 2 | Học viên | Slide/lab guide/Google | Tự tìm câu trả lời | Ước lượng 5-10 phút/lần | Dễ đọc sai context vì tài liệu ngoài không khớp bài lab. |
| 3 | Học viên | Câu hỏi chưa giải được | Gửi câu hỏi lên group hoặc gọi TA/mentor | Nhiều lần/buổi | Câu hỏi thường thiếu context: đang ở bước nào, lỗi gì, đã thử gì. |
| 4 | TA/mentor | Câu hỏi của học viên | Hỏi lại context và trả lời thủ công | Ước lượng chờ 5-20 phút tùy tải | Bottleneck chính: TA/mentor là nguồn lực hữu hạn. |
| 5 | TA/mentor + học viên | Câu trả lời thủ công | Học viên tiếp tục lab hoặc vẫn bị kẹt | Lặp lại với nhiều học viên | Nhiều câu hỏi giống nhau nhưng vẫn phải trả lời lại. |
| 6 | Lớp học | Nhiều học viên hỏi cùng lúc | Lab chậm, mentor bị phân tán | Quan sát theo buổi | Ảnh hưởng completion rate và trải nghiệm học. |

Bottleneck chính:

```text
Bottleneck nằm ở bước giải đáp thắc mắc real-time trong lab: học viên cần phản hồi ngay để tiếp tục thực hành, nhưng TA/mentor phải xử lý thủ công từng câu hỏi, trong đó có nhiều câu lặp lại hoặc có thể trả lời bằng tài liệu sẵn có.
```

## Bước 5.2 — Future workflow bản nhóm

Dán workflow:

```text
FUTURE STATE — Virtual TA pilot cho 1 bài lab

[Học viên hỏi Virtual TA]
        |
        v
[Rule phân loại: setup / thuật ngữ / lỗi code / ngoài scope]
        |
        v
[RAG tìm trong lab guide + slide + FAQ]
        |
        v
[AI trả lời ngắn + nguồn tham chiếu + bước thử tiếp theo]
        |
        v
[Học viên thử lại trong lab]
        |
        +-------------------------------+
        |                               |
        v                               v
[Resolved: ghi nhận feedback]   [Unresolved / low confidence]
                                        |
                                        v
                         [Escalate TA kèm tóm tắt context]

Human boundary:
- AI không làm hộ toàn bộ bài hoặc nộp code thay học viên.
- AI không trả lời nếu không tìm thấy nguồn trong tài liệu lớp.
- Câu hỏi khó, lỗi lạ, hoặc ảnh hưởng grading phải chuyển cho TA/mentor.
```

Before/after impact:

| Metric | Trước | Sau kỳ vọng | Ghi chú |
| :--- | ---: | ---: | :--- |
| Số bước chính để học viên nhận hỗ trợ | 5-6 bước | 4-5 bước | Giảm vòng hỏi-chờ-hỏi lại context. |
| Thời gian phản hồi đầu tiên | 5-20 phút | Dưới 1 phút cho câu hỏi phổ biến | Cần đo trong pilot, không coi là cam kết rollout. |
| Số bước thủ công của TA/mentor | 3-4 bước | 1-2 bước | TA chỉ xử lý câu hỏi khó hoặc câu AI không chắc. |
| Câu hỏi lặp lại gửi trực tiếp cho TA | Chưa đo; quan sát có nhiều câu/buổi | Giảm 30-50% trong nhóm câu hỏi setup/thuật ngữ phổ biến | Cần log câu hỏi trước và sau pilot. |
| Tỷ lệ hoàn thành lab đúng giờ | Chưa có baseline chính thức | Tăng nhẹ 10-20% ở nhóm dùng Virtual TA | Chỉ đo sau khi có pilot 1 buổi. |
| Risk mới | Thấp ở quy trình cũ nhưng chậm | AI có thể trả lời sai hoặc quá tự tin | Giảm rủi ro bằng nguồn tham chiếu, confidence, và handoff. |

## Bước 5.3 — Problem Statement v0

| Field | Nội dung |
| :--- | :--- |
| **Actor** | Học viên đang làm lab, đặc biệt học viên trái ngành; TA/mentor là actor phụ bị quá tải support. |
| **Workflow** | Trong lab, học viên gặp thuật ngữ/lỗi/setup, tự tra cứu, không giải được thì hỏi TA/mentor, chờ hỗ trợ, nhận câu trả lời thủ công rồi tiếp tục làm. |
| **Bottleneck** | Bước giải đáp thắc mắc real-time phụ thuộc quá nhiều vào TA/mentor, trong khi nhiều câu hỏi có thể trả lời bằng tài liệu lớp hoặc FAQ. |
| **Impact** | Học viên bị đứng tiến độ, không hoàn thành lab đúng giờ; TA/mentor bị phân tán bởi câu hỏi lặp lại; chất lượng buổi lab giảm. |
| **Success Metric** | Giảm thời gian phản hồi đầu tiên cho câu hỏi phổ biến xuống dưới 1 phút; giảm 30-50% câu hỏi lặp lại gửi trực tiếp cho TA; tăng tỷ lệ hoàn thành lab đúng giờ sau pilot. |
| **Boundary** | Chỉ xử lý 1 bài lab, các câu hỏi setup/thuật ngữ/lỗi phổ biến có trong tài liệu. Không làm hộ bài, không chấm điểm, không trả lời ngoài nguồn, không thay TA/mentor cho case khó. |

Điểm còn cần kiểm ở v0:

```text
Baseline chưa đủ chắc: cần đo số câu hỏi lặp lại, thời gian chờ TA, và completion rate trong ít nhất 1 buổi lab trước pilot.
```

---

# Phase 6 — Rule / Workflow / Agent + Decision

## Bước 6.0 — Ma trận độ phù hợp với AI

Bài toán của nhóm nằm ở ô nào?

```text
Độ mơ hồ trung bình-cao, độ phức tạp trung bình.
```

Vì sao?

```text
Câu hỏi của học viên có nhiều cách diễn đạt và thường thiếu context, nên không thể chỉ dùng keyword rule. Tuy vậy, workflow xử lý vẫn khá rõ: nhận câu hỏi, phân loại, truy xuất tài liệu, trả lời kèm nguồn, nhận feedback, escalates nếu không chắc. Vì vậy pilot nên là Workflow có RAG và rule handoff, chưa cần full Agent tự lập kế hoạch phức tạp.
```

## Bước 6.1 — So sánh Rule / Workflow / Agent

| Mức | Phương án cho bài toán nhóm | Khi nào đủ | Rủi ro | Chọn? |
| :--- | :--- | :--- | :--- | :--- |
| **Rule** | FAQ theo keyword: nếu câu hỏi chứa "API key", "cài môi trường", "deadline", "nộp bài" thì trả lời mẫu. | Đủ cho câu hỏi rất lặp lại, ít biến thể, câu trả lời cố định. | Không hiểu ngữ cảnh bài lab, dễ miss khi học viên diễn đạt khác, không giải thích được concept. | Không chọn làm mức chính; dùng làm guardrail/phân loại ban đầu. |
| **Workflow** | Virtual TA workflow: phân loại câu hỏi, RAG trên slide/lab guide/FAQ, trả lời kèm nguồn, xin thêm context nếu thiếu, escalates cho TA khi không chắc. | Đủ cho pilot 1 bài lab với tài liệu rõ và nhóm câu hỏi phổ biến. | Phụ thuộc chất lượng tài liệu; vẫn có rủi ro hallucination nếu retrieval sai. | **Chọn cho pilot.** |
| **Agent** | Agent có thể tự quyết định hỏi thêm, tìm nhiều nguồn, chạy tool kiểm tra lỗi, tạo checklist cá nhân hóa, theo dõi tiến độ từng học viên. | Hữu ích khi đã có data đầy đủ, nhiều loại tool, nhiều workflow phụ và owner vận hành. | Quá rộng cho lab hôm nay; rủi ro tự tin sai, khó debug, khó kiểm soát boundary. | Chưa chọn; để roadmap sau pilot. |

Mức chọn:

```text
Workflow
```

Vì sao chọn:

```text
Workflow đủ để giải bottleneck chính trong phạm vi nhỏ: học viên cần câu trả lời nhanh, có nguồn, đúng context bài lab và có đường chuyển cho TA khi AI không chắc. Workflow cũng dễ đo hơn Agent: đo số câu hỏi, thời gian phản hồi, tỷ lệ resolved, tỷ lệ escalated và feedback hữu ích/không hữu ích.
```

Vì sao không chọn mức đơn giản hơn:

```text
Rule-based FAQ chỉ xử lý được câu hỏi cố định. Trong lab, học viên thường mô tả lỗi/thuật ngữ bằng nhiều cách khác nhau, thiếu context hoặc hỏi theo bước đang làm. Vì vậy cần RAG để truy xuất đúng đoạn tài liệu và tạo câu trả lời theo ngữ cảnh.
```

Vì sao chưa chọn Agent:

```text
Agent đầy đủ chưa cần thiết cho pilot vì chưa có nhiều tool, chưa có dữ liệu tiến độ học viên, và chưa đủ guardrail để AI tự quyết định nhiều bước. Bắt đầu bằng Workflow giúp giảm rủi ro và vẫn đo được impact rõ.
```

## Bước 6.2 — Problem Statement v1

| Field | Nội dung |
| :--- | :--- |
| **Actor** | Học viên đang làm lab trong bootcamp AI/coding, đặc biệt học viên trái ngành; TA/mentor là người review và xử lý escalation. |
| **Workflow** | Khi làm lab, học viên gặp thuật ngữ, lỗi setup hoặc lỗi code phổ biến; hiện tại họ tự tra cứu hoặc chờ TA/mentor trả lời thủ công. |
| **Bottleneck** | Bước support tuyến đầu trong lab bị nghẽn vì nhiều câu hỏi lặp lại và nhiều học viên cần phản hồi cùng lúc, trong khi TA/mentor là nguồn lực hữu hạn. |
| **Impact** | Học viên bị đứng tiến độ, giảm tỷ lệ hoàn thành lab đúng giờ; TA/mentor mất thời gian với câu hỏi lặp lại thay vì hỗ trợ case khó; lớp học bị chậm nhịp. |
| **Success Metric** | Trong pilot 1 bài lab: thời gian phản hồi đầu tiên cho câu hỏi phổ biến dưới 1 phút; ít nhất 50% câu hỏi setup/thuật ngữ phổ biến được Virtual TA xử lý mà không cần TA; giảm 30-50% câu hỏi lặp lại gửi trực tiếp cho TA; học viên đánh giá câu trả lời hữu ích >= 4/5. |
| **Boundary** | Chỉ dùng tài liệu được duyệt: lab guide, slide, FAQ. Không làm hộ bài, không generate toàn bộ solution, không chấm điểm, không trả lời ngoài nguồn. Low confidence hoặc câu hỏi ảnh hưởng grading phải chuyển TA/mentor. |
| **AI intervention point** | Sau khi học viên đặt câu hỏi và trước khi hỏi TA: AI phân loại intent, truy xuất tài liệu, trả lời ngắn kèm nguồn, đề xuất bước thử tiếp theo, hoặc escalates cho TA nếu thiếu context/không chắc. |
| **Mức chọn** | Workflow: RAG QA + rule-based triage/escalation. |
| **Rủi ro & người thật kiểm tra** | Rủi ro chính là hallucination, nguồn lỗi thời, trả lời làm hộ. TA/mentor kiểm tra bộ FAQ, review các câu bị downvote/escalated, cập nhật tài liệu sau mỗi buổi lab. |

## Bước 6.3 — Final decision

| Câu hỏi | Yes / Not Yet / No | Ghi chú |
| :--- | :--- | :--- |
| Actor và workflow đã rõ chưa? | Yes | Actor chính là học viên làm lab; actor phụ là TA/mentor. Workflow trước-sau đã vẽ được. |
| Baseline và success metric đã đo được chưa? | Not Yet | Có metric mục tiêu, nhưng cần đo baseline trong 1 buổi lab thật. |
| Có data/input đủ dùng chưa? | Not Yet | Cần gom 1 lab guide, slide liên quan, FAQ setup, và 10-20 câu hỏi mẫu. |
| Nếu AI sai, hậu quả có chấp nhận được không? | Yes, nếu có boundary | Chỉ cho phép trả lời trong phạm vi tài liệu; câu không chắc phải chuyển TA. |
| Có người review/owner vận hành không? | Yes | TA/mentor là owner review câu trả lời lỗi và cập nhật FAQ. |
| Có cách non-AI đơn giản hơn không? | Yes | FAQ/checklist có thể xử lý một phần, nhưng không đủ cho câu hỏi diễn đạt đa dạng và cần giải thích theo context lab. |

Decision:

```text
Go cho pilot nhỏ; Not Yet cho rollout toàn lớp nếu chưa đo baseline và chưa chuẩn hóa tài liệu.
```

Lý do:

```text
Bài toán có actor, workflow, bottleneck và metric đủ rõ để thử nghiệm nhỏ. Tuy nhiên, quyết định Go chỉ áp dụng cho pilot giới hạn trong 1 bài lab, vì dữ liệu nguồn và baseline hiện tại chưa đủ chắc cho rollout rộng.
```

Nếu Go, pilot nhỏ nhất là:

```text
Làm Virtual TA cho 1 bài lab cụ thể trong 1 buổi:
1. Input: lab guide, slide liên quan, FAQ setup, 10-20 câu hỏi mẫu.
2. Scope: setup môi trường, thuật ngữ trong bài, lỗi phổ biến đã có trong tài liệu.
3. Output: câu trả lời ngắn, nguồn tham chiếu, bước thử tiếp theo, nút "hỏi TA".
4. Đo: số câu hỏi, thời gian phản hồi, tỷ lệ resolved, tỷ lệ escalated, feedback hữu ích 1-5, số câu hỏi lặp lại gửi trực tiếp cho TA.
```

Nếu Not Yet, cần validate gì trước:

```text
Trước rollout rộng cần validate: baseline thời gian chờ TA, tỷ lệ câu hỏi lặp lại, chất lượng tài liệu nguồn, mức độ học viên sẵn sàng hỏi Virtual TA trước khi hỏi người thật.
```

Nếu No-Go, nên làm gì thay AI:

```text
Nếu pilot cho thấy phần lớn pain đến từ tài liệu mở trễ hoặc học viên chưa đọc prerequisite, nên ưu tiên process fix: mở tài liệu sớm hơn, checklist trước buổi học, FAQ setup, và office hour ngắn trước lab.
```

