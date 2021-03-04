---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/set-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchService.md
ms.openlocfilehash: 8fadba097b602bd84c8eb36d75f5b7a331e2280b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887954"
---
# <span data-ttu-id="627b7-101">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="627b7-101">Set-AzSearchService</span></span>

## <span data-ttu-id="627b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="627b7-102">SYNOPSIS</span></span>
<span data-ttu-id="627b7-103">Atualize um serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="627b7-103">Update an Azure Cognitive Search service.</span></span>

## <span data-ttu-id="627b7-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="627b7-104">SYNTAX</span></span>

### <span data-ttu-id="627b7-105">ResourceNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="627b7-105">ResourceNameParameterSet (Default)</span></span>
```
Set-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-PartitionCount <Int32>]
 [-ReplicaCount <Int32>] [-PublicNetworkAccess <PSPublicNetworkAccess>] [-IdentityType <PSIdentityType>]
 [-IPRuleList <PSIpRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="627b7-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="627b7-106">InputObjectParameterSet</span></span>
```
Set-AzSearchService [-InputObject] <PSSearchService> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-PublicNetworkAccess <PSPublicNetworkAccess>] [-IdentityType <PSIdentityType>] [-IPRuleList <PSIpRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="627b7-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="627b7-107">ResourceIdParameterSet</span></span>
```
Set-AzSearchService [-ResourceId] <String> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-PublicNetworkAccess <PSPublicNetworkAccess>] [-IdentityType <PSIdentityType>] [-IPRuleList <PSIpRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="627b7-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="627b7-108">DESCRIPTION</span></span>
<span data-ttu-id="627b7-109">O cmdlet **Set-AzSearchService** modifica um serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="627b7-109">The **Set-AzSearchService** cmdlet modifies an Azure Cognitive Search service.</span></span>

## <span data-ttu-id="627b7-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="627b7-110">EXAMPLES</span></span>

### <span data-ttu-id="627b7-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="627b7-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01" -PartitionCount 2 -ReplicaCount 2


ResourceGroupName : TestAzureSearchPsGroup
Name              : pstestazuresearch01
Id                : /subscriptions/f9b96b36-1f5e-4021-8959-51527e26e6d3/resourceGroups/TestAzureSearchPsGroup/providers/Microsoft.Search/searchServices/pstestazuresearch01
Location          : West US
Sku               : Standard
ReplicaCount      : 2
PartitionCount    : 2
HostingMode       : Default
Tags              :
```

<span data-ttu-id="627b7-112">O exemplo altera a contagem de partições e a contagem de réplicas do serviço de Pesquisa Cognitiva do Azure para 2.</span><span class="sxs-lookup"><span data-stu-id="627b7-112">The example changes partition count and replica count of the Azure Cognitive Search service to 2.</span></span>

## <span data-ttu-id="627b7-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="627b7-113">PARAMETERS</span></span>

### <span data-ttu-id="627b7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="627b7-114">-DefaultProfile</span></span>
<span data-ttu-id="627b7-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="627b7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="627b7-116">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="627b7-116">-IdentityType</span></span>
<span data-ttu-id="627b7-117">(Opcional) Identidade do Serviço de Pesquisa Cognitiva do Azure (None/SystemAssigned)</span><span class="sxs-lookup"><span data-stu-id="627b7-117">(Optional) Azure Cognitive Search Service Identity (None/SystemAssigned)</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Management.Search.Models.PSIdentityType]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="627b7-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="627b7-118">-InputObject</span></span>
<span data-ttu-id="627b7-119">Objeto de Entrada do Serviço de Pesquisa.</span><span class="sxs-lookup"><span data-stu-id="627b7-119">Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="627b7-120">-IPRuleList</span><span class="sxs-lookup"><span data-stu-id="627b7-120">-IPRuleList</span></span>
<span data-ttu-id="627b7-121">(Opcional) Regras IP do Serviço de Pesquisa Cognitiva do Azure</span><span class="sxs-lookup"><span data-stu-id="627b7-121">(Optional) Azure Cognitive Search Service IP rules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSIpRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="627b7-122">-Name</span><span class="sxs-lookup"><span data-stu-id="627b7-122">-Name</span></span>
<span data-ttu-id="627b7-123">Nome do Serviço de Pesquisa.</span><span class="sxs-lookup"><span data-stu-id="627b7-123">Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="627b7-124">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="627b7-124">-PartitionCount</span></span>
<span data-ttu-id="627b7-125">Contagem de partições do Serviço de Pesquisa.</span><span class="sxs-lookup"><span data-stu-id="627b7-125">Search Service partition count.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="627b7-126">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="627b7-126">-PublicNetworkAccess</span></span>
<span data-ttu-id="627b7-127">(Opcional) Acesso à rede pública do Serviço de Pesquisa Cognitiva do Azure (Habilitado/Desabilitado)</span><span class="sxs-lookup"><span data-stu-id="627b7-127">(Optional) Azure Cognitive Search Service public network access (Enabled/Disabled)</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Management.Search.Models.PSPublicNetworkAccess]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="627b7-128">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="627b7-128">-ReplicaCount</span></span>
<span data-ttu-id="627b7-129">Contagem de réplicas do Serviço de Pesquisa.</span><span class="sxs-lookup"><span data-stu-id="627b7-129">Search Service replica count.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="627b7-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="627b7-130">-ResourceGroupName</span></span>
<span data-ttu-id="627b7-131">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="627b7-131">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="627b7-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="627b7-132">-ResourceId</span></span>
<span data-ttu-id="627b7-133">ID do Recurso do Serviço de Pesquisa.</span><span class="sxs-lookup"><span data-stu-id="627b7-133">Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="627b7-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="627b7-134">-Confirm</span></span>
<span data-ttu-id="627b7-135">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="627b7-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="627b7-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="627b7-136">-WhatIf</span></span>
<span data-ttu-id="627b7-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="627b7-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="627b7-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="627b7-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="627b7-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="627b7-139">CommonParameters</span></span>
<span data-ttu-id="627b7-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="627b7-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="627b7-141">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="627b7-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="627b7-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="627b7-142">INPUTS</span></span>

### <span data-ttu-id="627b7-143">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="627b7-143">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="627b7-144">System.String</span><span class="sxs-lookup"><span data-stu-id="627b7-144">System.String</span></span>

## <span data-ttu-id="627b7-145">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="627b7-145">OUTPUTS</span></span>

### <span data-ttu-id="627b7-146">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="627b7-146">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="627b7-147">NOTES</span><span class="sxs-lookup"><span data-stu-id="627b7-147">NOTES</span></span>

## <span data-ttu-id="627b7-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="627b7-148">RELATED LINKS</span></span>

[<span data-ttu-id="627b7-149">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="627b7-149">New-AzSearchService</span></span>](./New-AzSearchService.md)

[<span data-ttu-id="627b7-150">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="627b7-150">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="627b7-151">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="627b7-151">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)