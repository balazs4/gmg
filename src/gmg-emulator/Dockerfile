FROM mcr.microsoft.com/dotnet/core/sdk:2.1

COPY . /app
WORKDIR /app
RUN dotnet restore && dotnet build
CMD dotnet run
