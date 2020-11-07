---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/new-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalR.md
ms.openlocfilehash: 0f393a6442732e1f25edc6d6192bd6cf0a926a55
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772405"
---
# <span data-ttu-id="fd929-101">New-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="fd929-101">New-AzSignalR</span></span>

## <span data-ttu-id="fd929-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fd929-102">SYNOPSIS</span></span>
<span data-ttu-id="fd929-103">Criar um serviço de Sinaldor.</span><span class="sxs-lookup"><span data-stu-id="fd929-103">Create a SignalR service.</span></span>

## <span data-ttu-id="fd929-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fd929-104">SYNTAX</span></span>

```
New-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-Location <String>] [-Sku <String>]
 [-UnitCount <Int32>] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-ServiceMode <String>] [-AllowedOrigin <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd929-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fd929-105">DESCRIPTION</span></span>
<span data-ttu-id="fd929-106">Criar um serviço de Sinaldor.</span><span class="sxs-lookup"><span data-stu-id="fd929-106">Create a SignalR service.</span></span>
<span data-ttu-id="fd929-107">Os seguintes valores serão usados para os parâmetros se não forem especificados:</span><span class="sxs-lookup"><span data-stu-id="fd929-107">The following values will be used for the parameters if not specified:</span></span>
* <span data-ttu-id="fd929-108">`ResourceGroupName`: o grupo de recursos padrão definido por `Set-AzDefault -ResourceGroupName` .</span><span class="sxs-lookup"><span data-stu-id="fd929-108">`ResourceGroupName`: the default resource group set by `Set-AzDefault -ResourceGroupName`.</span></span>
* <span data-ttu-id="fd929-109">`Location`: o local do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="fd929-109">`Location`: the location of the resource group</span></span>
* <span data-ttu-id="fd929-110">`Sku`: `Standard_S1`</span><span class="sxs-lookup"><span data-stu-id="fd929-110">`Sku`: `Standard_S1`</span></span>

## <span data-ttu-id="fd929-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fd929-111">EXAMPLES</span></span>

### <span data-ttu-id="fd929-112">Criar um serviço de Sinaldor</span><span class="sxs-lookup"><span data-stu-id="fd929-112">Create a SignalR service</span></span>
```powershell
PS C:\> New-AzSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr1 -Location eastus -Sku Standard_S1 -UnitCount 5

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 5         Succeeded         1.0
```

### <span data-ttu-id="fd929-113">Especificar Servicemode e AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="fd929-113">Specify ServiceMode and AllowedOrigin</span></span>
```powershell
PS C:\> New-AzSignalR -ResourceGroupName myResourceGroup1 -Name mysignalr2 -Location eastus -ServiceMode Serverless -AllowedOrigin http://example1.com:12345, https://example2.cn

HostName                                 Location       ExternalIp      Sku         UnitCount ProvisioningState Version
--------                                 --------       ----------      ---         --------- ----------------- -------
mysignalr1.service.signalr.net           eastus         52.179.3.5      Standard_S1 1         Succeeded         1.0
```

## <span data-ttu-id="fd929-114">OS</span><span class="sxs-lookup"><span data-stu-id="fd929-114">PARAMETERS</span></span>

### <span data-ttu-id="fd929-115">-AllowedOrigin</span><span class="sxs-lookup"><span data-stu-id="fd929-115">-AllowedOrigin</span></span>
<span data-ttu-id="fd929-116">As origens permitidas para o serviço de Signalr.</span><span class="sxs-lookup"><span data-stu-id="fd929-116">The allowed origins for the SignalR service.</span></span> <span data-ttu-id="fd929-117">Para permitir tudo, use "\*" e remova todas as outras origens da lista.</span><span class="sxs-lookup"><span data-stu-id="fd929-117">To allow all, use "\*" and remove all other origins from the list.</span></span> <span data-ttu-id="fd929-118">Barras não são permitidas como parte do domínio ou após TLD</span><span class="sxs-lookup"><span data-stu-id="fd929-118">Slashes are not allowed as part of domain or after TLD</span></span>

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

### <span data-ttu-id="fd929-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fd929-119">-AsJob</span></span>
<span data-ttu-id="fd929-120">Execute o cmdlet em plano de trabalho em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="fd929-120">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="fd929-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd929-121">-DefaultProfile</span></span>
<span data-ttu-id="fd929-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fd929-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd929-123">-Local</span><span class="sxs-lookup"><span data-stu-id="fd929-123">-Location</span></span>
<span data-ttu-id="fd929-124">O local do serviço de sinal de sinal.</span><span class="sxs-lookup"><span data-stu-id="fd929-124">The SignalR service location.</span></span> <span data-ttu-id="fd929-125">O local do grupo de recursos será usado se não for especificado.</span><span class="sxs-lookup"><span data-stu-id="fd929-125">The resource group location will be used if not specified.</span></span>

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

### <span data-ttu-id="fd929-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="fd929-126">-Name</span></span>
<span data-ttu-id="fd929-127">O nome do serviço do Signalr.</span><span class="sxs-lookup"><span data-stu-id="fd929-127">The SignalR service name.</span></span>

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

### <span data-ttu-id="fd929-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd929-128">-ResourceGroupName</span></span>
<span data-ttu-id="fd929-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="fd929-129">The resource group name.</span></span> <span data-ttu-id="fd929-130">O padrão será usado se não for especificado.</span><span class="sxs-lookup"><span data-stu-id="fd929-130">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="fd929-131">-Serviçomode</span><span class="sxs-lookup"><span data-stu-id="fd929-131">-ServiceMode</span></span>
<span data-ttu-id="fd929-132">O modo de serviço para o serviço de Signalr.</span><span class="sxs-lookup"><span data-stu-id="fd929-132">The service mode for the SignalR service.</span></span>

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

### <span data-ttu-id="fd929-133">-SKU</span><span class="sxs-lookup"><span data-stu-id="fd929-133">-Sku</span></span>
<span data-ttu-id="fd929-134">A SKU do serviço Signalr.</span><span class="sxs-lookup"><span data-stu-id="fd929-134">The SignalR service SKU.</span></span>

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

### <span data-ttu-id="fd929-135">-Marca</span><span class="sxs-lookup"><span data-stu-id="fd929-135">-Tag</span></span>
<span data-ttu-id="fd929-136">As marcas do serviço de Signalr.</span><span class="sxs-lookup"><span data-stu-id="fd929-136">The tags for the SignalR service.</span></span>

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

### <span data-ttu-id="fd929-137">-UnitCount</span><span class="sxs-lookup"><span data-stu-id="fd929-137">-UnitCount</span></span>
<span data-ttu-id="fd929-138">A contagem de unidade de serviço do Signalr, de 1 a 10.</span><span class="sxs-lookup"><span data-stu-id="fd929-138">The SignalR service unit count, from 1 to 10.</span></span> <span data-ttu-id="fd929-139">O padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="fd929-139">Default to 1.</span></span>

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

### <span data-ttu-id="fd929-140">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fd929-140">-Confirm</span></span>
<span data-ttu-id="fd929-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd929-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd929-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd929-142">-WhatIf</span></span>
<span data-ttu-id="fd929-143">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fd929-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd929-144">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fd929-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd929-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd929-145">CommonParameters</span></span>
<span data-ttu-id="fd929-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd929-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd929-147">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fd929-147">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd929-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fd929-148">INPUTS</span></span>

### <span data-ttu-id="fd929-149">System. String</span><span class="sxs-lookup"><span data-stu-id="fd929-149">System.String</span></span>

## <span data-ttu-id="fd929-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fd929-150">OUTPUTS</span></span>

### <span data-ttu-id="fd929-151">Microsoft. Azure. Commands. Signalr. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="fd929-151">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="fd929-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fd929-152">NOTES</span></span>

## <span data-ttu-id="fd929-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fd929-153">RELATED LINKS</span></span>