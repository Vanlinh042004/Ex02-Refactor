# QUẢN LÝ DANH SÁCH SINH VIÊN

## Cấu trúc source code:

- Chia Project thành hai phần: Back-end và Front-end
  - Back-end
    ```
    Back-end/
    ├── .env
    ├── .gitignore
    ├── jest.config.js
    ├── nodemon.json
    ├── package.json
    ├── README-CLEAN-ARCHITECTURE.md
    ├── tsconfig.json
    └── src/
        ├── index.ts
        ├── application/
        │   ├── dtos/
        │   ├── exceptions/
        │   ├── repositories/
        │   ├── services/
        │   └── README.md
        ├── components/
        │   ├── class/
        │   │   ├── controllers/
        │   │   ├── models/
        │   │   ├── services/
        │   │   └── seeds/
        │   ├── course/
        │   │   ├── controllers/
        │   │   ├── models/
        │   │   ├── routes/
        │   │   ├── services/
        │   │   └── seeds/
        │   ├── email-domain/
        │   │   ├── controllers/
        │   │   ├── services/
        │   │   └── __test__/
        │   ├── faculty/
        │   │   ├── models/
        │   │   └── seeds/
        │   ├── phone-number/
        │   │   ├── models/
        │   │   └── seeds/
        │   ├── program/
        │   │   ├── models/
        │   │   └── seeds/
        │   ├── registration/
        │   │   ├── routes/
        │   │   └── services/
        │   ├── status/
        │   │   ├── models/
        │   │   └── seeds/
        │   └── student/
        │       ├── controllers/
        │       ├── models/
        │       ├── services/
        │       └── seeds/
        ├── config/
        │   └── database.ts
        ├── debug/
        │   └── checkFacultyData.ts
        ├── demo/
        │   └── facultyDemo.ts
        ├── domain/
        │   ├── entities/
        │   ├── repositories/
        │   ├── value-objects/
        │   └── index.ts
        ├── infrastructure/
        │   ├── adapters/
        │   ├── controllers/
        │   ├── database/
        │   │   └── mongo/
        │   ├── di/
        │   │   └── serviceRegistry.ts
        │   ├── logging/
        │   ├── mappers/
        │   ├── repositories/
        │   ├── webserver/
        │   ├── bootstrap.ts
        │   └── index.ts
        ├── middleware/
        │   └── requestLogger.ts
        ├── routes/
        │   └── index.ts
        ├── seeds/
        │   └── index.ts
        └── utils/
            ├── csvHandler.ts
            ├── jsonHandler.ts
            └── logger.ts
    ```
  - Front-end
    ```
    Front-end/
    ├── package.json
    ├── public/
    └── src/
        ├── App.css
        ├── App.js
        ├── App.test.js
        ├── index.css
        ├── index.js
        ├── logo.svg
        ├── reportWebVitals.js
        ├── setupTests.js
        ├── LayoutDefaut/
        │   ├── Layout.js
        │   ├── Footer/
        │   │   └── indexFooter.js
        │   └── Header/
        │       └── indexHeader.js
        ├── Pages/
        │   └── Home/
        │       ├── AddStudentModal.js
        │       ├── EditStudentModal.js
        │       └── indexHome.js
        ├── Routes/
        │   ├── indexRoutes.js
        │   └── Routes.js
        ├── Services/
        │   └── studentService.js
        ├── Style/
        │   ├── Header.scss
        │   ├── Home.scss
        │   └── style.css
        └── Utils/
            └── request.js
    ```

## Hướng dẫn cài đặt & chạy chương trình

#### Version 1.0

**_Back - end_**

1. Sử dụng file cấu hình .env để thiết lập các biến môi trường.

```properties
PORT=5000
MONGODB_URI=mongodb+srv://donalmun:eqia8yO1F0G3oBVx@tkpm.vufuh.mongodb.net/ex01?retryWrites=true&w=majority&appName=ex01
```

2. Cài đặt các package cần thiêt:

```bash
npm install
```

3. Chạy chương trình:

```bash
npm start
```

**_Front - end_**

1. Cài đặt các package cần thiêt:

```bash
npm install
```

2. Chạy chương trình:

```bash
npm start
```

---

#### Version 2.0

**_Back - end_**

1. Cài đặt các package cần thiêt:

```bash
npm install
```

2. Chạy chương trình:

```bash
npm run dev
```

**_Front - end_**

1. Cài đặt các package cần thiêt:

```bash
npm install
```

2. Chạy chương trình:

```bash
npm start
```

## Hình ảnh minh họa

**1. Cho phép đổi tên & thêm mới: khoa, tình trạng sinh viên, chương trình**

<img src="FeatureImg/Ex02/Feature1/AddFaculty.png" alt="AddFaculty" />
<img src="FeatureImg/Ex02/Feature1/AddProgram.png" alt="AddProgram" />
<img src="FeatureImg/Ex02/Feature1/AddStatus.png" alt="AddStatus" />
<img src="FeatureImg/Ex02/Feature1/RenameFaculty.png" alt="RenameFaculty" />
<img src="FeatureImg/Ex02/Feature1/RenameProgram.png" alt="RenameProgram" />
<img src="FeatureImg/Ex02/Feature1/RenameStatus.png" alt="RenameStatus" />

**2. Thêm chức năng tìm kiếm: tìm theo khoa, khoa + tên**

<img src="FeatureImg/Ex02/Feature2/SearchFaculty.png" alt="Search Faculty" width="500" height="300"/> 
<img src="FeatureImg/Ex02/Feature2/SearchName+Faculty.png" alt="Search Faculty" width="500" height="300"/>

**3. Hỗ trợ import/export dữ liệu: CSV, JSON, XML, Excel (chọn ít nhất 2)**

<img src="FeatureImg/Ex02/Feature3/Feature3.png" alt="Feature3" />
<img src="FeatureImg/Ex02/Feature3/Export.png" alt="Export" width="500" height="300"/>
<img src="FeatureImg/Ex02/Feature3/Export_csv.png" alt="Export_csv" width="500" height="300"/>
<img src="FeatureImg/Ex02/Feature3/Export_Json.png" alt="Export_Json" width="500" height="300"/>
<img src="FeatureImg/Ex02/Feature3/Import.png" alt="Import" width="500" height="300"/>

**4.Thêm logging mechanism để troubleshooting production issue & audit purposes**
<img src="FeatureImg/Ex02/Feature4/Feature4.png" alt="Feature4" />

---

#### Version 3.0

**_Back - end_**

1. Cài đặt các package cần thiêt:

```bash
npm install
```

2. Chạy chương trình:

```bash
npm run dev
```

**_Front - end_**

1. Cài đặt các package cần thiêt:

```bash
npm install
```

2. Chạy chương trình:

```bash
npm start
```

## Hình ảnh minh họa

**1. MSSV phải là duy nhất**
<img src="FeatureImg/Ex03/Rule01/image1.png"  />
<img src="FeatureImg/Ex03/Rule01/image2.png"  />

**2. Email phải thuộc một tên miền nhất định và có thể cấu hình động (configurable)**
<img src="FeatureImg/Ex03/Rule02/image1.png"  />
<img src="FeatureImg/Ex03/Rule02/image2.png"  />
<img src="FeatureImg/Ex03/Rule02/image3.png"  />

**3. Số điện thoại phải có định dạng hợp lệ theo quốc gia (configurable)**
<img src="FeatureImg/Ex03/Rule03/image1.png"  />
<img src="FeatureImg/Ex03/Rule03/image2.png"  />
<img src="FeatureImg/Ex03/Rule03/image3.png"  />

**4.Tình trạng sinh viên chỉ có thể thay đổi theo một số quy tắc (configurable)**
<img src="FeatureImg/Ex03/Rule04/image1.png"  />
<img src="FeatureImg/Ex03/Rule04/image2.png"  />
<img src="FeatureImg/Ex03/Rule04/image3.png"  />

---

# Version 5.0

## Hướng dẫn cài đặt & chạy chương trình

**_Back - end_**

1. Sử dụng file cấu hình .env để thiết lập các biến môi trường.

```properties
PORT=5000
MONGODB_URI=mongodb+srv://donalmun:eqia8yO1F0G3oBVx@tkpm.vufuh.mongodb.net/ex01?retryWrites=true&w=majority&appName=ex01
```

2. Cài đặt các package cần thiêt:

```bash
npm install
```

3. Chạy chương trình:

```bash
npm start
```

**_Front - end_**

1. Cài đặt các package cần thiêt:

```bash
npm install
```

2. Chạy chương trình:

```bash
npm start
```

## Hình ảnh minh họa

### QUẢN LÝ KHÓA HỌC & BẢNG ĐIỂM SINH VIÊN

#### **2.1 Quản Lý Khóa Học**

##### **User Story 1: Thêm khóa học mới**

<img src="FeatureImg/Ex05/ManageCourse/UserStory1/image1.png"  />
<img src="FeatureImg/Ex05/ManageCourse/UserStory1/image2.png"  />
<img src="FeatureImg/Ex05/ManageCourse/UserStory1/image3.png"  />

##### **User Story 2: Xóa khóa học**

<img src="FeatureImg/Ex05/ManageCourse/UserStory2/image1.png"  />
<img src="FeatureImg/Ex05/ManageCourse/UserStory2/image3.png"  />
<img src="FeatureImg/Ex05/ManageCourse/UserStory2/image2.png"  />
<img src="FeatureImg/Ex05/ManageCourse/UserStory2/image4.png"  />

##### **User Story 3: Cập nhật thông tin khóa học**

<img src="FeatureImg/Ex05/ManageCourse/UserStory3/image1.png"  />
<img src="FeatureImg/Ex05/ManageCourse/UserStory3/image2.png"  />
<img src="FeatureImg/Ex05/ManageCourse/UserStory3/image3.png"  />

##### **User Story 4: Mở lớp học cho một khóa học cụ thể**

<img src="FeatureImg/Ex05/ManageCourse/UserStory4/image1.png"  />
<img src="FeatureImg/Ex05/ManageCourse/UserStory4/image2.png"  />
<img src="FeatureImg/Ex05/ManageCourse/UserStory4/image3.png"  />

#### **2.2 Đăng Ký Khóa Học Cho Sinh Viên (Thủ Công Bởi Giáo Vụ)**

##### **User Story 5: Đăng ký khóa học cho sinh viên**

<img src="FeatureImg/Ex05/ManageCourse/UserStory5/1.PNG"  />
<img src="FeatureImg/Ex05/ManageCourse/UserStory5/2.PNG"  />
<img src="FeatureImg/Ex05/ManageCourse/UserStory5/3.PNG"  />

##### **User Story 6: Hủy đăng ký khóa học của sinh viên**

<img src="FeatureImg/Ex05/ManageCourse/UserStory6/1.PNG"  />
<img src="FeatureImg/Ex05/ManageCourse/UserStory6/2.PNG"  />
<img src="FeatureImg/Ex05/ManageCourse/UserStory6/3.PNG"  />

##### **User Story 7: In bảng điểm chính thức**

<img src="FeatureImg/Ex05/ManageCourse/UserStory7/1.PNG"  />
<img src="FeatureImg/Ex05/ManageCourse/UserStory7/2.PNG"  />
<img src="FeatureImg/Ex05/ManageCourse/UserStory7/4.PNG"  />

### **Unit Test**

<img src="FeatureImg/Ex05/ManageCourse/unittest.png"  />

---

# Version 6.0

## Hướng dẫn cài đặt & chạy chương trình

**_Back - end_**

1. Sử dụng file cấu hình .env để thiết lập các biến môi trường.

```properties
PORT=5000
MONGODB_URI=mongodb+srv://donalmun:eqia8yO1F0G3oBVx@tkpm.vufuh.mongodb.net/ex01?retryWrites=true&w=majority&appName=ex01
```

2. Cài đặt các package cần thiêt:

```bash
npm install
```

3. Chạy chương trình:

```bash
npm start
```

**_Front - end_**

1. Cài đặt các package cần thiêt:

```bash
npm install
```

2. Chạy chương trình:

```bash
npm start
```

## Hình ảnh minh họa

### **Unit Test**

<img src="FeatureImg/Ex06/image1.png"  />
<img src="FeatureImg/Ex06/image2.png"  />
<img src="FeatureImg/Ex06/image3.png"  />
