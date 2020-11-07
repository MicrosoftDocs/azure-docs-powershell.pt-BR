---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/update-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Update-AzSignalR.md
ms.openlocfilehash: 52e422f6c86f17c6620c58c1034b45250d4edf08
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93941282"
---
# <span data-ttu-id="ecd26-101">Update-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="ecd26-101">Update-AzSignalR</span></span>

## <span data-ttu-id="ecd26-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ecd26-102">SYNOPSIS</span></span>
<span data-ttu-id="ecd26-103">Atualizar um serviço de sinal.</span><span class="sxs-lookup"><span data-stu-id="ecd26-103">Update a SignalR service.</span></span>

## <span data-ttu-id="ecd26-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ecd26-104">SYNTAX</span></span>

### <span data-ttu-id="ecd26-105">ResourceGroupParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="ecd26-105">ResourceGroupParameterSet (Default)</span></span>
```
Update-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ecd26-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ecd26-106">ResourceIdParameterSet</span></span>
```
Update-AzSignalR -ResourceId <String> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ecd26-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ecd26-107">InputObjectParameterSet</span></span>
```
Update-AzSignalR -InputObject <PSSignalRResource> [-Sku <String>] [-UnitCount <Int32>]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>] [-ServiceMode <String>]
 [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ecd26-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ecd26-108">DESCRIPTION</span></span>
<span data-ttu-id="ecd26-109">Atualizar um serviço de sinal.</span><span class="sxs-lookup"><span data-stu-id="ecd26-109">Update a SignalR service.</span></span>
<span data-ttu-id="ecd26-110">Os seguintes valores serão usados para os parâmetros se não forem especificados:</span><span class="sxs-lookup"><span data-stu-id="ecd26-110">The following values will be used for the parameters if not specified:</span></span>
* <span data-ttu-id="ecd26-111">`ResourceGroupName`: o grupo de recursos padrão definido por `Set-AzDefault -ResourceGroupName` .</span><span class="sxs-lookup"><span data-stu-id="ecd26-111">`ResourceGroupName`: the default resource group set by `Set-AzDefault -ResourceGroupName`.</span></span>
* <span data-ttu-id="ecd26-112">`Sku`: `Standard_S1`</span><span class="sxs-lookup"><span data-stu-id="ecd26-112">`Sku`: `Standard_S1`</span></span>

## <span data-ttu-id="ecd26-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ecd26-113">EXAMPLES</span></span>

### <span data-ttu-id="ecd26-114">Atualize um serviço de sinal específico.</span><span class="sxs-lookup"><span data-stu-id="ecd26-114">Update a specific SignalR service.</span></span>
```powershell
PS C:\> Update-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -UnitCount 5

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 5         Succeeded         1.0
```

### <span data-ttu-id="ecd26-115">Especificar Servicemode e AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="ecd26-115">Specify ServiceMode and AllowedOrigin</span></span>
```powershell
PS C:\> Update-AzSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr2 -ServiceMode Serverless -AllowedOrigin http://example1.com:12345, https://example2.cn

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 1         Succeeded         1.0
```

## <span data-ttu-id="ecd26-116">OS</span><span class="sxs-lookup"><span data-stu-id="ecd26-116">PARAMETERS</span></span>

### <span data-ttu-id="ecd26-117">-AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="ecd26-117">-AllowedOrigin</span></span>
<span data-ttu-id="ecd26-118">As origens permitidas para o serviço de Signalr.</span><span class="sxs-lookup"><span data-stu-id="ecd26-118">The allowed origins for the SignalR service.</span></span> <span data-ttu-id="ecd26-119">Para permitir tudo, use "\*" e remova todas as outras origens da lista.</span><span class="sxs-lookup"><span data-stu-id="ecd26-119">To allow all, use "\*" and remove all other origins from the list.</span></span> <span data-ttu-id="ecd26-120">Barras não são permitidas como parte do domínio ou após TLD</span><span class="sxs-lookup"><span data-stu-id="ecd26-120">Slashes are not allowed as part of domain or after TLD</span></span>

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

### <span data-ttu-id="ecd26-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ecd26-121">-AsJob</span></span>
<span data-ttu-id="ecd26-122">Execute o cmdlet em plano de trabalho em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="ecd26-122">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="ecd26-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecd26-123">-DefaultProfile</span></span>
<span data-ttu-id="ecd26-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ecd26-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ecd26-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ecd26-125">-InputObject</span></span>
<span data-ttu-id="ecd26-126">O objeto de recurso Signalr.</span><span class="sxs-lookup"><span data-stu-id="ecd26-126">The SignalR resource object.</span></span>

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

### <span data-ttu-id="ecd26-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="ecd26-127">-Name</span></span>
<span data-ttu-id="ecd26-128">O nome do serviço do Signalr.</span><span class="sxs-lookup"><span data-stu-id="ecd26-128">The SignalR service name.</span></span>

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

### <span data-ttu-id="ecd26-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecd26-129">-ResourceGroupName</span></span>
<span data-ttu-id="ecd26-130">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ecd26-130">The resource group name.</span></span>
<span data-ttu-id="ecd26-131">O padrão será usado se não for especificado.</span><span class="sxs-lookup"><span data-stu-id="ecd26-131">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="ecd26-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ecd26-132">-ResourceId</span></span>
<span data-ttu-id="ecd26-133">A ID de recurso do serviço Signalr.</span><span class="sxs-lookup"><span data-stu-id="ecd26-133">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="ecd26-134">-Serviçomode</span><span class="sxs-lookup"><span data-stu-id="ecd26-134">-ServiceMode</span></span>
<span data-ttu-id="ecd26-135">O modo de serviço para o serviço de Signalr.</span><span class="sxs-lookup"><span data-stu-id="ecd26-135">The service mode for the SignalR service.</span></span>

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

### <span data-ttu-id="ecd26-136">-SKU</span><span class="sxs-lookup"><span data-stu-id="ecd26-136">-Sku</span></span>
<span data-ttu-id="ecd26-137">A SKU do serviço Signalr.</span><span class="sxs-lookup"><span data-stu-id="ecd26-137">The SignalR service SKU.</span></span>
<span data-ttu-id="ecd26-138">Padrão para "Standard_S1".</span><span class="sxs-lookup"><span data-stu-id="ecd26-138">Default to "Standard_S1".</span></span>

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

### <span data-ttu-id="ecd26-139">-Marca</span><span class="sxs-lookup"><span data-stu-id="ecd26-139">-Tag</span></span>
<span data-ttu-id="ecd26-140">As marcas do serviço de Signalr.</span><span class="sxs-lookup"><span data-stu-id="ecd26-140">The tags for the SignalR service.</span></span>

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

### <span data-ttu-id="ecd26-141">-UnitCount</span><span class="sxs-lookup"><span data-stu-id="ecd26-141">-UnitCount</span></span>
<span data-ttu-id="ecd26-142">A contagem de unidade de serviço do Signalr, valor apenas de {1, 2, 5, 10, 20, 50, 100}.</span><span class="sxs-lookup"><span data-stu-id="ecd26-142">The SignalR service unit count, value only from {1, 2, 5, 10, 20, 50, 100}.</span></span>
<span data-ttu-id="ecd26-143">O padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="ecd26-143">Default to 1.</span></span>

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

### <span data-ttu-id="ecd26-144">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ecd26-144">-Confirm</span></span>
<span data-ttu-id="ecd26-145">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ecd26-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecd26-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecd26-146">-WhatIf</span></span>
<span data-ttu-id="ecd26-147">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ecd26-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecd26-148">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ecd26-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecd26-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecd26-149">CommonParameters</span></span>
<span data-ttu-id="ecd26-150">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecd26-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecd26-151">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ecd26-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecd26-152">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ecd26-152">INPUTS</span></span>

### <span data-ttu-id="ecd26-153">System. String</span><span class="sxs-lookup"><span data-stu-id="ecd26-153">System.String</span></span>

### <span data-ttu-id="ecd26-154">Microsoft. Azure. Commands. Signalr. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="ecd26-154">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="ecd26-155">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ecd26-155">OUTPUTS</span></span>

### <span data-ttu-id="ecd26-156">Microsoft. Azure. Commands. Signalr. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="ecd26-156">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="ecd26-157">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ecd26-157">NOTES</span></span>

## <span data-ttu-id="ecd26-158">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ecd26-158">RELATED LINKS</span></span>
