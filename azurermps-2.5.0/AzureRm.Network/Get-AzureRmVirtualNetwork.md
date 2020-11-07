---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: CBDF4BCB-7EB3-4D64-B19C-1314D4AB84E4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetwork
schema: 2.0.0
ms.openlocfilehash: 983c23111486a964275a7efb85031b013fb365d2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786306"
---
# <span data-ttu-id="c365e-101">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c365e-101">Get-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="c365e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c365e-102">SYNOPSIS</span></span>
<span data-ttu-id="c365e-103">Obtém uma rede virtual em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c365e-103">Gets a virtual network in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c365e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c365e-104">SYNTAX</span></span>

### <span data-ttu-id="c365e-105">NOEXPAND</span><span class="sxs-lookup"><span data-stu-id="c365e-105">NoExpand</span></span>
```
Get-AzureRmVirtualNetwork [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c365e-106">Amplie</span><span class="sxs-lookup"><span data-stu-id="c365e-106">Expand</span></span>
```
Get-AzureRmVirtualNetwork -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c365e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c365e-107">DESCRIPTION</span></span>
<span data-ttu-id="c365e-108">O cmdlet **Get-AzureRmVirtualNetwork** Obtém uma ou mais redes virtuais n um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c365e-108">The **Get-AzureRmVirtualNetwork** cmdlet gets one or more virtual networks n a resource group.</span></span>

## <span data-ttu-id="c365e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c365e-109">EXAMPLES</span></span>

### <span data-ttu-id="c365e-110">1: recuperar uma rede virtual</span><span class="sxs-lookup"><span data-stu-id="c365e-110">1: Retrieve a virtual network</span></span>
```
Get-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="c365e-111">Esse comando obtém a rede virtual chamada MyVirtualNetwork na TestResourceGroup do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="c365e-111">This command gets the virtual network named MyVirtualNetwork in the resource group TestResourceGroup</span></span>

## <span data-ttu-id="c365e-112">OS</span><span class="sxs-lookup"><span data-stu-id="c365e-112">PARAMETERS</span></span>

### <span data-ttu-id="c365e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c365e-113">-DefaultProfile</span></span>
<span data-ttu-id="c365e-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c365e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c365e-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="c365e-115">-ExpandResource</span></span>
```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c365e-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="c365e-116">-Name</span></span>
<span data-ttu-id="c365e-117">Especifica o nome da rede virtual obtida por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c365e-117">Specifies the name of the virtual network that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c365e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c365e-118">-ResourceGroupName</span></span>
<span data-ttu-id="c365e-119">Especifica o nome do grupo de recursos ao qual a rede virtual pertence.</span><span class="sxs-lookup"><span data-stu-id="c365e-119">Specifies the name of the resource group that virtual network belongs to.</span></span>

```yaml
Type: String
Parameter Sets: NoExpand
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c365e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c365e-120">CommonParameters</span></span>
<span data-ttu-id="c365e-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c365e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c365e-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c365e-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c365e-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c365e-123">INPUTS</span></span>

## <span data-ttu-id="c365e-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c365e-124">OUTPUTS</span></span>

### <span data-ttu-id="c365e-125">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c365e-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="c365e-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c365e-126">NOTES</span></span>

## <span data-ttu-id="c365e-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c365e-127">RELATED LINKS</span></span>

[<span data-ttu-id="c365e-128">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c365e-128">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="c365e-129">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c365e-129">Remove-AzureRmVirtualNetwork</span></span>](./Remove-AzureRmVirtualNetwork.md)

[<span data-ttu-id="c365e-130">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c365e-130">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)


