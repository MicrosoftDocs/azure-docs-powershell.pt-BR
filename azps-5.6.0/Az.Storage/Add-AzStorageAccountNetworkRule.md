---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/add-azstorageaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountNetworkRule.md
ms.openlocfilehash: 0104c64bf65acc945609f4e2e0ae78ff288b142d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888408"
---
# <span data-ttu-id="38844-101">Add-AzStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="38844-101">Add-AzStorageAccountNetworkRule</span></span>

## <span data-ttu-id="38844-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38844-102">SYNOPSIS</span></span>
 <span data-ttu-id="38844-103">Adicionar IpRules ou VirtualNetworkRules à propriedade NetworkRule de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="38844-103">Add IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="38844-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="38844-104">SYNTAX</span></span>

### <span data-ttu-id="38844-105">NetWorkRuleString (Padrão)</span><span class="sxs-lookup"><span data-stu-id="38844-105">NetWorkRuleString (Default)</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="38844-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="38844-106">IpRuleObject</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38844-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="38844-107">NetworkRuleObject</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38844-108">ResourceAccessRuleObject</span><span class="sxs-lookup"><span data-stu-id="38844-108">ResourceAccessRuleObject</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -ResourceAccessRule <PSResourceAccessRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38844-109">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="38844-109">IpRuleString</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPAddressOrRange <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38844-110">ResourceAccessRuleString</span><span class="sxs-lookup"><span data-stu-id="38844-110">ResourceAccessRuleString</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -TenantId <String>
 -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="38844-111">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="38844-111">DESCRIPTION</span></span>
<span data-ttu-id="38844-112">O cmdlet **Add-AzStorageAccountNetworkRule** adiciona IpRules ou VirtualNetworkRules à propriedade NetworkRule de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="38844-112">The **Add-AzStorageAccountNetworkRule** cmdlet adds IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="38844-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="38844-113">EXAMPLES</span></span>

### <span data-ttu-id="38844-114">Exemplo 1: Adicionar vários IpRules com IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="38844-114">Example 1: Add several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -IPAddressOrRange "10.0.0.0/24","28.2.0.0/16"
```

<span data-ttu-id="38844-115">Este comando adiciona vários IpRules com IPAddressOrRange.</span><span class="sxs-lookup"><span data-stu-id="38844-115">This command add several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="38844-116">Exemplo 2: Adicionar um VirtualNetworkRule com VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="38844-116">Example 2: Add a VirtualNetworkRule with VirtualNetworkResourceID</span></span>
```
PS C:\>$subnet = Get-AzVirtualNetwork -ResourceGroupName "myResourceGroup" -Name "myvirtualnetwork" | Get-AzVirtualNetworkSubnetConfig
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -VirtualNetworkResourceId $subnet[0].Id
```

<span data-ttu-id="38844-117">Este comando adiciona um VirtualNetworkRule com VirtualNetworkResourceID.</span><span class="sxs-lookup"><span data-stu-id="38844-117">This command add a VirtualNetworkRule with VirtualNetworkResourceID.</span></span>

### <span data-ttu-id="38844-118">Exemplo 3: Adicionar VirtualNetworkRules com Objetos VirtualNetworkRule de outra conta</span><span class="sxs-lookup"><span data-stu-id="38844-118">Example 3: Add VirtualNetworkRules with VirtualNetworkRule Objects from another account</span></span>
```
PS C:\> $networkrule = Get-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "mystorageaccount1"
PS C:\> Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount2" -VirtualNetworkRule $networkrule.VirtualNetworkRules
```

<span data-ttu-id="38844-119">Este comando adiciona VirtualNetworkRules com Objetos VirtualNetworkRule de outra conta.</span><span class="sxs-lookup"><span data-stu-id="38844-119">This command add VirtualNetworkRules with VirtualNetworkRule Objects from another account.</span></span>

### <span data-ttu-id="38844-120">Exemplo 4: Adicionar vários IpRule com objetos IpRule, entrada com JSON</span><span class="sxs-lookup"><span data-stu-id="38844-120">Example 4: Add several IpRule with IpRule objects, input with JSON</span></span>
```
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -IPRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
```

<span data-ttu-id="38844-121">Este comando adiciona vários IpRule com objetos IpRule, entrada com JSON.</span><span class="sxs-lookup"><span data-stu-id="38844-121">This command add several IpRule with IpRule objects, input with JSON.</span></span>

### <span data-ttu-id="38844-122">Exemplo 5: Adicionar uma regra de acesso a recursos</span><span class="sxs-lookup"><span data-stu-id="38844-122">Example 5: Add a resource access rule</span></span>
```
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -TenantId $tenantId -ResourceId $ResourceId
```

<span data-ttu-id="38844-123">Este comando adiciona uma regra de acesso a recursos com TenantId e ResourceId.</span><span class="sxs-lookup"><span data-stu-id="38844-123">This command adds a resource access rule with TenantId and ResourceId.</span></span>

### <span data-ttu-id="38844-124">Exemplo 6: Adicionar todas as regras de acesso a recursos de uma conta de armazenamento a outra conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="38844-124">Example 6: Add all resource access rules of one storage account to another storage account</span></span>
```
PS C:\> (Get-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "mystorageaccount1").ResourceAccessRules | Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount2"
```

<span data-ttu-id="38844-125">Esse comando obtém todas as regras de acesso a recursos de uma conta de armazenamento e as adiciona a outra conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="38844-125">This command gets all resource access rules from one storage account, and adds them to another storage account.</span></span>

## <span data-ttu-id="38844-126">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="38844-126">PARAMETERS</span></span>

### <span data-ttu-id="38844-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="38844-127">-AsJob</span></span>
<span data-ttu-id="38844-128">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="38844-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="38844-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38844-129">-DefaultProfile</span></span>
<span data-ttu-id="38844-130">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="38844-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38844-131">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="38844-131">-IPAddressOrRange</span></span>
<span data-ttu-id="38844-132">A Matriz de IpAddressOrRange, adicione IpRules com a entrada IpAddressOrRange e a propriedade Action Allow to NetworkRule de entrada.</span><span class="sxs-lookup"><span data-stu-id="38844-132">The Array of IpAddressOrRange, add IpRules with the input IpAddressOrRange and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="38844-133">-IPRule</span><span class="sxs-lookup"><span data-stu-id="38844-133">-IPRule</span></span>
<span data-ttu-id="38844-134">A Matriz de objetos IpRule a ser adicionar à Propriedade NetworkRule.</span><span class="sxs-lookup"><span data-stu-id="38844-134">The Array of IpRule objects to add to the NetworkRule Property.</span></span>

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

### <span data-ttu-id="38844-135">-Name</span><span class="sxs-lookup"><span data-stu-id="38844-135">-Name</span></span>
<span data-ttu-id="38844-136">Especifica o nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="38844-136">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="38844-137">-ResourceAccessRule</span><span class="sxs-lookup"><span data-stu-id="38844-137">-ResourceAccessRule</span></span>
<span data-ttu-id="38844-138">Rede de Conta de ArmazenamentoRule ResourceAccessRules.</span><span class="sxs-lookup"><span data-stu-id="38844-138">Storage Account NetworkRule ResourceAccessRules.</span></span>

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

### <span data-ttu-id="38844-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38844-139">-ResourceGroupName</span></span>
<span data-ttu-id="38844-140">Especifica o nome do grupo de recursos que contém a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="38844-140">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="38844-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="38844-141">-ResourceId</span></span>
<span data-ttu-id="38844-142">Recurso de Conta de ArmazenamentoAccessRule ResourceId na cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="38844-142">Storage Account ResourceAccessRule ResourceId  in string.</span></span>

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

### <span data-ttu-id="38844-143">-TenantId</span><span class="sxs-lookup"><span data-stu-id="38844-143">-TenantId</span></span>
<span data-ttu-id="38844-144">Recurso de Conta de ArmazenamentoAccessRule TenantId na cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="38844-144">Storage Account ResourceAccessRule TenantId  in string.</span></span>

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

### <span data-ttu-id="38844-145">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="38844-145">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="38844-146">A Matriz de VirtualNetworkResourceId adicionará VirtualNetworkRule com a entrada VirtualNetworkResourceId e a propriedade Action Allow to NetworkRule de entrada.</span><span class="sxs-lookup"><span data-stu-id="38844-146">The Array of VirtualNetworkResourceId, will add VirtualNetworkRule with input VirtualNetworkResourceId and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="38844-147">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="38844-147">-VirtualNetworkRule</span></span>
<span data-ttu-id="38844-148">A Matriz de objetos VirtualNetworkRule a ser acrescentada à Propriedade NetworkRule.</span><span class="sxs-lookup"><span data-stu-id="38844-148">The Array of VirtualNetworkRule objects to add to the NetworkRule Property.</span></span>

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

### <span data-ttu-id="38844-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="38844-149">-Confirm</span></span>
<span data-ttu-id="38844-150">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38844-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38844-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38844-151">-WhatIf</span></span>
<span data-ttu-id="38844-152">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="38844-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38844-153">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="38844-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38844-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38844-154">CommonParameters</span></span>
<span data-ttu-id="38844-155">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38844-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38844-156">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38844-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38844-157">INPUTS</span><span class="sxs-lookup"><span data-stu-id="38844-157">INPUTS</span></span>

### <span data-ttu-id="38844-158">System.String</span><span class="sxs-lookup"><span data-stu-id="38844-158">System.String</span></span>

### <span data-ttu-id="38844-159">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span><span class="sxs-lookup"><span data-stu-id="38844-159">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>

### <span data-ttu-id="38844-160">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span><span class="sxs-lookup"><span data-stu-id="38844-160">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="38844-161">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="38844-161">OUTPUTS</span></span>

### <span data-ttu-id="38844-162">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="38844-162">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="38844-163">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span><span class="sxs-lookup"><span data-stu-id="38844-163">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="38844-164">NOTES</span><span class="sxs-lookup"><span data-stu-id="38844-164">NOTES</span></span>

## <span data-ttu-id="38844-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="38844-165">RELATED LINKS</span></span>
