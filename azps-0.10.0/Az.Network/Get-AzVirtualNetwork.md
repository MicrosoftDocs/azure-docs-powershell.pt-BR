---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: CBDF4BCB-7EB3-4D64-B19C-1314D4AB84E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetwork.md
ms.openlocfilehash: 97ae2607484828350be67cff9c9311fc73f19b6f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93775483"
---
# <span data-ttu-id="f797e-101">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f797e-101">Get-AzVirtualNetwork</span></span>

## <span data-ttu-id="f797e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f797e-102">SYNOPSIS</span></span>
<span data-ttu-id="f797e-103">Obtém uma rede virtual em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f797e-103">Gets a virtual network in a resource group.</span></span>

## <span data-ttu-id="f797e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f797e-104">SYNTAX</span></span>

### <span data-ttu-id="f797e-105">NOEXPAND</span><span class="sxs-lookup"><span data-stu-id="f797e-105">NoExpand</span></span>
```
Get-AzVirtualNetwork [-Name <String>] [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f797e-106">Amplie</span><span class="sxs-lookup"><span data-stu-id="f797e-106">Expand</span></span>
```
Get-AzVirtualNetwork -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f797e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f797e-107">DESCRIPTION</span></span>
<span data-ttu-id="f797e-108">O cmdlet **Get-AzVirtualNetwork** Obtém uma ou mais redes virtuais n um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="f797e-108">The **Get-AzVirtualNetwork** cmdlet gets one or more virtual networks n a resource group.</span></span>

## <span data-ttu-id="f797e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f797e-109">EXAMPLES</span></span>

### <span data-ttu-id="f797e-110">1: recuperar uma rede virtual</span><span class="sxs-lookup"><span data-stu-id="f797e-110">1: Retrieve a virtual network</span></span>
```
Get-AzVirtualNetwork -Name MyVirtualNetwork -ResourceGroupName TestResourceGroup
```

<span data-ttu-id="f797e-111">Esse comando obtém a rede virtual chamada MyVirtualNetwork na TestResourceGroup do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="f797e-111">This command gets the virtual network named MyVirtualNetwork in the resource group TestResourceGroup</span></span>

## <span data-ttu-id="f797e-112">OS</span><span class="sxs-lookup"><span data-stu-id="f797e-112">PARAMETERS</span></span>

### <span data-ttu-id="f797e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f797e-113">-DefaultProfile</span></span>
<span data-ttu-id="f797e-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f797e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f797e-115">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="f797e-115">-ExpandResource</span></span>
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

### <span data-ttu-id="f797e-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="f797e-116">-Name</span></span>
<span data-ttu-id="f797e-117">Especifica o nome da rede virtual obtida por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f797e-117">Specifies the name of the virtual network that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f797e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f797e-118">-ResourceGroupName</span></span>
<span data-ttu-id="f797e-119">Especifica o nome do grupo de recursos ao qual a rede virtual pertence.</span><span class="sxs-lookup"><span data-stu-id="f797e-119">Specifies the name of the resource group that virtual network belongs to.</span></span>

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

### <span data-ttu-id="f797e-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f797e-120">CommonParameters</span></span>
<span data-ttu-id="f797e-121">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f797e-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f797e-122">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f797e-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f797e-123">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f797e-123">INPUTS</span></span>

## <span data-ttu-id="f797e-124">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f797e-124">OUTPUTS</span></span>

### <span data-ttu-id="f797e-125">Microsoft. Azure. Commands. Network. Models. PSVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f797e-125">Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork</span></span>

## <span data-ttu-id="f797e-126">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f797e-126">NOTES</span></span>

## <span data-ttu-id="f797e-127">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f797e-127">RELATED LINKS</span></span>

[<span data-ttu-id="f797e-128">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f797e-128">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="f797e-129">Remove-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f797e-129">Remove-AzVirtualNetwork</span></span>](./Remove-AzVirtualNetwork.md)

[<span data-ttu-id="f797e-130">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f797e-130">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)


