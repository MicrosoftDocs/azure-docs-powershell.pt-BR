---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/restart-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Restart-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Restart-AzSignalR.md
ms.openlocfilehash: ea5de8ddd36d315381d4f60ee0fa1ce7dc49adc2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98428729"
---
# <span data-ttu-id="b6450-101">Restart-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="b6450-101">Restart-AzSignalR</span></span>

## <span data-ttu-id="b6450-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b6450-102">SYNOPSIS</span></span>
<span data-ttu-id="b6450-103">Reinicie um serviço de sinal de sinal.</span><span class="sxs-lookup"><span data-stu-id="b6450-103">Restart a SignalR service.</span></span>

## <span data-ttu-id="b6450-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b6450-104">SYNTAX</span></span>

### <span data-ttu-id="b6450-105">ResourceGroupParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="b6450-105">ResourceGroupParameterSet (Default)</span></span>
```
Restart-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6450-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6450-106">ResourceIdParameterSet</span></span>
```
Restart-AzSignalR -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6450-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b6450-107">InputObjectParameterSet</span></span>
```
Restart-AzSignalR -InputObject <PSSignalRResource> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6450-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b6450-108">DESCRIPTION</span></span>
<span data-ttu-id="b6450-109">Reinicie um serviço de sinal de sinal.</span><span class="sxs-lookup"><span data-stu-id="b6450-109">Restart a SignalR service.</span></span>

## <span data-ttu-id="b6450-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b6450-110">EXAMPLES</span></span>

### <span data-ttu-id="b6450-111">Reiniciar um serviço de sinal específico</span><span class="sxs-lookup"><span data-stu-id="b6450-111">Restart a specific SignalR service</span></span>
```powershell
PS C:\> Restart-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -PassThru

True
```

<span data-ttu-id="b6450-112">O grupo de recursos padrão pode ser definido por \` set-AzDefault-ResourceGroupName MyResource Group \` .</span><span class="sxs-lookup"><span data-stu-id="b6450-112">The default resource group can be set by \`Set-AzDefault -ResourceGroupName myResourceGroup\`.</span></span>

## <span data-ttu-id="b6450-113">OS</span><span class="sxs-lookup"><span data-stu-id="b6450-113">PARAMETERS</span></span>

### <span data-ttu-id="b6450-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b6450-114">-AsJob</span></span>
<span data-ttu-id="b6450-115">Execute o cmdlet em plano de trabalho em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="b6450-115">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="b6450-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6450-116">-DefaultProfile</span></span>
<span data-ttu-id="b6450-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b6450-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6450-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b6450-118">-InputObject</span></span>
<span data-ttu-id="b6450-119">O objeto de recurso Signalr.</span><span class="sxs-lookup"><span data-stu-id="b6450-119">The SignalR resource object.</span></span>

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

### <span data-ttu-id="b6450-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="b6450-120">-Name</span></span>
<span data-ttu-id="b6450-121">O nome do serviço do Signalr.</span><span class="sxs-lookup"><span data-stu-id="b6450-121">The SignalR service name.</span></span>

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

### <span data-ttu-id="b6450-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b6450-122">-PassThru</span></span>
<span data-ttu-id="b6450-123">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="b6450-123">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="b6450-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6450-124">-ResourceGroupName</span></span>
<span data-ttu-id="b6450-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b6450-125">The resource group name.</span></span>
<span data-ttu-id="b6450-126">O padrão será usado se não for especificado.</span><span class="sxs-lookup"><span data-stu-id="b6450-126">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="b6450-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b6450-127">-ResourceId</span></span>
<span data-ttu-id="b6450-128">A ID de recurso do serviço Signalr.</span><span class="sxs-lookup"><span data-stu-id="b6450-128">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="b6450-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b6450-129">-Confirm</span></span>
<span data-ttu-id="b6450-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6450-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6450-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6450-131">-WhatIf</span></span>
<span data-ttu-id="b6450-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b6450-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6450-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b6450-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6450-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6450-134">CommonParameters</span></span>
<span data-ttu-id="b6450-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6450-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6450-136">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b6450-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6450-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b6450-137">INPUTS</span></span>

### <span data-ttu-id="b6450-138">System. String</span><span class="sxs-lookup"><span data-stu-id="b6450-138">System.String</span></span>

### <span data-ttu-id="b6450-139">Microsoft. Azure. Commands. Signalr. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="b6450-139">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="b6450-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b6450-140">OUTPUTS</span></span>

### <span data-ttu-id="b6450-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b6450-141">System.Boolean</span></span>

## <span data-ttu-id="b6450-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b6450-142">NOTES</span></span>

## <span data-ttu-id="b6450-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b6450-143">RELATED LINKS</span></span>
