---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutecrossconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCrossConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCrossConnection.md
ms.openlocfilehash: 175082a90a1a494eb4508bc83d71584326c9eb97
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93771451"
---
# <span data-ttu-id="dc73c-101">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="dc73c-101">Set-AzExpressRouteCrossConnection</span></span>

## <span data-ttu-id="dc73c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dc73c-102">SYNOPSIS</span></span>
<span data-ttu-id="dc73c-103">Modifica uma conexão cruzada do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="dc73c-103">Modifies an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="dc73c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dc73c-104">SYNTAX</span></span>

### <span data-ttu-id="dc73c-105">ModifyByCircuitReference</span><span class="sxs-lookup"><span data-stu-id="dc73c-105">ModifyByCircuitReference</span></span>
```
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection <PSExpressRouteCrossConnection> [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc73c-106">ModifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="dc73c-106">ModifyByParameterValues</span></span>
```
Set-AzExpressRouteCrossConnection -ResourceGroupName <String> -Name <String>
 [-ServiceProviderProvisioningState <String>] [-ServiceProviderNotes <String>]
 [-Peerings <PSExpressRouteCrossConnectionPeering[]>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc73c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dc73c-107">DESCRIPTION</span></span>
<span data-ttu-id="dc73c-108">O cmdlet **set-AzExpressRouteCrossConnection** salva a conexão cruzada do ExpressRoute modificado no Azure.</span><span class="sxs-lookup"><span data-stu-id="dc73c-108">The **Set-AzExpressRouteCrossConnection** cmdlet saves the modified ExpressRoute cross connection to Azure.</span></span>

## <span data-ttu-id="dc73c-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dc73c-109">EXAMPLES</span></span>

### <span data-ttu-id="dc73c-110">Exemplo 1: alterar o estado de provisionamento do provedor de serviço de uma conexão cruzada do ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="dc73c-110">Example 1: Change the Service Provider Provisioning State of an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
$cc.ServiceProviderProvisioningState = 'Provisioned'
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="dc73c-111">OS</span><span class="sxs-lookup"><span data-stu-id="dc73c-111">PARAMETERS</span></span>

### <span data-ttu-id="dc73c-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dc73c-112">-AsJob</span></span>
<span data-ttu-id="dc73c-113">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="dc73c-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dc73c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc73c-114">-DefaultProfile</span></span>
<span data-ttu-id="dc73c-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dc73c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc73c-116">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="dc73c-116">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="dc73c-117">Especifica o objeto **ExpressRouteCrossConnection** que esse cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="dc73c-117">Specifies the **ExpressRouteCrossConnection** object that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="dc73c-118">-Force</span><span class="sxs-lookup"><span data-stu-id="dc73c-118">-Force</span></span>
<span data-ttu-id="dc73c-119">Não pedir confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="dc73c-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="dc73c-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="dc73c-120">-Name</span></span>
<span data-ttu-id="dc73c-121">O nome da conexão cruzada de rota expressa.</span><span class="sxs-lookup"><span data-stu-id="dc73c-121">The name of express route cross connection.</span></span>

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

### <span data-ttu-id="dc73c-122">-Correspondências</span><span class="sxs-lookup"><span data-stu-id="dc73c-122">-Peerings</span></span>
<span data-ttu-id="dc73c-123">A lista de pares para a conexão cruzada</span><span class="sxs-lookup"><span data-stu-id="dc73c-123">The list of peerings for the cross connection</span></span>

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

### <span data-ttu-id="dc73c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc73c-124">-ResourceGroupName</span></span>
<span data-ttu-id="dc73c-125">O ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="dc73c-125">The ExpressRouteCrossConnection</span></span>

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

### <span data-ttu-id="dc73c-126">-ServiceProviderNotes</span><span class="sxs-lookup"><span data-stu-id="dc73c-126">-ServiceProviderNotes</span></span>
<span data-ttu-id="dc73c-127">As anotações do provedor de serviços</span><span class="sxs-lookup"><span data-stu-id="dc73c-127">The service provider notes</span></span>

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

### <span data-ttu-id="dc73c-128">-ServiceProviderProvisioningState</span><span class="sxs-lookup"><span data-stu-id="dc73c-128">-ServiceProviderProvisioningState</span></span>
<span data-ttu-id="dc73c-129">O estado de provisionamento do provedor de serviço a ser definido</span><span class="sxs-lookup"><span data-stu-id="dc73c-129">The service provider provisioning state to be set</span></span>

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

### <span data-ttu-id="dc73c-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="dc73c-130">-Confirm</span></span>
<span data-ttu-id="dc73c-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc73c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc73c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc73c-132">-WhatIf</span></span>
<span data-ttu-id="dc73c-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="dc73c-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dc73c-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="dc73c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc73c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc73c-135">CommonParameters</span></span>
<span data-ttu-id="dc73c-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc73c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc73c-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc73c-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc73c-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dc73c-138">INPUTS</span></span>

### <span data-ttu-id="dc73c-139">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="dc73c-139">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="dc73c-140">O parâmetro ' ExpressRouteCrossConnection ' aceita o valor do tipo ' PSExpressRouteCrossConnection ' do pipeline</span><span class="sxs-lookup"><span data-stu-id="dc73c-140">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="dc73c-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dc73c-141">OUTPUTS</span></span>

### <span data-ttu-id="dc73c-142">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="dc73c-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="dc73c-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dc73c-143">NOTES</span></span>

## <span data-ttu-id="dc73c-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dc73c-144">RELATED LINKS</span></span>

[<span data-ttu-id="dc73c-145">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="dc73c-145">Get-AzExpressRouteCrossConnection</span></span>](./Get-AzExpressRouteCrossConnection.md)
