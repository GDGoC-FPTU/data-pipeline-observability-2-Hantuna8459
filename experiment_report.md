# Experiment Report: Data Quality Impact on AI Agent

**Student ID:** 2A202600847
**Name:** Trịnh Vũ Anh Tuấn
**Date:** 10/6/2026

---

## 1. Ket qua thi nghiem

Chay `agent_simulation.py` voi 2 bo du lieu va ghi lai ket qua:

| Scenario | Agent Response | Accuracy (1-10) | Notes |
|----------|----------------|-----------------|-------|
| Clean Data (`processed_data.csv`) | Based on my data, the best choice is Laptop at $1200 | | |
| Garbage Data (`garbage_data.csv`) | Based on my data, the best choice is Nuclear Reactor at $999999 | | |

---

## 2. Phan tich & nhan xet

### Tai sao Agent tra loi sai khi dung Garbage Data?

(Viet nhan xet cua ban o day — it nhat 50 tu)

(Hay phan tich cac van de nhu Duplicate IDs, wrong data types, outliers, null values
va giai thich tai sao chung anh huong den ket qua cua Agent.)

Agent tra loi sai khi dung Garbage Data vi du lieu dau vao chua nhieu loi lam sai lech qua trinh xu ly va phan tich. Duplicate IDs co the lam mot san pham bi dem nhieu lan, gay sai tong so record hoac thong ke doanh thu. Wrong data types, vi du price la chuoi thay vi so, co the lam pipeline khong tinh toan duoc discounted_price hoac tao ket qua sai. Outliers nhu gia qua lon hoac qua nho lam anh huong den gia tri trung binh va nhan xet cua Agent. Null values o category, price hoac product name lam thieu thong tin quan trong, khien Agent khong the phan loai hoac danh gia chinh xac. Vi vay, khi du lieu rac khong duoc validate va lam sach tot, Agent se dua ra cau tra loi kem tin cay.

---

## 3. Ket luan

**Quality Data > Quality Prompt?** (Dong y hay khong? Giai thich ngan gon.)

(Viet ket luan cua ban o day)

Dong y. Prompt tot co the huong dan agent xu ly dung quy trinh, nhung neu du lieu dau vao bi loi qua nhieu thi ket qua van se kem chat luong. Trong thi nghiem, clean data giup pipeline chay on dinh, so record bi loai bo it va ket qua dau ra dang tin cay hon. Nguoc lai, garbage data lam tang so loi validation, nhieu record bi loai bo va agent mat nhieu cong hon de xu ly.

Vi vay, chat luong du lieu dau vao la yeu to rat quan trong. Prompt tot la can thiet, nhung khong the hoan toan bu dap cho du lieu kem chat luong.
