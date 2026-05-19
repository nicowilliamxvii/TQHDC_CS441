# 🏠 House Price Prediction — Phan Tich Du Lieu

> **Observation chinh:** *"Gia nha duoc quyet dinh boi yeu to nao — dien tich vat ly, vi tri dia ly, hay tinh trang ngoi nha?"*



## 📊 Tong Quan Dataset

| Chi so | Gia tri |
|--------|---------|
| Tong quan sat | **2.000 can nha** |
| Gia trung binh | **$537.677** |
| Khoang gia | **$50K – $1M** |
| So bien so phan tich | **10 features** |
| Ngay bao cao | 19/05/2026 |

---

## 📋 Muc Luc

- [Q1 — Phan phoi gia nha](#q1--phan-phoi-gia-nha)
- [Q2 — Dien tich vs Gia](#q2--dien-tich-co-thuc-su-quyet-dinh-gia-khong)
- [Q3 — Anh huong cua vi tri](#q3--vi-tri-nao-co-gia-cao-nhat)
- [Q4 — Tinh trang nha](#q4--tinh-trang-nha-co-phan-anh-dung-gia-tri-khong)
- [Ket Luan](#ket-luan)
- [Huong Mo Rong](#huong-mo-rong--de-xuat)

---

## Q1 — Phan Phoi Gia Nha

> *Truoc khi di sau vao cac nhan to anh huong, can hieu toan canh phan phoi gia.*

Bieu do histogram the hien so luong can nha theo tung khoang gia $100K tren 2.000 quan sat.

### Thong ke mo ta

```
Gia trung binh  :  $537.677
Trung vi         :  $539.254
Do lech chuan   :  $276.429   ← rat rong, thi truong bien dong cao
Min / Max        :  $50.005  /  $999.656
```

> [!NOTE]
> **Insight Q1:** Gia nha phan bo tuong doi deu tu $50K den $1M, moi khoang gia co khoang 185–235 can. Khong co phan khuc nao chiem uu the ro rang — day la mot **thi truong da dang**, doi hoi phan tich sau hon.

---

## Q2 — Dien Tich Co Thuc Su Quyet Dinh Gia Khong?

> *Day la cau hoi truc giac nhat — va cung la phat hien bat ngo nhat.*

Gia su thong thuong: nha cang lon thi cang dat. Du lieu noi gi?

### He so tuong quan Pearson voi gia nha

| Bien so | He so tuong quan (r) | Nhan xet |
|---------|----------------------|----------|
| So tang (Floors) | `r = +0.056` | Tuong quan duong, rat yeu |
| Nam xay (YearBuilt) | `r = +0.005` | Gan nhu khong tuong quan |
| Dien tich (Area) | `r = +0.002` | **Gan nhu khong tuong quan** |
| Phong ngu (Bedrooms) | `r = -0.003` | Tuong quan am, khong dang ke |
| Phong tam (Bathrooms) | `r = -0.016` | Tuong quan am, khong dang ke |

> [!IMPORTANT]
> **Insight Q2 — PHAT HIEN TRUNG TAM:**
> He so tuong quan giua **Dien tich** va **Gia** chi la `r = 0.002`, gan bang 0.
> Cac bien so vat ly khac cung deu duoi `0.06`.
>
> ➜ **CAC DAC TRUNG VAT LY KHONG GIAI THICH DUOC GIA NHA** trong dataset nay.
>
> Mot can nha 500 ft² co the co gia tuong duong mot can 5.000 ft². Day la ly do chinh de su dung mo hinh **machine learning phi tuyen tinh** thay vi hoi quy don gian.

---

## Q3 — Vi Tri Nao Co Gia Cao Nhat?

> *Nguyen tac vang cua bat dong san: "location, location, location".*

### Gia trung binh theo 4 vung dia ly

| Vung | Dac diem | Nha o dien hinh | Vi du Viet Nam | Gia TB |
|------|----------|-----------------|----------------|--------|
| **Suburban** (Ngoai o) | Yen tinh, thap tang, nhieu cay xanh | Nha don lap co san vuon | Thu Duc, Binh Chanh (HCM) / Ha Dong (HN) | **$557K** ★ |
| **Rural** (Vung que) | Mat do thap, dat rong, thien nhien | Nha rong, trang trai | Cu Chi, Can Gio / Cac huyen xa | **$539K** |
| **Downtown** (Trung tam loi) | Cao oc, mat do cao, di bo duoc | Chung cu cao, penthouse | Quan 1 (HCM) / Hoan Kiem (HN) | **$536K** |
| **Urban** (Noi thanh) | Khu dan cu dong, tien ich da dang | Nha pho, townhouse, duplex | Quan 3, Binh Thanh / Dong Da (HN) | **$519K** |

```
Mo hinh vung do thi tu trung tam ra ngoai:

        ┌─────────────────────────────┐
        │           Rural             │
        │   ┌─────────────────────┐   │
        │   │      Suburban       │   │
        │   │   ┌─────────────┐   │   │
        │   │   │    Urban    │   │   │
        │   │   │  ┌───────┐  │   │   │
        │   │   │  │ Down  │  │   │   │
        │   │   │  │ town  │  │   │   │
        │   │   │  └───────┘  │   │   │
        │   │   └─────────────┘   │   │
        │   └─────────────────────┘   │
        └─────────────────────────────┘
```

> [!NOTE]
> **Insight Q3:** Suburban dan dau voi $557K, Urban thap nhat $519K — chenh lech chi **$38.000 (~7%)**.
> Khi xet phan phoi (boxplot), do bien dong **ben trong** moi vung con lon hon nhieu so voi chenh lech **giua** cac vung.
>
> ➜ Vi tri **co anh huong**, nhung **KHONG PHAI YEU TO QUYET DINH**.

---

## Q4 — Tinh Trang Nha Co Phan Anh Dung Gia Tri Khong?

> *Lieu nha "Excellent" co thuc su dat hon "Fair"?*

### Gia trung binh theo tinh trang nha

| Tinh trang | Gia TB | So luong | Nhan xet |
|------------|--------|----------|----------|
| **Fair** (Trung binh) | **$561K** | 521 can | 🔴 CAO NHAT — bat ngo! |
| Excellent (Tuyet voi) | $531K | 511 can | Thap hon Fair $30K |
| Good (Tot) | $529K | 461 can | Gap nau tuong duong Excellent |
| Poor (Kem) | $529K | 507 can | Gap nau tuong duong Good |

> [!WARNING]
> **Insight Q4:** Nha **"Fair"** (tinh trang trung binh) lai co gia cao nhat **$561K** — dat hon "Excellent" **$30K**.
> Garage co tac dong rat nho.
>
> Day la nghich ly — nhieu kha nang do yeu to **vi tri vi mo (micro-location)** hoac quy mo nha bi che khuat ben trong nhom "Fair" gay ra hien tuong nay.

---

## Ket Luan

> [!CAUTION]
> **TRA LOI OBSERVATION:**
> Khong co yeu to don le nao — dien tich, vi tri hay tinh trang — giai thich duoc gia nha mot cach ro rang trong dataset nay.
> Gia nha mang **tinh phuc tap cao**, doi hoi mo hinh phi tuyen tinh va ket hop nhieu bien tuong tac.

### Tom tat 4 cau hoi

| | Cau hoi | Ket qua chinh | Y nghia |
|--|---------|---------------|---------|
| **Q1** | Phan phoi gia | Dong deu $50K–$1M | Thi truong da dang, khong co xu huong ro |
| **Q2** | Dien tich vs Gia | `r = 0.002` (gan bang 0) | Thach thuc lon cho mo hinh tuyen tinh |
| **Q3** | Gia theo vi tri | Chenh lech chi 7% | Vi tri anh huong han che |
| **Q4** | Tinh trang nha | "Fair" dat hon "Excellent" | Du lieu co tinh phuc tap / nhieu ngo ngang |

---

## Huong Mo Rong & De Xuat

### Mo hinh de xuat

```python
# Thay vi Linear Regression don thuan:
from sklearn.ensemble import RandomForestRegressor, GradientBoostingRegressor
from xgboost import XGBRegressor

# Cac mo hinh phu hop cho du lieu phi tuyen:
models = [
    RandomForestRegressor(n_estimators=200),
    GradientBoostingRegressor(learning_rate=0.05),
    XGBRegressor(n_estimators=300, max_depth=6),
]
```

### Feature engineering goi y

- Tao bien tuong tac: `Location × Condition`, `Area × Floors`
- Phan tich vi tri cu the hon (ten quan/huyen thay vi 4 vung chung)
- Them bien: khoang cach den trung tam, diem truong, chat luong duong, mat tien

### Ly giai r ≈ 0 tren tat ca bien so

> Co kha nang dataset nay duoc tao bang **synthetic data** (qua trinh ngau nhien hoa), giai thich tai sao khong co bien so vat ly nao co tuong quan co y nghia voi gia. Day cung la dac trung thuong gap cua cac dataset luyen tap tren Kaggle.

---

## Dataset Info

```
Source  : House Price Prediction Dataset
Records : 2,000 observations
Features: 10 variables (Area, Bedrooms, Bathrooms, Floors,
          YearBuilt, Location, Condition, Garage, Price...)
Report  : 19/05/2026
Purpose : Academic / Learning
```

---

*Bao cao nay duoc xay dung phuc vu muc dich hoc thuat va trinh bay.*
