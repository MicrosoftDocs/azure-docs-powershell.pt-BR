---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azvirtualrouterpeer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualRouterPeer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzVirtualRouterPeer.md
ms.openlocfilehash: 2cb7bc759847af456286bfc611904922a26dc443
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428171"
---
# <span data-ttu-id="c5dfa-101">Add-AzVirtualRouterPeer</span><span class="sxs-lookup"><span data-stu-id="c5dfa-101">Add-AzVirtualRouterPeer</span></span>

## <span data-ttu-id="c5dfa-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c5dfa-102">SYNOPSIS</span></span>
<span data-ttu-id="c5dfa-103">Adicionar um par a um VirtualRouter do Azure</span><span class="sxs-lookup"><span data-stu-id="c5dfa-103">Add a Peer to an Azure VirtualRouter</span></span>

## <span data-ttu-id="c5dfa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c5dfa-104">SYNTAX</span></span>

```
Add-AzVirtualRouterPeer -ResourceGroupName <String> -PeerName <String> -PeerIp <String> -PeerAsn <UInt32>
 -VirtualRouterName <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c5dfa-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c5dfa-105">DESCRIPTION</span></span>
<span data-ttu-id="c5dfa-106">O cmdlet **Add-AzVirtualRouterPeer** adiciona um VirtualRouter de par para um VirtualRouter do Azure</span><span class="sxs-lookup"><span data-stu-id="c5dfa-106">The **Add-AzVirtualRouterPeer** cmdlet adds a VirtualRouter Peer to an Azure VirtualRouter</span></span>

## <span data-ttu-id="c5dfa-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c5dfa-107">EXAMPLES</span></span>

### <span data-ttu-id="c5dfa-108">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c5dfa-108">Example 1</span></span>
```powershell
Add-AzVirtualRouterPeer 1ResourceGroupName virtualRouterRG -PeerName csr -PeerIp 10.0.1.5 -PeerAsn 63000  -VirtualRouterName virtualRouter
```

## <span data-ttu-id="c5dfa-109">OS</span><span class="sxs-lookup"><span data-stu-id="c5dfa-109">PARAMETERS</span></span>

### <span data-ttu-id="c5dfa-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c5dfa-110">-AsJob</span></span>
<span data-ttu-id="c5dfa-111">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="c5dfa-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c5dfa-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5dfa-112">-DefaultProfile</span></span>
<span data-ttu-id="c5dfa-113">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c5dfa-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5dfa-114">-Force</span><span class="sxs-lookup"><span data-stu-id="c5dfa-114">-Force</span></span>
<span data-ttu-id="c5dfa-115">Não pedir confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="c5dfa-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="c5dfa-116">-PeerAsn</span><span class="sxs-lookup"><span data-stu-id="c5dfa-116">-PeerAsn</span></span>
<span data-ttu-id="c5dfa-117">ASN peer.</span><span class="sxs-lookup"><span data-stu-id="c5dfa-117">Peer ASN.</span></span>

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

### <span data-ttu-id="c5dfa-118">-PeerIp</span><span class="sxs-lookup"><span data-stu-id="c5dfa-118">-PeerIp</span></span>
<span data-ttu-id="c5dfa-119">IP de par.</span><span class="sxs-lookup"><span data-stu-id="c5dfa-119">Peer Ip.</span></span>

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

### <span data-ttu-id="c5dfa-120">-PeerName</span><span class="sxs-lookup"><span data-stu-id="c5dfa-120">-PeerName</span></span>
<span data-ttu-id="c5dfa-121">O nome do par de roteador virtual.</span><span class="sxs-lookup"><span data-stu-id="c5dfa-121">The name of the virtual router Peer.</span></span>

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

### <span data-ttu-id="c5dfa-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5dfa-122">-ResourceGroupName</span></span>
<span data-ttu-id="c5dfa-123">O nome do grupo de recursos do roteador virtual/par.</span><span class="sxs-lookup"><span data-stu-id="c5dfa-123">The resource group name of the virtual router/peer.</span></span>

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

### <span data-ttu-id="c5dfa-124">-VirtualRouterName</span><span class="sxs-lookup"><span data-stu-id="c5dfa-124">-VirtualRouterName</span></span>
<span data-ttu-id="c5dfa-125">O roteador virtual em que existe o par.</span><span class="sxs-lookup"><span data-stu-id="c5dfa-125">The virtual router where peer exists.</span></span>

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

### <span data-ttu-id="c5dfa-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c5dfa-126">-Confirm</span></span>
<span data-ttu-id="c5dfa-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5dfa-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5dfa-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5dfa-128">-WhatIf</span></span>
<span data-ttu-id="c5dfa-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c5dfa-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5dfa-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c5dfa-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5dfa-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5dfa-131">CommonParameters</span></span>
<span data-ttu-id="c5dfa-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5dfa-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5dfa-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c5dfa-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5dfa-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c5dfa-134">INPUTS</span></span>

### <span data-ttu-id="c5dfa-135">System. String</span><span class="sxs-lookup"><span data-stu-id="c5dfa-135">System.String</span></span>

### <span data-ttu-id="c5dfa-136">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="c5dfa-136">System.UInt32</span></span>

## <span data-ttu-id="c5dfa-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c5dfa-137">OUTPUTS</span></span>

### <span data-ttu-id="c5dfa-138">Microsoft. Azure. Commands. Network. Models. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="c5dfa-138">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="c5dfa-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c5dfa-139">NOTES</span></span>

## <span data-ttu-id="c5dfa-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c5dfa-140">RELATED LINKS</span></span>
