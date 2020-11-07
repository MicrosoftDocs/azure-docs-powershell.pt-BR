---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstorageaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageAccountNetworkRuleSet.md
ms.openlocfilehash: 64a2963f0b474341480b8e4794370ba90cffd71f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93774042"
---
# <span data-ttu-id="1052f-101">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="1052f-101">Update-AzStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="1052f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1052f-102">SYNOPSIS</span></span>
<span data-ttu-id="1052f-103">Atualizar a propriedade NetworkRule de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="1052f-103">Update the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="1052f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1052f-104">SYNTAX</span></span>

```
Update-AzStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-Bypass <PSNetWorkRuleBypassEnum>] [-DefaultAction <PSNetWorkRuleDefaultActionEnum>] [-IPRule <PSIpRule[]>]
 [-VirtualNetworkRule <PSVirtualNetworkRule[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1052f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1052f-105">DESCRIPTION</span></span>
<span data-ttu-id="1052f-106">O cmdlet **Update-AzStorageAccountNetworkRuleSet** atualiza a propriedade NetworkRule de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="1052f-106">The **Update-AzStorageAccountNetworkRuleSet** cmdlet updates the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="1052f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1052f-107">EXAMPLES</span></span>

### <span data-ttu-id="1052f-108">Exemplo 1: atualizar todas as propriedades de NetworkRule, regras de entrada com JSON</span><span class="sxs-lookup"><span data-stu-id="1052f-108">Example 1: Update all properties of NetworkRule, input Rules with JSON</span></span>
```
PS C:\> Update-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -Bypass Logging,Metrics -DefaultAction Allow -IpRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
    -VirtualNetworkRule (@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualN
    etworks/vnet2/subnets/subnet2";Action="allow"})
```

<span data-ttu-id="1052f-109">Esse comando atualiza todas as propriedades de NetworkRule, regras de entrada com JSON.</span><span class="sxs-lookup"><span data-stu-id="1052f-109">This command update all properties of NetworkRule, input Rules with JSON.</span></span>

### <span data-ttu-id="1052f-110">Exemplo 2: atualizar a propriedade bypass de NetworkRule</span><span class="sxs-lookup"><span data-stu-id="1052f-110">Example 2: Update Bypass property of NetworkRule</span></span>
```
PS C:\> Update-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -Bypass AzureServices,Metrics
```

<span data-ttu-id="1052f-111">Esta propriedade de atualização de comando bypass de NetworkRule (outras propriedades não se alteram).</span><span class="sxs-lookup"><span data-stu-id="1052f-111">This command update Bypass property of NetworkRule (other properties won't change).</span></span>

### <span data-ttu-id="1052f-112">Exemplo 3: limpar regras de NetworkRule de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="1052f-112">Example 3: Clean up rules of NetworkRule of a Storage account</span></span>
```
PS C:\> Update-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -IpRule @() -VirtualNetworkRule @()
```

<span data-ttu-id="1052f-113">Este comando limpa as regras de NetworkRule de uma conta de armazenamento (outras propriedades não são alteradas).</span><span class="sxs-lookup"><span data-stu-id="1052f-113">This command clean up rules of NetworkRule of a Storage account (other properties not change).</span></span>

## <span data-ttu-id="1052f-114">OS</span><span class="sxs-lookup"><span data-stu-id="1052f-114">PARAMETERS</span></span>

### <span data-ttu-id="1052f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1052f-115">-AsJob</span></span>
<span data-ttu-id="1052f-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="1052f-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1052f-117">-Ignorar</span><span class="sxs-lookup"><span data-stu-id="1052f-117">-Bypass</span></span>
<span data-ttu-id="1052f-118">O valor de bypass a ser atualizado para a propriedade NetworkRule de uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="1052f-118">The Bypass value to update to the NetworkRule property of a Storage account.</span></span>
<span data-ttu-id="1052f-119">O valor permitido é nenhuma ou qualquer combinação de: • registro em log • métricas • Azureservices</span><span class="sxs-lookup"><span data-stu-id="1052f-119">The allowed value are none or any combination of: • Logging • Metrics • Azureservices</span></span>

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

### <span data-ttu-id="1052f-120">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="1052f-120">-DefaultAction</span></span>
<span data-ttu-id="1052f-121">O valor DefaultAction para atualizar para a propriedade NetworkRule de uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="1052f-121">The DefaultAction value to update to the NetworkRule property of a Storage account.</span></span>
<span data-ttu-id="1052f-122">As opções permitidas: • permitir • negar</span><span class="sxs-lookup"><span data-stu-id="1052f-122">The allowed Options: • Allow • Deny</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSNetWorkRuleDefaultActionEnum
Parameter Sets: (All)
Aliases:
Accepted values: Deny, Allow

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1052f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1052f-123">-DefaultProfile</span></span>
<span data-ttu-id="1052f-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1052f-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1052f-125">-IPRule</span><span class="sxs-lookup"><span data-stu-id="1052f-125">-IPRule</span></span>
<span data-ttu-id="1052f-126">A matriz de objetos IpRule para atualizar para a propriedade NetworkRule de uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="1052f-126">The Array of IpRule objects to update to the NetworkRule Property of a Storage account.</span></span>

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

### <span data-ttu-id="1052f-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="1052f-127">-Name</span></span>
<span data-ttu-id="1052f-128">Especifica o nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="1052f-128">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="1052f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1052f-129">-ResourceGroupName</span></span>
<span data-ttu-id="1052f-130">Especifica o nome do grupo de recursos que contém a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="1052f-130">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="1052f-131">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="1052f-131">-VirtualNetworkRule</span></span>
<span data-ttu-id="1052f-132">A matriz de objetos VirtualNetworkRule para atualizar para a propriedade NetworkRule de uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="1052f-132">The Array of VirtualNetworkRule objects to update to the NetworkRule Property of a Storage account.</span></span>

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

### <span data-ttu-id="1052f-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1052f-133">-Confirm</span></span>
<span data-ttu-id="1052f-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1052f-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1052f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1052f-135">-WhatIf</span></span>
<span data-ttu-id="1052f-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1052f-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1052f-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1052f-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1052f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1052f-138">CommonParameters</span></span>
<span data-ttu-id="1052f-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1052f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1052f-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1052f-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1052f-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1052f-141">INPUTS</span></span>

### <span data-ttu-id="1052f-142">System. String</span><span class="sxs-lookup"><span data-stu-id="1052f-142">System.String</span></span>

### <span data-ttu-id="1052f-143">Microsoft. Azure. Commands. Management. Storage. Models. PSIpRule []</span><span class="sxs-lookup"><span data-stu-id="1052f-143">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>

### <span data-ttu-id="1052f-144">Microsoft. Azure. Commands. Management. Storage. Models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="1052f-144">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="1052f-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1052f-145">OUTPUTS</span></span>

### <span data-ttu-id="1052f-146">Microsoft. Azure. Commands. Management. Storage. Models. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="1052f-146">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="1052f-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1052f-147">NOTES</span></span>

## <span data-ttu-id="1052f-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1052f-148">RELATED LINKS</span></span>