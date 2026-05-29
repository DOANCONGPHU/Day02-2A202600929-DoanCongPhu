# Phase 7 — Individual Reflection (15')

## Tôi đã tham gia vào phần nào?

| Hoạt động | Tôi đã làm gì? | Kết quả / ảnh hưởng |
|---|---|---|
| Scan cá nhân | Tôi scan 9 vấn đề từ trải nghiệm học bootcamp, tập trung nhiều vào học viên trái ngành, tài liệu mở sát giờ, thiếu AI tutor, setup môi trường và các pain trong lớp. | Có đủ input cá nhân để pitch với nhóm, trong đó top 3 đều có actor, bottleneck, impact và workflow sơ bộ. |
| Pitch Problem Card | Tôi pitch 3 problem chính: tài liệu mở sát giờ, học viên trái ngành không load kịp kiến thức, và thiếu AI tutor hỗ trợ recap/giải thích thuật ngữ. | Nhóm hiểu rõ cụm "hỗ trợ học tập" và đưa các vấn đề này vào cluster A/B khi hội tụ. |
| Challenge bài của bạn khác | Tôi so sánh các candidate của bạn khác theo actor, workflow, bottleneck, impact đo được và độ vừa sức lab. | Nhóm không chọn theo cảm tính mà dùng tiêu chí rõ hơn để shortlist và score. |
| Gom trùng / cluster | Tôi tham gia gom các vấn đề thành 4 nhóm: hỗ trợ học tập, tiếp thu kiến thức, giao tiếp/thông báo và vận hành B2B. | Các candidate rời rạc được nhìn theo pattern chung, giúp nhóm dễ so sánh hơn. |
| Chọn candidate problem | Ban đầu tôi nghiêng về Virtual TA vì gần trải nghiệm học tập, nhưng sau khi score theo từng candidate, tôi đồng ý chọn #9 về QA cuộc gọi CSKH. | Nhóm chọn được bài ít trùng hơn, có KPI business rõ và vẫn phù hợp AI. |
| Validation / research | Tôi cùng nhóm xác định cần validate thêm bằng transcript/recording mẫu, rubric QA, baseline coverage và thời gian QA/call. | Bài không bị "AI-first"; nhóm ghi rõ phần nào là evidence hiện có, phần nào cần kiểm chứng trước rollout. |
| Workflow nhóm | Tôi góp phần chuyển workflow từ mô tả chung sang before/after cụ thể cho QA cuộc gọi: nghe thủ công -> transcript/rule/LLM scorecard/human review. | Workflow thể hiện rõ bottleneck, AI intervention point và human boundary. |
| Problem Statement | Tôi tham gia làm rõ Actor, Workflow, Bottleneck, Impact, Success Metric và Boundary cho candidate #9. | Problem Statement v1 chặt hơn v0, có metric và giới hạn AI rõ hơn. |
| Rule / Workflow / Agent | Tôi cùng nhóm so sánh Rule, Workflow và Agent, sau đó chọn Workflow thay vì nhảy thẳng sang Agent. | Quyết định hợp lý hơn vì pilot chỉ cần transcript + rule check + LLM scorecard + QA review. |
| Decision | Tôi đồng thuận decision: Go cho pilot nhỏ bằng transcript mẫu, Not Yet cho rollout production. | Quyết định cuối cân bằng giữa tiềm năng business và rủi ro privacy/compliance. |

## Bảng dùng AI trong reflection

| Phase | Tôi dùng AI để làm gì? | AI hữu ích ở đâu? | AI sai/hời hợt ở đâu? | Tôi sửa gì bằng nhận định của mình? |
|---|---|---|---|---|
| Scan | Gợi ý thêm góc nhìn problem và kiểm tra problem card. | Giúp tôi nhìn rõ actor, bottleneck và metric cho các vấn đề học tập. | Có lúc gợi ý hơi rộng như "AI tutor cá nhân hóa toàn bộ". | Tôi giữ lại các pain mình thật sự quan sát được trong lớp. |
| Problem Card | Nhờ AI phản biện Problem Card theo tiêu chí actor/workflow/bottleneck/metric. | Giúp làm rõ workflow hiện tại và success metric. | AI có xu hướng làm solution nghe "ngầu" hơn cần thiết. | Tôi bổ sung non-AI alternative như mở tài liệu sớm, checklist, FAQ. |
| Workflow | Nhờ AI chuyển mô tả thành ASCII workflow before/after. | Nhanh hơn khi vẽ flow và thấy rõ bước nghẽn. | Ban đầu AI gộp nhiều bước lại, làm bottleneck chưa sắc. | Tôi tách lại từng bước: input, actor, output, thời gian/tần suất. |
| Research | Nhờ AI gợi ý các tool/case tương tự cho QA cuộc gọi CSKH. | Giúp tìm pattern như scorecard, transcript analytics, human review, coaching. | Một số claim nếu không có nguồn sẽ dễ thành bịa số liệu. | Tôi chỉ giữ nguồn/tool có link rõ và không dùng số liệu chưa verify. |
| Problem Statement | Nhờ AI giúp cấu trúc v0/v1 theo 6 field và thêm boundary. | Giúp câu chữ chặt hơn, nhất là phần impact và success metric. | AI ban đầu nghiêng về Virtual TA do gần context học tập hơn. | Tôi cập nhật lại toàn bộ PS theo candidate #9 sau khi nhóm chọn business problem. |
| Rule / Workflow / Agent | Nhờ AI so sánh 3 mức giải pháp. | Giúp thấy Rule đủ cho keyword/script, Workflow đủ cho pilot, Agent là roadmap sau. | AI có thể đề xuất Agent quá sớm. | Tôi hạ mức chọn về Workflow để giảm rủi ro và dễ đo trong lab. |
| Decision | Nhờ AI kiểm tra decision Go/Not Yet/No-Go có nhất quán không. | Giúp tách rõ Go cho pilot nhỏ và Not Yet cho production. | Nếu để AI quyết định thay, dễ bỏ qua privacy/compliance. | Tôi giữ human review, ẩn danh dữ liệu và QA duyệt cuối trong boundary. |

## Reflection câu hỏi mở

- Tôi học được gì khi nghe top 3 problems của các bạn khác?
- Nhóm có lúc nào bị solution-first không?
- Tôi có thay đổi ý kiến sau khi bị challenge không?
- Tôi đóng góp gì thật sự vào artifact cuối?
- Điều khó nhất khi viết Problem Statement là gì?
- Nếu làm lại, tôi sẽ challenge nhóm mạnh hơn ở điểm nào?

Reflection:

```text
Điều tôi học được nhiều nhất là một problem tốt không nhất thiết phải là problem gần trải nghiệm cá nhân nhất. Ban đầu tôi tập trung nhiều vào các vấn đề học tập như tài liệu mở sát giờ, học viên trái ngành không theo kịp lab, hoặc thiếu AI tutor. Các bài này rất thật với tôi, nhưng khi nhóm chấm theo candidate cụ thể thì bài QA cuộc gọi CSKH lại nổi bật hơn vì actor rõ, workflow rõ, bottleneck nằm ở một bước rất cụ thể và impact đo được bằng KPI vận hành.

Nhóm có lúc hơi solution-first, đặc biệt khi nói đến AI tutor hoặc Agent. Sau khi dùng tiêu chí shortlist và score, tôi thấy phải quay lại câu hỏi nền tảng hơn: ai đang đau, đang mắc ở bước nào, đo được gì, và nếu không dùng AI thì có cách nào đơn giản hơn không. Việc này giúp nhóm không chọn Agent chỉ vì nghe hiện đại.

Tôi có thay đổi ý kiến sau khi bị challenge. Ban đầu tôi nghiêng về Virtual TA vì đây là pain tôi hiểu rõ nhất. Nhưng candidate #9 có lợi thế là ít trùng, có ROI business rõ, và có thể làm prototype bằng transcript mẫu. Vì vậy tôi đồng ý với quyết định chọn #9, miễn là boundary phải rõ: AI chỉ pre-score, QA vẫn review cuối, dữ liệu phải ẩn danh và không dùng AI để kỷ luật tự động.

Đóng góp thật sự của tôi là đưa vào nhóm các problem học tập có workflow và dấu hiệu thật, tham gia gom cluster, đặt câu hỏi về độ rộng của solution, và cùng nhóm chỉnh từ "dùng AI để chấm cuộc gọi" thành một workflow cụ thể hơn: transcript -> rule check -> LLM scorecard -> evidence -> QA review. Điều khó nhất khi viết Problem Statement là biến một ý tưởng nghe đúng thành metric và boundary rõ. Nếu làm lại, tôi sẽ challenge nhóm mạnh hơn ở phần baseline: cần số cuộc gọi/ngày, thời gian QA/call và rubric thật trước khi nói impact chắc chắn.
```

## Tự kiểm cuối bài

- [x] [12đ cá nhân] Cá nhân có 5+ problems và top 3 Problem Cards.
- [x] [12đ cá nhân] Tôi đã pitch rõ và challenge nhóm đúng trọng tâm.
- [x] Nhóm có nhật ký hội tụ từ candidates về 1 bài.
- [x] [15đ nhóm] Nhóm có workflow trước/sau.
- [x] [20đ nhóm] Nhóm có Problem Statement v0/v1 với metric và boundary rõ.
- [x] [15đ nhóm] Nhóm có so sánh No AI / Rule / Workflow / Agent.
- [x] [10đ nhóm] Nhóm có Go / Not Yet / No-Go và lý do rõ.
- [x] [10đ cá nhân] Reflection cá nhân có nói rõ vai trò trong nhóm, cách dùng AI, điều học được và nếu làm lại sẽ đổi gì.
- [x] [6đ cá nhân] Tôi tự giải thích được mạch problem -> workflow -> metric -> boundary -> độ phù hợp với AI.

---
