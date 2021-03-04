---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/remove-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorWafPolicy.md
ms.openlocfilehash: 707f3157cead45d501cdfdaf357222cdaceac826
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901479"
---
# <span data-ttu-id="1ad9d-101">Remove-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="1ad9d-101">Remove-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="1ad9d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ad9d-102">SYNOPSIS</span></span>
<span data-ttu-id="1ad9d-103">Remover política WAF</span><span class="sxs-lookup"><span data-stu-id="1ad9d-103">Remove WAF policy</span></span>

## <span data-ttu-id="1ad9d-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="1ad9d-104">SYNTAX</span></span>

### <span data-ttu-id="1ad9d-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="1ad9d-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzFrontDoorWafPolicy -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ad9d-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ad9d-106">ByObjectParameterSet</span></span>
```
Remove-AzFrontDoorWafPolicy -InputObject <PSPolicy> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ad9d-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ad9d-107">ByResourceIdParameterSet</span></span>
```
Remove-AzFrontDoorWafPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ad9d-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="1ad9d-108">DESCRIPTION</span></span>
<span data-ttu-id="1ad9d-109">O cmdlet **Remove-AzFrontDoorWafPolicy** remove uma política WAF na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="1ad9d-109">The **Remove-AzFrontDoorWafPolicy** cmdlet removes a WAF policy under the current subscription</span></span>

## <span data-ttu-id="1ad9d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1ad9d-110">EXAMPLES</span></span>

### <span data-ttu-id="1ad9d-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1ad9d-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName
```

<span data-ttu-id="1ad9d-112">Remova a política WAF chamada $policyName no $resourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="1ad9d-112">Remove the WAF policy called $policyName in $resourceGroupName.</span></span>

### <span data-ttu-id="1ad9d-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="1ad9d-113">Example 2</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -ResourceGroupName $resourceGroupName | Remove-AzFrontDoorWafPolicy
```

<span data-ttu-id="1ad9d-114">Remova toda a política WAF no $resourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="1ad9d-114">Remove all WAF policy in $resourceGroupName.</span></span>

## <span data-ttu-id="1ad9d-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="1ad9d-115">PARAMETERS</span></span>

### <span data-ttu-id="1ad9d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ad9d-116">-DefaultProfile</span></span>
<span data-ttu-id="1ad9d-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1ad9d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ad9d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1ad9d-118">-InputObject</span></span>
<span data-ttu-id="1ad9d-119">O objeto de política WAF a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="1ad9d-119">The WAF policy object to delete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ad9d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="1ad9d-120">-Name</span></span>
<span data-ttu-id="1ad9d-121">O nome da política WAF a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="1ad9d-121">The name of the WAF policy to delete.</span></span>

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

### <span data-ttu-id="1ad9d-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1ad9d-122">-PassThru</span></span>
<span data-ttu-id="1ad9d-123">Objeto Return (se especificado).</span><span class="sxs-lookup"><span data-stu-id="1ad9d-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="1ad9d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ad9d-124">-ResourceGroupName</span></span>
<span data-ttu-id="1ad9d-125">O grupo de recursos ao qual a política WAF pertence.</span><span class="sxs-lookup"><span data-stu-id="1ad9d-125">The resource group to which the WAF policy belongs.</span></span>

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

### <span data-ttu-id="1ad9d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1ad9d-126">-ResourceId</span></span>
<span data-ttu-id="1ad9d-127">ID de recurso da política WAF a ser excluído</span><span class="sxs-lookup"><span data-stu-id="1ad9d-127">Resource Id of the WAF policy to delete</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ad9d-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1ad9d-128">-Confirm</span></span>
<span data-ttu-id="1ad9d-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1ad9d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ad9d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ad9d-130">-WhatIf</span></span>
<span data-ttu-id="1ad9d-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1ad9d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ad9d-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1ad9d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ad9d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ad9d-133">CommonParameters</span></span>
<span data-ttu-id="1ad9d-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ad9d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ad9d-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1ad9d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ad9d-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1ad9d-136">INPUTS</span></span>

### <span data-ttu-id="1ad9d-137">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span><span class="sxs-lookup"><span data-stu-id="1ad9d-137">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="1ad9d-138">System.String</span><span class="sxs-lookup"><span data-stu-id="1ad9d-138">System.String</span></span>

## <span data-ttu-id="1ad9d-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="1ad9d-139">OUTPUTS</span></span>

### <span data-ttu-id="1ad9d-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1ad9d-140">System.Boolean</span></span>

## <span data-ttu-id="1ad9d-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="1ad9d-141">NOTES</span></span>

## <span data-ttu-id="1ad9d-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1ad9d-142">RELATED LINKS</span></span>

<span data-ttu-id="1ad9d-143">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="1ad9d-143">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)</span></span>
