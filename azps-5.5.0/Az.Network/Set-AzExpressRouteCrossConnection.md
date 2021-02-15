---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutecrossconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCrossConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCrossConnection.md
ms.openlocfilehash: 649ae6233f312dab4f18263bb65c4a9cd43b2aee
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114098"
---
# <span data-ttu-id="0f553-101">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="0f553-101">Set-AzExpressRouteCrossConnection</span></span>

## <span data-ttu-id="0f553-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0f553-102">SYNOPSIS</span></span>
<span data-ttu-id="0f553-103">Modifica uma conexão cruzada do ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="0f553-103">Modifies an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="0f553-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0f553-104">SYNTAX</span></span>

### <span data-ttu-id="0f553-105">ModifyBy CircuitReference</span><span class="sxs-lookup"><span data-stu-id="0f553-105">ModifyByCircuitReference</span></span>
```
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection <PSExpressRouteCrossConnection> [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f553-106">ModifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="0f553-106">ModifyByParameterValues</span></span>
```
Set-AzExpressRouteCrossConnection -ResourceGroupName <String> -Name <String>
 [-ServiceProviderProvisioningState <String>] [-ServiceProviderNotes <String>]
 [-Peerings <PSExpressRouteCrossConnectionPeering[]>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f553-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="0f553-107">DESCRIPTION</span></span>
<span data-ttu-id="0f553-108">O cmdlet **Set-AzExpressRouteCrossConnection** salva a conexão cruzada do ExpressRoute modificada com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0f553-108">The **Set-AzExpressRouteCrossConnection** cmdlet saves the modified ExpressRoute cross connection to Azure.</span></span>

## <span data-ttu-id="0f553-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0f553-109">EXAMPLES</span></span>

### <span data-ttu-id="0f553-110">Exemplo 1: Alterar o Estado de Provisionamento do Provedor de Serviços de uma conexão cruzada do ExpressRoute</span><span class="sxs-lookup"><span data-stu-id="0f553-110">Example 1: Change the Service Provider Provisioning State of an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
$cc.ServiceProviderProvisioningState = 'Provisioned'
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="0f553-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0f553-111">PARAMETERS</span></span>

### <span data-ttu-id="0f553-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0f553-112">-AsJob</span></span>
<span data-ttu-id="0f553-113">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="0f553-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0f553-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f553-114">-DefaultProfile</span></span>
<span data-ttu-id="0f553-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="0f553-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f553-116">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="0f553-116">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="0f553-117">Especifica o objeto **ExpressRouteCrossConnection** que este cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="0f553-117">Specifies the **ExpressRouteCrossConnection** object that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="0f553-118">-Forçar</span><span class="sxs-lookup"><span data-stu-id="0f553-118">-Force</span></span>
<span data-ttu-id="0f553-119">Não peça confirmação se quiser substituir um recurso</span><span class="sxs-lookup"><span data-stu-id="0f553-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="0f553-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="0f553-120">-Name</span></span>
<span data-ttu-id="0f553-121">O nome da conexão cruzada de rota expressa.</span><span class="sxs-lookup"><span data-stu-id="0f553-121">The name of express route cross connection.</span></span>

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

### <span data-ttu-id="0f553-122">-Peerings</span><span class="sxs-lookup"><span data-stu-id="0f553-122">-Peerings</span></span>
<span data-ttu-id="0f553-123">A lista de pares para a conexão cruzada</span><span class="sxs-lookup"><span data-stu-id="0f553-123">The list of peerings for the cross connection</span></span>

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

### <span data-ttu-id="0f553-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f553-124">-ResourceGroupName</span></span>
<span data-ttu-id="0f553-125">O ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="0f553-125">The ExpressRouteCrossConnection</span></span>

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

### <span data-ttu-id="0f553-126">-ServiceProviderNotes</span><span class="sxs-lookup"><span data-stu-id="0f553-126">-ServiceProviderNotes</span></span>
<span data-ttu-id="0f553-127">As anotações do provedor de serviços</span><span class="sxs-lookup"><span data-stu-id="0f553-127">The service provider notes</span></span>

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

### <span data-ttu-id="0f553-128">-ServiceProviderProvisioningState</span><span class="sxs-lookup"><span data-stu-id="0f553-128">-ServiceProviderProvisioningState</span></span>
<span data-ttu-id="0f553-129">O estado de provisionamento do provedor de serviços a ser definido</span><span class="sxs-lookup"><span data-stu-id="0f553-129">The service provider provisioning state to be set</span></span>

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

### <span data-ttu-id="0f553-130">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="0f553-130">-Confirm</span></span>
<span data-ttu-id="0f553-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f553-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f553-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f553-132">-WhatIf</span></span>
<span data-ttu-id="0f553-133">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="0f553-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0f553-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0f553-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f553-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f553-135">CommonParameters</span></span>
<span data-ttu-id="0f553-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f553-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f553-137">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f553-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f553-138">Entradas</span><span class="sxs-lookup"><span data-stu-id="0f553-138">INPUTS</span></span>

### <span data-ttu-id="0f553-139">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="0f553-139">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="0f553-140">Parâmetro 'ExpressRouteCrossConnection' aceita o valor do tipo 'PSExpressRouteCrossConnection' do pipeline</span><span class="sxs-lookup"><span data-stu-id="0f553-140">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="0f553-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="0f553-141">OUTPUTS</span></span>

### <span data-ttu-id="0f553-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="0f553-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="0f553-143">Notas</span><span class="sxs-lookup"><span data-stu-id="0f553-143">NOTES</span></span>

## <span data-ttu-id="0f553-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0f553-144">RELATED LINKS</span></span>

[<span data-ttu-id="0f553-145">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="0f553-145">Get-AzExpressRouteCrossConnection</span></span>](./Get-AzExpressRouteCrossConnection.md)
