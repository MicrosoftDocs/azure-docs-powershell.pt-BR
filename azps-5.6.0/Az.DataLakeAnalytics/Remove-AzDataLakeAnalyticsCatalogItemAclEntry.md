---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticscatalogitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsCatalogItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsCatalogItemAclEntry.md
ms.openlocfilehash: 968acf65d0f3e045614b5ade094bb50c90acac46
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886778"
---
# <span data-ttu-id="787f0-101">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="787f0-101">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>

## <span data-ttu-id="787f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="787f0-102">SYNOPSIS</span></span>
<span data-ttu-id="787f0-103">Exclui uma entrada da ACL de um item de catálogo ou catálogo no Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="787f0-103">Deletes an entry from the ACL of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="787f0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="787f0-104">SYNTAX</span></span>

### <span data-ttu-id="787f0-105">RemoveCatalogAclEntryForUser (Padrão)</span><span class="sxs-lookup"><span data-stu-id="787f0-105">RemoveCatalogAclEntryForUser (Default)</span></span>
```
Remove-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="787f0-106">RemoveCatalogItemAclEntryForUser</span><span class="sxs-lookup"><span data-stu-id="787f0-106">RemoveCatalogItemAclEntryForUser</span></span>
```
Remove-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid> -ItemType <String>
 -Path <CatalogPathInstance> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="787f0-107">RemoveCatalogAclEntryForGroup</span><span class="sxs-lookup"><span data-stu-id="787f0-107">RemoveCatalogAclEntryForGroup</span></span>
```
Remove-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="787f0-108">RemoveCatalogItemAclEntryForGroup</span><span class="sxs-lookup"><span data-stu-id="787f0-108">RemoveCatalogItemAclEntryForGroup</span></span>
```
Remove-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid> -ItemType <String>
 -Path <CatalogPathInstance> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="787f0-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="787f0-109">DESCRIPTION</span></span>
<span data-ttu-id="787f0-110">O cmdlet **Remove-AzDataLakeAnalyticsCatalogItemAclEntry** remove uma entrada (ACE) da lista de controle de acesso (ACL) de um item de catálogo ou catálogo no Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="787f0-110">The **Remove-AzDataLakeAnalyticsCatalogItemAclEntry** cmdlet removes an entry (ACE) from the access control list (ACL) of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="787f0-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="787f0-111">EXAMPLES</span></span>

### <span data-ttu-id="787f0-112">Exemplo 1: Remover a ACL do usuário para um catálogo</span><span class="sxs-lookup"><span data-stu-id="787f0-112">Example 1: Remove the user ACL for a catalog</span></span>
```powershell
PS C:\> Remove-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzADUser -Mail "PattiFuller@contoso.com").Id
```

<span data-ttu-id="787f0-113">Este comando remove o catálogo ACL para Patti Fuller da conta contosoadla.</span><span class="sxs-lookup"><span data-stu-id="787f0-113">This command removes the catalog ACL for Patti Fuller of the contosoadla account.</span></span>

### <span data-ttu-id="787f0-114">Exemplo 2: Remover a ACL do usuário para um banco de dados</span><span class="sxs-lookup"><span data-stu-id="787f0-114">Example 2: Remove the user ACL for a database</span></span>
```powershell
PS C:\> Remove-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzADUser -Mail "PattiFuller@contoso.com").Id -ItemType Database -Path "databaseName"
```

<span data-ttu-id="787f0-115">Este comando remove o banco de dados ACL de Patti Fuller da conta contosoadla.</span><span class="sxs-lookup"><span data-stu-id="787f0-115">This command removes the database ACL for Patti Fuller of the contosoadla account.</span></span>

## <span data-ttu-id="787f0-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="787f0-116">PARAMETERS</span></span>

### <span data-ttu-id="787f0-117">-Account</span><span class="sxs-lookup"><span data-stu-id="787f0-117">-Account</span></span>
<span data-ttu-id="787f0-118">Especifica o nome da conta do Data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="787f0-118">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="787f0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="787f0-119">-DefaultProfile</span></span>
<span data-ttu-id="787f0-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="787f0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="787f0-121">-Group</span><span class="sxs-lookup"><span data-stu-id="787f0-121">-Group</span></span>
<span data-ttu-id="787f0-122">Remova a entrada ACL do catálogo para o grupo.</span><span class="sxs-lookup"><span data-stu-id="787f0-122">Remove ACL entry of catalog for group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RemoveCatalogAclEntryForGroup, RemoveCatalogItemAclEntryForGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="787f0-123">-ItemType</span><span class="sxs-lookup"><span data-stu-id="787f0-123">-ItemType</span></span>
<span data-ttu-id="787f0-124">Especifica o tipo de catálogo ou item de catálogo.</span><span class="sxs-lookup"><span data-stu-id="787f0-124">Specifies the type of the catalog or catalog item(s).</span></span> <span data-ttu-id="787f0-125">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="787f0-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="787f0-126">Catálogo</span><span class="sxs-lookup"><span data-stu-id="787f0-126">Catalog</span></span>
- <span data-ttu-id="787f0-127">Banco de Dados</span><span class="sxs-lookup"><span data-stu-id="787f0-127">Database</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveCatalogItemAclEntryForUser, RemoveCatalogItemAclEntryForGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="787f0-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="787f0-128">-ObjectId</span></span>
<span data-ttu-id="787f0-129">A identidade do usuário a ser removido.</span><span class="sxs-lookup"><span data-stu-id="787f0-129">The identity of the user to remove.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: Id, UserId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="787f0-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="787f0-130">-PassThru</span></span>
<span data-ttu-id="787f0-131">Indica que uma resposta booleana deve ser retornada indicando o resultado da operação de exclusão.</span><span class="sxs-lookup"><span data-stu-id="787f0-131">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="787f0-132">-Path</span><span class="sxs-lookup"><span data-stu-id="787f0-132">-Path</span></span>
<span data-ttu-id="787f0-133">Especifica o caminho do Data Lake Analytics de um catálogo ou item de catálogo.</span><span class="sxs-lookup"><span data-stu-id="787f0-133">Specifies the Data Lake Analytics path of an catalog or catalog item.</span></span>
<span data-ttu-id="787f0-134">As partes do caminho devem ser separadas por um ponto (.).</span><span class="sxs-lookup"><span data-stu-id="787f0-134">The parts of the path should be separated by a period (.).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance
Parameter Sets: RemoveCatalogItemAclEntryForUser, RemoveCatalogItemAclEntryForGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="787f0-135">-User</span><span class="sxs-lookup"><span data-stu-id="787f0-135">-User</span></span>
<span data-ttu-id="787f0-136">Remova a entrada ACL do catálogo para o usuário.</span><span class="sxs-lookup"><span data-stu-id="787f0-136">Remove ACL entry of catalog for user.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RemoveCatalogAclEntryForUser, RemoveCatalogItemAclEntryForUser
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="787f0-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="787f0-137">-Confirm</span></span>
<span data-ttu-id="787f0-138">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="787f0-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="787f0-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="787f0-139">-WhatIf</span></span>
<span data-ttu-id="787f0-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="787f0-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="787f0-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="787f0-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="787f0-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="787f0-142">CommonParameters</span></span>
<span data-ttu-id="787f0-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="787f0-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="787f0-144">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="787f0-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="787f0-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="787f0-145">INPUTS</span></span>

### <span data-ttu-id="787f0-146">System.String</span><span class="sxs-lookup"><span data-stu-id="787f0-146">System.String</span></span>

### <span data-ttu-id="787f0-147">System.Guid</span><span class="sxs-lookup"><span data-stu-id="787f0-147">System.Guid</span></span>

### <span data-ttu-id="787f0-148">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="787f0-148">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="787f0-149">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="787f0-149">OUTPUTS</span></span>

### <span data-ttu-id="787f0-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="787f0-150">System.Boolean</span></span>

## <span data-ttu-id="787f0-151">NOTES</span><span class="sxs-lookup"><span data-stu-id="787f0-151">NOTES</span></span>

## <span data-ttu-id="787f0-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="787f0-152">RELATED LINKS</span></span>

[<span data-ttu-id="787f0-153">O U-SQL agora oferece controle de acesso de nível de banco de dados</span><span class="sxs-lookup"><span data-stu-id="787f0-153">U-SQL now offers database level access control</span></span>](https://github.com/Azure/AzureDataLake/blob/master/docs/Release_Notes/2016/2016_08_01/USQL_Release_Notes_2016_08_01.md#u-sql-now-offers-database-level-access-control)

[<span data-ttu-id="787f0-154">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="787f0-154">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Get-AzDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="787f0-155">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="787f0-155">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Set-AzDataLakeAnalyticsCatalogItemAclEntry.md)
