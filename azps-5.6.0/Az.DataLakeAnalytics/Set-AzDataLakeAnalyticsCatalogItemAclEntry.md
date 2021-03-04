---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticscatalogitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsCatalogItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsCatalogItemAclEntry.md
ms.openlocfilehash: a4569f8ce570a537896c4c39b916aca271111f06
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890441"
---
# <span data-ttu-id="b8e4a-101">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="b8e4a-101">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>

## <span data-ttu-id="b8e4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8e4a-102">SYNOPSIS</span></span>
<span data-ttu-id="b8e4a-103">Modifica uma entrada na ACL de um item de catálogo ou catálogo no Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="b8e4a-103">Modifies an entry in the ACL of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="b8e4a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b8e4a-104">SYNTAX</span></span>

### <span data-ttu-id="b8e4a-105">SetCatalogAclEntryForUser (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b8e4a-105">SetCatalogAclEntryForUser (Default)</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid>
 -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b8e4a-106">SetCatalogItemAclEntryForUser</span><span class="sxs-lookup"><span data-stu-id="b8e4a-106">SetCatalogItemAclEntryForUser</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid> -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8e4a-107">SetCatalogAclEntryForGroup</span><span class="sxs-lookup"><span data-stu-id="b8e4a-107">SetCatalogAclEntryForGroup</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid>
 -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b8e4a-108">SetCatalogItemAclEntryForGroup</span><span class="sxs-lookup"><span data-stu-id="b8e4a-108">SetCatalogItemAclEntryForGroup</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid> -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8e4a-109">SetCatalogAclEntryForOther</span><span class="sxs-lookup"><span data-stu-id="b8e4a-109">SetCatalogAclEntryForOther</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Other] -Permissions <PermissionType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8e4a-110">SetCatalogItemAclEntryForOther</span><span class="sxs-lookup"><span data-stu-id="b8e4a-110">SetCatalogItemAclEntryForOther</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Other] -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8e4a-111">SetCatalogAclEntryForUserOwner</span><span class="sxs-lookup"><span data-stu-id="b8e4a-111">SetCatalogAclEntryForUserOwner</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner] -Permissions <PermissionType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8e4a-112">SetCatalogItemAclEntryForUserOwner</span><span class="sxs-lookup"><span data-stu-id="b8e4a-112">SetCatalogItemAclEntryForUserOwner</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner] -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8e4a-113">SetCatalogAclEntryForGroupOwner</span><span class="sxs-lookup"><span data-stu-id="b8e4a-113">SetCatalogAclEntryForGroupOwner</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner] -Permissions <PermissionType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8e4a-114">SetCatalogItemAclEntryForGroupOwner</span><span class="sxs-lookup"><span data-stu-id="b8e4a-114">SetCatalogItemAclEntryForGroupOwner</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner] -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8e4a-115">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b8e4a-115">DESCRIPTION</span></span>
<span data-ttu-id="b8e4a-116">O cmdlet **Set-AzDataLakeAnalyticsCatalogItemAclEntry** adiciona ou modifica uma entrada (ACE) na lista de controles de acesso (ACL) de um item de catálogo ou catálogo no Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="b8e4a-116">The **Set-AzDataLakeAnalyticsCatalogItemAclEntry** cmdlet adds or modifies an entry (ACE) in the access control list (ACL) of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="b8e4a-117">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b8e4a-117">EXAMPLES</span></span>

### <span data-ttu-id="b8e4a-118">Exemplo 1: Modificar permissões de usuário para um catálogo</span><span class="sxs-lookup"><span data-stu-id="b8e4a-118">Example 1: Modify user permissions for a catalog</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzADUser -Mail "PattiFuller@contoso.com").Id -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

<span data-ttu-id="b8e4a-119">Este comando modifica o ACE do catálogo para Patti Fuller ter permissões de leitura.</span><span class="sxs-lookup"><span data-stu-id="b8e4a-119">This command modifies the catalog ACE for Patti Fuller to have read permissions.</span></span>

### <span data-ttu-id="b8e4a-120">Exemplo 2: Modificar permissões de usuário para um banco de dados</span><span class="sxs-lookup"><span data-stu-id="b8e4a-120">Example 2: Modify user Permissions for a database</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzADUser -Mail "PattiFuller@contoso.com").Id -ItemType Database -Path "databaseName" -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

<span data-ttu-id="b8e4a-121">Este comando modifica o ACE do banco de dados para Patti Fuller ter permissões de leitura.</span><span class="sxs-lookup"><span data-stu-id="b8e4a-121">This command modifies the database ACE for Patti Fuller to have read permissions.</span></span>

### <span data-ttu-id="b8e4a-122">Exemplo 3: Modificar outras permissões para um catálogo</span><span class="sxs-lookup"><span data-stu-id="b8e4a-122">Example 3: Modify other permissions for a catalog</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -Other -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        Read
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

<span data-ttu-id="b8e4a-123">Este comando modifica o ACE do catálogo para que outros tenham permissões de leitura.</span><span class="sxs-lookup"><span data-stu-id="b8e4a-123">This command modifies the catalog ACE for other to have read permissions.</span></span>

### <span data-ttu-id="b8e4a-124">Exemplo 4: Modificar outras permissões para um banco de dados</span><span class="sxs-lookup"><span data-stu-id="b8e4a-124">Example 4: Modify other Permissions for a database</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -Other -ItemType Database -Path "databaseName" -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        Read
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

### <span data-ttu-id="b8e4a-125">Exemplo 5: Modificar permissões de proprietário do usuário para um catálogo</span><span class="sxs-lookup"><span data-stu-id="b8e4a-125">Example 5: Modify user owner permissions for a catalog</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner -Permissions Read

Type      Id                                   Permissions
----      --                                   -----------
UserOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc        Read
```

<span data-ttu-id="b8e4a-126">Este comando define a permissão do proprietário da conta como Read.</span><span class="sxs-lookup"><span data-stu-id="b8e4a-126">This command sets the owner permission for the account to Read.</span></span>

### <span data-ttu-id="b8e4a-127">Exemplo 6: Modificar permissões do proprietário do usuário para um banco de dados</span><span class="sxs-lookup"><span data-stu-id="b8e4a-127">Example 6: Modify user owner Permissions for a database</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner -ItemType Database -Path "databaseName" -Permissions Read

Type       Id                                   Permissions
----       --                                   -----------
GroupOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc        Read
```

<span data-ttu-id="b8e4a-128">Este comando define a permissão do proprietário do banco de dados como Leitura.</span><span class="sxs-lookup"><span data-stu-id="b8e4a-128">This command sets the owner permission for the database to Read.</span></span>

## <span data-ttu-id="b8e4a-129">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b8e4a-129">PARAMETERS</span></span>

### <span data-ttu-id="b8e4a-130">-Account</span><span class="sxs-lookup"><span data-stu-id="b8e4a-130">-Account</span></span>
<span data-ttu-id="b8e4a-131">Especifica o nome da conta do Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="b8e4a-131">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8e4a-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8e4a-132">-DefaultProfile</span></span>
<span data-ttu-id="b8e4a-133">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b8e4a-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8e4a-134">-Group</span><span class="sxs-lookup"><span data-stu-id="b8e4a-134">-Group</span></span>
<span data-ttu-id="b8e4a-135">Definir a entrada ACL do catálogo para o grupo.</span><span class="sxs-lookup"><span data-stu-id="b8e4a-135">Set ACL entry of catalog for group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetCatalogAclEntryForGroup, SetCatalogItemAclEntryForGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8e4a-136">-GroupOwner</span><span class="sxs-lookup"><span data-stu-id="b8e4a-136">-GroupOwner</span></span>
<span data-ttu-id="b8e4a-137">Definir a entrada ACL do catálogo para o proprietário do grupo.</span><span class="sxs-lookup"><span data-stu-id="b8e4a-137">Set ACL entry of catalog for group owner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetCatalogAclEntryForGroupOwner, SetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8e4a-138">-ItemType</span><span class="sxs-lookup"><span data-stu-id="b8e4a-138">-ItemType</span></span>
<span data-ttu-id="b8e4a-139">Especifica o tipo de catálogo ou item de catálogo.</span><span class="sxs-lookup"><span data-stu-id="b8e4a-139">Specifies the type of the catalog or catalog item(s).</span></span> <span data-ttu-id="b8e4a-140">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="b8e4a-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b8e4a-141">Catálogo</span><span class="sxs-lookup"><span data-stu-id="b8e4a-141">Catalog</span></span>
- <span data-ttu-id="b8e4a-142">Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="b8e4a-142">Database</span></span>

```yaml
Type: System.String
Parameter Sets: SetCatalogItemAclEntryForUser, SetCatalogItemAclEntryForGroup, SetCatalogItemAclEntryForOther, SetCatalogItemAclEntryForUserOwner, SetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8e4a-143">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="b8e4a-143">-ObjectId</span></span>
<span data-ttu-id="b8e4a-144">A identidade do usuário a ser definida.</span><span class="sxs-lookup"><span data-stu-id="b8e4a-144">The identity of the user to set.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SetCatalogAclEntryForUser, SetCatalogItemAclEntryForUser, SetCatalogAclEntryForGroup, SetCatalogItemAclEntryForGroup
Aliases: Id, UserId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8e4a-145">-Other</span><span class="sxs-lookup"><span data-stu-id="b8e4a-145">-Other</span></span>
<span data-ttu-id="b8e4a-146">Definir a entrada ACL do catálogo para outro.</span><span class="sxs-lookup"><span data-stu-id="b8e4a-146">Set ACL entry of catalog for other.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetCatalogAclEntryForOther, SetCatalogItemAclEntryForOther
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8e4a-147">-Path</span><span class="sxs-lookup"><span data-stu-id="b8e4a-147">-Path</span></span>
<span data-ttu-id="b8e4a-148">Especifica o caminho do Data Lake Analytics de um catálogo ou item de catálogo.</span><span class="sxs-lookup"><span data-stu-id="b8e4a-148">Specifies the Data Lake Analytics path of an catalog or catalog item.</span></span>
<span data-ttu-id="b8e4a-149">As partes do caminho devem ser separadas por um ponto (.).</span><span class="sxs-lookup"><span data-stu-id="b8e4a-149">The parts of the path should be separated by a period (.).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance
Parameter Sets: SetCatalogItemAclEntryForUser, SetCatalogItemAclEntryForGroup, SetCatalogItemAclEntryForOther, SetCatalogItemAclEntryForUserOwner, SetCatalogItemAclEntryForGroupOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8e4a-150">-Permissões</span><span class="sxs-lookup"><span data-stu-id="b8e4a-150">-Permissions</span></span>
<span data-ttu-id="b8e4a-151">Especifica as permissões para o ACE.</span><span class="sxs-lookup"><span data-stu-id="b8e4a-151">Specifies the permissions for the ACE.</span></span>
<span data-ttu-id="b8e4a-152">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="b8e4a-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b8e4a-153">Nenhum</span><span class="sxs-lookup"><span data-stu-id="b8e4a-153">None</span></span>
- <span data-ttu-id="b8e4a-154">Leitura</span><span class="sxs-lookup"><span data-stu-id="b8e4a-154">Read</span></span>
- <span data-ttu-id="b8e4a-155">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="b8e4a-155">ReadWrite</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+PermissionType
Parameter Sets: (All)
Aliases:
Accepted values: None, Read, ReadWrite

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8e4a-156">-User</span><span class="sxs-lookup"><span data-stu-id="b8e4a-156">-User</span></span>
<span data-ttu-id="b8e4a-157">Definir a entrada ACL do catálogo para o usuário.</span><span class="sxs-lookup"><span data-stu-id="b8e4a-157">Set ACL entry of catalog for user.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetCatalogAclEntryForUser, SetCatalogItemAclEntryForUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8e4a-158">-UserOwner</span><span class="sxs-lookup"><span data-stu-id="b8e4a-158">-UserOwner</span></span>
<span data-ttu-id="b8e4a-159">Definir a entrada ACL do catálogo para o proprietário do usuário.</span><span class="sxs-lookup"><span data-stu-id="b8e4a-159">Set ACL entry of catalog for user owner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetCatalogAclEntryForUserOwner, SetCatalogItemAclEntryForUserOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8e4a-160">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b8e4a-160">-Confirm</span></span>
<span data-ttu-id="b8e4a-161">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8e4a-161">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8e4a-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8e4a-162">-WhatIf</span></span>
<span data-ttu-id="b8e4a-163">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b8e4a-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8e4a-164">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b8e4a-164">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8e4a-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8e4a-165">CommonParameters</span></span>
<span data-ttu-id="b8e4a-166">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8e4a-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8e4a-167">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8e4a-167">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8e4a-168">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b8e4a-168">INPUTS</span></span>

### <span data-ttu-id="b8e4a-169">System.String</span><span class="sxs-lookup"><span data-stu-id="b8e4a-169">System.String</span></span>

### <span data-ttu-id="b8e4a-170">System.Guid</span><span class="sxs-lookup"><span data-stu-id="b8e4a-170">System.Guid</span></span>

### <span data-ttu-id="b8e4a-171">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="b8e4a-171">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

### <span data-ttu-id="b8e4a-172">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+PermissionType</span><span class="sxs-lookup"><span data-stu-id="b8e4a-172">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+PermissionType</span></span>

## <span data-ttu-id="b8e4a-173">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b8e4a-173">OUTPUTS</span></span>

### <span data-ttu-id="b8e4a-174">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl</span><span class="sxs-lookup"><span data-stu-id="b8e4a-174">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl</span></span>

## <span data-ttu-id="b8e4a-175">NOTES</span><span class="sxs-lookup"><span data-stu-id="b8e4a-175">NOTES</span></span>

## <span data-ttu-id="b8e4a-176">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b8e4a-176">RELATED LINKS</span></span>

[<span data-ttu-id="b8e4a-177">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="b8e4a-177">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Get-AzDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="b8e4a-178">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="b8e4a-178">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Remove-AzDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="b8e4a-179">O U-SQL agora oferece controle de acesso de nível de banco de dados</span><span class="sxs-lookup"><span data-stu-id="b8e4a-179">U-SQL now offers database level access control</span></span>](https://github.com/Azure/AzureDataLake/blob/master/docs/Release_Notes/2016/2016_08_01/USQL_Release_Notes_2016_08_01.md#u-sql-now-offers-database-level-access-control)
