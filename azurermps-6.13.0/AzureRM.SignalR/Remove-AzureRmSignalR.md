---
external help file: Microsoft.Azure.Commands.SignalR.dll-Help.xml
Module Name: AzureRM.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.signalr/new-azurermsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/Remove-AzureRmSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SignalR/Commands.SignalR/help/Remove-AzureRmSignalR.md
ms.openlocfilehash: 5fcf62e592ed1e842c3dc6f4be21462170c4f83b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430838"
---
# <span data-ttu-id="d874b-101">Remove-AzureRmSignalR</span><span class="sxs-lookup"><span data-stu-id="d874b-101">Remove-AzureRmSignalR</span></span>

## <span data-ttu-id="d874b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d874b-102">SYNOPSIS</span></span>
<span data-ttu-id="d874b-103">Remover um serviço de sinal de sinal.</span><span class="sxs-lookup"><span data-stu-id="d874b-103">Remove a SignalR service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d874b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d874b-104">SYNTAX</span></span>

### <span data-ttu-id="d874b-105">ResourceGroupParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="d874b-105">ResourceGroupParameterSet (Default)</span></span>
```
Remove-AzureRmSignalR [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d874b-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d874b-106">ResourceIdParameterSet</span></span>
```
Remove-AzureRmSignalR -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d874b-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d874b-107">InputObjectParameterSet</span></span>
```
Remove-AzureRmSignalR -InputObject <PSSignalRResource> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d874b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d874b-108">DESCRIPTION</span></span>
<span data-ttu-id="d874b-109">Remover um serviço de sinal de sinal.</span><span class="sxs-lookup"><span data-stu-id="d874b-109">Remove a SignalR service.</span></span>

## <span data-ttu-id="d874b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d874b-110">EXAMPLES</span></span>

### <span data-ttu-id="d874b-111">Remover um serviço de sinal de sinal</span><span class="sxs-lookup"><span data-stu-id="d874b-111">Remove a SignalR service</span></span>
```powershell
PS C:\> Remove-AzureRmSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -PassThru

True
```

### <span data-ttu-id="d874b-112">Remover todos os serviços de sinal da conexão</span><span class="sxs-lookup"><span data-stu-id="d874b-112">Remove all SignalR service from pipe</span></span>
```powershell
PS C:\> Get-AzureRmSignalR -ResourceGroupName myResourceGroup | Remove-AzureRmSignalR
```

## <span data-ttu-id="d874b-113">OS</span><span class="sxs-lookup"><span data-stu-id="d874b-113">PARAMETERS</span></span>

### <span data-ttu-id="d874b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d874b-114">-AsJob</span></span>
<span data-ttu-id="d874b-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="d874b-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d874b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d874b-116">-DefaultProfile</span></span>
<span data-ttu-id="d874b-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d874b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d874b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d874b-118">-InputObject</span></span>
<span data-ttu-id="d874b-119">O objeto de recurso Signalr.</span><span class="sxs-lookup"><span data-stu-id="d874b-119">The SignalR resource object.</span></span>

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

### <span data-ttu-id="d874b-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="d874b-120">-Name</span></span>
<span data-ttu-id="d874b-121">Nome do serviço de sinal de sinal.</span><span class="sxs-lookup"><span data-stu-id="d874b-121">SignalR service name.</span></span>

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

### <span data-ttu-id="d874b-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d874b-122">-PassThru</span></span>
<span data-ttu-id="d874b-123">Retorna verdadeiro se a remoção for concluída com êxito.</span><span class="sxs-lookup"><span data-stu-id="d874b-123">Returns true if the removal was completed successfully.</span></span>

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

### <span data-ttu-id="d874b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d874b-124">-ResourceGroupName</span></span>
<span data-ttu-id="d874b-125">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d874b-125">Resource group name.</span></span>

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

### <span data-ttu-id="d874b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d874b-126">-ResourceId</span></span>
<span data-ttu-id="d874b-127">A ID de recurso do serviço Signalr.</span><span class="sxs-lookup"><span data-stu-id="d874b-127">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="d874b-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d874b-128">-Confirm</span></span>
<span data-ttu-id="d874b-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d874b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d874b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d874b-130">-WhatIf</span></span>
<span data-ttu-id="d874b-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d874b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d874b-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d874b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d874b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d874b-133">CommonParameters</span></span>
<span data-ttu-id="d874b-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d874b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d874b-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d874b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d874b-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d874b-136">INPUTS</span></span>

### <span data-ttu-id="d874b-137">System. String</span><span class="sxs-lookup"><span data-stu-id="d874b-137">System.String</span></span>
<span data-ttu-id="d874b-138">Parâmetros: ResourceId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d874b-138">Parameters: ResourceId (ByValue)</span></span>

### <span data-ttu-id="d874b-139">Microsoft. Azure. Commands. Signalr. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="d874b-139">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
<span data-ttu-id="d874b-140">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d874b-140">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="d874b-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d874b-141">OUTPUTS</span></span>

### <span data-ttu-id="d874b-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d874b-142">System.Boolean</span></span>

## <span data-ttu-id="d874b-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d874b-143">NOTES</span></span>

## <span data-ttu-id="d874b-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d874b-144">RELATED LINKS</span></span>
