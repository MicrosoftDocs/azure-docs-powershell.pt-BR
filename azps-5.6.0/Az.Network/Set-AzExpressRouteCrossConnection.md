---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: https://docs.microsoft.com/powershell/module/az.network/set-azexpressroutecrossconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCrossConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCrossConnection.md
ms.openlocfilehash: 9769a5506f528eb03d5e6d5a26340b961786c363
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886885"
---
# <span data-ttu-id="7b179-101">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="7b179-101">Set-AzExpressRouteCrossConnection</span></span>

## <span data-ttu-id="7b179-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b179-102">SYNOPSIS</span></span>
<span data-ttu-id="7b179-103">Modifica uma conexão cruzada ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="7b179-103">Modifies an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="7b179-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7b179-104">SYNTAX</span></span>

### <span data-ttu-id="7b179-105">ModifyByCircuitReference</span><span class="sxs-lookup"><span data-stu-id="7b179-105">ModifyByCircuitReference</span></span>
```
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection <PSExpressRouteCrossConnection> [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b179-106">ModifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="7b179-106">ModifyByParameterValues</span></span>
```
Set-AzExpressRouteCrossConnection -ResourceGroupName <String> -Name <String>
 [-ServiceProviderProvisioningState <String>] [-ServiceProviderNotes <String>]
 [-Peerings <PSExpressRouteCrossConnectionPeering[]>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b179-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7b179-107">DESCRIPTION</span></span>
<span data-ttu-id="7b179-108">O cmdlet **Set-AzExpressRouteCrossConnection** salva a conexão cruzada expressRoute modificada com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7b179-108">The **Set-AzExpressRouteCrossConnection** cmdlet saves the modified ExpressRoute cross connection to Azure.</span></span>

## <span data-ttu-id="7b179-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7b179-109">EXAMPLES</span></span>

### <span data-ttu-id="7b179-110">Exemplo 1: Alterar o Estado de Provisionamento do Provedor de Serviços de uma conexão cruzada ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="7b179-110">Example 1: Change the Service Provider Provisioning State of an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
$cc.ServiceProviderProvisioningState = 'Provisioned'
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="7b179-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7b179-111">PARAMETERS</span></span>

### <span data-ttu-id="7b179-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7b179-112">-AsJob</span></span>
<span data-ttu-id="7b179-113">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="7b179-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7b179-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b179-114">-DefaultProfile</span></span>
<span data-ttu-id="7b179-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="7b179-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b179-116">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="7b179-116">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="7b179-117">Especifica o **objeto ExpressRouteCrossConnection** que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="7b179-117">Specifies the **ExpressRouteCrossConnection** object that this cmdlet modifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection
Parameter Sets: ModifyByCircuitReference
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b179-118">-Force</span><span class="sxs-lookup"><span data-stu-id="7b179-118">-Force</span></span>
<span data-ttu-id="7b179-119">Não peça confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="7b179-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="7b179-120">-Name</span><span class="sxs-lookup"><span data-stu-id="7b179-120">-Name</span></span>
<span data-ttu-id="7b179-121">O nome da conexão entre rotas expressas.</span><span class="sxs-lookup"><span data-stu-id="7b179-121">The name of express route cross connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ModifyByParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b179-122">-Peerings</span><span class="sxs-lookup"><span data-stu-id="7b179-122">-Peerings</span></span>
<span data-ttu-id="7b179-123">A lista de pares para a conexão cruzada</span><span class="sxs-lookup"><span data-stu-id="7b179-123">The list of peerings for the cross connection</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnectionPeering[]
Parameter Sets: ModifyByParameterValues
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b179-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b179-124">-ResourceGroupName</span></span>
<span data-ttu-id="7b179-125">The ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="7b179-125">The ExpressRouteCrossConnection</span></span>

```yaml
Type: System.String
Parameter Sets: ModifyByParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b179-126">-ServiceProviderNotes</span><span class="sxs-lookup"><span data-stu-id="7b179-126">-ServiceProviderNotes</span></span>
<span data-ttu-id="7b179-127">Observações do provedor de serviços</span><span class="sxs-lookup"><span data-stu-id="7b179-127">The service provider notes</span></span>

```yaml
Type: System.String
Parameter Sets: ModifyByParameterValues
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b179-128">-ServiceProviderProvisioningState</span><span class="sxs-lookup"><span data-stu-id="7b179-128">-ServiceProviderProvisioningState</span></span>
<span data-ttu-id="7b179-129">O estado de provisionamento do provedor de serviços a ser definido</span><span class="sxs-lookup"><span data-stu-id="7b179-129">The service provider provisioning state to be set</span></span>

```yaml
Type: System.String
Parameter Sets: ModifyByParameterValues
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7b179-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7b179-130">-Confirm</span></span>
<span data-ttu-id="7b179-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b179-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b179-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b179-132">-WhatIf</span></span>
<span data-ttu-id="7b179-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7b179-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7b179-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7b179-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b179-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b179-135">CommonParameters</span></span>
<span data-ttu-id="7b179-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b179-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b179-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b179-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b179-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7b179-138">INPUTS</span></span>

### <span data-ttu-id="7b179-139">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="7b179-139">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="7b179-140">Parâmetro 'ExpressRouteCrossConnection' aceita o valor do tipo 'PSExpressRouteCrossConnection' do pipeline</span><span class="sxs-lookup"><span data-stu-id="7b179-140">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="7b179-141">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7b179-141">OUTPUTS</span></span>

### <span data-ttu-id="7b179-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="7b179-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="7b179-143">NOTES</span><span class="sxs-lookup"><span data-stu-id="7b179-143">NOTES</span></span>

## <span data-ttu-id="7b179-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7b179-144">RELATED LINKS</span></span>

[<span data-ttu-id="7b179-145">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="7b179-145">Get-AzExpressRouteCrossConnection</span></span>](./Get-AzExpressRouteCrossConnection.md)
