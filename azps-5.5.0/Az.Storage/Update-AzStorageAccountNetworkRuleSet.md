---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstorageaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageAccountNetworkRuleSet.md
ms.openlocfilehash: 04611df4dd315c972d9e32b280d635a6ecd0ed21
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116088"
---
# <span data-ttu-id="37ae2-101">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="37ae2-101">Update-AzStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="37ae2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="37ae2-102">SYNOPSIS</span></span>
<span data-ttu-id="37ae2-103">Atualizar a propriedade NetworkRule de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="37ae2-103">Update the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="37ae2-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="37ae2-104">SYNTAX</span></span>

```
Update-AzStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-Bypass <PSNetWorkRuleBypassEnum>] [-DefaultAction <PSNetWorkRuleDefaultActionEnum>] [-IPRule <PSIpRule[]>]
 [-VirtualNetworkRule <PSVirtualNetworkRule[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37ae2-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="37ae2-105">DESCRIPTION</span></span>
<span data-ttu-id="37ae2-106">O cmdlet **Update-AzStorageAccountNetworkRuleSet** atualiza a propriedade NetworkRule de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="37ae2-106">The **Update-AzStorageAccountNetworkRuleSet** cmdlet updates the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="37ae2-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="37ae2-107">EXAMPLES</span></span>

### <span data-ttu-id="37ae2-108">Exemplo 1: Atualizar todas as propriedades do NetworkRule, regras de entrada com JSON</span><span class="sxs-lookup"><span data-stu-id="37ae2-108">Example 1: Update all properties of NetworkRule, input Rules with JSON</span></span>
```
PS C:\> Update-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -Bypass Logging,Metrics -DefaultAction Allow -IpRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
    -VirtualNetworkRule (@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualN
    etworks/vnet2/subnets/subnet2";Action="allow"})
```

<span data-ttu-id="37ae2-109">Este comando atualiza todas as propriedades de NetworkRule, regras de entrada com JSON.</span><span class="sxs-lookup"><span data-stu-id="37ae2-109">This command update all properties of NetworkRule, input Rules with JSON.</span></span>

### <span data-ttu-id="37ae2-110">Exemplo 2: atualizar a propriedade Bypass da NetworkRule</span><span class="sxs-lookup"><span data-stu-id="37ae2-110">Example 2: Update Bypass property of NetworkRule</span></span>
```
PS C:\> Update-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -Bypass AzureServices,Metrics
```

<span data-ttu-id="37ae2-111">Esta propriedade de atualização de comando Bypass da NetworkRule (outras propriedades não mudarão).</span><span class="sxs-lookup"><span data-stu-id="37ae2-111">This command update Bypass property of NetworkRule (other properties won't change).</span></span>

### <span data-ttu-id="37ae2-112">Exemplo 3: Limpar regras de NetworkRule de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="37ae2-112">Example 3: Clean up rules of NetworkRule of a Storage account</span></span>
```
PS C:\> Update-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -IpRule @() -VirtualNetworkRule @()
```

<span data-ttu-id="37ae2-113">Este comando limpa as regras de NetworkRule de uma conta de Armazenamento (outras propriedades não mudam).</span><span class="sxs-lookup"><span data-stu-id="37ae2-113">This command clean up rules of NetworkRule of a Storage account (other properties not change).</span></span>

## <span data-ttu-id="37ae2-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="37ae2-114">PARAMETERS</span></span>

### <span data-ttu-id="37ae2-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="37ae2-115">-AsJob</span></span>
<span data-ttu-id="37ae2-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="37ae2-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="37ae2-117">-Ignorar</span><span class="sxs-lookup"><span data-stu-id="37ae2-117">-Bypass</span></span>
<span data-ttu-id="37ae2-118">O valor bypass a ser atualizado para a propriedade NetworkRule de uma conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="37ae2-118">The Bypass value to update to the NetworkRule property of a Storage account.</span></span>
<span data-ttu-id="37ae2-119">O valor permitido não é nenhum ou qualquer combinação de: • Log • Métricas • Azureservices</span><span class="sxs-lookup"><span data-stu-id="37ae2-119">The allowed value are none or any combination of: • Logging • Metrics • Azureservices</span></span>

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

### <span data-ttu-id="37ae2-120">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="37ae2-120">-DefaultAction</span></span>
<span data-ttu-id="37ae2-121">O valor DefaultAction a ser atualizado para a propriedade NetworkRule de uma conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="37ae2-121">The DefaultAction value to update to the NetworkRule property of a Storage account.</span></span>
<span data-ttu-id="37ae2-122">As Opções permitidas: • Permitir • Negar</span><span class="sxs-lookup"><span data-stu-id="37ae2-122">The allowed Options: • Allow • Deny</span></span>

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

### <span data-ttu-id="37ae2-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37ae2-123">-DefaultProfile</span></span>
<span data-ttu-id="37ae2-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="37ae2-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37ae2-125">-IPRule</span><span class="sxs-lookup"><span data-stu-id="37ae2-125">-IPRule</span></span>
<span data-ttu-id="37ae2-126">A matriz de objetos IpRule para atualizar para a propriedade NetworkRule de uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="37ae2-126">The Array of IpRule objects to update to the NetworkRule Property of a Storage account.</span></span>

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

### <span data-ttu-id="37ae2-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="37ae2-127">-Name</span></span>
<span data-ttu-id="37ae2-128">Especifica o nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="37ae2-128">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="37ae2-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37ae2-129">-ResourceGroupName</span></span>
<span data-ttu-id="37ae2-130">Especifica o nome do grupo de recursos que contém a conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="37ae2-130">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="37ae2-131">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="37ae2-131">-VirtualNetworkRule</span></span>
<span data-ttu-id="37ae2-132">A matriz de objetos VirtualNetworkRule para atualizar para a propriedade NetworkRule de uma conta de Armazenamento.</span><span class="sxs-lookup"><span data-stu-id="37ae2-132">The Array of VirtualNetworkRule objects to update to the NetworkRule Property of a Storage account.</span></span>

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

### <span data-ttu-id="37ae2-133">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="37ae2-133">-Confirm</span></span>
<span data-ttu-id="37ae2-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37ae2-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37ae2-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37ae2-135">-WhatIf</span></span>
<span data-ttu-id="37ae2-136">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="37ae2-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37ae2-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="37ae2-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37ae2-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37ae2-138">CommonParameters</span></span>
<span data-ttu-id="37ae2-139">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37ae2-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37ae2-140">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37ae2-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37ae2-141">Entradas</span><span class="sxs-lookup"><span data-stu-id="37ae2-141">INPUTS</span></span>

### <span data-ttu-id="37ae2-142">System.String</span><span class="sxs-lookup"><span data-stu-id="37ae2-142">System.String</span></span>

### <span data-ttu-id="37ae2-143">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span><span class="sxs-lookup"><span data-stu-id="37ae2-143">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>

### <span data-ttu-id="37ae2-144">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span><span class="sxs-lookup"><span data-stu-id="37ae2-144">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="37ae2-145">Saídas</span><span class="sxs-lookup"><span data-stu-id="37ae2-145">OUTPUTS</span></span>

### <span data-ttu-id="37ae2-146">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="37ae2-146">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="37ae2-147">Notas</span><span class="sxs-lookup"><span data-stu-id="37ae2-147">NOTES</span></span>

## <span data-ttu-id="37ae2-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="37ae2-148">RELATED LINKS</span></span>
