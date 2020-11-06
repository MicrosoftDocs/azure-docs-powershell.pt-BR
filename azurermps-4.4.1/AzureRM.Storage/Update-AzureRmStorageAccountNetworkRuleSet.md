---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Update-AzureRmStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Update-AzureRmStorageAccountNetworkRuleSet.md
ms.openlocfilehash: 09619247f41acb60180a7d3045afdcd689d5c183
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610143"
---
# <span data-ttu-id="c4eb3-101">Update-AzureRmStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="c4eb3-101">Update-AzureRmStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="c4eb3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c4eb3-102">SYNOPSIS</span></span>
<span data-ttu-id="c4eb3-103">Atualizar a propriedade NetworkRule de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="c4eb3-103">Update the NetworkRule property of a Storage Account</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4eb3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c4eb3-104">SYNTAX</span></span>

```
Update-AzureRmStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-Bypass <PSNetWorkRuleBypassEnum>] [-DefaultAction <PSNetWorkRuleDefaultActionEnum>] [-IPRule <PSIpRule[]>]
 [-VirtualNetworkRule <PSVirtualNetworkRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c4eb3-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c4eb3-105">DESCRIPTION</span></span>
<span data-ttu-id="c4eb3-106">O cmdlet **Update-AzureRmStorageAccountNetworkRuleSet** atualiza a propriedade NetworkRule de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="c4eb3-106">The **Update-AzureRmStorageAccountNetworkRuleSet** cmdlet updates the NetworkRule property of a Storage Account</span></span>

## <span data-ttu-id="c4eb3-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c4eb3-107">EXAMPLES</span></span>

### <span data-ttu-id="c4eb3-108">Exemplo 1: atualizar todas as propriedades de NetworkRule, regras de entrada com JSON</span><span class="sxs-lookup"><span data-stu-id="c4eb3-108">Example 1: Update all properties of NetworkRule, input Rules with JSON</span></span>
```
PS C:\> Update-AzureRmStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Bypass Logging,Metrics -DefaultAction Allow -IpRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
    -VirtualNetworkRule (@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualN
    etworks/vnet2/subnets/subnet2";Action="allow"})
```

<span data-ttu-id="c4eb3-109">Esse comando atualiza todas as propriedades de NetworkRule, regras de entrada com JSON.</span><span class="sxs-lookup"><span data-stu-id="c4eb3-109">This command update all properties of NetworkRule, input Rules with JSON.</span></span>

### <span data-ttu-id="c4eb3-110">Exemplo 2: atualizar a propriedade bypass de NetworkRule</span><span class="sxs-lookup"><span data-stu-id="c4eb3-110">Example 2: Update Bypass property of NetworkRule</span></span>
```
PS C:\> Update-AzureRmStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Bypass AzureServices,Metrics
```

<span data-ttu-id="c4eb3-111">Esta propriedade de atualização de comando bypass de NetworkRule (outras propriedades não se alteram).</span><span class="sxs-lookup"><span data-stu-id="c4eb3-111">This command update Bypass property of NetworkRule (other properties won't change).</span></span>

### <span data-ttu-id="c4eb3-112">Exemplo 3: limpar regras de NetworkRule de uma conta de armazenamento</span><span class="sxs-lookup"><span data-stu-id="c4eb3-112">Example 3: Clean up rules of NetworkRule of a Storage Account</span></span>
```
PS C:\> Update-AzureRmStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -IpRule @() -VirtualNetworkRule @()
```

<span data-ttu-id="c4eb3-113">Este comando limpa as regras de NetworkRule de uma conta de armazenamento (outras propriedades não são alteradas).</span><span class="sxs-lookup"><span data-stu-id="c4eb3-113">This command clean up rules of NetworkRule of a Storage Account (other properties not change).</span></span>

## <span data-ttu-id="c4eb3-114">OS</span><span class="sxs-lookup"><span data-stu-id="c4eb3-114">PARAMETERS</span></span>

### <span data-ttu-id="c4eb3-115">-Ignorar</span><span class="sxs-lookup"><span data-stu-id="c4eb3-115">-Bypass</span></span>
<span data-ttu-id="c4eb3-116">O valor de bypass a ser atualizado para a propriedade NetworkRule de uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c4eb3-116">The Bypass value to update to the NetworkRule property of a Storage Account.</span></span>
<span data-ttu-id="c4eb3-117">O valor permitido é nenhuma ou qualquer combinação de: â € ¢ log â € ¢ métricas â € ¢ Azureservices</span><span class="sxs-lookup"><span data-stu-id="c4eb3-117">The allowed value are none or any combination of: â€¢ Logging â€¢ Metrics â€¢ Azureservices</span></span>

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

### <span data-ttu-id="c4eb3-118">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="c4eb3-118">-DefaultAction</span></span>
<span data-ttu-id="c4eb3-119">O valor DefaultAction para atualizar para a propriedade NetworkRule de uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c4eb3-119">The DefaultAction value to update to the NetworkRule property of a Storage Account.</span></span>
<span data-ttu-id="c4eb3-120">As opções permitidas: â € ¢ permitir â € ¢ negar</span><span class="sxs-lookup"><span data-stu-id="c4eb3-120">The allowed Options: â€¢ Allow â€¢ Deny</span></span>

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

### <span data-ttu-id="c4eb3-121">-IPRule</span><span class="sxs-lookup"><span data-stu-id="c4eb3-121">-IPRule</span></span>
<span data-ttu-id="c4eb3-122">A matriz de objetos IpRule para atualizar para a propriedade NetworkRule de uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c4eb3-122">The Array of IpRule objects to update to the NetworkRule Property of a Storage Account.</span></span>

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

### <span data-ttu-id="c4eb3-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="c4eb3-123">-Name</span></span>
<span data-ttu-id="c4eb3-124">Especifica o nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c4eb3-124">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="c4eb3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4eb3-125">-ResourceGroupName</span></span>
<span data-ttu-id="c4eb3-126">Especifica o nome do grupo de recursos que contém a conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c4eb3-126">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="c4eb3-127">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="c4eb3-127">-VirtualNetworkRule</span></span>
<span data-ttu-id="c4eb3-128">A matriz de objetos VirtualNetworkRule para atualizar para a propriedade NetworkRule de uma conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c4eb3-128">The Array of VirtualNetworkRule objects to update to the NetworkRule Property of a Storage Account.</span></span>

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

### <span data-ttu-id="c4eb3-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c4eb3-129">-Confirm</span></span>
<span data-ttu-id="c4eb3-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4eb3-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4eb3-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4eb3-131">-WhatIf</span></span>
<span data-ttu-id="c4eb3-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c4eb3-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4eb3-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c4eb3-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4eb3-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4eb3-134">-DefaultProfile</span></span>
<span data-ttu-id="c4eb3-135">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c4eb3-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4eb3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4eb3-136">CommonParameters</span></span>
<span data-ttu-id="c4eb3-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4eb3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4eb3-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4eb3-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4eb3-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c4eb3-139">INPUTS</span></span>

### <span data-ttu-id="c4eb3-140">System. String</span><span class="sxs-lookup"><span data-stu-id="c4eb3-140">System.String</span></span>
<span data-ttu-id="c4eb3-141">Microsoft. Azure. Commands. Management. Storage. Models. PSIpRule [] Microsoft. Azure. Commands. Management. Storage. Models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="c4eb3-141">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[] Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="c4eb3-142">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c4eb3-142">OUTPUTS</span></span>

### <span data-ttu-id="c4eb3-143">Microsoft. Azure. Commands. Management. Storage. Models. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="c4eb3-143">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="c4eb3-144">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c4eb3-144">NOTES</span></span>

## <span data-ttu-id="c4eb3-145">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c4eb3-145">RELATED LINKS</span></span>

