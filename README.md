[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=24112774&assignment_repo_type=AssignmentRepo)
# Day 10 Lab: Data Pipeline & Data Observability

**Student Email:** hannuta69@gmail.com
**Name:** Trịnh Vũ Anh Tuấn

---

## Mo ta

(Mo ta ngan gon bai lab va nhung gi ban da lam)
- Set up môi trường ảo cho dự án
- Trong solution.py, load data từ raw_data.json, validate price và category, transform theo yêu cầu task 3, và load ra file processed_data
- Chạy Generate_garbage để tạo garbage_data
- Chạy agent_simulation để chạy cả processed_data và garbage_data
---

## Cach chay (How to Run)

### Prerequisites
```bash
pip install pandas
```

### Chay ETL Pipeline
```bash
python solution.py
```

### Chay Agent Simulation (Stress Test)
```bash
# Mo ta cach ban chay thi nghiem Clean vs Garbage data
```
Chay agent_simulation.py de kiem tra pipeline voi 2 bo du lieu:
1. Clean data: dữ liệu hợp lệ, có category va price > 0
2. Garbage data: dữ liệu lỗi (extreme outlier)
---

## Cau truc thu muc

```
├── solution.py              # ETL Pipeline script
├── processed_data.csv       # Output cua pipeline
├── experiment_report.md     # Bao cao thi nghiem
└── README.md                # File nay
```

---

## Ket qua

(Tom tat ket qua: bao nhieu records da xu ly, bao nhieu bi loai, v.v.)
