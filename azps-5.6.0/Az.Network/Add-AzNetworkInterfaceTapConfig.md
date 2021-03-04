---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: 2da755a4ac3044c6499faee82a74e2c9ec7d9f6e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889192"
---
# <span data-ttu-id="ffd59-101">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="ffd59-101">Add-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="ffd59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ffd59-102">SYNOPSIS</span></span>
<span data-ttu-id="ffd59-103">Cria um recurso TapConfiguration associado a um NetworkInterface.</span><span class="sxs-lookup"><span data-stu-id="ffd59-103">Creates a TapConfiguration resource associated to a NetworkInterface.</span></span> <span data-ttu-id="ffd59-104">Isso fará referência a um recurso VirtualNetworkTap existente.</span><span class="sxs-lookup"><span data-stu-id="ffd59-104">This will reference to an existing VirtualNetworkTap resource.</span></span>

## <span data-ttu-id="ffd59-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ffd59-105">SYNTAX</span></span>

### <span data-ttu-id="ffd59-106">SetByResource (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ffd59-106">SetByResource (Default)</span></span>
```
Add-AzNetworkInterfaceTapConfig -NetworkInterface <PSNetworkInterface> -Name <String>
 [-VirtualNetworkTap <PSVirtualNetworkTap>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ffd59-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="ffd59-107">SetByResourceId</span></span>
```
Add-AzNetworkInterfaceTapConfig -NetworkInterface <PSNetworkInterface> -Name <String>
 [-VirtualNetworkTapId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ffd59-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ffd59-108">DESCRIPTION</span></span>
<span data-ttu-id="ffd59-109">O cmdlet **Add-AzNetworkInterfaceTapConfig** cria um recurso TapConfiguration associado a um NetworkInterface.</span><span class="sxs-lookup"><span data-stu-id="ffd59-109">The **Add-AzNetworkInterfaceTapConfig** cmdlet creates a TapConfiguration resource associated to a NetworkInterface.</span></span> <span data-ttu-id="ffd59-110">Isso fará referência a um recurso VirtualNetworkTap existente.</span><span class="sxs-lookup"><span data-stu-id="ffd59-110">This will reference to an existing VirtualNetworkTap resource.</span></span>

## <span data-ttu-id="ffd59-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ffd59-111">EXAMPLES</span></span>

### <span data-ttu-id="ffd59-112">Exemplo 1: Adicionar TapConfiguration a um determinado NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="ffd59-112">Example 1: Add TapConfiguration to a given NetworkInterface</span></span>
```
PS C:\>Add-AzNetworkInterfaceTapConfig -NetworkInterface $sourceNic -VirtualNetworkTap $vVirtualNetworkTap -Name 'myTapConfig'
```

<span data-ttu-id="ffd59-113">Adicione o TapConfiguration a um sourceNic.</span><span class="sxs-lookup"><span data-stu-id="ffd59-113">Add the TapConfiguration to a sourceNic.</span></span> <span data-ttu-id="ffd59-114">O tráfego da VM sourceNic será espelhado para a VM de destino referida no recurso vVirtualNetworkTap.</span><span class="sxs-lookup"><span data-stu-id="ffd59-114">The traffic from sourceNic VM will be mirrored to destination VM referred in vVirtualNetworkTap resource.</span></span>

## <span data-ttu-id="ffd59-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ffd59-115">PARAMETERS</span></span>

### <span data-ttu-id="ffd59-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffd59-116">-DefaultProfile</span></span>
<span data-ttu-id="ffd59-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ffd59-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ffd59-118">-Name</span><span class="sxs-lookup"><span data-stu-id="ffd59-118">-Name</span></span>
<span data-ttu-id="ffd59-119">Nome da configuração do toque.</span><span class="sxs-lookup"><span data-stu-id="ffd59-119">Name of the tap configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffd59-120">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="ffd59-120">-NetworkInterface</span></span>
<span data-ttu-id="ffd59-121">A referência do recurso de interface de rede.</span><span class="sxs-lookup"><span data-stu-id="ffd59-121">The reference of the network interface resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterface
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ffd59-122">-VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="ffd59-122">-VirtualNetworkTap</span></span>
<span data-ttu-id="ffd59-123">A referência do recurso de toque de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="ffd59-123">The reference of the virtual network tap resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffd59-124">-VirtualNetworkTapId</span><span class="sxs-lookup"><span data-stu-id="ffd59-124">-VirtualNetworkTapId</span></span>
<span data-ttu-id="ffd59-125">A referência do recurso de toque de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="ffd59-125">The reference of the virtual network tap resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffd59-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ffd59-126">-Confirm</span></span>
<span data-ttu-id="ffd59-127">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ffd59-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffd59-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffd59-128">-WhatIf</span></span>
<span data-ttu-id="ffd59-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ffd59-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ffd59-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ffd59-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffd59-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffd59-131">CommonParameters</span></span>
<span data-ttu-id="ffd59-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffd59-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffd59-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffd59-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffd59-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ffd59-134">INPUTS</span></span>

### <span data-ttu-id="ffd59-135">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="ffd59-135">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

### <span data-ttu-id="ffd59-136">System.String</span><span class="sxs-lookup"><span data-stu-id="ffd59-136">System.String</span></span>

### <span data-ttu-id="ffd59-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="ffd59-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="ffd59-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ffd59-138">OUTPUTS</span></span>

### <span data-ttu-id="ffd59-139">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="ffd59-139">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="ffd59-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="ffd59-140">NOTES</span></span>

## <span data-ttu-id="ffd59-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ffd59-141">RELATED LINKS</span></span>

[<span data-ttu-id="ffd59-142">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="ffd59-142">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="ffd59-143">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="ffd59-143">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="ffd59-144">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="ffd59-144">Set-AzNetworkInterfaceTapConfig</span></span>](./Set-AzNetworkInterfaceTapConfig.md)
