### 1. Vuejs là gì?
  - Là 1 framework để xây nên các giao diện người dùng.
### Lợi ích của Vuejs?
  - Vue nhẹ
  - Hiệu suất cao.
  - Dễ học.
  - Linh hoạt.
### 2. Vue instance là gì?
  - là thể hiện của lớp Vue, thường được gọi là vm trong Vue là ViewModel của mẫu MVVM mà Vue tuân theo.
### 3. Lifecycle của một component là gì và gồm những giai đoạn nào ?
- Những giai đoạn của lifecycle bao gồm:
   + Giai đoạn khởi tạo: 
     + beforeCreate(): chạy ngay trước quá trình mà một component được khởi tạo. Trong quá trình này các data mà chúng ta khai báo chưa reactive (tự thay đổi khi có cập nhật) đồng thời các events cũng chưa được khởi tạo.
     
     + created(): được chạy khi data, event trước khi các phần tử DOM được render ra. Thường được gọi API và gắn kết các giá trị trong data.
   + Giai đoạn gắn kết vào DOM: 
     + beforeMounte(): ược gọi sau khi component đã được compile và trước lần render đầu tiên.
     
     + mounted():Ở quá trình này chúng ta đã có đầy đủ quyền truy cập vào data, template, DOM (bằng cách gọi this.$el)
   + Giai đoạn cập nhật DOM khi dữ liệu thay đổi:
     + beforeUpdate():Quá trình này được gọi ngay sau khi dữ liệu trên component bị thay đổi và trước khi component re-render.
    
     + updated(): Quá trình này xảy ra sau beforeUpdate, ở đây DOM đã được cập nhật lại.
   + Giai đoạn hủy instance hay kết thúc vòng đời của component:
     + beforeDestroy():Quá trình này xay ra ngay trước khi component của chúng ta bị huỷ đi (ví dụ như lúc chúng ta chuyển từ component này sang component khác, hay như lúc ta chuyển route,...). Tại đây component vẫn còn đầy đủ những yếu tố như data, events,... Ta thường dùng hàm này để xoá đi các sự kiện không cần thiết sau khi component bị huỷ.
    
     + destroyed(): Tại quá trình này thì hầu như mọi thứ trên component đã bị huỷ đi: các directives bị huỷ, các event lắng nghe bị bỏ đi, các component con cũng đã bị destroy, watchers cũng đã bị huỷ,... nhưng ở ta vẫn có thể làm một số việc như thông báo với remote server là component vừa bị huỷ chẳng hạn.
### 4. Các tính năng chính của Vue là gì?
  - Virtural DOM: là 1 đại diện cây trong bộ nhớ có dung lượng nhẹ của DOM HTML gốc và được cập nhật mà ko ảnh hưởng đến DOM gốc.
  - Component: Tạo các phần tử tùy chỉnh có thể tái sử dụng trong Vuejs
  - Template: Vuejs cung cấp các template dựa trên HTML liên kết DOM với dữ liệu.
  - Routing: điều hướng giữa các trang thông qua vue-router.
- Light-weight: là 1 thư viện nhẹ so với các framework khác
### 5.  Các lệnh điều kiện có sẵn trong Vuejs là gì?
- Những lệnh điều kiện có sẵn trọng Vuejs bao gồm những lệnh như sau: v-else, v-if,  v-show và v-else-if.
### 6. Sự khác nhau g v-if và v-show là?
  - v-if : sẽ không hiển thị trong DOM nếu biểu thức có giá trị false. hỗ trọ v-else, v-else-if và có thể sử dụng bên trong <template>
  - v-show: sẽ chỉ bị ẩn đi trong DOM nếu false
### 7. Vue Router là gì?
- Vue Router là bộ định tuyến chính thức của Vue.js để tạo các trang với các tuyến đường khác nhau. Nó hỗ trợ định tuyến lồng nhau, ánh xạ chế độ xem và có thể cấu hình cao; thông số tuyến đường, truy vấn, ký tự đại diện.
### 8. Dynamic route matching là gì?
- Dynamic route matching giúp ta map các route tới component với các pattern khác nhau. Ví dụ:
    ```
    // Sử dụng từ khóa in, loop trong dãy từ 1->10
    const Aritcle = {
    template: '<div>Aritcle {{ $route.params.subjectId }}, PostId: {{ route.params.postid }}</div>'
    }
    
    const router = new VueRouter({
    routes: [
    // dynamic segments start with a colon
    { path: '/subject/:subjectId/post/:postid', component: Aritcle }
    ]
    })
    ```
- Khi sử dụng, các URL mapping với router param sẽ cho các kết quả như sau:
    + `/subject/vuejs/post/123` hoặc `/subject/react/post/234`
### 9. Mục đích của keep alive tag?
- Keep-alive tag sử dụng để giữ trạng thái hiện có của component và tránh việc render lại component quá nhiều lần. Các đối tượng được đóng ở trong tag keep-alive sẽ được giữ instances.
### 10. Đạo cụ là gì?
- Đạo cụ là các thuộc tính tùy chỉnh mà bạn có thể đăng ký vào một thành phần. Khi được truyền từ một thành phần khác hoặc thể hiện Vue gốc, phần hỗ trợ sẽ trở thành một thuộc tính của thành phần mà bạn đã truyền nó cho. Bạn có thể chỉ định nhiều đạo cụ và xác định loại của chúng.Ví dụ:
    ```
    Vue.component('myComponent', {
      props: ['name'],
      // OR
      // props: { name: String },
      template: '<div>Hello {{ name }}</div>'
    })
    <my-component name="Giuseppe Campanelli"></my-component>
    ```
