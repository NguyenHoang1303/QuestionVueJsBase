# QuestionVueJsBase



### VueJs là gì?
  - Là 1 framework để xây nên các giao diện người dùng.
### Lợi ích của Vuejs?
  - Vue nhẹ
  - Hiệu suất cao.
  - Dễ học.
  - Linh hoạt.

### Vue instance là gì?
  - là thể hiện của lớp Vue, thường được gọi là vm trong Vue là ViewModel của mẫu MVVM mà Vue tuân theo.
### Sự khác nhau g v-if và v-show là?
  - v-if : sẽ không hiển thị trong DOM nếu biểu thức có giá trị false. hỗ trọ v-else, v-else-if và có thể sử dụng bên trong <template>
  - v-show: sẽ chỉ bị ẩn đi trong DOM nếu false.
### Computed và method là gì?
  - Computed: biết các giá trị được sử dụng trong hàm có thay đổi không, để chúng không cần phải chạy mọi lúc để kiểm tra. Tức là nếu trong hàm có bất gì giá trị nào thay đổi thì cả cái hàm đó sẽ chạy để tính toán lại. Và đặc biệt là khi sử dụng các hàm trong computed thì sẽ không có dấu ngoặc như cách dùng hàm của methods.
  - Methods: không thể biết các giá trị trong hàm có thay đổi hay không nên hàm sẽ không chạy lại nếu các giá trị trong hàm đó thay đổi.
### Created và mounted là gì?
  - Created: được chạy khi data, event trước khi các phần tử DOM được render ra. Thường được gọi API và gắn kết các giá trị trong data.
  - Mounted: giai đoạn này chúng ta có thể truy cập vào data, template, DOM.
### Lifecycle của một component là gì và gồm những giai đoạn nào ?
- Những giai đoạn của lifecycle bao gồm:
   + Giai đoạn khởi tạo: beforeCreate(), created()
   + Giai đoạn gắn kết vào DOM: beforeMounte(), mounted()
   + Giai đoạn cập nhật DOM khi dữ liệu thay đổi: beforeUpdate(), updated()
   + Giai đoạn hủy instance hay kết thúc vòng đời của component: beforeDestroy(), destroyed()
### Các tính năng chính của Vue là gì?
  - Virtural DOM: là 1 đại diện cây trong bộ nhớ có dung lượng nhẹ của DOM HTML gốc và được cập nhật mà ko ảnh hưởng đến DOM gốc.
  - Component: Tạo các phần tử tùy chỉnh có thể tái sử dụng trong Vuejs
  - Template: Vuejs cung cấp các template dựa trên HTML liên kết DOM với dữ liệu.
  - Routing: điều hướng giữa các trang thông qua vue-router.
- Light-weight: là 1 thư viện nhẹ so với các framework kh
