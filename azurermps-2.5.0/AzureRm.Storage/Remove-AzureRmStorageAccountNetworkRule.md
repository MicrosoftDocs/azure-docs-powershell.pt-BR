---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/remove-azurermstorageaccountnetworkrule
schema: 2.0.0
ms.openlocfilehash: 6fd79e458c4ac288c6bc8f26add140e8f0a695ca
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785290"
---
# <span data-ttu-id="cbcf9-101">Remove-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="cbcf9-101">Remove-AzureRmStorageAccountNetworkRule</span></span>

## <span data-ttu-id="cbcf9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cbcf9-102">SYNOPSIS</span></span>
<span data-ttu-id="cbcf9-103">Remover IpRules ou VirtualNetworkRules da propriedade NetWorkRule de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="cbcf9-103">Remove IpRules or VirtualNetworkRules from the NetWorkRule property of a Storage account</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cbcf9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cbcf9-104">SYNTAX</span></span>

### <span data-ttu-id="cbcf9-105">NetWorkRuleString (padrão)</span><span class="sxs-lookup"><span data-stu-id="cbcf9-105">NetWorkRuleString (Default)</span></span>
```
Remove-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cbcf9-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="cbcf9-106">IpRuleObject</span></span>
```
Remove-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbcf9-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="cbcf9-107">NetworkRuleObject</span></span>
```
Remove-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbcf9-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="cbcf9-108">IpRuleString</span></span>
```
Remove-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IPAddressOrRange <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cbcf9-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cbcf9-109">DESCRIPTION</span></span>
<span data-ttu-id="cbcf9-110">O cmdlet **Remove-AzureRmStorageAccountNetworkRule** remove IpRules ou VirtualNetworkRules da propriedade NetWorkRule de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="cbcf9-110">The **Remove-AzureRmStorageAccountNetworkRule** cmdlet removes IpRules or VirtualNetworkRules from the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="cbcf9-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cbcf9-111">EXAMPLES</span></span>

### <span data-ttu-id="cbcf9-112">Exemplo 1: remover vários IpRules com IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="cbcf9-112">Example 1: Remove several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Remove-AzureRmStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -IPAddressOrRange "10.0.0.0/24,28.1.0.0/16"
```

<span data-ttu-id="cbcf9-113">Esse comando Remove vários IpRules com IPAddressOrRange.</span><span class="sxs-lookup"><span data-stu-id="cbcf9-113">This command remove several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="cbcf9-114">Exemplo 2: remover um VirtualNetworkRule com a entrada de objeto VirtualNetworkRule com JSON</span><span class="sxs-lookup"><span data-stu-id="cbcf9-114">Example 2: Remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON</span></span>
```
PS C:\>Remove-AzureRmStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -VirtualNetworkRules (@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"})
```

<span data-ttu-id="cbcf9-115">Esse comando Remove um VirtualNetworkRule com a entrada do objeto VirtualNetworkRule com JSON.</span><span class="sxs-lookup"><span data-stu-id="cbcf9-115">This command remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON.</span></span>

### <span data-ttu-id="cbcf9-116">Exemplo 3: remover o primeiro IpRule com o pipeline</span><span class="sxs-lookup"><span data-stu-id="cbcf9-116">Example 3: Remove first IpRule with pipeline</span></span>
```
PS C:\>(Get-AzureRmStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount").IpRules[0] | Remove-AzureRmStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
```

<span data-ttu-id="cbcf9-117">Este comando Remove Primeiro IpRule com pipeline.</span><span class="sxs-lookup"><span data-stu-id="cbcf9-117">This command remove first IpRule with pipeline.</span></span>

### <span data-ttu-id="cbcf9-118">Exemplo 4: remover vários VirtualNetworkRules com VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="cbcf9-118">Example 4: Remove several VirtualNetworkRules with VirtualNetworkResourceID</span></span>
```
PS C:\>Remove-AzureRmStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -VirtualNetworkResourceId "/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1","/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2"
```

<span data-ttu-id="cbcf9-119">Esse comando Remove vários VirtualNetworkRules com VirtualNetworkResourceID.</span><span class="sxs-lookup"><span data-stu-id="cbcf9-119">This command remove several VirtualNetworkRules with VirtualNetworkResourceID.</span></span>

## <span data-ttu-id="cbcf9-120">OS</span><span class="sxs-lookup"><span data-stu-id="cbcf9-120">PARAMETERS</span></span>

### <span data-ttu-id="cbcf9-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cbcf9-121">-AsJob</span></span>
<span data-ttu-id="cbcf9-122">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="cbcf9-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cbcf9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbcf9-123">-DefaultProfile</span></span>
<span data-ttu-id="cbcf9-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cbcf9-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbcf9-125">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="cbcf9-125">-IPAddressOrRange</span></span>
<span data-ttu-id="cbcf9-126">A matriz de IpAddressOrRange irá remover IpRule com o mesmo IpAddressOrRange da propriedade NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="cbcf9-126">The Array of IpAddressOrRange, will remove IpRule with same IpAddressOrRange from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="cbcf9-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="cbcf9-127">-IPRule</span></span>
<span data-ttu-id="cbcf9-128">A matriz de objetos IpRule a serem removidos da propriedade NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="cbcf9-128">The Array of IpRule objects to remove from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="cbcf9-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="cbcf9-129">-Name</span></span>
<span data-ttu-id="cbcf9-130">Especifica o nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="cbcf9-130">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="cbcf9-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbcf9-131">-ResourceGroupName</span></span>
<span data-ttu-id="cbcf9-132">Especifica o nome do grupo de recursos que contém a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="cbcf9-132">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="cbcf9-133">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="cbcf9-133">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="cbcf9-134">A matriz de VirtualNetworkResourceId irá remover VirtualNetworkRule com o mesmo VirtualNetworkResourceId da propriedade NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="cbcf9-134">The Array of VirtualNetworkResourceId, will remove VirtualNetworkRule with same VirtualNetworkResourceId from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="cbcf9-135">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="cbcf9-135">-VirtualNetworkRule</span></span>
<span data-ttu-id="cbcf9-136">A matriz de objetos VirtualNetworkRule a serem removidos da propriedade NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="cbcf9-136">The Array of VirtualNetworkRule objects to remove from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="cbcf9-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="cbcf9-137">-Confirm</span></span>
<span data-ttu-id="cbcf9-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cbcf9-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbcf9-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbcf9-139">-WhatIf</span></span>
<span data-ttu-id="cbcf9-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cbcf9-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cbcf9-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cbcf9-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbcf9-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbcf9-142">CommonParameters</span></span>
<span data-ttu-id="cbcf9-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbcf9-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbcf9-144">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbcf9-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbcf9-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cbcf9-145">INPUTS</span></span>

### <span data-ttu-id="cbcf9-146">System. String</span><span class="sxs-lookup"><span data-stu-id="cbcf9-146">System.String</span></span>

### <span data-ttu-id="cbcf9-147">Microsoft. Azure. Commands. Management. Storage. Models. PSIpRule []</span><span class="sxs-lookup"><span data-stu-id="cbcf9-147">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>
<span data-ttu-id="cbcf9-148">Parâmetros: IPRule (ByValue)</span><span class="sxs-lookup"><span data-stu-id="cbcf9-148">Parameters: IPRule (ByValue)</span></span>

### <span data-ttu-id="cbcf9-149">Microsoft. Azure. Commands. Management. Storage. Models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="cbcf9-149">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>
<span data-ttu-id="cbcf9-150">Parâmetros: VirtualNetworkRule (ByValue)</span><span class="sxs-lookup"><span data-stu-id="cbcf9-150">Parameters: VirtualNetworkRule (ByValue)</span></span>

## <span data-ttu-id="cbcf9-151">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cbcf9-151">OUTPUTS</span></span>

### <span data-ttu-id="cbcf9-152">Microsoft. Azure. Commands. Management. Storage. Models. PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="cbcf9-152">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="cbcf9-153">Microsoft. Azure. Commands. Management. Storage. Models. PSIpRule</span><span class="sxs-lookup"><span data-stu-id="cbcf9-153">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="cbcf9-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cbcf9-154">NOTES</span></span>

## <span data-ttu-id="cbcf9-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cbcf9-155">RELATED LINKS</span></span>
