---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/new-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchService.md
ms.openlocfilehash: 61101242b100ca4b477910a0dfa339ef7f9ea81b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886136"
---
# <span data-ttu-id="5332f-101">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="5332f-101">New-AzSearchService</span></span>

## <span data-ttu-id="5332f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5332f-102">SYNOPSIS</span></span>
<span data-ttu-id="5332f-103">Cria um serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="5332f-103">Creates an Azure Cognitive Search service.</span></span>

## <span data-ttu-id="5332f-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="5332f-104">SYNTAX</span></span>

```
New-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-Sku] <PSSkuName> [-Location] <String>
 [-PartitionCount <Int32>] [-ReplicaCount <Int32>] [-HostingMode <PSHostingMode>]
 [-PublicNetworkAccess <PSPublicNetworkAccess>] [-IdentityType <PSIdentityType>] [-IPRuleList <PSIpRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5332f-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="5332f-105">DESCRIPTION</span></span>
<span data-ttu-id="5332f-106">O cmdlet **New-AzSearchService** cria um serviço de Pesquisa Cognitiva do Azure com parâmetros especificados.</span><span class="sxs-lookup"><span data-stu-id="5332f-106">The **New-AzSearchService** cmdlet creates an Azure Cognitive Search service with specified parameters.</span></span>

## <span data-ttu-id="5332f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5332f-107">EXAMPLES</span></span>

### <span data-ttu-id="5332f-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5332f-108">Example 1</span></span>
```powershell
PS C:\> New-AzSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01" -Sku "Standard" -Location "West US" -PartitionCount 1 -ReplicaCount 1 -HostingMode Default -Force


ResourceGroupName : TestAzureSearchPsGroup
Name              : pstestazuresearch01
Id                : /subscriptions/f9b96b36-1f5e-4021-8959-51527e26e6d3/resourceGroups/TestAzureSearchPsGroup/providers/Microsoft.Search/searchServices/pstestazuresearch01
Location          : West US
Sku               : Standard
ReplicaCount      : 1
PartitionCount    : 1
HostingMode       : Default
Tags              :
```

<span data-ttu-id="5332f-109">O comando cria um serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="5332f-109">The command creates an Azure Cognitive Search service.</span></span>

## <span data-ttu-id="5332f-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="5332f-110">PARAMETERS</span></span>

### <span data-ttu-id="5332f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5332f-111">-DefaultProfile</span></span>
<span data-ttu-id="5332f-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5332f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5332f-113">-HostingMode</span><span class="sxs-lookup"><span data-stu-id="5332f-113">-HostingMode</span></span>
<span data-ttu-id="5332f-114">Modo de hospedagem do Serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="5332f-114">Azure Cognitive Search Service hosting mode.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Management.Search.Models.PSHostingMode]
Parameter Sets: (All)
Aliases:
Accepted values: Default, HighDensity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5332f-115">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="5332f-115">-IdentityType</span></span>
<span data-ttu-id="5332f-116">(Opcional) Identidade do Serviço de Pesquisa Cognitiva do Azure (None/SystemAssigned)</span><span class="sxs-lookup"><span data-stu-id="5332f-116">(Optional) Azure Cognitive Search Service Identity (None/SystemAssigned)</span></span>

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

### <span data-ttu-id="5332f-117">-IPRuleList</span><span class="sxs-lookup"><span data-stu-id="5332f-117">-IPRuleList</span></span>
<span data-ttu-id="5332f-118">(Opcional) Regras IP do Serviço de Pesquisa Cognitiva do Azure</span><span class="sxs-lookup"><span data-stu-id="5332f-118">(Optional) Azure Cognitive Search Service IP rules</span></span>

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

### <span data-ttu-id="5332f-119">-Location</span><span class="sxs-lookup"><span data-stu-id="5332f-119">-Location</span></span>
<span data-ttu-id="5332f-120">Local do Serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="5332f-120">Azure Cognitive Search Service location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5332f-121">-Name</span><span class="sxs-lookup"><span data-stu-id="5332f-121">-Name</span></span>
<span data-ttu-id="5332f-122">Nome do Serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="5332f-122">Azure Cognitive Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5332f-123">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="5332f-123">-PartitionCount</span></span>
<span data-ttu-id="5332f-124">Contagem de partições do Serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="5332f-124">Azure Cognitive Search Service partition count.</span></span>

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

### <span data-ttu-id="5332f-125">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="5332f-125">-PublicNetworkAccess</span></span>
<span data-ttu-id="5332f-126">(Opcional) Acesso à rede pública do Serviço de Pesquisa Cognitiva do Azure (Habilitado/Desabilitado)</span><span class="sxs-lookup"><span data-stu-id="5332f-126">(Optional) Azure Cognitive Search Service public network access (Enabled/Disabled)</span></span>

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

### <span data-ttu-id="5332f-127">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="5332f-127">-ReplicaCount</span></span>
<span data-ttu-id="5332f-128">Contagem de réplicas do Serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="5332f-128">Azure Cognitive Search Service replica count.</span></span>

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

### <span data-ttu-id="5332f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5332f-129">-ResourceGroupName</span></span>
<span data-ttu-id="5332f-130">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="5332f-130">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5332f-131">-Sku</span><span class="sxs-lookup"><span data-stu-id="5332f-131">-Sku</span></span>
<span data-ttu-id="5332f-132">Sku do Serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="5332f-132">Azure Cognitive Search Service Sku.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSkuName
Parameter Sets: (All)
Aliases:
Accepted values: Free, Basic, Standard, Standard2, Standard3

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5332f-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5332f-133">-Confirm</span></span>
<span data-ttu-id="5332f-134">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5332f-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5332f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5332f-135">-WhatIf</span></span>
<span data-ttu-id="5332f-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5332f-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5332f-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5332f-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5332f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5332f-138">CommonParameters</span></span>
<span data-ttu-id="5332f-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5332f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5332f-140">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5332f-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5332f-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5332f-141">INPUTS</span></span>

### <span data-ttu-id="5332f-142">Nenhum</span><span class="sxs-lookup"><span data-stu-id="5332f-142">None</span></span>

## <span data-ttu-id="5332f-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="5332f-143">OUTPUTS</span></span>

### <span data-ttu-id="5332f-144">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="5332f-144">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="5332f-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="5332f-145">NOTES</span></span>

## <span data-ttu-id="5332f-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5332f-146">RELATED LINKS</span></span>

[<span data-ttu-id="5332f-147">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="5332f-147">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="5332f-148">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="5332f-148">Set-AzSearchService</span></span>](./Set-AzSearchService.md)

[<span data-ttu-id="5332f-149">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="5332f-149">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)