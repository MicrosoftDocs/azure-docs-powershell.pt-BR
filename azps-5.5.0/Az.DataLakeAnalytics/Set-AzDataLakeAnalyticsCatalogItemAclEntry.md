---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticscatalogitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsCatalogItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsCatalogItemAclEntry.md
ms.openlocfilehash: ab02a118eab993174261fc1a70c2dedbd6403d5a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115407"
---
# <span data-ttu-id="4416d-101">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="4416d-101">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>

## <span data-ttu-id="4416d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4416d-102">SYNOPSIS</span></span>
<span data-ttu-id="4416d-103">Modifica uma entrada na ACL de um item de catálogo ou de catálogo no Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="4416d-103">Modifies an entry in the ACL of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="4416d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4416d-104">SYNTAX</span></span>

### <span data-ttu-id="4416d-105">SetCatalogAclEntryForUser (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4416d-105">SetCatalogAclEntryForUser (Default)</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid>
 -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4416d-106">SetCatalogItemAclEntryForUser</span><span class="sxs-lookup"><span data-stu-id="4416d-106">SetCatalogItemAclEntryForUser</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid> -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4416d-107">SetCatalogAclEntryForGroup</span><span class="sxs-lookup"><span data-stu-id="4416d-107">SetCatalogAclEntryForGroup</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid>
 -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4416d-108">SetCatalogItemAclEntryForGroup</span><span class="sxs-lookup"><span data-stu-id="4416d-108">SetCatalogItemAclEntryForGroup</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid> -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4416d-109">SetCatalogAclEntryForOther</span><span class="sxs-lookup"><span data-stu-id="4416d-109">SetCatalogAclEntryForOther</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Other] -Permissions <PermissionType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4416d-110">SetCatalogItemAclEntryForOther</span><span class="sxs-lookup"><span data-stu-id="4416d-110">SetCatalogItemAclEntryForOther</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Other] -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4416d-111">SetCatalogAclEntryForUserOwner</span><span class="sxs-lookup"><span data-stu-id="4416d-111">SetCatalogAclEntryForUserOwner</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner] -Permissions <PermissionType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4416d-112">SetCatalogItemAclEntryForUserOwner</span><span class="sxs-lookup"><span data-stu-id="4416d-112">SetCatalogItemAclEntryForUserOwner</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-UserOwner] -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4416d-113">SetCatalogAclEntryForGroupOwner</span><span class="sxs-lookup"><span data-stu-id="4416d-113">SetCatalogAclEntryForGroupOwner</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner] -Permissions <PermissionType>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4416d-114">SetCatalogItemAclEntryForGroupOwner</span><span class="sxs-lookup"><span data-stu-id="4416d-114">SetCatalogItemAclEntryForGroupOwner</span></span>
```
Set-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-GroupOwner] -ItemType <String>
 -Path <CatalogPathInstance> -Permissions <PermissionType> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4416d-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="4416d-115">DESCRIPTION</span></span>
<span data-ttu-id="4416d-116">O cmdlet **Set-AzDataLakeAnalyticsCatalogItemAclEntry** adiciona ou modifica uma entrada (ACE) na lista de controles de acesso (ACL) de um item de catálogo ou de catálogo no Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="4416d-116">The **Set-AzDataLakeAnalyticsCatalogItemAclEntry** cmdlet adds or modifies an entry (ACE) in the access control list (ACL) of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="4416d-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="4416d-117">EXAMPLES</span></span>

### <span data-ttu-id="4416d-118">Exemplo 1: Modificar permissões de usuário para um catálogo</span><span class="sxs-lookup"><span data-stu-id="4416d-118">Example 1: Modify user permissions for a catalog</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzADUser -Mail "PattiFuller@contoso.com").Id -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

<span data-ttu-id="4416d-119">Esse comando modifica o ace de catálogo para que Ela Tenha permissões de leitura.</span><span class="sxs-lookup"><span data-stu-id="4416d-119">This command modifies the catalog ACE for Patti Fuller to have read permissions.</span></span>

### <span data-ttu-id="4416d-120">Exemplo 2: Modificar permissões de usuário para um banco de dados</span><span class="sxs-lookup"><span data-stu-id="4416d-120">Example 2: Modify user Permissions for a database</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzADUser -Mail "PattiFuller@contoso.com").Id -ItemType Database -Path "databaseName" -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        None
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

<span data-ttu-id="4416d-121">Esse comando modifica o ACE do banco de dados para Que ele tenha permissões de leitura.</span><span class="sxs-lookup"><span data-stu-id="4416d-121">This command modifies the database ACE for Patti Fuller to have read permissions.</span></span>

### <span data-ttu-id="4416d-122">Exemplo 3: Modificar outras permissões para um catálogo</span><span class="sxs-lookup"><span data-stu-id="4416d-122">Example 3: Modify other permissions for a catalog</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -Other -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        Read
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

<span data-ttu-id="4416d-123">Esse comando modifica o ACE de catálogo para que outros tenham permissões de leitura.</span><span class="sxs-lookup"><span data-stu-id="4416d-123">This command modifies the catalog ACE for other to have read permissions.</span></span>

### <span data-ttu-id="4416d-124">Exemplo 4: Modificar outras permissões para um banco de dados</span><span class="sxs-lookup"><span data-stu-id="4416d-124">Example 4: Modify other Permissions for a database</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -Other -ItemType Database -Path "databaseName" -Permissions Read

Type  Id                                   Permissions
----  --                                   -----------
User  90a6f74b-fd73-490e-900a-c4f0f9694d02        Read
Group 902b155a-5601-4ca8-8178-ad3289211f88   ReadWrite
Other 00000000-0000-0000-0000-000000000000        Read
User  bd0b55bb-3a57-442a-b2f6-78c95c10ef86        Read
```

### <span data-ttu-id="4416d-125">Exemplo 5: Modificar permissões de proprietário do usuário para um catálogo</span><span class="sxs-lookup"><span data-stu-id="4416d-125">Example 5: Modify user owner permissions for a catalog</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner -Permissions Read

Type      Id                                   Permissions
----      --                                   -----------
UserOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc        Read
```

<span data-ttu-id="4416d-126">Esse comando define a permissão de proprietário da conta como Lida.</span><span class="sxs-lookup"><span data-stu-id="4416d-126">This command sets the owner permission for the account to Read.</span></span>

### <span data-ttu-id="4416d-127">Exemplo 6: Modificar permissões de proprietário do usuário para um banco de dados</span><span class="sxs-lookup"><span data-stu-id="4416d-127">Example 6: Modify user owner Permissions for a database</span></span>
```powershell
PS C:\> Set-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -UserOwner -ItemType Database -Path "databaseName" -Permissions Read

Type       Id                                   Permissions
----       --                                   -----------
GroupOwner 0316ac75-6703-4ace-984f-a4dd79aeeafc        Read
```

<span data-ttu-id="4416d-128">Esse comando define a permissão de proprietário do banco de dados como Lida.</span><span class="sxs-lookup"><span data-stu-id="4416d-128">This command sets the owner permission for the database to Read.</span></span>

## <span data-ttu-id="4416d-129">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4416d-129">PARAMETERS</span></span>

### <span data-ttu-id="4416d-130">-Conta</span><span class="sxs-lookup"><span data-stu-id="4416d-130">-Account</span></span>
<span data-ttu-id="4416d-131">Especifica o nome da conta do Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="4416d-131">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="4416d-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4416d-132">-DefaultProfile</span></span>
<span data-ttu-id="4416d-133">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4416d-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4416d-134">-Agrupar</span><span class="sxs-lookup"><span data-stu-id="4416d-134">-Group</span></span>
<span data-ttu-id="4416d-135">Definir a entrada ACL do catálogo para o grupo.</span><span class="sxs-lookup"><span data-stu-id="4416d-135">Set ACL entry of catalog for group.</span></span>

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

### <span data-ttu-id="4416d-136">-GroupOwner</span><span class="sxs-lookup"><span data-stu-id="4416d-136">-GroupOwner</span></span>
<span data-ttu-id="4416d-137">Definir a entrada ACL do catálogo para o proprietário do grupo.</span><span class="sxs-lookup"><span data-stu-id="4416d-137">Set ACL entry of catalog for group owner.</span></span>

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

### <span data-ttu-id="4416d-138">-ItemType</span><span class="sxs-lookup"><span data-stu-id="4416d-138">-ItemType</span></span>
<span data-ttu-id="4416d-139">Especifica o tipo de catálogo ou item de catálogo.</span><span class="sxs-lookup"><span data-stu-id="4416d-139">Specifies the type of the catalog or catalog item(s).</span></span> <span data-ttu-id="4416d-140">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="4416d-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4416d-141">Catálogo</span><span class="sxs-lookup"><span data-stu-id="4416d-141">Catalog</span></span>
- <span data-ttu-id="4416d-142">Database</span><span class="sxs-lookup"><span data-stu-id="4416d-142">Database</span></span>

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

### <span data-ttu-id="4416d-143">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="4416d-143">-ObjectId</span></span>
<span data-ttu-id="4416d-144">A identidade do usuário a ser definida.</span><span class="sxs-lookup"><span data-stu-id="4416d-144">The identity of the user to set.</span></span>

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

### <span data-ttu-id="4416d-145">-Outros</span><span class="sxs-lookup"><span data-stu-id="4416d-145">-Other</span></span>
<span data-ttu-id="4416d-146">Definir a entrada ACL do catálogo para outros.</span><span class="sxs-lookup"><span data-stu-id="4416d-146">Set ACL entry of catalog for other.</span></span>

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

### <span data-ttu-id="4416d-147">-Caminho</span><span class="sxs-lookup"><span data-stu-id="4416d-147">-Path</span></span>
<span data-ttu-id="4416d-148">Especifica o caminho do Data Lake Analytics de um catálogo ou item de catálogo.</span><span class="sxs-lookup"><span data-stu-id="4416d-148">Specifies the Data Lake Analytics path of an catalog or catalog item.</span></span>
<span data-ttu-id="4416d-149">As partes do caminho devem ser separadas por um ponto (.).</span><span class="sxs-lookup"><span data-stu-id="4416d-149">The parts of the path should be separated by a period (.).</span></span>

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

### <span data-ttu-id="4416d-150">-Permissões</span><span class="sxs-lookup"><span data-stu-id="4416d-150">-Permissions</span></span>
<span data-ttu-id="4416d-151">Especifica as permissões para o ACE.</span><span class="sxs-lookup"><span data-stu-id="4416d-151">Specifies the permissions for the ACE.</span></span>
<span data-ttu-id="4416d-152">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="4416d-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4416d-153">Nenhum</span><span class="sxs-lookup"><span data-stu-id="4416d-153">None</span></span>
- <span data-ttu-id="4416d-154">Ler</span><span class="sxs-lookup"><span data-stu-id="4416d-154">Read</span></span>
- <span data-ttu-id="4416d-155">Readwrite</span><span class="sxs-lookup"><span data-stu-id="4416d-155">ReadWrite</span></span>

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

### <span data-ttu-id="4416d-156">-Usuário</span><span class="sxs-lookup"><span data-stu-id="4416d-156">-User</span></span>
<span data-ttu-id="4416d-157">Definir a entrada ACL do catálogo para o usuário.</span><span class="sxs-lookup"><span data-stu-id="4416d-157">Set ACL entry of catalog for user.</span></span>

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

### <span data-ttu-id="4416d-158">-UserOwner</span><span class="sxs-lookup"><span data-stu-id="4416d-158">-UserOwner</span></span>
<span data-ttu-id="4416d-159">Definir a entrada ACL do catálogo para o proprietário do usuário.</span><span class="sxs-lookup"><span data-stu-id="4416d-159">Set ACL entry of catalog for user owner.</span></span>

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

### <span data-ttu-id="4416d-160">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="4416d-160">-Confirm</span></span>
<span data-ttu-id="4416d-161">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4416d-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4416d-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4416d-162">-WhatIf</span></span>
<span data-ttu-id="4416d-163">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="4416d-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4416d-164">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4416d-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4416d-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4416d-165">CommonParameters</span></span>
<span data-ttu-id="4416d-166">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4416d-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4416d-167">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4416d-167">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4416d-168">Entradas</span><span class="sxs-lookup"><span data-stu-id="4416d-168">INPUTS</span></span>

### <span data-ttu-id="4416d-169">System.String</span><span class="sxs-lookup"><span data-stu-id="4416d-169">System.String</span></span>

### <span data-ttu-id="4416d-170">System.Guid</span><span class="sxs-lookup"><span data-stu-id="4416d-170">System.Guid</span></span>

### <span data-ttu-id="4416d-171">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="4416d-171">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

### <span data-ttu-id="4416d-172">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+PermissionType</span><span class="sxs-lookup"><span data-stu-id="4416d-172">Microsoft.Azure.Commands.DataLakeAnalytics.Models.DataLakeAnalyticsEnums+PermissionType</span></span>

## <span data-ttu-id="4416d-173">Saídas</span><span class="sxs-lookup"><span data-stu-id="4416d-173">OUTPUTS</span></span>

### <span data-ttu-id="4416d-174">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl</span><span class="sxs-lookup"><span data-stu-id="4416d-174">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAcl</span></span>

## <span data-ttu-id="4416d-175">Notas</span><span class="sxs-lookup"><span data-stu-id="4416d-175">NOTES</span></span>

## <span data-ttu-id="4416d-176">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4416d-176">RELATED LINKS</span></span>

[<span data-ttu-id="4416d-177">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="4416d-177">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Get-AzDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="4416d-178">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="4416d-178">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Remove-AzDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="4416d-179">O U-SQL agora oferece controle de acesso em nível de banco de dados</span><span class="sxs-lookup"><span data-stu-id="4416d-179">U-SQL now offers database level access control</span></span>](https://github.com/Azure/AzureDataLake/blob/master/docs/Release_Notes/2016/2016_08_01/USQL_Release_Notes_2016_08_01.md#u-sql-now-offers-database-level-access-control)
