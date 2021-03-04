---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/remove-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOriginGroup.md
ms.openlocfilehash: a954b6c259b9e793ca4e35e99ecb4c710ab7a4e3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885488"
---
# <span data-ttu-id="bf847-101">Remove-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="bf847-101">Remove-AzCdnOriginGroup</span></span>

## <span data-ttu-id="bf847-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf847-102">SYNOPSIS</span></span>
<span data-ttu-id="bf847-103">Remove um grupo de origem da CDN</span><span class="sxs-lookup"><span data-stu-id="bf847-103">Removes a CDN origin group</span></span>

## <span data-ttu-id="bf847-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="bf847-104">SYNTAX</span></span>

### <span data-ttu-id="bf847-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="bf847-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzCdnOriginGroup -OriginGroupName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bf847-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf847-106">ByResourceIdParameterSet</span></span>
```
Remove-AzCdnOriginGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf847-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bf847-107">ByObjectParameterSet</span></span>
```
Remove-AzCdnOriginGroup [-PassThru] -CdnOriginGroup <PSOriginGroup> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf847-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="bf847-108">DESCRIPTION</span></span>
<span data-ttu-id="bf847-109">Remove-AzCdnOriginGroup removerá um grupo de origem da CDN do ponto de extremidade especificado.</span><span class="sxs-lookup"><span data-stu-id="bf847-109">Remove-AzCdnOriginGroup will remove a CDN origin group from the specified endpoint.</span></span> 

## <span data-ttu-id="bf847-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bf847-110">EXAMPLES</span></span>

### <span data-ttu-id="bf847-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bf847-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName
```

<span data-ttu-id="bf847-112">Este cmdlet removerá o grupo de origem especificado do ponto de extremidade determinado.</span><span class="sxs-lookup"><span data-stu-id="bf847-112">This cmdlet will remove the specified origin group from the given endpoint.</span></span> 

## <span data-ttu-id="bf847-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="bf847-113">PARAMETERS</span></span>

### <span data-ttu-id="bf847-114">-CdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="bf847-114">-CdnOriginGroup</span></span>
<span data-ttu-id="bf847-115">O objeto do grupo de origem CDN.</span><span class="sxs-lookup"><span data-stu-id="bf847-115">The CDN origin group object.</span></span>

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

### <span data-ttu-id="bf847-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf847-116">-DefaultProfile</span></span>
<span data-ttu-id="bf847-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bf847-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf847-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="bf847-118">-EndpointName</span></span>
<span data-ttu-id="bf847-119">Nome do ponto de extremidade cdn do Azure.</span><span class="sxs-lookup"><span data-stu-id="bf847-119">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="bf847-120">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="bf847-120">-OriginGroupName</span></span>
<span data-ttu-id="bf847-121">Nome do grupo de origem cdn do Azure.</span><span class="sxs-lookup"><span data-stu-id="bf847-121">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="bf847-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bf847-122">-PassThru</span></span>
<span data-ttu-id="bf847-123">Retornar objeto, se especificado.</span><span class="sxs-lookup"><span data-stu-id="bf847-123">Return object if specified.</span></span>

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

### <span data-ttu-id="bf847-124">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="bf847-124">-ProfileName</span></span>
<span data-ttu-id="bf847-125">Nome do perfil cdn do Azure.</span><span class="sxs-lookup"><span data-stu-id="bf847-125">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="bf847-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf847-126">-ResourceGroupName</span></span>
<span data-ttu-id="bf847-127">O grupo de recursos do perfil cdn do Azure.</span><span class="sxs-lookup"><span data-stu-id="bf847-127">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="bf847-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bf847-128">-ResourceId</span></span>
<span data-ttu-id="bf847-129">A id de recurso do grupo de origem cdn do Azure.</span><span class="sxs-lookup"><span data-stu-id="bf847-129">The resource id of the Azure CDN origin group.</span></span>

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

### <span data-ttu-id="bf847-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bf847-130">-Confirm</span></span>
<span data-ttu-id="bf847-131">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf847-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf847-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf847-132">-WhatIf</span></span>
<span data-ttu-id="bf847-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="bf847-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf847-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="bf847-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf847-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf847-135">CommonParameters</span></span>
<span data-ttu-id="bf847-136">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf847-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf847-137">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bf847-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf847-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bf847-138">INPUTS</span></span>

### <span data-ttu-id="bf847-139">Nenhum</span><span class="sxs-lookup"><span data-stu-id="bf847-139">None</span></span>

## <span data-ttu-id="bf847-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="bf847-140">OUTPUTS</span></span>

### <span data-ttu-id="bf847-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bf847-141">System.Boolean</span></span>

## <span data-ttu-id="bf847-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="bf847-142">NOTES</span></span>

## <span data-ttu-id="bf847-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bf847-143">RELATED LINKS</span></span>
