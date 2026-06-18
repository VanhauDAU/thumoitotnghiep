# Thu moi tot nghiep

Website thu moi tot nghiep mobile-first, gom:

- Trang ngoai cho nguoi duoc moi: `/`
- Trang quan tri cau hinh noi dung va anh: `/admin`
- Backend Node/Express luu cau hinh vao JSON va serve anh upload tu `/uploads`
- Dong ho dem nguoc theo ngay/gio to chuc
- Nhieu anh cua nguoi tot nghiep, hien thi bang carousel ngang co auto-slide va ho tro vuot tren mobile
- Anh chinh co the upload nhieu anh de hien thi trong khung hero collage
- Section loi nhan gui rieng co the cau hinh tu admin
- Cau hinh luu y va ky niem dang nho nhu danh hieu, hoat dong, ngoai khoa

## Chay local

```bash
npm install
npm run build
npm start
```

Mo `http://localhost:4000`.

Khi phat trien giao dien:

```bash
npm run dev
```

Frontend chay o `http://localhost:5173`, backend chay o `http://localhost:4000`.

## Deploy Render

Repo da co `render.yaml`. Render se:

- build bang `npm install && npm run build`
- start bang `npm start`
- mount disk vao `/var/data`
- dat `UPLOAD_DIR=/var/data/uploads`
- dat `DATA_DIR=/var/data`

Cach nay giup anh upload khong mat khi service restart. Neu khong dung Render Disk, file upload tren Render co the bi mat khi deploy/restart.

Nen them bien moi truong:

```bash
ADMIN_TOKEN=mot-chuoi-bi-mat
```

Sau do vao `/admin`, nhap token nay vao o `Admin token` de upload anh va luu cau hinh.

## Cau hinh trong admin

Trong `/admin` co the sua:

- Ten nguoi tot nghiep, nganh hoc, truong
- Thoi gian, dia diem, link Google Maps
- Anh chinh va thu vien anh
- Loi moi, loi nhan, mo ta them
- Loi nhan gui rieng
- Luu y cho khach moi
- Ky niem dang nho gom tieu de va mo ta

Trang ngoai khong hien nut/icon quan tri. Muon vao admin thi truy cap truc tiep URL `/admin`.

## Ghi chu Figma

Phien nay chua lay duoc frame tu Figma qua plugin UIPro, nen giao dien da duoc dung mobile-first theo yeu cau san pham. Neu muon map sat 100% voi thiet ke, hay mo Figma plugin UIPro, generate code/screenshot cho frame mobile, roi chay lai yeu cau import.
