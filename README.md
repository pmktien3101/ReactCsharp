# ReactCsharp
## React: 
+ tạo dự án vs cú pháp => npx create-react-app@latest app-name 
+ cài axios để gọi API => npm i axios
+ tạo thư mục api để cấu hình đơn giản
+ tạo env để chứa URL dùng chung => sau này có deploy lên thì chỉ cần chỉnh sửa đường dẫn này
  <img width="430" alt="image" src="https://github.com/user-attachments/assets/8e5dae98-83fd-4930-86ee-7f5b576982f6">
###### Khi nào nên sử dụng Axios trong React?
Khi bạn cần giao tiếp với API từ ứng dụng React để lấy dữ liệu hoặc gửi dữ liệu đến server.
Khi bạn cần tùy chỉnh yêu cầu HTTP (thêm headers, cài đặt timeout, v.v.).
Khi bạn cần xử lý lỗi một cách hiệu quả và linh hoạt trong ứng dụng.
Khi bạn muốn tối ưu hóa xử lý dữ liệu với Promises hoặc async/await.
## .NET:
+ cấu hình lại bên .net để tránh lỗi No 'Access-Control-Allow-Origin' header is present on the requested resource. =>
  // show useCors with corsPolicyBuilder
app.UseCors(builder =>
{
    builder
    .AllowAnyHeader()
    .AllowAnyOrigin()
    .AllowAnyMethod();
});
##### tại folder data để kết nối vs database, tạo trên .net ko tạo bảng bằng vật lý 
+ install 6 cái entity framework core
+ config để tạo bảng
+ tạo bảng rồi thì phải kết nối vs csdl
##### migrate database để tạo cấu trúc cho table
+ add-migration init-todos
+ update-Database để có thể tạo bảng trong csdl
##### tạo dữ liệu mẫu cho table
+ tạo folder tên seeders
+ tạo databseSeeder để static 
+ xóa folder migration để chạy lại 
+ bỏ modelBuilder.Seed() trong Data file
+  add-migration init-todos
+ update-Database để có thể tạo bảng trong csdl
##### hiện dữ liệu ra trong phần controller
+ tạo folder service
+ cấu hình lại trong program.cs
  builder.Services.AddTransient<ITodosService, TodoService>();
