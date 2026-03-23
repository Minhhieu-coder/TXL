# Tien Xu Ly Du Lieu -- Brazilian E-Commerce (Olist)

Do an mon Tien Xu Ly Du Lieu: Phan tich kham pha va xay dung mo hinh phan loai tren bo du lieu thuong mai dien tu Brazil (Olist).

---

## Gioi thieu

Du an su dung bo du lieu **Brazilian E-Commerce Public Dataset by Olist** (Kaggle) gom hon 99,000 don hang trong giai doan 2016-2018. Noi dung chinh bao gom:

- Phan tich kham pha du lieu (EDA): kiem tra gia tri thieu, phan phoi bien, xu huong theo thoi gian
- Tien xu ly du lieu: chuyen doi datetime, trich xuat dac trung thoi gian, xu ly null bang median, chuan hoa bang StandardScaler
- Tao bien muc tieu nhi phan (`don_giao_tc`): 1 = da giao thanh cong, 0 = chua giao
- Xay dung va so sanh 4 mo hinh hoc may: Naive Bayes, KNN, Decision Tree, SVM (RBF kernel)
- Danh gia mo hinh bang Accuracy, F1-Score (Weighted va Macro), Confusion Matrix, Radar Chart

### Du lieu su dung

| File | Mo ta |
|------|-------|
| `olist_orders_dataset.csv` | Thong tin don hang (trang thai, cac moc thoi gian) |
| `olist_order_items_dataset.csv` | Chi tiet san pham trong tung don hang (gia, phi van chuyen) |

### Cau truc notebook

Notebook `tien_xu_ly_du_lieu.ipynb` gom 16 phan:

1. Import thu vien va cau hinh
2. Load va chuan bi du lieu
3. Kham pha bang don hang chinh
4. Phan tich bien phan loai chinh
5. Xu ly va chuyen doi du lieu
6. Phan tich xu huong theo thoi gian
7. Phan tich phan phoi bien lien tuc
8. Tao bien muc tieu (binary)
9. Ket hop du lieu -- Master Dataset
10. Encoding va Scaling
11. Mo hinh Naive Bayes
12. Mo hinh KNN
13. Mo hinh Decision Tree
14. Mo hinh SVM
15. So sanh ket qua cac mo hinh
16. Ket luan va Insights

---

## Thu vien can cai

Du an su dung Python 3. Cac thu vien can thiet:

| Thu vien | Muc dich |
|----------|----------|
| `numpy` | Tinh toan so hoc |
| `pandas` | Xu ly va phan tich du lieu |
| `matplotlib` | Truc quan hoa co ban |
| `seaborn` | Truc quan hoa nang cao |
| `scikit-learn` | Tien xu ly, mo hinh hoc may, danh gia |

Cai dat tat ca bang lenh:

```bash
pip install numpy pandas matplotlib seaborn scikit-learn
```

---

## Cach chay code

### Buoc 1: Clone repository

```bash
git clone https://github.com/<username>/TXL.git
cd TXL
```

### Buoc 2: Cai thu vien

```bash
pip install numpy pandas matplotlib seaborn scikit-learn
```

### Buoc 3: Mo va chay notebook

Mo file `tien_xu_ly_du_lieu.ipynb` bang mot trong cac cach sau:

- **VS Code**: Mo file `.ipynb` truc tiep, chon kernel Python, chay toan bo cell (Run All)
- **Jupyter Notebook**:
  ```bash
  jupyter notebook tien_xu_ly_du_lieu.ipynb
  ```
- **Jupyter Lab**:
  ```bash
  jupyter lab tien_xu_ly_du_lieu.ipynb
  ```

Chay tuan tu cac cell tu tren xuong duoi. Khong can thay doi duong dan vi cac file CSV nam cung thu muc voi notebook.

### Luu y

- Dam bao tat ca file CSV nam cung thu muc voi notebook
- Kernel Python phai la phien ban 3.x
- Mot so cell (SVM) co the mat vai phut do tinh toan tren tap du lieu lon

---

## Ket qua chinh

| Mo hinh | Accuracy | F1 Weighted | F1 Macro |
|---------|----------|-------------|----------|
| Naive Bayes | 0.9695 | 0.9649 | 0.6576 |
| KNN (K=1) | 0.9722 | 0.9731 | 0.7741 |
| Decision Tree | 0.9993 | 0.9993 | 0.9944 |
| SVM (RBF) | 0.8093 | 0.8715 | 0.5599 |

Mo hinh Decision Tree dat hieu suat tot nhat tren ca 3 chi so danh gia.