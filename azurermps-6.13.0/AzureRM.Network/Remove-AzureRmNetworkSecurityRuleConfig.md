---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2E43D0D8-EF93-443B-AA8F-58C992026E95
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkSecurityRuleConfig.md
ms.openlocfilehash: d6ca2ac1e091e3576af51ba8f1a2f50676994ce1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440345"
---
# <span data-ttu-id="df2ad-101">Remove-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="df2ad-101">Remove-AzureRmNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="df2ad-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="df2ad-102">SYNOPSIS</span></span>
<span data-ttu-id="df2ad-103">Remove uma regra de segurança de rede de um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="df2ad-103">Removes a network security rule from a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df2ad-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="df2ad-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df2ad-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="df2ad-105">DESCRIPTION</span></span>
<span data-ttu-id="df2ad-106">O cmdlet **Remove-AzureRmNetworkSecurityRuleConfig** remove uma configuração de regra de segurança de rede de um grupo de segurança de rede do Azure.</span><span class="sxs-lookup"><span data-stu-id="df2ad-106">The **Remove-AzureRmNetworkSecurityRuleConfig** cmdlet removes a network security rule configuration from an Azure network security group.</span></span>

## <span data-ttu-id="df2ad-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="df2ad-107">EXAMPLES</span></span>

### <span data-ttu-id="df2ad-108">Exemplo 1: remover uma configuração de regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="df2ad-108">Example 1: Remove a network security rule configuration</span></span>
```
PS C:\>$rule1 = New-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
PS C:\> $nsg = New-AzureRmNetworkSecurityGroup -ResourceGroupName "TestRG" -Location "westus" -Name "NSG-FrontEnd" -SecurityRules $rule1
PS C:\> Remove-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg
```

<span data-ttu-id="df2ad-109">O primeiro comando cria uma configuração de regra de segurança de rede chamada RDP-Rule e a armazena na variável $rule 1.</span><span class="sxs-lookup"><span data-stu-id="df2ad-109">The first command creates a network security rule configuration named rdp-rule, and then stores it in the $rule1 variable.</span></span>
<span data-ttu-id="df2ad-110">O segundo comando cria um grupo de segurança de rede usando a regra no $rule 1 e armazena o grupo de segurança de rede na variável $nsg.</span><span class="sxs-lookup"><span data-stu-id="df2ad-110">The second command creates a network security group using the rule in $rule1, and then stores the network security group in the $nsg variable.</span></span>
<span data-ttu-id="df2ad-111">O terceiro comando Remove a configuração de regra de segurança de rede chamada RDP-Rule do grupo de segurança de rede em $nsg.</span><span class="sxs-lookup"><span data-stu-id="df2ad-111">The third command removes the network security rule configuration named rdp-rule from the network security group in $nsg.</span></span>

## <span data-ttu-id="df2ad-112">OS</span><span class="sxs-lookup"><span data-stu-id="df2ad-112">PARAMETERS</span></span>

### <span data-ttu-id="df2ad-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df2ad-113">-DefaultProfile</span></span>
<span data-ttu-id="df2ad-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="df2ad-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df2ad-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="df2ad-115">-Name</span></span>
<span data-ttu-id="df2ad-116">Especifica o nome da configuração de regra de segurança de rede que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="df2ad-116">Specifies the name of the network security rule configuration that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df2ad-117">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="df2ad-117">-NetworkSecurityGroup</span></span>
<span data-ttu-id="df2ad-118">Especifica um objeto **NetworkSecurityGroup** .</span><span class="sxs-lookup"><span data-stu-id="df2ad-118">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="df2ad-119">Esse objeto contém a configuração de regra de segurança de rede a ser removida.</span><span class="sxs-lookup"><span data-stu-id="df2ad-119">This object contains the network security rule configuration to remove.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="df2ad-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df2ad-120">CommonParameters</span></span>
<span data-ttu-id="df2ad-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df2ad-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df2ad-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df2ad-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df2ad-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="df2ad-123">INPUTS</span></span>

### <span data-ttu-id="df2ad-124">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="df2ad-124">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>
<span data-ttu-id="df2ad-125">Parâmetros: NetworkSecurityGroup (ByValue)</span><span class="sxs-lookup"><span data-stu-id="df2ad-125">Parameters: NetworkSecurityGroup (ByValue)</span></span>

## <span data-ttu-id="df2ad-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="df2ad-126">OUTPUTS</span></span>

### <span data-ttu-id="df2ad-127">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="df2ad-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="df2ad-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="df2ad-128">NOTES</span></span>

## <span data-ttu-id="df2ad-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="df2ad-129">RELATED LINKS</span></span>

[<span data-ttu-id="df2ad-130">Add-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="df2ad-130">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="df2ad-131">Get-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="df2ad-131">Get-AzureRmNetworkSecurityRuleConfig</span></span>](./Get-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="df2ad-132">New-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="df2ad-132">New-AzureRmNetworkSecurityGroup</span></span>](./New-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="df2ad-133">New-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="df2ad-133">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="df2ad-134">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="df2ad-134">Set-AzureRmNetworkSecurityRuleConfig</span></span>](./Set-AzureRmNetworkSecurityRuleConfig.md)


