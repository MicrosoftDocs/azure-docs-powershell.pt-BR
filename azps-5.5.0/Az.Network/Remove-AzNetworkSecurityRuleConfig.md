---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2E43D0D8-EF93-443B-AA8F-58C992026E95
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 7f5d41774af2f5ee74c5d343fa9b143801c139f2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114656"
---
# <span data-ttu-id="fd15c-101">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fd15c-101">Remove-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="fd15c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fd15c-102">SYNOPSIS</span></span>
<span data-ttu-id="fd15c-103">Remove uma regra de segurança de rede de um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="fd15c-103">Removes a network security rule from a network security group.</span></span>

## <span data-ttu-id="fd15c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fd15c-104">SYNTAX</span></span>

```
Remove-AzNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd15c-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="fd15c-105">DESCRIPTION</span></span>
<span data-ttu-id="fd15c-106">O cmdlet **Remove-AzNetworkSecurityRuleConfig** remove uma configuração de regra de segurança de rede de um grupo de segurança de rede do Azure.</span><span class="sxs-lookup"><span data-stu-id="fd15c-106">The **Remove-AzNetworkSecurityRuleConfig** cmdlet removes a network security rule configuration from an Azure network security group.</span></span>

## <span data-ttu-id="fd15c-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fd15c-107">EXAMPLES</span></span>

### <span data-ttu-id="fd15c-108">Exemplo 1: Remover uma configuração de regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="fd15c-108">Example 1: Remove a network security rule configuration</span></span>
```
PS C:\>$rule1 = New-AzNetworkSecurityRuleConfig -Name "rdp-rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange * -DestinationAddressPrefix * -DestinationPortRange 3389
PS C:\> $nsg = New-AzNetworkSecurityGroup -ResourceGroupName "TestRG" -Location "westus" -Name "NSG-FrontEnd" -SecurityRules $rule1
PS C:\> Remove-AzNetworkSecurityRuleConfig -Name "rdp-rule" -NetworkSecurityGroup $nsg
PS C:\> $nsg | Set-AzNetworkSecurityGroup
```

<span data-ttu-id="fd15c-109">O primeiro comando cria uma configuração de regra de segurança de rede chamada rdp-rule e a armazena na variável $rule 1.</span><span class="sxs-lookup"><span data-stu-id="fd15c-109">The first command creates a network security rule configuration named rdp-rule, and then stores it in the $rule1 variable.</span></span>
<span data-ttu-id="fd15c-110">O segundo comando cria um grupo de segurança de rede usando a regra no $rule 1 e armazena o grupo de segurança de rede na variável $nsg de rede.</span><span class="sxs-lookup"><span data-stu-id="fd15c-110">The second command creates a network security group using the rule in $rule1, and then stores the network security group in the $nsg variable.</span></span>
<span data-ttu-id="fd15c-111">O terceiro comando remove a configuração de regra de segurança de rede chamada rdp-rule do grupo de segurança de rede no $nsg.</span><span class="sxs-lookup"><span data-stu-id="fd15c-111">The third command removes the network security rule configuration named rdp-rule from the network security group in $nsg.</span></span>
<span data-ttu-id="fd15c-112">O comando forth salva a alteração.</span><span class="sxs-lookup"><span data-stu-id="fd15c-112">The forth command saves the change.</span></span>

## <span data-ttu-id="fd15c-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fd15c-113">PARAMETERS</span></span>

### <span data-ttu-id="fd15c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd15c-114">-DefaultProfile</span></span>
<span data-ttu-id="fd15c-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="fd15c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd15c-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="fd15c-116">-Name</span></span>
<span data-ttu-id="fd15c-117">Especifica o nome da configuração da regra de segurança de rede que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="fd15c-117">Specifies the name of the network security rule configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="fd15c-118">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="fd15c-118">-NetworkSecurityGroup</span></span>
<span data-ttu-id="fd15c-119">Especifica um objeto **NetworkSecurityGroup.**</span><span class="sxs-lookup"><span data-stu-id="fd15c-119">Specifies a **NetworkSecurityGroup** object.</span></span>
<span data-ttu-id="fd15c-120">Este objeto contém a configuração da regra de segurança de rede a ser removido.</span><span class="sxs-lookup"><span data-stu-id="fd15c-120">This object contains the network security rule configuration to remove.</span></span>

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

### <span data-ttu-id="fd15c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd15c-121">CommonParameters</span></span>
<span data-ttu-id="fd15c-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd15c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd15c-123">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd15c-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd15c-124">Entradas</span><span class="sxs-lookup"><span data-stu-id="fd15c-124">INPUTS</span></span>

### <span data-ttu-id="fd15c-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="fd15c-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="fd15c-126">Saídas</span><span class="sxs-lookup"><span data-stu-id="fd15c-126">OUTPUTS</span></span>

### <span data-ttu-id="fd15c-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="fd15c-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="fd15c-128">Notas</span><span class="sxs-lookup"><span data-stu-id="fd15c-128">NOTES</span></span>

## <span data-ttu-id="fd15c-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fd15c-129">RELATED LINKS</span></span>

[<span data-ttu-id="fd15c-130">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fd15c-130">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="fd15c-131">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fd15c-131">Get-AzNetworkSecurityRuleConfig</span></span>](./Get-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="fd15c-132">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="fd15c-132">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="fd15c-133">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fd15c-133">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="fd15c-134">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="fd15c-134">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


