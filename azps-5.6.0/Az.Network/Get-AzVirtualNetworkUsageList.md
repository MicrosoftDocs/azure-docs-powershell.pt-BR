---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworkusagelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkUsageList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkUsageList.md
ms.openlocfilehash: b4daa24f787633d2f18896910faed340a969a0f9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891338"
---
# <span data-ttu-id="f3f74-101">Get-AzVirtualNetworkUsageList</span><span class="sxs-lookup"><span data-stu-id="f3f74-101">Get-AzVirtualNetworkUsageList</span></span>

## <span data-ttu-id="f3f74-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3f74-102">SYNOPSIS</span></span>
<span data-ttu-id="f3f74-103">Obtém o uso atual da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="f3f74-103">Gets virtual network current usage.</span></span>

## <span data-ttu-id="f3f74-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="f3f74-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkUsageList -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3f74-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="f3f74-105">DESCRIPTION</span></span>
<span data-ttu-id="f3f74-106">O cmdlet **Get-AzVirtualNetworkUsageList** obtém o uso por sub-rede da rede virtual especificada.</span><span class="sxs-lookup"><span data-stu-id="f3f74-106">The **Get-AzVirtualNetworkUsageList** cmdlet gets per subnet usage for the specified virtual network.</span></span>

## <span data-ttu-id="f3f74-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f3f74-107">EXAMPLES</span></span>

### <span data-ttu-id="f3f74-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f3f74-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkUsageList -ResourceGroupName test -Name usagetest

Get-AzVirtualNetworkUsageList -ResourceGroupName test -Name usagetest

Name         : Subnet size and usage
Id           : /subscriptions/sub1/resourceGroups/test/providers/Microsoft.Network/virtualNetworks/usagetest/subnets/subnet
CurrentValue : 1
Limit        : 65531
Unit         : Count

Name         : Subnet size and usage
Id           : /subscriptions/sub1/resourceGroups/test/providers/Microsoft.Network/virtualNetworks/usagetest/subnets/subnet11
CurrentValue : 0
Limit        : 251
Unit         : Count
```

<span data-ttu-id="f3f74-109">Obtém por sub-rede valores atuais de uso para a rede virtual mais testada.</span><span class="sxs-lookup"><span data-stu-id="f3f74-109">Gets per subnet current values of usage for usagetest virtual network.</span></span>

## <span data-ttu-id="f3f74-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="f3f74-110">PARAMETERS</span></span>

### <span data-ttu-id="f3f74-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3f74-111">-DefaultProfile</span></span>
<span data-ttu-id="f3f74-112">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="f3f74-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3f74-113">-Name</span><span class="sxs-lookup"><span data-stu-id="f3f74-113">-Name</span></span>
<span data-ttu-id="f3f74-114">Especifica o nome da rede virtual para o que mostrar os usos.</span><span class="sxs-lookup"><span data-stu-id="f3f74-114">Specifies the name of the virtual network to show usages for.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3f74-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3f74-115">-ResourceGroupName</span></span>
<span data-ttu-id="f3f74-116">Especifica o nome do grupo de recursos ao que a rede virtual pertence.</span><span class="sxs-lookup"><span data-stu-id="f3f74-116">Specifies the name of the resource group that virtual network belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3f74-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3f74-117">CommonParameters</span></span>
<span data-ttu-id="f3f74-118">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3f74-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3f74-119">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f3f74-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3f74-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="f3f74-120">INPUTS</span></span>

### <span data-ttu-id="f3f74-121">System.String</span><span class="sxs-lookup"><span data-stu-id="f3f74-121">System.String</span></span>

## <span data-ttu-id="f3f74-122">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="f3f74-122">OUTPUTS</span></span>

### <span data-ttu-id="f3f74-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkUsage</span><span class="sxs-lookup"><span data-stu-id="f3f74-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkUsage</span></span>

## <span data-ttu-id="f3f74-124">NOTES</span><span class="sxs-lookup"><span data-stu-id="f3f74-124">NOTES</span></span>

## <span data-ttu-id="f3f74-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f3f74-125">RELATED LINKS</span></span>
