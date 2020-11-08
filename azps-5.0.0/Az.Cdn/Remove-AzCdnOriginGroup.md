---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/remove-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Remove-AzCdnOriginGroup.md
ms.openlocfilehash: 081d5a73d6bd3cefff6f0c3bc57d3e0190f785a7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94125037"
---
# <span data-ttu-id="68a3f-101">Remove-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="68a3f-101">Remove-AzCdnOriginGroup</span></span>

## <span data-ttu-id="68a3f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="68a3f-102">SYNOPSIS</span></span>
<span data-ttu-id="68a3f-103">Remove um grupo de origens CDN</span><span class="sxs-lookup"><span data-stu-id="68a3f-103">Removes a CDN origin group</span></span>

## <span data-ttu-id="68a3f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="68a3f-104">SYNTAX</span></span>

### <span data-ttu-id="68a3f-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="68a3f-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzCdnOriginGroup -OriginGroupName <String> -EndpointName <String> -ProfileName <String>
 -ResourceGroupName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="68a3f-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="68a3f-106">ByResourceIdParameterSet</span></span>
```
Remove-AzCdnOriginGroup -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68a3f-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="68a3f-107">ByObjectParameterSet</span></span>
```
Remove-AzCdnOriginGroup [-PassThru] -CdnOriginGroup <PSOriginGroup> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68a3f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="68a3f-108">DESCRIPTION</span></span>
<span data-ttu-id="68a3f-109">Remove-AzCdnOriginGroup removerá um grupo de origem CDN do ponto de extremidade especificado.</span><span class="sxs-lookup"><span data-stu-id="68a3f-109">Remove-AzCdnOriginGroup will remove a CDN origin group from the specified endpoint.</span></span> 

## <span data-ttu-id="68a3f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="68a3f-110">EXAMPLES</span></span>

### <span data-ttu-id="68a3f-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="68a3f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName
```

<span data-ttu-id="68a3f-112">Esse cmdlet removerá o grupo de origem especificado do ponto de extremidade fornecido.</span><span class="sxs-lookup"><span data-stu-id="68a3f-112">This cmdlet will remove the specified origin group from the given endpoint.</span></span> 

## <span data-ttu-id="68a3f-113">OS</span><span class="sxs-lookup"><span data-stu-id="68a3f-113">PARAMETERS</span></span>

### <span data-ttu-id="68a3f-114">-CdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="68a3f-114">-CdnOriginGroup</span></span>
<span data-ttu-id="68a3f-115">O objeto do grupo de origem CDN.</span><span class="sxs-lookup"><span data-stu-id="68a3f-115">The CDN origin group object.</span></span>

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

### <span data-ttu-id="68a3f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68a3f-116">-DefaultProfile</span></span>
<span data-ttu-id="68a3f-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="68a3f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="68a3f-118">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="68a3f-118">-EndpointName</span></span>
<span data-ttu-id="68a3f-119">Nome do ponto de extremidade CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="68a3f-119">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="68a3f-120">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="68a3f-120">-OriginGroupName</span></span>
<span data-ttu-id="68a3f-121">Nome do grupo de origens da CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="68a3f-121">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="68a3f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="68a3f-122">-PassThru</span></span>
<span data-ttu-id="68a3f-123">Objeto de retorno, se especificado.</span><span class="sxs-lookup"><span data-stu-id="68a3f-123">Return object if specified.</span></span>

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

### <span data-ttu-id="68a3f-124">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="68a3f-124">-ProfileName</span></span>
<span data-ttu-id="68a3f-125">Nome do perfil CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="68a3f-125">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="68a3f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68a3f-126">-ResourceGroupName</span></span>
<span data-ttu-id="68a3f-127">O grupo de recursos do perfil CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="68a3f-127">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="68a3f-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="68a3f-128">-ResourceId</span></span>
<span data-ttu-id="68a3f-129">A ID do recurso do grupo de origens da CDN do Azure.</span><span class="sxs-lookup"><span data-stu-id="68a3f-129">The resource id of the Azure CDN origin group.</span></span>

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

### <span data-ttu-id="68a3f-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="68a3f-130">-Confirm</span></span>
<span data-ttu-id="68a3f-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68a3f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="68a3f-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68a3f-132">-WhatIf</span></span>
<span data-ttu-id="68a3f-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="68a3f-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68a3f-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="68a3f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="68a3f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68a3f-135">CommonParameters</span></span>
<span data-ttu-id="68a3f-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68a3f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68a3f-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="68a3f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68a3f-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="68a3f-138">INPUTS</span></span>

### <span data-ttu-id="68a3f-139">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="68a3f-139">None</span></span>

## <span data-ttu-id="68a3f-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="68a3f-140">OUTPUTS</span></span>

### <span data-ttu-id="68a3f-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="68a3f-141">System.Boolean</span></span>

## <span data-ttu-id="68a3f-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="68a3f-142">NOTES</span></span>

## <span data-ttu-id="68a3f-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="68a3f-143">RELATED LINKS</span></span>
