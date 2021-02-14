---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOriginGroup.md
ms.openlocfilehash: 58a9d45c29a9a11b31bff510e6b4e1c63844dd5d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116578"
---
# <span data-ttu-id="a3a8e-101">Set-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="a3a8e-101">Set-AzCdnOriginGroup</span></span>

## <span data-ttu-id="a3a8e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a3a8e-102">SYNOPSIS</span></span>
<span data-ttu-id="a3a8e-103">Atualiza o grupo de origem da CDN</span><span class="sxs-lookup"><span data-stu-id="a3a8e-103">Updates the CDN origin group</span></span>

## <span data-ttu-id="a3a8e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a3a8e-104">SYNTAX</span></span>

### <span data-ttu-id="a3a8e-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a3a8e-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String>
 -OriginId <System.Collections.Generic.List`1[System.String]> [-ProbeIntervalInSeconds <Int32>]
 [-ProbePath <String>] [-ProbeProtocol <String>] [-ProbeRequestType <String>] -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a3a8e-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a3a8e-106">ByObjectParameterSet</span></span>
```
Set-AzCdnOriginGroup -CdnOriginGroup <PSOriginGroup> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3a8e-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="a3a8e-107">DESCRIPTION</span></span>
<span data-ttu-id="a3a8e-108">Set-AzCdnOriginGroup atualizará o grupo de origem especificado dentro de determinado ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="a3a8e-108">Set-AzCdnOriginGroup will update the specified origin group within the given endpoint.</span></span> 

## <span data-ttu-id="a3a8e-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a3a8e-109">EXAMPLES</span></span>

### <span data-ttu-id="a3a8e-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a3a8e-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName -OriginId $originIds -ProbeIntervalInSeconds $probeInterval 
```
<span data-ttu-id="a3a8e-111">Este cmdlet atualizará a propriedade ElevalInSeconds no grupo de origem.</span><span class="sxs-lookup"><span data-stu-id="a3a8e-111">This cmdlet will update the ProbeIntervalInSeconds property in the origin group.</span></span> 

## <span data-ttu-id="a3a8e-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a3a8e-112">PARAMETERS</span></span>

### <span data-ttu-id="a3a8e-113">-CdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="a3a8e-113">-CdnOriginGroup</span></span>
<span data-ttu-id="a3a8e-114">O objeto do grupo de origem CDN.</span><span class="sxs-lookup"><span data-stu-id="a3a8e-114">The CDN origin group object.</span></span>

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

### <span data-ttu-id="a3a8e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3a8e-115">-DefaultProfile</span></span>
<span data-ttu-id="a3a8e-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a3a8e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3a8e-117">-Nomedo Ponto de Extremidade</span><span class="sxs-lookup"><span data-stu-id="a3a8e-117">-EndpointName</span></span>
<span data-ttu-id="a3a8e-118">Nome do ponto de extremidade CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="a3a8e-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="a3a8e-119">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="a3a8e-119">-OriginGroupName</span></span>
<span data-ttu-id="a3a8e-120">Nome do grupo de origem cdn do Azure.</span><span class="sxs-lookup"><span data-stu-id="a3a8e-120">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="a3a8e-121">-OriginId</span><span class="sxs-lookup"><span data-stu-id="a3a8e-121">-OriginId</span></span>
<span data-ttu-id="a3a8e-122">IDs do grupo de origem cdn do Azure.</span><span class="sxs-lookup"><span data-stu-id="a3a8e-122">Azure CDN origin group ids.</span></span>

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

### <span data-ttu-id="a3a8e-123">-ElevaIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="a3a8e-123">-ProbeIntervalInSeconds</span></span>
<span data-ttu-id="a3a8e-124">O número de segundos entre problemas de saúde.</span><span class="sxs-lookup"><span data-stu-id="a3a8e-124">The number of seconds between health probes.</span></span>

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

### <span data-ttu-id="a3a8e-125">-Path</span><span class="sxs-lookup"><span data-stu-id="a3a8e-125">-ProbePath</span></span>
<span data-ttu-id="a3a8e-126">O caminho em relação à origem usado para determinar a saúde da origem.</span><span class="sxs-lookup"><span data-stu-id="a3a8e-126">The path relative to the origin that is used to determine the health of the origin.</span></span>

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

### <span data-ttu-id="a3a8e-127">-Elaprotocol</span><span class="sxs-lookup"><span data-stu-id="a3a8e-127">-ProbeProtocol</span></span>
<span data-ttu-id="a3a8e-128">Protocolo a ser usado para a saúde.</span><span class="sxs-lookup"><span data-stu-id="a3a8e-128">Protocol to use for health probe.</span></span>

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

### <span data-ttu-id="a3a8e-129">-Ela é um tipo de autoconsuidade</span><span class="sxs-lookup"><span data-stu-id="a3a8e-129">-ProbeRequestType</span></span>
<span data-ttu-id="a3a8e-130">O tipo de solicitação de saúde que é feita.</span><span class="sxs-lookup"><span data-stu-id="a3a8e-130">The type of health probe request that is made.</span></span>

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

### <span data-ttu-id="a3a8e-131">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="a3a8e-131">-ProfileName</span></span>
<span data-ttu-id="a3a8e-132">Nome de perfil cdn do Azure.</span><span class="sxs-lookup"><span data-stu-id="a3a8e-132">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="a3a8e-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3a8e-133">-ResourceGroupName</span></span>
<span data-ttu-id="a3a8e-134">O grupo de recursos do perfil de CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="a3a8e-134">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="a3a8e-135">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="a3a8e-135">-Confirm</span></span>
<span data-ttu-id="a3a8e-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a3a8e-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3a8e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3a8e-137">-WhatIf</span></span>
<span data-ttu-id="a3a8e-138">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="a3a8e-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3a8e-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a3a8e-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3a8e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3a8e-140">CommonParameters</span></span>
<span data-ttu-id="a3a8e-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3a8e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3a8e-142">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a3a8e-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3a8e-143">Entradas</span><span class="sxs-lookup"><span data-stu-id="a3a8e-143">INPUTS</span></span>

### <span data-ttu-id="a3a8e-144">System.Object</span><span class="sxs-lookup"><span data-stu-id="a3a8e-144">System.Object</span></span>

## <span data-ttu-id="a3a8e-145">Saídas</span><span class="sxs-lookup"><span data-stu-id="a3a8e-145">OUTPUTS</span></span>

### <span data-ttu-id="a3a8e-146">System.Object</span><span class="sxs-lookup"><span data-stu-id="a3a8e-146">System.Object</span></span>

## <span data-ttu-id="a3a8e-147">Notas</span><span class="sxs-lookup"><span data-stu-id="a3a8e-147">NOTES</span></span>

## <span data-ttu-id="a3a8e-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a3a8e-148">RELATED LINKS</span></span>
