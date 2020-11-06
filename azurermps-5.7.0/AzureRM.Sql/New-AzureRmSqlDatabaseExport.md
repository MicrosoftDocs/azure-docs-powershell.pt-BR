---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 3D4822DD-736B-42DF-8D9A-1CB23FEF052E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabaseexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseExport.md
ms.openlocfilehash: 324686ace908235e3b48fb150249d2bad22c169b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426550"
---
# <span data-ttu-id="3ecf1-101">New-AzureRmSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="3ecf1-101">New-AzureRmSqlDatabaseExport</span></span>

## <span data-ttu-id="3ecf1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3ecf1-102">SYNOPSIS</span></span>
<span data-ttu-id="3ecf1-103">Exporta um banco de dados SQL do Azure como um arquivo. bacpac para uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="3ecf1-103">Exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3ecf1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3ecf1-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseExport [-DatabaseName] <String> [-ServerName] <String> -StorageKeyType <StorageKeyType>
 -StorageKey <String> -StorageUri <Uri> -AdministratorLogin <String> -AdministratorLoginPassword <SecureString>
 [-AuthenticationType <AuthenticationType>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ecf1-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3ecf1-105">DESCRIPTION</span></span>
<span data-ttu-id="3ecf1-106">O cmdlet **New-AzureRmSqlDatabaseExport** exporta um banco de dados SQL do Azure como um arquivo. bacpac para uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="3ecf1-106">The **New-AzureRmSqlDatabaseExport** cmdlet exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>
<span data-ttu-id="3ecf1-107">A solicitação de status de obter o banco de dados de exportação pode ser enviada para recuperar informações de status para essa solicitação.</span><span class="sxs-lookup"><span data-stu-id="3ecf1-107">The get export database status request may be sent to retrieve status information for this request.</span></span>

<span data-ttu-id="3ecf1-108">Esse cmdlet também é compatível com o serviço Stretch Database do SQL Server no Azure.</span><span class="sxs-lookup"><span data-stu-id="3ecf1-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="3ecf1-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3ecf1-109">EXAMPLES</span></span>

### <span data-ttu-id="3ecf1-110">Exemplo 1: criar uma solicitação de exportação para um banco de dados</span><span class="sxs-lookup"><span data-stu-id="3ecf1-110">Example 1: Create an export request for a database</span></span>
```
PS C:\>New-AzureRmSqlDatabaseExport -ResourceGroupName "RG01" -ServerName "Server01" -DatabaseName "Database01" -StorageKeyType "StorageAccessKey" -StorageKey "StorageKey01" -StorageUri "http://account01.blob.core.contoso.net/bacpacs/database01.bacpac" -AdministratorLogin "User" -AdministratorLoginPassword "secure password"
ResourceGroupName          : RG01
ServerName                 : Server01
DatabaseName               : Database01
StorageKeyType             : StorageAccessKey
StorageKey                 : 
StorageUri                 : http://account01.blob.core.contoso.net/bacpacs/database01.bacpac
AdministratorLogin         : User
AdministratorLoginPassword : 
AuthenticationType         : None
OperationStatusLink        : https://management.azure.com/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/resource01/providers/Microsoft.Sql/servers/server01/databases/database01/importExportOperationResults/00000000-00
                             0-0000-0000-000000000000?api-version=2014-04-01
Status                     : InProgress
ErrorMessage               :
```

<span data-ttu-id="3ecf1-111">Esse comando cria uma solicitação de exportação para o banco de dados especificado.</span><span class="sxs-lookup"><span data-stu-id="3ecf1-111">This command creates an export request for the specified database.</span></span>

## <span data-ttu-id="3ecf1-112">OS</span><span class="sxs-lookup"><span data-stu-id="3ecf1-112">PARAMETERS</span></span>

### <span data-ttu-id="3ecf1-113">-AdministratorLogin</span><span class="sxs-lookup"><span data-stu-id="3ecf1-113">-AdministratorLogin</span></span>
<span data-ttu-id="3ecf1-114">Especifica o nome do administrador do SQL.</span><span class="sxs-lookup"><span data-stu-id="3ecf1-114">Specifies the name of the SQL administrator.</span></span>

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

### <span data-ttu-id="3ecf1-115">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="3ecf1-115">-AdministratorLoginPassword</span></span>
<span data-ttu-id="3ecf1-116">Especifica a senha do administrador do SQL.</span><span class="sxs-lookup"><span data-stu-id="3ecf1-116">Specifies the password of the SQL administrator.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ecf1-117">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="3ecf1-117">-AuthenticationType</span></span>
<span data-ttu-id="3ecf1-118">Especifica o tipo de autenticação usado para acessar o servidor.</span><span class="sxs-lookup"><span data-stu-id="3ecf1-118">Specifies the type of authentication used to access the server.</span></span>
<span data-ttu-id="3ecf1-119">O valor padrão é SQL se nenhum tipo de autenticação for definido.</span><span class="sxs-lookup"><span data-stu-id="3ecf1-119">The default value is SQL if no authentication type is set.</span></span>

<span data-ttu-id="3ecf1-120">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="3ecf1-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3ecf1-121">Server.</span><span class="sxs-lookup"><span data-stu-id="3ecf1-121">Sql.</span></span>
<span data-ttu-id="3ecf1-122">Autenticação do SQL.</span><span class="sxs-lookup"><span data-stu-id="3ecf1-122">SQL authentication.</span></span>
<span data-ttu-id="3ecf1-123">Defina *AdministratorLogin* e *AdministratorLoginPassword* para o nome de usuário e a senha do administrador do SQL.</span><span class="sxs-lookup"><span data-stu-id="3ecf1-123">Set the *AdministratorLogin* and *AdministratorLoginPassword* to the SQL administrator username and password.</span></span> 
- <span data-ttu-id="3ecf1-124">ADPassword.</span><span class="sxs-lookup"><span data-stu-id="3ecf1-124">ADPassword.</span></span>
<span data-ttu-id="3ecf1-125">Autenticação do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3ecf1-125">Azure Active Directory authentication.</span></span>
<span data-ttu-id="3ecf1-126">Defina *AdministratorLogin* e *AdministratorLoginPassword* para o nome de usuário e a senha do administrador do Azure AD.</span><span class="sxs-lookup"><span data-stu-id="3ecf1-126">Set *AdministratorLogin* and *AdministratorLoginPassword* to the Azure AD administrator username and password.</span></span>

<span data-ttu-id="3ecf1-127">Esse parâmetro só está disponível em servidores do banco de dados SQL V12.</span><span class="sxs-lookup"><span data-stu-id="3ecf1-127">This parameter is only available on SQL Database V12 servers.</span></span>

```yaml
Type: AuthenticationType
Parameter Sets: (All)
Aliases:
Accepted values: None, Sql, AdPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ecf1-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3ecf1-128">-DatabaseName</span></span>
<span data-ttu-id="3ecf1-129">Especifica o nome do banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="3ecf1-129">Specifies the name of the SQL Database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ecf1-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ecf1-130">-DefaultProfile</span></span>
<span data-ttu-id="3ecf1-131">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="3ecf1-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ecf1-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ecf1-132">-ResourceGroupName</span></span>
<span data-ttu-id="3ecf1-133">Especifica o nome do grupo de recursos do servidor de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="3ecf1-133">Specifies the name of the resource group for the SQL Database server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ecf1-134">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="3ecf1-134">-ServerName</span></span>
<span data-ttu-id="3ecf1-135">Especifica o nome do servidor de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="3ecf1-135">Specifies the name of the SQL Database server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ecf1-136">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="3ecf1-136">-StorageKey</span></span>
<span data-ttu-id="3ecf1-137">Especifica a tecla de acesso para a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="3ecf1-137">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="3ecf1-138">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="3ecf1-138">-StorageKeyType</span></span>
<span data-ttu-id="3ecf1-139">Especifica o tipo de tecla de acesso da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="3ecf1-139">Specifies the type of access key for the storage account.</span></span>

<span data-ttu-id="3ecf1-140">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="3ecf1-140">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3ecf1-141">StorageAccessKey.</span><span class="sxs-lookup"><span data-stu-id="3ecf1-141">StorageAccessKey.</span></span>
<span data-ttu-id="3ecf1-142">Esse valor usa uma chave de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="3ecf1-142">This value uses a storage account key.</span></span> 
- <span data-ttu-id="3ecf1-143">SharedAccessKey.</span><span class="sxs-lookup"><span data-stu-id="3ecf1-143">SharedAccessKey.</span></span>
<span data-ttu-id="3ecf1-144">Esse valor usa uma chave de assinatura de acesso compartilhado (SAS).</span><span class="sxs-lookup"><span data-stu-id="3ecf1-144">This value uses a Shared Access Signature (SAS) key.</span></span>

```yaml
Type: StorageKeyType
Parameter Sets: (All)
Aliases:
Accepted values: StorageAccessKey, SharedAccessKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ecf1-145">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="3ecf1-145">-StorageUri</span></span>
<span data-ttu-id="3ecf1-146">Especifica o link de BLOB, como uma URL, para o arquivo. bacpac.</span><span class="sxs-lookup"><span data-stu-id="3ecf1-146">Specifies the blob link, as a URL, to the .bacpac file.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ecf1-147">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3ecf1-147">-Confirm</span></span>
<span data-ttu-id="3ecf1-148">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ecf1-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ecf1-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ecf1-149">-WhatIf</span></span>
<span data-ttu-id="3ecf1-150">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3ecf1-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ecf1-151">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3ecf1-151">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ecf1-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ecf1-152">CommonParameters</span></span>
<span data-ttu-id="3ecf1-153">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ecf1-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ecf1-154">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ecf1-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ecf1-155">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3ecf1-155">INPUTS</span></span>

### <span data-ttu-id="3ecf1-156">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="3ecf1-156">None</span></span>
<span data-ttu-id="3ecf1-157">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="3ecf1-157">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3ecf1-158">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3ecf1-158">OUTPUTS</span></span>

### <span data-ttu-id="3ecf1-159">Microsoft. Azure. Commands. Sql. Database. Model. AzureSqlDatabaseImportExportBaseModel</span><span class="sxs-lookup"><span data-stu-id="3ecf1-159">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseImportExportBaseModel</span></span>

## <span data-ttu-id="3ecf1-160">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3ecf1-160">NOTES</span></span>
* <span data-ttu-id="3ecf1-161">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, SQL, Database, MSSQL</span><span class="sxs-lookup"><span data-stu-id="3ecf1-161">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="3ecf1-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3ecf1-162">RELATED LINKS</span></span>

[<span data-ttu-id="3ecf1-163">Get-AzureRmSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="3ecf1-163">Get-AzureRmSqlDatabaseImportExportStatus</span></span>](./Get-AzureRmSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="3ecf1-164">New-AzureRmSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="3ecf1-164">New-AzureRmSqlDatabaseImport</span></span>](./New-AzureRmSqlDatabaseImport.md)

[<span data-ttu-id="3ecf1-165">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="3ecf1-165">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)