---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/get-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprint.md
ms.openlocfilehash: ab383b1fb46759c2369d94d4bb57284ba59cf671
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98430368"
---
# <span data-ttu-id="ce4ff-101">Get-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="ce4ff-101">Get-AzBlueprint</span></span>

## <span data-ttu-id="ce4ff-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ce4ff-102">SYNOPSIS</span></span>
<span data-ttu-id="ce4ff-103">Obtenha uma ou mais definições de Blueprint.</span><span class="sxs-lookup"><span data-stu-id="ce4ff-103">Get one or more blueprint definitions.</span></span>

## <span data-ttu-id="ce4ff-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ce4ff-104">SYNTAX</span></span>

### <span data-ttu-id="ce4ff-105">SubscriptionScope (padrão)</span><span class="sxs-lookup"><span data-stu-id="ce4ff-105">SubscriptionScope (Default)</span></span>
```
Get-AzBlueprint [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce4ff-106">ByManagementGroupNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="ce4ff-106">ByManagementGroupNameAndVersion</span></span>
```
Get-AzBlueprint -Name <String> -ManagementGroupId <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce4ff-107">BySubscriptionAndName</span><span class="sxs-lookup"><span data-stu-id="ce4ff-107">BySubscriptionAndName</span></span>
```
Get-AzBlueprint [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ce4ff-108">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="ce4ff-108">ByManagementGroupAndName</span></span>
```
Get-AzBlueprint -Name <String> -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ce4ff-109">ByManagementGroupNameAndLatestPublished</span><span class="sxs-lookup"><span data-stu-id="ce4ff-109">ByManagementGroupNameAndLatestPublished</span></span>
```
Get-AzBlueprint -Name <String> -ManagementGroupId <String> [-LatestPublished]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce4ff-110">BySubscriptionNameAndLatestPublished</span><span class="sxs-lookup"><span data-stu-id="ce4ff-110">BySubscriptionNameAndLatestPublished</span></span>
```
Get-AzBlueprint -Name <String> [-SubscriptionId <String>] [-LatestPublished]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce4ff-111">BySubscriptionNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="ce4ff-111">BySubscriptionNameAndVersion</span></span>
```
Get-AzBlueprint -Name <String> [-SubscriptionId <String>] [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ce4ff-112">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="ce4ff-112">ManagementGroupScope</span></span>
```
Get-AzBlueprint -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce4ff-113">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ce4ff-113">DESCRIPTION</span></span>
<span data-ttu-id="ce4ff-114">Obtenha uma ou mais definições de Blueprint.</span><span class="sxs-lookup"><span data-stu-id="ce4ff-114">Get one or more blueprint definitions.</span></span> <span data-ttu-id="ce4ff-115">Há definições Blueprints no grupo de gerenciamento ou no escopo da assinatura.</span><span class="sxs-lookup"><span data-stu-id="ce4ff-115">Blueprint definitions exist at the management group or subscription scope.</span></span>

## <span data-ttu-id="ce4ff-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ce4ff-116">EXAMPLES</span></span>

### <span data-ttu-id="ce4ff-117">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ce4ff-117">Example 1</span></span>
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

<span data-ttu-id="ce4ff-118">Obtenha as definições Blueprints dentro da assinatura atual e a hierarquia grupo de gerenciamento da assinatura.</span><span class="sxs-lookup"><span data-stu-id="ce4ff-118">Get the blueprint definitions within the current subscription and the management group hierarchy of the subscription.</span></span>

### <span data-ttu-id="ce4ff-119">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ce4ff-119">Example 2</span></span>
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

<span data-ttu-id="ce4ff-120">Obter as definições Blueprints dentro do grupo de gerenciamento especificado.</span><span class="sxs-lookup"><span data-stu-id="ce4ff-120">Get the blueprint definitions within the specified management group.</span></span>

### <span data-ttu-id="ce4ff-121">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="ce4ff-121">Example 3</span></span>
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

<span data-ttu-id="ce4ff-122">Obter as definições Blueprints dentro da assinatura especificada e da hierarquia do grupo de gerenciamento da assinatura.</span><span class="sxs-lookup"><span data-stu-id="ce4ff-122">Get the blueprint definitions within the specified subscription and the management group hierarchy of the subscription.</span></span>

### <span data-ttu-id="ce4ff-123">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="ce4ff-123">Example 4</span></span>
```powershell
PS> Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
```

<span data-ttu-id="ce4ff-124">Obtenha a definição Blueprint com o nome especificado na assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="ce4ff-124">Get the blueprint definition with the given name within the specified subscription.</span></span>

### <span data-ttu-id="ce4ff-125">Exemplo 5</span><span class="sxs-lookup"><span data-stu-id="ce4ff-125">Example 5</span></span>
```powershell
PS> Get-AzBlueprint -ManagementGroupId "myManagementGroupId" -Name "myBlueprintName" -Version "myBlueprintVersion"
```

<span data-ttu-id="ce4ff-126">Obtenha a definição Blueprint com o nome e a versão fornecidos dentro do grupo de gerenciamento especificado.</span><span class="sxs-lookup"><span data-stu-id="ce4ff-126">Get the blueprint definition with the given name and version within the specified management group.</span></span>

### <span data-ttu-id="ce4ff-127">Exemplo 6</span><span class="sxs-lookup"><span data-stu-id="ce4ff-127">Example 6</span></span>
```powershell
PS> Get-AzBlueprint -ManagementGroupId "myManagementGroupId" -Name "myBlueprintName" -LatestPublished
```

<span data-ttu-id="ce4ff-128">Obtenha a definição mais recente do plano gráfico publicado com o nome fornecido dentro do grupo de gerenciamento especificado.</span><span class="sxs-lookup"><span data-stu-id="ce4ff-128">Get the latest published blueprint definition with the given name within the specified management group.</span></span>

## <span data-ttu-id="ce4ff-129">OS</span><span class="sxs-lookup"><span data-stu-id="ce4ff-129">PARAMETERS</span></span>

### <span data-ttu-id="ce4ff-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce4ff-130">-DefaultProfile</span></span>
<span data-ttu-id="ce4ff-131">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ce4ff-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce4ff-132">-LatestPublished</span><span class="sxs-lookup"><span data-stu-id="ce4ff-132">-LatestPublished</span></span>
<span data-ttu-id="ce4ff-133">O sinalizador de definição Blueprint mais recente publicada.</span><span class="sxs-lookup"><span data-stu-id="ce4ff-133">The latest published blueprint definition flag.</span></span>
<span data-ttu-id="ce4ff-134">Quando definido, executar retorna a versão mais recente publicada da definição Blueprint.</span><span class="sxs-lookup"><span data-stu-id="ce4ff-134">When set, execution returns the latest published version of the blueprint definition.</span></span>
<span data-ttu-id="ce4ff-135">O padrão é false.</span><span class="sxs-lookup"><span data-stu-id="ce4ff-135">Defaults to false.</span></span>

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

### <span data-ttu-id="ce4ff-136">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="ce4ff-136">-ManagementGroupId</span></span>
<span data-ttu-id="ce4ff-137">ID do grupo de gerenciamento em que a definição Blueprint é salva.</span><span class="sxs-lookup"><span data-stu-id="ce4ff-137">Management Group Id where the blueprint definition is saved.</span></span>

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

### <span data-ttu-id="ce4ff-138">-Nome</span><span class="sxs-lookup"><span data-stu-id="ce4ff-138">-Name</span></span>
<span data-ttu-id="ce4ff-139">Nome da definição do plano.</span><span class="sxs-lookup"><span data-stu-id="ce4ff-139">Blueprint definition name.</span></span>

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

### <span data-ttu-id="ce4ff-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ce4ff-140">-SubscriptionId</span></span>
<span data-ttu-id="ce4ff-141">ID da assinatura na qual a definição Blueprint é salva.</span><span class="sxs-lookup"><span data-stu-id="ce4ff-141">Subscription Id where the blueprint definition is saved.</span></span>

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

### <span data-ttu-id="ce4ff-142">-Versão</span><span class="sxs-lookup"><span data-stu-id="ce4ff-142">-Version</span></span>
<span data-ttu-id="ce4ff-143">Versão de definição de esquema publicada.</span><span class="sxs-lookup"><span data-stu-id="ce4ff-143">Published blueprint definition version.</span></span>

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

### <span data-ttu-id="ce4ff-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce4ff-144">CommonParameters</span></span>
<span data-ttu-id="ce4ff-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce4ff-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce4ff-146">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ce4ff-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce4ff-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ce4ff-147">INPUTS</span></span>

### <span data-ttu-id="ce4ff-148">System. String</span><span class="sxs-lookup"><span data-stu-id="ce4ff-148">System.String</span></span>

## <span data-ttu-id="ce4ff-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ce4ff-149">OUTPUTS</span></span>

### <span data-ttu-id="ce4ff-150">System. Object</span><span class="sxs-lookup"><span data-stu-id="ce4ff-150">System.Object</span></span>
## <span data-ttu-id="ce4ff-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ce4ff-151">NOTES</span></span>

## <span data-ttu-id="ce4ff-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ce4ff-152">RELATED LINKS</span></span>
