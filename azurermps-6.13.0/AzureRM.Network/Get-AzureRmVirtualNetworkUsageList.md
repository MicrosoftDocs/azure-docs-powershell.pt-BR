---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkusagelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkUsageList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkUsageList.md
ms.openlocfilehash: 855385b55922f6255b407ceafef7422113968516
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429497"
---
# <span data-ttu-id="f6820-101">Get-AzureRmVirtualNetworkUsageList</span><span class="sxs-lookup"><span data-stu-id="f6820-101">Get-AzureRmVirtualNetworkUsageList</span></span>

## <span data-ttu-id="f6820-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f6820-102">SYNOPSIS</span></span>
<span data-ttu-id="f6820-103">Obtém o uso atual da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="f6820-103">Gets virtual network current usage.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6820-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f6820-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkUsageList -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6820-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f6820-105">DESCRIPTION</span></span>
<span data-ttu-id="f6820-106">O cmdlet **Get-AzureRmVirtualNetworkUsageList** tem uso por sub-rede para a rede virtual especificada.</span><span class="sxs-lookup"><span data-stu-id="f6820-106">The **Get-AzureRmVirtualNetworkUsageList** cmdlet gets per subnet usage for the specified virtual network.</span></span>

## <span data-ttu-id="f6820-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f6820-107">EXAMPLES</span></span>

### <span data-ttu-id="f6820-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f6820-108">Example 1</span></span>
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

<span data-ttu-id="f6820-109">Obtém valores atuais de uso de sub-rede para a rede virtual usagetest.</span><span class="sxs-lookup"><span data-stu-id="f6820-109">Gets per subnet current values of usage for usagetest virtual network.</span></span>

## <span data-ttu-id="f6820-110">OS</span><span class="sxs-lookup"><span data-stu-id="f6820-110">PARAMETERS</span></span>

### <span data-ttu-id="f6820-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6820-111">-DefaultProfile</span></span>
<span data-ttu-id="f6820-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f6820-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6820-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="f6820-113">-Name</span></span>
<span data-ttu-id="f6820-114">Especifica o nome da rede virtual para mostrar os usos.</span><span class="sxs-lookup"><span data-stu-id="f6820-114">Specifies the name of the virtual network to show usages for.</span></span>

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

### <span data-ttu-id="f6820-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6820-115">-ResourceGroupName</span></span>
<span data-ttu-id="f6820-116">Especifica o nome do grupo de recursos ao qual a rede virtual pertence.</span><span class="sxs-lookup"><span data-stu-id="f6820-116">Specifies the name of the resource group that virtual network belongs to.</span></span>

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

### <span data-ttu-id="f6820-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6820-117">CommonParameters</span></span>
<span data-ttu-id="f6820-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6820-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6820-119">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6820-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6820-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f6820-120">INPUTS</span></span>

### <span data-ttu-id="f6820-121">System. String</span><span class="sxs-lookup"><span data-stu-id="f6820-121">System.String</span></span>

## <span data-ttu-id="f6820-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f6820-122">OUTPUTS</span></span>

### <span data-ttu-id="f6820-123">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkUsage</span><span class="sxs-lookup"><span data-stu-id="f6820-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkUsage</span></span>

## <span data-ttu-id="f6820-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f6820-124">NOTES</span></span>

## <span data-ttu-id="f6820-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f6820-125">RELATED LINKS</span></span>
