---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticscatalogitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsCatalogItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsCatalogItemAclEntry.md
ms.openlocfilehash: 6d30985baed220ee4a7a599f1214c0c4124ef08d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770974"
---
# <span data-ttu-id="c9f87-101">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="c9f87-101">Remove-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>

## <span data-ttu-id="c9f87-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c9f87-102">SYNOPSIS</span></span>
<span data-ttu-id="c9f87-103">Exclui uma entrada da ACL de um catálogo ou item de catálogo na análise do data Lake.</span><span class="sxs-lookup"><span data-stu-id="c9f87-103">Deletes an entry from the ACL of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="c9f87-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c9f87-104">SYNTAX</span></span>

### <span data-ttu-id="c9f87-105">RemoveCatalogAclEntryForUser (padrão)</span><span class="sxs-lookup"><span data-stu-id="c9f87-105">RemoveCatalogAclEntryForUser (Default)</span></span>
```
Remove-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9f87-106">RemoveCatalogItemAclEntryForUser</span><span class="sxs-lookup"><span data-stu-id="c9f87-106">RemoveCatalogItemAclEntryForUser</span></span>
```
Remove-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-User] -ObjectId <Guid> -ItemType <String>
 -Path <CatalogPathInstance> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c9f87-107">RemoveCatalogAclEntryForGroup</span><span class="sxs-lookup"><span data-stu-id="c9f87-107">RemoveCatalogAclEntryForGroup</span></span>
```
Remove-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9f87-108">RemoveCatalogItemAclEntryForGroup</span><span class="sxs-lookup"><span data-stu-id="c9f87-108">RemoveCatalogItemAclEntryForGroup</span></span>
```
Remove-AzDataLakeAnalyticsCatalogItemAclEntry [-Account] <String> [-Group] -ObjectId <Guid> -ItemType <String>
 -Path <CatalogPathInstance> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c9f87-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c9f87-109">DESCRIPTION</span></span>
<span data-ttu-id="c9f87-110">O cmdlet **Remove-AzDataLakeAnalyticsCatalogItemAclEntry** remove uma entrada (ACE) da lista de controle de acesso (ACL) de um catálogo ou item de catálogo na análise do data Lake.</span><span class="sxs-lookup"><span data-stu-id="c9f87-110">The **Remove-AzDataLakeAnalyticsCatalogItemAclEntry** cmdlet removes an entry (ACE) from the access control list (ACL) of a catalog or catalog item in Data Lake Analytics.</span></span>

## <span data-ttu-id="c9f87-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c9f87-111">EXAMPLES</span></span>

### <span data-ttu-id="c9f87-112">Exemplo 1: remover a ACL do usuário de um catálogo</span><span class="sxs-lookup"><span data-stu-id="c9f87-112">Example 1: Remove the user ACL for a catalog</span></span>
```powershell
PS C:\> Remove-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzADUser -Mail "PattiFuller@contoso.com").Id
```

<span data-ttu-id="c9f87-113">Esse comando Remove a ACL do catálogo para Patti Pereira da conta contosoadla.</span><span class="sxs-lookup"><span data-stu-id="c9f87-113">This command removes the catalog ACL for Patti Fuller of the contosoadla account.</span></span>

### <span data-ttu-id="c9f87-114">Exemplo 2: remover a ACL do usuário de um banco de dados</span><span class="sxs-lookup"><span data-stu-id="c9f87-114">Example 2: Remove the user ACL for a database</span></span>
```powershell
PS C:\> Remove-AzDataLakeAnalyticsCatalogItemAclEntry -Account "contosoadla" -User -ObjectId (Get-AzADUser -Mail "PattiFuller@contoso.com").Id -ItemType Database -Path "databaseName"
```

<span data-ttu-id="c9f87-115">Esse comando Remove a ACL do banco de dados para Patti Pereira da conta contosoadla.</span><span class="sxs-lookup"><span data-stu-id="c9f87-115">This command removes the database ACL for Patti Fuller of the contosoadla account.</span></span>

## <span data-ttu-id="c9f87-116">OS</span><span class="sxs-lookup"><span data-stu-id="c9f87-116">PARAMETERS</span></span>

### <span data-ttu-id="c9f87-117">-Conta</span><span class="sxs-lookup"><span data-stu-id="c9f87-117">-Account</span></span>
<span data-ttu-id="c9f87-118">Especifica o nome da conta do data Lake Analytics.</span><span class="sxs-lookup"><span data-stu-id="c9f87-118">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="c9f87-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9f87-119">-DefaultProfile</span></span>
<span data-ttu-id="c9f87-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c9f87-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9f87-121">-Grupo</span><span class="sxs-lookup"><span data-stu-id="c9f87-121">-Group</span></span>
<span data-ttu-id="c9f87-122">Remover a entrada ACL do catálogo para o grupo.</span><span class="sxs-lookup"><span data-stu-id="c9f87-122">Remove ACL entry of catalog for group.</span></span>

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

### <span data-ttu-id="c9f87-123">-ItemType</span><span class="sxs-lookup"><span data-stu-id="c9f87-123">-ItemType</span></span>
<span data-ttu-id="c9f87-124">Especifica o tipo de catálogo ou item (ns) de catálogo.</span><span class="sxs-lookup"><span data-stu-id="c9f87-124">Specifies the type of the catalog or catalog item(s).</span></span> <span data-ttu-id="c9f87-125">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="c9f87-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c9f87-126">Catálogo</span><span class="sxs-lookup"><span data-stu-id="c9f87-126">Catalog</span></span>
- <span data-ttu-id="c9f87-127">Base</span><span class="sxs-lookup"><span data-stu-id="c9f87-127">Database</span></span>

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

### <span data-ttu-id="c9f87-128">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="c9f87-128">-ObjectId</span></span>
<span data-ttu-id="c9f87-129">A identidade do usuário a ser removida.</span><span class="sxs-lookup"><span data-stu-id="c9f87-129">The identity of the user to remove.</span></span>

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

### <span data-ttu-id="c9f87-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c9f87-130">-PassThru</span></span>
<span data-ttu-id="c9f87-131">Indica que uma resposta booliana deve ser retornada indicando o resultado da operação de exclusão.</span><span class="sxs-lookup"><span data-stu-id="c9f87-131">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="c9f87-132">-Caminho</span><span class="sxs-lookup"><span data-stu-id="c9f87-132">-Path</span></span>
<span data-ttu-id="c9f87-133">Especifica o caminho do data Lake Analytics de um catálogo ou item de catálogo.</span><span class="sxs-lookup"><span data-stu-id="c9f87-133">Specifies the Data Lake Analytics path of an catalog or catalog item.</span></span>
<span data-ttu-id="c9f87-134">As partes do caminho devem ser separadas por um ponto (.).</span><span class="sxs-lookup"><span data-stu-id="c9f87-134">The parts of the path should be separated by a period (.).</span></span>

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

### <span data-ttu-id="c9f87-135">-Usuário</span><span class="sxs-lookup"><span data-stu-id="c9f87-135">-User</span></span>
<span data-ttu-id="c9f87-136">Remover a entrada ACL do catálogo para o usuário.</span><span class="sxs-lookup"><span data-stu-id="c9f87-136">Remove ACL entry of catalog for user.</span></span>

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

### <span data-ttu-id="c9f87-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c9f87-137">-Confirm</span></span>
<span data-ttu-id="c9f87-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9f87-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9f87-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9f87-139">-WhatIf</span></span>
<span data-ttu-id="c9f87-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c9f87-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9f87-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c9f87-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9f87-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9f87-142">CommonParameters</span></span>
<span data-ttu-id="c9f87-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9f87-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9f87-144">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9f87-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9f87-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c9f87-145">INPUTS</span></span>

### <span data-ttu-id="c9f87-146">System. String</span><span class="sxs-lookup"><span data-stu-id="c9f87-146">System.String</span></span>

### <span data-ttu-id="c9f87-147">System. GUID</span><span class="sxs-lookup"><span data-stu-id="c9f87-147">System.Guid</span></span>

### <span data-ttu-id="c9f87-148">Microsoft. Azure. Commands. DataLakeAnalytics. Models. CatalogPathInstance</span><span class="sxs-lookup"><span data-stu-id="c9f87-148">Microsoft.Azure.Commands.DataLakeAnalytics.Models.CatalogPathInstance</span></span>

## <span data-ttu-id="c9f87-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c9f87-149">OUTPUTS</span></span>

### <span data-ttu-id="c9f87-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c9f87-150">System.Boolean</span></span>

## <span data-ttu-id="c9f87-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c9f87-151">NOTES</span></span>

## <span data-ttu-id="c9f87-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c9f87-152">RELATED LINKS</span></span>

[<span data-ttu-id="c9f87-153">O U-SQL agora oferece controle de acesso no nível do banco de dados</span><span class="sxs-lookup"><span data-stu-id="c9f87-153">U-SQL now offers database level access control</span></span>](https://github.com/Azure/AzureDataLake/blob/master/docs/Release_Notes/2016/2016_08_01/USQL_Release_Notes_2016_08_01.md#u-sql-now-offers-database-level-access-control)

[<span data-ttu-id="c9f87-154">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="c9f87-154">Get-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Get-AzDataLakeAnalyticsCatalogItemAclEntry.md)

[<span data-ttu-id="c9f87-155">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="c9f87-155">Set-AzDataLakeAnalyticsCatalogItemAclEntry</span></span>](Set-AzDataLakeAnalyticsCatalogItemAclEntry.md)
