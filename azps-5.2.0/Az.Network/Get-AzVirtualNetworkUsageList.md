---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkusagelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkUsageList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkUsageList.md
ms.openlocfilehash: 023eb245132a7b451fc6e30351db5751fb754cde
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98257118"
---
# <span data-ttu-id="0f4f6-101">Get-AzVirtualNetworkUsageList</span><span class="sxs-lookup"><span data-stu-id="0f4f6-101">Get-AzVirtualNetworkUsageList</span></span>

## <span data-ttu-id="0f4f6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0f4f6-102">SYNOPSIS</span></span>
<span data-ttu-id="0f4f6-103">Obtém o uso atual da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="0f4f6-103">Gets virtual network current usage.</span></span>

## <span data-ttu-id="0f4f6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0f4f6-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkUsageList -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f4f6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0f4f6-105">DESCRIPTION</span></span>
<span data-ttu-id="0f4f6-106">O cmdlet **Get-AzVirtualNetworkUsageList** tem uso por sub-rede para a rede virtual especificada.</span><span class="sxs-lookup"><span data-stu-id="0f4f6-106">The **Get-AzVirtualNetworkUsageList** cmdlet gets per subnet usage for the specified virtual network.</span></span>

## <span data-ttu-id="0f4f6-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0f4f6-107">EXAMPLES</span></span>

### <span data-ttu-id="0f4f6-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0f4f6-108">Example 1</span></span>
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

<span data-ttu-id="0f4f6-109">Obtém valores atuais de uso de sub-rede para a rede virtual usagetest.</span><span class="sxs-lookup"><span data-stu-id="0f4f6-109">Gets per subnet current values of usage for usagetest virtual network.</span></span>

## <span data-ttu-id="0f4f6-110">OS</span><span class="sxs-lookup"><span data-stu-id="0f4f6-110">PARAMETERS</span></span>

### <span data-ttu-id="0f4f6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f4f6-111">-DefaultProfile</span></span>
<span data-ttu-id="0f4f6-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0f4f6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f4f6-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="0f4f6-113">-Name</span></span>
<span data-ttu-id="0f4f6-114">Especifica o nome da rede virtual para mostrar os usos.</span><span class="sxs-lookup"><span data-stu-id="0f4f6-114">Specifies the name of the virtual network to show usages for.</span></span>

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

### <span data-ttu-id="0f4f6-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f4f6-115">-ResourceGroupName</span></span>
<span data-ttu-id="0f4f6-116">Especifica o nome do grupo de recursos ao qual a rede virtual pertence.</span><span class="sxs-lookup"><span data-stu-id="0f4f6-116">Specifies the name of the resource group that virtual network belongs to.</span></span>

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

### <span data-ttu-id="0f4f6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f4f6-117">CommonParameters</span></span>
<span data-ttu-id="0f4f6-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f4f6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f4f6-119">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0f4f6-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f4f6-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0f4f6-120">INPUTS</span></span>

### <span data-ttu-id="0f4f6-121">System. String</span><span class="sxs-lookup"><span data-stu-id="0f4f6-121">System.String</span></span>

## <span data-ttu-id="0f4f6-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0f4f6-122">OUTPUTS</span></span>

### <span data-ttu-id="0f4f6-123">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkUsage</span><span class="sxs-lookup"><span data-stu-id="0f4f6-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkUsage</span></span>

## <span data-ttu-id="0f4f6-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0f4f6-124">NOTES</span></span>

## <span data-ttu-id="0f4f6-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0f4f6-125">RELATED LINKS</span></span>
