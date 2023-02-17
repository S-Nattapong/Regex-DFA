# Regex-DFA
- main method

   ![image](https://user-images.githubusercontent.com/78334486/219798420-e633234e-8e53-4bfc-b42a-98bd7a07b42a.png)



- DStates เป็นชุดของ state ที่ใช้สำหรับสร้าง final dfa 
- input นั้นจะถูกรับมาจาก users
- String regex = มีไว้สำหรับรับ RE ที่ต้องการจาก stdin
- getSymbols (regex); = โค้ดบรรทัดนี้ตั้งค่าอินพุต Set
- SyntaxTree st = SyntaxTree ใหม่ (regex); บรรทัดนี้มีไว้สร้างโครงสร้างไวยากรณ์ที่สอดคล้องกันของ RE ที่ป้อน
- root = st.getRoot(); รับรูทของแผนผังไวยากรณ์
- followPos = st.getFollowPos(); ทำการอ้างอิงใหม่ไปยังตัวแปร Set of followpos
- State q0 = createDFA();  สร้าง DFA โดยใช้โครงสร้างไวยากรณ์และกำหนด q0 เป็น start state ของ DFA ที่เป็นผลลัพธ์
- DfaTraversal dfat = new DfaTraversal(q0, input); สร้างวัตถุ DFA Traversal ใหม่สำหรับการเดินใน DFA และรับรู้ว่า DFA สามารถ accept string นั้นได้หรือไม่

========================================================================================================================================================================================

- ตัวอย่างการทำงานของโปรแกรม โดยขั้นแรกให้ป้อนRE เข้าไปตามด้วย input ที่ต้องการ จากนั้นจะได้ output ออกมาตามภาพ                                                                       output ที่แสดงออกมาจะบ่งออกว่า input ที่ป้อนเข้าไปนั้น ถูก accept โดย RE หรือไม่

ตัวอย่างที่ RE accept

![image](https://user-images.githubusercontent.com/78334486/219796851-1618cc8f-b064-4d92-acd7-17e51a29fbfd.png) 


ตัวอย่างที่ RE ไม่ accept


![image](https://user-images.githubusercontent.com/78334486/219797708-d78c977e-1176-4f21-8e43-53bd941eca2d.png)



