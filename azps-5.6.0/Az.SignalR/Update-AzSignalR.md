---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/powershell/module/az.signalr/update-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalR.md
ms.openlocfilehash: d02db6e59c688a79b0088c3b3b42fde0cbc13bb8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885805"
---
# <span data-ttu-id="1f6bb-101">Update-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="1f6bb-101">Update-AzSignalR</span></span>

## <span data-ttu-id="1f6bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f6bb-102">SYNOPSIS</span></span>
<span data-ttu-id="1f6bb-103">Atualize um serviço SignalR.</span><span class="sxs-lookup"><span data-stu-id="1f6bb-103">Update a SignalR service.</span></span>

## <span data-ttu-id="1f6bb-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="1f6bb-104">SYNTAX</span></span>

### <span data-ttu-id="1f6bb-105">ResourceGroupParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="1f6bb-105">ResourceGroupParameterSet (Default)</span></span>
```
Update-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1f6bb-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f6bb-106">ResourceIdParameterSet</span></span>
```
Update-AzSignalR -ResourceId <String> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1f6bb-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f6bb-107">InputObjectParameterSet</span></span>
```
Update-AzSignalR -InputObject <PSSignalRResource> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1f6bb-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="1f6bb-108">DESCRIPTION</span></span>
<span data-ttu-id="1f6bb-109">Atualize um serviço SignalR.</span><span class="sxs-lookup"><span data-stu-id="1f6bb-109">Update a SignalR service.</span></span>
<span data-ttu-id="1f6bb-110">Os seguintes valores serão usados para os parâmetros se não for especificado:</span><span class="sxs-lookup"><span data-stu-id="1f6bb-110">The following values will be used for the parameters if not specified:</span></span>
* <span data-ttu-id="1f6bb-111">`ResourceGroupName`: o grupo de recursos padrão definido por `Set-AzDefault -ResourceGroupName` .</span><span class="sxs-lookup"><span data-stu-id="1f6bb-111">`ResourceGroupName`: the default resource group set by `Set-AzDefault -ResourceGroupName`.</span></span>
* <span data-ttu-id="1f6bb-112">`Sku`: `Standard_S1`</span><span class="sxs-lookup"><span data-stu-id="1f6bb-112">`Sku`: `Standard_S1`</span></span>

## <span data-ttu-id="1f6bb-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1f6bb-113">EXAMPLES</span></span>

### <span data-ttu-id="1f6bb-114">Atualize um serviço SignalR específico.</span><span class="sxs-lookup"><span data-stu-id="1f6bb-114">Update a specific SignalR service.</span></span>
```powershell
PS C:\> Update-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -UnitCount 5

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 5         Succeeded         1.0
```

### <span data-ttu-id="1f6bb-115">Especificar ServiceMode e AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="1f6bb-115">Specify ServiceMode and AllowedOrigin</span></span>
```powershell
PS C:\> Update-AzSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr2 -ServiceMode Serverless -AllowedOrigin http://example1.com:12345, https://example2.cn

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 1         Succeeded         1.0
```

## <span data-ttu-id="1f6bb-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="1f6bb-116">PARAMETERS</span></span>

### <span data-ttu-id="1f6bb-117">-AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="1f6bb-117">-AllowedOrigin</span></span>
<span data-ttu-id="1f6bb-118">As origens permitidas para o serviço SignalR.</span><span class="sxs-lookup"><span data-stu-id="1f6bb-118">The allowed origins for the SignalR service.</span></span> <span data-ttu-id="1f6bb-119">Para permitir tudo, use "\*" e remova todas as outras origens da lista.</span><span class="sxs-lookup"><span data-stu-id="1f6bb-119">To allow all, use "\*" and remove all other origins from the list.</span></span> <span data-ttu-id="1f6bb-120">As barras não são permitidas como parte do domínio ou após o TLD</span><span class="sxs-lookup"><span data-stu-id="1f6bb-120">Slashes are not allowed as part of domain or after TLD</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f6bb-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1f6bb-121">-AsJob</span></span>
<span data-ttu-id="1f6bb-122">Execute o cmdlet em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="1f6bb-122">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="1f6bb-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f6bb-123">-DefaultProfile</span></span>
<span data-ttu-id="1f6bb-124">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1f6bb-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f6bb-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1f6bb-125">-InputObject</span></span>
<span data-ttu-id="1f6bb-126">O objeto de recurso SignalR.</span><span class="sxs-lookup"><span data-stu-id="1f6bb-126">The SignalR resource object.</span></span>

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

### <span data-ttu-id="1f6bb-127">-Name</span><span class="sxs-lookup"><span data-stu-id="1f6bb-127">-Name</span></span>
<span data-ttu-id="1f6bb-128">O nome do serviço SignalR.</span><span class="sxs-lookup"><span data-stu-id="1f6bb-128">The SignalR service name.</span></span>

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

### <span data-ttu-id="1f6bb-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f6bb-129">-ResourceGroupName</span></span>
<span data-ttu-id="1f6bb-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1f6bb-130">The resource group name.</span></span>
<span data-ttu-id="1f6bb-131">O padrão será usado se não for especificado.</span><span class="sxs-lookup"><span data-stu-id="1f6bb-131">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="1f6bb-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1f6bb-132">-ResourceId</span></span>
<span data-ttu-id="1f6bb-133">A ID do recurso de serviço SignalR.</span><span class="sxs-lookup"><span data-stu-id="1f6bb-133">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="1f6bb-134">-ServiceMode</span><span class="sxs-lookup"><span data-stu-id="1f6bb-134">-ServiceMode</span></span>
<span data-ttu-id="1f6bb-135">O modo de serviço do serviço SignalR.</span><span class="sxs-lookup"><span data-stu-id="1f6bb-135">The service mode for the SignalR service.</span></span>

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

### <span data-ttu-id="1f6bb-136">-Sku</span><span class="sxs-lookup"><span data-stu-id="1f6bb-136">-Sku</span></span>
<span data-ttu-id="1f6bb-137">SKU do serviço SignalR.</span><span class="sxs-lookup"><span data-stu-id="1f6bb-137">The SignalR service SKU.</span></span>
<span data-ttu-id="1f6bb-138">Padrão para "Standard_S1".</span><span class="sxs-lookup"><span data-stu-id="1f6bb-138">Default to "Standard_S1".</span></span>

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

### <span data-ttu-id="1f6bb-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="1f6bb-139">-Tag</span></span>
<span data-ttu-id="1f6bb-140">As marcas do serviço SignalR.</span><span class="sxs-lookup"><span data-stu-id="1f6bb-140">The tags for the SignalR service.</span></span>

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

### <span data-ttu-id="1f6bb-141">-UnitCount</span><span class="sxs-lookup"><span data-stu-id="1f6bb-141">-UnitCount</span></span>
<span data-ttu-id="1f6bb-142">A contagem da unidade de serviço signalr, valor somente de {1, 2, 5, 10, 20, 50, 100}.</span><span class="sxs-lookup"><span data-stu-id="1f6bb-142">The SignalR service unit count, value only from {1, 2, 5, 10, 20, 50, 100}.</span></span>
<span data-ttu-id="1f6bb-143">Padrão para 1.</span><span class="sxs-lookup"><span data-stu-id="1f6bb-143">Default to 1.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f6bb-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1f6bb-144">-Confirm</span></span>
<span data-ttu-id="1f6bb-145">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f6bb-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f6bb-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f6bb-146">-WhatIf</span></span>
<span data-ttu-id="1f6bb-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1f6bb-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f6bb-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1f6bb-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f6bb-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f6bb-149">CommonParameters</span></span>
<span data-ttu-id="1f6bb-150">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f6bb-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f6bb-151">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1f6bb-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f6bb-152">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1f6bb-152">INPUTS</span></span>

### <span data-ttu-id="1f6bb-153">System.String</span><span class="sxs-lookup"><span data-stu-id="1f6bb-153">System.String</span></span>

### <span data-ttu-id="1f6bb-154">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="1f6bb-154">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="1f6bb-155">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="1f6bb-155">OUTPUTS</span></span>

### <span data-ttu-id="1f6bb-156">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="1f6bb-156">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="1f6bb-157">NOTES</span><span class="sxs-lookup"><span data-stu-id="1f6bb-157">NOTES</span></span>

## <span data-ttu-id="1f6bb-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1f6bb-158">RELATED LINKS</span></span>
