---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/set-azsignalrupstream
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Set-AzSignalRUpstream.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Set-AzSignalRUpstream.md
ms.openlocfilehash: e04e87067f86f529117512e7443118f308b20547
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118633"
---
# <span data-ttu-id="849ff-101">Set-AzSignalRUpstream</span><span class="sxs-lookup"><span data-stu-id="849ff-101">Set-AzSignalRUpstream</span></span>

## <span data-ttu-id="849ff-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="849ff-102">SYNOPSIS</span></span>
<span data-ttu-id="849ff-103">Definir as configurações upstream de um serviço de Sinalização.</span><span class="sxs-lookup"><span data-stu-id="849ff-103">Set the upstream settings of a SignalR service.</span></span>

## <span data-ttu-id="849ff-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="849ff-104">SYNTAX</span></span>

### <span data-ttu-id="849ff-105">ResourceGroupParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="849ff-105">ResourceGroupParameterSet (Default)</span></span>
```
Set-AzSignalRUpstream [-ResourceGroupName <String>] [-Name] <String> [-AsJob]
 [-Template <PSUpstreamTemplate[]>] [-Clear] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="849ff-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="849ff-106">ResourceIdParameterSet</span></span>
```
Set-AzSignalRUpstream -ResourceId <String> [-AsJob] [-Template <PSUpstreamTemplate[]>] [-Clear]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="849ff-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="849ff-107">InputObjectParameterSet</span></span>
```
Set-AzSignalRUpstream -InputObject <PSSignalRResource> [-AsJob] [-Template <PSUpstreamTemplate[]>] [-Clear]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="849ff-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="849ff-108">DESCRIPTION</span></span>
<span data-ttu-id="849ff-109">Definir as configurações upstream de um serviço de Sinalização.</span><span class="sxs-lookup"><span data-stu-id="849ff-109">Set the upstream settings of a SignalR service.</span></span>

## <span data-ttu-id="849ff-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="849ff-110">EXAMPLES</span></span>

### <span data-ttu-id="849ff-111">Definir dois modelos de upstream ordenados</span><span class="sxs-lookup"><span data-stu-id="849ff-111">Set two ordered upstream templates</span></span>
```powershell
PS C:\>  Set-AzSignalRUpstream -name pssignalr -ResourceGroupName test_resource_group -Template @{UrlTemplate='http://host-connections1.com'; HubPattern='chat';EventPattern='broadcast' }, @{UrlTemplate='http://host-connections2.com'}

Templates
---------
{Microsoft.Azure.Commands.SignalR.Models.PSUpstreamTemplate, Microsoft.Azure.Commands.SignalR.Models.PSUpstreamTemplat…
```

<span data-ttu-id="849ff-112">O seguinte JSON representa o conjunto real de modelos.</span><span class="sxs-lookup"><span data-stu-id="849ff-112">The following JSON represents the actual templates set.</span></span> 

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

### <span data-ttu-id="849ff-113">Limpar todas as configurações de upstream</span><span class="sxs-lookup"><span data-stu-id="849ff-113">Clear all the upstream settings</span></span>
```powershell
PS C:\>  Set-AzSignalRUpstream -name pssignalr -ResourceGroupName test_resource_group -Clear

Templates
---------
{}
```

## <span data-ttu-id="849ff-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="849ff-114">PARAMETERS</span></span>

### <span data-ttu-id="849ff-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="849ff-115">-AsJob</span></span>
<span data-ttu-id="849ff-116">Execute o cmdlet em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="849ff-116">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="849ff-117">-Limpar</span><span class="sxs-lookup"><span data-stu-id="849ff-117">-Clear</span></span>
<span data-ttu-id="849ff-118">Limpe todas as configurações de upstream.</span><span class="sxs-lookup"><span data-stu-id="849ff-118">Clear all the upstream settings.</span></span>

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

### <span data-ttu-id="849ff-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="849ff-119">-DefaultProfile</span></span>
<span data-ttu-id="849ff-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="849ff-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="849ff-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="849ff-121">-InputObject</span></span>
<span data-ttu-id="849ff-122">O objeto de recurso signalr.</span><span class="sxs-lookup"><span data-stu-id="849ff-122">The SignalR resource object.</span></span>

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

### <span data-ttu-id="849ff-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="849ff-123">-Name</span></span>
<span data-ttu-id="849ff-124">O nome do serviço de Sinalização.</span><span class="sxs-lookup"><span data-stu-id="849ff-124">The SignalR service name.</span></span>

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

### <span data-ttu-id="849ff-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="849ff-125">-ResourceGroupName</span></span>
<span data-ttu-id="849ff-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="849ff-126">The resource group name.</span></span>
<span data-ttu-id="849ff-127">O padrão será usado se não for especificado.</span><span class="sxs-lookup"><span data-stu-id="849ff-127">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="849ff-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="849ff-128">-ResourceId</span></span>
<span data-ttu-id="849ff-129">A ID do recurso de serviço de Sinalização.</span><span class="sxs-lookup"><span data-stu-id="849ff-129">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="849ff-130">-Modelo</span><span class="sxs-lookup"><span data-stu-id="849ff-130">-Template</span></span>
<span data-ttu-id="849ff-131">Itens de modelo para configurações upstream.</span><span class="sxs-lookup"><span data-stu-id="849ff-131">Template item(s) for upstream settings.</span></span>
<span data-ttu-id="849ff-132">Chave necessária: UrlTemplate.</span><span class="sxs-lookup"><span data-stu-id="849ff-132">Required key: UrlTemplate.</span></span>
<span data-ttu-id="849ff-133">Teclas opcionais: HubPattern, EventPattern, CategoryPattern.</span><span class="sxs-lookup"><span data-stu-id="849ff-133">Optional keys: HubPattern, EventPattern, CategoryPattern.</span></span>
<span data-ttu-id="849ff-134">Exemplo de como usar a sintaxe de aprovação para passar o parâmetro de modelos: @{UrlTemplate=' http://host-connections1.com ', HubPattern= 'chat'; EventPattern='broadcast' },@{UrlTemplate=' http://host-connections2.com '}</span><span class="sxs-lookup"><span data-stu-id="849ff-134">Example using splatting syntax to pass templates parameter: @{UrlTemplate='http://host-connections1.com', HubPattern= 'chat';EventPattern='broadcast' },@{UrlTemplate='http://host-connections2.com'}</span></span>

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

### <span data-ttu-id="849ff-135">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="849ff-135">-Confirm</span></span>
<span data-ttu-id="849ff-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="849ff-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="849ff-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="849ff-137">-WhatIf</span></span>
<span data-ttu-id="849ff-138">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="849ff-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="849ff-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="849ff-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="849ff-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="849ff-140">CommonParameters</span></span>
<span data-ttu-id="849ff-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="849ff-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="849ff-142">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="849ff-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="849ff-143">Entradas</span><span class="sxs-lookup"><span data-stu-id="849ff-143">INPUTS</span></span>

### <span data-ttu-id="849ff-144">System.String</span><span class="sxs-lookup"><span data-stu-id="849ff-144">System.String</span></span>

## <span data-ttu-id="849ff-145">Saídas</span><span class="sxs-lookup"><span data-stu-id="849ff-145">OUTPUTS</span></span>

### <span data-ttu-id="849ff-146">Microsoft.Azure.Commands.Signalr.Models.PSServerlessUpstreamSettings</span><span class="sxs-lookup"><span data-stu-id="849ff-146">Microsoft.Azure.Commands.SignalR.Models.PSServerlessUpstreamSettings</span></span>

## <span data-ttu-id="849ff-147">Notas</span><span class="sxs-lookup"><span data-stu-id="849ff-147">NOTES</span></span>

## <span data-ttu-id="849ff-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="849ff-148">RELATED LINKS</span></span>

[<span data-ttu-id="849ff-149">Como usar o splatting para passar parâmetros para comandos no PowerShell</span><span class="sxs-lookup"><span data-stu-id="849ff-149">How to use splatting to pass parameters to commands in PowerShell</span></span>](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.core/about/about_splatting?view=powershell-7)
