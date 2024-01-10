# webbase
**Application**: Chứa các Use Cases và Services để thực hiện logic ứng dụng cụ thể.
  

**Domain**: Chứa các Entities định nghĩa cốt lõi của ứng dụng, Repositories để truy cập dữ liệu, và Services chứa các phương thức nghiệp vụ.

**Infrastructure**: Chứa các thành phần liên quan đến việc triển khai cụ thể, bao gồm các đối tượng truy cập dữ liệu, các dịch vụ giao tiếp với bên ngoài như Payment Gateways, Email Services và các dịch vụ khác.

**Presentation**: Chứa các thành phần giao diện người dùng, ví dụ như các Controllers trong MVC (Model-View-Controller) framework, Views, và các thành phần khác liên quan đến giao diện người dùng.

Cấu trúc này giúp phân tách rõ ràng các phần của ứng dụng, giúp việc bảo trì, mở rộng và kiểm thử trở nên dễ dàng hơn bằng cách giảm sự phụ thuộc giữa các thành phần khác nhau.

- Application/
  - UseCases/
    - CreateUserUseCase.cs
    - UpdateUserUseCase.cs
    - DeleteUserUseCase.cs
    - ...
  - Services/
    - UserService.cs
    - AuthenticationService.cs
    - ...
- Domain/
  - Entities/
    - User.cs
    - Product.cs
    - ...
  - Repositories/
    - UserRepository.cs
    - ProductRepository.cs
    - ...
  - Services/
    - IUserService.cs
    - IProductService.cs
    - ...
- Infrastructure/
  - Persistence/
    - UserRepository.cs (Implementations của Repository Interface)
    - ProductRepository.cs (Implementations của Repository Interface)
    - DbContext.cs (Database context nếu sử dụng ORM)
  - ExternalServices/
    - PaymentGateway.cs
    - EmailService.cs
    - ...
- Presentation/
  - Controllers/
    - UserController.cs
    - ProductController.cs
    - ...
  - Views/
    - ...
