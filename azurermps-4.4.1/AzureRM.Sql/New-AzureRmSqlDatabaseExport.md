---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 3D4822DD-736B-42DF-8D9A-1CB23FEF052E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseExport.md
ms.openlocfilehash: f7ede8432f8e833b3d309925daab591889836257
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610696"
---
# <span data-ttu-id="47433-101">New-AzureRmSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="47433-101">New-AzureRmSqlDatabaseExport</span></span>

## <span data-ttu-id="47433-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="47433-102">SYNOPSIS</span></span>
<span data-ttu-id="47433-103">Exporta um banco de dados SQL do Azure como um arquivo. bacpac para uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="47433-103">Exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47433-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="47433-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseExport [-DatabaseName] <String> [-ServerName] <String> -StorageKeyType <StorageKeyType>
 -StorageKey <String> -StorageUri <Uri> -AdministratorLogin <String> -AdministratorLoginPassword <SecureString>
 [-AuthenticationType <AuthenticationType>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47433-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="47433-105">DESCRIPTION</span></span>
<span data-ttu-id="47433-106">O cmdlet **New-AzureRmSqlDatabaseExport** exporta um banco de dados SQL do Azure como um arquivo. bacpac para uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="47433-106">The **New-AzureRmSqlDatabaseExport** cmdlet exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>
<span data-ttu-id="47433-107">A solicitação de status de obter o banco de dados de exportação pode ser enviada para recuperar informações de status para essa solicitação.</span><span class="sxs-lookup"><span data-stu-id="47433-107">The get export database status request may be sent to retrieve status information for this request.</span></span>

<span data-ttu-id="47433-108">Esse cmdlet também é compatível com o serviço Stretch Database do SQL Server no Azure.</span><span class="sxs-lookup"><span data-stu-id="47433-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="47433-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="47433-109">EXAMPLES</span></span>

### <span data-ttu-id="47433-110">Exemplo 1: criar uma solicitação de exportação para um banco de dados</span><span class="sxs-lookup"><span data-stu-id="47433-110">Example 1: Create an export request for a database</span></span>
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

<span data-ttu-id="47433-111">Esse comando cria uma solicitação de exportação para o banco de dados especificado.</span><span class="sxs-lookup"><span data-stu-id="47433-111">This command creates an export request for the specified database.</span></span>

## <span data-ttu-id="47433-112">OS</span><span class="sxs-lookup"><span data-stu-id="47433-112">PARAMETERS</span></span>

### <span data-ttu-id="47433-113">-AdministratorLogin</span><span class="sxs-lookup"><span data-stu-id="47433-113">-AdministratorLogin</span></span>
<span data-ttu-id="47433-114">Especifica o nome do administrador do SQL.</span><span class="sxs-lookup"><span data-stu-id="47433-114">Specifies the name of the SQL administrator.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47433-115">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="47433-115">-AdministratorLoginPassword</span></span>
<span data-ttu-id="47433-116">Especifica a senha do administrador do SQL.</span><span class="sxs-lookup"><span data-stu-id="47433-116">Specifies the password of the SQL administrator.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47433-117">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="47433-117">-AuthenticationType</span></span>
<span data-ttu-id="47433-118">Especifica o tipo de autenticação usado para acessar o servidor.</span><span class="sxs-lookup"><span data-stu-id="47433-118">Specifies the type of authentication used to access the server.</span></span>
<span data-ttu-id="47433-119">O valor padrão é SQL se nenhum tipo de autenticação for definido.</span><span class="sxs-lookup"><span data-stu-id="47433-119">The default value is SQL if no authentication type is set.</span></span>

<span data-ttu-id="47433-120">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="47433-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="47433-121">Server.</span><span class="sxs-lookup"><span data-stu-id="47433-121">Sql.</span></span>
<span data-ttu-id="47433-122">Autenticação do SQL.</span><span class="sxs-lookup"><span data-stu-id="47433-122">SQL authentication.</span></span>
<span data-ttu-id="47433-123">Defina *AdministratorLogin* e *AdministratorLoginPassword* para o nome de usuário e a senha do administrador do SQL.</span><span class="sxs-lookup"><span data-stu-id="47433-123">Set the *AdministratorLogin* and *AdministratorLoginPassword* to the SQL administrator username and password.</span></span> 
- <span data-ttu-id="47433-124">ADPassword.</span><span class="sxs-lookup"><span data-stu-id="47433-124">ADPassword.</span></span>
<span data-ttu-id="47433-125">Autenticação do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="47433-125">Azure Active Directory authentication.</span></span>
<span data-ttu-id="47433-126">Defina *AdministratorLogin* e *AdministratorLoginPassword* para o nome de usuário e a senha do administrador do Azure AD.</span><span class="sxs-lookup"><span data-stu-id="47433-126">Set *AdministratorLogin* and *AdministratorLoginPassword* to the Azure AD administrator username and password.</span></span>

<span data-ttu-id="47433-127">Esse parâmetro só está disponível em servidores do banco de dados SQL V12.</span><span class="sxs-lookup"><span data-stu-id="47433-127">This parameter is only available on SQL Database V12 servers.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ImportExport.Model.AuthenticationType
Parameter Sets: (All)
Aliases: 
Accepted values: None, Sql, AdPassword

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47433-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="47433-128">-DatabaseName</span></span>
<span data-ttu-id="47433-129">Especifica o nome do banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="47433-129">Specifies the name of the SQL Database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47433-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47433-130">-ResourceGroupName</span></span>
<span data-ttu-id="47433-131">Especifica o nome do grupo de recursos do servidor de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="47433-131">Specifies the name of the resource group for the SQL Database server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47433-132">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="47433-132">-ServerName</span></span>
<span data-ttu-id="47433-133">Especifica o nome do servidor de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="47433-133">Specifies the name of the SQL Database server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47433-134">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="47433-134">-StorageKey</span></span>
<span data-ttu-id="47433-135">Especifica a tecla de acesso para a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="47433-135">Specifies the access key for the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47433-136">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="47433-136">-StorageKeyType</span></span>
<span data-ttu-id="47433-137">Especifica o tipo de tecla de acesso da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="47433-137">Specifies the type of access key for the storage account.</span></span>

<span data-ttu-id="47433-138">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="47433-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="47433-139">StorageAccessKey.</span><span class="sxs-lookup"><span data-stu-id="47433-139">StorageAccessKey.</span></span>
<span data-ttu-id="47433-140">Esse valor usa uma chave de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="47433-140">This value uses a storage account key.</span></span> 
- <span data-ttu-id="47433-141">SharedAccessKey.</span><span class="sxs-lookup"><span data-stu-id="47433-141">SharedAccessKey.</span></span>
<span data-ttu-id="47433-142">Esse valor usa uma chave de assinatura de acesso compartilhado (SAS).</span><span class="sxs-lookup"><span data-stu-id="47433-142">This value uses a Shared Access Signature (SAS) key.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ImportExport.Model.StorageKeyType
Parameter Sets: (All)
Aliases: 
Accepted values: StorageAccessKey, SharedAccessKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47433-143">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="47433-143">-StorageUri</span></span>
<span data-ttu-id="47433-144">Especifica o link de BLOB, como uma URL, para o arquivo. bacpac.</span><span class="sxs-lookup"><span data-stu-id="47433-144">Specifies the blob link, as a URL, to the .bacpac file.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47433-145">-Confirme</span><span class="sxs-lookup"><span data-stu-id="47433-145">-Confirm</span></span>
<span data-ttu-id="47433-146">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47433-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47433-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47433-147">-WhatIf</span></span>
<span data-ttu-id="47433-148">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="47433-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47433-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="47433-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47433-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47433-150">-DefaultProfile</span></span>
<span data-ttu-id="47433-151">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="47433-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47433-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47433-152">CommonParameters</span></span>
<span data-ttu-id="47433-153">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47433-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47433-154">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47433-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47433-155">SENSORES</span><span class="sxs-lookup"><span data-stu-id="47433-155">INPUTS</span></span>

## <span data-ttu-id="47433-156">EXIBE</span><span class="sxs-lookup"><span data-stu-id="47433-156">OUTPUTS</span></span>

### <span data-ttu-id="47433-157">Microsoft. Azure. Commands. Sql. Database. Model. AzureSqlDatabaseImportExportBaseModel</span><span class="sxs-lookup"><span data-stu-id="47433-157">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseImportExportBaseModel</span></span>

## <span data-ttu-id="47433-158">INFORMA</span><span class="sxs-lookup"><span data-stu-id="47433-158">NOTES</span></span>
* <span data-ttu-id="47433-159">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, SQL, Database, MSSQL</span><span class="sxs-lookup"><span data-stu-id="47433-159">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="47433-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="47433-160">RELATED LINKS</span></span>

[<span data-ttu-id="47433-161">Get-AzureRmSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="47433-161">Get-AzureRmSqlDatabaseImportExportStatus</span></span>](./Get-AzureRmSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="47433-162">New-AzureRmSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="47433-162">New-AzureRmSqlDatabaseImport</span></span>](./New-AzureRmSqlDatabaseImport.md)

[<span data-ttu-id="47433-163">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="47433-163">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
