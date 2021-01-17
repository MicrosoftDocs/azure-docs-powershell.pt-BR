---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 3D4822DD-736B-42DF-8D9A-1CB23FEF052E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabaseexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseExport.md
ms.openlocfilehash: 737b7170b774be712fb316f5c76b95d326e22fdb
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427972"
---
# <span data-ttu-id="2b937-101">New-AzSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="2b937-101">New-AzSqlDatabaseExport</span></span>

## <span data-ttu-id="2b937-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2b937-102">SYNOPSIS</span></span>
<span data-ttu-id="2b937-103">Exporta um banco de dados SQL do Azure como um arquivo. bacpac para uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="2b937-103">Exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>

## <span data-ttu-id="2b937-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2b937-104">SYNTAX</span></span>

```
New-AzSqlDatabaseExport [-DatabaseName] <String> [-ServerName] <String> -StorageKeyType <StorageKeyType>
 -StorageKey <String> -StorageUri <Uri> -AdministratorLogin <String> -AdministratorLoginPassword <SecureString>
 [-AuthenticationType <AuthenticationType>] [-UseNetworkIsolation <Boolean>]
 [-StorageAccountResourceIdForPrivateLink <String>] [-SqlServerResourceIdForPrivateLink <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2b937-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2b937-105">DESCRIPTION</span></span>
<span data-ttu-id="2b937-106">O cmdlet **New-AzSqlDatabaseExport** exporta um banco de dados SQL do Azure como um arquivo. bacpac para uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="2b937-106">The **New-AzSqlDatabaseExport** cmdlet exports an Azure SQL Database as a .bacpac file to a storage account.</span></span>
<span data-ttu-id="2b937-107">A solicitação de status de obter o banco de dados de exportação pode ser enviada para recuperar informações de status para essa solicitação.</span><span class="sxs-lookup"><span data-stu-id="2b937-107">The get export database status request may be sent to retrieve status information for this request.</span></span>
<span data-ttu-id="2b937-108">Esse cmdlet também é compatível com o serviço Stretch Database do SQL Server no Azure.</span><span class="sxs-lookup"><span data-stu-id="2b937-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2b937-109">Para usar este cmdlet, o firewall no SQL Server do Azure precisará ser configurado para "permitir que os serviços e recursos do Azure acessem este servidor".</span><span class="sxs-lookup"><span data-stu-id="2b937-109">In order to make use of this cmdlet the firewall on the Azure SQL Server will need to be configured to "Allow Azure services and resources to access this server".</span></span> <span data-ttu-id="2b937-110">Se isso não estiver configurado, os erros do GatewayTimeout serão detectados.</span><span class="sxs-lookup"><span data-stu-id="2b937-110">If this is not configured then GatewayTimeout errors will be experienced.</span></span>

## <span data-ttu-id="2b937-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2b937-111">EXAMPLES</span></span>

### <span data-ttu-id="2b937-112">Exemplo 1: criar uma solicitação de exportação para um banco de dados</span><span class="sxs-lookup"><span data-stu-id="2b937-112">Example 1: Create an export request for a database</span></span>
```
PS C:\>New-AzSqlDatabaseExport -ResourceGroupName "RG01" -ServerName "Server01" -DatabaseName "Database01" -StorageKeyType "StorageAccessKey" -StorageKey "StorageKey01" -StorageUri "http://account01.blob.core.contoso.net/bacpacs/database01.bacpac" -AdministratorLogin "User" -AdministratorLoginPassword "secure password"
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

<span data-ttu-id="2b937-113">Esse comando cria uma solicitação de exportação para o banco de dados especificado.</span><span class="sxs-lookup"><span data-stu-id="2b937-113">This command creates an export request for the specified database.</span></span>

## <span data-ttu-id="2b937-114">OS</span><span class="sxs-lookup"><span data-stu-id="2b937-114">PARAMETERS</span></span>

### <span data-ttu-id="2b937-115">-AdministratorLogin</span><span class="sxs-lookup"><span data-stu-id="2b937-115">-AdministratorLogin</span></span>
<span data-ttu-id="2b937-116">Especifica o nome do administrador do SQL.</span><span class="sxs-lookup"><span data-stu-id="2b937-116">Specifies the name of the SQL administrator.</span></span>

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

### <span data-ttu-id="2b937-117">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="2b937-117">-AdministratorLoginPassword</span></span>
<span data-ttu-id="2b937-118">Especifica a senha do administrador do SQL.</span><span class="sxs-lookup"><span data-stu-id="2b937-118">Specifies the password of the SQL administrator.</span></span>

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

### <span data-ttu-id="2b937-119">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="2b937-119">-AuthenticationType</span></span>
<span data-ttu-id="2b937-120">Especifica o tipo de autenticação usado para acessar o servidor.</span><span class="sxs-lookup"><span data-stu-id="2b937-120">Specifies the type of authentication used to access the server.</span></span>
<span data-ttu-id="2b937-121">O valor padrão é SQL se nenhum tipo de autenticação for definido.</span><span class="sxs-lookup"><span data-stu-id="2b937-121">The default value is SQL if no authentication type is set.</span></span>
<span data-ttu-id="2b937-122">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="2b937-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2b937-123">Server.</span><span class="sxs-lookup"><span data-stu-id="2b937-123">Sql.</span></span>
<span data-ttu-id="2b937-124">Autenticação do SQL.</span><span class="sxs-lookup"><span data-stu-id="2b937-124">SQL authentication.</span></span>
<span data-ttu-id="2b937-125">Defina *AdministratorLogin* e *AdministratorLoginPassword* para o nome de usuário e a senha do administrador do SQL.</span><span class="sxs-lookup"><span data-stu-id="2b937-125">Set the *AdministratorLogin* and *AdministratorLoginPassword* to the SQL administrator username and password.</span></span> 
- <span data-ttu-id="2b937-126">ADPassword.</span><span class="sxs-lookup"><span data-stu-id="2b937-126">ADPassword.</span></span>
<span data-ttu-id="2b937-127">Autenticação do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2b937-127">Azure Active Directory authentication.</span></span>
<span data-ttu-id="2b937-128">Defina *AdministratorLogin* e *AdministratorLoginPassword* para o nome de usuário e a senha do administrador do Azure AD.</span><span class="sxs-lookup"><span data-stu-id="2b937-128">Set *AdministratorLogin* and *AdministratorLoginPassword* to the Azure AD administrator username and password.</span></span>
<span data-ttu-id="2b937-129">Esse parâmetro só está disponível em servidores do banco de dados SQL V12.</span><span class="sxs-lookup"><span data-stu-id="2b937-129">This parameter is only available on SQL Database V12 servers.</span></span>

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

### <span data-ttu-id="2b937-130">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2b937-130">-DatabaseName</span></span>
<span data-ttu-id="2b937-131">Especifica o nome do banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="2b937-131">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="2b937-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b937-132">-DefaultProfile</span></span>
<span data-ttu-id="2b937-133">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="2b937-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b937-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b937-134">-ResourceGroupName</span></span>
<span data-ttu-id="2b937-135">Especifica o nome do grupo de recursos do servidor de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="2b937-135">Specifies the name of the resource group for the SQL Database server.</span></span>

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

### <span data-ttu-id="2b937-136">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="2b937-136">-ServerName</span></span>
<span data-ttu-id="2b937-137">Especifica o nome do servidor de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="2b937-137">Specifies the name of the SQL Database server.</span></span>

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

### <span data-ttu-id="2b937-138">-SqlServerResourceIdForPrivateLink</span><span class="sxs-lookup"><span data-stu-id="2b937-138">-SqlServerResourceIdForPrivateLink</span></span>
<span data-ttu-id="2b937-139">A ID de recurso do SQL Server para criar um link privado</span><span class="sxs-lookup"><span data-stu-id="2b937-139">The sql server resource id to create private link</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b937-140">-StorageAccountResourceIdForPrivateLink</span><span class="sxs-lookup"><span data-stu-id="2b937-140">-StorageAccountResourceIdForPrivateLink</span></span>
<span data-ttu-id="2b937-141">A ID do recurso da conta de armazenamento para criar um link privado</span><span class="sxs-lookup"><span data-stu-id="2b937-141">The storage account resource id to create private link</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b937-142">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="2b937-142">-StorageKey</span></span>
<span data-ttu-id="2b937-143">Especifica a tecla de acesso para a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="2b937-143">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="2b937-144">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="2b937-144">-StorageKeyType</span></span>
<span data-ttu-id="2b937-145">Especifica o tipo de tecla de acesso da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="2b937-145">Specifies the type of access key for the storage account.</span></span>
<span data-ttu-id="2b937-146">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="2b937-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2b937-147">StorageAccessKey.</span><span class="sxs-lookup"><span data-stu-id="2b937-147">StorageAccessKey.</span></span>
<span data-ttu-id="2b937-148">Esse valor usa uma chave de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="2b937-148">This value uses a storage account key.</span></span> 
- <span data-ttu-id="2b937-149">SharedAccessKey.</span><span class="sxs-lookup"><span data-stu-id="2b937-149">SharedAccessKey.</span></span>
<span data-ttu-id="2b937-150">Esse valor usa uma chave de assinatura de acesso compartilhado (SAS).</span><span class="sxs-lookup"><span data-stu-id="2b937-150">This value uses a Shared Access Signature (SAS) key.</span></span>

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

### <span data-ttu-id="2b937-151">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="2b937-151">-StorageUri</span></span>
<span data-ttu-id="2b937-152">Especifica o link de BLOB, como uma URL, para o arquivo. bacpac.</span><span class="sxs-lookup"><span data-stu-id="2b937-152">Specifies the blob link, as a URL, to the .bacpac file.</span></span>

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

### <span data-ttu-id="2b937-153">-UseNetworkIsolation</span><span class="sxs-lookup"><span data-stu-id="2b937-153">-UseNetworkIsolation</span></span>
<span data-ttu-id="2b937-154">Se definido, criará um link privado para a conta de armazenamento e/ou o SQL Server</span><span class="sxs-lookup"><span data-stu-id="2b937-154">If set, will create private link for storage account and/or SQL server</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b937-155">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2b937-155">-Confirm</span></span>
<span data-ttu-id="2b937-156">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b937-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b937-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b937-157">-WhatIf</span></span>
<span data-ttu-id="2b937-158">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2b937-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b937-159">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2b937-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b937-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b937-160">CommonParameters</span></span>
<span data-ttu-id="2b937-161">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b937-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b937-162">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2b937-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b937-163">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2b937-163">INPUTS</span></span>

### <span data-ttu-id="2b937-164">System. String</span><span class="sxs-lookup"><span data-stu-id="2b937-164">System.String</span></span>

## <span data-ttu-id="2b937-165">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2b937-165">OUTPUTS</span></span>

### <span data-ttu-id="2b937-166">Microsoft. Azure. Commands. Sql. ImportExport. Model. AzureSqlDatabaseImportExportBaseModel</span><span class="sxs-lookup"><span data-stu-id="2b937-166">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportBaseModel</span></span>

## <span data-ttu-id="2b937-167">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2b937-167">NOTES</span></span>
* <span data-ttu-id="2b937-168">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, SQL, Database, MSSQL</span><span class="sxs-lookup"><span data-stu-id="2b937-168">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="2b937-169">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2b937-169">RELATED LINKS</span></span>

[<span data-ttu-id="2b937-170">Get-AzSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="2b937-170">Get-AzSqlDatabaseImportExportStatus</span></span>](./Get-AzSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="2b937-171">New-AzSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="2b937-171">New-AzSqlDatabaseImport</span></span>](./New-AzSqlDatabaseImport.md)

[<span data-ttu-id="2b937-172">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="2b937-172">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
