---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzP2sVpnGateway.md
ms.openlocfilehash: 704a8e0164361c338ac182eef3bf09758eec363b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117344"
---
# <span data-ttu-id="e5bbc-101">Remove-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="e5bbc-101">Remove-AzP2sVpnGateway</span></span>

## <span data-ttu-id="e5bbc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e5bbc-102">SYNOPSIS</span></span>
<span data-ttu-id="e5bbc-103">Remove um P2SVpnGateway existente.</span><span class="sxs-lookup"><span data-stu-id="e5bbc-103">Removes an existing P2SVpnGateway.</span></span>

## <span data-ttu-id="e5bbc-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e5bbc-104">SYNTAX</span></span>

### <span data-ttu-id="e5bbc-105">ByP2SVpnGatewayName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e5bbc-105">ByP2SVpnGatewayName (Default)</span></span>
```
Remove-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5bbc-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="e5bbc-106">ByP2SVpnGatewayObject</span></span>
```
Remove-AzP2sVpnGateway -InputObject <PSP2SVpnGateway> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e5bbc-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="e5bbc-107">ByP2SVpnGatewayResourceId</span></span>
```
Remove-AzP2sVpnGateway -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5bbc-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="e5bbc-108">DESCRIPTION</span></span>
<span data-ttu-id="e5bbc-109">O cmdlet **Remove-AzP2sVpnGateway** permite remover um P2SVpnGateway existente no VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="e5bbc-109">The **Remove-AzP2sVpnGateway** cmdlet enables you to remove an existing P2SVpnGateway under VirtualHub.</span></span> <span data-ttu-id="e5bbc-110">Toda a conectividade de clientes de site falhará após a remoção do P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="e5bbc-110">All the point to site clients connectivity will fail after P2SVpnGateway is removed.</span></span>

## <span data-ttu-id="e5bbc-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e5bbc-111">EXAMPLES</span></span>

### <span data-ttu-id="e5bbc-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e5bbc-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzP2sVpnGateway -Name 683482ade8564515aed4b8448c9757ea-westus-gw-ResourceGroupName P2SCortexGATesting -Force -PassThru
```

<span data-ttu-id="e5bbc-113">O cmdlet **Remove-AzP2sVpnGateway** permite remover um P2SVpnGateway existente no VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="e5bbc-113">The **Remove-AzP2sVpnGateway** cmdlet enables you to remove an existing P2SVpnGateway under VirtualHub.</span></span>

## <span data-ttu-id="e5bbc-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e5bbc-114">PARAMETERS</span></span>

### <span data-ttu-id="e5bbc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5bbc-115">-DefaultProfile</span></span>
<span data-ttu-id="e5bbc-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e5bbc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5bbc-117">-Forçar</span><span class="sxs-lookup"><span data-stu-id="e5bbc-117">-Force</span></span>
<span data-ttu-id="e5bbc-118">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="e5bbc-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="e5bbc-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5bbc-119">-InputObject</span></span>
<span data-ttu-id="e5bbc-120">O objeto p2sVpnGateway a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="e5bbc-120">The p2sVpnGateway object to be deleted.</span></span>

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

### <span data-ttu-id="e5bbc-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="e5bbc-121">-Name</span></span>
<span data-ttu-id="e5bbc-122">O nome P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="e5bbc-122">The P2SVpnGateway name.</span></span>

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

### <span data-ttu-id="e5bbc-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e5bbc-123">-PassThru</span></span>
<span data-ttu-id="e5bbc-124">Retorna um objeto que representa o item no qual esta operação está sendo executada.</span><span class="sxs-lookup"><span data-stu-id="e5bbc-124">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="e5bbc-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5bbc-125">-ResourceGroupName</span></span>
<span data-ttu-id="e5bbc-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e5bbc-126">The resource group name.</span></span>

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

### <span data-ttu-id="e5bbc-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e5bbc-127">-ResourceId</span></span>
<span data-ttu-id="e5bbc-128">A ID de recurso do Azure para que o p2sVpnGateway seja excluído.</span><span class="sxs-lookup"><span data-stu-id="e5bbc-128">The Azure resource ID for the p2sVpnGateway to be deleted.</span></span>

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

### <span data-ttu-id="e5bbc-129">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="e5bbc-129">-Confirm</span></span>
<span data-ttu-id="e5bbc-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e5bbc-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5bbc-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5bbc-131">-WhatIf</span></span>
<span data-ttu-id="e5bbc-132">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="e5bbc-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5bbc-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e5bbc-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5bbc-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5bbc-134">CommonParameters</span></span>
<span data-ttu-id="e5bbc-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5bbc-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5bbc-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5bbc-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5bbc-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="e5bbc-137">INPUTS</span></span>

### <span data-ttu-id="e5bbc-138">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="e5bbc-138">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>
<span data-ttu-id="e5bbc-139">System.String</span><span class="sxs-lookup"><span data-stu-id="e5bbc-139">System.String</span></span>

## <span data-ttu-id="e5bbc-140">Saídas</span><span class="sxs-lookup"><span data-stu-id="e5bbc-140">OUTPUTS</span></span>

### <span data-ttu-id="e5bbc-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e5bbc-141">System.Boolean</span></span>

## <span data-ttu-id="e5bbc-142">Notas</span><span class="sxs-lookup"><span data-stu-id="e5bbc-142">NOTES</span></span>

## <span data-ttu-id="e5bbc-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e5bbc-143">RELATED LINKS</span></span>
