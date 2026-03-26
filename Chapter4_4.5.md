## 4.5 คำสำคัญ คำถามทบทวน และโจทย์ปัญหา

### คำสำคัญ

access time, associative mapping, cache hit, cache line, cache memory, cache miss, cache set, data cache, direct access, direct mapping, high-performance computing (HPC), hit, hit ratio, instruction cache, L1 cache, L2 cache, L3 cache, line, locality, logical cache, memory hierarchy, miss, multilevel cache, physical address, physical cache, random access, replacement algorithm, secondary memory, sequential access, set-associative mapping, spatial locality, split cache, tag, temporal locality, unified cache, virtual address, virtual cache, write back, write through

### คำถามทบทวน

**4.1** ความแตกต่างระหว่าง sequential access, direct access และ random access คืออะไร?

**4.2** ความสัมพันธ์ทั่วไประหว่าง access time, ราคาหน่วยความจำ และความจุคืออะไร?

**4.3** หลักการ locality เกี่ยวข้องกับการใช้หน่วยความจำหลายระดับอย่างไร?

**4.4** ความแตกต่างระหว่าง direct mapping, associative mapping และ set-associative mapping คืออะไร?

**4.5** สำหรับ direct-mapped cache ที่อยู่ main memory ถูกมองว่าประกอบด้วยสามฟิลด์ แสดงรายการและนิยามสามฟิลด์นั้น

**4.6** สำหรับ associative cache ที่อยู่ main memory ถูกมองว่าประกอบด้วยสองฟิลด์ แสดงรายการและนิยามสองฟิลด์นั้น

**4.7** สำหรับ set-associative cache ที่อยู่ main memory ถูกมองว่าประกอบด้วยสามฟิลด์ แสดงรายการและนิยามสามฟิลด์นั้น

**4.8** ความแตกต่างระหว่าง spatial locality และ temporal locality คืออะไร?

**4.9** โดยทั่วไป กลยุทธ์สำหรับการใช้ประโยชน์จาก spatial locality และ temporal locality คืออะไร?

### โจทย์ปัญหา

**4.1** set-associative cache ประกอบด้วย 64 line หรือ slot แบ่งเป็น four-line set Main memory มี 4K block ของ 128 word แต่ละ block แสดงรูปแบบที่อยู่ main memory

**4.2** two-way set-associative cache มี line ขนาด 16 byte และขนาดรวม 8 kB Main memory ขนาด 64 MB สามารถระบุที่อยู่ได้ระดับ byte แสดงรูปแบบที่อยู่ main memory

**4.3** สำหรับที่อยู่ main memory แบบ hexadecimal 111111, 666666, BBBBBB แสดงข้อมูลต่อไปนี้ในรูปแบบ hexadecimal:
  - a. ค่า Tag, Line และ Word สำหรับ direct-mapped cache โดยใช้รูปแบบของรูปที่ 4.10
  - b. ค่า Tag และ Word สำหรับ associative cache โดยใช้รูปแบบของรูปที่ 4.12
  - c. ค่า Tag, Set และ Word สำหรับ two-way set-associative cache โดยใช้รูปแบบของรูปที่ 4.15

**4.4** แสดงค่าต่อไปนี้:
  - a. สำหรับตัวอย่าง direct cache ในรูปที่ 4.10: ความยาวที่อยู่, จำนวน addressable unit, ขนาด block, จำนวน block ใน main memory, จำนวน line ใน cache, ขนาด tag
  - b. สำหรับตัวอย่าง associative cache ในรูปที่ 4.12: ความยาวที่อยู่, จำนวน addressable unit, ขนาด block, จำนวน block ใน main memory, จำนวน line ใน cache, ขนาด tag
  - c. สำหรับตัวอย่าง two-way set-associative cache ในรูปที่ 4.15: ความยาวที่อยู่, จำนวน addressable unit, ขนาด block, จำนวน block ใน main memory, จำนวน line ใน set, จำนวน set, จำนวน line ใน cache, ขนาด tag

**4.5** พิจารณา 32-bit microprocessor ที่มี on-chip 16-kB four-way set-associative cache สมมติว่า cache มี line size สี่ 32-bit word วาด block diagram ของ cache นี้ที่แสดงองค์กรและวิธีที่ address field ต่าง ๆ ใช้ระบุ cache hit/miss word จากตำแหน่ง memory ABCDE8F8 แมปไปยังที่ใดใน cache?

**4.6** กำหนด specification ต่อไปนี้สำหรับ external cache memory: four-way set associative; line size สอง 16-bit word; สามารถรองรับ 4K 32-bit word รวมจาก main memory; ใช้กับ 16-bit processor ที่ออก 24-bit address ออกแบบโครงสร้าง cache พร้อมข้อมูลที่เกี่ยวข้องทั้งหมดและแสดงวิธีที่ cache ตีความที่อยู่ของโปรเซสเซอร์

**4.7** Intel 80486 มี on-chip, unified cache มีขนาด 8 kB และมี four-way set-associative organization และ block length สี่ 32-bit word cache ถูกจัดเป็น 128 set มี "line valid bit" เดียวและสามบิต B0, B1 และ B2 ("LRU" bits) ต่อ line เมื่อ cache miss 80486 อ่าน 16-byte line จาก main memory ใน bus memory read burst วาด diagram ที่เรียบง่ายของ cache และแสดงวิธีที่ address field ต่าง ๆ ถูกตีความ

**4.8** พิจารณาเครื่องที่มี byte addressable main memory ขนาด 2¹⁶ byte และ block size 8 byte สมมติว่าใช้ direct mapped cache ประกอบด้วย 32 line กับเครื่องนี้
  - a. 16-bit memory address ถูกแบ่งอย่างไรเป็น tag, line number และ byte number?
  - b. byte ที่มีที่อยู่แต่ละตัวต่อไปนี้จะถูกจัดเก็บใน line ใด?
    - 0001 0001 0001 1011
    - 1100 0011 0011 0100
    - 1101 0000 0001 1101
    - 1010 1010 1010 1010
  - c. สมมติว่า byte ที่มีที่อยู่ 0001 1010 0001 1010 ถูกจัดเก็บใน cache ที่อยู่ของ byte อื่นที่จัดเก็บพร้อมกับมันคืออะไร?
  - d. จำนวน byte ทั้งหมดของ memory ที่สามารถจัดเก็บใน cache คือเท่าไหร่?
  - e. ทำไม tag ถึงถูกจัดเก็บใน cache ด้วย?

**4.9** สำหรับ on-chip cache Intel 80486 ใช้ replacement algorithm ที่เรียกว่า pseudo least recently used เชื่อมกับแต่ละ 128 set ของสี่ line (ระบุว่า L0, L1, L2, L3) มีสามบิต B0, B1 และ B2 replacement algorithm ทำงานดังนี้: เมื่อ line ต้องถูกแทนที่ cache จะระบุก่อนว่าการใช้ล่าสุดมาจาก L0 และ L1 หรือ L2 และ L3 แล้ว cache จะระบุว่า block คู่ใดถูกใช้น้อยกว่าล่าสุดและระบุให้แทนที่
  - a. ระบุวิธีที่บิต B0, B1 และ B2 ถูกตั้งค่า แล้วอธิบายด้วยคำพูดว่าใช้อย่างไรใน replacement algorithm
  - b. แสดงว่า algorithm ของ 80486 เป็น approximation ของ LRU algorithm จริง ๆ
  - c. แสดงให้เห็นว่า LRU algorithm จริงต้องการ 6 bit ต่อ set

**4.10** set-associative cache มี block size สี่ 16-bit word และ set size 2 cache สามารถรองรับรวม 4096 word main memory ขนาดที่สามารถ cache ได้คือ 64K × 32 bit ออกแบบโครงสร้าง cache และแสดงวิธีที่ที่อยู่ของโปรเซสเซอร์ถูกตีความ

**4.11** พิจารณาระบบหน่วยความจำที่ใช้ 32-bit address ระบุที่อยู่ระดับ byte บวกกับ cache ที่ใช้ line size 64 byte
  - a. สมมติว่า direct mapped cache มี tag field ในที่อยู่ 20 bit แสดงรูปแบบที่อยู่และระบุ parameter ต่อไปนี้: จำนวน addressable unit, จำนวน block ใน main memory, จำนวน line ใน cache, ขนาด tag
  - b. สมมติว่า associative cache แสดงรูปแบบที่อยู่และระบุ parameter: จำนวน addressable unit, จำนวน block ใน main memory, จำนวน line ใน cache, ขนาด tag
  - c. สมมติว่า four-way set-associative cache มี tag field ในที่อยู่ 9 bit แสดงรูปแบบที่อยู่และระบุ parameter: จำนวน addressable unit, จำนวน block ใน main memory, จำนวน line ใน set, จำนวน set ใน cache, จำนวน line ใน cache, ขนาด tag

**4.12** พิจารณาคอมพิวเตอร์ที่มีคุณลักษณะต่อไปนี้: main memory รวม 1 MB; word size 1 byte; block size 16 byte; และ cache size 64 kB
  - a. สำหรับที่อยู่ main memory F0010, 01234 และ CABBE ให้ tag ที่สอดคล้องกัน, cache line address และ word offset สำหรับ direct-mapped cache
  - b. ให้สองที่อยู่ main memory ใด ๆ ที่มี tag ต่างกันซึ่งแมปไปยัง cache slot เดียวกันสำหรับ direct-mapped cache
  - c. สำหรับที่อยู่ main memory F0010 และ CABBE ให้ค่า tag และ offset ที่สอดคล้องกันสำหรับ fully-associative cache
  - d. สำหรับที่อยู่ main memory F0010 และ CABBE ให้ค่า tag, cache set และ offset ที่สอดคล้องกันสำหรับ two-way set-associative cache

**4.13** อธิบายเทคนิคง่าย ๆ สำหรับการนำ LRU replacement algorithm ไปใช้ใน four-way set-associative cache

**4.14** พิจารณาตัวอย่าง 4.3 อีกครั้ง คำตอบเปลี่ยนไปอย่างไรถ้า main memory ใช้ block transfer capability ที่มี first-word access time 30 ns และ access time 5 ns สำหรับแต่ละ word ต่อไป?

**4.15** พิจารณา code ต่อไปนี้:
```
for (i = 0; i < 20; i++)
  for (j = 0; j < 10; j++)
    a[i] = a[i] * j
```
  - a. ให้ตัวอย่างหนึ่งของ spatial locality ใน code
  - b. ให้ตัวอย่างหนึ่งของ temporal locality ใน code

**4.16** Generalize สมการ (4.2) และ (4.3) ในภาคผนวก 4A ให้กับ N-level memory hierarchy

**4.17** ระบบคอมพิวเตอร์มี main memory 32K 16-bit word และ 4K word cache แบ่งเป็น four-line set ที่มี 64 word ต่อ line สมมติว่า cache ว่างในตอนแรก โปรเซสเซอร์ดึง word จากตำแหน่ง 0, 1, 2, …, 4351 ตามลำดับ แล้วทำซ้ำลำดับการดึงนี้อีกเก้าครั้ง cache เร็วกว่า main memory 10 เท่า ประมาณการปรับปรุงที่เกิดจากการใช้ cache สมมติว่าใช้ LRU policy สำหรับการแทนที่ block

**4.18** พิจารณา cache ที่มี 4 line ของ 16 byte แต่ละตัว Main memory แบ่งเป็น block ขนาด 16 byte แต่ละ block นั่นคือ block 0 มี byte ที่มีที่อยู่ 0 ถึง 15 เป็นต้น พิจารณาโปรแกรมที่เข้าถึงหน่วยความจำในลำดับที่อยู่ต่อไปนี้: ครั้งเดียว: 63 ถึง 70; วนซ้ำสิบครั้ง: 15 ถึง 32; 80 ถึง 95
  - a. สมมติว่า cache ถูกจัดเป็น direct mapped Memory block 0, 4 และต่อไปถูกกำหนดให้ line 1; block 1, 5 และต่อไปให้ line 2; เป็นต้น คำนวณ hit ratio
  - b. สมมติว่า cache ถูกจัดเป็น two-way set associative มีสอง set ของสอง line แต่ละตัว block คู่ถูกกำหนดให้ set 0 และ block คี่ถูกกำหนดให้ set 1 คำนวณ hit ratio สำหรับ two-way set-associative cache โดยใช้ least recently used replacement scheme

**4.19** พิจารณาระบบหน่วยความจำที่มี parameter ต่อไปนี้:
$$T_c = 100\ \text{ns} \quad C_c = 10^{-4}\ \text{\$/bit}$$
$$T_m = 1200\ \text{ns} \quad C_m = 10^{-5}\ \text{\$/bit}$$
  - a. ราคาของ main memory 1 MB คือเท่าไหร่?
  - b. ราคาของ main memory 1 MB โดยใช้เทคโนโลยี cache memory คือเท่าไหร่?
  - c. ถ้า effective access time มากกว่า cache access time 10% hit ratio H คือเท่าไหร่?

**4.20**
  - a. พิจารณา L1 cache ที่มี access time 1 ns และ hit ratio H = 0.95 สมมติว่าเราสามารถเปลี่ยนการออกแบบ cache (ขนาด cache, cache organization) เพื่อเพิ่ม H เป็น 0.97 แต่เพิ่ม access time เป็น 1.5 ns เงื่อนไขใดบ้างที่ต้องเป็นจริงเพื่อให้การเปลี่ยนแปลงนี้ส่งผลให้ประสิทธิภาพดีขึ้น?
  - d. อธิบายว่าทำไมผลลัพธ์นี้จึงสมเหตุสมผลในเชิงสัญชาตญาณ

**4.21** พิจารณา single-level cache ที่มี access time 2.5 ns, line size 64 byte และ hit ratio H = 0.95 Main memory ใช้ block transfer capability ที่มี first-word (4 byte) access time 50 ns และ access time 5 ns สำหรับแต่ละ word ต่อไป
  - a. access time เมื่อเกิด cache miss คือเท่าไหร่? สมมติว่า cache รอจนกว่า line จะถูกดึงจาก main memory แล้วประมวลผลซ้ำสำหรับ hit
  - b. สมมติว่าการเพิ่ม line size เป็น 128 byte ทำให้ H เพิ่มเป็น 0.97 สิ่งนี้ลด average memory access time หรือไม่?

**4.22** คอมพิวเตอร์มี cache, main memory และ disk ที่ใช้สำหรับ virtual memory ถ้า word ที่อ้างอิงอยู่ใน cache จะใช้เวลา 20 ns ในการเข้าถึง ถ้าอยู่ใน main memory แต่ไม่ใน cache จะต้องใช้ 60 ns เพื่อโหลดเข้า cache แล้วเริ่มอ้างอิงใหม่ ถ้า word ไม่อยู่ใน main memory จะต้องใช้ 12 ms เพื่อดึง word จาก disk ตามด้วย 60 ns เพื่อ copy ไปยัง cache แล้วเริ่มอ้างอิงใหม่ cache hit ratio คือ 0.9 และ main memory hit ratio คือ 0.6 เวลาเฉลี่ยเป็นนาโนวินาทีที่ต้องการในการเข้าถึง word ที่อ้างอิงบนระบบนี้คือเท่าไหร่?

**4.23** พิจารณา cache ที่มี line size 64 byte สมมติว่าโดยเฉลี่ย 30% ของ line ใน cache เป็น dirty word ประกอบด้วย 8 byte
  - a. สมมติว่ามี miss rate 3% (0.97 hit ratio) คำนวณปริมาณ main memory traffic เป็น byte ต่อ instruction สำหรับทั้ง write-through และ write-back policy Memory ถูกอ่านเข้า cache ทีละ line แต่สำหรับ write-back word เดียวสามารถเขียนจาก cache ไปยัง main memory
  - b. ทำซ้ำส่วน a สำหรับ rate 5%
  - c. ทำซ้ำส่วน a สำหรับ rate 7%
  - d. ข้อสรุปใดที่คุณสามารถดึงออกมาจากผลลัพธ์เหล่านี้?

**4.24** บน Motorola 68020 microprocessor การเข้าถึง cache ใช้เวลา clock cycle สองรอบ การเข้าถึง data จาก main memory ผ่าน bus ไปยังโปรเซสเซอร์ใช้เวลา clock cycle สามรอบในกรณีที่ไม่มีการแทรก wait state; ข้อมูลถูกส่งให้โปรเซสเซอร์พร้อมกันกับการส่งไปยัง cache
  - a. คำนวณความยาวที่มีประสิทธิภาพของ memory cycle โดยกำหนด hit ratio 0.9 และ clocking rate 16.67 MHz
  - b. ทำซ้ำการคำนวณโดยสมมติว่ามีการแทรก wait state สองตัวของ one cycle แต่ละตัวต่อ memory cycle คุณสรุปอะไรได้จากผลลัพธ์?

**4.25** สมมติว่าโปรเซสเซอร์มี memory cycle time 300 ns และ instruction processing rate 1 MIPS โดยเฉลี่ยแต่ละ instruction ต้องการ bus memory cycle หนึ่งรอบสำหรับ instruction fetch และหนึ่งรอบสำหรับ operand ที่เกี่ยวข้อง
  - a. คำนวณ utilization ของ bus โดยโปรเซสเซอร์
  - b. สมมติว่าโปรเซสเซอร์ติดตั้ง instruction cache และ hit ratio ที่เกี่ยวข้องคือ 0.5 ระบุผลกระทบต่อ bus utilization

**4.26** ประสิทธิภาพของระบบ single-level cache สำหรับ read operation สามารถระบุลักษณะได้ด้วยสมการต่อไปนี้:
$$T_a = T_c + (1-H)T_m$$
โดยที่ $T_a$ คือ average access time, $T_c$ คือ cache access time, $T_m$ คือ memory access time (memory to processor register) และ H คือ hit ratio สำหรับความเรียบง่าย สมมติว่า word ที่เป็นคำถามถูกโหลดเข้า cache พร้อมกันกับการโหลดเข้า processor register นี่เป็นรูปแบบเดียวกับสมการ (4.2)
  - a. นิยาม $T_b$ = เวลาในการถ่ายโอน line ระหว่าง cache และ main memory และ W = เศษส่วนของ write reference ปรับสมการก่อนหน้าเพื่อรองรับทั้ง write และ read โดยใช้ write-through policy
  - b. นิยาม $W_b$ เป็นความน่าจะเป็นที่ line ใน cache ถูกแก้ไข ให้สมการสำหรับ $T_a$ สำหรับ write-back policy

**4.27** สำหรับระบบที่มี cache สองระดับ นิยาม $T_{c_1}$ = first-level cache access time; $T_{c_2}$ = second-level cache access time; $T_m$ = memory access time; $H_1$ = first-level cache hit ratio; $H_2$ = combined first/second level cache hit ratio ให้สมการสำหรับ $T_a$ สำหรับ read operation

**4.28** สมมติว่ามีคุณลักษณะประสิทธิภาพต่อไปนี้บน cache read miss: หนึ่ง clock cycle เพื่อส่งที่อยู่ไปยัง main memory และสี่ clock cycle เพื่อเข้าถึง 32-bit word จาก main memory และถ่ายโอนไปยังโปรเซสเซอร์และ cache
  - a. ถ้า cache line size เป็น one word miss penalty (เวลาเพิ่มเติมที่ต้องการสำหรับ read เมื่อเกิด read miss) คือเท่าไหร่?
  - b. miss penalty คือเท่าไหรถ้า cache line size เป็นสี่ word และมีการดำเนินการ multiple, nonburst transfer?
  - c. miss penalty คือเท่าไหรถ้า cache line size เป็นสี่ word และดำเนินการ transfer โดยมีหนึ่ง clock cycle ต่อ word transfer?

**4.29** สำหรับการออกแบบ cache ของปัญหาก่อนหน้า สมมติว่าการเพิ่ม line size จาก one word เป็นสี่ word ส่งผลให้ read miss rate ลดลงจาก 3.2% เป็น 1.1% สำหรับทั้ง nonburst transfer และ burst transfer case average miss penalty เฉลี่ยในการ read ทั้งหมดสำหรับ line size ทั้งสองแบบคือเท่าไหร่?

---
