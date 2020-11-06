---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9F69DAEF-F2ED-449B-B75F-FCA7ED73D98F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworksecuritygroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkSecurityGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkSecurityGroup.md
ms.openlocfilehash: 3ef8248f90e24da8818a0fa1a8ff6b05970be397
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426315"
---
# <span data-ttu-id="ce3b0-101">Set-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ce3b0-101">Set-AzureRmNetworkSecurityGroup</span></span>

## <span data-ttu-id="ce3b0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ce3b0-102">SYNOPSIS</span></span>
<span data-ttu-id="ce3b0-103">Define o estado da meta para um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="ce3b0-103">Sets the goal state for a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce3b0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ce3b0-104">SYNTAX</span></span>

```
Set-AzureRmNetworkSecurityGroup -NetworkSecurityGroup <PSNetworkSecurityGroup> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce3b0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ce3b0-105">DESCRIPTION</span></span>
<span data-ttu-id="ce3b0-106">O cmdlet **set-AzureRmNetworkSecurityGroup** define o estado da meta para um grupo de segurança de rede do Azure.</span><span class="sxs-lookup"><span data-stu-id="ce3b0-106">The **Set-AzureRmNetworkSecurityGroup** cmdlet sets the goal state for an Azure network security group.</span></span>

## <span data-ttu-id="ce3b0-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ce3b0-107">EXAMPLES</span></span>

### <span data-ttu-id="ce3b0-108">Exemplo 1: definir o estado da meta para um grupo de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="ce3b0-108">Example 1: Set the goal state for a network security group</span></span>
```
PS C:\>Get-AzureRmNetworkSecurityGroup -Name "Nsg1" -ResourceGroupName "Rg1" | Add-AzureRmNetworkSecurityRuleConfig -Name "Rdp-Rule" -Description "Allow RDP" -Access "Allow" -Protocol "Tcp" -Direction "Inbound" -Priority 100 -SourceAddressPrefix "Internet" -SourcePortRange "*" -DestinationAddressPrefix "*" -DestinationPortRange "3389" | Set-AzureRmNetworkSecurityGroup
```

<span data-ttu-id="ce3b0-109">Esse comando obtém o grupo de segurança de rede do Azure chamado Nsg1 e adiciona uma regra de segurança de rede chamada Rdp-Rule para permitir o tráfego de Internet na porta 3389 para o objeto do grupo de segurança de rede recuperada usando Add-AzureRmNetworkSecurityRuleConfig.</span><span class="sxs-lookup"><span data-stu-id="ce3b0-109">This command gets the Azure network security group named Nsg1, and adds a network security rule named Rdp-Rule to allow Internet traffic on port 3389 to the retrieved network security group object using Add-AzureRmNetworkSecurityRuleConfig.</span></span>
<span data-ttu-id="ce3b0-110">O comando persiste o grupo de segurança de rede do Azure modificado usando **set-AzureRmNetworkSecurityGroup**.</span><span class="sxs-lookup"><span data-stu-id="ce3b0-110">The command persists the modified Azure network security group using **Set-AzureRmNetworkSecurityGroup**.</span></span>

## <span data-ttu-id="ce3b0-111">OS</span><span class="sxs-lookup"><span data-stu-id="ce3b0-111">PARAMETERS</span></span>

### <span data-ttu-id="ce3b0-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ce3b0-112">-AsJob</span></span>
<span data-ttu-id="ce3b0-113">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="ce3b0-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ce3b0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce3b0-114">-DefaultProfile</span></span>
<span data-ttu-id="ce3b0-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ce3b0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce3b0-116">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ce3b0-116">-NetworkSecurityGroup</span></span>
<span data-ttu-id="ce3b0-117">Um objeto de grupo de segurança de rede que representa o estado da meta à qual o cmdlet define o grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="ce3b0-117">A network security group object representing the goal state to which the cmdlet sets the network security group.</span></span>

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

### <span data-ttu-id="ce3b0-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ce3b0-118">-Confirm</span></span>
<span data-ttu-id="ce3b0-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce3b0-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce3b0-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce3b0-120">-WhatIf</span></span>
<span data-ttu-id="ce3b0-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ce3b0-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ce3b0-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ce3b0-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce3b0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce3b0-123">CommonParameters</span></span>
<span data-ttu-id="ce3b0-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce3b0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce3b0-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce3b0-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce3b0-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ce3b0-126">INPUTS</span></span>

### <span data-ttu-id="ce3b0-127">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ce3b0-127">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>
<span data-ttu-id="ce3b0-128">Parâmetros: NetworkSecurityGroup (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ce3b0-128">Parameters: NetworkSecurityGroup (ByValue)</span></span>

## <span data-ttu-id="ce3b0-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ce3b0-129">OUTPUTS</span></span>

### <span data-ttu-id="ce3b0-130">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ce3b0-130">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="ce3b0-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ce3b0-131">NOTES</span></span>

## <span data-ttu-id="ce3b0-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ce3b0-132">RELATED LINKS</span></span>

[<span data-ttu-id="ce3b0-133">Get-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ce3b0-133">Get-AzureRmNetworkSecurityGroup</span></span>](./Get-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="ce3b0-134">New-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ce3b0-134">New-AzureRmNetworkSecurityGroup</span></span>](./New-AzureRmNetworkSecurityGroup.md)

[<span data-ttu-id="ce3b0-135">Remove-AzureRmNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="ce3b0-135">Remove-AzureRmNetworkSecurityGroup</span></span>](./Remove-AzureRmNetworkSecurityGroup.md)


