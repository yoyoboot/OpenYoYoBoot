# OpenYoYoBoot

欢迎来到 OpenYoYoBoot 仓库！🎉

OpenYoYoBoot 是一个增强版的 ASP.NET Boilerplate 框架，它在原版基础上引入了灵活的主键类型，帮助开发者更高效地构建基于 ASP.NET 的应用程序。

![OpenYoYoBoot Logo](https://path-to-logo-image)

## 特性 ✨

- **灵活的主键类型**：支持多种类型的主键，满足不同应用场景的需求。
- **开箱即用的功能**：包括身份验证、授权、日志记录、多租户等。
- **模块化设计**：通过模块化架构，简化开发和维护。
- **高扩展性**：提供丰富的扩展点，方便定制和扩展功能。
- **活跃的社区支持**：拥有活跃的开发者社区，提供及时的技术支持和帮助。

## 快速开始 🚀

1. **克隆仓库**：
    ```bash
    git clone https://github.com/yoyoboot/OpenYoYoBoot.git
    cd OpenYoYoBoot
    ```

2. **安装依赖**：
    ```bash
    dotnet restore
    ```

3. **运行项目**：
    ```bash
    dotnet run
    ```

4. **访问应用**：
    打开浏览器并访问 [http://localhost:5000](http://localhost:5000) 以查看运行中的应用。

## 示例代码 📦

```csharp
public class MyAppService : ApplicationService
{
    private readonly IRepository<MyEntity, Guid> _myRepository;

    public MyAppService(IRepository<MyEntity, Guid> myRepository)
    {
        _myRepository = myRepository;
    }

    public async Task<MyDto> GetMyEntityAsync(Guid id)
    {
        var entity = await _myRepository.GetAsync(id);
        return ObjectMapper.Map<MyEntity, MyDto>(entity);
    }
}

# OpenYoYoBoot