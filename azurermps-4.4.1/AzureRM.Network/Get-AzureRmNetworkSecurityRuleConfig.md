---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 5A0D9326-3A8A-4156-8372-EBA93C1BB4E4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkSecurityRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkSecurityRuleConfig.md
ms.openlocfilehash: 903738f1cb2e816ce18c9e5e3c9b01cf3d4baa9a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441009"
---
# <span data-ttu-id="dbfa9-101">Get-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dbfa9-101">Get-AzureRmNetworkSecurityRuleConfig</span></span>

## <span data-ttu-id="dbfa9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dbfa9-102">SYNOPSIS</span></span>
<span data-ttu-id="dbfa9-103">Obter uma configuração de regra de segurança de rede para um grupo de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="dbfa9-103">Get a network security rule configuration for a network security group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dbfa9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dbfa9-104">SYNTAX</span></span>

```
Get-AzureRmNetworkSecurityRuleConfig [-Name <String>] -NetworkSecurityGroup <PSNetworkSecurityGroup>
 [-DefaultRules] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dbfa9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dbfa9-105">DESCRIPTION</span></span>
<span data-ttu-id="dbfa9-106">O cmdlet **Get-AzureRmNetworkSecurityRuleConfig** Obtém uma configuração de regra de segurança de rede para um grupo de segurança de rede do Azure.</span><span class="sxs-lookup"><span data-stu-id="dbfa9-106">The **Get-AzureRmNetworkSecurityRuleConfig** cmdlet gets a network security rule configuration for an Azure network security group.</span></span>

## <span data-ttu-id="dbfa9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dbfa9-107">EXAMPLES</span></span>

### <span data-ttu-id="dbfa9-108">1: Recuperando uma configuração de regra de segurança de rede</span><span class="sxs-lookup"><span data-stu-id="dbfa9-108">1: Retrieving a network security rule config</span></span>
```
Get-AzureRmNetworkSecurityGroup -Name  nsg1 -ResourceGroupName rg1 
    | Get-AzureRmNetworkSecurityRuleConfig -Name AllowInternetOutBound -DefaultRules
```

<span data-ttu-id="dbfa9-109">Esse comando recupera a regra padrão chamada "AllowInternetOutBound" do grupo do Azure Network Security chamado "nsg1" no grupo de recursos "Rg1"</span><span class="sxs-lookup"><span data-stu-id="dbfa9-109">This command retrieves the default rule named "AllowInternetOutBound" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

### <span data-ttu-id="dbfa9-110">2: Recuperando uma configuração de regra de segurança de rede usando somente o nome</span><span class="sxs-lookup"><span data-stu-id="dbfa9-110">2: Retrieving a network security rule config using only the name</span></span>
```
Get-AzureRmNetworkSecurityGroup -Name  nsg1 -ResourceGroupName rg1 
    | Get-AzureRmNetworkSecurityRuleConfig -Name "rdp-rule"
```

<span data-ttu-id="dbfa9-111">Este comando recupera a regra definida pelo usuário chamada "RDP-Rule" do grupo do Azure Network Security chamado "nsg1" no grupo de recursos "Rg1"</span><span class="sxs-lookup"><span data-stu-id="dbfa9-111">This command retrieves user defined rule named "rdp-rule" from Azure network security group named "nsg1" in resource group "rg1"</span></span>

## <span data-ttu-id="dbfa9-112">OS</span><span class="sxs-lookup"><span data-stu-id="dbfa9-112">PARAMETERS</span></span>

### <span data-ttu-id="dbfa9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbfa9-113">-DefaultProfile</span></span>
<span data-ttu-id="dbfa9-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dbfa9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dbfa9-115">-Defaultrules</span><span class="sxs-lookup"><span data-stu-id="dbfa9-115">-DefaultRules</span></span>
<span data-ttu-id="dbfa9-116">Indica se esse cmdlet obtém uma configuração de regra criada pelo usuário ou uma configuração de regra padrão.</span><span class="sxs-lookup"><span data-stu-id="dbfa9-116">Indicates whether this cmdlet gets a user-created rule configuration or a default rule configuration.</span></span>

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

### <span data-ttu-id="dbfa9-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="dbfa9-117">-Name</span></span>
<span data-ttu-id="dbfa9-118">Especifica o nome da configuração de regra de segurança de rede a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="dbfa9-118">Specifies the name of the network security rule configuration to get.</span></span>

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

### <span data-ttu-id="dbfa9-119">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="dbfa9-119">-NetworkSecurityGroup</span></span>
<span data-ttu-id="dbfa9-120">Especifica um objeto **NetworkSecurityGroup** que contém a configuração da regra de segurança de rede a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="dbfa9-120">Specifies a **NetworkSecurityGroup** object that contains the network security rule configuration to get.</span></span>

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

### <span data-ttu-id="dbfa9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbfa9-121">CommonParameters</span></span>
<span data-ttu-id="dbfa9-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbfa9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbfa9-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbfa9-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbfa9-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dbfa9-124">INPUTS</span></span>

### <span data-ttu-id="dbfa9-125">PSNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="dbfa9-125">PSNetworkSecurityGroup</span></span>
<span data-ttu-id="dbfa9-126">O parâmetro ' NetworkSecurityGroup ' aceita o valor do tipo ' PSNetworkSecurityGroup ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="dbfa9-126">Parameter 'NetworkSecurityGroup' accepts value of type 'PSNetworkSecurityGroup' from the pipeline</span></span>

## <span data-ttu-id="dbfa9-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dbfa9-127">OUTPUTS</span></span>

### <span data-ttu-id="dbfa9-128">Microsoft. Azure. Commands. Network. Models. PSSecurityRule</span><span class="sxs-lookup"><span data-stu-id="dbfa9-128">Microsoft.Azure.Commands.Network.Models.PSSecurityRule</span></span>

## <span data-ttu-id="dbfa9-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dbfa9-129">NOTES</span></span>

## <span data-ttu-id="dbfa9-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dbfa9-130">RELATED LINKS</span></span>

[<span data-ttu-id="dbfa9-131">Add-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dbfa9-131">Add-AzureRmNetworkSecurityRuleConfig</span></span>](./Add-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="dbfa9-132">New-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dbfa9-132">New-AzureRmNetworkSecurityRuleConfig</span></span>](./New-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="dbfa9-133">Remove-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dbfa9-133">Remove-AzureRmNetworkSecurityRuleConfig</span></span>](./Remove-AzureRmNetworkSecurityRuleConfig.md)

[<span data-ttu-id="dbfa9-134">Set-AzureRmNetworkSecurityRuleConfig</span><span class="sxs-lookup"><span data-stu-id="dbfa9-134">Set-AzureRmNetworkSecurityRuleConfig</span></span>](./Set-AzureRmNetworkSecurityRuleConfig.md)


