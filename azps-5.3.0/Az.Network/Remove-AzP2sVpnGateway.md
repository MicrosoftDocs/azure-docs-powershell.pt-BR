---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzP2sVpnGateway.md
ms.openlocfilehash: 704a8e0164361c338ac182eef3bf09758eec363b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434699"
---
# <span data-ttu-id="6ba8c-101">Remove-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="6ba8c-101">Remove-AzP2sVpnGateway</span></span>

## <span data-ttu-id="6ba8c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6ba8c-102">SYNOPSIS</span></span>
<span data-ttu-id="6ba8c-103">Remove um P2SVpnGateway existente.</span><span class="sxs-lookup"><span data-stu-id="6ba8c-103">Removes an existing P2SVpnGateway.</span></span>

## <span data-ttu-id="6ba8c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6ba8c-104">SYNTAX</span></span>

### <span data-ttu-id="6ba8c-105">ByP2SVpnGatewayName (padrão)</span><span class="sxs-lookup"><span data-stu-id="6ba8c-105">ByP2SVpnGatewayName (Default)</span></span>
```
Remove-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ba8c-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="6ba8c-106">ByP2SVpnGatewayObject</span></span>
```
Remove-AzP2sVpnGateway -InputObject <PSP2SVpnGateway> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ba8c-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="6ba8c-107">ByP2SVpnGatewayResourceId</span></span>
```
Remove-AzP2sVpnGateway -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ba8c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6ba8c-108">DESCRIPTION</span></span>
<span data-ttu-id="6ba8c-109">O cmdlet **Remove-AzP2sVpnGateway** permite remover um P2SVpnGateway existente em VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="6ba8c-109">The **Remove-AzP2sVpnGateway** cmdlet enables you to remove an existing P2SVpnGateway under VirtualHub.</span></span> <span data-ttu-id="6ba8c-110">Todo o ponto para a conectividade dos clientes do site falhará depois que o P2SVpnGateway for removido.</span><span class="sxs-lookup"><span data-stu-id="6ba8c-110">All the point to site clients connectivity will fail after P2SVpnGateway is removed.</span></span>

## <span data-ttu-id="6ba8c-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6ba8c-111">EXAMPLES</span></span>

### <span data-ttu-id="6ba8c-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6ba8c-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzP2sVpnGateway -Name 683482ade8564515aed4b8448c9757ea-westus-gw-ResourceGroupName P2SCortexGATesting -Force -PassThru
```

<span data-ttu-id="6ba8c-113">O cmdlet **Remove-AzP2sVpnGateway** permite remover um P2SVpnGateway existente em VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="6ba8c-113">The **Remove-AzP2sVpnGateway** cmdlet enables you to remove an existing P2SVpnGateway under VirtualHub.</span></span>

## <span data-ttu-id="6ba8c-114">OS</span><span class="sxs-lookup"><span data-stu-id="6ba8c-114">PARAMETERS</span></span>

### <span data-ttu-id="6ba8c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ba8c-115">-DefaultProfile</span></span>
<span data-ttu-id="6ba8c-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6ba8c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ba8c-117">-Force</span><span class="sxs-lookup"><span data-stu-id="6ba8c-117">-Force</span></span>
<span data-ttu-id="6ba8c-118">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="6ba8c-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="6ba8c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6ba8c-119">-InputObject</span></span>
<span data-ttu-id="6ba8c-120">O objeto p2sVpnGateway a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="6ba8c-120">The p2sVpnGateway object to be deleted.</span></span>

```yaml
Type: PSP2SVpnGateway
Parameter Sets: ByP2SVpnGatewayObject
Aliases: P2SVpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6ba8c-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="6ba8c-121">-Name</span></span>
<span data-ttu-id="6ba8c-122">O nome P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="6ba8c-122">The P2SVpnGateway name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases: ResourceName, P2SVpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ba8c-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6ba8c-123">-PassThru</span></span>
<span data-ttu-id="6ba8c-124">Retorna um objeto que representa o item em que essa operação está sendo executada.</span><span class="sxs-lookup"><span data-stu-id="6ba8c-124">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="6ba8c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ba8c-125">-ResourceGroupName</span></span>
<span data-ttu-id="6ba8c-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6ba8c-126">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ba8c-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ba8c-127">-ResourceId</span></span>
<span data-ttu-id="6ba8c-128">A ID de recurso do Azure para o p2sVpnGateway a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="6ba8c-128">The Azure resource ID for the p2sVpnGateway to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayResourceId
Aliases: p2sVpnGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ba8c-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6ba8c-129">-Confirm</span></span>
<span data-ttu-id="6ba8c-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ba8c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ba8c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ba8c-131">-WhatIf</span></span>
<span data-ttu-id="6ba8c-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6ba8c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ba8c-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6ba8c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ba8c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ba8c-134">CommonParameters</span></span>
<span data-ttu-id="6ba8c-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ba8c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ba8c-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ba8c-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ba8c-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6ba8c-137">INPUTS</span></span>

### <span data-ttu-id="6ba8c-138">Microsoft. Azure. Commands. Network. Models. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="6ba8c-138">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>
<span data-ttu-id="6ba8c-139">System. String</span><span class="sxs-lookup"><span data-stu-id="6ba8c-139">System.String</span></span>

## <span data-ttu-id="6ba8c-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6ba8c-140">OUTPUTS</span></span>

### <span data-ttu-id="6ba8c-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6ba8c-141">System.Boolean</span></span>

## <span data-ttu-id="6ba8c-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6ba8c-142">NOTES</span></span>

## <span data-ttu-id="6ba8c-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6ba8c-143">RELATED LINKS</span></span>
