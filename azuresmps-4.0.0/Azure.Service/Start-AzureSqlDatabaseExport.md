---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 3005E411-9466-4602-8E07-F4EF8804AB2A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 22bff485bf49e0ec5f482e1325af661862583605
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945752"
---
# <span data-ttu-id="befab-101">Start-AzureSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="befab-101">Start-AzureSqlDatabaseExport</span></span>

## <span data-ttu-id="befab-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="befab-102">SYNOPSIS</span></span>
<span data-ttu-id="befab-103">Inicia uma operação de exportação de um banco de dados SQL do Azure para o armazenamento de BLOB.</span><span class="sxs-lookup"><span data-stu-id="befab-103">Starts an export operation from an Azure SQL Database to Blob storage.</span></span>

## <span data-ttu-id="befab-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="befab-104">SYNTAX</span></span>

### <span data-ttu-id="befab-105">ByContainerObject</span><span class="sxs-lookup"><span data-stu-id="befab-105">ByContainerObject</span></span>
```
Start-AzureSqlDatabaseExport -SqlConnectionContext <ISqlServerConnectionInformation>
 -StorageContainer <AzureStorageContainer> -DatabaseName <String> -BlobName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="befab-106">ByContainerName</span><span class="sxs-lookup"><span data-stu-id="befab-106">ByContainerName</span></span>
```
Start-AzureSqlDatabaseExport -SqlConnectionContext <ISqlServerConnectionInformation>
 -StorageContext <IStorageContext> -StorageContainerName <String> -DatabaseName <String> -BlobName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="befab-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="befab-107">DESCRIPTION</span></span>
<span data-ttu-id="befab-108">O cmdlet **Start-AzureSqlDatabaseExport** inicia uma operação de exportação de um banco de dados SQL do Azure para o armazenamento de BLOB.</span><span class="sxs-lookup"><span data-stu-id="befab-108">The **Start-AzureSqlDatabaseExport** cmdlet starts an export operation from an Azure SQL Database to Blob storage.</span></span>
<span data-ttu-id="befab-109">A operação requer um contexto de conexão do servidor de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="befab-109">The operation requires a database server connection context.</span></span>
<span data-ttu-id="befab-110">Use o cmdlet Get-AzureSqlDatabaseImportExportStatus para obter o status da operação de exportação.</span><span class="sxs-lookup"><span data-stu-id="befab-110">Use the Get-AzureSqlDatabaseImportExportStatus cmdlet to get the status of the export operation.</span></span>

## <span data-ttu-id="befab-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="befab-111">EXAMPLES</span></span>

### <span data-ttu-id="befab-112">Exemplo 1: exportar um banco de dados</span><span class="sxs-lookup"><span data-stu-id="befab-112">Example 1: Export a database</span></span>
```
PS C:\>$Credential = Get-Credential
PS C:\> $SqlContext = New-AzureSqlDatabaseServerContext -ServerName $ServerName -Credential $Credential
PS C:\> $StorageContext = New-AzureStorageContext -StorageAccountName $StorageName -StorageAccountKey $StorageKey
PS C:\> $Container = Get-AzureStorageContainer -Name $ContainerName -Context $StorageContext
PS C:\> $exportRequest = Start-AzureSqlDatabaseExport -SqlConnectionContext $SqlContext -StorageContainer $Container -DatabaseName $DatabaseName -BlobName $BlobName
```

<span data-ttu-id="befab-113">Este exemplo inicia um processo de exportação do banco de dados SQL do Azure que tem o nome armazenado na variável $DatabaseName para o armazenamento blob armazenado na variável $BlobName.</span><span class="sxs-lookup"><span data-stu-id="befab-113">This example initiates an export process from the Azure SQL Database that has the name stored in the $DatabaseName variable to the Blob storage stored in the $BlobName variable.</span></span>

## <span data-ttu-id="befab-114">OS</span><span class="sxs-lookup"><span data-stu-id="befab-114">PARAMETERS</span></span>

### <span data-ttu-id="befab-115">-Blobname</span><span class="sxs-lookup"><span data-stu-id="befab-115">-BlobName</span></span>
<span data-ttu-id="befab-116">Especifica o nome do armazenamento de blob do Azure no qual esse cmdlet exporta o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="befab-116">Specifies the name of the Azure Blob storage into which this cmdlet exports the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="befab-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="befab-117">-DatabaseName</span></span>
<span data-ttu-id="befab-118">Especifica o nome do banco de dados a partir do qual esse cmdlet exporta dados.</span><span class="sxs-lookup"><span data-stu-id="befab-118">Specifies the name of the database from which this cmdlet exports data.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="befab-119">-Perfil</span><span class="sxs-lookup"><span data-stu-id="befab-119">-Profile</span></span>
<span data-ttu-id="befab-120">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="befab-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="befab-121">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="befab-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="befab-122">-SqlConnectionContext</span><span class="sxs-lookup"><span data-stu-id="befab-122">-SqlConnectionContext</span></span>
<span data-ttu-id="befab-123">Especifica o contexto de conexão de um servidor que contém o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="befab-123">Specifies the connection context of a server that contains the database.</span></span>

```yaml
Type: ISqlServerConnectionInformation
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="befab-124">-StorageContainer</span><span class="sxs-lookup"><span data-stu-id="befab-124">-StorageContainer</span></span>
<span data-ttu-id="befab-125">Especifica o contêiner de armazenamento que contém o blob em que esse cmdlet exporta um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="befab-125">Specifies the storage container that contains the Blob into which this cmdlet export a database.</span></span>

```yaml
Type: AzureStorageContainer
Parameter Sets: ByContainerObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="befab-126">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="befab-126">-StorageContainerName</span></span>
<span data-ttu-id="befab-127">Especifica o nome do contêiner de armazenamento que contém o blob em que esse cmdlet exporta um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="befab-127">Specifies the name of the storage container that contains the Blob into which this cmdlet exports a database.</span></span>

```yaml
Type: String
Parameter Sets: ByContainerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="befab-128">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="befab-128">-StorageContext</span></span>
<span data-ttu-id="befab-129">Especifica o contexto do contêiner de armazenamento BLOB.</span><span class="sxs-lookup"><span data-stu-id="befab-129">Specifies the context of the Blob storage container.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ByContainerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="befab-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="befab-130">CommonParameters</span></span>
<span data-ttu-id="befab-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="befab-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="befab-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="befab-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="befab-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="befab-133">INPUTS</span></span>

## <span data-ttu-id="befab-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="befab-134">OUTPUTS</span></span>

### <span data-ttu-id="befab-135">Microsoft. WindowsAzure. Commands. SQLDatabase. Services. ImportExportRequest</span><span class="sxs-lookup"><span data-stu-id="befab-135">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.ImportExportRequest</span></span>

## <span data-ttu-id="befab-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="befab-136">NOTES</span></span>

## <span data-ttu-id="befab-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="befab-137">RELATED LINKS</span></span>

[<span data-ttu-id="befab-138">Banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="befab-138">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="befab-139">Exportar banco de dados</span><span class="sxs-lookup"><span data-stu-id="befab-139">Export Database</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn781282.aspx)

[<span data-ttu-id="befab-140">Operações para bancos de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="befab-140">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="befab-141">Get-AzureSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="befab-141">Get-AzureSqlDatabaseImportExportStatus</span></span>](./Get-AzureSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="befab-142">Start-AzureSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="befab-142">Start-AzureSqlDatabaseImport</span></span>](./Start-AzureSqlDatabaseImport.md)


