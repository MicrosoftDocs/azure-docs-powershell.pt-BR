---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOriginGroup.md
ms.openlocfilehash: 9c499fe716df97edc4644729dc996bd4f9bae992
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116921"
---
# <span data-ttu-id="a145d-101">New-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="a145d-101">New-AzCdnOriginGroup</span></span>

## <span data-ttu-id="a145d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a145d-102">SYNOPSIS</span></span>
<span data-ttu-id="a145d-103">Cria um novo grupo de origem de CDN</span><span class="sxs-lookup"><span data-stu-id="a145d-103">Creates a new CDN origin group</span></span>

## <span data-ttu-id="a145d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a145d-104">SYNTAX</span></span>

### <span data-ttu-id="a145d-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a145d-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String>
 -OriginId <System.Collections.Generic.List`1[System.String]> [-ProbeIntervalInSeconds <Int32>]
 [-ProbePath <String>] [-ProbeProtocol <String>] [-ProbeRequestType <String>] -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a145d-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a145d-106">ByObjectParameterSet</span></span>
```
New-AzCdnOriginGroup -CdnOriginGroup <PSOriginGroup> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a145d-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="a145d-107">DESCRIPTION</span></span>
<span data-ttu-id="a145d-108">A New-AzCdnOriginGroup criará um novo grupo de origem dentro do ponto de extremidade especificado.</span><span class="sxs-lookup"><span data-stu-id="a145d-108">The New-AzCdnOriginGroup will create a new origin group within the specified endpoint.</span></span> <span data-ttu-id="a145d-109">Se esse for o primeiro grupo de origem do ponto de extremidade, a propriedade DefaultOriginGroup também deverá ser definida.</span><span class="sxs-lookup"><span data-stu-id="a145d-109">If this is the first origin group for endpoint, then the DefaultOriginGroup property must also be set.</span></span>

## <span data-ttu-id="a145d-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a145d-110">EXAMPLES</span></span>

### <span data-ttu-id="a145d-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a145d-111">Example 1</span></span>
```powershell
PS C:\> New-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName -OriginId $originId
```
<span data-ttu-id="a145d-112">Esse cmdlet criará um novo grupo de origem dentro do ponto de extremidade especificado.</span><span class="sxs-lookup"><span data-stu-id="a145d-112">This cmdlet will create a new origin group within the specified endpoint.</span></span> <span data-ttu-id="a145d-113">Ela utilizará as IDs de origem determinadas como o conjunto de origens.</span><span class="sxs-lookup"><span data-stu-id="a145d-113">It will utilize the given origin ids as the set of origins.</span></span>

## <span data-ttu-id="a145d-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a145d-114">PARAMETERS</span></span>

### <span data-ttu-id="a145d-115">-CdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="a145d-115">-CdnOriginGroup</span></span>
<span data-ttu-id="a145d-116">O objeto do grupo de origem CDN.</span><span class="sxs-lookup"><span data-stu-id="a145d-116">The CDN origin group object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.OriginGroup.PSOriginGroup
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a145d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a145d-117">-DefaultProfile</span></span>
<span data-ttu-id="a145d-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a145d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a145d-119">-Nomedo Ponto de Extremidade</span><span class="sxs-lookup"><span data-stu-id="a145d-119">-EndpointName</span></span>
<span data-ttu-id="a145d-120">Nome do ponto de extremidade CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="a145d-120">Azure CDN endpoint name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a145d-121">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="a145d-121">-OriginGroupName</span></span>
<span data-ttu-id="a145d-122">Nome do grupo de origem cdn do Azure.</span><span class="sxs-lookup"><span data-stu-id="a145d-122">Azure CDN origin group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a145d-123">-OriginId</span><span class="sxs-lookup"><span data-stu-id="a145d-123">-OriginId</span></span>
<span data-ttu-id="a145d-124">IDs do grupo de origem cdn do Azure.</span><span class="sxs-lookup"><span data-stu-id="a145d-124">Azure CDN origin group ids.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a145d-125">-ElevaIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="a145d-125">-ProbeIntervalInSeconds</span></span>
<span data-ttu-id="a145d-126">O número de segundos entre problemas de saúde.</span><span class="sxs-lookup"><span data-stu-id="a145d-126">The number of seconds between health probes.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a145d-127">-Path</span><span class="sxs-lookup"><span data-stu-id="a145d-127">-ProbePath</span></span>
<span data-ttu-id="a145d-128">O caminho em relação à origem usado para determinar a saúde da origem.</span><span class="sxs-lookup"><span data-stu-id="a145d-128">The path relative to the origin that is used to determine the health of the origin.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a145d-129">-Elaprotocol</span><span class="sxs-lookup"><span data-stu-id="a145d-129">-ProbeProtocol</span></span>
<span data-ttu-id="a145d-130">Protocolo a ser usado para a saúde.</span><span class="sxs-lookup"><span data-stu-id="a145d-130">Protocol to use for health probe.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a145d-131">-Ela é um tipo de autoconsuidade</span><span class="sxs-lookup"><span data-stu-id="a145d-131">-ProbeRequestType</span></span>
<span data-ttu-id="a145d-132">O tipo de solicitação de saúde que é feita.</span><span class="sxs-lookup"><span data-stu-id="a145d-132">The type of health probe request that is made.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a145d-133">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="a145d-133">-ProfileName</span></span>
<span data-ttu-id="a145d-134">Nome de perfil cdn do Azure.</span><span class="sxs-lookup"><span data-stu-id="a145d-134">Azure CDN profile name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a145d-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a145d-135">-ResourceGroupName</span></span>
<span data-ttu-id="a145d-136">O grupo de recursos do perfil de CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="a145d-136">The resource group of the Azure CDN profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a145d-137">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="a145d-137">-Confirm</span></span>
<span data-ttu-id="a145d-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a145d-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a145d-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a145d-139">-WhatIf</span></span>
<span data-ttu-id="a145d-140">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="a145d-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a145d-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a145d-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a145d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a145d-142">CommonParameters</span></span>
<span data-ttu-id="a145d-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a145d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a145d-144">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a145d-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a145d-145">Entradas</span><span class="sxs-lookup"><span data-stu-id="a145d-145">INPUTS</span></span>

### <span data-ttu-id="a145d-146">System.Object</span><span class="sxs-lookup"><span data-stu-id="a145d-146">System.Object</span></span>

## <span data-ttu-id="a145d-147">Saídas</span><span class="sxs-lookup"><span data-stu-id="a145d-147">OUTPUTS</span></span>

### <span data-ttu-id="a145d-148">System.Object</span><span class="sxs-lookup"><span data-stu-id="a145d-148">System.Object</span></span>

## <span data-ttu-id="a145d-149">Notas</span><span class="sxs-lookup"><span data-stu-id="a145d-149">NOTES</span></span>

## <span data-ttu-id="a145d-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a145d-150">RELATED LINKS</span></span>
