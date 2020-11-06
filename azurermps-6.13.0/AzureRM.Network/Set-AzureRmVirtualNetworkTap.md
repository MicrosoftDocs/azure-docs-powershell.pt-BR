---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkTap.md
ms.openlocfilehash: 1d767677c547c2418ca19e3206f3ca5a25638de0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440742"
---
# <span data-ttu-id="688cb-101">Set-AzureRmVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="688cb-101">Set-AzureRmVirtualNetworkTap</span></span>

## <span data-ttu-id="688cb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="688cb-102">SYNOPSIS</span></span>
<span data-ttu-id="688cb-103">Define o estado da meta para uma rede virtual, toque em.</span><span class="sxs-lookup"><span data-stu-id="688cb-103">Sets the goal state for a virtual network tap.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="688cb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="688cb-104">SYNTAX</span></span>

```
Set-AzureRmVirtualNetworkTap -VirtualNetworkTap <PSVirtualNetworkTap> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="688cb-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="688cb-105">DESCRIPTION</span></span>
<span data-ttu-id="688cb-106">O **set-AzureRmVirtualNetworkTap** define o estado da meta para um toque de rede virtual do Azure.</span><span class="sxs-lookup"><span data-stu-id="688cb-106">The **Set-AzureRmVirtualNetworkTap** sets the goal state for an Azure virtual network tap.</span></span>

## <span data-ttu-id="688cb-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="688cb-107">EXAMPLES</span></span>

### <span data-ttu-id="688cb-108">Exemplo 1: configurar um toque de rede virtual</span><span class="sxs-lookup"><span data-stu-id="688cb-108">Example 1: Configure a Virtual network tap</span></span>
```
PS C:\>$vTap = Get-AzureRmVirtualNetworkTap -ResourceGroupName "ResourceGroup1" -Name "VirtualTap1"
PS C:\>$vTap.DestinationNetworkInterfaceIPConfiguration = $newDestinationNic.IpConfigurations[0]
PS C:\>Set-AzureRmVirtualNetworkTap -VirtualNetworkTap $vTap
```

<span data-ttu-id="688cb-109">O comando atualiza a IpConfiguration de destino e atualiza o toque da rede virtual.</span><span class="sxs-lookup"><span data-stu-id="688cb-109">The command updates the Destination IpConfiguration and updates the Virtual network tap.</span></span>
<span data-ttu-id="688cb-110">Se houver qualquer toque de configuração que faz referência a ele, todo o tráfego de origem não será iniciado para a nova postagem de configuração de IP de destino.</span><span class="sxs-lookup"><span data-stu-id="688cb-110">If there are any tap configurations referencing it, then all the source traffic will not start be mirrored to new destination ip configuration post update.</span></span>

## <span data-ttu-id="688cb-111">OS</span><span class="sxs-lookup"><span data-stu-id="688cb-111">PARAMETERS</span></span>

### <span data-ttu-id="688cb-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="688cb-112">-AsJob</span></span>
<span data-ttu-id="688cb-113">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="688cb-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="688cb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="688cb-114">-DefaultProfile</span></span>
<span data-ttu-id="688cb-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="688cb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="688cb-116">-VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="688cb-116">-VirtualNetworkTap</span></span>
<span data-ttu-id="688cb-117">O toque da rede virtual</span><span class="sxs-lookup"><span data-stu-id="688cb-117">The virtual network tap</span></span>

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

### <span data-ttu-id="688cb-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="688cb-118">-Confirm</span></span>
<span data-ttu-id="688cb-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="688cb-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="688cb-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="688cb-120">-WhatIf</span></span>
<span data-ttu-id="688cb-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="688cb-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="688cb-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="688cb-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="688cb-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="688cb-123">CommonParameters</span></span>
<span data-ttu-id="688cb-124">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="688cb-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="688cb-125">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="688cb-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="688cb-126">SENSORES</span><span class="sxs-lookup"><span data-stu-id="688cb-126">INPUTS</span></span>

### <span data-ttu-id="688cb-127">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="688cb-127">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="688cb-128">EXIBE</span><span class="sxs-lookup"><span data-stu-id="688cb-128">OUTPUTS</span></span>

### <span data-ttu-id="688cb-129">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="688cb-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="688cb-130">INFORMA</span><span class="sxs-lookup"><span data-stu-id="688cb-130">NOTES</span></span>

## <span data-ttu-id="688cb-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="688cb-131">RELATED LINKS</span></span>
