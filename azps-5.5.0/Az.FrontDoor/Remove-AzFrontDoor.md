---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoor.md
ms.openlocfilehash: 133afe9b64fd9161bb7d39fadf6349803f9e2282
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113199"
---
# <span data-ttu-id="d20ac-101">Remove-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="d20ac-101">Remove-AzFrontDoor</span></span>

## <span data-ttu-id="d20ac-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d20ac-102">SYNOPSIS</span></span>
<span data-ttu-id="d20ac-103">Remover o balanceador de carga da porta da frente</span><span class="sxs-lookup"><span data-stu-id="d20ac-103">Remove Front Door load balancer</span></span>

## <span data-ttu-id="d20ac-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d20ac-104">SYNTAX</span></span>

### <span data-ttu-id="d20ac-105">ByFieldsParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d20ac-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzFrontDoor -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d20ac-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d20ac-106">ByObjectParameterSet</span></span>
```
Remove-AzFrontDoor -InputObject <PSFrontDoor> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d20ac-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d20ac-107">ByResourceIdParameterSet</span></span>
```
Remove-AzFrontDoor -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d20ac-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="d20ac-108">DESCRIPTION</span></span>
<span data-ttu-id="d20ac-109">O **cmdlet Remove-AzFrontDoor** remove um balanceador de carga porta da frente sob a assinatura atual</span><span class="sxs-lookup"><span data-stu-id="d20ac-109">The **Remove-AzFrontDoor** cmdlet removes a Front Door load balancer under the current subscription</span></span>

## <span data-ttu-id="d20ac-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d20ac-110">EXAMPLES</span></span>

### <span data-ttu-id="d20ac-111">Exemplo 1: Remover "frontdoor1" no grupo de recursos "rg1" na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="d20ac-111">Example 1: Remove "frontdoor1" in resource group "rg1" under the current subscription.</span></span>
```powershell
PS C:\> Remove-AzFrontDoor -Name "frontdoor1" -ResourceGroupName "rg1"
```

<span data-ttu-id="d20ac-112">Remova "frontdoor1" no grupo de recursos "rg1" na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="d20ac-112">Remove "frontdoor1" in resource group "rg1" under the current subscription.</span></span>

### <span data-ttu-id="d20ac-113">Exemplo 2: Remover todos os FrontDoors no grupo de recursos "rg1" na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="d20ac-113">Example 2: Remove all FrontDoors in resource group "rg1" under the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor -ResourceGroupName "rg1" | Remove-AzFrontDoor
```

<span data-ttu-id="d20ac-114">Remova todos os FrontDoors no grupo de recursos "rg1" na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="d20ac-114">Remove all FrontDoors in resource group "rg1" under the current subscription.</span></span>

### <span data-ttu-id="d20ac-115">Exemplo 3: Remover todos os FrontDoors sob a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="d20ac-115">Example 3: Remove all FrontDoors under the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor | Remove-AzFrontDoor
```

<span data-ttu-id="d20ac-116">Remova todos os FrontDoors sob a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="d20ac-116">Remove all FrontDoors under the current subscription.</span></span>

### <span data-ttu-id="d20ac-117">Exemplo 4: Remover todos os FrontDoors com o nome "frontdoor1" na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="d20ac-117">Example 4: Remove all FrontDoors with name "frontdoor1" under the current subscription.</span></span>
```powershell
PS C:\> Remove-AzFrontDoor -Name "frontdoor1" | Remove-AzFrontDoor
```

<span data-ttu-id="d20ac-118">Remova todos os FrontDoors com o nome "frontdoor1" na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="d20ac-118">Remove all FrontDoors with name "frontdoor1" under the current subscription.</span></span>

## <span data-ttu-id="d20ac-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d20ac-119">PARAMETERS</span></span>

### <span data-ttu-id="d20ac-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d20ac-120">-DefaultProfile</span></span>
<span data-ttu-id="d20ac-121">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d20ac-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d20ac-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d20ac-122">-InputObject</span></span>
<span data-ttu-id="d20ac-123">O objeto Front Door a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="d20ac-123">The Front Door object to delete.</span></span>

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

### <span data-ttu-id="d20ac-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="d20ac-124">-Name</span></span>
<span data-ttu-id="d20ac-125">O nome da Porta da Frente a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="d20ac-125">The name of the Front Door to delete.</span></span>

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

### <span data-ttu-id="d20ac-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d20ac-126">-PassThru</span></span>
<span data-ttu-id="d20ac-127">Objeto return (se especificado).</span><span class="sxs-lookup"><span data-stu-id="d20ac-127">Return object (if specified).</span></span>

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

### <span data-ttu-id="d20ac-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d20ac-128">-ResourceGroupName</span></span>
<span data-ttu-id="d20ac-129">O grupo de recursos ao qual a Porta da Frente pertence.</span><span class="sxs-lookup"><span data-stu-id="d20ac-129">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="d20ac-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d20ac-130">-ResourceId</span></span>
<span data-ttu-id="d20ac-131">ID do Recurso da Porta da Frente para excluir</span><span class="sxs-lookup"><span data-stu-id="d20ac-131">Resource Id of the Front Door to delete</span></span>

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

### <span data-ttu-id="d20ac-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="d20ac-132">-Confirm</span></span>
<span data-ttu-id="d20ac-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d20ac-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d20ac-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d20ac-134">-WhatIf</span></span>
<span data-ttu-id="d20ac-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="d20ac-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d20ac-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d20ac-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d20ac-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d20ac-137">CommonParameters</span></span>
<span data-ttu-id="d20ac-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d20ac-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d20ac-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d20ac-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d20ac-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="d20ac-140">INPUTS</span></span>

### <span data-ttu-id="d20ac-141">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="d20ac-141">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

### <span data-ttu-id="d20ac-142">System.String</span><span class="sxs-lookup"><span data-stu-id="d20ac-142">System.String</span></span>

## <span data-ttu-id="d20ac-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="d20ac-143">OUTPUTS</span></span>

### <span data-ttu-id="d20ac-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d20ac-144">System.Boolean</span></span>

## <span data-ttu-id="d20ac-145">Notas</span><span class="sxs-lookup"><span data-stu-id="d20ac-145">NOTES</span></span>

## <span data-ttu-id="d20ac-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d20ac-146">RELATED LINKS</span></span>

<span data-ttu-id="d20ac-147">[Novo-AzFrontDoor](./New-AzFrontDoor.md) 
 [Get-AzFrontDoor](./Get-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="d20ac-147">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Get-AzFrontDoor](./Get-AzFrontDoor.md)</span></span>