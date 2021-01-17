---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/remove-azcognitiveservicesaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccountNetworkRule.md
ms.openlocfilehash: 2faf890cda0c87d15704a14f9c4ae12c5b3d81c2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434406"
---
# <span data-ttu-id="12f1e-101">Remove-AzCognitiveServicesAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="12f1e-101">Remove-AzCognitiveServicesAccountNetworkRule</span></span>

## <span data-ttu-id="12f1e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="12f1e-102">SYNOPSIS</span></span>
<span data-ttu-id="12f1e-103">Remova IpRules ou VirtualNetworkRules da propriedade NetWorkRule de uma conta de serviços cognitivas</span><span class="sxs-lookup"><span data-stu-id="12f1e-103">Remove IpRules or VirtualNetworkRules from the NetWorkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="12f1e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="12f1e-104">SYNTAX</span></span>

### <span data-ttu-id="12f1e-105">NetWorkRuleString (padrão)</span><span class="sxs-lookup"><span data-stu-id="12f1e-105">NetWorkRuleString (Default)</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="12f1e-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="12f1e-106">IpRuleObject</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IpRule <PSIpRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12f1e-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="12f1e-107">NetworkRuleObject</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="12f1e-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="12f1e-108">IpRuleString</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IpAddressOrRange <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="12f1e-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="12f1e-109">DESCRIPTION</span></span>
<span data-ttu-id="12f1e-110">O cmdlet **Remove-AzCognitiveServicesAccountNetworkRule** remove IpRules ou VirtualNetworkRules da propriedade NetWorkRule de uma conta de serviços cognitivas</span><span class="sxs-lookup"><span data-stu-id="12f1e-110">The **Remove-AzCognitiveServicesAccountNetworkRule** cmdlet removes IpRules or VirtualNetworkRules from the NetWorkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="12f1e-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="12f1e-111">EXAMPLES</span></span>

### <span data-ttu-id="12f1e-112">Exemplo 1: remover vários IpRules com IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="12f1e-112">Example 1: Remove several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpAddressOrRange "10.0.0.0/24,28.1.0.0/16"
```

<span data-ttu-id="12f1e-113">Esse comando Remove vários IpRules com IPAddressOrRange.</span><span class="sxs-lookup"><span data-stu-id="12f1e-113">This command remove several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="12f1e-114">Exemplo 2: remover um VirtualNetworkRule com a entrada de objeto VirtualNetworkRule com JSON</span><span class="sxs-lookup"><span data-stu-id="12f1e-114">Example 2: Remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON</span></span>
```
PS C:\>Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -VirtualNetworkRules (@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1"})
```

<span data-ttu-id="12f1e-115">Esse comando Remove um VirtualNetworkRule com a entrada do objeto VirtualNetworkRule com JSON.</span><span class="sxs-lookup"><span data-stu-id="12f1e-115">This command remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON.</span></span>

### <span data-ttu-id="12f1e-116">Exemplo 3: remover o primeiro IpRule com o pipeline</span><span class="sxs-lookup"><span data-stu-id="12f1e-116">Example 3: Remove first IpRule with pipeline</span></span>
```
PS C:\>(Get-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount").IpRules[0] | Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount"
```

<span data-ttu-id="12f1e-117">Este comando Remove Primeiro IpRule com pipeline.</span><span class="sxs-lookup"><span data-stu-id="12f1e-117">This command remove first IpRule with pipeline.</span></span>

### <span data-ttu-id="12f1e-118">Exemplo 4: remover vários VirtualNetworkRules com VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="12f1e-118">Example 4: Remove several VirtualNetworkRules with VirtualNetworkResourceID</span></span>
```
PS C:\>Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -VirtualNetworkResourceId "/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1","/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2"
```

<span data-ttu-id="12f1e-119">Esse comando Remove vários VirtualNetworkRules com VirtualNetworkResourceID.</span><span class="sxs-lookup"><span data-stu-id="12f1e-119">This command remove several VirtualNetworkRules with VirtualNetworkResourceID.</span></span> 

## <span data-ttu-id="12f1e-120">OS</span><span class="sxs-lookup"><span data-stu-id="12f1e-120">PARAMETERS</span></span>

### <span data-ttu-id="12f1e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12f1e-121">-DefaultProfile</span></span>
<span data-ttu-id="12f1e-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="12f1e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12f1e-123">-IpAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="12f1e-123">-IpAddressOrRange</span></span>
<span data-ttu-id="12f1e-124">Conta de serviços cognitiva NetworkRule IpRules IpAddressOrRange em cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="12f1e-124">Cognitive Services Account NetworkRule IpRules IpAddressOrRange in string.</span></span>

```yaml
Type: System.String[]
Parameter Sets: IpRuleString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12f1e-125">-IpRule</span><span class="sxs-lookup"><span data-stu-id="12f1e-125">-IpRule</span></span>
<span data-ttu-id="12f1e-126">Conta de serviços cognitiva NetworkRule IpRules.</span><span class="sxs-lookup"><span data-stu-id="12f1e-126">Cognitive Services Account NetworkRule IpRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]
Parameter Sets: IpRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12f1e-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="12f1e-127">-Name</span></span>
<span data-ttu-id="12f1e-128">Nome da conta de serviços cognitiva.</span><span class="sxs-lookup"><span data-stu-id="12f1e-128">Cognitive Services Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12f1e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12f1e-129">-ResourceGroupName</span></span>
<span data-ttu-id="12f1e-130">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="12f1e-130">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12f1e-131">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="12f1e-131">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="12f1e-132">Conta de serviços cognitiva NetworkRule VirtualNetworkRules VirtualNetworkResourceId em cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="12f1e-132">Cognitive Services Account NetworkRule VirtualNetworkRules VirtualNetworkResourceId in string.</span></span>

```yaml
Type: System.String[]
Parameter Sets: NetWorkRuleString
Aliases: SubnetId, VirtualNetworkId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12f1e-133">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="12f1e-133">-VirtualNetworkRule</span></span>
<span data-ttu-id="12f1e-134">Conta de serviços cognitiva NetworkRule VirtualNetworkRules.</span><span class="sxs-lookup"><span data-stu-id="12f1e-134">Cognitive Services Account NetworkRule VirtualNetworkRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]
Parameter Sets: NetworkRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12f1e-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="12f1e-135">-Confirm</span></span>
<span data-ttu-id="12f1e-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12f1e-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12f1e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12f1e-137">-WhatIf</span></span>
<span data-ttu-id="12f1e-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="12f1e-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12f1e-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="12f1e-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12f1e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12f1e-140">CommonParameters</span></span>
<span data-ttu-id="12f1e-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12f1e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12f1e-142">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="12f1e-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12f1e-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="12f1e-143">INPUTS</span></span>

### <span data-ttu-id="12f1e-144">System. String</span><span class="sxs-lookup"><span data-stu-id="12f1e-144">System.String</span></span>

### <span data-ttu-id="12f1e-145">Microsoft. Azure. Commands. Management. Cognitivaservices. Models. PSIpRule []</span><span class="sxs-lookup"><span data-stu-id="12f1e-145">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span></span>

### <span data-ttu-id="12f1e-146">Microsoft. Azure. Commands. Management. Cognitivaservices. Models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="12f1e-146">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="12f1e-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="12f1e-147">OUTPUTS</span></span>

### <span data-ttu-id="12f1e-148">Microsoft. Azure. Commands. Management. Cognitivaservices. Models. PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="12f1e-148">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="12f1e-149">Microsoft. Azure. Commands. Management. Cognitivaservices. Models. PSIpRule</span><span class="sxs-lookup"><span data-stu-id="12f1e-149">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule</span></span>

## <span data-ttu-id="12f1e-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="12f1e-150">NOTES</span></span>

## <span data-ttu-id="12f1e-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="12f1e-151">RELATED LINKS</span></span>
