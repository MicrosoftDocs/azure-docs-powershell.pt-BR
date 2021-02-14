---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOrigin.md
ms.openlocfilehash: 8198d189d9619528bdc7fb80d30285ce9126dfed
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116906"
---
# <span data-ttu-id="b9ff1-101">Remove-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="b9ff1-101">Remove-AzCdnOrigin</span></span>

## <span data-ttu-id="b9ff1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b9ff1-102">SYNOPSIS</span></span>
<span data-ttu-id="b9ff1-103">Remove a origem de uma CDN</span><span class="sxs-lookup"><span data-stu-id="b9ff1-103">Removes a CDN origin</span></span>

## <span data-ttu-id="b9ff1-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b9ff1-104">SYNTAX</span></span>

### <span data-ttu-id="b9ff1-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b9ff1-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzCdnOrigin -OriginName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b9ff1-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9ff1-106">ByResourceIdParameterSet</span></span>
```
Remove-AzCdnOrigin -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9ff1-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b9ff1-107">ByObjectParameterSet</span></span>
```
Remove-AzCdnOrigin [-PassThru] -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9ff1-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="b9ff1-108">DESCRIPTION</span></span>
<span data-ttu-id="b9ff1-109">Remove-AzCdnOrigin excluirá uma origem de CDN do ponto de extremidade determinado.</span><span class="sxs-lookup"><span data-stu-id="b9ff1-109">Remove-AzCdnOrigin will delete a CDN origin from the given endpoint.</span></span> <span data-ttu-id="b9ff1-110">Se a origem for a única origem dentro do ponto de extremidade especificado, a exclusão falhará uma vez que pelo menos uma origem é necessária.</span><span class="sxs-lookup"><span data-stu-id="b9ff1-110">If the origin is the only origin within the specified endpoint, then the deletion will fail since at least 1 origin is needed.</span></span> 

## <span data-ttu-id="b9ff1-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b9ff1-111">EXAMPLES</span></span>

### <span data-ttu-id="b9ff1-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b9ff1-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzCdnOrigin -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginName $originName 
```
<span data-ttu-id="b9ff1-113">Esse cmdlet removerá a origem especificada do ponto de extremidade determinado.</span><span class="sxs-lookup"><span data-stu-id="b9ff1-113">This cmdlet will remove the specified origin from the given endpoint.</span></span> 

## <span data-ttu-id="b9ff1-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b9ff1-114">PARAMETERS</span></span>

### <span data-ttu-id="b9ff1-115">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="b9ff1-115">-CdnOrigin</span></span>
<span data-ttu-id="b9ff1-116">O objeto de origem CDN.</span><span class="sxs-lookup"><span data-stu-id="b9ff1-116">The CDN origin object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9ff1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9ff1-117">-DefaultProfile</span></span>
<span data-ttu-id="b9ff1-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b9ff1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9ff1-119">-Nomedo Ponto de Extremidade</span><span class="sxs-lookup"><span data-stu-id="b9ff1-119">-EndpointName</span></span>
<span data-ttu-id="b9ff1-120">Nome do ponto de extremidade CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="b9ff1-120">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="b9ff1-121">-OriginName</span><span class="sxs-lookup"><span data-stu-id="b9ff1-121">-OriginName</span></span>
<span data-ttu-id="b9ff1-122">Nome de origem do CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="b9ff1-122">Azure CDN origin name.</span></span>

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

### <span data-ttu-id="b9ff1-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b9ff1-123">-PassThru</span></span>
<span data-ttu-id="b9ff1-124">Retornar objeto, se especificado.</span><span class="sxs-lookup"><span data-stu-id="b9ff1-124">Return object if specified.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9ff1-125">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="b9ff1-125">-ProfileName</span></span>
<span data-ttu-id="b9ff1-126">Nome de perfil cdn do Azure.</span><span class="sxs-lookup"><span data-stu-id="b9ff1-126">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="b9ff1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9ff1-127">-ResourceGroupName</span></span>
<span data-ttu-id="b9ff1-128">O grupo de recursos do perfil de CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="b9ff1-128">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="b9ff1-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b9ff1-129">-ResourceId</span></span>
<span data-ttu-id="b9ff1-130">A ID do recurso da origem da CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="b9ff1-130">The resource id of the Azure CDN origin.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b9ff1-131">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="b9ff1-131">-Confirm</span></span>
<span data-ttu-id="b9ff1-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9ff1-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9ff1-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9ff1-133">-WhatIf</span></span>
<span data-ttu-id="b9ff1-134">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="b9ff1-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9ff1-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b9ff1-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9ff1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9ff1-136">CommonParameters</span></span>
<span data-ttu-id="b9ff1-137">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9ff1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9ff1-138">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b9ff1-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9ff1-139">Entradas</span><span class="sxs-lookup"><span data-stu-id="b9ff1-139">INPUTS</span></span>

### <span data-ttu-id="b9ff1-140">Nenhum</span><span class="sxs-lookup"><span data-stu-id="b9ff1-140">None</span></span>

## <span data-ttu-id="b9ff1-141">Saídas</span><span class="sxs-lookup"><span data-stu-id="b9ff1-141">OUTPUTS</span></span>

### <span data-ttu-id="b9ff1-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b9ff1-142">System.Boolean</span></span>

## <span data-ttu-id="b9ff1-143">Notas</span><span class="sxs-lookup"><span data-stu-id="b9ff1-143">NOTES</span></span>

## <span data-ttu-id="b9ff1-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b9ff1-144">RELATED LINKS</span></span>
