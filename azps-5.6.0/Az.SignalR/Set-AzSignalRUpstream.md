---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/powershell/module/az.signalr/set-azsignalrupstream
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Set-AzSignalRUpstream.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Set-AzSignalRUpstream.md
ms.openlocfilehash: 7fde7a8f40efaee9cbf3011e844ee8a48e3949a4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885807"
---
# <span data-ttu-id="6524b-101">Set-AzSignalRUpstream</span><span class="sxs-lookup"><span data-stu-id="6524b-101">Set-AzSignalRUpstream</span></span>

## <span data-ttu-id="6524b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6524b-102">SYNOPSIS</span></span>
<span data-ttu-id="6524b-103">Definir as configurações upstream de um serviço SignalR.</span><span class="sxs-lookup"><span data-stu-id="6524b-103">Set the upstream settings of a SignalR service.</span></span>

## <span data-ttu-id="6524b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6524b-104">SYNTAX</span></span>

### <span data-ttu-id="6524b-105">ResourceGroupParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="6524b-105">ResourceGroupParameterSet (Default)</span></span>
```
Set-AzSignalRUpstream [-ResourceGroupName <String>] [-Name] <String> [-AsJob]
 [-Template <PSUpstreamTemplate[]>] [-Clear] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6524b-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6524b-106">ResourceIdParameterSet</span></span>
```
Set-AzSignalRUpstream -ResourceId <String> [-AsJob] [-Template <PSUpstreamTemplate[]>] [-Clear]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6524b-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6524b-107">InputObjectParameterSet</span></span>
```
Set-AzSignalRUpstream -InputObject <PSSignalRResource> [-AsJob] [-Template <PSUpstreamTemplate[]>] [-Clear]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6524b-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6524b-108">DESCRIPTION</span></span>
<span data-ttu-id="6524b-109">Definir as configurações upstream de um serviço SignalR.</span><span class="sxs-lookup"><span data-stu-id="6524b-109">Set the upstream settings of a SignalR service.</span></span>

## <span data-ttu-id="6524b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6524b-110">EXAMPLES</span></span>

### <span data-ttu-id="6524b-111">Definir dois modelos de upstream ordenados</span><span class="sxs-lookup"><span data-stu-id="6524b-111">Set two ordered upstream templates</span></span>
```powershell
PS C:\>  Set-AzSignalRUpstream -name pssignalr -ResourceGroupName test_resource_group -Template @{UrlTemplate='http://host-connections1.com'; HubPattern='chat';EventPattern='broadcast' }, @{UrlTemplate='http://host-connections2.com'}

Templates
---------
{Microsoft.Azure.Commands.SignalR.Models.PSUpstreamTemplate, Microsoft.Azure.Commands.SignalR.Models.PSUpstreamTemplat…
```

<span data-ttu-id="6524b-112">O JSON a seguir representa o conjunto de modelos reais.</span><span class="sxs-lookup"><span data-stu-id="6524b-112">The following JSON represents the actual templates set.</span></span> 

 `
{
    "hubPattern": "chat",
    "eventPattern": "broadcast",
    "categoryPattern": "*",
    "urlTemplate": "http://host-connections1.com"
},
{
    "hubPattern": "*",
    "eventPattern": "*",
    "categoryPattern": "*",
    "urlTemplate": "http://host-connections2.com"
}
`

### <span data-ttu-id="6524b-113">Limpar todas as configurações de upstream</span><span class="sxs-lookup"><span data-stu-id="6524b-113">Clear all the upstream settings</span></span>
```powershell
PS C:\>  Set-AzSignalRUpstream -name pssignalr -ResourceGroupName test_resource_group -Clear

Templates
---------
{}
```

## <span data-ttu-id="6524b-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6524b-114">PARAMETERS</span></span>

### <span data-ttu-id="6524b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6524b-115">-AsJob</span></span>
<span data-ttu-id="6524b-116">Execute o cmdlet em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="6524b-116">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="6524b-117">-Clear</span><span class="sxs-lookup"><span data-stu-id="6524b-117">-Clear</span></span>
<span data-ttu-id="6524b-118">Desembaixe todas as configurações de upstream.</span><span class="sxs-lookup"><span data-stu-id="6524b-118">Clear all the upstream settings.</span></span>

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

### <span data-ttu-id="6524b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6524b-119">-DefaultProfile</span></span>
<span data-ttu-id="6524b-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6524b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6524b-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6524b-121">-InputObject</span></span>
<span data-ttu-id="6524b-122">O objeto de recurso SignalR.</span><span class="sxs-lookup"><span data-stu-id="6524b-122">The SignalR resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6524b-123">-Name</span><span class="sxs-lookup"><span data-stu-id="6524b-123">-Name</span></span>
<span data-ttu-id="6524b-124">O nome do serviço SignalR.</span><span class="sxs-lookup"><span data-stu-id="6524b-124">The SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6524b-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6524b-125">-ResourceGroupName</span></span>
<span data-ttu-id="6524b-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6524b-126">The resource group name.</span></span>
<span data-ttu-id="6524b-127">O padrão será usado se não for especificado.</span><span class="sxs-lookup"><span data-stu-id="6524b-127">The default one will be used if not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6524b-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6524b-128">-ResourceId</span></span>
<span data-ttu-id="6524b-129">A ID do recurso de serviço SignalR.</span><span class="sxs-lookup"><span data-stu-id="6524b-129">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6524b-130">-Template</span><span class="sxs-lookup"><span data-stu-id="6524b-130">-Template</span></span>
<span data-ttu-id="6524b-131">Itens de modelo para configurações upstream.</span><span class="sxs-lookup"><span data-stu-id="6524b-131">Template item(s) for upstream settings.</span></span>
<span data-ttu-id="6524b-132">Chave necessária: UrlTemplate.</span><span class="sxs-lookup"><span data-stu-id="6524b-132">Required key: UrlTemplate.</span></span>
<span data-ttu-id="6524b-133">Teclas opcionais: HubPattern, EventPattern, CategoryPattern.</span><span class="sxs-lookup"><span data-stu-id="6524b-133">Optional keys: HubPattern, EventPattern, CategoryPattern.</span></span>
<span data-ttu-id="6524b-134">Exemplo usando a sintaxe de splatting para passar o parâmetro templates: @{UrlTemplate=' http://host-connections1.com ', HubPattern= 'chat'; EventPattern='broadcast' },@{UrlTemplate=' http://host-connections2.com '}</span><span class="sxs-lookup"><span data-stu-id="6524b-134">Example using splatting syntax to pass templates parameter: @{UrlTemplate='http://host-connections1.com', HubPattern= 'chat';EventPattern='broadcast' },@{UrlTemplate='http://host-connections2.com'}</span></span>

```yaml
Type: Microsoft.Azure.Commands.SignalR.Models.PSUpstreamTemplate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6524b-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6524b-135">-Confirm</span></span>
<span data-ttu-id="6524b-136">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6524b-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6524b-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6524b-137">-WhatIf</span></span>
<span data-ttu-id="6524b-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6524b-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6524b-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6524b-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6524b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6524b-140">CommonParameters</span></span>
<span data-ttu-id="6524b-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6524b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6524b-142">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6524b-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6524b-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6524b-143">INPUTS</span></span>

### <span data-ttu-id="6524b-144">System.String</span><span class="sxs-lookup"><span data-stu-id="6524b-144">System.String</span></span>

## <span data-ttu-id="6524b-145">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6524b-145">OUTPUTS</span></span>

### <span data-ttu-id="6524b-146">Microsoft.Azure.Commands.SignalR.Models.PSServerlessUpstreamSettings</span><span class="sxs-lookup"><span data-stu-id="6524b-146">Microsoft.Azure.Commands.SignalR.Models.PSServerlessUpstreamSettings</span></span>

## <span data-ttu-id="6524b-147">NOTES</span><span class="sxs-lookup"><span data-stu-id="6524b-147">NOTES</span></span>

## <span data-ttu-id="6524b-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6524b-148">RELATED LINKS</span></span>

[<span data-ttu-id="6524b-149">Como usar o splatting para passar parâmetros para comandos no PowerShell</span><span class="sxs-lookup"><span data-stu-id="6524b-149">How to use splatting to pass parameters to commands in PowerShell</span></span>](https://docs.microsoft.com/powershell/module/microsoft.powershell.core/about/about_splatting?view=powershell-7)
