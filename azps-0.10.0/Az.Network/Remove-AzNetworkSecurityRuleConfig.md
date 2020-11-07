---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2E43D0D8-EF93-443B-AA8F-58C992026E95
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 8a2851f34cfbeb9fec72830334c52a9b4a83d064
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775281"
---
# <span data-ttu-id="3129f-101">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3129f-101">Remove-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="3129f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3129f-102">SYNOPSIS</span></span>
<span data-ttu-id="3129f-103">Remove uma regra de segurança de rede de um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="3129f-103">Removes a network security rule from a network security group.</span></span>

## <span data-ttu-id="3129f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3129f-104">SYNTAX</span></span>

```
Remove-AzNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3129f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3129f-105">DESCRIPTION</span></span>
<span data-ttu-id="3129f-106">O cmdlet **Remove-AzNetworkSecurityRuleConfig** remove uma configuração de regra de segurança de rede de um grupo de segurança de rede do Azure.</span><span class="sxs-lookup"><span data-stu-id="3129f-106">The **Remove-AzNetworkSecurityRuleConfig** cmdlet removes a network security rule configuration from an Azure network security group.</span></span>

## <span data-ttu-id="3129f-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3129f-107">EXAMPLES</span></span>

### <span data-ttu-id="3129f-108">Exemplo 1: remover uma configuração de regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="3129f-108">Example 1: Remove a network security rule configuration</span></span>
```
PS C:\>$rule1 = New-AzNetworkSecurityRuleConfig -Name "rdp-rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
PS C:\> $nsg = New-AzNetworkSecurityGroup -ResourceGroupName "TestRG" -Location "westus" -Name "NSG-FrontEnd" -SecurityRules $rule1
PS C:\> Remove-AzNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg
```

<span data-ttu-id="3129f-109">O primeiro comando cria uma configuração de regra de segurança de rede chamada RDP-Rule e a armazena na variável $rule 1.</span><span class="sxs-lookup"><span data-stu-id="3129f-109">The first command creates a network security rule configuration named rdp-rule, and then stores it in the $rule1 variable.</span></span>

<span data-ttu-id="3129f-110">O segundo comando cria um grupo de segurança de rede usando a regra no $rule 1 e armazena o grupo de segurança de rede na variável $nsg.</span><span class="sxs-lookup"><span data-stu-id="3129f-110">The second command creates a network security group using the rule in $rule1, and then stores the network security group in the $nsg variable.</span></span>

<span data-ttu-id="3129f-111">O terceiro comando Remove a configuração de regra de segurança de rede chamada RDP-Rule do grupo de segurança de rede em $nsg.</span><span class="sxs-lookup"><span data-stu-id="3129f-111">The third command removes the network security rule configuration named rdp-rule from the network security group in $nsg.</span></span>

## <span data-ttu-id="3129f-112">OS</span><span class="sxs-lookup"><span data-stu-id="3129f-112">PARAMETERS</span></span>

### <span data-ttu-id="3129f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3129f-113">-DefaultProfile</span></span>
<span data-ttu-id="3129f-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3129f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3129f-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="3129f-115">-Name</span></span>
<span data-ttu-id="3129f-116">Especifica o nome da configuração de regra de segurança de rede que este cmdlet Remove.</span><span class="sxs-lookup"><span data-stu-id="3129f-116">Specifies the name of the network security rule configuration that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3129f-117">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3129f-117">-NetworkSecurityGroup</span></span>
<span data-ttu-id="3129f-118">Especifica um objeto **NetworkSecurityGroup** .</span><span class="sxs-lookup"><span data-stu-id="3129f-118">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="3129f-119">Esse objeto contém a configuração de regra de segurança de rede a ser removida.</span><span class="sxs-lookup"><span data-stu-id="3129f-119">This object contains the network security rule configuration to remove.</span></span>

```yaml
Type: PSNetworkSecurityGroup
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3129f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3129f-120">CommonParameters</span></span>
<span data-ttu-id="3129f-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3129f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3129f-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3129f-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3129f-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3129f-123">INPUTS</span></span>

### <span data-ttu-id="3129f-124">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3129f-124">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="3129f-125">O parâmetro ' NetworkSecurityGroup ' aceita o valor do tipo ' PSNetworkSecurityGroup ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="3129f-125">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="3129f-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3129f-126">OUTPUTS</span></span>

### <span data-ttu-id="3129f-127">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3129f-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="3129f-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3129f-128">NOTES</span></span>

## <span data-ttu-id="3129f-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3129f-129">RELATED LINKS</span></span>

[<span data-ttu-id="3129f-130">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3129f-130">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="3129f-131">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3129f-131">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="3129f-132">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3129f-132">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="3129f-133">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3129f-133">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="3129f-134">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3129f-134">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


