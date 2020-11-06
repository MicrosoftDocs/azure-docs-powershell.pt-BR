---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: A1327BC6-F090-490E-8DC2-2CC48A21C2C0
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabaseimport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseImport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseImport.md
ms.openlocfilehash: a571621f7129b5d402521462f3d8273f55d9303d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598898"
---
# <span data-ttu-id="3e115-101">New-AzSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="3e115-101">New-AzSqlDatabaseImport</span></span>

## <span data-ttu-id="3e115-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3e115-102">SYNOPSIS</span></span>
<span data-ttu-id="3e115-103">Importa um arquivo. bacpac e cria um novo banco de dados no servidor.</span><span class="sxs-lookup"><span data-stu-id="3e115-103">Imports a .bacpac file and create a new database on the server.</span></span>

## <span data-ttu-id="3e115-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3e115-104">SYNTAX</span></span>

```
New-AzSqlDatabaseImport -DatabaseName <String> -Edition <DatabaseEdition> -ServiceObjectiveName <String>
 -DatabaseMaxSizeBytes <Int64> [-ServerName] <String> -StorageKeyType <StorageKeyType> -StorageKey <String>
 -StorageUri <Uri> -AdministratorLogin <String> -AdministratorLoginPassword <SecureString>
 [-AuthenticationType <AuthenticationType>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e115-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3e115-105">DESCRIPTION</span></span>
<span data-ttu-id="3e115-106">O cmdlet **New-AzSqlDatabaseImport** importa um arquivo bacpac de uma conta de armazenamento do Azure para um novo banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="3e115-106">The **New-AzSqlDatabaseImport** cmdlet imports a bacpac file from an Azure storage account to a new Azure SQL Database.</span></span>
<span data-ttu-id="3e115-107">A solicitação de status de obtenção de banco de dados de importação pode ser enviada para recuperar informações de status para essa solicitação.</span><span class="sxs-lookup"><span data-stu-id="3e115-107">The get import database status request may be sent to retrieve status information for this request.</span></span>

## <span data-ttu-id="3e115-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3e115-108">EXAMPLES</span></span>

### <span data-ttu-id="3e115-109">Exemplo 1: criar uma solicitação de importação para um arquivo bacpac</span><span class="sxs-lookup"><span data-stu-id="3e115-109">Example 1: Create an import request for a bacpac file</span></span>
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

<span data-ttu-id="3e115-110">Esse comando cria uma solicitação de importação para importar um. bacpac para um novo banco de dados.</span><span class="sxs-lookup"><span data-stu-id="3e115-110">This command creates an import request to import a .bacpac to a new database.</span></span>

## <span data-ttu-id="3e115-111">OS</span><span class="sxs-lookup"><span data-stu-id="3e115-111">PARAMETERS</span></span>

### <span data-ttu-id="3e115-112">-AdministratorLogin</span><span class="sxs-lookup"><span data-stu-id="3e115-112">-AdministratorLogin</span></span>
<span data-ttu-id="3e115-113">Especifica o nome do administrador do SQL.</span><span class="sxs-lookup"><span data-stu-id="3e115-113">Specifies the name of the SQL administrator.</span></span>

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

### <span data-ttu-id="3e115-114">-AdministratorLoginPassword</span><span class="sxs-lookup"><span data-stu-id="3e115-114">-AdministratorLoginPassword</span></span>
<span data-ttu-id="3e115-115">Especifica a senha do administrador do SQL.</span><span class="sxs-lookup"><span data-stu-id="3e115-115">Specifies the password of the SQL administrator.</span></span>

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

### <span data-ttu-id="3e115-116">-AuthenticationType</span><span class="sxs-lookup"><span data-stu-id="3e115-116">-AuthenticationType</span></span>
<span data-ttu-id="3e115-117">Especifica o tipo de autenticação usado para acessar o servidor.</span><span class="sxs-lookup"><span data-stu-id="3e115-117">Specifies the type of authentication used to access the server.</span></span>
<span data-ttu-id="3e115-118">Esse parâmetro assume o padrão de SQL se nenhum tipo de autenticação for definido.</span><span class="sxs-lookup"><span data-stu-id="3e115-118">This parameter defaults to SQL if no authentication type is set.</span></span>
<span data-ttu-id="3e115-119">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="3e115-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3e115-120">Server.</span><span class="sxs-lookup"><span data-stu-id="3e115-120">SQL.</span></span>
<span data-ttu-id="3e115-121">Autenticação do SQL.</span><span class="sxs-lookup"><span data-stu-id="3e115-121">SQL authentication.</span></span>
<span data-ttu-id="3e115-122">Defina os parâmetros *AdministratorLogin* e *AdministratorLoginPassword* para o nome de usuário e a senha do administrador do SQL.</span><span class="sxs-lookup"><span data-stu-id="3e115-122">Set the *AdministratorLogin* and *AdministratorLoginPassword* parameters to the SQL administrator username and password.</span></span> 
- <span data-ttu-id="3e115-123">ADPassword.</span><span class="sxs-lookup"><span data-stu-id="3e115-123">ADPassword.</span></span>
<span data-ttu-id="3e115-124">Autenticação do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3e115-124">Azure Active Directory authentication.</span></span>
<span data-ttu-id="3e115-125">Defina *AdministratorLogin* e *AdministratorLoginPassword* para o nome de usuário e a senha de administrador do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="3e115-125">Set *AdministratorLogin* and *AdministratorLoginPassword* to the Azure Active Directory administrator username and password.</span></span>
<span data-ttu-id="3e115-126">Esse parâmetro só está disponível em servidores do banco de dados SQL V12.</span><span class="sxs-lookup"><span data-stu-id="3e115-126">This parameter is only available on SQL Database V12 servers.</span></span>

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

### <span data-ttu-id="3e115-127">-DatabaseMaxSizeBytes</span><span class="sxs-lookup"><span data-stu-id="3e115-127">-DatabaseMaxSizeBytes</span></span>
<span data-ttu-id="3e115-128">Especifica o tamanho máximo para o banco de dados recém importado.</span><span class="sxs-lookup"><span data-stu-id="3e115-128">Specifies the maximum size for the newly imported database.</span></span>

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

### <span data-ttu-id="3e115-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3e115-129">-DatabaseName</span></span>
<span data-ttu-id="3e115-130">Especifica o nome do banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="3e115-130">Specifies the name of the SQL Database.</span></span>

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

### <span data-ttu-id="3e115-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e115-131">-DefaultProfile</span></span>
<span data-ttu-id="3e115-132">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="3e115-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3e115-133">-Edição</span><span class="sxs-lookup"><span data-stu-id="3e115-133">-Edition</span></span>
<span data-ttu-id="3e115-134">Especifica a edição do novo banco de dados a ser importado.</span><span class="sxs-lookup"><span data-stu-id="3e115-134">Specifies the edition of the new database to import to.</span></span>
<span data-ttu-id="3e115-135">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="3e115-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3e115-136">Gratifica</span><span class="sxs-lookup"><span data-stu-id="3e115-136">Premium</span></span>
- <span data-ttu-id="3e115-137">Basic</span><span class="sxs-lookup"><span data-stu-id="3e115-137">Basic</span></span>
- <span data-ttu-id="3e115-138">Oficial</span><span class="sxs-lookup"><span data-stu-id="3e115-138">Standard</span></span>
- <span data-ttu-id="3e115-139">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="3e115-139">DataWarehouse</span></span>
- <span data-ttu-id="3e115-140">Gratuito</span><span class="sxs-lookup"><span data-stu-id="3e115-140">Free</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseEdition
Parameter Sets: (All)
Aliases:
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS, GeneralPurpose, BusinessCritical

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e115-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e115-141">-ResourceGroupName</span></span>
<span data-ttu-id="3e115-142">Especifica o nome do grupo de recursos do servidor de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="3e115-142">Specifies the name of the resource group for the SQL Database server.</span></span>

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

### <span data-ttu-id="3e115-143">-Nomedoservidor</span><span class="sxs-lookup"><span data-stu-id="3e115-143">-ServerName</span></span>
<span data-ttu-id="3e115-144">Especifica o nome do servidor de banco de dados SQL.</span><span class="sxs-lookup"><span data-stu-id="3e115-144">Specifies the name of the SQL Database server.</span></span>

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

### <span data-ttu-id="3e115-145">-Imobjecname</span><span class="sxs-lookup"><span data-stu-id="3e115-145">-ServiceObjectiveName</span></span>
<span data-ttu-id="3e115-146">Especifica o nome do objetivo de serviço a ser atribuído ao banco de dados SQL do Azure.</span><span class="sxs-lookup"><span data-stu-id="3e115-146">Specifies the name of the service objective to assign to the Azure SQL Database.</span></span>

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

### <span data-ttu-id="3e115-147">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="3e115-147">-StorageKey</span></span>
<span data-ttu-id="3e115-148">Especifica a tecla de acesso para a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="3e115-148">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="3e115-149">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="3e115-149">-StorageKeyType</span></span>
<span data-ttu-id="3e115-150">Especifica o tipo de tecla de acesso da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="3e115-150">Specifies the type of access key for the storage account.</span></span>
<span data-ttu-id="3e115-151">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="3e115-151">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3e115-152">StorageAccessKey.</span><span class="sxs-lookup"><span data-stu-id="3e115-152">StorageAccessKey.</span></span>
<span data-ttu-id="3e115-153">Usa a chave da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="3e115-153">Uses the storage account key.</span></span> 
- <span data-ttu-id="3e115-154">SharedAccessKey.</span><span class="sxs-lookup"><span data-stu-id="3e115-154">SharedAccessKey.</span></span>
<span data-ttu-id="3e115-155">Usa a chave de assinatura de acesso compartilhado (SAS).</span><span class="sxs-lookup"><span data-stu-id="3e115-155">Uses the Shared Access Signature (SAS) key.</span></span>

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

### <span data-ttu-id="3e115-156">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="3e115-156">-StorageUri</span></span>
<span data-ttu-id="3e115-157">Especifica o URI do blob do arquivo. bacpac.</span><span class="sxs-lookup"><span data-stu-id="3e115-157">Specifies the blob URI of the .bacpac file.</span></span>

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

### <span data-ttu-id="3e115-158">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3e115-158">-Confirm</span></span>
<span data-ttu-id="3e115-159">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e115-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e115-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e115-160">-WhatIf</span></span>
<span data-ttu-id="3e115-161">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3e115-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e115-162">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3e115-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e115-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e115-163">CommonParameters</span></span>
<span data-ttu-id="3e115-164">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e115-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e115-165">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3e115-165">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e115-166">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3e115-166">INPUTS</span></span>

### <span data-ttu-id="3e115-167">System. String</span><span class="sxs-lookup"><span data-stu-id="3e115-167">System.String</span></span>

## <span data-ttu-id="3e115-168">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3e115-168">OUTPUTS</span></span>

### <span data-ttu-id="3e115-169">Microsoft. Azure. Commands. Sql. ImportExport. Model. AzureSqlDatabaseImportExportBaseModel</span><span class="sxs-lookup"><span data-stu-id="3e115-169">Microsoft.Azure.Commands.Sql.ImportExport.Model.AzureSqlDatabaseImportExportBaseModel</span></span>

## <span data-ttu-id="3e115-170">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3e115-170">NOTES</span></span>
* <span data-ttu-id="3e115-171">Palavras-chave: Azure, azurerm, ARM, Resource, Management, Manager, SQL, Database, MSSQL</span><span class="sxs-lookup"><span data-stu-id="3e115-171">Keywords: azure, azurerm, arm, resource, management, manager, sql, database, mssql</span></span>

## <span data-ttu-id="3e115-172">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3e115-172">RELATED LINKS</span></span>

[<span data-ttu-id="3e115-173">Get-AzSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="3e115-173">Get-AzSqlDatabaseImportExportStatus</span></span>](./Get-AzSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="3e115-174">New-AzSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="3e115-174">New-AzSqlDatabaseExport</span></span>](./New-AzSqlDatabaseExport.md)

[<span data-ttu-id="3e115-175">Documentação do banco de dados SQL</span><span class="sxs-lookup"><span data-stu-id="3e115-175">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

