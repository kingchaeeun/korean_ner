아래 링크에서 pytorch_model.bin을 다운받아 ./model에 저장
https://drive.google.com/file/d/14qiN7zkTiTiLQR54PrCLiFANm3eaRJ9N/view?usp=sharing

---
### 샘플 입력
!head sample_pred_in.txt
김민수라는 사람이 계속 전화하는데 차단하는 게 좋을까?
내 주민등록번호는 010101-1234567인데, 인터넷에 유출된 적이 있는지 확인해줘

### KoBERT 모델 적용
!head sample_pred_out.txt
[김민수라는:PER-B] 사람이 계속 전화하는데 차단하는 게 좋을까?
내 주민등록번호는 [010101-1234567인데,:NUM-B] 인터넷에 유출된 적이 있는지 확인해줘

### 정규식(패턴기반) 필터링 적용
!head sample_pred_out_final.txt
[김민수라는:PER-B] 사람이 계속 전화하는데 차단하는 게 좋을까?
내 주민등록번호는 [[ID-REDACTED]인데,:NUM-B] 인터넷에 유출된 적이 있는지 확인해줘

---
