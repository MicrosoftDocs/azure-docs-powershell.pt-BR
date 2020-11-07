---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkTap.md
ms.openlocfilehash: 38995222182d120cd2067429d0f78798a9ebaaf8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940652"
---
# <span data-ttu-id="395b7-101">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="395b7-101">Set-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="395b7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="395b7-102">SYNOPSIS</span></span>
<span data-ttu-id="395b7-103">Atualiza uma rede virtual, toque em.</span><span class="sxs-lookup"><span data-stu-id="395b7-103">Updates a virtual network tap.</span></span>

## <span data-ttu-id="395b7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="395b7-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkTap -VirtualNetworkTap <PSVirtualNetworkTap> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="395b7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="395b7-105">DESCRIPTION</span></span>
<span data-ttu-id="395b7-106">O cmdlet **set-AzVirtualNetworkTap** atualiza um toque de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="395b7-106">The **Set-AzVirtualNetworkTap** cmdlet updates a virtual network tap.</span></span>

## <span data-ttu-id="395b7-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="395b7-107">EXAMPLES</span></span>

### <span data-ttu-id="395b7-108">Exemplo 1: configurar um toque de rede virtual</span><span class="sxs-lookup"><span data-stu-id="395b7-108">Example 1: Configure a Virtual network tap</span></span>
```
PS C:\>$vTap = Get-AzVirtualNetworkTap -ResourceGroupName "ResourceGroup1" -Name "VirtualTap1"
PS C:\>$vTap.DestinationNetworkInterfaceIPConfiguration = $newDestinationNic.IpConfigurations[0]
PS C:\>Set-AzVirtualNetworkTap -VirtualNetworkTap $vTap
```

<span data-ttu-id="395b7-109">O comando atualiza a IpConfiguration de destino e atualiza o toque da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="395b7-109">The command updates the Destination IpConfiguration and updates the Virtual network tap.</span></span>
<span data-ttu-id="395b7-110">Se houver qualquer toque de configuração que faz referência a ele, todo o tráfego de origem não será iniciado para a nova postagem de configuração de IP de destino.</span><span class="sxs-lookup"><span data-stu-id="395b7-110">If there are any tap configurations referencing it, then all the source traffic will not start be mirrored to new destination ip configuration post update.</span></span>

## <span data-ttu-id="395b7-111">OS</span><span class="sxs-lookup"><span data-stu-id="395b7-111">PARAMETERS</span></span>

### <span data-ttu-id="395b7-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="395b7-112">-AsJob</span></span>
<span data-ttu-id="395b7-113">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="395b7-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="395b7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="395b7-114">-DefaultProfile</span></span>
<span data-ttu-id="395b7-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="395b7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="395b7-116">-VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="395b7-116">-VirtualNetworkTap</span></span>
<span data-ttu-id="395b7-117">O toque da rede virtual</span><span class="sxs-lookup"><span data-stu-id="395b7-117">The virtual network tap</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="395b7-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="395b7-118">-Confirm</span></span>
<span data-ttu-id="395b7-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="395b7-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="395b7-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="395b7-120">-WhatIf</span></span>
<span data-ttu-id="395b7-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="395b7-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="395b7-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="395b7-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="395b7-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="395b7-123">CommonParameters</span></span>
<span data-ttu-id="395b7-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="395b7-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="395b7-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="395b7-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="395b7-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="395b7-126">INPUTS</span></span>

### <span data-ttu-id="395b7-127">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="395b7-127">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="395b7-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="395b7-128">OUTPUTS</span></span>

### <span data-ttu-id="395b7-129">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="395b7-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="395b7-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="395b7-130">NOTES</span></span>

## <span data-ttu-id="395b7-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="395b7-131">RELATED LINKS</span></span>

[<span data-ttu-id="395b7-132">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="395b7-132">Get-AzVirtualNetworkTap</span></span>](./Get-AzVirtualNetworkTap.md)

[<span data-ttu-id="395b7-133">New-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="395b7-133">New-AzVirtualNetworkTap</span></span>](./New-AzVirtualNetworkTap.md)

[<span data-ttu-id="395b7-134">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="395b7-134">Remove-AzVirtualNetworkTap</span></span>](./Remove-AzVirtualNetworkTap.md)
