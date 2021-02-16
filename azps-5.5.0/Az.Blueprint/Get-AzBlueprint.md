---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/get-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprint.md
ms.openlocfilehash: ab383b1fb46759c2369d94d4bb57284ba59cf671
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117918"
---
# <span data-ttu-id="97ac2-101">Get-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="97ac2-101">Get-AzBlueprint</span></span>

## <span data-ttu-id="97ac2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="97ac2-102">SYNOPSIS</span></span>
<span data-ttu-id="97ac2-103">Obter uma ou mais definições de diagrama.</span><span class="sxs-lookup"><span data-stu-id="97ac2-103">Get one or more blueprint definitions.</span></span>

## <span data-ttu-id="97ac2-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="97ac2-104">SYNTAX</span></span>

### <span data-ttu-id="97ac2-105">SubscriptionScope (Padrão)</span><span class="sxs-lookup"><span data-stu-id="97ac2-105">SubscriptionScope (Default)</span></span>
```
Get-AzBlueprint [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97ac2-106">ByManagementGroupNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="97ac2-106">ByManagementGroupNameAndVersion</span></span>
```
Get-AzBlueprint -Name <String> -ManagementGroupId <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97ac2-107">BySubscriptionAndName</span><span class="sxs-lookup"><span data-stu-id="97ac2-107">BySubscriptionAndName</span></span>
```
Get-AzBlueprint [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="97ac2-108">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="97ac2-108">ByManagementGroupAndName</span></span>
```
Get-AzBlueprint -Name <String> -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="97ac2-109">ByManagementGroupNameAndLatestPublished</span><span class="sxs-lookup"><span data-stu-id="97ac2-109">ByManagementGroupNameAndLatestPublished</span></span>
```
Get-AzBlueprint -Name <String> -ManagementGroupId <String> [-LatestPublished]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97ac2-110">BySubscriptionNameAndLatestPublished</span><span class="sxs-lookup"><span data-stu-id="97ac2-110">BySubscriptionNameAndLatestPublished</span></span>
```
Get-AzBlueprint -Name <String> [-SubscriptionId <String>] [-LatestPublished]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97ac2-111">BySubscriptionNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="97ac2-111">BySubscriptionNameAndVersion</span></span>
```
Get-AzBlueprint -Name <String> [-SubscriptionId <String>] [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="97ac2-112">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="97ac2-112">ManagementGroupScope</span></span>
```
Get-AzBlueprint -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97ac2-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="97ac2-113">DESCRIPTION</span></span>
<span data-ttu-id="97ac2-114">Obter uma ou mais definições de diagrama.</span><span class="sxs-lookup"><span data-stu-id="97ac2-114">Get one or more blueprint definitions.</span></span> <span data-ttu-id="97ac2-115">As definições de diagrama existem no grupo de gerenciamento ou no escopo da assinatura.</span><span class="sxs-lookup"><span data-stu-id="97ac2-115">Blueprint definitions exist at the management group or subscription scope.</span></span>

## <span data-ttu-id="97ac2-116">Exemplos</span><span class="sxs-lookup"><span data-stu-id="97ac2-116">EXAMPLES</span></span>

### <span data-ttu-id="97ac2-117">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="97ac2-117">Example 1</span></span>
```powershell
PS> Get-AzBlueprint

Name                 : PS-BlueprintDefinition
Id                   : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprints/PS-BlueprintDefinition
SubscriptionId       : 00000000-1111-0000-1111-000000000000
Versions             : {1.0}
Description          : Powershell test blueprint
TimeCreated          : 2019-02-01
TargetScope          : Subscription
Parameters           : {storageData_storageAccountType, storageData_location, allowedlocations_listOfAllowedLocations}
ResourceGroups       : ResourceGroup
```

<span data-ttu-id="97ac2-118">Obter as definições de diagrama dentro da assinatura atual e a hierarquia de grupo de gerenciamento da assinatura.</span><span class="sxs-lookup"><span data-stu-id="97ac2-118">Get the blueprint definitions within the current subscription and the management group hierarchy of the subscription.</span></span>

### <span data-ttu-id="97ac2-119">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="97ac2-119">Example 2</span></span>
```powershell
PS> Get-AzBlueprint -ManagementGroupId "myManagementGroupId"

Name                 : PS-MG-BlueprintDefinition
Id                   : /providers/Microsoft.Management/managementGroups/myManagementGroupId/providers/Microsoft.Blueprint/blueprints/PS-MG-BlueprintDefinition
ManagementGroupId    : myManagementGroupId
Versions             : {1.0, 2.0, 3.0, 4.0}
TimeCreated          : 2019-03-04
TargetScope          : Subscription
Parameters           : {enforcetaganditsvalue_tagName, enforcetaganditsvalue_tagValue, [Usergrouporapplicationname]:Contributor_RoleAssignmentName,
                       [Usergrouporapplicationname]:Owner_RoleAssignmentName}
ResourceGroups       : {ResourceGroup, ResourceGroup2}
```

<span data-ttu-id="97ac2-120">Obter as definições de diagrama dentro do grupo de gerenciamento especificado.</span><span class="sxs-lookup"><span data-stu-id="97ac2-120">Get the blueprint definitions within the specified management group.</span></span>

### <span data-ttu-id="97ac2-121">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="97ac2-121">Example 3</span></span>
```powershell
PS> Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000"

Name                 : PS-BlueprintDefinition
Id                   : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprints/PS-BlueprintDefinition
SubscriptionId       : 00000000-1111-0000-1111-000000000000
Versions             : {1.0}
Description          : Powershell test blueprint
TimeCreated          : 2019-02-01
TargetScope          : Subscription
Parameters           : {storageData_storageAccountType, storageData_location, allowedlocations_listOfAllowedLocations}
ResourceGroups       : ResourceGroup
```

<span data-ttu-id="97ac2-122">Obter as definições de diagrama dentro da assinatura especificada e a hierarquia de grupo de gerenciamento da assinatura.</span><span class="sxs-lookup"><span data-stu-id="97ac2-122">Get the blueprint definitions within the specified subscription and the management group hierarchy of the subscription.</span></span>

### <span data-ttu-id="97ac2-123">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="97ac2-123">Example 4</span></span>
```powershell
PS> Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
```

<span data-ttu-id="97ac2-124">Obter a definição de diagrama com o nome determinado dentro da assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="97ac2-124">Get the blueprint definition with the given name within the specified subscription.</span></span>

### <span data-ttu-id="97ac2-125">Exemplo 5</span><span class="sxs-lookup"><span data-stu-id="97ac2-125">Example 5</span></span>
```powershell
PS> Get-AzBlueprint -ManagementGroupId "myManagementGroupId" -Name "myBlueprintName" -Version "myBlueprintVersion"
```

<span data-ttu-id="97ac2-126">Obter a definição do diagrama com o nome e a versão indicados dentro do grupo de gerenciamento especificado.</span><span class="sxs-lookup"><span data-stu-id="97ac2-126">Get the blueprint definition with the given name and version within the specified management group.</span></span>

### <span data-ttu-id="97ac2-127">Exemplo 6</span><span class="sxs-lookup"><span data-stu-id="97ac2-127">Example 6</span></span>
```powershell
PS> Get-AzBlueprint -ManagementGroupId "myManagementGroupId" -Name "myBlueprintName" -LatestPublished
```

<span data-ttu-id="97ac2-128">Obter a definição de diagrama publicada mais recente com o nome determinado dentro do grupo de gerenciamento especificado.</span><span class="sxs-lookup"><span data-stu-id="97ac2-128">Get the latest published blueprint definition with the given name within the specified management group.</span></span>

## <span data-ttu-id="97ac2-129">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="97ac2-129">PARAMETERS</span></span>

### <span data-ttu-id="97ac2-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97ac2-130">-DefaultProfile</span></span>
<span data-ttu-id="97ac2-131">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="97ac2-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97ac2-132">-LatestPublished</span><span class="sxs-lookup"><span data-stu-id="97ac2-132">-LatestPublished</span></span>
<span data-ttu-id="97ac2-133">O sinalizador de definição de planta publicado mais recente.</span><span class="sxs-lookup"><span data-stu-id="97ac2-133">The latest published blueprint definition flag.</span></span>
<span data-ttu-id="97ac2-134">Quando definida, a execução retorna a versão publicada mais recente da definição de diagrama.</span><span class="sxs-lookup"><span data-stu-id="97ac2-134">When set, execution returns the latest published version of the blueprint definition.</span></span>
<span data-ttu-id="97ac2-135">O padrão é falso.</span><span class="sxs-lookup"><span data-stu-id="97ac2-135">Defaults to false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByManagementGroupNameAndLatestPublished, BySubscriptionNameAndLatestPublished
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97ac2-136">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="97ac2-136">-ManagementGroupId</span></span>
<span data-ttu-id="97ac2-137">ID do Grupo de Gerenciamento onde a definição de diagrama é salva.</span><span class="sxs-lookup"><span data-stu-id="97ac2-137">Management Group Id where the blueprint definition is saved.</span></span>

```yaml
Type: System.String
Parameter Sets: ByManagementGroupNameAndVersion, ByManagementGroupAndName, ByManagementGroupNameAndLatestPublished, ManagementGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97ac2-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="97ac2-138">-Name</span></span>
<span data-ttu-id="97ac2-139">Nome da definição de planta.</span><span class="sxs-lookup"><span data-stu-id="97ac2-139">Blueprint definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByManagementGroupNameAndVersion, ByManagementGroupAndName, ByManagementGroupNameAndLatestPublished, BySubscriptionNameAndLatestPublished, BySubscriptionNameAndVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: BySubscriptionAndName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97ac2-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="97ac2-140">-SubscriptionId</span></span>
<span data-ttu-id="97ac2-141">ID da assinatura onde a definição de plano de trabalho é salva.</span><span class="sxs-lookup"><span data-stu-id="97ac2-141">Subscription Id where the blueprint definition is saved.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionScope, BySubscriptionAndName, BySubscriptionNameAndLatestPublished, BySubscriptionNameAndVersion
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97ac2-142">-Versão</span><span class="sxs-lookup"><span data-stu-id="97ac2-142">-Version</span></span>
<span data-ttu-id="97ac2-143">Versão de definição de planta publicada.</span><span class="sxs-lookup"><span data-stu-id="97ac2-143">Published blueprint definition version.</span></span>

```yaml
Type: System.String
Parameter Sets: ByManagementGroupNameAndVersion, BySubscriptionNameAndVersion
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97ac2-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97ac2-144">CommonParameters</span></span>
<span data-ttu-id="97ac2-145">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97ac2-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97ac2-146">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="97ac2-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97ac2-147">Entradas</span><span class="sxs-lookup"><span data-stu-id="97ac2-147">INPUTS</span></span>

### <span data-ttu-id="97ac2-148">System.String</span><span class="sxs-lookup"><span data-stu-id="97ac2-148">System.String</span></span>

## <span data-ttu-id="97ac2-149">Saídas</span><span class="sxs-lookup"><span data-stu-id="97ac2-149">OUTPUTS</span></span>

### <span data-ttu-id="97ac2-150">System.Object</span><span class="sxs-lookup"><span data-stu-id="97ac2-150">System.Object</span></span>
## <span data-ttu-id="97ac2-151">Notas</span><span class="sxs-lookup"><span data-stu-id="97ac2-151">NOTES</span></span>

## <span data-ttu-id="97ac2-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="97ac2-152">RELATED LINKS</span></span>
