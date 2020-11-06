---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/new-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalR.md
ms.openlocfilehash: 8c8240ed1df30dface1bdb2ce0b649bacf17d08a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599093"
---
# <span data-ttu-id="d7d9a-101">New-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="d7d9a-101">New-AzSignalR</span></span>

## <span data-ttu-id="d7d9a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d7d9a-102">SYNOPSIS</span></span>
<span data-ttu-id="d7d9a-103">Criar um serviço de Sinaldor.</span><span class="sxs-lookup"><span data-stu-id="d7d9a-103">Create a SignalR service.</span></span>

## <span data-ttu-id="d7d9a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d7d9a-104">SYNTAX</span></span>

```
New-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-Location <String>] [-Sku <String>]
 [-UnitCount <Int32>] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7d9a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d7d9a-105">DESCRIPTION</span></span>
<span data-ttu-id="d7d9a-106">Criar um serviço de Sinaldor.</span><span class="sxs-lookup"><span data-stu-id="d7d9a-106">Create a SignalR service.</span></span>
<span data-ttu-id="d7d9a-107">Os seguintes valores serão usados para os parâmetros se não forem especificados:</span><span class="sxs-lookup"><span data-stu-id="d7d9a-107">The following values will be used for the parameters if not specified:</span></span>
* <span data-ttu-id="d7d9a-108">`ResourceGroupName`: o grupo de recursos padrão definido por `Set-AzDefault -ResourceGroupName` .</span><span class="sxs-lookup"><span data-stu-id="d7d9a-108">`ResourceGroupName`: the default resource group set by `Set-AzDefault -ResourceGroupName`.</span></span>
* <span data-ttu-id="d7d9a-109">`Location`: o local do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="d7d9a-109">`Location`: the location of the resource group</span></span>
* <span data-ttu-id="d7d9a-110">`Sku`: `Standard_S1`</span><span class="sxs-lookup"><span data-stu-id="d7d9a-110">`Sku`: `Standard_S1`</span></span>

## <span data-ttu-id="d7d9a-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d7d9a-111">EXAMPLES</span></span>

### <span data-ttu-id="d7d9a-112">Criar um envio de Signalr</span><span class="sxs-lookup"><span data-stu-id="d7d9a-112">Create a SignalR serivce</span></span>
```powershell
PS C:\> New-AzSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr1 -Location eastus -Sku Standard_S1

HostName                                           Location       ServerPort PublicPort ProvisioningState Version
--------                                           --------       ---------- ---------- ----------------- -------
mysignalr1.service.signalr.net                     eastus         5002       5001       Succeeded         1.0-preview
```

## <span data-ttu-id="d7d9a-113">OS</span><span class="sxs-lookup"><span data-stu-id="d7d9a-113">PARAMETERS</span></span>

### <span data-ttu-id="d7d9a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d7d9a-114">-AsJob</span></span>
<span data-ttu-id="d7d9a-115">Execute o cmdlet em plano de trabalho em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="d7d9a-115">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="d7d9a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7d9a-116">-DefaultProfile</span></span>
<span data-ttu-id="d7d9a-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d7d9a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7d9a-118">-Local</span><span class="sxs-lookup"><span data-stu-id="d7d9a-118">-Location</span></span>
<span data-ttu-id="d7d9a-119">O local do serviço de sinal de sinal.</span><span class="sxs-lookup"><span data-stu-id="d7d9a-119">The SignalR service location.</span></span> <span data-ttu-id="d7d9a-120">O local do grupo de recursos será usado se não for especificado.</span><span class="sxs-lookup"><span data-stu-id="d7d9a-120">The resource group location will be used if not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7d9a-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="d7d9a-121">-Name</span></span>
<span data-ttu-id="d7d9a-122">O nome do serviço do Signalr.</span><span class="sxs-lookup"><span data-stu-id="d7d9a-122">The SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7d9a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7d9a-123">-ResourceGroupName</span></span>
<span data-ttu-id="d7d9a-124">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d7d9a-124">The resource group name.</span></span> <span data-ttu-id="d7d9a-125">O padrão será usado se não for especificado.</span><span class="sxs-lookup"><span data-stu-id="d7d9a-125">The default one will be used if not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7d9a-126">-SKU</span><span class="sxs-lookup"><span data-stu-id="d7d9a-126">-Sku</span></span>
<span data-ttu-id="d7d9a-127">A SKU do serviço Signalr.</span><span class="sxs-lookup"><span data-stu-id="d7d9a-127">The SignalR service SKU.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Standard_S1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7d9a-128">-Marca</span><span class="sxs-lookup"><span data-stu-id="d7d9a-128">-Tag</span></span>
<span data-ttu-id="d7d9a-129">As marcas do serviço de Signalr.</span><span class="sxs-lookup"><span data-stu-id="d7d9a-129">The tags for the SignalR service.</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7d9a-130">-UnitCount</span><span class="sxs-lookup"><span data-stu-id="d7d9a-130">-UnitCount</span></span>
<span data-ttu-id="d7d9a-131">A contagem de unidade de serviço do Signalr, de 1 a 10.</span><span class="sxs-lookup"><span data-stu-id="d7d9a-131">The SignalR service unit count, from 1 to 10.</span></span> <span data-ttu-id="d7d9a-132">O padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="d7d9a-132">Default to 1.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7d9a-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d7d9a-133">-Confirm</span></span>
<span data-ttu-id="d7d9a-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7d9a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7d9a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7d9a-135">-WhatIf</span></span>
<span data-ttu-id="d7d9a-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d7d9a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7d9a-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d7d9a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7d9a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7d9a-138">CommonParameters</span></span>
<span data-ttu-id="d7d9a-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7d9a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7d9a-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7d9a-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7d9a-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d7d9a-141">INPUTS</span></span>

### <span data-ttu-id="d7d9a-142">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="d7d9a-142">None</span></span>

## <span data-ttu-id="d7d9a-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d7d9a-143">OUTPUTS</span></span>

### <span data-ttu-id="d7d9a-144">Microsoft. Azure. Commands. Signalr. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="d7d9a-144">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="d7d9a-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d7d9a-145">NOTES</span></span>

## <span data-ttu-id="d7d9a-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d7d9a-146">RELATED LINKS</span></span>
