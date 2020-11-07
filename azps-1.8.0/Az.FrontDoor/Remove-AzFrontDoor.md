---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoor.md
ms.openlocfilehash: fbbd2b5047811f09a8142eea2a84e8f77c405be3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770846"
---
# <span data-ttu-id="ed5ce-101">Remove-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="ed5ce-101">Remove-AzFrontDoor</span></span>

## <span data-ttu-id="ed5ce-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ed5ce-102">SYNOPSIS</span></span>
<span data-ttu-id="ed5ce-103">Remover o balanceador de carga da porta frontal</span><span class="sxs-lookup"><span data-stu-id="ed5ce-103">Remove Front Door load balancer</span></span>

## <span data-ttu-id="ed5ce-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ed5ce-104">SYNTAX</span></span>

### <span data-ttu-id="ed5ce-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="ed5ce-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzFrontDoor -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed5ce-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed5ce-106">ByObjectParameterSet</span></span>
```
Remove-AzFrontDoor -InputObject <PSFrontDoor> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed5ce-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed5ce-107">ByResourceIdParameterSet</span></span>
```
Remove-AzFrontDoor -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed5ce-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ed5ce-108">DESCRIPTION</span></span>
<span data-ttu-id="ed5ce-109">O cmdlet **Remove-AzFrontDoor** remove um balanceador de carga de porta frontal na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="ed5ce-109">The **Remove-AzFrontDoor** cmdlet removes a Front Door load balancer under the current subscription</span></span>

## <span data-ttu-id="ed5ce-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ed5ce-110">EXAMPLES</span></span>

### <span data-ttu-id="ed5ce-111">Exemplo 1: remover "frontdoor1" no grupo de recursos "Rg1" na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="ed5ce-111">Example 1: Remove "frontdoor1" in resource group "rg1" under the current subscription.</span></span>
```powershell
PS C:\> Remove-AzFrontDoor -Name "frontdoor1" -ResourceGroupName "rg1"
```

<span data-ttu-id="ed5ce-112">Remova "frontdoor1" no grupo de recursos "Rg1" na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="ed5ce-112">Remove "frontdoor1" in resource group "rg1" under the current subscription.</span></span>

### <span data-ttu-id="ed5ce-113">Exemplo 2: remover todas as FrontDoors no grupo de recursos "Rg1" na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="ed5ce-113">Example 2: Remove all FrontDoors in resource group "rg1" under the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor -ResourceGroupName "rg1" | Remove-AzFrontDoor
```

<span data-ttu-id="ed5ce-114">Remover todas as FrontDoors no grupo de recursos "Rg1" na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="ed5ce-114">Remove all FrontDoors in resource group "rg1" under the current subscription.</span></span>

### <span data-ttu-id="ed5ce-115">Exemplo 3: remover todas as FrontDoors sob a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="ed5ce-115">Example 3: Remove all FrontDoors under the current subscription.</span></span>
```powershell
PS C:\> Get-AzFrontDoor | Remove-AzFrontDoor
```

<span data-ttu-id="ed5ce-116">Remover todas as FrontDoors sob a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="ed5ce-116">Remove all FrontDoors under the current subscription.</span></span>

### <span data-ttu-id="ed5ce-117">Exemplo 4: remover todos os FrontDoors com nome "frontdoor1" sob a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="ed5ce-117">Example 4: Remove all FrontDoors with name "frontdoor1" under the current subscription.</span></span>
```powershell
PS C:\> Remove-AzFrontDoor -Name "frontdoor1" | Remove-AzFrontDoor
```

<span data-ttu-id="ed5ce-118">Remova todos os FrontDoors com o nome "frontdoor1" sob a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="ed5ce-118">Remove all FrontDoors with name "frontdoor1" under the current subscription.</span></span>

## <span data-ttu-id="ed5ce-119">OS</span><span class="sxs-lookup"><span data-stu-id="ed5ce-119">PARAMETERS</span></span>

### <span data-ttu-id="ed5ce-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed5ce-120">-DefaultProfile</span></span>
<span data-ttu-id="ed5ce-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ed5ce-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed5ce-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ed5ce-122">-InputObject</span></span>
<span data-ttu-id="ed5ce-123">O objeto da porta frontal a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="ed5ce-123">The Front Door object to delete.</span></span>

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

### <span data-ttu-id="ed5ce-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="ed5ce-124">-Name</span></span>
<span data-ttu-id="ed5ce-125">O nome da porta frontal a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="ed5ce-125">The name of the Front Door to delete.</span></span>

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

### <span data-ttu-id="ed5ce-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ed5ce-126">-PassThru</span></span>
<span data-ttu-id="ed5ce-127">Objeto de retorno (se especificado).</span><span class="sxs-lookup"><span data-stu-id="ed5ce-127">Return object (if specified).</span></span>

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

### <span data-ttu-id="ed5ce-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed5ce-128">-ResourceGroupName</span></span>
<span data-ttu-id="ed5ce-129">O grupo de recursos ao qual a porta frontal pertence.</span><span class="sxs-lookup"><span data-stu-id="ed5ce-129">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="ed5ce-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed5ce-130">-ResourceId</span></span>
<span data-ttu-id="ed5ce-131">ID do recurso da porta frontal a ser excluída</span><span class="sxs-lookup"><span data-stu-id="ed5ce-131">Resource Id of the Front Door to delete</span></span>

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

### <span data-ttu-id="ed5ce-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ed5ce-132">-Confirm</span></span>
<span data-ttu-id="ed5ce-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed5ce-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed5ce-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed5ce-134">-WhatIf</span></span>
<span data-ttu-id="ed5ce-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ed5ce-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed5ce-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ed5ce-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed5ce-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed5ce-137">CommonParameters</span></span>
<span data-ttu-id="ed5ce-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed5ce-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed5ce-139">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ed5ce-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed5ce-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ed5ce-140">INPUTS</span></span>

### <span data-ttu-id="ed5ce-141">Microsoft. Azure. Commands. FrontDoor. Models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="ed5ce-141">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

### <span data-ttu-id="ed5ce-142">System. String</span><span class="sxs-lookup"><span data-stu-id="ed5ce-142">System.String</span></span>

## <span data-ttu-id="ed5ce-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ed5ce-143">OUTPUTS</span></span>

### <span data-ttu-id="ed5ce-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ed5ce-144">System.Boolean</span></span>

## <span data-ttu-id="ed5ce-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ed5ce-145">NOTES</span></span>

## <span data-ttu-id="ed5ce-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ed5ce-146">RELATED LINKS</span></span>

<span data-ttu-id="ed5ce-147">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Get-AzFrontDoor](./Get-AzFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="ed5ce-147">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Get-AzFrontDoor](./Get-AzFrontDoor.md)</span></span>