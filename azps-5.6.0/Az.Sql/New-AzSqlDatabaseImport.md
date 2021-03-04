---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: A1327BC6-F090-490E-8DC2-2CC48A21C2C0
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqldatabaseimport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseImport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseImport.md
ms.openlocfilehash: e0f23e1d41e27e7e16cf9a1cbead42a979f73eed
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888785"
---
# <span data-ttu-id="3ca51-101">New-AzSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="3ca51-101">New-AzSqlDatabaseImport</span></span>

## <span data-ttu-id="3ca51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ca51-102">SYNOPSIS</span></span>
<span data-ttu-id="3ca51-103">Importa um arquivo .bacpac e cria um novo banco de dados no servidor.</span><span class="sxs-lookup"><span data-stu-id="3ca51-103">Imports a .bacpac file and create a new database on the server.</span></span>

## <span data-ttu-id="3ca51-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="3ca51-104">SYNTAX</span></span>

```
New-AzSqlDatabaseImport -DatabaseName <String> -Edition <DatabaseEdition> -ServiceObjectiveName <String>
 -DatabaseMaxSizeBytes <Int64> [-ServerName] <String> -StorageKeyType <StorageKeyType> -StorageKey <String>
 -StorageUri <Uri> -AdministratorLogin <String> -AdministratorLoginPassword <SecureString>
 [-AuthenticationType <AuthenticationType>] [-UseNetworkIsolation <Boolean>]
 [-StorageAccountResourceIdForPrivateLink <String>] [-SqlServerResourceIdForPrivateLink <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3ca51-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3ca51-105">DESCRIPTION</span></span>
<span data-ttu-id="3ca51-106">O cmdlet **New-AzSqlDatabaseImport** importa um arquivo bacpac de uma conta de armazenamento do Azure para um novo banco de dados do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="3ca51-106">The **New-AzSqlDatabaseImport** cmdlet imports a bacpac file from an Azure storage account to a new Azure SQL Database.</span></span>
<span data-ttu-id="3ca51-107">A solicitação de status do banco de dados de importação pode ser enviada para recuperar informações de status para essa solicitação.</span><span class="sxs-lookup"><span data-stu-id="3ca51-107">The get import database status request may be sent to retrieve status information for this request.</span></span>

## <span data-ttu-id="3ca51-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3ca51-108">EXAMPLES</span></span>

### <span data-ttu-id="3ca51-109">Exemplo 1: Criar uma solicitação de importação para um arquivo bacpac</span><span class="sxs-lookup"><span data-stu-id="3ca51-109">Example 1: Create an import request for a bacpac file</span></span>
```
PS C:\>New-AzSqlDatabaseImport -ResourceGroupName "RG01" -ServerName "Server01" -DatabaseName "Database01" -StorageKeyType "StorageAccessKey" -StorageKey "StorageKey01" -StorageUri "http://account01.blob.core.contoso.net/bacpacs/database01.bacpac" -AdministratorLogin "User" -AdministratorLoginPassword $SecureString -Edition Standard -ServiceObjectiveName S0 -DatabaseMaxSizeBytes 5000000
ResourceGroupName          : RG01
ServerName                 : Server01
DatabaseName               : Database01
StorageKeyType             : StorageAccessKey
StorageKey                 : 
StorageUri                 : http://account01.blob.core.contoso.net/bacpacs/database01.bacpac
AdministratorLogin         : User
AdministratorLoginPassword : 
AuthenticationType         : None
OperationStatusLink        : https://management.contoso.com/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/resource01/providers/Microsoft.Sql/servers/server01/databases/database01/importExportOperationResults/00000000-00
                             0-0000-0000-000000000000?api-version=2014-04-01
Status                     : InProgress
ErrorMessage               :
```

<span data-ttu-id="3ca51-110">Este comando cria uma solicitação de importação para importar um .bacpac para um novo banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3ca51-110">This command creates an import request to import a .bacpac to a new database.</span></span>

## <span data-ttu-id="3ca51-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="3ca51-111">PARAMETERS</span></span>

### <span data-ttu-id="3ca51-112">-AdministratorLogin</span><span class="sxs-lookup"><span data-stu-id="3ca51-112">-AdministratorLogin</span></span>
<span data-ttu-id="3ca51-113">Especifica o nome do SQL administrador.</span><span class="sxs-lookup"><span data-stu-id="3ca51-113">Specifies the name of the SQL administrator.</span></span>

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

### <span data-ttu-id="3ca51-114">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="3ca51-114">-AdministratorLoginPassword</span></span>
<span data-ttu-id="3ca51-115">Especifica a senha do SQL administrador.</span><span class="sxs-lookup"><span data-stu-id="3ca51-115">Specifies the password of the SQL administrator.</span></span>

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

### <span data-ttu-id="3ca51-116">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="3ca51-116">-AuthenticationType</span></span>
<span data-ttu-id="3ca51-117">Especifica o tipo de autenticação usada para acessar o servidor.</span><span class="sxs-lookup"><span data-stu-id="3ca51-117">Specifies the type of authentication used to access the server.</span></span>
<span data-ttu-id="3ca51-118">Esse parâmetro é padrão para SQL se nenhum tipo de autenticação estiver definido.</span><span class="sxs-lookup"><span data-stu-id="3ca51-118">This parameter defaults to SQL if no authentication type is set.</span></span>
<span data-ttu-id="3ca51-119">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="3ca51-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3ca51-120">SQL.</span><span class="sxs-lookup"><span data-stu-id="3ca51-120">SQL.</span></span>
<span data-ttu-id="3ca51-121">SQL autenticação.</span><span class="sxs-lookup"><span data-stu-id="3ca51-121">SQL authentication.</span></span>
<span data-ttu-id="3ca51-122">De definir *os parâmetros AdministratorLogin* e *AdministratorLoginPassword* como o nome de usuário e a senha SQL administrador.</span><span class="sxs-lookup"><span data-stu-id="3ca51-122">Set the *AdministratorLogin* and *AdministratorLoginPassword* parameters to the SQL administrator username and password.</span></span> 
- <span data-ttu-id="3ca51-123">ADPassword.</span><span class="sxs-lookup"><span data-stu-id="3ca51-123">ADPassword.</span></span>
<span data-ttu-id="3ca51-124">Autenticação do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3ca51-124">Azure Active Directory authentication.</span></span>
<span data-ttu-id="3ca51-125">De *set AdministratorLogin* and *AdministratorLoginPassword* to the Azure Active Directory administrator username and password.</span><span class="sxs-lookup"><span data-stu-id="3ca51-125">Set *AdministratorLogin* and *AdministratorLoginPassword* to the Azure Active Directory administrator username and password.</span></span>
<span data-ttu-id="3ca51-126">Esse parâmetro só está disponível em servidores V12 SQL Banco de Dados.</span><span class="sxs-lookup"><span data-stu-id="3ca51-126">This parameter is only available on SQL Database V12 servers.</span></span>

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

### <span data-ttu-id="3ca51-127">-DatabaseMaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="3ca51-127">-DatabaseMaxSizeBytes</span></span>
<span data-ttu-id="3ca51-128">Especifica o tamanho máximo do banco de dados recém-importado.</span><span class="sxs-lookup"><span data-stu-id="3ca51-128">Specifies the maximum size for the newly imported database.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ca51-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3ca51-129">-DatabaseName</span></span>
<span data-ttu-id="3ca51-130">Especifica o nome do banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="3ca51-130">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="3ca51-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ca51-131">-DefaultProfile</span></span>
<span data-ttu-id="3ca51-132">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="3ca51-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3ca51-133">-Edition</span><span class="sxs-lookup"><span data-stu-id="3ca51-133">-Edition</span></span>
<span data-ttu-id="3ca51-134">Especifica a edição do novo banco de dados a ser importado.</span><span class="sxs-lookup"><span data-stu-id="3ca51-134">Specifies the edition of the new database to import to.</span></span>
<span data-ttu-id="3ca51-135">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="3ca51-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3ca51-136">Premium</span><span class="sxs-lookup"><span data-stu-id="3ca51-136">Premium</span></span>
- <span data-ttu-id="3ca51-137">Básico</span><span class="sxs-lookup"><span data-stu-id="3ca51-137">Basic</span></span>
- <span data-ttu-id="3ca51-138">Standard</span><span class="sxs-lookup"><span data-stu-id="3ca51-138">Standard</span></span>
- <span data-ttu-id="3ca51-139">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="3ca51-139">DataWarehouse</span></span>
- <span data-ttu-id="3ca51-140">Gratuito</span><span class="sxs-lookup"><span data-stu-id="3ca51-140">Free</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseEdition
Parameter Sets: (All)
Aliases:
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS, GeneralPurpose, BusinessCritical, Hyperscale

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ca51-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ca51-141">-ResourceGroupName</span></span>
<span data-ttu-id="3ca51-142">Especifica o nome do grupo de recursos do servidor SQL Database.</span><span class="sxs-lookup"><span data-stu-id="3ca51-142">Specifies the name of the resource group for the SQL Database server.</span></span>

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

### <span data-ttu-id="3ca51-143">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3ca51-143">-ServerName</span></span>
<span data-ttu-id="3ca51-144">Especifica o nome do servidor SQL Banco de Dados.</span><span class="sxs-lookup"><span data-stu-id="3ca51-144">Specifies the name of the SQL Database server.</span></span>

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

### <span data-ttu-id="3ca51-145">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="3ca51-145">-ServiceObjectiveName</span></span>
<span data-ttu-id="3ca51-146">Especifica o nome do objetivo do serviço a ser atribuído ao banco de dados do Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="3ca51-146">Specifies the name of the service objective to assign to the Azure SQL Database.</span></span>

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

### <span data-ttu-id="3ca51-147">-SqlServerResourceIdForPrivateLink</span><span class="sxs-lookup"><span data-stu-id="3ca51-147">-SqlServerResourceIdForPrivateLink</span></span>
<span data-ttu-id="3ca51-148">A ID de recurso do sql Server para criar um link privado</span><span class="sxs-lookup"><span data-stu-id="3ca51-148">The sql server resource id to create private link</span></span>

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

### <span data-ttu-id="3ca51-149">-StorageAccountResourceIdForPrivateLink</span><span class="sxs-lookup"><span data-stu-id="3ca51-149">-StorageAccountResourceIdForPrivateLink</span></span>
<span data-ttu-id="3ca51-150">A ID do recurso de conta de armazenamento para criar um link privado</span><span class="sxs-lookup"><span data-stu-id="3ca51-150">The storage account resource id to create private link</span></span>

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

### <span data-ttu-id="3ca51-151">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="3ca51-151">-StorageKey</span></span>
<span data-ttu-id="3ca51-152">Especifica a chave de acesso para a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="3ca51-152">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="3ca51-153">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="3ca51-153">-StorageKeyType</span></span>
<span data-ttu-id="3ca51-154">Especifica o tipo de chave de acesso para a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="3ca51-154">Specifies the type of access key for the storage account.</span></span>
<span data-ttu-id="3ca51-155">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="3ca51-155">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3ca51-156">StorageAccessKey.</span><span class="sxs-lookup"><span data-stu-id="3ca51-156">StorageAccessKey.</span></span>
<span data-ttu-id="3ca51-157">Usa a chave da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="3ca51-157">Uses the storage account key.</span></span> 
- <span data-ttu-id="3ca51-158">SharedAccessKey.</span><span class="sxs-lookup"><span data-stu-id="3ca51-158">SharedAccessKey.</span></span>
<span data-ttu-id="3ca51-159">Usa a chave SAS (Assinatura de Acesso Compartilhado).</span><span class="sxs-lookup"><span data-stu-id="3ca51-159">Uses the Shared Access Signature (SAS) key.</span></span>

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

### <span data-ttu-id="3ca51-160">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="3ca51-160">-StorageUri</span></span>
<span data-ttu-id="3ca51-161">Especifica o URI blob do arquivo .bacpac.</span><span class="sxs-lookup"><span data-stu-id="3ca51-161">Specifies the blob URI of the .bacpac file.</span></span>

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

### <span data-ttu-id="3ca51-162">-UseNetworkIsolation</span><span class="sxs-lookup"><span data-stu-id="3ca51-162">-UseNetworkIsolation</span></span>
<span data-ttu-id="3ca51-163">Se definido, criará link privado para conta de armazenamento e/ou SQL servidor</span><span class="sxs-lookup"><span data-stu-id="3ca51-163">If set, will create private link for storage account and/or SQL server</span></span>

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

### <span data-ttu-id="3ca51-164">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3ca51-164">-Confirm</span></span>
<span data-ttu-id="3ca51-165">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ca51-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ca51-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ca51-166">-WhatIf</span></span>
<span data-ttu-id="3ca51-167">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3ca51-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ca51-168">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3ca51-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ca51-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ca51-169">CommonParameters</span></span>
<span data-ttu-id="3ca51-170">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ca51-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ca51-171">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3ca51-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ca51-172">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3ca51-172">INPUTS</span></span>

### <span data-ttu-id="3ca51-173">System.String</span><span class="sxs-lookup"><span data-stu-id="3ca51-173">System.String</span></span>

## <span data-ttu-id="3ca51-174">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="3ca51-174">OUTPUTS</span></span>

### <span data-ttu-id="3ca51-175">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportBaseModel</span><span class="sxs-lookup"><span data-stu-id="3ca51-175">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportBaseModel</span></span>

## <span data-ttu-id="3ca51-176">NOTES</span><span class="sxs-lookup"><span data-stu-id="3ca51-176">NOTES</span></span>
* <span data-ttu-id="3ca51-177">Palavras-chave: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span><span class="sxs-lookup"><span data-stu-id="3ca51-177">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="3ca51-178">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3ca51-178">RELATED LINKS</span></span>

[<span data-ttu-id="3ca51-179">Get-AzSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="3ca51-179">Get-AzSqlDatabaseImportExportStatus</span></span>](./Get-AzSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="3ca51-180">New-AzSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="3ca51-180">New-AzSqlDatabaseExport</span></span>](./New-AzSqlDatabaseExport.md)

[<span data-ttu-id="3ca51-181">SQL documentação do banco de dados</span><span class="sxs-lookup"><span data-stu-id="3ca51-181">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

