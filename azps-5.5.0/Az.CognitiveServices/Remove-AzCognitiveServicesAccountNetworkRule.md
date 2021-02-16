---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/remove-azcognitiveservicesaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Remove-AzCognitiveServicesAccountNetworkRule.md
ms.openlocfilehash: 2faf890cda0c87d15704a14f9c4ae12c5b3d81c2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117889"
---
# <span data-ttu-id="cd336-101">Remove-AzCognitiveServicesAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="cd336-101">Remove-AzCognitiveServicesAccountNetworkRule</span></span>

## <span data-ttu-id="cd336-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cd336-102">SYNOPSIS</span></span>
<span data-ttu-id="cd336-103">Remover IpRules ou VirtualNetworkRules da propriedade NetWorkRule de uma conta do Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="cd336-103">Remove IpRules or VirtualNetworkRules from the NetWorkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="cd336-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cd336-104">SYNTAX</span></span>

### <span data-ttu-id="cd336-105">NetWorkRuleString (Padrão)</span><span class="sxs-lookup"><span data-stu-id="cd336-105">NetWorkRuleString (Default)</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cd336-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="cd336-106">IpRuleObject</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IpRule <PSIpRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd336-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="cd336-107">NetworkRuleObject</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cd336-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="cd336-108">IpRuleString</span></span>
```
Remove-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IpAddressOrRange <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cd336-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="cd336-109">DESCRIPTION</span></span>
<span data-ttu-id="cd336-110">O cmdlet **Remove-AzCognitiveServicesAccountNetworkRule** remove IpRules ou VirtualNetworkRules da propriedade NetWorkRule de uma conta do Cognitive Services</span><span class="sxs-lookup"><span data-stu-id="cd336-110">The **Remove-AzCognitiveServicesAccountNetworkRule** cmdlet removes IpRules or VirtualNetworkRules from the NetWorkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="cd336-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="cd336-111">EXAMPLES</span></span>

### <span data-ttu-id="cd336-112">Exemplo 1: Remover vários IpRules com IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="cd336-112">Example 1: Remove several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpAddressOrRange "10.0.0.0/24,28.1.0.0/16"
```

<span data-ttu-id="cd336-113">Esse comando remove vários IpRules com IPAddressOrRange.</span><span class="sxs-lookup"><span data-stu-id="cd336-113">This command remove several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="cd336-114">Exemplo 2: Remover uma VirtualNetworkRule com entrada de Objeto VirtualNetworkRule com JSON</span><span class="sxs-lookup"><span data-stu-id="cd336-114">Example 2: Remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON</span></span>
```
PS C:\>Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -VirtualNetworkRules (@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1"})
```

<span data-ttu-id="cd336-115">Esse comando remove uma VirtualNetworkRule com entrada de Objeto VirtualNetworkRule com JSON.</span><span class="sxs-lookup"><span data-stu-id="cd336-115">This command remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON.</span></span>

### <span data-ttu-id="cd336-116">Exemplo 3: Remover o primeiro IpRule com pipeline</span><span class="sxs-lookup"><span data-stu-id="cd336-116">Example 3: Remove first IpRule with pipeline</span></span>
```
PS C:\>(Get-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount").IpRules[0] | Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount"
```

<span data-ttu-id="cd336-117">Este comando remove o primeiro IpRule com pipeline.</span><span class="sxs-lookup"><span data-stu-id="cd336-117">This command remove first IpRule with pipeline.</span></span>

### <span data-ttu-id="cd336-118">Exemplo 4: Remover várias VirtualNetworkRules com o VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="cd336-118">Example 4: Remove several VirtualNetworkRules with VirtualNetworkResourceID</span></span>
```
PS C:\>Remove-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -VirtualNetworkResourceId "/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1","/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2"
```

<span data-ttu-id="cd336-119">Este comando remove várias VirtualNetworkRules com VirtualNetworkResourceID.</span><span class="sxs-lookup"><span data-stu-id="cd336-119">This command remove several VirtualNetworkRules with VirtualNetworkResourceID.</span></span> 

## <span data-ttu-id="cd336-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cd336-120">PARAMETERS</span></span>

### <span data-ttu-id="cd336-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd336-121">-DefaultProfile</span></span>
<span data-ttu-id="cd336-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cd336-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd336-123">-IpAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="cd336-123">-IpAddressOrRange</span></span>
<span data-ttu-id="cd336-124">Conta cognitiva NetworkRule IpRules IpAddressOrRange em cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="cd336-124">Cognitive Services Account NetworkRule IpRules IpAddressOrRange in string.</span></span>

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

### <span data-ttu-id="cd336-125">-IpRule</span><span class="sxs-lookup"><span data-stu-id="cd336-125">-IpRule</span></span>
<span data-ttu-id="cd336-126">IpRules networkrule da conta dos Serviços Cognitivas.</span><span class="sxs-lookup"><span data-stu-id="cd336-126">Cognitive Services Account NetworkRule IpRules.</span></span>

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

### <span data-ttu-id="cd336-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="cd336-127">-Name</span></span>
<span data-ttu-id="cd336-128">Nome da conta do Serviço Cognitiva.</span><span class="sxs-lookup"><span data-stu-id="cd336-128">Cognitive Services Account Name.</span></span>

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

### <span data-ttu-id="cd336-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd336-129">-ResourceGroupName</span></span>
<span data-ttu-id="cd336-130">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cd336-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="cd336-131">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="cd336-131">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="cd336-132">Conta cognitiva NetworkRule VirtualNetworkRules VirtualNetworkResourceId na cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="cd336-132">Cognitive Services Account NetworkRule VirtualNetworkRules VirtualNetworkResourceId in string.</span></span>

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

### <span data-ttu-id="cd336-133">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="cd336-133">-VirtualNetworkRule</span></span>
<span data-ttu-id="cd336-134">Conta cognitiva NetworkRule VirtualNetworkRules.</span><span class="sxs-lookup"><span data-stu-id="cd336-134">Cognitive Services Account NetworkRule VirtualNetworkRules.</span></span>

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

### <span data-ttu-id="cd336-135">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="cd336-135">-Confirm</span></span>
<span data-ttu-id="cd336-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd336-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd336-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd336-137">-WhatIf</span></span>
<span data-ttu-id="cd336-138">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="cd336-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd336-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cd336-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd336-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd336-140">CommonParameters</span></span>
<span data-ttu-id="cd336-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd336-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd336-142">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cd336-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd336-143">Entradas</span><span class="sxs-lookup"><span data-stu-id="cd336-143">INPUTS</span></span>

### <span data-ttu-id="cd336-144">System.String</span><span class="sxs-lookup"><span data-stu-id="cd336-144">System.String</span></span>

### <span data-ttu-id="cd336-145">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span><span class="sxs-lookup"><span data-stu-id="cd336-145">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span></span>

### <span data-ttu-id="cd336-146">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span><span class="sxs-lookup"><span data-stu-id="cd336-146">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="cd336-147">Saídas</span><span class="sxs-lookup"><span data-stu-id="cd336-147">OUTPUTS</span></span>

### <span data-ttu-id="cd336-148">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="cd336-148">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="cd336-149">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule</span><span class="sxs-lookup"><span data-stu-id="cd336-149">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule</span></span>

## <span data-ttu-id="cd336-150">Notas</span><span class="sxs-lookup"><span data-stu-id="cd336-150">NOTES</span></span>

## <span data-ttu-id="cd336-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cd336-151">RELATED LINKS</span></span>
