---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkTap.md
ms.openlocfilehash: 22d2396e4471e2321ff9e532d4361909baa67163
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885388"
---
# <span data-ttu-id="e3a1b-101">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="e3a1b-101">Set-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="e3a1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3a1b-102">SYNOPSIS</span></span>
<span data-ttu-id="e3a1b-103">Atualiza um toque de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="e3a1b-103">Updates a virtual network tap.</span></span>

## <span data-ttu-id="e3a1b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e3a1b-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkTap -VirtualNetworkTap <PSVirtualNetworkTap> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3a1b-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e3a1b-105">DESCRIPTION</span></span>
<span data-ttu-id="e3a1b-106">O cmdlet **Set-AzVirtualNetworkTap** atualiza um toque de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="e3a1b-106">The **Set-AzVirtualNetworkTap** cmdlet updates a virtual network tap.</span></span>

## <span data-ttu-id="e3a1b-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e3a1b-107">EXAMPLES</span></span>

### <span data-ttu-id="e3a1b-108">Exemplo 1: Configurar um toque de rede virtual</span><span class="sxs-lookup"><span data-stu-id="e3a1b-108">Example 1: Configure a Virtual network tap</span></span>
```
PS C:\>$vTap = Get-AzVirtualNetworkTap -ResourceGroupName "ResourceGroup1" -Name "VirtualTap1"
PS C:\>$vTap.DestinationNetworkInterfaceIPConfiguration = $newDestinationNic.IpConfigurations[0]
PS C:\>Set-AzVirtualNetworkTap -VirtualNetworkTap $vTap
```

<span data-ttu-id="e3a1b-109">O comando atualiza o IpConfiguration de Destino e atualiza o toque de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="e3a1b-109">The command updates the Destination IpConfiguration and updates the Virtual network tap.</span></span>
<span data-ttu-id="e3a1b-110">Se houver configurações de toque fazendo referência a ela, todo o tráfego de origem não será espelhado para a nova atualização pós-atualização de configuração ip de destino.</span><span class="sxs-lookup"><span data-stu-id="e3a1b-110">If there are any tap configurations referencing it, then all the source traffic will not start be mirrored to new destination ip configuration post update.</span></span>

## <span data-ttu-id="e3a1b-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e3a1b-111">PARAMETERS</span></span>

### <span data-ttu-id="e3a1b-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e3a1b-112">-AsJob</span></span>
<span data-ttu-id="e3a1b-113">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="e3a1b-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e3a1b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3a1b-114">-DefaultProfile</span></span>
<span data-ttu-id="e3a1b-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e3a1b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3a1b-116">-VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="e3a1b-116">-VirtualNetworkTap</span></span>
<span data-ttu-id="e3a1b-117">O toque de rede virtual</span><span class="sxs-lookup"><span data-stu-id="e3a1b-117">The virtual network tap</span></span>

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

### <span data-ttu-id="e3a1b-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e3a1b-118">-Confirm</span></span>
<span data-ttu-id="e3a1b-119">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3a1b-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3a1b-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3a1b-120">-WhatIf</span></span>
<span data-ttu-id="e3a1b-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e3a1b-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3a1b-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e3a1b-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3a1b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3a1b-123">CommonParameters</span></span>
<span data-ttu-id="e3a1b-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3a1b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3a1b-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3a1b-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3a1b-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e3a1b-126">INPUTS</span></span>

### <span data-ttu-id="e3a1b-127">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="e3a1b-127">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="e3a1b-128">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e3a1b-128">OUTPUTS</span></span>

### <span data-ttu-id="e3a1b-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="e3a1b-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="e3a1b-130">NOTES</span><span class="sxs-lookup"><span data-stu-id="e3a1b-130">NOTES</span></span>

## <span data-ttu-id="e3a1b-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e3a1b-131">RELATED LINKS</span></span>

[<span data-ttu-id="e3a1b-132">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="e3a1b-132">Get-AzVirtualNetworkTap</span></span>](./Get-AzVirtualNetworkTap.md)

[<span data-ttu-id="e3a1b-133">New-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="e3a1b-133">New-AzVirtualNetworkTap</span></span>](./New-AzVirtualNetworkTap.md)

[<span data-ttu-id="e3a1b-134">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="e3a1b-134">Remove-AzVirtualNetworkTap</span></span>](./Remove-AzVirtualNetworkTap.md)
