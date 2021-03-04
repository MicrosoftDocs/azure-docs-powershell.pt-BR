---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9F69DAEF-F2ED-449B-B75F-FCA7ED73D98F
online version: https://docs.microsoft.com/powershell/module/az.network/set-aznetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkSecurityGroup.md
ms.openlocfilehash: 91144275806c5e3a6913d39990ad68644c71b244
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892065"
---
# <span data-ttu-id="20ae0-101">Set-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="20ae0-101">Set-AzNetworkSecurityGroup</span></span>

## <span data-ttu-id="20ae0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20ae0-102">SYNOPSIS</span></span>
<span data-ttu-id="20ae0-103">Atualiza um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="20ae0-103">Updates a network security group.</span></span>

## <span data-ttu-id="20ae0-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="20ae0-104">SYNTAX</span></span>

```
Set-AzNetworkSecurityGroup -NetworkSecurityGroup <PSNetworkSecurityGroup> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20ae0-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="20ae0-105">DESCRIPTION</span></span>
<span data-ttu-id="20ae0-106">O cmdlet **Set-AzNetworkSecurityGroup** atualiza um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="20ae0-106">The **Set-AzNetworkSecurityGroup** cmdlet updates a network security group.</span></span>

## <span data-ttu-id="20ae0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="20ae0-107">EXAMPLES</span></span>

### <span data-ttu-id="20ae0-108">Exemplo 1: atualizar um grupo de segurança de rede existente</span><span class="sxs-lookup"><span data-stu-id="20ae0-108">Example 1: Update an existing network security group</span></span>
```
PS C:\>Get-AzNetworkSecurityGroup -Name "Nsg1" -ResourceGroupName "Rg1" | Add-AzNetworkSecurityRuleConfig -Name "Rdp-Rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange "*" -DestinationAddressPrefix "*" -DestinationPortRange "3389" | Set-AzNetworkSecurityGroup
```

<span data-ttu-id="20ae0-109">Este comando obtém o grupo de segurança de rede do Azure chamado Nsg1 e adiciona uma regra de segurança de rede chamada Rdp-Rule para permitir o tráfego de Internet na porta 3389 para o objeto do grupo de segurança de rede recuperado usando Add-AzNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="20ae0-109">This command gets the Azure network security group named Nsg1, and adds a network security rule named Rdp-Rule to allow Internet traffic on port 3389 to the retrieved network security group object using Add-AzNetworkSecurityRuleConfig.</span></span>
<span data-ttu-id="20ae0-110">O comando persiste no grupo de segurança de rede modificado do Azure usando **Set-AzNetworkSecurityGroup**.</span><span class="sxs-lookup"><span data-stu-id="20ae0-110">The command persists the modified Azure network security group using **Set-AzNetworkSecurityGroup**.</span></span>

## <span data-ttu-id="20ae0-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="20ae0-111">PARAMETERS</span></span>

### <span data-ttu-id="20ae0-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="20ae0-112">-AsJob</span></span>
<span data-ttu-id="20ae0-113">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="20ae0-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="20ae0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20ae0-114">-DefaultProfile</span></span>
<span data-ttu-id="20ae0-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="20ae0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20ae0-116">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="20ae0-116">-NetworkSecurityGroup</span></span>
<span data-ttu-id="20ae0-117">Especifica um objeto de grupo de segurança de rede que representa o estado ao qual o grupo de segurança de rede deve ser definido.</span><span class="sxs-lookup"><span data-stu-id="20ae0-117">Specifies a network security group object representing the state to which the network security group should be set.</span></span>

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

### <span data-ttu-id="20ae0-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="20ae0-118">-Confirm</span></span>
<span data-ttu-id="20ae0-119">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20ae0-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20ae0-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20ae0-120">-WhatIf</span></span>
<span data-ttu-id="20ae0-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="20ae0-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="20ae0-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="20ae0-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20ae0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20ae0-123">CommonParameters</span></span>
<span data-ttu-id="20ae0-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20ae0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20ae0-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20ae0-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20ae0-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="20ae0-126">INPUTS</span></span>

### <span data-ttu-id="20ae0-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="20ae0-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="20ae0-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="20ae0-128">OUTPUTS</span></span>

### <span data-ttu-id="20ae0-129">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="20ae0-129">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="20ae0-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="20ae0-130">NOTES</span></span>

## <span data-ttu-id="20ae0-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="20ae0-131">RELATED LINKS</span></span>

[<span data-ttu-id="20ae0-132">Get-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="20ae0-132">Get-AzNetworkSecurityGroup</span></span>](./Get-AzNetworkSecurityGroup.md)

[<span data-ttu-id="20ae0-133">New-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="20ae0-133">New-AzNetworkSecurityGroup</span></span>](./New-AzNetworkSecurityGroup.md)

[<span data-ttu-id="20ae0-134">Remove-AzNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="20ae0-134">Remove-AzNetworkSecurityGroup</span></span>](./Remove-AzNetworkSecurityGroup.md)


