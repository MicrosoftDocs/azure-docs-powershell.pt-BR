---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualRouter.md
ms.openlocfilehash: 75315de4e6ca2cf799f6cefb1d3b9c143631f5a3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943222"
---
# <span data-ttu-id="bf7a7-101">New-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="bf7a7-101">New-AzVirtualRouter</span></span>

## <span data-ttu-id="bf7a7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bf7a7-102">SYNOPSIS</span></span>
<span data-ttu-id="bf7a7-103">Cria um VirtualRouter do Azure.</span><span class="sxs-lookup"><span data-stu-id="bf7a7-103">Creates an Azure VirtualRouter.</span></span>

## <span data-ttu-id="bf7a7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bf7a7-104">SYNTAX</span></span>

### <span data-ttu-id="bf7a7-105">HostedGatewayParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="bf7a7-105">HostedGatewayParameterSet (Default)</span></span>
```
New-AzVirtualRouter -ResourceGroupName <String> -Name <String> -HostedGateway <PSVirtualNetworkGateway>
 -Location <String> [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf7a7-106">HostedGatewayIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf7a7-106">HostedGatewayIdParameterSet</span></span>
```
New-AzVirtualRouter -ResourceGroupName <String> -Name <String> -HostedGatewayId <String> -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bf7a7-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bf7a7-107">DESCRIPTION</span></span>
<span data-ttu-id="bf7a7-108">O cmdlet **New-AzVirtualRouter** cria um Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="bf7a7-108">The **New-AzVirtualRouter** cmdlet creates an Azure VirtualRouter</span></span>


## <span data-ttu-id="bf7a7-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bf7a7-109">EXAMPLES</span></span>

### <span data-ttu-id="bf7a7-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bf7a7-110">Example 1</span></span>
```powershell
$gatewayId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualNetworkGateways/erGateway'
New-AzVirtualRouter -RouterName virtualRouter -ResourceGroupName virtualRouterRG -Location 'West US'  -HostedGatewayId $gatewayId
```

### <span data-ttu-id="bf7a7-111">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="bf7a7-111">Example 2</span></span>
```powershell
$gateway = Get-AzVirtualNetworkGateway -Name erGateway -ResourceGroupName virtualRouterRG
New-AzVirtualRouter -RouterName virtualRouter -ResourceGroupName virtualRouterRG -Location 'West US'  -HostedGateway $gateway
```

## <span data-ttu-id="bf7a7-112">OS</span><span class="sxs-lookup"><span data-stu-id="bf7a7-112">PARAMETERS</span></span>

### <span data-ttu-id="bf7a7-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bf7a7-113">-AsJob</span></span>
<span data-ttu-id="bf7a7-114">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="bf7a7-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf7a7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf7a7-115">-DefaultProfile</span></span>
<span data-ttu-id="bf7a7-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bf7a7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf7a7-117">-Force</span><span class="sxs-lookup"><span data-stu-id="bf7a7-117">-Force</span></span>
<span data-ttu-id="bf7a7-118">Não pedir confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="bf7a7-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf7a7-119">-HostedGateway</span><span class="sxs-lookup"><span data-stu-id="bf7a7-119">-HostedGateway</span></span>
<span data-ttu-id="bf7a7-120">O gateway em que o roteador virtual precisa ser hospedado.</span><span class="sxs-lookup"><span data-stu-id="bf7a7-120">The gateway where Virtual Router needs to be hosted.</span></span>

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: HostedGatewayParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf7a7-121">-HostedGatewayId</span><span class="sxs-lookup"><span data-stu-id="bf7a7-121">-HostedGatewayId</span></span>
<span data-ttu-id="bf7a7-122">A ID do gateway em que o roteador virtual precisa ser hospedado.</span><span class="sxs-lookup"><span data-stu-id="bf7a7-122">The id of gateway where Virtual Router needs to be hosted.</span></span>

```yaml
Type: String
Parameter Sets: HostedGatewayIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf7a7-123">-Local</span><span class="sxs-lookup"><span data-stu-id="bf7a7-123">-Location</span></span>
<span data-ttu-id="bf7a7-124">O local.</span><span class="sxs-lookup"><span data-stu-id="bf7a7-124">The location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf7a7-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="bf7a7-125">-Name</span></span>
<span data-ttu-id="bf7a7-126">O nome do roteador virtual.</span><span class="sxs-lookup"><span data-stu-id="bf7a7-126">The name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf7a7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf7a7-127">-ResourceGroupName</span></span>
<span data-ttu-id="bf7a7-128">O nome do grupo de recursos do roteador virtual.</span><span class="sxs-lookup"><span data-stu-id="bf7a7-128">The resource group name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf7a7-129">-Marca</span><span class="sxs-lookup"><span data-stu-id="bf7a7-129">-Tag</span></span>
<span data-ttu-id="bf7a7-130">Uma Hashtable que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="bf7a7-130">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf7a7-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="bf7a7-131">-Confirm</span></span>
<span data-ttu-id="bf7a7-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf7a7-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf7a7-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf7a7-133">-WhatIf</span></span>
<span data-ttu-id="bf7a7-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bf7a7-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf7a7-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bf7a7-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf7a7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf7a7-136">CommonParameters</span></span>
<span data-ttu-id="bf7a7-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf7a7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="bf7a7-138">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf7a7-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf7a7-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bf7a7-139">INPUTS</span></span>

### <span data-ttu-id="bf7a7-140">System. String</span><span class="sxs-lookup"><span data-stu-id="bf7a7-140">System.String</span></span>

### <span data-ttu-id="bf7a7-141">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="bf7a7-141">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="bf7a7-142">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="bf7a7-142">System.Collections.Hashtable</span></span>

## <span data-ttu-id="bf7a7-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bf7a7-143">OUTPUTS</span></span>

### <span data-ttu-id="bf7a7-144">Microsoft. Azure. Commands. Network. Models. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="bf7a7-144">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="bf7a7-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bf7a7-145">NOTES</span></span>

## <span data-ttu-id="bf7a7-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bf7a7-146">RELATED LINKS</span></span>
