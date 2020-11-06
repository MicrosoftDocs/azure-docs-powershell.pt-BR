---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: CBDF4BCB-7EB3-4D64-B19C-1314D4AB84E4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetwork.md
ms.openlocfilehash: d955cb51d92d9d0f3c156900d847e903d642e9af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431100"
---
# <span data-ttu-id="cecad-101">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cecad-101">Get-AzureRmVirtualNetwork</span></span>

## <span data-ttu-id="cecad-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cecad-102">SYNOPSIS</span></span>
<span data-ttu-id="cecad-103">Obtém uma rede virtual em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cecad-103">Gets a virtual network in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cecad-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cecad-104">SYNTAX</span></span>

### <span data-ttu-id="cecad-105">NOEXPAND</span><span class="sxs-lookup"><span data-stu-id="cecad-105">NoExpand</span></span>
```
Get-AzureRmVirtualNetwork [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cecad-106">Amplie</span><span class="sxs-lookup"><span data-stu-id="cecad-106">Expand</span></span>
```
Get-AzureRmVirtualNetwork -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cecad-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cecad-107">DESCRIPTION</span></span>
<span data-ttu-id="cecad-108">O cmdlet **Get-AzureRmVirtualNetwork** Obtém uma ou mais redes virtuais n um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="cecad-108">The **Get-AzureRmVirtualNetwork** cmdlet gets one or more virtual networks n a resource group.</span></span>

## <span data-ttu-id="cecad-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cecad-109">EXAMPLES</span></span>

### <span data-ttu-id="cecad-110">1: recuperar uma rede virtual</span><span class="sxs-lookup"><span data-stu-id="cecad-110">1: Retrieve a virtual network</span></span>
```
Get-AzureRmVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="cecad-111">Esse comando obtém a rede virtual chamada MyVirtualNetwork na TestResourceGroup do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="cecad-111">This command gets the virtual network named MyVirtualNetwork in the resource group TestResourceGroup</span></span>

## <span data-ttu-id="cecad-112">OS</span><span class="sxs-lookup"><span data-stu-id="cecad-112">PARAMETERS</span></span>

### <span data-ttu-id="cecad-113">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="cecad-113">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cecad-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="cecad-114">-Name</span></span>
<span data-ttu-id="cecad-115">Especifica o nome da rede virtual obtida por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cecad-115">Specifies the name of the virtual network that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cecad-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cecad-116">-ResourceGroupName</span></span>
<span data-ttu-id="cecad-117">Especifica o nome do grupo de recursos ao qual a rede virtual pertence.</span><span class="sxs-lookup"><span data-stu-id="cecad-117">Specifies the name of the resource group that virtual network belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpand
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Expand
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cecad-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cecad-118">-DefaultProfile</span></span>
<span data-ttu-id="cecad-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cecad-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cecad-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cecad-120">CommonParameters</span></span>
<span data-ttu-id="cecad-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cecad-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cecad-122">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cecad-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cecad-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cecad-123">INPUTS</span></span>

## <span data-ttu-id="cecad-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cecad-124">OUTPUTS</span></span>

### <span data-ttu-id="cecad-125">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cecad-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="cecad-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cecad-126">NOTES</span></span>

## <span data-ttu-id="cecad-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cecad-127">RELATED LINKS</span></span>

[<span data-ttu-id="cecad-128">New-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cecad-128">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="cecad-129">Remove-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cecad-129">Remove-AzureRmVirtualNetwork</span></span>](./Remove-AzureRmVirtualNetwork.md)

[<span data-ttu-id="cecad-130">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="cecad-130">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)


