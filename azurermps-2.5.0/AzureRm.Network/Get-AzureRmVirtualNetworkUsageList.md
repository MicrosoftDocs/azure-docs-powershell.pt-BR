---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkusagelist
schema: 2.0.0
ms.openlocfilehash: 61717f314629259caca9329c2ef1a458aa9a0e0f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785178"
---
# <span data-ttu-id="a31ca-101">Get-AzureRmVirtualNetworkUsageList</span><span class="sxs-lookup"><span data-stu-id="a31ca-101">Get-AzureRmVirtualNetworkUsageList</span></span>

## <span data-ttu-id="a31ca-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a31ca-102">SYNOPSIS</span></span>
<span data-ttu-id="a31ca-103">Obtém o uso atual da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="a31ca-103">Gets virtual network current usage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a31ca-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a31ca-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkUsageList -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a31ca-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a31ca-105">DESCRIPTION</span></span>
<span data-ttu-id="a31ca-106">O cmdlet **Get-AzureRmVirtualNetworkUsageList** tem uso por sub-rede para a rede virtual especificada.</span><span class="sxs-lookup"><span data-stu-id="a31ca-106">The **Get-AzureRmVirtualNetworkUsageList** cmdlet gets per subnet usage for the specified virtual network.</span></span>

## <span data-ttu-id="a31ca-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a31ca-107">EXAMPLES</span></span>

### <span data-ttu-id="a31ca-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a31ca-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkUsageList -ResourceGroupName test -Name usagetest

Get-AzureRmVirtualNetworkUsageList -ResourceGroupName test -Name usagetest

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

<span data-ttu-id="a31ca-109">Obtém valores atuais de uso de sub-rede para a rede virtual usagetest.</span><span class="sxs-lookup"><span data-stu-id="a31ca-109">Gets per subnet current values of usage for usagetest virtual network.</span></span>

## <span data-ttu-id="a31ca-110">OS</span><span class="sxs-lookup"><span data-stu-id="a31ca-110">PARAMETERS</span></span>

### <span data-ttu-id="a31ca-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a31ca-111">-DefaultProfile</span></span>
<span data-ttu-id="a31ca-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a31ca-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a31ca-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="a31ca-113">-Name</span></span>
<span data-ttu-id="a31ca-114">Especifica o nome da rede virtual para mostrar os usos.</span><span class="sxs-lookup"><span data-stu-id="a31ca-114">Specifies the name of the virtual network to show usages for.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a31ca-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a31ca-115">-ResourceGroupName</span></span>
<span data-ttu-id="a31ca-116">Especifica o nome do grupo de recursos ao qual a rede virtual pertence.</span><span class="sxs-lookup"><span data-stu-id="a31ca-116">Specifies the name of the resource group that virtual network belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a31ca-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a31ca-117">CommonParameters</span></span>
<span data-ttu-id="a31ca-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a31ca-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a31ca-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a31ca-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a31ca-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a31ca-120">INPUTS</span></span>

### <span data-ttu-id="a31ca-121">System. String</span><span class="sxs-lookup"><span data-stu-id="a31ca-121">System.String</span></span>

## <span data-ttu-id="a31ca-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a31ca-122">OUTPUTS</span></span>

### <span data-ttu-id="a31ca-123">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkUsage</span><span class="sxs-lookup"><span data-stu-id="a31ca-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkUsage</span></span>

## <span data-ttu-id="a31ca-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a31ca-124">NOTES</span></span>

## <span data-ttu-id="a31ca-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a31ca-125">RELATED LINKS</span></span>

