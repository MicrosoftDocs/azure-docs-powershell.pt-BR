---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/powershell/module/az.blueprint/get-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprint.md
ms.openlocfilehash: 6b646e22ff32d9fe361cdedd6dbb6fa5c9fba270
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893007"
---
# <span data-ttu-id="d366b-101">Get-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="d366b-101">Get-AzBlueprint</span></span>

## <span data-ttu-id="d366b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d366b-102">SYNOPSIS</span></span>
<span data-ttu-id="d366b-103">Obter uma ou mais definições de projeto.</span><span class="sxs-lookup"><span data-stu-id="d366b-103">Get one or more blueprint definitions.</span></span>

## <span data-ttu-id="d366b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d366b-104">SYNTAX</span></span>

### <span data-ttu-id="d366b-105">SubscriptionScope (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d366b-105">SubscriptionScope (Default)</span></span>
```
Get-AzBlueprint [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d366b-106">ByManagementGroupNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="d366b-106">ByManagementGroupNameAndVersion</span></span>
```
Get-AzBlueprint -Name <String> -ManagementGroupId <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d366b-107">BySubscriptionAndName</span><span class="sxs-lookup"><span data-stu-id="d366b-107">BySubscriptionAndName</span></span>
```
Get-AzBlueprint [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d366b-108">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="d366b-108">ByManagementGroupAndName</span></span>
```
Get-AzBlueprint -Name <String> -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d366b-109">ByManagementGroupNameAndLatestPublished</span><span class="sxs-lookup"><span data-stu-id="d366b-109">ByManagementGroupNameAndLatestPublished</span></span>
```
Get-AzBlueprint -Name <String> -ManagementGroupId <String> [-LatestPublished]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d366b-110">BySubscriptionNameAndLatestPublished</span><span class="sxs-lookup"><span data-stu-id="d366b-110">BySubscriptionNameAndLatestPublished</span></span>
```
Get-AzBlueprint -Name <String> [-SubscriptionId <String>] [-LatestPublished]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d366b-111">BySubscriptionNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="d366b-111">BySubscriptionNameAndVersion</span></span>
```
Get-AzBlueprint -Name <String> [-SubscriptionId <String>] [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d366b-112">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="d366b-112">ManagementGroupScope</span></span>
```
Get-AzBlueprint -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d366b-113">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d366b-113">DESCRIPTION</span></span>
<span data-ttu-id="d366b-114">Obter uma ou mais definições de projeto.</span><span class="sxs-lookup"><span data-stu-id="d366b-114">Get one or more blueprint definitions.</span></span> <span data-ttu-id="d366b-115">As definições de projeto existem no grupo de gerenciamento ou no escopo de assinatura.</span><span class="sxs-lookup"><span data-stu-id="d366b-115">Blueprint definitions exist at the management group or subscription scope.</span></span>

## <span data-ttu-id="d366b-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d366b-116">EXAMPLES</span></span>

### <span data-ttu-id="d366b-117">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d366b-117">Example 1</span></span>
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

<span data-ttu-id="d366b-118">Obter as definições de projeto dentro da assinatura atual e a hierarquia de grupo de gerenciamento da assinatura.</span><span class="sxs-lookup"><span data-stu-id="d366b-118">Get the blueprint definitions within the current subscription and the management group hierarchy of the subscription.</span></span>

### <span data-ttu-id="d366b-119">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d366b-119">Example 2</span></span>
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

<span data-ttu-id="d366b-120">Obter as definições de projeto dentro do grupo de gerenciamento especificado.</span><span class="sxs-lookup"><span data-stu-id="d366b-120">Get the blueprint definitions within the specified management group.</span></span>

### <span data-ttu-id="d366b-121">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="d366b-121">Example 3</span></span>
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

<span data-ttu-id="d366b-122">Obter as definições de projeto dentro da assinatura especificada e a hierarquia de grupo de gerenciamento da assinatura.</span><span class="sxs-lookup"><span data-stu-id="d366b-122">Get the blueprint definitions within the specified subscription and the management group hierarchy of the subscription.</span></span>

### <span data-ttu-id="d366b-123">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="d366b-123">Example 4</span></span>
```powershell
PS> Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
```

<span data-ttu-id="d366b-124">Obter a definição de projeto com o nome determinado dentro da assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="d366b-124">Get the blueprint definition with the given name within the specified subscription.</span></span>

### <span data-ttu-id="d366b-125">Exemplo 5</span><span class="sxs-lookup"><span data-stu-id="d366b-125">Example 5</span></span>
```powershell
PS> Get-AzBlueprint -ManagementGroupId "myManagementGroupId" -Name "myBlueprintName" -Version "myBlueprintVersion"
```

<span data-ttu-id="d366b-126">Obter a definição de projeto com o nome e a versão especificados no grupo de gerenciamento especificado.</span><span class="sxs-lookup"><span data-stu-id="d366b-126">Get the blueprint definition with the given name and version within the specified management group.</span></span>

### <span data-ttu-id="d366b-127">Exemplo 6</span><span class="sxs-lookup"><span data-stu-id="d366b-127">Example 6</span></span>
```powershell
PS> Get-AzBlueprint -ManagementGroupId "myManagementGroupId" -Name "myBlueprintName" -LatestPublished
```

<span data-ttu-id="d366b-128">Obter a definição de projeto publicado mais recente com o nome indicado no grupo de gerenciamento especificado.</span><span class="sxs-lookup"><span data-stu-id="d366b-128">Get the latest published blueprint definition with the given name within the specified management group.</span></span>

## <span data-ttu-id="d366b-129">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d366b-129">PARAMETERS</span></span>

### <span data-ttu-id="d366b-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d366b-130">-DefaultProfile</span></span>
<span data-ttu-id="d366b-131">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d366b-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d366b-132">-LatestPublished</span><span class="sxs-lookup"><span data-stu-id="d366b-132">-LatestPublished</span></span>
<span data-ttu-id="d366b-133">O sinalizador de definição de projeto publicado mais recente.</span><span class="sxs-lookup"><span data-stu-id="d366b-133">The latest published blueprint definition flag.</span></span>
<span data-ttu-id="d366b-134">Quando definido, a execução retorna a versão publicada mais recente da definição do modelo.</span><span class="sxs-lookup"><span data-stu-id="d366b-134">When set, execution returns the latest published version of the blueprint definition.</span></span>
<span data-ttu-id="d366b-135">O padrão é false.</span><span class="sxs-lookup"><span data-stu-id="d366b-135">Defaults to false.</span></span>

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

### <span data-ttu-id="d366b-136">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="d366b-136">-ManagementGroupId</span></span>
<span data-ttu-id="d366b-137">ID do Grupo de Gerenciamento onde a definição de projeto é salva.</span><span class="sxs-lookup"><span data-stu-id="d366b-137">Management Group Id where the blueprint definition is saved.</span></span>

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

### <span data-ttu-id="d366b-138">-Name</span><span class="sxs-lookup"><span data-stu-id="d366b-138">-Name</span></span>
<span data-ttu-id="d366b-139">Nome da definição de projeto.</span><span class="sxs-lookup"><span data-stu-id="d366b-139">Blueprint definition name.</span></span>

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

### <span data-ttu-id="d366b-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d366b-140">-SubscriptionId</span></span>
<span data-ttu-id="d366b-141">ID da assinatura onde a definição de projeto é salva.</span><span class="sxs-lookup"><span data-stu-id="d366b-141">Subscription Id where the blueprint definition is saved.</span></span>

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

### <span data-ttu-id="d366b-142">-Version</span><span class="sxs-lookup"><span data-stu-id="d366b-142">-Version</span></span>
<span data-ttu-id="d366b-143">Versão de definição de projeto publicada.</span><span class="sxs-lookup"><span data-stu-id="d366b-143">Published blueprint definition version.</span></span>

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

### <span data-ttu-id="d366b-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d366b-144">CommonParameters</span></span>
<span data-ttu-id="d366b-145">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d366b-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d366b-146">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d366b-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d366b-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d366b-147">INPUTS</span></span>

### <span data-ttu-id="d366b-148">System.String</span><span class="sxs-lookup"><span data-stu-id="d366b-148">System.String</span></span>

## <span data-ttu-id="d366b-149">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d366b-149">OUTPUTS</span></span>

### <span data-ttu-id="d366b-150">System.Object</span><span class="sxs-lookup"><span data-stu-id="d366b-150">System.Object</span></span>
## <span data-ttu-id="d366b-151">NOTES</span><span class="sxs-lookup"><span data-stu-id="d366b-151">NOTES</span></span>

## <span data-ttu-id="d366b-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d366b-152">RELATED LINKS</span></span>
