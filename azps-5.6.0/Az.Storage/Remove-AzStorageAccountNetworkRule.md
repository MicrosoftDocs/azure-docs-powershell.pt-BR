---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azstorageaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountNetworkRule.md
ms.openlocfilehash: 295f79f48ffa966024561486745cdcf52ec8e38f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888052"
---
# <span data-ttu-id="f4dd4-101">Remove-AzStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f4dd4-101">Remove-AzStorageAccountNetworkRule</span></span>

## <span data-ttu-id="f4dd4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4dd4-102">SYNOPSIS</span></span>
<span data-ttu-id="f4dd4-103">Remover IpRules ou VirtualNetworkRules da propriedade NetWorkRule de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="f4dd4-103">Remove IpRules or VirtualNetworkRules from the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="f4dd4-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f4dd4-104">SYNTAX</span></span>

### <span data-ttu-id="f4dd4-105">NetWorkRuleString (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f4dd4-105">NetWorkRuleString (Default)</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f4dd4-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="f4dd4-106">IpRuleObject</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4dd4-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="f4dd4-107">NetworkRuleObject</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4dd4-108">ResourceAccessRuleObject</span><span class="sxs-lookup"><span data-stu-id="f4dd4-108">ResourceAccessRuleObject</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -ResourceAccessRule <PSResourceAccessRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4dd4-109">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="f4dd4-109">IpRuleString</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPAddressOrRange <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4dd4-110">ResourceAccessRuleString</span><span class="sxs-lookup"><span data-stu-id="f4dd4-110">ResourceAccessRuleString</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -TenantId <String>
 -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f4dd4-111">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f4dd4-111">DESCRIPTION</span></span>
<span data-ttu-id="f4dd4-112">O cmdlet **Remove-AzStorageAccountNetworkRule** remove IpRules ou VirtualNetworkRules da propriedade NetWorkRule de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="f4dd4-112">The **Remove-AzStorageAccountNetworkRule** cmdlet removes IpRules or VirtualNetworkRules from the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="f4dd4-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f4dd4-113">EXAMPLES</span></span>

### <span data-ttu-id="f4dd4-114">Exemplo 1: Remover vários IpRules com IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="f4dd4-114">Example 1: Remove several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -IPAddressOrRange "10.0.0.0/24,28.1.0.0/16"
```

<span data-ttu-id="f4dd4-115">Este comando remove vários IpRules com IPAddressOrRange.</span><span class="sxs-lookup"><span data-stu-id="f4dd4-115">This command remove several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="f4dd4-116">Exemplo 2: Remover uma VirtualNetworkRule com entrada de objeto VirtualNetworkRule com JSON</span><span class="sxs-lookup"><span data-stu-id="f4dd4-116">Example 2: Remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -VirtualNetworkRules (@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"})
```

<span data-ttu-id="f4dd4-117">Este comando remove uma entrada VirtualNetworkRule com o Objeto VirtualNetworkRule com JSON.</span><span class="sxs-lookup"><span data-stu-id="f4dd4-117">This command remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON.</span></span>

### <span data-ttu-id="f4dd4-118">Exemplo 3: Remover o primeiro IpRule com pipeline</span><span class="sxs-lookup"><span data-stu-id="f4dd4-118">Example 3: Remove first IpRule with pipeline</span></span>
```
PS C:\>(Get-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount").IpRules[0] | Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
```

<span data-ttu-id="f4dd4-119">Este comando remove o primeiro IpRule com pipeline.</span><span class="sxs-lookup"><span data-stu-id="f4dd4-119">This command remove first IpRule with pipeline.</span></span>

### <span data-ttu-id="f4dd4-120">Exemplo 4: Remover vários VirtualNetworkRules com VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="f4dd4-120">Example 4: Remove several VirtualNetworkRules with VirtualNetworkResourceID</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -VirtualNetworkResourceId "/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1","/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2"
```

<span data-ttu-id="f4dd4-121">Este comando remove vários VirtualNetworkRules com VirtualNetworkResourceID.</span><span class="sxs-lookup"><span data-stu-id="f4dd4-121">This command remove several VirtualNetworkRules with VirtualNetworkResourceID.</span></span>

### <span data-ttu-id="f4dd4-122">Exemplo 5: Remover uma regra de acesso a recursos com TenantId e ResourceId.</span><span class="sxs-lookup"><span data-stu-id="f4dd4-122">Example 5: Remove a resource access rule with TenantId and ResourceId.</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount"  -TenantId $tenantId -ResourceId $ResourceId
```

<span data-ttu-id="f4dd4-123">Este comando remove uma regra de acesso a recursos com TenantId e ResourceId.</span><span class="sxs-lookup"><span data-stu-id="f4dd4-123">This command removes a resource access rule with TenantId and ResourceId.</span></span>

### <span data-ttu-id="f4dd4-124">Exemplo 6: Remover as três primeiras regras de acesso a recursos de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="f4dd4-124">Example 6: Remove the first 3 resource access rules from a storage account</span></span>
```
PS C:\> (Get-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "mystorageaccount").ResourceAccessRules | Select-Object -First 3 | Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount"
```

<span data-ttu-id="f4dd4-125">Este comando remove as três primeiras regras de acesso a recursos de uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f4dd4-125">This command removes the first 3 resource access rules from a storage account.</span></span>

## <span data-ttu-id="f4dd4-126">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f4dd4-126">PARAMETERS</span></span>

### <span data-ttu-id="f4dd4-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f4dd4-127">-AsJob</span></span>
<span data-ttu-id="f4dd4-128">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="f4dd4-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f4dd4-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4dd4-129">-DefaultProfile</span></span>
<span data-ttu-id="f4dd4-130">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f4dd4-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4dd4-131">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="f4dd4-131">-IPAddressOrRange</span></span>
<span data-ttu-id="f4dd4-132">A Matriz de IpAddressOrRange removerá IpRule com o mesmo IpAddressOrRange da Propriedade NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="f4dd4-132">The Array of IpAddressOrRange, will remove IpRule with same IpAddressOrRange from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="f4dd4-133">-IPRule</span><span class="sxs-lookup"><span data-stu-id="f4dd4-133">-IPRule</span></span>
<span data-ttu-id="f4dd4-134">A Matriz de objetos IpRule a ser removido da Propriedade NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="f4dd4-134">The Array of IpRule objects to remove from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="f4dd4-135">-Name</span><span class="sxs-lookup"><span data-stu-id="f4dd4-135">-Name</span></span>
<span data-ttu-id="f4dd4-136">Especifica o nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f4dd4-136">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="f4dd4-137">-ResourceAccessRule</span><span class="sxs-lookup"><span data-stu-id="f4dd4-137">-ResourceAccessRule</span></span>
<span data-ttu-id="f4dd4-138">Rede de Conta de ArmazenamentoRule ResourceAccessRules.</span><span class="sxs-lookup"><span data-stu-id="f4dd4-138">Storage Account NetworkRule ResourceAccessRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSResourceAccessRule[]
Parameter Sets: ResourceAccessRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f4dd4-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4dd4-139">-ResourceGroupName</span></span>
<span data-ttu-id="f4dd4-140">Especifica o nome do grupo de recursos que contém a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="f4dd4-140">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="f4dd4-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4dd4-141">-ResourceId</span></span>
<span data-ttu-id="f4dd4-142">Recurso de Conta de ArmazenamentoAccessRule ResourceId na cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="f4dd4-142">Storage Account ResourceAccessRule ResourceId  in string.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceAccessRuleString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4dd4-143">-TenantId</span><span class="sxs-lookup"><span data-stu-id="f4dd4-143">-TenantId</span></span>
<span data-ttu-id="f4dd4-144">Recurso de Conta de ArmazenamentoAccessRule TenantId na cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="f4dd4-144">Storage Account ResourceAccessRule TenantId  in string.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceAccessRuleString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4dd4-145">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="f4dd4-145">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="f4dd4-146">A Matriz de VirtualNetworkResourceId removerá VirtualNetworkRule com o mesmo VirtualNetworkResourceId da propriedade NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="f4dd4-146">The Array of VirtualNetworkResourceId, will remove VirtualNetworkRule with same VirtualNetworkResourceId from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="f4dd4-147">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f4dd4-147">-VirtualNetworkRule</span></span>
<span data-ttu-id="f4dd4-148">A Matriz de objetos VirtualNetworkRule a ser removido da Propriedade NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="f4dd4-148">The Array of VirtualNetworkRule objects to remove from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="f4dd4-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f4dd4-149">-Confirm</span></span>
<span data-ttu-id="f4dd4-150">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4dd4-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4dd4-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4dd4-151">-WhatIf</span></span>
<span data-ttu-id="f4dd4-152">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f4dd4-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4dd4-153">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f4dd4-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4dd4-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4dd4-154">CommonParameters</span></span>
<span data-ttu-id="f4dd4-155">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4dd4-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4dd4-156">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4dd4-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4dd4-157">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f4dd4-157">INPUTS</span></span>

### <span data-ttu-id="f4dd4-158">System.String</span><span class="sxs-lookup"><span data-stu-id="f4dd4-158">System.String</span></span>

### <span data-ttu-id="f4dd4-159">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span><span class="sxs-lookup"><span data-stu-id="f4dd4-159">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>

### <span data-ttu-id="f4dd4-160">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span><span class="sxs-lookup"><span data-stu-id="f4dd4-160">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="f4dd4-161">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f4dd4-161">OUTPUTS</span></span>

### <span data-ttu-id="f4dd4-162">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f4dd4-162">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="f4dd4-163">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span><span class="sxs-lookup"><span data-stu-id="f4dd4-163">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="f4dd4-164">NOTES</span><span class="sxs-lookup"><span data-stu-id="f4dd4-164">NOTES</span></span>

## <span data-ttu-id="f4dd4-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f4dd4-165">RELATED LINKS</span></span>
