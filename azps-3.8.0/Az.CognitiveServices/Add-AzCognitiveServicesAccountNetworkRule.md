---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/add-azcognitiveservicesaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Add-AzCognitiveServicesAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Add-AzCognitiveServicesAccountNetworkRule.md
ms.openlocfilehash: 039a3e4bf676f29d55f48e7e0883f5818e7367b7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940320"
---
# <span data-ttu-id="14019-101">Add-AzCognitiveServicesAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="14019-101">Add-AzCognitiveServicesAccountNetworkRule</span></span>

## <span data-ttu-id="14019-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="14019-102">SYNOPSIS</span></span>
<span data-ttu-id="14019-103">Adicione IpRules ou VirtualNetworkRules à propriedade NetworkRule de uma conta de serviços cognitivas</span><span class="sxs-lookup"><span data-stu-id="14019-103">Add IpRules or VirtualNetworkRules to the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="14019-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="14019-104">SYNTAX</span></span>

### <span data-ttu-id="14019-105">NetWorkRuleString (padrão)</span><span class="sxs-lookup"><span data-stu-id="14019-105">NetWorkRuleString (Default)</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="14019-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="14019-106">IpRuleObject</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IpRule <PSIpRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14019-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="14019-107">NetworkRuleObject</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="14019-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="14019-108">IpRuleString</span></span>
```
Add-AzCognitiveServicesAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IpAddressOrRange <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="14019-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="14019-109">DESCRIPTION</span></span>
<span data-ttu-id="14019-110">O cmdlet **Add-AzCognitiveServicesAccountNetworkRule** adiciona IpRules ou VirtualNetworkRules à propriedade NetworkRule de uma conta de serviços cognitivas</span><span class="sxs-lookup"><span data-stu-id="14019-110">The **Add-AzCognitiveServicesAccountNetworkRule** cmdlet adds IpRules or VirtualNetworkRules to the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="14019-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="14019-111">EXAMPLES</span></span>

### <span data-ttu-id="14019-112">Exemplo 1: adicionar vários IpRules com IpAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="14019-112">Example 1: Add several IpRules with IpAddressOrRange</span></span>
```
PS C:\>Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpAddressOrRange "200.0.0.0/24","28.2.0.0/16"
```

<span data-ttu-id="14019-113">Esse comando adiciona vários IpRules com IpAddressOrRange.</span><span class="sxs-lookup"><span data-stu-id="14019-113">This command add several IpRules with IpAddressOrRange.</span></span>

### <span data-ttu-id="14019-114">Exemplo 2: adicionar um VirtualNetworkRule com VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="14019-114">Example 2: Add a VirtualNetworkRule with VirtualNetworkResourceID</span></span>
```
PS C:\>$subnet = Get-AzVirtualNetwork -ResourceGroupName "myResourceGroup" -Name "myvirtualnetwork" | Get-AzVirtualNetworkSubnetConfig
PS C:\>Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -VirtualNetworkResourceId $subnet[0].Id
```

<span data-ttu-id="14019-115">Esse comando adiciona um VirtualNetworkRule com VirtualNetworkResourceID.</span><span class="sxs-lookup"><span data-stu-id="14019-115">This command add a VirtualNetworkRule with VirtualNetworkResourceID.</span></span>

### <span data-ttu-id="14019-116">Exemplo 3: Adicionar VirtualNetworkRules com objetos VirtualNetworkRule de outra conta</span><span class="sxs-lookup"><span data-stu-id="14019-116">Example 3: Add VirtualNetworkRules with VirtualNetworkRule Objects from another account</span></span>
```
PS C:\> $networkrule = Get-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount1"
PS C:\> Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount2" -VirtualNetworkRule $networkrule.VirtualNetworkRules
```

<span data-ttu-id="14019-117">Esse comando adiciona VirtualNetworkRules com objetos VirtualNetworkRule de outra conta.</span><span class="sxs-lookup"><span data-stu-id="14019-117">This command add VirtualNetworkRules with VirtualNetworkRule Objects from another account.</span></span>

### <span data-ttu-id="14019-118">Exemplo 4: adicionar vários IpRule com objetos IpRule, entrada com JSON</span><span class="sxs-lookup"><span data-stu-id="14019-118">Example 4: Add several IpRule with IpRule objects, input with JSON</span></span>
```
PS C:\>Add-AzCognitiveServicesAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpRule (@{IpAddressOrRange="200.0.0.0/24"},@{IpAddressOrRange="28.2.0.0/16"})
```

<span data-ttu-id="14019-119">Esse comando adiciona vários IpRule com objetos IpRule, entrada com JSON.</span><span class="sxs-lookup"><span data-stu-id="14019-119">This command add several IpRule with IpRule objects, input with JSON.</span></span>

## <span data-ttu-id="14019-120">OS</span><span class="sxs-lookup"><span data-stu-id="14019-120">PARAMETERS</span></span>

### <span data-ttu-id="14019-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14019-121">-DefaultProfile</span></span>
<span data-ttu-id="14019-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="14019-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14019-123">-IpAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="14019-123">-IpAddressOrRange</span></span>
<span data-ttu-id="14019-124">Conta de serviços cognitiva NetworkRule IpRules IpAddressOrRange em cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="14019-124">Cognitive Services Account NetworkRule IpRules IpAddressOrRange in string.</span></span>

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

### <span data-ttu-id="14019-125">-IpRule</span><span class="sxs-lookup"><span data-stu-id="14019-125">-IpRule</span></span>
<span data-ttu-id="14019-126">Conta de serviços cognitiva NetworkRule IpRules.</span><span class="sxs-lookup"><span data-stu-id="14019-126">Cognitive Services Account NetworkRule IpRules.</span></span>

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

### <span data-ttu-id="14019-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="14019-127">-Name</span></span>
<span data-ttu-id="14019-128">Nome da conta de serviços cognitiva.</span><span class="sxs-lookup"><span data-stu-id="14019-128">Cognitive Services Account Name.</span></span>

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

### <span data-ttu-id="14019-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14019-129">-ResourceGroupName</span></span>
<span data-ttu-id="14019-130">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="14019-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="14019-131">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="14019-131">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="14019-132">Conta de serviços cognitiva NetworkRule VirtualNetworkRules VirtualNetworkResourceId em cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="14019-132">Cognitive Services Account NetworkRule VirtualNetworkRules VirtualNetworkResourceId in string.</span></span>

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

### <span data-ttu-id="14019-133">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="14019-133">-VirtualNetworkRule</span></span>
<span data-ttu-id="14019-134">Conta de serviços cognitiva NetworkRule VirtualNetworkRules.</span><span class="sxs-lookup"><span data-stu-id="14019-134">Cognitive Services Account NetworkRule VirtualNetworkRules.</span></span>

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

### <span data-ttu-id="14019-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="14019-135">-Confirm</span></span>
<span data-ttu-id="14019-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14019-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14019-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14019-137">-WhatIf</span></span>
<span data-ttu-id="14019-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="14019-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14019-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="14019-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14019-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14019-140">CommonParameters</span></span>
<span data-ttu-id="14019-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14019-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14019-142">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="14019-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14019-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="14019-143">INPUTS</span></span>

### <span data-ttu-id="14019-144">System. String</span><span class="sxs-lookup"><span data-stu-id="14019-144">System.String</span></span>

### <span data-ttu-id="14019-145">Microsoft. Azure. Commands. Management. Cognitivaservices. Models. PSIpRule []</span><span class="sxs-lookup"><span data-stu-id="14019-145">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span></span>

### <span data-ttu-id="14019-146">Microsoft. Azure. Commands. Management. Cognitivaservices. Models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="14019-146">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="14019-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="14019-147">OUTPUTS</span></span>

### <span data-ttu-id="14019-148">Microsoft. Azure. Commands. Management. Cognitivaservices. Models. PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="14019-148">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="14019-149">Microsoft. Azure. Commands. Management. Cognitivaservices. Models. PSIpRule</span><span class="sxs-lookup"><span data-stu-id="14019-149">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule</span></span>

## <span data-ttu-id="14019-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="14019-150">NOTES</span></span>

## <span data-ttu-id="14019-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="14019-151">RELATED LINKS</span></span>
