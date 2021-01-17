---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOriginGroup.md
ms.openlocfilehash: 58a9d45c29a9a11b31bff510e6b4e1c63844dd5d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434419"
---
# <span data-ttu-id="ca773-101">Set-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="ca773-101">Set-AzCdnOriginGroup</span></span>

## <span data-ttu-id="ca773-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ca773-102">SYNOPSIS</span></span>
<span data-ttu-id="ca773-103">Atualiza o grupo de origens CDN</span><span class="sxs-lookup"><span data-stu-id="ca773-103">Updates the CDN origin group</span></span>

## <span data-ttu-id="ca773-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ca773-104">SYNTAX</span></span>

### <span data-ttu-id="ca773-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="ca773-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String>
 -OriginId <System.Collections.Generic.List`1[System.String]> [-ProbeIntervalInSeconds <Int32>]
 [-ProbePath <String>] [-ProbeProtocol <String>] [-ProbeRequestType <String>] -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ca773-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca773-106">ByObjectParameterSet</span></span>
```
Set-AzCdnOriginGroup -CdnOriginGroup <PSOriginGroup> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca773-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ca773-107">DESCRIPTION</span></span>
<span data-ttu-id="ca773-108">Set-AzCdnOriginGroup atualizará o grupo de origem especificado dentro de um determinado ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="ca773-108">Set-AzCdnOriginGroup will update the specified origin group within the given endpoint.</span></span> 

## <span data-ttu-id="ca773-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ca773-109">EXAMPLES</span></span>

### <span data-ttu-id="ca773-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ca773-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName -OriginId $originIds -ProbeIntervalInSeconds $probeInterval 
```
<span data-ttu-id="ca773-111">Esse cmdlet atualizará a propriedade ProbeIntervalInSeconds no grupo Origin.</span><span class="sxs-lookup"><span data-stu-id="ca773-111">This cmdlet will update the ProbeIntervalInSeconds property in the origin group.</span></span> 

## <span data-ttu-id="ca773-112">OS</span><span class="sxs-lookup"><span data-stu-id="ca773-112">PARAMETERS</span></span>

### <span data-ttu-id="ca773-113">-CdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="ca773-113">-CdnOriginGroup</span></span>
<span data-ttu-id="ca773-114">O objeto do grupo de origem CDN.</span><span class="sxs-lookup"><span data-stu-id="ca773-114">The CDN origin group object.</span></span>

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

### <span data-ttu-id="ca773-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca773-115">-DefaultProfile</span></span>
<span data-ttu-id="ca773-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ca773-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca773-117">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="ca773-117">-EndpointName</span></span>
<span data-ttu-id="ca773-118">Nome do ponto de extremidade CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="ca773-118">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="ca773-119">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="ca773-119">-OriginGroupName</span></span>
<span data-ttu-id="ca773-120">Nome do grupo de origens da CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="ca773-120">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="ca773-121">-Originid</span><span class="sxs-lookup"><span data-stu-id="ca773-121">-OriginId</span></span>
<span data-ttu-id="ca773-122">IDs do grupo de origens da CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="ca773-122">Azure CDN origin group ids.</span></span>

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

### <span data-ttu-id="ca773-123">-ProbeIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="ca773-123">-ProbeIntervalInSeconds</span></span>
<span data-ttu-id="ca773-124">O número de segundos entre testes de integridade.</span><span class="sxs-lookup"><span data-stu-id="ca773-124">The number of seconds between health probes.</span></span>

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

### <span data-ttu-id="ca773-125">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="ca773-125">-ProbePath</span></span>
<span data-ttu-id="ca773-126">O caminho relativo à origem que é usada para determinar a integridade da origem.</span><span class="sxs-lookup"><span data-stu-id="ca773-126">The path relative to the origin that is used to determine the health of the origin.</span></span>

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

### <span data-ttu-id="ca773-127">-ProbeProtocol</span><span class="sxs-lookup"><span data-stu-id="ca773-127">-ProbeProtocol</span></span>
<span data-ttu-id="ca773-128">Protocolo a ser usado para investigação de integridade.</span><span class="sxs-lookup"><span data-stu-id="ca773-128">Protocol to use for health probe.</span></span>

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

### <span data-ttu-id="ca773-129">-ProbeRequestType</span><span class="sxs-lookup"><span data-stu-id="ca773-129">-ProbeRequestType</span></span>
<span data-ttu-id="ca773-130">O tipo de solicitação de investigação de integridade feita.</span><span class="sxs-lookup"><span data-stu-id="ca773-130">The type of health probe request that is made.</span></span>

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

### <span data-ttu-id="ca773-131">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="ca773-131">-ProfileName</span></span>
<span data-ttu-id="ca773-132">Nome do perfil CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="ca773-132">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="ca773-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca773-133">-ResourceGroupName</span></span>
<span data-ttu-id="ca773-134">O grupo de recursos do perfil CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="ca773-134">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="ca773-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ca773-135">-Confirm</span></span>
<span data-ttu-id="ca773-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca773-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca773-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca773-137">-WhatIf</span></span>
<span data-ttu-id="ca773-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ca773-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca773-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ca773-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca773-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca773-140">CommonParameters</span></span>
<span data-ttu-id="ca773-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca773-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca773-142">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ca773-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca773-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ca773-143">INPUTS</span></span>

### <span data-ttu-id="ca773-144">System. Object</span><span class="sxs-lookup"><span data-stu-id="ca773-144">System.Object</span></span>

## <span data-ttu-id="ca773-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ca773-145">OUTPUTS</span></span>

### <span data-ttu-id="ca773-146">System. Object</span><span class="sxs-lookup"><span data-stu-id="ca773-146">System.Object</span></span>

## <span data-ttu-id="ca773-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ca773-147">NOTES</span></span>

## <span data-ttu-id="ca773-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ca773-148">RELATED LINKS</span></span>
