---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5A0D9326-3A8A-4156-8372-EBA93C1BB4E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworksecurityruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkSecurityRuleConfig.md
ms.openlocfilehash: 3d8b2445d6bb1c92d7246f1d9f33a06dfef3c58b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98271858"
---
# <span data-ttu-id="3711b-101">Get-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3711b-101">Get-AzNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="3711b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3711b-102">SYNOPSIS</span></span>
<span data-ttu-id="3711b-103">Obter uma configuração de regra de segurança de rede para um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="3711b-103">Get a network security rule configuration for a network security group.</span></span>

## <span data-ttu-id="3711b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3711b-104">SYNTAX</span></span>

```
Get-AzNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup> [-DefaultRules]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3711b-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3711b-105">DESCRIPTION</span></span>
<span data-ttu-id="3711b-106">O cmdlet **Get-AzNetworkSecurityRuleConfig** Obtém uma configuração de regra de segurança de rede para um grupo de segurança de rede do Azure.</span><span class="sxs-lookup"><span data-stu-id="3711b-106">The **Get-AzNetworkSecurityRuleConfig** cmdlet gets a network security rule configuration for an Azure network security group.</span></span>

## <span data-ttu-id="3711b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3711b-107">EXAMPLES</span></span>

### <span data-ttu-id="3711b-108">1: Recuperando uma configuração de regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="3711b-108">1: Retrieving a network security rule config</span></span>
```
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 
    | Get-AzNetworkSecurityRuleConfig -Name AllowInternetOutBound -DefaultRules
```

<span data-ttu-id="3711b-109">Esse comando recupera a regra padrão chamada "AllowInternetOutBound" do grupo do Azure Network Security chamado "nsg1" no grupo de recursos "Rg1"</span><span class="sxs-lookup"><span data-stu-id="3711b-109">This command retrieves the default rule named "AllowInternetOutBound" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

### <span data-ttu-id="3711b-110">2: Recuperando uma configuração de regra de segurança de rede usando somente o nome</span><span class="sxs-lookup"><span data-stu-id="3711b-110">2: Retrieving a network security rule config using only the name</span></span>
```
Get-AzNetworkSecurityGroup -Name nsg1 -ResourceGroupName rg1 
    | Get-AzNetworkSecurityRuleConfig -Name "rdp-rule"
```

<span data-ttu-id="3711b-111">Este comando recupera a regra definida pelo usuário chamada "RDP-Rule" do grupo do Azure Network Security chamado "nsg1" no grupo de recursos "Rg1"</span><span class="sxs-lookup"><span data-stu-id="3711b-111">This command retrieves user defined rule named "rdp-rule" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

## <span data-ttu-id="3711b-112">OS</span><span class="sxs-lookup"><span data-stu-id="3711b-112">PARAMETERS</span></span>

### <span data-ttu-id="3711b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3711b-113">-DefaultProfile</span></span>
<span data-ttu-id="3711b-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3711b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3711b-115">-Defaultrules</span><span class="sxs-lookup"><span data-stu-id="3711b-115">-DefaultRules</span></span>
<span data-ttu-id="3711b-116">Indica se esse cmdlet obtém uma configuração de regra criada pelo usuário ou uma configuração de regra padrão.</span><span class="sxs-lookup"><span data-stu-id="3711b-116">Indicates whether this cmdlet gets a user-created rule configuration or a default rule configuration.</span></span>

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

### <span data-ttu-id="3711b-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="3711b-117">-Name</span></span>
<span data-ttu-id="3711b-118">Especifica o nome da configuração de regra de segurança de rede a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="3711b-118">Specifies the name of the network security rule configuration to get.</span></span>

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

### <span data-ttu-id="3711b-119">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3711b-119">-NetworkSecurityGroup</span></span>
<span data-ttu-id="3711b-120">Especifica um objeto **NetworkSecurityGroup** que contém a configuração da regra de segurança de rede a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="3711b-120">Specifies a **NetworkSecurityGroup** object that contains the network security rule configuration to get.</span></span>

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

### <span data-ttu-id="3711b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3711b-121">CommonParameters</span></span>
<span data-ttu-id="3711b-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3711b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3711b-123">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3711b-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3711b-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3711b-124">INPUTS</span></span>

### <span data-ttu-id="3711b-125">Microsoft. Azure. Commands. Network. Models. PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3711b-125">Microsoft.Azure.Commands.Network.Models.PSNetworkSecurityGroup</span></span>

## <span data-ttu-id="3711b-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3711b-126">OUTPUTS</span></span>

### <span data-ttu-id="3711b-127">Microsoft. Azure. Commands. Network. Models. PSSecurityRule</span><span class="sxs-lookup"><span data-stu-id="3711b-127">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="3711b-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3711b-128">NOTES</span></span>

## <span data-ttu-id="3711b-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3711b-129">RELATED LINKS</span></span>

[<span data-ttu-id="3711b-130">Add-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3711b-130">Add-AzNetworkSecurityRuleConfig</span></span>](./Add-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="3711b-131">New-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3711b-131">New-AzNetworkSecurityRuleConfig</span></span>](./New-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="3711b-132">Remove-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3711b-132">Remove-AzNetworkSecurityRuleConfig</span></span>](./Remove-AzNetworkSecurityRuleConfig.md)

[<span data-ttu-id="3711b-133">Set-AzNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="3711b-133">Set-AzNetworkSecurityRuleConfig</span></span>](./Set-AzNetworkSecurityRuleConfig.md)


