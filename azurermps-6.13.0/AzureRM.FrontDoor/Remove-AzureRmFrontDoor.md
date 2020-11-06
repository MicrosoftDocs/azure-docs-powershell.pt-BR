---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/remove-azurermfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Remove-AzureRmFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Remove-AzureRmFrontDoor.md
ms.openlocfilehash: 8eae5034080bd1035cfe7e8331ca015820688e63
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93601969"
---
# <span data-ttu-id="130fd-101">Remove-AzureRmFrontDoor</span><span class="sxs-lookup"><span data-stu-id="130fd-101">Remove-AzureRmFrontDoor</span></span>

## <span data-ttu-id="130fd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="130fd-102">SYNOPSIS</span></span>
<span data-ttu-id="130fd-103">Remover o balanceador de carga da porta frontal</span><span class="sxs-lookup"><span data-stu-id="130fd-103">Remove Front Door load balancer</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="130fd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="130fd-104">SYNTAX</span></span>

### <span data-ttu-id="130fd-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="130fd-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzureRmFrontDoor -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="130fd-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="130fd-106">ByObjectParameterSet</span></span>
```
Remove-AzureRmFrontDoor -InputObject <PSFrontDoor> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="130fd-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="130fd-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmFrontDoor -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="130fd-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="130fd-108">DESCRIPTION</span></span>
<span data-ttu-id="130fd-109">O cmdlet **Remove-AzureRmFrontDoor** remove um balanceador de carga de porta frontal na assinatura atual</span><span class="sxs-lookup"><span data-stu-id="130fd-109">The **Remove-AzureRmFrontDoor** cmdlet removes a Front Door load balancer under the current subscription</span></span>

## <span data-ttu-id="130fd-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="130fd-110">EXAMPLES</span></span>

### <span data-ttu-id="130fd-111">Exemplo 1: remover "frontdoor1" no grupo de recursos "Rg1" na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="130fd-111">Example 1: Remove "frontdoor1" in resource group "rg1" under the current subscription.</span></span>
```powershell
PS C:\> Remove-AzureRmFrontDoor -Name "frontdoor1" -ResourceGroupName "rg1"
```

<span data-ttu-id="130fd-112">Remova "frontdoor1" no grupo de recursos "Rg1" na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="130fd-112">Remove "frontdoor1" in resource group "rg1" under the current subscription.</span></span>

### <span data-ttu-id="130fd-113">Exemplo 2: remover todas as FrontDoors no grupo de recursos "Rg1" na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="130fd-113">Example 2: Remove all FrontDoors in resource group "rg1" under the current subscription.</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoor -ResourceGroupName "rg1" | Remove-AzureRmFrontDoor
```

<span data-ttu-id="130fd-114">Remover todas as FrontDoors no grupo de recursos "Rg1" na assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="130fd-114">Remove all FrontDoors in resource group "rg1" under the current subscription.</span></span>

### <span data-ttu-id="130fd-115">Exemplo 3: remover todas as FrontDoors sob a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="130fd-115">Example 3: Remove all FrontDoors under the current subscription.</span></span>
```powershell
PS C:\> Get-AzureRmFrontDoor | Remove-AzureRmFrontDoor
```

<span data-ttu-id="130fd-116">Remover todas as FrontDoors sob a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="130fd-116">Remove all FrontDoors under the current subscription.</span></span>

### <span data-ttu-id="130fd-117">Exemplo 4: remover todos os FrontDoors com nome "frontdoor1" sob a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="130fd-117">Example 4: Remove all FrontDoors with name "frontdoor1" under the current subscription.</span></span>
```powershell
PS C:\> Remove-AzureRmFrontDoor -Name "frontdoor1" | Remove-AzureRmFrontDoor
```

<span data-ttu-id="130fd-118">Remova todos os FrontDoors com o nome "frontdoor1" sob a assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="130fd-118">Remove all FrontDoors with name "frontdoor1" under the current subscription.</span></span>

## <span data-ttu-id="130fd-119">OS</span><span class="sxs-lookup"><span data-stu-id="130fd-119">PARAMETERS</span></span>

### <span data-ttu-id="130fd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="130fd-120">-DefaultProfile</span></span>
<span data-ttu-id="130fd-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="130fd-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="130fd-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="130fd-122">-InputObject</span></span>
<span data-ttu-id="130fd-123">O objeto da porta frontal a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="130fd-123">The Front Door object to delete.</span></span>

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

### <span data-ttu-id="130fd-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="130fd-124">-Name</span></span>
<span data-ttu-id="130fd-125">O nome da porta frontal a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="130fd-125">The name of the Front Door to delete.</span></span>

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

### <span data-ttu-id="130fd-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="130fd-126">-PassThru</span></span>
<span data-ttu-id="130fd-127">Objeto de retorno (se especificado).</span><span class="sxs-lookup"><span data-stu-id="130fd-127">Return object (if specified).</span></span>

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

### <span data-ttu-id="130fd-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="130fd-128">-ResourceGroupName</span></span>
<span data-ttu-id="130fd-129">O grupo de recursos ao qual a porta frontal pertence.</span><span class="sxs-lookup"><span data-stu-id="130fd-129">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="130fd-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="130fd-130">-ResourceId</span></span>
<span data-ttu-id="130fd-131">ID do recurso da porta frontal a ser excluída</span><span class="sxs-lookup"><span data-stu-id="130fd-131">Resource Id of the Front Door to delete</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="130fd-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="130fd-132">-Confirm</span></span>
<span data-ttu-id="130fd-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="130fd-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="130fd-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="130fd-134">-WhatIf</span></span>
<span data-ttu-id="130fd-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="130fd-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="130fd-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="130fd-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="130fd-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="130fd-137">CommonParameters</span></span>
<span data-ttu-id="130fd-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="130fd-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="130fd-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="130fd-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="130fd-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="130fd-140">INPUTS</span></span>

### <span data-ttu-id="130fd-141">Microsoft. Azure. Commands. FrontDoor. Models. PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="130fd-141">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

### <span data-ttu-id="130fd-142">System. String</span><span class="sxs-lookup"><span data-stu-id="130fd-142">System.String</span></span>

### <span data-ttu-id="130fd-143">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="130fd-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="130fd-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="130fd-144">OUTPUTS</span></span>

### <span data-ttu-id="130fd-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="130fd-145">System.Boolean</span></span>

## <span data-ttu-id="130fd-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="130fd-146">NOTES</span></span>

## <span data-ttu-id="130fd-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="130fd-147">RELATED LINKS</span></span>

<span data-ttu-id="130fd-148">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md) 
 [Get-AzureRmFrontDoor](./Get-AzureRmFrontDoor.md)</span><span class="sxs-lookup"><span data-stu-id="130fd-148">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Get-AzureRmFrontDoor](./Get-AzureRmFrontDoor.md)</span></span>
