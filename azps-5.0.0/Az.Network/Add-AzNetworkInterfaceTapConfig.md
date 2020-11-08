---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-aznetworkinterfacetapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceTapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzNetworkInterfaceTapConfig.md
ms.openlocfilehash: 1b51b7d086af738e356d7a6b65c17bdb45cbb518
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94118381"
---
# <span data-ttu-id="fb72e-101">Add-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="fb72e-101">Add-AzNetworkInterfaceTapConfig</span></span>

## <span data-ttu-id="fb72e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fb72e-102">SYNOPSIS</span></span>
<span data-ttu-id="fb72e-103">Cria um recurso TapConfiguration associado a uma NetworkInterface.</span><span class="sxs-lookup"><span data-stu-id="fb72e-103">Creates a TapConfiguration resource associated to a NetworkInterface.</span></span> <span data-ttu-id="fb72e-104">Isso fará referência a um recurso VirtualNetworkTap existente.</span><span class="sxs-lookup"><span data-stu-id="fb72e-104">This will reference to an existing VirtualNetworkTap resource.</span></span>

## <span data-ttu-id="fb72e-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fb72e-105">SYNTAX</span></span>

### <span data-ttu-id="fb72e-106">SetByResource (padrão)</span><span class="sxs-lookup"><span data-stu-id="fb72e-106">SetByResource (Default)</span></span>
```
Add-AzNetworkInterfaceTapConfig -NetworkInterface <PSNetworkInterface> -Name <String>
 [-VirtualNetworkTap <PSVirtualNetworkTap>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fb72e-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="fb72e-107">SetByResourceId</span></span>
```
Add-AzNetworkInterfaceTapConfig -NetworkInterface <PSNetworkInterface> -Name <String>
 [-VirtualNetworkTapId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fb72e-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fb72e-108">DESCRIPTION</span></span>
<span data-ttu-id="fb72e-109">O cmdlet **Add-AzNetworkInterfaceTapConfig** cria um recurso TapConfiguration associado a uma NetworkInterface.</span><span class="sxs-lookup"><span data-stu-id="fb72e-109">The **Add-AzNetworkInterfaceTapConfig** cmdlet creates a TapConfiguration resource associated to a NetworkInterface.</span></span> <span data-ttu-id="fb72e-110">Isso fará referência a um recurso VirtualNetworkTap existente.</span><span class="sxs-lookup"><span data-stu-id="fb72e-110">This will reference to an existing VirtualNetworkTap resource.</span></span>

## <span data-ttu-id="fb72e-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fb72e-111">EXAMPLES</span></span>

### <span data-ttu-id="fb72e-112">Exemplo 1: Adicionar TapConfiguration a uma determinada NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="fb72e-112">Example 1: Add TapConfiguration to a given NetworkInterface</span></span>
```
PS C:\>Add-AzNetworkInterfaceTapConfig -NetworkInterface $sourceNic -VirtualNetworkTap $vVirtualNetworkTap -Name 'myTapConfig'
```

<span data-ttu-id="fb72e-113">Adicione o TapConfiguration a um sourceNic.</span><span class="sxs-lookup"><span data-stu-id="fb72e-113">Add the TapConfiguration to a sourceNic.</span></span> <span data-ttu-id="fb72e-114">O tráfego da VM sourceNic será espelhado na VM de destino referenciada no recurso vVirtualNetworkTap.</span><span class="sxs-lookup"><span data-stu-id="fb72e-114">The traffic from sourceNic VM will be mirrored to destination VM referred in vVirtualNetworkTap resource.</span></span>

## <span data-ttu-id="fb72e-115">OS</span><span class="sxs-lookup"><span data-stu-id="fb72e-115">PARAMETERS</span></span>

### <span data-ttu-id="fb72e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb72e-116">-DefaultProfile</span></span>
<span data-ttu-id="fb72e-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fb72e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb72e-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="fb72e-118">-Name</span></span>
<span data-ttu-id="fb72e-119">Nome da configuração de toque.</span><span class="sxs-lookup"><span data-stu-id="fb72e-119">Name of the tap configuration.</span></span>

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

### <span data-ttu-id="fb72e-120">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="fb72e-120">-NetworkInterface</span></span>
<span data-ttu-id="fb72e-121">A referência do recurso de interface de rede.</span><span class="sxs-lookup"><span data-stu-id="fb72e-121">The reference of the network interface resource.</span></span>

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

### <span data-ttu-id="fb72e-122">-VirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="fb72e-122">-VirtualNetworkTap</span></span>
<span data-ttu-id="fb72e-123">A referência do recurso de toque na rede virtual.</span><span class="sxs-lookup"><span data-stu-id="fb72e-123">The reference of the virtual network tap resource.</span></span>

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

### <span data-ttu-id="fb72e-124">-VirtualNetworkTapId</span><span class="sxs-lookup"><span data-stu-id="fb72e-124">-VirtualNetworkTapId</span></span>
<span data-ttu-id="fb72e-125">A referência do recurso de toque na rede virtual.</span><span class="sxs-lookup"><span data-stu-id="fb72e-125">The reference of the virtual network tap resource.</span></span>

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

### <span data-ttu-id="fb72e-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fb72e-126">-Confirm</span></span>
<span data-ttu-id="fb72e-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fb72e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb72e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb72e-128">-WhatIf</span></span>
<span data-ttu-id="fb72e-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fb72e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb72e-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fb72e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb72e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb72e-131">CommonParameters</span></span>
<span data-ttu-id="fb72e-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb72e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb72e-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb72e-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb72e-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fb72e-134">INPUTS</span></span>

### <span data-ttu-id="fb72e-135">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="fb72e-135">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

### <span data-ttu-id="fb72e-136">System. String</span><span class="sxs-lookup"><span data-stu-id="fb72e-136">System.String</span></span>

### <span data-ttu-id="fb72e-137">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="fb72e-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="fb72e-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fb72e-138">OUTPUTS</span></span>

### <span data-ttu-id="fb72e-139">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="fb72e-139">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="fb72e-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fb72e-140">NOTES</span></span>

## <span data-ttu-id="fb72e-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fb72e-141">RELATED LINKS</span></span>

[<span data-ttu-id="fb72e-142">Get-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="fb72e-142">Get-AzNetworkInterfaceTapConfig</span></span>](./Get-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="fb72e-143">Remove-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="fb72e-143">Remove-AzNetworkInterfaceTapConfig</span></span>](./Remove-AzNetworkInterfaceTapConfig.md)

[<span data-ttu-id="fb72e-144">Set-AzNetworkInterfaceTapConfig</span><span class="sxs-lookup"><span data-stu-id="fb72e-144">Set-AzNetworkInterfaceTapConfig</span></span>](./Set-AzNetworkInterfaceTapConfig.md)
