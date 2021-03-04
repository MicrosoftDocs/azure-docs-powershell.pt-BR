---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/update-azstorageaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageAccountNetworkRuleSet.md
ms.openlocfilehash: 03e6169a9e69b9f2faa3dfaccba934428f7db4e7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888047"
---
# <span data-ttu-id="3a5ac-101">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="3a5ac-101">Update-AzStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="3a5ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a5ac-102">SYNOPSIS</span></span>
<span data-ttu-id="3a5ac-103">Atualizar a propriedade NetworkRule de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="3a5ac-103">Update the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="3a5ac-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="3a5ac-104">SYNTAX</span></span>

```
Update-AzStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-Bypass <PSNetWorkRuleBypassEnum>] [-DefaultAction <PSNetWorkRuleDefaultActionEnum>] [-IPRule <PSIpRule[]>]
 [-VirtualNetworkRule <PSVirtualNetworkRule[]>] [-ResourceAccessRule <PSResourceAccessRule[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a5ac-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3a5ac-105">DESCRIPTION</span></span>
<span data-ttu-id="3a5ac-106">O cmdlet **Update-AzStorageAccountNetworkRuleSet** atualiza a propriedade NetworkRule de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="3a5ac-106">The **Update-AzStorageAccountNetworkRuleSet** cmdlet updates the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="3a5ac-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3a5ac-107">EXAMPLES</span></span>

### <span data-ttu-id="3a5ac-108">Exemplo 1: Atualizar todas as propriedades de NetworkRule, regras de entrada com JSON</span><span class="sxs-lookup"><span data-stu-id="3a5ac-108">Example 1: Update all properties of NetworkRule, input Rules with JSON</span></span>
```
PS C:\> Update-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -Bypass Logging,Metrics -DefaultAction Allow -IpRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
    -VirtualNetworkRule (@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualN
    etworks/vnet2/subnets/subnet2";Action="allow"}) -ResourceAccessRule (@{ResourceId=$ResourceId1;TenantId=$tenantId1},@{ResourceId=$ResourceId2;TenantId=$tenantId1})
```

<span data-ttu-id="3a5ac-109">Este comando atualiza todas as propriedades de NetworkRule, regras de entrada com JSON.</span><span class="sxs-lookup"><span data-stu-id="3a5ac-109">This command update all properties of NetworkRule, input Rules with JSON.</span></span>

### <span data-ttu-id="3a5ac-110">Exemplo 2: Atualizar a propriedade Bypass de NetworkRule</span><span class="sxs-lookup"><span data-stu-id="3a5ac-110">Example 2: Update Bypass property of NetworkRule</span></span>
```
PS C:\> Update-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -Bypass AzureServices,Metrics
```

<span data-ttu-id="3a5ac-111">Este comando atualiza a propriedade Bypass de NetworkRule (outras propriedades não mudarão).</span><span class="sxs-lookup"><span data-stu-id="3a5ac-111">This command update Bypass property of NetworkRule (other properties won't change).</span></span>

### <span data-ttu-id="3a5ac-112">Exemplo 3: Limpar regras de NetworkRule de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="3a5ac-112">Example 3: Clean up rules of NetworkRule of a Storage account</span></span>
```
PS C:\> Update-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -IpRule @() -VirtualNetworkRule @() -ResourceAccessRule @()
```

<span data-ttu-id="3a5ac-113">Este comando limpa as regras de NetworkRule de uma conta de Armazenamento (outras propriedades não mudam).</span><span class="sxs-lookup"><span data-stu-id="3a5ac-113">This command clean up rules of NetworkRule of a Storage account (other properties not change).</span></span>

## <span data-ttu-id="3a5ac-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="3a5ac-114">PARAMETERS</span></span>

### <span data-ttu-id="3a5ac-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3a5ac-115">-AsJob</span></span>
<span data-ttu-id="3a5ac-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="3a5ac-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3a5ac-117">-Bypass</span><span class="sxs-lookup"><span data-stu-id="3a5ac-117">-Bypass</span></span>
<span data-ttu-id="3a5ac-118">O valor Bypass a ser atualizado para a propriedade NetworkRule de uma conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="3a5ac-118">The Bypass value to update to the NetworkRule property of a Storage account.</span></span>
<span data-ttu-id="3a5ac-119">O valor permitido não é nenhum ou qualquer combinação de: • Log • Métricas • Azureservices</span><span class="sxs-lookup"><span data-stu-id="3a5ac-119">The allowed value are none or any combination of: • Logging • Metrics • Azureservices</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSNetWorkRuleBypassEnum
Parameter Sets: (All)
Aliases:
Accepted values: None, Logging, Metrics, AzureServices

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a5ac-120">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="3a5ac-120">-DefaultAction</span></span>
<span data-ttu-id="3a5ac-121">O valor DefaultAction a ser atualizado para a propriedade NetworkRule de uma conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="3a5ac-121">The DefaultAction value to update to the NetworkRule property of a Storage account.</span></span>
<span data-ttu-id="3a5ac-122">As opções permitidas: • Permitir • Negar</span><span class="sxs-lookup"><span data-stu-id="3a5ac-122">The allowed Options: • Allow • Deny</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSNetWorkRuleDefaultActionEnum
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a5ac-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a5ac-123">-DefaultProfile</span></span>
<span data-ttu-id="3a5ac-124">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3a5ac-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a5ac-125">-IPRule</span><span class="sxs-lookup"><span data-stu-id="3a5ac-125">-IPRule</span></span>
<span data-ttu-id="3a5ac-126">A Matriz de objetos IpRule a ser atualizada para a Propriedade NetworkRule de uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="3a5ac-126">The Array of IpRule objects to update to the NetworkRule Property of a Storage account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a5ac-127">-Name</span><span class="sxs-lookup"><span data-stu-id="3a5ac-127">-Name</span></span>
<span data-ttu-id="3a5ac-128">Especifica o nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="3a5ac-128">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="3a5ac-129">-ResourceAccessRule</span><span class="sxs-lookup"><span data-stu-id="3a5ac-129">-ResourceAccessRule</span></span>
<span data-ttu-id="3a5ac-130">Rede de Conta de ArmazenamentoRule ResourceAccessRules.</span><span class="sxs-lookup"><span data-stu-id="3a5ac-130">Storage Account NetworkRule ResourceAccessRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSResourceAccessRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a5ac-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a5ac-131">-ResourceGroupName</span></span>
<span data-ttu-id="3a5ac-132">Especifica o nome do grupo de recursos que contém a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="3a5ac-132">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="3a5ac-133">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="3a5ac-133">-VirtualNetworkRule</span></span>
<span data-ttu-id="3a5ac-134">A Matriz de objetos VirtualNetworkRule a ser atualizada para a Propriedade NetworkRule de uma conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="3a5ac-134">The Array of VirtualNetworkRule objects to update to the NetworkRule Property of a Storage account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a5ac-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3a5ac-135">-Confirm</span></span>
<span data-ttu-id="3a5ac-136">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a5ac-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a5ac-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a5ac-137">-WhatIf</span></span>
<span data-ttu-id="3a5ac-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3a5ac-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a5ac-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3a5ac-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a5ac-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a5ac-140">CommonParameters</span></span>
<span data-ttu-id="3a5ac-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a5ac-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a5ac-142">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a5ac-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a5ac-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3a5ac-143">INPUTS</span></span>

### <span data-ttu-id="3a5ac-144">System.String</span><span class="sxs-lookup"><span data-stu-id="3a5ac-144">System.String</span></span>

### <span data-ttu-id="3a5ac-145">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span><span class="sxs-lookup"><span data-stu-id="3a5ac-145">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>

### <span data-ttu-id="3a5ac-146">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span><span class="sxs-lookup"><span data-stu-id="3a5ac-146">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="3a5ac-147">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="3a5ac-147">OUTPUTS</span></span>

### <span data-ttu-id="3a5ac-148">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="3a5ac-148">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="3a5ac-149">NOTES</span><span class="sxs-lookup"><span data-stu-id="3a5ac-149">NOTES</span></span>

## <span data-ttu-id="3a5ac-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3a5ac-150">RELATED LINKS</span></span>
