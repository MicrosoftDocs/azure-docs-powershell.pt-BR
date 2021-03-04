---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/add-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualRouterPeer.md
ms.openlocfilehash: 87647d504d47bf3f53b775d68b42ab617485f73d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888851"
---
# <span data-ttu-id="483ca-101">Add-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="483ca-101">Add-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="483ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="483ca-102">SYNOPSIS</span></span>
<span data-ttu-id="483ca-103">Adicionar um Par a um Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="483ca-103">Add a Peer to an Azure VirtualRouter</span></span>

## <span data-ttu-id="483ca-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="483ca-104">SYNTAX</span></span>

```
Add-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 -VirtualRouterName <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="483ca-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="483ca-105">DESCRIPTION</span></span>
<span data-ttu-id="483ca-106">O cmdlet **Add-AzVirtualRouterPeer** adiciona um Par virtualRouter a um Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="483ca-106">The **Add-AzVirtualRouterPeer** cmdlet adds a VirtualRouter Peer to an Azure VirtualRouter</span></span>

## <span data-ttu-id="483ca-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="483ca-107">EXAMPLES</span></span>

### <span data-ttu-id="483ca-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="483ca-108">Example 1</span></span>
```powershell
Add-AzVirtualRouterPeer 1ResourceGroupName virtualRouterRG -PeerName csr -PeerIp 10.0.1.5 -PeerAsn 63000  -VirtualRouterName virtualRouter
```

## <span data-ttu-id="483ca-109">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="483ca-109">PARAMETERS</span></span>

### <span data-ttu-id="483ca-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="483ca-110">-AsJob</span></span>
<span data-ttu-id="483ca-111">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="483ca-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="483ca-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="483ca-112">-DefaultProfile</span></span>
<span data-ttu-id="483ca-113">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="483ca-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="483ca-114">-Force</span><span class="sxs-lookup"><span data-stu-id="483ca-114">-Force</span></span>
<span data-ttu-id="483ca-115">Não peça confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="483ca-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="483ca-116">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="483ca-116">-PeerAsn</span></span>
<span data-ttu-id="483ca-117">Peer ASN.</span><span class="sxs-lookup"><span data-stu-id="483ca-117">Peer ASN.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="483ca-118">-PeerIp</span><span class="sxs-lookup"><span data-stu-id="483ca-118">-PeerIp</span></span>
<span data-ttu-id="483ca-119">Peer Ip.</span><span class="sxs-lookup"><span data-stu-id="483ca-119">Peer Ip.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="483ca-120">-PeerName</span><span class="sxs-lookup"><span data-stu-id="483ca-120">-PeerName</span></span>
<span data-ttu-id="483ca-121">O nome do roteador virtual Peer.</span><span class="sxs-lookup"><span data-stu-id="483ca-121">The name of the virtual router Peer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="483ca-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="483ca-122">-ResourceGroupName</span></span>
<span data-ttu-id="483ca-123">O nome do grupo de recursos do roteador virtual/par.</span><span class="sxs-lookup"><span data-stu-id="483ca-123">The resource group name of the virtual router/peer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="483ca-124">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="483ca-124">-VirtualRouterName</span></span>
<span data-ttu-id="483ca-125">O roteador virtual onde o par existe.</span><span class="sxs-lookup"><span data-stu-id="483ca-125">The virtual router where peer exists.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="483ca-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="483ca-126">-Confirm</span></span>
<span data-ttu-id="483ca-127">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="483ca-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="483ca-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="483ca-128">-WhatIf</span></span>
<span data-ttu-id="483ca-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="483ca-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="483ca-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="483ca-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="483ca-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="483ca-131">CommonParameters</span></span>
<span data-ttu-id="483ca-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="483ca-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="483ca-133">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="483ca-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="483ca-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="483ca-134">INPUTS</span></span>

### <span data-ttu-id="483ca-135">System.String</span><span class="sxs-lookup"><span data-stu-id="483ca-135">System.String</span></span>

### <span data-ttu-id="483ca-136">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="483ca-136">System.UInt32</span></span>

## <span data-ttu-id="483ca-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="483ca-137">OUTPUTS</span></span>

### <span data-ttu-id="483ca-138">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="483ca-138">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="483ca-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="483ca-139">NOTES</span></span>

## <span data-ttu-id="483ca-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="483ca-140">RELATED LINKS</span></span>
