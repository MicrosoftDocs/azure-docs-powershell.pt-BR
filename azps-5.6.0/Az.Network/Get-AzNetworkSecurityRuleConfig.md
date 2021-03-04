---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5A0D9326-3A8A-4156-8372-EBA93C1BB4E4
online version: https://docs.microsoft.com/powershell/module/az.network/get-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: c45df01f86abcd7a2f475b62b517765f3045cb10
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101892442"
---
# <span data-ttu-id="8acda-101">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8acda-101">Get-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="8acda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8acda-102">SYNOPSIS</span></span>
<span data-ttu-id="8acda-103">Obter uma configuração de regra de segurança de rede para um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="8acda-103">Get a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="8acda-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8acda-104">SYNTAX</span></span>

```
Get-AzNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup> [-DefaultRules]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8acda-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8acda-105">DESCRIPTION</span></span>
<span data-ttu-id="8acda-106">O cmdlet **Get-AzNetworkSecurityRuleConfig obtém** uma configuração de regra de segurança de rede para um grupo de segurança de rede do Azure.</span><span class="sxs-lookup"><span data-stu-id="8acda-106">The **Get-AzNetworkSecurityRuleConfig** cmdlet gets a network security rule configuration for an Azure network security group.</span></span>

## <span data-ttu-id="8acda-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8acda-107">EXAMPLES</span></span>

### <span data-ttu-id="8acda-108">1: Recuperando uma configuração de regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="8acda-108">1: Retrieving a network security rule config</span></span>
```
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 
    | Get-AzNetworkSecurityRuleConfig -Name AllowInternetOutBound -DefaultRules
```

<span data-ttu-id="8acda-109">Este comando recupera a regra padrão chamada "AllowInternetOutBound" do grupo de segurança de rede do Azure chamado "nsg1" no grupo de recursos "rg1"</span><span class="sxs-lookup"><span data-stu-id="8acda-109">This command retrieves the default rule named "AllowInternetOutBound" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

### <span data-ttu-id="8acda-110">2: Recuperar uma configuração de regra de segurança de rede usando apenas o nome</span><span class="sxs-lookup"><span data-stu-id="8acda-110">2: Retrieving a network security rule config using only the name</span></span>
```
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 
    | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
```

<span data-ttu-id="8acda-111">Este comando recupera uma regra definida pelo usuário chamada "rdp-rule" do grupo de segurança de rede do Azure chamado "nsg1" no grupo de recursos "rg1"</span><span class="sxs-lookup"><span data-stu-id="8acda-111">This command retrieves user defined rule named "rdp-rule" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

## <span data-ttu-id="8acda-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8acda-112">PARAMETERS</span></span>

### <span data-ttu-id="8acda-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8acda-113">-DefaultProfile</span></span>
<span data-ttu-id="8acda-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="8acda-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8acda-115">-DefaultRules</span><span class="sxs-lookup"><span data-stu-id="8acda-115">-DefaultRules</span></span>
<span data-ttu-id="8acda-116">Indica se esse cmdlet obtém uma configuração de regra criada pelo usuário ou uma configuração de regra padrão.</span><span class="sxs-lookup"><span data-stu-id="8acda-116">Indicates whether this cmdlet gets a user-created rule configuration or a default rule configuration.</span></span>

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

### <span data-ttu-id="8acda-117">-Name</span><span class="sxs-lookup"><span data-stu-id="8acda-117">-Name</span></span>
<span data-ttu-id="8acda-118">Especifica o nome da configuração da regra de segurança de rede a ser obter.</span><span class="sxs-lookup"><span data-stu-id="8acda-118">Specifies the name of the network security rule configuration to get.</span></span>

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

### <span data-ttu-id="8acda-119">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8acda-119">-NetworkSecurityGroup</span></span>
<span data-ttu-id="8acda-120">Especifica um **objeto NetworkSecurityGroup** que contém a configuração de regra de segurança de rede a ser obter.</span><span class="sxs-lookup"><span data-stu-id="8acda-120">Specifies a **NetworkSecurityGroup** object that contains the network security rule configuration to get.</span></span>

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

### <span data-ttu-id="8acda-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8acda-121">CommonParameters</span></span>
<span data-ttu-id="8acda-122">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8acda-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8acda-123">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8acda-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8acda-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8acda-124">INPUTS</span></span>

### <span data-ttu-id="8acda-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="8acda-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="8acda-126">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8acda-126">OUTPUTS</span></span>

### <span data-ttu-id="8acda-127">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span><span class="sxs-lookup"><span data-stu-id="8acda-127">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="8acda-128">NOTES</span><span class="sxs-lookup"><span data-stu-id="8acda-128">NOTES</span></span>

## <span data-ttu-id="8acda-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8acda-129">RELATED LINKS</span></span>

[<span data-ttu-id="8acda-130">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8acda-130">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="8acda-131">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8acda-131">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="8acda-132">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8acda-132">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="8acda-133">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8acda-133">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


