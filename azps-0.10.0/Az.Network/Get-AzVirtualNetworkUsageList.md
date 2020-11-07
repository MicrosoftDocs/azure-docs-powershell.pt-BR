---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkusagelist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkUsageList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkUsageList.md
ms.openlocfilehash: 07c7d0e099cb5b83a0f98cfe8404be7e79b0427a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775461"
---
# <span data-ttu-id="fc5db-101">Get-AzVirtualNetworkUsageList</span><span class="sxs-lookup"><span data-stu-id="fc5db-101">Get-AzVirtualNetworkUsageList</span></span>

## <span data-ttu-id="fc5db-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fc5db-102">SYNOPSIS</span></span>
<span data-ttu-id="fc5db-103">Obtém o uso atual da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="fc5db-103">Gets virtual network current usage.</span></span>

## <span data-ttu-id="fc5db-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fc5db-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkUsageList -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc5db-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fc5db-105">DESCRIPTION</span></span>
<span data-ttu-id="fc5db-106">O cmdlet **Get-AzVirtualNetworkUsageList** tem uso por sub-rede para a rede virtual especificada.</span><span class="sxs-lookup"><span data-stu-id="fc5db-106">The **Get-AzVirtualNetworkUsageList** cmdlet gets per subnet usage for the specified virtual network.</span></span>

## <span data-ttu-id="fc5db-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fc5db-107">EXAMPLES</span></span>

### <span data-ttu-id="fc5db-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fc5db-108">Example 1</span></span>
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

<span data-ttu-id="fc5db-109">Obtém valores atuais de uso de sub-rede para a rede virtual usagetest.</span><span class="sxs-lookup"><span data-stu-id="fc5db-109">Gets per subnet current values of usage for usagetest virtual network.</span></span>

## <span data-ttu-id="fc5db-110">OS</span><span class="sxs-lookup"><span data-stu-id="fc5db-110">PARAMETERS</span></span>

### <span data-ttu-id="fc5db-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc5db-111">-DefaultProfile</span></span>
<span data-ttu-id="fc5db-112">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fc5db-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc5db-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="fc5db-113">-Name</span></span>
<span data-ttu-id="fc5db-114">Especifica o nome da rede virtual para mostrar os usos.</span><span class="sxs-lookup"><span data-stu-id="fc5db-114">Specifies the name of the virtual network to show usages for.</span></span>

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

### <span data-ttu-id="fc5db-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc5db-115">-ResourceGroupName</span></span>
<span data-ttu-id="fc5db-116">Especifica o nome do grupo de recursos ao qual a rede virtual pertence.</span><span class="sxs-lookup"><span data-stu-id="fc5db-116">Specifies the name of the resource group that virtual network belongs to.</span></span>

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

### <span data-ttu-id="fc5db-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc5db-117">CommonParameters</span></span>
<span data-ttu-id="fc5db-118">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc5db-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc5db-119">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc5db-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc5db-120">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fc5db-120">INPUTS</span></span>

### <span data-ttu-id="fc5db-121">System. String</span><span class="sxs-lookup"><span data-stu-id="fc5db-121">System.String</span></span>

## <span data-ttu-id="fc5db-122">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fc5db-122">OUTPUTS</span></span>

### <span data-ttu-id="fc5db-123">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkUsage</span><span class="sxs-lookup"><span data-stu-id="fc5db-123">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkUsage</span></span>

## <span data-ttu-id="fc5db-124">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fc5db-124">NOTES</span></span>

## <span data-ttu-id="fc5db-125">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fc5db-125">RELATED LINKS</span></span>

