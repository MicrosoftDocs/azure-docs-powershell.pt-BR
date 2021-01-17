---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: A1327BC6-F090-490E-8DC2-2CC48A21C2C0
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabaseimport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseImport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseImport.md
ms.openlocfilehash: ab1fcfa9b050f795a464488df51768b95996eb8c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427970"
---
# <span data-ttu-id="54c13-101">New-AzSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="54c13-101">New-AzSqlDatabaseImport</span></span>

## <span data-ttu-id="54c13-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="54c13-102">SYNOPSIS</span></span>
<span data-ttu-id="54c13-103">Importa um arquivo. bacpac e cria um novo banco de dados no servidor.</span><span class="sxs-lookup"><span data-stu-id="54c13-103">Imports a .bacpac file and create a new database on the server.</span></span>

## <span data-ttu-id="54c13-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="54c13-104">SYNTAX</span></span>

```
New-AzSqlDatabaseImport -DatabaseName <String> -Edition <DatabaseEdition> -ServiceObjectiveName <String>
 -DatabaseMaxSizeBytes <Int64> [-ServerName] <String> -StorageKeyType <StorageKeyType> -StorageKey <String>
 -StorageUri <Uri> -AdministratorLogin <String> -AdministratorLoginPassword <SecureString>
 [-AuthenticationType <AuthenticationType>] [-UseNetworkIsolation <Boolean>]
 [-StorageAccountResourceIdForPrivateLink <String>] [-SqlServerResourceIdForPrivateLink <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="54c13-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="54c13-105">DESCRIPTION</span></span>
<span data-ttu-id="54c13-106">O cmdlet **New-AzSqlDatabaseImport** importa um arquivo bacpac de uma conta de armazenamento do Azure para um novo banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="54c13-106">The **New-AzSqlDatabaseImport** cmdlet imports a bacpac file from an Azure storage account to a new Azure SQL Database.</span></span>
<span data-ttu-id="54c13-107">A solicitação de status de obtenção de banco de dados de importação pode ser enviada para recuperar informações de status para essa solicitação.</span><span class="sxs-lookup"><span data-stu-id="54c13-107">The get import database status request may be sent to retrieve status information for this request.</span></span>

## <span data-ttu-id="54c13-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="54c13-108">EXAMPLES</span></span>

### <span data-ttu-id="54c13-109">Exemplo 1: criar uma solicitação de importação para um arquivo bacpac</span><span class="sxs-lookup"><span data-stu-id="54c13-109">Example 1: Create an import request for a bacpac file</span></span>
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

<span data-ttu-id="54c13-110">Esse comando cria uma solicitação de importação para importar um. bacpac para um novo banco de dados.</span><span class="sxs-lookup"><span data-stu-id="54c13-110">This command creates an import request to import a .bacpac to a new database.</span></span>

## <span data-ttu-id="54c13-111">OS</span><span class="sxs-lookup"><span data-stu-id="54c13-111">PARAMETERS</span></span>

### <span data-ttu-id="54c13-112">-AdministratorLogin</span><span class="sxs-lookup"><span data-stu-id="54c13-112">-AdministratorLogin</span></span>
<span data-ttu-id="54c13-113">Especifica o nome do administrador do SQL.</span><span class="sxs-lookup"><span data-stu-id="54c13-113">Specifies the name of the SQL administrator.</span></span>

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

### <span data-ttu-id="54c13-114">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="54c13-114">-AdministratorLoginPassword</span></span>
<span data-ttu-id="54c13-115">Especifica a senha do administrador do SQL.</span><span class="sxs-lookup"><span data-stu-id="54c13-115">Specifies the password of the SQL administrator.</span></span>

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

### <span data-ttu-id="54c13-116">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="54c13-116">-AuthenticationType</span></span>
<span data-ttu-id="54c13-117">Especifica o tipo de autenticação usado para acessar o servidor.</span><span class="sxs-lookup"><span data-stu-id="54c13-117">Specifies the type of authentication used to access the server.</span></span>
<span data-ttu-id="54c13-118">Esse parâmetro assume o padrão de SQL se nenhum tipo de autenticação for definido.</span><span class="sxs-lookup"><span data-stu-id="54c13-118">This parameter defaults to SQL if no authentication type is set.</span></span>
<span data-ttu-id="54c13-119">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="54c13-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="54c13-120">Server.</span><span class="sxs-lookup"><span data-stu-id="54c13-120">SQL.</span></span>
<span data-ttu-id="54c13-121">Autenticação do SQL.</span><span class="sxs-lookup"><span data-stu-id="54c13-121">SQL authentication.</span></span>
<span data-ttu-id="54c13-122">Defina os parâmetros *AdministratorLogin* e *AdministratorLoginPassword* para o nome de usuário e a senha do administrador do SQL.</span><span class="sxs-lookup"><span data-stu-id="54c13-122">Set the *AdministratorLogin* and *AdministratorLoginPassword* parameters to the SQL administrator username and password.</span></span> 
- <span data-ttu-id="54c13-123">ADPassword.</span><span class="sxs-lookup"><span data-stu-id="54c13-123">ADPassword.</span></span>
<span data-ttu-id="54c13-124">Autenticação do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="54c13-124">Azure Active Directory authentication.</span></span>
<span data-ttu-id="54c13-125">Defina *AdministratorLogin* e *AdministratorLoginPassword* para o nome de usuário e a senha de administrador do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="54c13-125">Set *AdministratorLogin* and *AdministratorLoginPassword* to the Azure Active Directory administrator username and password.</span></span>
<span data-ttu-id="54c13-126">Esse parâmetro só está disponível em servidores do banco de dados SQL V12.</span><span class="sxs-lookup"><span data-stu-id="54c13-126">This parameter is only available on SQL Database V12 servers.</span></span>

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

### <span data-ttu-id="54c13-127">-DatabaseMaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="54c13-127">-DatabaseMaxSizeBytes</span></span>
<span data-ttu-id="54c13-128">Especifica o tamanho máximo para o banco de dados recém importado.</span><span class="sxs-lookup"><span data-stu-id="54c13-128">Specifies the maximum size for the newly imported database.</span></span>

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

### <span data-ttu-id="54c13-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="54c13-129">-DatabaseName</span></span>
<span data-ttu-id="54c13-130">Especifica o nome do banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="54c13-130">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="54c13-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54c13-131">-DefaultProfile</span></span>
<span data-ttu-id="54c13-132">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="54c13-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="54c13-133">-Edição</span><span class="sxs-lookup"><span data-stu-id="54c13-133">-Edition</span></span>
<span data-ttu-id="54c13-134">Especifica a edição do novo banco de dados a ser importado.</span><span class="sxs-lookup"><span data-stu-id="54c13-134">Specifies the edition of the new database to import to.</span></span>
<span data-ttu-id="54c13-135">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="54c13-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="54c13-136">Gratifica</span><span class="sxs-lookup"><span data-stu-id="54c13-136">Premium</span></span>
- <span data-ttu-id="54c13-137">Basic</span><span class="sxs-lookup"><span data-stu-id="54c13-137">Basic</span></span>
- <span data-ttu-id="54c13-138">Oficial</span><span class="sxs-lookup"><span data-stu-id="54c13-138">Standard</span></span>
- <span data-ttu-id="54c13-139">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="54c13-139">DataWarehouse</span></span>
- <span data-ttu-id="54c13-140">Gratuito</span><span class="sxs-lookup"><span data-stu-id="54c13-140">Free</span></span>

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

### <span data-ttu-id="54c13-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54c13-141">-ResourceGroupName</span></span>
<span data-ttu-id="54c13-142">Especifica o nome do grupo de recursos do servidor de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="54c13-142">Specifies the name of the resource group for the SQL Database server.</span></span>

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

### <span data-ttu-id="54c13-143">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="54c13-143">-ServerName</span></span>
<span data-ttu-id="54c13-144">Especifica o nome do servidor de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="54c13-144">Specifies the name of the SQL Database server.</span></span>

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

### <span data-ttu-id="54c13-145">-Imobjecname</span><span class="sxs-lookup"><span data-stu-id="54c13-145">-ServiceObjectiveName</span></span>
<span data-ttu-id="54c13-146">Especifica o nome do objetivo de serviço a ser atribuído ao banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="54c13-146">Specifies the name of the service objective to assign to the Azure SQL Database.</span></span>

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

### <span data-ttu-id="54c13-147">-SqlServerResourceIdForPrivateLink</span><span class="sxs-lookup"><span data-stu-id="54c13-147">-SqlServerResourceIdForPrivateLink</span></span>
<span data-ttu-id="54c13-148">A ID de recurso do SQL Server para criar um link privado</span><span class="sxs-lookup"><span data-stu-id="54c13-148">The sql server resource id to create private link</span></span>

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

### <span data-ttu-id="54c13-149">-StorageAccountResourceIdForPrivateLink</span><span class="sxs-lookup"><span data-stu-id="54c13-149">-StorageAccountResourceIdForPrivateLink</span></span>
<span data-ttu-id="54c13-150">A ID do recurso da conta de armazenamento para criar um link privado</span><span class="sxs-lookup"><span data-stu-id="54c13-150">The storage account resource id to create private link</span></span>

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

### <span data-ttu-id="54c13-151">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="54c13-151">-StorageKey</span></span>
<span data-ttu-id="54c13-152">Especifica a tecla de acesso para a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="54c13-152">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="54c13-153">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="54c13-153">-StorageKeyType</span></span>
<span data-ttu-id="54c13-154">Especifica o tipo de tecla de acesso da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="54c13-154">Specifies the type of access key for the storage account.</span></span>
<span data-ttu-id="54c13-155">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="54c13-155">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="54c13-156">StorageAccessKey.</span><span class="sxs-lookup"><span data-stu-id="54c13-156">StorageAccessKey.</span></span>
<span data-ttu-id="54c13-157">Usa a chave da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="54c13-157">Uses the storage account key.</span></span> 
- <span data-ttu-id="54c13-158">SharedAccessKey.</span><span class="sxs-lookup"><span data-stu-id="54c13-158">SharedAccessKey.</span></span>
<span data-ttu-id="54c13-159">Usa a chave de assinatura de acesso compartilhado (SAS).</span><span class="sxs-lookup"><span data-stu-id="54c13-159">Uses the Shared Access Signature (SAS) key.</span></span>

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

### <span data-ttu-id="54c13-160">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="54c13-160">-StorageUri</span></span>
<span data-ttu-id="54c13-161">Especifica o URI do blob do arquivo. bacpac.</span><span class="sxs-lookup"><span data-stu-id="54c13-161">Specifies the blob URI of the .bacpac file.</span></span>

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

### <span data-ttu-id="54c13-162">-UseNetworkIsolation</span><span class="sxs-lookup"><span data-stu-id="54c13-162">-UseNetworkIsolation</span></span>
<span data-ttu-id="54c13-163">Se definido, criará um link privado para a conta de armazenamento e/ou o SQL Server</span><span class="sxs-lookup"><span data-stu-id="54c13-163">If set, will create private link for storage account and/or SQL server</span></span>

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

### <span data-ttu-id="54c13-164">-Confirme</span><span class="sxs-lookup"><span data-stu-id="54c13-164">-Confirm</span></span>
<span data-ttu-id="54c13-165">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54c13-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54c13-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54c13-166">-WhatIf</span></span>
<span data-ttu-id="54c13-167">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="54c13-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54c13-168">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="54c13-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54c13-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54c13-169">CommonParameters</span></span>
<span data-ttu-id="54c13-170">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54c13-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54c13-171">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="54c13-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54c13-172">SENSORES</span><span class="sxs-lookup"><span data-stu-id="54c13-172">INPUTS</span></span>

### <span data-ttu-id="54c13-173">System. String</span><span class="sxs-lookup"><span data-stu-id="54c13-173">System.String</span></span>

## <span data-ttu-id="54c13-174">EXIBE</span><span class="sxs-lookup"><span data-stu-id="54c13-174">OUTPUTS</span></span>

### <span data-ttu-id="54c13-175">Microsoft. Azure. Commands. Sql. ImportExport. Model. AzureSqlDatabaseImportExportBaseModel</span><span class="sxs-lookup"><span data-stu-id="54c13-175">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportBaseModel</span></span>

## <span data-ttu-id="54c13-176">INFORMA</span><span class="sxs-lookup"><span data-stu-id="54c13-176">NOTES</span></span>
* <span data-ttu-id="54c13-177">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, SQL, Database, MSSQL</span><span class="sxs-lookup"><span data-stu-id="54c13-177">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="54c13-178">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="54c13-178">RELATED LINKS</span></span>

[<span data-ttu-id="54c13-179">Get-AzSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="54c13-179">Get-AzSqlDatabaseImportExportStatus</span></span>](./Get-AzSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="54c13-180">New-AzSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="54c13-180">New-AzSqlDatabaseExport</span></span>](./New-AzSqlDatabaseExport.md)

[<span data-ttu-id="54c13-181">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="54c13-181">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

