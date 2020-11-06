---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: CBDF4BCB-7EB3-4D64-B19C-1314D4AB84E4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetwork.md
ms.openlocfilehash: 1745e3a87d91917e762c9b0e441110b4b6945601
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428171"
---
# <span data-ttu-id="15b41-101">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="15b41-101">Get-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="15b41-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="15b41-102">SYNOPSIS</span></span>
<span data-ttu-id="15b41-103">Obtém uma rede virtual em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="15b41-103">Gets a virtual network in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15b41-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="15b41-104">SYNTAX</span></span>

### <span data-ttu-id="15b41-105">NOEXPAND</span><span class="sxs-lookup"><span data-stu-id="15b41-105">NoExpand</span></span>
```
Get-AzureRmVirtualNetwork [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15b41-106">Amplie</span><span class="sxs-lookup"><span data-stu-id="15b41-106">Expand</span></span>
```
Get-AzureRmVirtualNetwork -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15b41-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="15b41-107">DESCRIPTION</span></span>
<span data-ttu-id="15b41-108">O cmdlet **Get-AzureRmVirtualNetwork** Obtém uma ou mais redes virtuais n um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="15b41-108">The **Get-AzureRmVirtualNetwork** cmdlet gets one or more virtual networks n a resource group.</span></span>

## <span data-ttu-id="15b41-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="15b41-109">EXAMPLES</span></span>

### <span data-ttu-id="15b41-110">1: recuperar uma rede virtual</span><span class="sxs-lookup"><span data-stu-id="15b41-110">1: Retrieve a virtual network</span></span>
```
Get-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="15b41-111">Esse comando obtém a rede virtual chamada MyVirtualNetwork na TestResourceGroup do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="15b41-111">This command gets the virtual network named MyVirtualNetwork in the resource group TestResourceGroup</span></span>

## <span data-ttu-id="15b41-112">OS</span><span class="sxs-lookup"><span data-stu-id="15b41-112">PARAMETERS</span></span>

### <span data-ttu-id="15b41-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15b41-113">-DefaultProfile</span></span>
<span data-ttu-id="15b41-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="15b41-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15b41-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="15b41-115">-ExpandResource</span></span>
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

### <span data-ttu-id="15b41-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="15b41-116">-Name</span></span>
<span data-ttu-id="15b41-117">Especifica o nome da rede virtual obtida por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15b41-117">Specifies the name of the virtual network that this cmdlet gets.</span></span>

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

### <span data-ttu-id="15b41-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15b41-118">-ResourceGroupName</span></span>
<span data-ttu-id="15b41-119">Especifica o nome do grupo de recursos ao qual a rede virtual pertence.</span><span class="sxs-lookup"><span data-stu-id="15b41-119">Specifies the name of the resource group that virtual network belongs to.</span></span>

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

### <span data-ttu-id="15b41-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15b41-120">CommonParameters</span></span>
<span data-ttu-id="15b41-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15b41-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15b41-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15b41-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15b41-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="15b41-123">INPUTS</span></span>

### <span data-ttu-id="15b41-124">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="15b41-124">None</span></span>
<span data-ttu-id="15b41-125">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="15b41-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="15b41-126">EXIBE</span><span class="sxs-lookup"><span data-stu-id="15b41-126">OUTPUTS</span></span>

### <span data-ttu-id="15b41-127">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="15b41-127">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="15b41-128">INFORMA</span><span class="sxs-lookup"><span data-stu-id="15b41-128">NOTES</span></span>

## <span data-ttu-id="15b41-129">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="15b41-129">RELATED LINKS</span></span>

[<span data-ttu-id="15b41-130">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="15b41-130">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="15b41-131">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="15b41-131">Remove-AzureRmVirtualNetwork</span></span>](./Remove-AzureRmVirtualNetwork.md)

[<span data-ttu-id="15b41-132">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="15b41-132">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)

