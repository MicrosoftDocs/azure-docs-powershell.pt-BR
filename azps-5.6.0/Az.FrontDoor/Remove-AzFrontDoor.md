---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/remove-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoor.md
ms.openlocfilehash: 79307a12fbcf5be02d9ea356f41398f76e292379
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901482"
---
# <span data-ttu-id="cc963-101">Remove-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="cc963-101">Remove-AzFrontDoor</span></span>

## <span data-ttu-id="cc963-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc963-102">SYNOPSIS</span></span>
<span data-ttu-id="cc963-103">Remover balanceador de carga da porta frontal</span><span class="sxs-lookup"><span data-stu-id="cc963-103">Remove Front Door load balancer</span></span>

## <span data-ttu-id="cc963-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="cc963-104">SYNTAX</span></span>

### <span data-ttu-id="cc963-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="cc963-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzFrontDoor -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc963-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc963-106">ByObjectParameterSet</span></span>
```
Remove-AzFrontDoor -InputObject <PSFrontDoor> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc963-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc963-107">ByResourceIdParameterSet</span></span>
```
Remove-AzFrontDoor -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc963-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="cc963-108">DESCRIPTION</span></span>
<span data-ttu-id="cc963-109">O cmdlet **Remove-AzFrontDoor** remove um balanceador de carga da Porta Da Frente sob a assinatura atual</span><span class="sxs-lookup"><span data-stu-id="cc963-109">The **Remove-AzFrontDoor** cmdlet removes a Front Door load balancer under the current subscription</span></span>

## <span data-ttu-id="cc963-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cc963-110">EXAMPLES</span></span>

### <span data-ttu-id="cc963-111">Exemplo 1: Remover "frontdoor1" no grupo de recursos "rg1" na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="cc963-111">Example 1: Remove "frontdoor1" in resource group "rg1" under the current subscription.</span></span>
```powershell
PS C:\> Remove-AzFrontDoor -Name "frontdoor1" -ResourceGroupName "rg1"
```

<span data-ttu-id="cc963-112">Remova "frontdoor1" no grupo de recursos "rg1" na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="cc963-112">Remove "frontdoor1" in resource group "rg1" under the current subscription.</span></span>

### <span data-ttu-id="cc963-113">Exemplo 2: Remover todos os FrontDoors no grupo de recursos "rg1" na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="cc963-113">Example 2: Remove all FrontDoors in resource group "rg1" under the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor -ResourceGroupName "rg1" | Remove-AzFrontDoor
```

<span data-ttu-id="cc963-114">Remova todos os FrontDoors no grupo de recursos "rg1" na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="cc963-114">Remove all FrontDoors in resource group "rg1" under the current subscription.</span></span>

### <span data-ttu-id="cc963-115">Exemplo 3: Remover todos os FrontDoors sob a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="cc963-115">Example 3: Remove all FrontDoors under the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor | Remove-AzFrontDoor
```

<span data-ttu-id="cc963-116">Remova todos os FrontDoors sob a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="cc963-116">Remove all FrontDoors under the current subscription.</span></span>

### <span data-ttu-id="cc963-117">Exemplo 4: Remova todos os FrontDoors com o nome "frontdoor1" na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="cc963-117">Example 4: Remove all FrontDoors with name "frontdoor1" under the current subscription.</span></span>
```powershell
PS C:\> Remove-AzFrontDoor -Name "frontdoor1" | Remove-AzFrontDoor
```

<span data-ttu-id="cc963-118">Remova todos os FrontDoors com o nome "frontdoor1" na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="cc963-118">Remove all FrontDoors with name "frontdoor1" under the current subscription.</span></span>

## <span data-ttu-id="cc963-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="cc963-119">PARAMETERS</span></span>

### <span data-ttu-id="cc963-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc963-120">-DefaultProfile</span></span>
<span data-ttu-id="cc963-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="cc963-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc963-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cc963-122">-InputObject</span></span>
<span data-ttu-id="cc963-123">O objeto Front Door a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="cc963-123">The Front Door object to delete.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc963-124">-Name</span><span class="sxs-lookup"><span data-stu-id="cc963-124">-Name</span></span>
<span data-ttu-id="cc963-125">O nome da Porta da Frente a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="cc963-125">The name of the Front Door to delete.</span></span>

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

### <span data-ttu-id="cc963-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cc963-126">-PassThru</span></span>
<span data-ttu-id="cc963-127">Objeto Return (se especificado).</span><span class="sxs-lookup"><span data-stu-id="cc963-127">Return object (if specified).</span></span>

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

### <span data-ttu-id="cc963-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc963-128">-ResourceGroupName</span></span>
<span data-ttu-id="cc963-129">O grupo de recursos ao qual a Porta da Frente pertence.</span><span class="sxs-lookup"><span data-stu-id="cc963-129">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="cc963-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cc963-130">-ResourceId</span></span>
<span data-ttu-id="cc963-131">ID de recurso da Porta da Frente para excluir</span><span class="sxs-lookup"><span data-stu-id="cc963-131">Resource Id of the Front Door to delete</span></span>

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

### <span data-ttu-id="cc963-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cc963-132">-Confirm</span></span>
<span data-ttu-id="cc963-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc963-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc963-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc963-134">-WhatIf</span></span>
<span data-ttu-id="cc963-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="cc963-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc963-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="cc963-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc963-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc963-137">CommonParameters</span></span>
<span data-ttu-id="cc963-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc963-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc963-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cc963-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc963-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cc963-140">INPUTS</span></span>

### <span data-ttu-id="cc963-141">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="cc963-141">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

### <span data-ttu-id="cc963-142">System.String</span><span class="sxs-lookup"><span data-stu-id="cc963-142">System.String</span></span>

## <span data-ttu-id="cc963-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="cc963-143">OUTPUTS</span></span>

### <span data-ttu-id="cc963-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cc963-144">System.Boolean</span></span>

## <span data-ttu-id="cc963-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="cc963-145">NOTES</span></span>

## <span data-ttu-id="cc963-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cc963-146">RELATED LINKS</span></span>

<span data-ttu-id="cc963-147">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Get-AzFrontDoor](./Get-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="cc963-147">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Get-AzFrontDoor](./Get-AzFrontDoor.md)</span></span>