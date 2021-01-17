---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/new-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/New-AzCdnOriginGroup.md
ms.openlocfilehash: 9c499fe716df97edc4644729dc996bd4f9bae992
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434427"
---
# <span data-ttu-id="8ef15-101">New-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="8ef15-101">New-AzCdnOriginGroup</span></span>

## <span data-ttu-id="8ef15-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8ef15-102">SYNOPSIS</span></span>
<span data-ttu-id="8ef15-103">Cria um novo grupo de origens CDN</span><span class="sxs-lookup"><span data-stu-id="8ef15-103">Creates a new CDN origin group</span></span>

## <span data-ttu-id="8ef15-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8ef15-104">SYNTAX</span></span>

### <span data-ttu-id="8ef15-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="8ef15-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String>
 -OriginId <System.Collections.Generic.List`1[System.String]> [-ProbeIntervalInSeconds <Int32>]
 [-ProbePath <String>] [-ProbeProtocol <String>] [-ProbeRequestType <String>] -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8ef15-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8ef15-106">ByObjectParameterSet</span></span>
```
New-AzCdnOriginGroup -CdnOriginGroup <PSOriginGroup> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ef15-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8ef15-107">DESCRIPTION</span></span>
<span data-ttu-id="8ef15-108">O New-AzCdnOriginGroup criará um novo grupo de origem dentro do ponto de extremidade especificado.</span><span class="sxs-lookup"><span data-stu-id="8ef15-108">The New-AzCdnOriginGroup will create a new origin group within the specified endpoint.</span></span> <span data-ttu-id="8ef15-109">Se esse for o primeiro grupo de origem para o ponto de extremidade, a propriedade defaultorigin também deve ser definida.</span><span class="sxs-lookup"><span data-stu-id="8ef15-109">If this is the first origin group for endpoint, then the DefaultOriginGroup property must also be set.</span></span>

## <span data-ttu-id="8ef15-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8ef15-110">EXAMPLES</span></span>

### <span data-ttu-id="8ef15-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8ef15-111">Example 1</span></span>
```powershell
PS C:\> New-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName -OriginId $originId
```
<span data-ttu-id="8ef15-112">Esse cmdlet criará um novo grupo de origem dentro do ponto de extremidade especificado.</span><span class="sxs-lookup"><span data-stu-id="8ef15-112">This cmdlet will create a new origin group within the specified endpoint.</span></span> <span data-ttu-id="8ef15-113">Ele usará as identificações de origem fornecidas como o conjunto de origens.</span><span class="sxs-lookup"><span data-stu-id="8ef15-113">It will utilize the given origin ids as the set of origins.</span></span>

## <span data-ttu-id="8ef15-114">OS</span><span class="sxs-lookup"><span data-stu-id="8ef15-114">PARAMETERS</span></span>

### <span data-ttu-id="8ef15-115">-CdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="8ef15-115">-CdnOriginGroup</span></span>
<span data-ttu-id="8ef15-116">O objeto do grupo de origem CDN.</span><span class="sxs-lookup"><span data-stu-id="8ef15-116">The CDN origin group object.</span></span>

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

### <span data-ttu-id="8ef15-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ef15-117">-DefaultProfile</span></span>
<span data-ttu-id="8ef15-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8ef15-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ef15-119">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="8ef15-119">-EndpointName</span></span>
<span data-ttu-id="8ef15-120">Nome do ponto de extremidade CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="8ef15-120">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="8ef15-121">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="8ef15-121">-OriginGroupName</span></span>
<span data-ttu-id="8ef15-122">Nome do grupo de origens da CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="8ef15-122">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="8ef15-123">-Originid</span><span class="sxs-lookup"><span data-stu-id="8ef15-123">-OriginId</span></span>
<span data-ttu-id="8ef15-124">IDs do grupo de origens da CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="8ef15-124">Azure CDN origin group ids.</span></span>

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

### <span data-ttu-id="8ef15-125">-ProbeIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="8ef15-125">-ProbeIntervalInSeconds</span></span>
<span data-ttu-id="8ef15-126">O número de segundos entre testes de integridade.</span><span class="sxs-lookup"><span data-stu-id="8ef15-126">The number of seconds between health probes.</span></span>

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

### <span data-ttu-id="8ef15-127">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="8ef15-127">-ProbePath</span></span>
<span data-ttu-id="8ef15-128">O caminho relativo à origem que é usada para determinar a integridade da origem.</span><span class="sxs-lookup"><span data-stu-id="8ef15-128">The path relative to the origin that is used to determine the health of the origin.</span></span>

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

### <span data-ttu-id="8ef15-129">-ProbeProtocol</span><span class="sxs-lookup"><span data-stu-id="8ef15-129">-ProbeProtocol</span></span>
<span data-ttu-id="8ef15-130">Protocolo a ser usado para investigação de integridade.</span><span class="sxs-lookup"><span data-stu-id="8ef15-130">Protocol to use for health probe.</span></span>

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

### <span data-ttu-id="8ef15-131">-ProbeRequestType</span><span class="sxs-lookup"><span data-stu-id="8ef15-131">-ProbeRequestType</span></span>
<span data-ttu-id="8ef15-132">O tipo de solicitação de investigação de integridade feita.</span><span class="sxs-lookup"><span data-stu-id="8ef15-132">The type of health probe request that is made.</span></span>

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

### <span data-ttu-id="8ef15-133">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="8ef15-133">-ProfileName</span></span>
<span data-ttu-id="8ef15-134">Nome do perfil CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="8ef15-134">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="8ef15-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ef15-135">-ResourceGroupName</span></span>
<span data-ttu-id="8ef15-136">O grupo de recursos do perfil CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="8ef15-136">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="8ef15-137">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8ef15-137">-Confirm</span></span>
<span data-ttu-id="8ef15-138">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ef15-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ef15-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ef15-139">-WhatIf</span></span>
<span data-ttu-id="8ef15-140">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8ef15-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8ef15-141">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8ef15-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ef15-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ef15-142">CommonParameters</span></span>
<span data-ttu-id="8ef15-143">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ef15-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ef15-144">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8ef15-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ef15-145">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8ef15-145">INPUTS</span></span>

### <span data-ttu-id="8ef15-146">System. Object</span><span class="sxs-lookup"><span data-stu-id="8ef15-146">System.Object</span></span>

## <span data-ttu-id="8ef15-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8ef15-147">OUTPUTS</span></span>

### <span data-ttu-id="8ef15-148">System. Object</span><span class="sxs-lookup"><span data-stu-id="8ef15-148">System.Object</span></span>

## <span data-ttu-id="8ef15-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8ef15-149">NOTES</span></span>

## <span data-ttu-id="8ef15-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8ef15-150">RELATED LINKS</span></span>
