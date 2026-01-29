# .NET Upgrade Notes

## .NET 10.0 LTS Upgrade (January 2026)

### Overview
The ZavaStorefront project has been upgraded from .NET 6.0 to .NET 10.0 LTS (Long-Term Support).

### Why .NET 10.0?
- **Current LTS Version**: .NET 10.0 was released in November 2025
- **Support Timeline**: Supported until November 2028 (3 years)
- **Previous Version**: .NET 6.0 reached end-of-support in November 2024

### Changes Made
1. Updated `src/ZavaStorefront.csproj`:
   - Changed `<TargetFramework>` from `net6.0` to `net10.0`

2. Updated `src/README.md`:
   - Updated technology stack references from .NET 6 to .NET 10 LTS

### Compatibility
- ✅ **Build**: No issues - project builds successfully
- ✅ **Runtime**: No issues - application runs as expected
- ✅ **Dependencies**: No package updates required
- ⚠️ **Warnings**: Pre-existing nullable reference warnings (not related to upgrade)

### Testing Performed
- [x] Build verification: `dotnet build` - SUCCESS
- [x] Runtime verification: `dotnet run` - SUCCESS
- [x] HTTP/HTTPS endpoint checks - SUCCESS (HTTP 200 responses)

### No Breaking Changes
This upgrade required no code changes due to:
- Simple project structure (ASP.NET Core MVC)
- No external dependencies in .csproj
- Modern C# features already in use (nullable enabled, implicit usings)

### Developer Requirements
To work with this project, you need:
- .NET 10.0 SDK or later
- Download from: https://dotnet.microsoft.com/download/dotnet/10.0

### CI/CD Impact
- No CI/CD workflows required updates (no .NET-specific workflows exist)
- If adding .NET workflows in the future, use `dotnet-version: '10.0.x'` in setup actions

### Future Upgrades
Next recommended upgrade: .NET 12.0 LTS (expected November 2027)

### References
- [.NET Support Policy](https://dotnet.microsoft.com/platform/support/policy/dotnet-core)
- [.NET 10.0 Release Notes](https://dotnet.microsoft.com/download/dotnet/10.0)
