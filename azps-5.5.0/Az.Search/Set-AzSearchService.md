---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/set-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchService.md
ms.openlocfilehash: 60969665c2989e026af3334e38e1d3035467b25b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111385"
---
# <span data-ttu-id="c8c08-101">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="c8c08-101">Set-AzSearchService</span></span>

## <span data-ttu-id="c8c08-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c8c08-102">SYNOPSIS</span></span>
<span data-ttu-id="c8c08-103">Atualizar um serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="c8c08-103">Update an Azure Cognitive Search service.</span></span>

## <span data-ttu-id="c8c08-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c8c08-104">SYNTAX</span></span>

### <span data-ttu-id="c8c08-105">ResourceNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c8c08-105">ResourceNameParameterSet (Default)</span></span>
```
Set-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-PartitionCount <Int32>]
 [-ReplicaCount <Int32>] [-PublicNetworkAccess <PSPublicNetworkAccess>] [-IdentityType <PSIdentityType>]
 [-IPRuleList <PSIpRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c8c08-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8c08-106">InputObjectParameterSet</span></span>
```
Set-AzSearchService [-InputObject] <PSSearchService> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-PublicNetworkAccess <PSPublicNetworkAccess>] [-IdentityType <PSIdentityType>] [-IPRuleList <PSIpRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8c08-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8c08-107">ResourceIdParameterSet</span></span>
```
Set-AzSearchService [-ResourceId] <String> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-PublicNetworkAccess <PSPublicNetworkAccess>] [-IdentityType <PSIdentityType>] [-IPRuleList <PSIpRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8c08-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="c8c08-108">DESCRIPTION</span></span>
<span data-ttu-id="c8c08-109">O **cmdlet Set-AzSearchService** modifica um serviço de Pesquisa Cognitiva do Azure.</span><span class="sxs-lookup"><span data-stu-id="c8c08-109">The **Set-AzSearchService** cmdlet modifies an Azure Cognitive Search service.</span></span>

## <span data-ttu-id="c8c08-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c8c08-110">EXAMPLES</span></span>

### <span data-ttu-id="c8c08-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c8c08-111">Example 1</span></span>
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

<span data-ttu-id="c8c08-112">O exemplo altera a contagem de partições e a contagem de réplicas do serviço pesquisa cognitiva do Azure para 2.</span><span class="sxs-lookup"><span data-stu-id="c8c08-112">The example changes partition count and replica count of the Azure Cognitive Search service to 2.</span></span>

## <span data-ttu-id="c8c08-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c8c08-113">PARAMETERS</span></span>

### <span data-ttu-id="c8c08-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8c08-114">-DefaultProfile</span></span>
<span data-ttu-id="c8c08-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c8c08-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8c08-116">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="c8c08-116">-IdentityType</span></span>
<span data-ttu-id="c8c08-117">(Opcional) Identidade do Serviço de Pesquisa Cognitiva do Azure (Nenhum/SystemAssigned)</span><span class="sxs-lookup"><span data-stu-id="c8c08-117">(Optional) Azure Cognitive Search Service Identity (None/SystemAssigned)</span></span>

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

### <span data-ttu-id="c8c08-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c8c08-118">-InputObject</span></span>
<span data-ttu-id="c8c08-119">Objeto de Entrada do Serviço de Pesquisa.</span><span class="sxs-lookup"><span data-stu-id="c8c08-119">Search Service Input Object.</span></span>

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

### <span data-ttu-id="c8c08-120">-IPRuleList</span><span class="sxs-lookup"><span data-stu-id="c8c08-120">-IPRuleList</span></span>
<span data-ttu-id="c8c08-121">(Opcional) Regras ip do Serviço de Pesquisa Cognitiva do Azure</span><span class="sxs-lookup"><span data-stu-id="c8c08-121">(Optional) Azure Cognitive Search Service IP rules</span></span>

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

### <span data-ttu-id="c8c08-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="c8c08-122">-Name</span></span>
<span data-ttu-id="c8c08-123">Nome do serviço de pesquisa.</span><span class="sxs-lookup"><span data-stu-id="c8c08-123">Search Service name.</span></span>

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

### <span data-ttu-id="c8c08-124">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="c8c08-124">-PartitionCount</span></span>
<span data-ttu-id="c8c08-125">Pesquisar contagem de partição do serviço.</span><span class="sxs-lookup"><span data-stu-id="c8c08-125">Search Service partition count.</span></span>

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

### <span data-ttu-id="c8c08-126">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="c8c08-126">-PublicNetworkAccess</span></span>
<span data-ttu-id="c8c08-127">(Opcional) Acesso à rede pública do Serviço de Pesquisa Cognitiva do Azure (Habilitado/Desabilitado)</span><span class="sxs-lookup"><span data-stu-id="c8c08-127">(Optional) Azure Cognitive Search Service public network access (Enabled/Disabled)</span></span>

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

### <span data-ttu-id="c8c08-128">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="c8c08-128">-ReplicaCount</span></span>
<span data-ttu-id="c8c08-129">Contagem de replicas do Serviço de Pesquisa.</span><span class="sxs-lookup"><span data-stu-id="c8c08-129">Search Service replica count.</span></span>

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

### <span data-ttu-id="c8c08-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8c08-130">-ResourceGroupName</span></span>
<span data-ttu-id="c8c08-131">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="c8c08-131">Resource Group name.</span></span>

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

### <span data-ttu-id="c8c08-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c8c08-132">-ResourceId</span></span>
<span data-ttu-id="c8c08-133">Pesquisar ID de Recurso do Serviço.</span><span class="sxs-lookup"><span data-stu-id="c8c08-133">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="c8c08-134">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="c8c08-134">-Confirm</span></span>
<span data-ttu-id="c8c08-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8c08-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8c08-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8c08-136">-WhatIf</span></span>
<span data-ttu-id="c8c08-137">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="c8c08-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c8c08-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c8c08-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8c08-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8c08-139">CommonParameters</span></span>
<span data-ttu-id="c8c08-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8c08-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8c08-141">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c8c08-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8c08-142">Entradas</span><span class="sxs-lookup"><span data-stu-id="c8c08-142">INPUTS</span></span>

### <span data-ttu-id="c8c08-143">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="c8c08-143">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="c8c08-144">System.String</span><span class="sxs-lookup"><span data-stu-id="c8c08-144">System.String</span></span>

## <span data-ttu-id="c8c08-145">Saídas</span><span class="sxs-lookup"><span data-stu-id="c8c08-145">OUTPUTS</span></span>

### <span data-ttu-id="c8c08-146">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="c8c08-146">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="c8c08-147">Notas</span><span class="sxs-lookup"><span data-stu-id="c8c08-147">NOTES</span></span>

## <span data-ttu-id="c8c08-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c8c08-148">RELATED LINKS</span></span>

[<span data-ttu-id="c8c08-149">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="c8c08-149">New-AzSearchService</span></span>](./New-AzSearchService.md)

[<span data-ttu-id="c8c08-150">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="c8c08-150">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="c8c08-151">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="c8c08-151">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)