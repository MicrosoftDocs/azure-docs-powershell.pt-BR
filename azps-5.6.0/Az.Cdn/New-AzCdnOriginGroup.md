---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/new-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOriginGroup.md
ms.openlocfilehash: 34d5b4dccb43f604625652f1c39b2250926058d8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891513"
---
# <span data-ttu-id="cdc6e-101">New-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="cdc6e-101">New-AzCdnOriginGroup</span></span>

## <span data-ttu-id="cdc6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cdc6e-102">SYNOPSIS</span></span>
<span data-ttu-id="cdc6e-103">Cria um novo grupo de origem da CDN</span><span class="sxs-lookup"><span data-stu-id="cdc6e-103">Creates a new CDN origin group</span></span>

## <span data-ttu-id="cdc6e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="cdc6e-104">SYNTAX</span></span>

### <span data-ttu-id="cdc6e-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="cdc6e-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String>
 -OriginId <System.Collections.Generic.List`1[System.String]> [-ProbeIntervalInSeconds <Int32>]
 [-ProbePath <String>] [-ProbeProtocol <String>] [-ProbeRequestType <String>] -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cdc6e-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cdc6e-106">ByObjectParameterSet</span></span>
```
New-AzCdnOriginGroup -CdnOriginGroup <PSOriginGroup> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cdc6e-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="cdc6e-107">DESCRIPTION</span></span>
<span data-ttu-id="cdc6e-108">O New-AzCdnOriginGroup criará um novo grupo de origem dentro do ponto de extremidade especificado.</span><span class="sxs-lookup"><span data-stu-id="cdc6e-108">The New-AzCdnOriginGroup will create a new origin group within the specified endpoint.</span></span> <span data-ttu-id="cdc6e-109">Se esse for o primeiro grupo de origem do ponto de extremidade, a propriedade DefaultOriginGroup também deverá ser definida.</span><span class="sxs-lookup"><span data-stu-id="cdc6e-109">If this is the first origin group for endpoint, then the DefaultOriginGroup property must also be set.</span></span>

## <span data-ttu-id="cdc6e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cdc6e-110">EXAMPLES</span></span>

### <span data-ttu-id="cdc6e-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="cdc6e-111">Example 1</span></span>
```powershell
PS C:\> New-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName -OriginId $originId
```
<span data-ttu-id="cdc6e-112">Este cmdlet criará um novo grupo de origem dentro do ponto de extremidade especificado.</span><span class="sxs-lookup"><span data-stu-id="cdc6e-112">This cmdlet will create a new origin group within the specified endpoint.</span></span> <span data-ttu-id="cdc6e-113">Ele utilizará as IDs de origem determinadas como o conjunto de origens.</span><span class="sxs-lookup"><span data-stu-id="cdc6e-113">It will utilize the given origin ids as the set of origins.</span></span>

## <span data-ttu-id="cdc6e-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="cdc6e-114">PARAMETERS</span></span>

### <span data-ttu-id="cdc6e-115">-CdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="cdc6e-115">-CdnOriginGroup</span></span>
<span data-ttu-id="cdc6e-116">O objeto do grupo de origem CDN.</span><span class="sxs-lookup"><span data-stu-id="cdc6e-116">The CDN origin group object.</span></span>

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

### <span data-ttu-id="cdc6e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdc6e-117">-DefaultProfile</span></span>
<span data-ttu-id="cdc6e-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cdc6e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cdc6e-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="cdc6e-119">-EndpointName</span></span>
<span data-ttu-id="cdc6e-120">Nome do ponto de extremidade cdn do Azure.</span><span class="sxs-lookup"><span data-stu-id="cdc6e-120">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="cdc6e-121">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="cdc6e-121">-OriginGroupName</span></span>
<span data-ttu-id="cdc6e-122">Nome do grupo de origem cdn do Azure.</span><span class="sxs-lookup"><span data-stu-id="cdc6e-122">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="cdc6e-123">-OriginId</span><span class="sxs-lookup"><span data-stu-id="cdc6e-123">-OriginId</span></span>
<span data-ttu-id="cdc6e-124">Ids de grupo de origem da CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="cdc6e-124">Azure CDN origin group ids.</span></span>

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

### <span data-ttu-id="cdc6e-125">-ProbeIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="cdc6e-125">-ProbeIntervalInSeconds</span></span>
<span data-ttu-id="cdc6e-126">O número de segundos entre as sondas de saúde.</span><span class="sxs-lookup"><span data-stu-id="cdc6e-126">The number of seconds between health probes.</span></span>

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

### <span data-ttu-id="cdc6e-127">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="cdc6e-127">-ProbePath</span></span>
<span data-ttu-id="cdc6e-128">O caminho relativo à origem usada para determinar a saúde da origem.</span><span class="sxs-lookup"><span data-stu-id="cdc6e-128">The path relative to the origin that is used to determine the health of the origin.</span></span>

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

### <span data-ttu-id="cdc6e-129">-ProbeProtocol</span><span class="sxs-lookup"><span data-stu-id="cdc6e-129">-ProbeProtocol</span></span>
<span data-ttu-id="cdc6e-130">Protocolo a ser usado para a sonda de saúde.</span><span class="sxs-lookup"><span data-stu-id="cdc6e-130">Protocol to use for health probe.</span></span>

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

### <span data-ttu-id="cdc6e-131">-ProbeRequestType</span><span class="sxs-lookup"><span data-stu-id="cdc6e-131">-ProbeRequestType</span></span>
<span data-ttu-id="cdc6e-132">O tipo de solicitação de sonda de saúde que é feita.</span><span class="sxs-lookup"><span data-stu-id="cdc6e-132">The type of health probe request that is made.</span></span>

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

### <span data-ttu-id="cdc6e-133">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="cdc6e-133">-ProfileName</span></span>
<span data-ttu-id="cdc6e-134">Nome do perfil cdn do Azure.</span><span class="sxs-lookup"><span data-stu-id="cdc6e-134">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="cdc6e-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdc6e-135">-ResourceGroupName</span></span>
<span data-ttu-id="cdc6e-136">O grupo de recursos do perfil cdn do Azure.</span><span class="sxs-lookup"><span data-stu-id="cdc6e-136">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="cdc6e-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cdc6e-137">-Confirm</span></span>
<span data-ttu-id="cdc6e-138">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cdc6e-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cdc6e-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdc6e-139">-WhatIf</span></span>
<span data-ttu-id="cdc6e-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cdc6e-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cdc6e-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cdc6e-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cdc6e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdc6e-142">CommonParameters</span></span>
<span data-ttu-id="cdc6e-143">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdc6e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdc6e-144">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cdc6e-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdc6e-145">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cdc6e-145">INPUTS</span></span>

### <span data-ttu-id="cdc6e-146">System.Object</span><span class="sxs-lookup"><span data-stu-id="cdc6e-146">System.Object</span></span>

## <span data-ttu-id="cdc6e-147">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="cdc6e-147">OUTPUTS</span></span>

### <span data-ttu-id="cdc6e-148">System.Object</span><span class="sxs-lookup"><span data-stu-id="cdc6e-148">System.Object</span></span>

## <span data-ttu-id="cdc6e-149">NOTES</span><span class="sxs-lookup"><span data-stu-id="cdc6e-149">NOTES</span></span>

## <span data-ttu-id="cdc6e-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cdc6e-150">RELATED LINKS</span></span>
