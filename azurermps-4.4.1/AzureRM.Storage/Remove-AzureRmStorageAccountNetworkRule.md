---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageAccountNetworkRule.md
ms.openlocfilehash: abfd6f06a0d3f81c84f79e4a5fa6870ad60ba18d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603089"
---
# <span data-ttu-id="5fbc7-101">Remove-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="5fbc7-101">Remove-AzureRmStorageAccountNetworkRule</span></span>

## <span data-ttu-id="5fbc7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5fbc7-102">SYNOPSIS</span></span>
<span data-ttu-id="5fbc7-103">Remover IpRules ou VirtualNetworkRules da propriedade NetWorkRule de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="5fbc7-103">Remove IpRules or VirtualNetworkRules from the NetWorkRule property of a Storage Account</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5fbc7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5fbc7-104">SYNTAX</span></span>

### <span data-ttu-id="5fbc7-105">NetWorkRuleString (padrão)</span><span class="sxs-lookup"><span data-stu-id="5fbc7-105">NetWorkRuleString (Default)</span></span>
```
Remove-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5fbc7-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="5fbc7-106">IpRuleObject</span></span>
```
Remove-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5fbc7-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="5fbc7-107">NetworkRuleObject</span></span>
```
Remove-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5fbc7-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="5fbc7-108">IpRuleString</span></span>
```
Remove-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IPAddressOrRange <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5fbc7-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5fbc7-109">DESCRIPTION</span></span>
<span data-ttu-id="5fbc7-110">O cmdlet **Remove-AzureRmStorageAccountNetworkRule** remove IpRules ou VirtualNetworkRules da propriedade NetWorkRule de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="5fbc7-110">The **Remove-AzureRmStorageAccountNetworkRule** cmdlet removes IpRules or VirtualNetworkRules from the NetWorkRule property of a Storage Account</span></span>

## <span data-ttu-id="5fbc7-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5fbc7-111">EXAMPLES</span></span>

### <span data-ttu-id="5fbc7-112">Exemplo 1: remover vários IpRules com IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="5fbc7-112">Example 1: Remove several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Remove-AzureRmStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -IPAddressOrRange "10.0.0.0/24,28.1.0.0/16"
```

<span data-ttu-id="5fbc7-113">Esse comando Remove vários IpRules com IPAddressOrRange.</span><span class="sxs-lookup"><span data-stu-id="5fbc7-113">This command remove several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="5fbc7-114">Exemplo 2: remover um VirtualNetworkRule com a entrada de objeto VirtualNetworkRule com JSON</span><span class="sxs-lookup"><span data-stu-id="5fbc7-114">Example 2: Remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON</span></span>
```
PS C:\>Remove-AzureRmStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -VirtualNetworkRules (@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"})
```

<span data-ttu-id="5fbc7-115">Esse comando Remove um VirtualNetworkRule com a entrada do objeto VirtualNetworkRule com JSON.</span><span class="sxs-lookup"><span data-stu-id="5fbc7-115">This command remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON.</span></span>

### <span data-ttu-id="5fbc7-116">Exemplo 3: remover o primeiro IpRule com o pipeline</span><span class="sxs-lookup"><span data-stu-id="5fbc7-116">Example 3: Remove first IpRule with pipeline</span></span>
```
PS C:\>(Get-AzureRmStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount").IpRules[0] | Remove-AzureRmStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
```

<span data-ttu-id="5fbc7-117">Este comando Remove Primeiro IpRule com pipeline.</span><span class="sxs-lookup"><span data-stu-id="5fbc7-117">This command remove first IpRule with pipeline.</span></span>

### <span data-ttu-id="5fbc7-118">Exemplo 4: remover vários VirtualNetworkRules com VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="5fbc7-118">Example 4: Remove several VirtualNetworkRules with VirtualNetworkResourceID</span></span>
```
PS C:\>Remove-AzureRmStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -VirtualNetworkResourceId "/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1","/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2"
```

<span data-ttu-id="5fbc7-119">Esse comando Remove vários VirtualNetworkRules com VirtualNetworkResourceID.</span><span class="sxs-lookup"><span data-stu-id="5fbc7-119">This command remove several VirtualNetworkRules with VirtualNetworkResourceID.</span></span>

## <span data-ttu-id="5fbc7-120">OS</span><span class="sxs-lookup"><span data-stu-id="5fbc7-120">PARAMETERS</span></span>

### <span data-ttu-id="5fbc7-121">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="5fbc7-121">-IPAddressOrRange</span></span>
<span data-ttu-id="5fbc7-122">A matriz de IpAddressOrRange irá remover IpRule com o mesmo IpAddressOrRange da propriedade NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="5fbc7-122">The Array of IpAddressOrRange, will remove IpRule with same IpAddressOrRange from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="5fbc7-123">-IPRule</span><span class="sxs-lookup"><span data-stu-id="5fbc7-123">-IPRule</span></span>
<span data-ttu-id="5fbc7-124">A matriz de objetos IpRule a serem removidos da propriedade NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="5fbc7-124">The Array of IpRule objects to remove from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="5fbc7-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="5fbc7-125">-Name</span></span>
<span data-ttu-id="5fbc7-126">Especifica o nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="5fbc7-126">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="5fbc7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5fbc7-127">-ResourceGroupName</span></span>
<span data-ttu-id="5fbc7-128">Especifica o nome do grupo de recursos que contém a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="5fbc7-128">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="5fbc7-129">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="5fbc7-129">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="5fbc7-130">A matriz de VirtualNetworkResourceId irá remover VirtualNetworkRule com o mesmo VirtualNetworkResourceId da propriedade NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="5fbc7-130">The Array of VirtualNetworkResourceId, will remove VirtualNetworkRule with same VirtualNetworkResourceId from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="5fbc7-131">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="5fbc7-131">-VirtualNetworkRule</span></span>
<span data-ttu-id="5fbc7-132">A matriz de objetos VirtualNetworkRule a serem removidos da propriedade NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="5fbc7-132">The Array of VirtualNetworkRule objects to remove from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="5fbc7-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5fbc7-133">-Confirm</span></span>
<span data-ttu-id="5fbc7-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5fbc7-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5fbc7-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5fbc7-135">-WhatIf</span></span>
<span data-ttu-id="5fbc7-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5fbc7-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5fbc7-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5fbc7-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5fbc7-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5fbc7-138">-DefaultProfile</span></span>
<span data-ttu-id="5fbc7-139">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5fbc7-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5fbc7-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5fbc7-140">CommonParameters</span></span>
<span data-ttu-id="5fbc7-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5fbc7-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5fbc7-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5fbc7-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5fbc7-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5fbc7-143">INPUTS</span></span>

### <span data-ttu-id="5fbc7-144">System. String</span><span class="sxs-lookup"><span data-stu-id="5fbc7-144">System.String</span></span>
<span data-ttu-id="5fbc7-145">Microsoft. Azure. Commands. Management. Storage. Models. PSIpRule [] Microsoft. Azure. Commands. Management. Storage. Models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="5fbc7-145">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[] Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="5fbc7-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5fbc7-146">OUTPUTS</span></span>

### <span data-ttu-id="5fbc7-147">Microsoft. Azure. Commands. Management. Storage. Models. PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="5fbc7-147">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>
<span data-ttu-id="5fbc7-148">Microsoft. Azure. Commands. Management. Storage. Models. PSIpRule</span><span class="sxs-lookup"><span data-stu-id="5fbc7-148">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="5fbc7-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5fbc7-149">NOTES</span></span>

## <span data-ttu-id="5fbc7-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5fbc7-150">RELATED LINKS</span></span>

