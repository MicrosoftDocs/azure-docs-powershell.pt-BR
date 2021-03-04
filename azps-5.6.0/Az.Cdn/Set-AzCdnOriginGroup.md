---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/set-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOriginGroup.md
ms.openlocfilehash: c70c08ad88491d7624b078babb5e62437c22e116
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889569"
---
# <span data-ttu-id="2d10e-101">Set-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="2d10e-101">Set-AzCdnOriginGroup</span></span>

## <span data-ttu-id="2d10e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d10e-102">SYNOPSIS</span></span>
<span data-ttu-id="2d10e-103">Atualiza o grupo de origem da CDN</span><span class="sxs-lookup"><span data-stu-id="2d10e-103">Updates the CDN origin group</span></span>

## <span data-ttu-id="2d10e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="2d10e-104">SYNTAX</span></span>

### <span data-ttu-id="2d10e-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2d10e-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String>
 -OriginId <System.Collections.Generic.List`1[System.String]> [-ProbeIntervalInSeconds <Int32>]
 [-ProbePath <String>] [-ProbeProtocol <String>] [-ProbeRequestType <String>] -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2d10e-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2d10e-106">ByObjectParameterSet</span></span>
```
Set-AzCdnOriginGroup -CdnOriginGroup <PSOriginGroup> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d10e-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="2d10e-107">DESCRIPTION</span></span>
<span data-ttu-id="2d10e-108">Set-AzCdnOriginGroup atualizará o grupo de origem especificado dentro do ponto de extremidade determinado.</span><span class="sxs-lookup"><span data-stu-id="2d10e-108">Set-AzCdnOriginGroup will update the specified origin group within the given endpoint.</span></span> 

## <span data-ttu-id="2d10e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2d10e-109">EXAMPLES</span></span>

### <span data-ttu-id="2d10e-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2d10e-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName -OriginId $originIds -ProbeIntervalInSeconds $probeInterval 
```
<span data-ttu-id="2d10e-111">Este cmdlet atualizará a propriedade ProbeIntervalInSeconds no grupo de origem.</span><span class="sxs-lookup"><span data-stu-id="2d10e-111">This cmdlet will update the ProbeIntervalInSeconds property in the origin group.</span></span> 

## <span data-ttu-id="2d10e-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="2d10e-112">PARAMETERS</span></span>

### <span data-ttu-id="2d10e-113">-CdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="2d10e-113">-CdnOriginGroup</span></span>
<span data-ttu-id="2d10e-114">O objeto do grupo de origem CDN.</span><span class="sxs-lookup"><span data-stu-id="2d10e-114">The CDN origin group object.</span></span>

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

### <span data-ttu-id="2d10e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d10e-115">-DefaultProfile</span></span>
<span data-ttu-id="2d10e-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2d10e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d10e-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="2d10e-117">-EndpointName</span></span>
<span data-ttu-id="2d10e-118">Nome do ponto de extremidade cdn do Azure.</span><span class="sxs-lookup"><span data-stu-id="2d10e-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="2d10e-119">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="2d10e-119">-OriginGroupName</span></span>
<span data-ttu-id="2d10e-120">Nome do grupo de origem cdn do Azure.</span><span class="sxs-lookup"><span data-stu-id="2d10e-120">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="2d10e-121">-OriginId</span><span class="sxs-lookup"><span data-stu-id="2d10e-121">-OriginId</span></span>
<span data-ttu-id="2d10e-122">Ids de grupo de origem da CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="2d10e-122">Azure CDN origin group ids.</span></span>

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

### <span data-ttu-id="2d10e-123">-ProbeIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="2d10e-123">-ProbeIntervalInSeconds</span></span>
<span data-ttu-id="2d10e-124">O número de segundos entre as sondas de saúde.</span><span class="sxs-lookup"><span data-stu-id="2d10e-124">The number of seconds between health probes.</span></span>

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

### <span data-ttu-id="2d10e-125">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="2d10e-125">-ProbePath</span></span>
<span data-ttu-id="2d10e-126">O caminho relativo à origem usada para determinar a saúde da origem.</span><span class="sxs-lookup"><span data-stu-id="2d10e-126">The path relative to the origin that is used to determine the health of the origin.</span></span>

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

### <span data-ttu-id="2d10e-127">-ProbeProtocol</span><span class="sxs-lookup"><span data-stu-id="2d10e-127">-ProbeProtocol</span></span>
<span data-ttu-id="2d10e-128">Protocolo a ser usado para a sonda de saúde.</span><span class="sxs-lookup"><span data-stu-id="2d10e-128">Protocol to use for health probe.</span></span>

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

### <span data-ttu-id="2d10e-129">-ProbeRequestType</span><span class="sxs-lookup"><span data-stu-id="2d10e-129">-ProbeRequestType</span></span>
<span data-ttu-id="2d10e-130">O tipo de solicitação de sonda de saúde que é feita.</span><span class="sxs-lookup"><span data-stu-id="2d10e-130">The type of health probe request that is made.</span></span>

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

### <span data-ttu-id="2d10e-131">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="2d10e-131">-ProfileName</span></span>
<span data-ttu-id="2d10e-132">Nome do perfil cdn do Azure.</span><span class="sxs-lookup"><span data-stu-id="2d10e-132">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="2d10e-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d10e-133">-ResourceGroupName</span></span>
<span data-ttu-id="2d10e-134">O grupo de recursos do perfil cdn do Azure.</span><span class="sxs-lookup"><span data-stu-id="2d10e-134">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="2d10e-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2d10e-135">-Confirm</span></span>
<span data-ttu-id="2d10e-136">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d10e-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d10e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d10e-137">-WhatIf</span></span>
<span data-ttu-id="2d10e-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="2d10e-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d10e-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2d10e-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d10e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d10e-140">CommonParameters</span></span>
<span data-ttu-id="2d10e-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d10e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d10e-142">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2d10e-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d10e-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2d10e-143">INPUTS</span></span>

### <span data-ttu-id="2d10e-144">System.Object</span><span class="sxs-lookup"><span data-stu-id="2d10e-144">System.Object</span></span>

## <span data-ttu-id="2d10e-145">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="2d10e-145">OUTPUTS</span></span>

### <span data-ttu-id="2d10e-146">System.Object</span><span class="sxs-lookup"><span data-stu-id="2d10e-146">System.Object</span></span>

## <span data-ttu-id="2d10e-147">NOTES</span><span class="sxs-lookup"><span data-stu-id="2d10e-147">NOTES</span></span>

## <span data-ttu-id="2d10e-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2d10e-148">RELATED LINKS</span></span>
