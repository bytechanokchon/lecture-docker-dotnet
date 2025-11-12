
# STAGE 1
# ใช้สำหรับแปรงชุดคำสั่ง C# เป็น Binary
FROM mcr.microsoft.com/dotnet/sdk:9.0 AS build
WORKDIR /src
COPY . .
RUN dotnet publish "hello-docker.csproj" -o /published /p:UseAppHost=false

# STAGE 2
FROM mcr.microsoft.com/dotnet/aspnet:9.0
WORKDIR /app
COPY --from=build /published .
ENTRYPOINT [ "dotnet", "hello-docker.dll" ]