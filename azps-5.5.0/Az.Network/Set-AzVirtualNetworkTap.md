---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkTap.md
ms.openlocfilehash: 38995222182d120cd2067429d0f78798a9ebaaf8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114609"
---
# <span data-ttu-id="76051-101">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="76051-101">Set-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="76051-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="76051-102">SYNOPSIS</span></span>
<span data-ttu-id="76051-103">Atualiza um toque de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="76051-103">Updates a virtual network tap.</span></span>

## <span data-ttu-id="76051-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="76051-104">SYNTAX</span></span>

```
Set-AzVirtualNetworkTap -VirtualNetworkTap <PSVirtualNetworkTap> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76051-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="76051-105">DESCRIPTION</span></span>
<span data-ttu-id="76051-106">O cmdlet **Set-AzVirtualNetworkTap** atualiza um toque de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="76051-106">The **Set-AzVirtualNetworkTap** cmdlet updates a virtual network tap.</span></span>

## <span data-ttu-id="76051-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="76051-107">EXAMPLES</span></span>

### <span data-ttu-id="76051-108">Exemplo 1: Configurar um toque de rede Virtual</span><span class="sxs-lookup"><span data-stu-id="76051-108">Example 1: Configure a Virtual network tap</span></span>
```
PS C:\>$vTap = Get-AzVirtualNetworkTap -ResourceGroupName "ResourceGroup1" -Name "VirtualTap1"
PS C:\>$vTap.DestinationNetworkInterfaceIPConfiguration = $newDestinationNic.IpConfigurations[0]
PS C:\>Set-AzVirtualNetworkTap -VirtualNetworkTap $vTap
```

<span data-ttu-id="76051-109">O comando atualiza o IpConfiguration de Destino e atualiza o toque de rede Virtual.</span><span class="sxs-lookup"><span data-stu-id="76051-109">The command updates the Destination IpConfiguration and updates the Virtual network tap.</span></span>
<span data-ttu-id="76051-110">Se houver alguma configuração de toque fazendo referência a ela, todo o tráfego de origem não será espelhado para a nova atualização pós-atualização de configuração ip de destino.</span><span class="sxs-lookup"><span data-stu-id="76051-110">If there are any tap configurations referencing it, then all the source traffic will not start be mirrored to new destination ip configuration post update.</span></span>

## <span data-ttu-id="76051-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="76051-111">PARAMETERS</span></span>

### <span data-ttu-id="76051-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="76051-112">-AsJob</span></span>
<span data-ttu-id="76051-113">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="76051-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="76051-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76051-114">-DefaultProfile</span></span>
<span data-ttu-id="76051-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="76051-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76051-116">-VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="76051-116">-VirtualNetworkTap</span></span>
<span data-ttu-id="76051-117">Toque na rede virtual</span><span class="sxs-lookup"><span data-stu-id="76051-117">The virtual network tap</span></span>

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

### <span data-ttu-id="76051-118">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="76051-118">-Confirm</span></span>
<span data-ttu-id="76051-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76051-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76051-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76051-120">-WhatIf</span></span>
<span data-ttu-id="76051-121">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="76051-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76051-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="76051-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76051-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76051-123">CommonParameters</span></span>
<span data-ttu-id="76051-124">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76051-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76051-125">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76051-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76051-126">Entradas</span><span class="sxs-lookup"><span data-stu-id="76051-126">INPUTS</span></span>

### <span data-ttu-id="76051-127">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="76051-127">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="76051-128">Saídas</span><span class="sxs-lookup"><span data-stu-id="76051-128">OUTPUTS</span></span>

### <span data-ttu-id="76051-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="76051-129">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="76051-130">Notas</span><span class="sxs-lookup"><span data-stu-id="76051-130">NOTES</span></span>

## <span data-ttu-id="76051-131">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="76051-131">RELATED LINKS</span></span>

[<span data-ttu-id="76051-132">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="76051-132">Get-AzVirtualNetworkTap</span></span>](./Get-AzVirtualNetworkTap.md)

[<span data-ttu-id="76051-133">New-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="76051-133">New-AzVirtualNetworkTap</span></span>](./New-AzVirtualNetworkTap.md)

[<span data-ttu-id="76051-134">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="76051-134">Remove-AzVirtualNetworkTap</span></span>](./Remove-AzVirtualNetworkTap.md)
