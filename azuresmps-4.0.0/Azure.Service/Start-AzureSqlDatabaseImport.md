---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 5EE936CA-DD9A-4BC6-B835-E22AE633B46D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4bc7c8f39f1bdbd35cfffeb59b3b4f184f30845e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945427"
---
# <span data-ttu-id="0f1f8-101">Start-AzureSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="0f1f8-101">Start-AzureSqlDatabaseImport</span></span>

## <span data-ttu-id="0f1f8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0f1f8-102">SYNOPSIS</span></span>
<span data-ttu-id="0f1f8-103">Inicia uma operação de importação do armazenamento de BLOB para um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="0f1f8-103">Starts an import operation from blob storage to an Azure SQL Database.</span></span>

## <span data-ttu-id="0f1f8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0f1f8-104">SYNTAX</span></span>

### <span data-ttu-id="0f1f8-105">ByContainerObject</span><span class="sxs-lookup"><span data-stu-id="0f1f8-105">ByContainerObject</span></span>
```
Start-AzureSqlDatabaseImport -SqlConnectionContext <ISqlServerConnectionInformation>
 -StorageContainer <AzureStorageContainer> -DatabaseName <String> -BlobName <String>
 [-Edition <DatabaseEdition>] [-DatabaseMaxSize <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0f1f8-106">ByContainerName</span><span class="sxs-lookup"><span data-stu-id="0f1f8-106">ByContainerName</span></span>
```
Start-AzureSqlDatabaseImport -SqlConnectionContext <ISqlServerConnectionInformation>
 -StorageContext <IStorageContext> -StorageContainerName <String> -DatabaseName <String> -BlobName <String>
 [-Edition <DatabaseEdition>] [-DatabaseMaxSize <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0f1f8-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0f1f8-107">DESCRIPTION</span></span>
<span data-ttu-id="0f1f8-108">O cmdlet **Start-AzureSqlDatabaseImport** inicia uma operação de importação do armazenamento do blob do Azure para um banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="0f1f8-108">The **Start-AzureSqlDatabaseImport** cmdlet starts an import operation from Azure Blob storage to an Azure SQL Database.</span></span>
<span data-ttu-id="0f1f8-109">Se o banco de dados não existir, esse cmdlet o cria usando os valores de tamanho e edição que você especificar.</span><span class="sxs-lookup"><span data-stu-id="0f1f8-109">If the database does not exist, this cmdlet creates it by using the size and edition values that you specify.</span></span>
<span data-ttu-id="0f1f8-110">A operação requer um contexto de conexão do servidor de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="0f1f8-110">The operation requires a database server connection context.</span></span>
<span data-ttu-id="0f1f8-111">Use o cmdlet Get-AzureSqlDatabaseImportExportStatus para obter o status da operação de importação.</span><span class="sxs-lookup"><span data-stu-id="0f1f8-111">Use the Get-AzureSqlDatabaseImportExportStatus cmdlet to get the status of the import operation.</span></span>

## <span data-ttu-id="0f1f8-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0f1f8-112">EXAMPLES</span></span>

### <span data-ttu-id="0f1f8-113">Exemplo 1: importar um banco de dados</span><span class="sxs-lookup"><span data-stu-id="0f1f8-113">Example 1: Import a database</span></span>
```
PS C:\>$Credential = Get-Credential
PS C:\> $SqlContext = New-AzureSqlDatabaseServerContext -ServerName $ServerName -Credentials $Credential
PS C:\> $StorageContext = New-AzureStorageContext -StorageAccountName $StorageName -StorageAccountKey $StorageKey
PS C:\> $Container = Get-AzureStorageContainer -Name $ContainerName -Context $StorageContext
PS C:\> $ImportRequest = Start-AzureSqlDatabaseImport -SqlConnectionContext $SqlContext -StorageContainer $Container -DatabaseName $DatabaseName -BlobName $BlobName
```

<span data-ttu-id="0f1f8-114">Este exemplo inicia um processo de importação do armazenamento de blob na variável $BlobName para o banco de dados SQL do Azure chamado DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="0f1f8-114">This example initiates an import process from the Blob storage in the $BlobName variable into the Azure SQL Database named DatabaseName.</span></span>

## <span data-ttu-id="0f1f8-115">OS</span><span class="sxs-lookup"><span data-stu-id="0f1f8-115">PARAMETERS</span></span>

### <span data-ttu-id="0f1f8-116">-Blobname</span><span class="sxs-lookup"><span data-stu-id="0f1f8-116">-BlobName</span></span>
<span data-ttu-id="0f1f8-117">Especifica o nome do armazenamento de blob do Azure do qual esse cmdlet importa o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="0f1f8-117">Specifies the name of the Azure Blob storage from which this cmdlet imports the database.</span></span>

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

### <span data-ttu-id="0f1f8-118">-DatabaseMaxSize</span><span class="sxs-lookup"><span data-stu-id="0f1f8-118">-DatabaseMaxSize</span></span>
<span data-ttu-id="0f1f8-119">Especifica o tamanho máximo, em gigabytes, para o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="0f1f8-119">Specifies the maximum size, in gigabytes, for the database.</span></span>
<span data-ttu-id="0f1f8-120">Se o banco de dados não existir, esse cmdlet o cria com base nesse tamanho máximo.</span><span class="sxs-lookup"><span data-stu-id="0f1f8-120">If the database does not exist, this cmdlet creates it based on this maximum size.</span></span>
<span data-ttu-id="0f1f8-121">Os valores aceitáveis são diferentes de acordo com a edição.</span><span class="sxs-lookup"><span data-stu-id="0f1f8-121">The acceptable values differ based on edition.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f1f8-122">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0f1f8-122">-DatabaseName</span></span>
<span data-ttu-id="0f1f8-123">Especifica um nome para o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="0f1f8-123">Specifies a name for the database.</span></span>
<span data-ttu-id="0f1f8-124">Se o banco de dados não existir, esse cmdlet o criará e atribuirá o nome que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="0f1f8-124">If the database does not exist, this cmdlet creates it, and assigns the name that this parameter specifies.</span></span>

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

### <span data-ttu-id="0f1f8-125">-Edição</span><span class="sxs-lookup"><span data-stu-id="0f1f8-125">-Edition</span></span>
<span data-ttu-id="0f1f8-126">Especifica a edição do banco de dados.</span><span class="sxs-lookup"><span data-stu-id="0f1f8-126">Specifies the edition of the database.</span></span>
<span data-ttu-id="0f1f8-127">Se o banco de dados não existir, esse cmdlet o criará como esta edição.</span><span class="sxs-lookup"><span data-stu-id="0f1f8-127">If the database does not exist, this cmdlet creates it as this edition.</span></span>
<span data-ttu-id="0f1f8-128">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="0f1f8-128">Valid values are:</span></span> 

- <span data-ttu-id="0f1f8-129">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="0f1f8-129">None</span></span>
- <span data-ttu-id="0f1f8-130">Pela</span><span class="sxs-lookup"><span data-stu-id="0f1f8-130">Web</span></span> 
- <span data-ttu-id="0f1f8-131">Empresarial</span><span class="sxs-lookup"><span data-stu-id="0f1f8-131">Business</span></span> 
- <span data-ttu-id="0f1f8-132">Basic</span><span class="sxs-lookup"><span data-stu-id="0f1f8-132">Basic</span></span>
- <span data-ttu-id="0f1f8-133">Oficial</span><span class="sxs-lookup"><span data-stu-id="0f1f8-133">Standard</span></span>
- <span data-ttu-id="0f1f8-134">Gratifica</span><span class="sxs-lookup"><span data-stu-id="0f1f8-134">Premium</span></span>

<span data-ttu-id="0f1f8-135">O padrão é Web.</span><span class="sxs-lookup"><span data-stu-id="0f1f8-135">The default is Web.</span></span>

```yaml
Type: DatabaseEdition
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f1f8-136">-Perfil</span><span class="sxs-lookup"><span data-stu-id="0f1f8-136">-Profile</span></span>
<span data-ttu-id="0f1f8-137">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="0f1f8-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0f1f8-138">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="0f1f8-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0f1f8-139">-SqlConnectionContext</span><span class="sxs-lookup"><span data-stu-id="0f1f8-139">-SqlConnectionContext</span></span>
<span data-ttu-id="0f1f8-140">Especifica o contexto de conexão de um servidor que contém o banco de dados.</span><span class="sxs-lookup"><span data-stu-id="0f1f8-140">Specifies the connection context of a server that contains the database.</span></span>

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

### <span data-ttu-id="0f1f8-141">-StorageContainer</span><span class="sxs-lookup"><span data-stu-id="0f1f8-141">-StorageContainer</span></span>
<span data-ttu-id="0f1f8-142">Especifica o contêiner de armazenamento que contém o blob do qual esse cmdlet importa um banco de dados.</span><span class="sxs-lookup"><span data-stu-id="0f1f8-142">Specifies the storage container that contains the Blob from which this cmdlet imports a database.</span></span>

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

### <span data-ttu-id="0f1f8-143">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="0f1f8-143">-StorageContainerName</span></span>
<span data-ttu-id="0f1f8-144">Especifica o nome do contêiner de armazenamento BLOB.</span><span class="sxs-lookup"><span data-stu-id="0f1f8-144">Specifies the name of the Blob storage container.</span></span>

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

### <span data-ttu-id="0f1f8-145">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="0f1f8-145">-StorageContext</span></span>
<span data-ttu-id="0f1f8-146">Especifica o contexto do contêiner de armazenamento BLOB.</span><span class="sxs-lookup"><span data-stu-id="0f1f8-146">Specifies the context of the Blob storage container.</span></span>

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

### <span data-ttu-id="0f1f8-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f1f8-147">CommonParameters</span></span>
<span data-ttu-id="0f1f8-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f1f8-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f1f8-149">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f1f8-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f1f8-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0f1f8-150">INPUTS</span></span>

## <span data-ttu-id="0f1f8-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0f1f8-151">OUTPUTS</span></span>

### <span data-ttu-id="0f1f8-152">Microsoft. WindowsAzure. Commands. SQLDatabase. Services. ImportExportRequest</span><span class="sxs-lookup"><span data-stu-id="0f1f8-152">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.ImportExportRequest</span></span>

## <span data-ttu-id="0f1f8-153">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0f1f8-153">NOTES</span></span>

## <span data-ttu-id="0f1f8-154">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0f1f8-154">RELATED LINKS</span></span>

[<span data-ttu-id="0f1f8-155">Banco de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="0f1f8-155">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="0f1f8-156">Importar banco de dados</span><span class="sxs-lookup"><span data-stu-id="0f1f8-156">Import Database</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn781284.aspx)

[<span data-ttu-id="0f1f8-157">Operações para bancos de dados SQL do Azure</span><span class="sxs-lookup"><span data-stu-id="0f1f8-157">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="0f1f8-158">Get-AzureSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="0f1f8-158">Get-AzureSqlDatabaseImportExportStatus</span></span>](./Get-AzureSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="0f1f8-159">Start-AzureSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="0f1f8-159">Start-AzureSqlDatabaseExport</span></span>](./Start-AzureSqlDatabaseExport.md)


