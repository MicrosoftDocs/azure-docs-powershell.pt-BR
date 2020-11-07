---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 4661C479-6E3B-425D-B9D2-B36D7A83130C
online version: ''
schema: 2.0.0
ms.openlocfilehash: c3c55ebd22337a8078f3ae495b3901317f4201e0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946294"
---
# <span data-ttu-id="54024-101">Get-AzureSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="54024-101">Get-AzureSqlDatabaseImportExportStatus</span></span>

## <span data-ttu-id="54024-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="54024-102">SYNOPSIS</span></span>
<span data-ttu-id="54024-103">Obtém o status de uma solicitação de importação ou exportação.</span><span class="sxs-lookup"><span data-stu-id="54024-103">Gets the status of an import or export request.</span></span>

## <span data-ttu-id="54024-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="54024-104">SYNTAX</span></span>

### <span data-ttu-id="54024-105">ByConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="54024-105">ByConnectionInfo</span></span>
```
Get-AzureSqlDatabaseImportExportStatus -Username <String> -Password <String> -ServerName <String>
 -RequestId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="54024-106">ByRequestObject</span><span class="sxs-lookup"><span data-stu-id="54024-106">ByRequestObject</span></span>
```
Get-AzureSqlDatabaseImportExportStatus -Request <ImportExportRequest> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="54024-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="54024-107">DESCRIPTION</span></span>
<span data-ttu-id="54024-108">O cmdlet **Get-AzureSqlDatabaseImportExportStatus** Obtém o status de uma solicitação de importação ou exportação.</span><span class="sxs-lookup"><span data-stu-id="54024-108">The **Get-AzureSqlDatabaseImportExportStatus** cmdlet gets the status of an import or export request.</span></span>
<span data-ttu-id="54024-109">O cmdlet Start-AzureSqlDatabaseImport ou Start-AzureSqlDatabaseExport iniciar solicitações.</span><span class="sxs-lookup"><span data-stu-id="54024-109">The Start-AzureSqlDatabaseImport or Start-AzureSqlDatabaseExport cmdlet initiates requests.</span></span>
<span data-ttu-id="54024-110">Você pode especificar o objeto de solicitação usando o parâmetro de *solicitação* ou pode identificar a solicitação usando o parâmetro *RequestId* e os parâmetros *username* , *password* e *nomedoservidor* .</span><span class="sxs-lookup"><span data-stu-id="54024-110">You can specify the request object by using the *Request* parameter, or you can identify the request by using the *RequestId* parameter and the *Username* , *Password* , and *ServerName* parameters.</span></span>

## <span data-ttu-id="54024-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="54024-111">EXAMPLES</span></span>

### <span data-ttu-id="54024-112">Exemplo 1: obter o status de uma solicitação de exportação</span><span class="sxs-lookup"><span data-stu-id="54024-112">Example 1: Get the status of an export request</span></span>
```
PS C:\> $ExportRequest = Start-AzureSqlDatabaseExport -SqlConnectionContext $SqlContext -StorageContainer $Container -DatabaseName $DatabaseName -BlobName $BlobName
PS C:\> Get-AzureSqlDatabaseImportExportStatus -Request $ExportRequest
```

<span data-ttu-id="54024-113">O primeiro comando cria uma solicitação de exportação e armazena-a na variável $ExportRequest.</span><span class="sxs-lookup"><span data-stu-id="54024-113">The first command creates an export request, and then stores it in the $ExportRequest variable.</span></span>

<span data-ttu-id="54024-114">O segundo comando obtém o status da solicitação de exportação armazenada em $ExportRequest.</span><span class="sxs-lookup"><span data-stu-id="54024-114">The second command gets the status of the export request stored in $ExportRequest.</span></span>

## <span data-ttu-id="54024-115">OS</span><span class="sxs-lookup"><span data-stu-id="54024-115">PARAMETERS</span></span>

### <span data-ttu-id="54024-116">-Senha</span><span class="sxs-lookup"><span data-stu-id="54024-116">-Password</span></span>
<span data-ttu-id="54024-117">Especifica a senha necessária para se conectar ao servidor do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="54024-117">Specifies the password that is required to connect to the Azure SQL Database server.</span></span>
<span data-ttu-id="54024-118">Você deve especificar esse parâmetro se tiver especificado o parâmetro *RequestId* .</span><span class="sxs-lookup"><span data-stu-id="54024-118">You must specify this parameter if you specified the *RequestId* parameter.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54024-119">-Perfil</span><span class="sxs-lookup"><span data-stu-id="54024-119">-Profile</span></span>
<span data-ttu-id="54024-120">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="54024-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="54024-121">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="54024-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="54024-122">-Solicitação</span><span class="sxs-lookup"><span data-stu-id="54024-122">-Request</span></span>
<span data-ttu-id="54024-123">Especifica um objeto **ImportExportRequest** .</span><span class="sxs-lookup"><span data-stu-id="54024-123">Specifies an **ImportExportRequest** object.</span></span>
<span data-ttu-id="54024-124">Para obter um objeto de solicitação de importação ou exportação, use o cmdlet Start-AzureSqlDatabaseImport ou Start-AzureSqlDatabaseExport.</span><span class="sxs-lookup"><span data-stu-id="54024-124">To obtain an import or export request object, use the Start-AzureSqlDatabaseImport or Start-AzureSqlDatabaseExport cmdlet.</span></span>

```yaml
Type: ImportExportRequest
Parameter Sets: ByRequestObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54024-125">-RequestId</span><span class="sxs-lookup"><span data-stu-id="54024-125">-RequestId</span></span>
<span data-ttu-id="54024-126">Especifica o GUID da operação de importação ou de exportação para a qual esse cmdlet obtém o status.</span><span class="sxs-lookup"><span data-stu-id="54024-126">Specifies the GUID of the import or export operation for which this cmdlet gets status.</span></span>
<span data-ttu-id="54024-127">Se você especificar esse parâmetro, você deve especificar os parâmetros *username* , *password* e *nomedoservidor* .</span><span class="sxs-lookup"><span data-stu-id="54024-127">If you specify this parameter, you must specify the *UserName* , *Password* , and *ServerName* parameters.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54024-128">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="54024-128">-ServerName</span></span>
<span data-ttu-id="54024-129">Especifica o nome do servidor de banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="54024-129">Specifies the name of the Azure SQL Database server.</span></span>
<span data-ttu-id="54024-130">Você deve especificar esse parâmetro se tiver especificado o parâmetro *RequestId* .</span><span class="sxs-lookup"><span data-stu-id="54024-130">You must specify this parameter if you specified the *RequestId* parameter.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54024-131">-Username</span><span class="sxs-lookup"><span data-stu-id="54024-131">-Username</span></span>
<span data-ttu-id="54024-132">Especifica o nome de usuário necessário para se conectar ao servidor do banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="54024-132">Specifies the user name required to connect to the Azure SQL Database server.</span></span>
<span data-ttu-id="54024-133">Você deve especificar esse parâmetro se tiver especificado o parâmetro *RequestId* .</span><span class="sxs-lookup"><span data-stu-id="54024-133">You must specify this parameter if you specified the *RequestId* parameter.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54024-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54024-134">CommonParameters</span></span>
<span data-ttu-id="54024-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54024-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54024-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54024-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54024-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="54024-137">INPUTS</span></span>

## <span data-ttu-id="54024-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="54024-138">OUTPUTS</span></span>

### <span data-ttu-id="54024-139">Microsoft. WindowsAzure. Commands. SQLDatabase. Services. ImportExport. StatusInfo</span><span class="sxs-lookup"><span data-stu-id="54024-139">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.ImportExport.StatusInfo</span></span>

## <span data-ttu-id="54024-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="54024-140">NOTES</span></span>

## <span data-ttu-id="54024-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="54024-141">RELATED LINKS</span></span>

[<span data-ttu-id="54024-142">Banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="54024-142">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="54024-143">Obter o status do banco de dados de exportação de importação</span><span class="sxs-lookup"><span data-stu-id="54024-143">Get Import Export Database Status</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn781289.aspx)

[<span data-ttu-id="54024-144">Operações para bancos de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="54024-144">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="54024-145">Start-AzureSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="54024-145">Start-AzureSqlDatabaseExport</span></span>](./Start-AzureSqlDatabaseExport.md)

[<span data-ttu-id="54024-146">Start-AzureSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="54024-146">Start-AzureSqlDatabaseImport</span></span>](./Start-AzureSqlDatabaseImport.md)


