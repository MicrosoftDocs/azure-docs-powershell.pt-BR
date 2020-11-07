---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/remove-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Remove-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Remove-AzSignalR.md
ms.openlocfilehash: 075c8e7604ab800e8f1065ff4d025b105d8effc3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772401"
---
# <span data-ttu-id="60814-101">Remove-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="60814-101">Remove-AzSignalR</span></span>

## <span data-ttu-id="60814-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="60814-102">SYNOPSIS</span></span>
<span data-ttu-id="60814-103">Remover um serviço de sinal de sinal.</span><span class="sxs-lookup"><span data-stu-id="60814-103">Remove a SignalR service.</span></span>

## <span data-ttu-id="60814-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="60814-104">SYNTAX</span></span>

### <span data-ttu-id="60814-105">ResourceGroupParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="60814-105">ResourceGroupParameterSet (Default)</span></span>
```
Remove-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60814-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="60814-106">ResourceIdParameterSet</span></span>
```
Remove-AzSignalR -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60814-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="60814-107">InputObjectParameterSet</span></span>
```
Remove-AzSignalR -InputObject <PSSignalRResource> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60814-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="60814-108">DESCRIPTION</span></span>
<span data-ttu-id="60814-109">Remover um serviço de sinal de sinal.</span><span class="sxs-lookup"><span data-stu-id="60814-109">Remove a SignalR service.</span></span>

## <span data-ttu-id="60814-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="60814-110">EXAMPLES</span></span>

### <span data-ttu-id="60814-111">Remover um serviço de sinal de sinal</span><span class="sxs-lookup"><span data-stu-id="60814-111">Remove a SignalR service</span></span>
```
PS C:\> Remove-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -PassThru

True
```

### <span data-ttu-id="60814-112">Remover todos os serviços de sinal da conexão</span><span class="sxs-lookup"><span data-stu-id="60814-112">Remove all SignalR service from pipe</span></span>
```
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup | Remove-AzSignalR
```

## <span data-ttu-id="60814-113">OS</span><span class="sxs-lookup"><span data-stu-id="60814-113">PARAMETERS</span></span>

### <span data-ttu-id="60814-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="60814-114">-AsJob</span></span>
<span data-ttu-id="60814-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="60814-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60814-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60814-116">-DefaultProfile</span></span>
<span data-ttu-id="60814-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="60814-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60814-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="60814-118">-InputObject</span></span>
<span data-ttu-id="60814-119">O objeto de recurso Signalr.</span><span class="sxs-lookup"><span data-stu-id="60814-119">The SignalR resource object.</span></span>

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

### <span data-ttu-id="60814-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="60814-120">-Name</span></span>
<span data-ttu-id="60814-121">Nome do serviço de sinal de sinal.</span><span class="sxs-lookup"><span data-stu-id="60814-121">SignalR service name.</span></span>

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

### <span data-ttu-id="60814-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="60814-122">-PassThru</span></span>
<span data-ttu-id="60814-123">Retorna verdadeiro se a remoção for concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="60814-123">Returns true if the removal was completed successfully.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60814-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60814-124">-ResourceGroupName</span></span>
<span data-ttu-id="60814-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="60814-125">Resource group name.</span></span>

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

### <span data-ttu-id="60814-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="60814-126">-ResourceId</span></span>
<span data-ttu-id="60814-127">A ID de recurso do serviço Signalr.</span><span class="sxs-lookup"><span data-stu-id="60814-127">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60814-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="60814-128">-Confirm</span></span>
<span data-ttu-id="60814-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60814-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60814-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60814-130">-WhatIf</span></span>
<span data-ttu-id="60814-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="60814-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60814-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="60814-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60814-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60814-133">CommonParameters</span></span>
<span data-ttu-id="60814-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60814-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60814-135">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="60814-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60814-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="60814-136">INPUTS</span></span>

### <span data-ttu-id="60814-137">System. String</span><span class="sxs-lookup"><span data-stu-id="60814-137">System.String</span></span>
### <span data-ttu-id="60814-138">Microsoft. Azure. Commands. Signalr. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="60814-138">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="60814-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="60814-139">OUTPUTS</span></span>

### <span data-ttu-id="60814-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="60814-140">System.Boolean</span></span>
## <span data-ttu-id="60814-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="60814-141">NOTES</span></span>

## <span data-ttu-id="60814-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="60814-142">RELATED LINKS</span></span>