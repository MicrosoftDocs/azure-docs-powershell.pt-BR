---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/add-azstorageaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountNetworkRule.md
ms.openlocfilehash: e1517801c964c4794c21ada6b7d64152c6e58178
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94283997"
---
# <span data-ttu-id="64abf-101">Add-AzStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="64abf-101">Add-AzStorageAccountNetworkRule</span></span>

## <span data-ttu-id="64abf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="64abf-102">SYNOPSIS</span></span>
 <span data-ttu-id="64abf-103">Adicionar IpRules ou VirtualNetworkRules à propriedade NetworkRule de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="64abf-103">Add IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="64abf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="64abf-104">SYNTAX</span></span>

### <span data-ttu-id="64abf-105">NetWorkRuleString (padrão)</span><span class="sxs-lookup"><span data-stu-id="64abf-105">NetWorkRuleString (Default)</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="64abf-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="64abf-106">IpRuleObject</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64abf-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="64abf-107">NetworkRuleObject</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64abf-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="64abf-108">IpRuleString</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPAddressOrRange <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64abf-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="64abf-109">DESCRIPTION</span></span>
<span data-ttu-id="64abf-110">O cmdlet **Add-AzStorageAccountNetworkRule** adiciona IpRules ou VirtualNetworkRules à propriedade NetworkRule de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="64abf-110">The **Add-AzStorageAccountNetworkRule** cmdlet adds IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="64abf-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="64abf-111">EXAMPLES</span></span>

### <span data-ttu-id="64abf-112">Exemplo 1: adicionar vários IpRules com IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="64abf-112">Example 1: Add several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -IPAddressOrRange "10.0.0.0/24","28.2.0.0/16"
```

<span data-ttu-id="64abf-113">Esse comando adiciona vários IpRules com IPAddressOrRange.</span><span class="sxs-lookup"><span data-stu-id="64abf-113">This command add several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="64abf-114">Exemplo 2: adicionar um VirtualNetworkRule com VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="64abf-114">Example 2: Add a VirtualNetworkRule with VirtualNetworkResourceID</span></span>
```
PS C:\>$subnet = Get-AzVirtualNetwork -ResourceGroupName "myResourceGroup" -Name "myvirtualnetwork" | Get-AzVirtualNetworkSubnetConfig
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -VirtualNetworkResourceId $subnet[0].Id
```

<span data-ttu-id="64abf-115">Esse comando adiciona um VirtualNetworkRule com VirtualNetworkResourceID.</span><span class="sxs-lookup"><span data-stu-id="64abf-115">This command add a VirtualNetworkRule with VirtualNetworkResourceID.</span></span>

### <span data-ttu-id="64abf-116">Exemplo 3: Adicionar VirtualNetworkRules com objetos VirtualNetworkRule de outra conta</span><span class="sxs-lookup"><span data-stu-id="64abf-116">Example 3: Add VirtualNetworkRules with VirtualNetworkRule Objects from another account</span></span>
```
PS C:\> $networkrule = Get-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "mystorageaccount1"
PS C:\> Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount2" -VirtualNetworkRule $networkrule.VirtualNetworkRules
```

<span data-ttu-id="64abf-117">Esse comando adiciona VirtualNetworkRules com objetos VirtualNetworkRule de outra conta.</span><span class="sxs-lookup"><span data-stu-id="64abf-117">This command add VirtualNetworkRules with VirtualNetworkRule Objects from another account.</span></span>

### <span data-ttu-id="64abf-118">Exemplo 4: adicionar vários IpRule com objetos IpRule, entrada com JSON</span><span class="sxs-lookup"><span data-stu-id="64abf-118">Example 4: Add several IpRule with IpRule objects, input with JSON</span></span>
```
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -IPRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
```

<span data-ttu-id="64abf-119">Esse comando adiciona vários IpRule com objetos IpRule, entrada com JSON.</span><span class="sxs-lookup"><span data-stu-id="64abf-119">This command add several IpRule with IpRule objects, input with JSON.</span></span>

## <span data-ttu-id="64abf-120">OS</span><span class="sxs-lookup"><span data-stu-id="64abf-120">PARAMETERS</span></span>

### <span data-ttu-id="64abf-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="64abf-121">-AsJob</span></span>
<span data-ttu-id="64abf-122">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="64abf-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="64abf-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64abf-123">-DefaultProfile</span></span>
<span data-ttu-id="64abf-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="64abf-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64abf-125">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="64abf-125">-IPAddressOrRange</span></span>
<span data-ttu-id="64abf-126">A matriz de IpAddressOrRange, adicione IpRules com o IpAddressOrRange de entrada e a ação padrão Allow à propriedade NetworkRule.</span><span class="sxs-lookup"><span data-stu-id="64abf-126">The Array of IpAddressOrRange, add IpRules with the input IpAddressOrRange and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="64abf-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="64abf-127">-IPRule</span></span>
<span data-ttu-id="64abf-128">A matriz de objetos IpRule para adicionar à propriedade NetworkRule.</span><span class="sxs-lookup"><span data-stu-id="64abf-128">The Array of IpRule objects to add to the NetworkRule Property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]
Parameter Sets: IpRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64abf-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="64abf-129">-Name</span></span>
<span data-ttu-id="64abf-130">Especifica o nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="64abf-130">Specifies the name of the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64abf-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64abf-131">-ResourceGroupName</span></span>
<span data-ttu-id="64abf-132">Especifica o nome do grupo de recursos que contém a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="64abf-132">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="64abf-133">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="64abf-133">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="64abf-134">A matriz de VirtualNetworkResourceId, adicionará VirtualNetworkRule com VirtualNetworkResourceId de entrada e a ação padrão permitir à propriedade NetworkRule.</span><span class="sxs-lookup"><span data-stu-id="64abf-134">The Array of VirtualNetworkResourceId, will add VirtualNetworkRule with input VirtualNetworkResourceId and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="64abf-135">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="64abf-135">-VirtualNetworkRule</span></span>
<span data-ttu-id="64abf-136">A matriz de objetos VirtualNetworkRule para adicionar à propriedade NetworkRule.</span><span class="sxs-lookup"><span data-stu-id="64abf-136">The Array of VirtualNetworkRule objects to add to the NetworkRule Property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]
Parameter Sets: NetworkRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64abf-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="64abf-137">-Confirm</span></span>
<span data-ttu-id="64abf-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64abf-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64abf-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64abf-139">-WhatIf</span></span>
<span data-ttu-id="64abf-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="64abf-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64abf-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="64abf-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64abf-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64abf-142">CommonParameters</span></span>
<span data-ttu-id="64abf-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64abf-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64abf-144">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64abf-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64abf-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="64abf-145">INPUTS</span></span>

### <span data-ttu-id="64abf-146">System. String</span><span class="sxs-lookup"><span data-stu-id="64abf-146">System.String</span></span>

### <span data-ttu-id="64abf-147">Microsoft. Azure. Commands. Management. Storage. Models. PSIpRule []</span><span class="sxs-lookup"><span data-stu-id="64abf-147">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>

### <span data-ttu-id="64abf-148">Microsoft. Azure. Commands. Management. Storage. Models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="64abf-148">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="64abf-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="64abf-149">OUTPUTS</span></span>

### <span data-ttu-id="64abf-150">Microsoft. Azure. Commands. Management. Storage. Models. PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="64abf-150">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="64abf-151">Microsoft. Azure. Commands. Management. Storage. Models. PSIpRule</span><span class="sxs-lookup"><span data-stu-id="64abf-151">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="64abf-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="64abf-152">NOTES</span></span>

## <span data-ttu-id="64abf-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="64abf-153">RELATED LINKS</span></span>
