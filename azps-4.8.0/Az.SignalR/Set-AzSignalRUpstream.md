---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/set-azsignalrupstream
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Set-AzSignalRUpstream.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Set-AzSignalRUpstream.md
ms.openlocfilehash: e04e87067f86f529117512e7443118f308b20547
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93956209"
---
# <span data-ttu-id="fa1a5-101">Set-AzSignalRUpstream</span><span class="sxs-lookup"><span data-stu-id="fa1a5-101">Set-AzSignalRUpstream</span></span>

## <span data-ttu-id="fa1a5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fa1a5-102">SYNOPSIS</span></span>
<span data-ttu-id="fa1a5-103">Definir as configurações de upstream de um serviço de sinal.</span><span class="sxs-lookup"><span data-stu-id="fa1a5-103">Set the upstream settings of a SignalR service.</span></span>

## <span data-ttu-id="fa1a5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fa1a5-104">SYNTAX</span></span>

### <span data-ttu-id="fa1a5-105">ResourceGroupParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="fa1a5-105">ResourceGroupParameterSet (Default)</span></span>
```
Set-AzSignalRUpstream [-ResourceGroupName <String>] [-Name] <String> [-AsJob]
 [-Template <PSUpstreamTemplate[]>] [-Clear] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fa1a5-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa1a5-106">ResourceIdParameterSet</span></span>
```
Set-AzSignalRUpstream -ResourceId <String> [-AsJob] [-Template <PSUpstreamTemplate[]>] [-Clear]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa1a5-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa1a5-107">InputObjectParameterSet</span></span>
```
Set-AzSignalRUpstream -InputObject <PSSignalRResource> [-AsJob] [-Template <PSUpstreamTemplate[]>] [-Clear]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa1a5-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fa1a5-108">DESCRIPTION</span></span>
<span data-ttu-id="fa1a5-109">Definir as configurações de upstream de um serviço de sinal.</span><span class="sxs-lookup"><span data-stu-id="fa1a5-109">Set the upstream settings of a SignalR service.</span></span>

## <span data-ttu-id="fa1a5-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fa1a5-110">EXAMPLES</span></span>

### <span data-ttu-id="fa1a5-111">Definir dois modelos de upstream ordenados</span><span class="sxs-lookup"><span data-stu-id="fa1a5-111">Set two ordered upstream templates</span></span>
```powershell
PS C:\>  Set-AzSignalRUpstream -name pssignalr -ResourceGroupName test_resource_group -Template @{UrlTemplate='http://host-connections1.com'; HubPattern='chat';EventPattern='broadcast' }, @{UrlTemplate='http://host-connections2.com'}

Templates
---------
{Microsoft.Azure.Commands.SignalR.Models.PSUpstreamTemplate, Microsoft.Azure.Commands.SignalR.Models.PSUpstreamTemplat…
```

<span data-ttu-id="fa1a5-112">O JSON a seguir representa os modelos reais definidos.</span><span class="sxs-lookup"><span data-stu-id="fa1a5-112">The following JSON represents the actual templates set.</span></span> 

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

### <span data-ttu-id="fa1a5-113">Limpar todas as configurações de upstream</span><span class="sxs-lookup"><span data-stu-id="fa1a5-113">Clear all the upstream settings</span></span>
```powershell
PS C:\>  Set-AzSignalRUpstream -name pssignalr -ResourceGroupName test_resource_group -Clear

Templates
---------
{}
```

## <span data-ttu-id="fa1a5-114">OS</span><span class="sxs-lookup"><span data-stu-id="fa1a5-114">PARAMETERS</span></span>

### <span data-ttu-id="fa1a5-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fa1a5-115">-AsJob</span></span>
<span data-ttu-id="fa1a5-116">Execute o cmdlet em plano de trabalho em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="fa1a5-116">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="fa1a5-117">-Limpar</span><span class="sxs-lookup"><span data-stu-id="fa1a5-117">-Clear</span></span>
<span data-ttu-id="fa1a5-118">Desmarque todas as configurações de upstream.</span><span class="sxs-lookup"><span data-stu-id="fa1a5-118">Clear all the upstream settings.</span></span>

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

### <span data-ttu-id="fa1a5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa1a5-119">-DefaultProfile</span></span>
<span data-ttu-id="fa1a5-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fa1a5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa1a5-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fa1a5-121">-InputObject</span></span>
<span data-ttu-id="fa1a5-122">O objeto de recurso Signalr.</span><span class="sxs-lookup"><span data-stu-id="fa1a5-122">The SignalR resource object.</span></span>

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

### <span data-ttu-id="fa1a5-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="fa1a5-123">-Name</span></span>
<span data-ttu-id="fa1a5-124">O nome do serviço do Signalr.</span><span class="sxs-lookup"><span data-stu-id="fa1a5-124">The SignalR service name.</span></span>

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

### <span data-ttu-id="fa1a5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa1a5-125">-ResourceGroupName</span></span>
<span data-ttu-id="fa1a5-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fa1a5-126">The resource group name.</span></span>
<span data-ttu-id="fa1a5-127">O padrão será usado se não for especificado.</span><span class="sxs-lookup"><span data-stu-id="fa1a5-127">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="fa1a5-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fa1a5-128">-ResourceId</span></span>
<span data-ttu-id="fa1a5-129">A ID de recurso do serviço Signalr.</span><span class="sxs-lookup"><span data-stu-id="fa1a5-129">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="fa1a5-130">-Modelo</span><span class="sxs-lookup"><span data-stu-id="fa1a5-130">-Template</span></span>
<span data-ttu-id="fa1a5-131">Item (ns) de modelo para configurações de upstream.</span><span class="sxs-lookup"><span data-stu-id="fa1a5-131">Template item(s) for upstream settings.</span></span>
<span data-ttu-id="fa1a5-132">Chave necessária: UrlTemplate.</span><span class="sxs-lookup"><span data-stu-id="fa1a5-132">Required key: UrlTemplate.</span></span>
<span data-ttu-id="fa1a5-133">Chaves opcionais: HubPattern, EventPattern, CategoryPattern.</span><span class="sxs-lookup"><span data-stu-id="fa1a5-133">Optional keys: HubPattern, EventPattern, CategoryPattern.</span></span>
<span data-ttu-id="fa1a5-134">Exemplo usando a sintaxe splatting para transmitir o parâmetro templates: @ {UrlTemplate = ' http://host-connections1.com ', HubPattern = ' chat '; EventPattern = "transmissão"}, @ {UrlTemplate = " http://host-connections2.com "}</span><span class="sxs-lookup"><span data-stu-id="fa1a5-134">Example using splatting syntax to pass templates parameter: @{UrlTemplate='http://host-connections1.com', HubPattern= 'chat';EventPattern='broadcast' },@{UrlTemplate='http://host-connections2.com'}</span></span>

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

### <span data-ttu-id="fa1a5-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fa1a5-135">-Confirm</span></span>
<span data-ttu-id="fa1a5-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa1a5-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa1a5-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa1a5-137">-WhatIf</span></span>
<span data-ttu-id="fa1a5-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fa1a5-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa1a5-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fa1a5-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa1a5-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa1a5-140">CommonParameters</span></span>
<span data-ttu-id="fa1a5-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa1a5-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa1a5-142">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fa1a5-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa1a5-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fa1a5-143">INPUTS</span></span>

### <span data-ttu-id="fa1a5-144">System. String</span><span class="sxs-lookup"><span data-stu-id="fa1a5-144">System.String</span></span>

## <span data-ttu-id="fa1a5-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fa1a5-145">OUTPUTS</span></span>

### <span data-ttu-id="fa1a5-146">Microsoft. Azure. Commands. Signalr. Models. PSServerlessUpstreamSettings</span><span class="sxs-lookup"><span data-stu-id="fa1a5-146">Microsoft.Azure.Commands.SignalR.Models.PSServerlessUpstreamSettings</span></span>

## <span data-ttu-id="fa1a5-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fa1a5-147">NOTES</span></span>

## <span data-ttu-id="fa1a5-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fa1a5-148">RELATED LINKS</span></span>

[<span data-ttu-id="fa1a5-149">Como usar o splatting para passar parâmetros para comandos no PowerShell</span><span class="sxs-lookup"><span data-stu-id="fa1a5-149">How to use splatting to pass parameters to commands in PowerShell</span></span>](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.core/about/about_splatting?view=powershell-7)
