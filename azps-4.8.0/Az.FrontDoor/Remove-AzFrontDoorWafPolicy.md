---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorWafPolicy.md
ms.openlocfilehash: ec68316ecac3921f37641b83f45b9bd922e90b46
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93947748"
---
# <span data-ttu-id="60b8c-101">Remove-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="60b8c-101">Remove-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="60b8c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="60b8c-102">SYNOPSIS</span></span>
<span data-ttu-id="60b8c-103">Remover política WAF</span><span class="sxs-lookup"><span data-stu-id="60b8c-103">Remove WAF policy</span></span>

## <span data-ttu-id="60b8c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="60b8c-104">SYNTAX</span></span>

### <span data-ttu-id="60b8c-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="60b8c-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzFrontDoorWafPolicy -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60b8c-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="60b8c-106">ByObjectParameterSet</span></span>
```
Remove-AzFrontDoorWafPolicy -InputObject <PSPolicy> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60b8c-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="60b8c-107">ByResourceIdParameterSet</span></span>
```
Remove-AzFrontDoorWafPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60b8c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="60b8c-108">DESCRIPTION</span></span>
<span data-ttu-id="60b8c-109">O cmdlet **Remove-AzFrontDoorWafPolicy** remove uma política WAF sob a assinatura atual</span><span class="sxs-lookup"><span data-stu-id="60b8c-109">The **Remove-AzFrontDoorWafPolicy** cmdlet removes a WAF policy under the current subscription</span></span>

## <span data-ttu-id="60b8c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="60b8c-110">EXAMPLES</span></span>

### <span data-ttu-id="60b8c-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="60b8c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName
```

<span data-ttu-id="60b8c-112">Remova a política WAF chamada $policyName em $resourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="60b8c-112">Remove the WAF policy called $policyName in $resourceGroupName.</span></span>

### <span data-ttu-id="60b8c-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="60b8c-113">Example 2</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -ResourceGroupName $resourceGroupName | Remove-AzFrontDoorWafPolicy
```

<span data-ttu-id="60b8c-114">Remover toda a política WAF em $resourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="60b8c-114">Remove all WAF policy in $resourceGroupName.</span></span>

## <span data-ttu-id="60b8c-115">OS</span><span class="sxs-lookup"><span data-stu-id="60b8c-115">PARAMETERS</span></span>

### <span data-ttu-id="60b8c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60b8c-116">-DefaultProfile</span></span>
<span data-ttu-id="60b8c-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="60b8c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60b8c-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="60b8c-118">-InputObject</span></span>
<span data-ttu-id="60b8c-119">O objeto de política WAF a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="60b8c-119">The WAF policy object to delete.</span></span>

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

### <span data-ttu-id="60b8c-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="60b8c-120">-Name</span></span>
<span data-ttu-id="60b8c-121">O nome da política WAF a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="60b8c-121">The name of the WAF policy to delete.</span></span>

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

### <span data-ttu-id="60b8c-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="60b8c-122">-PassThru</span></span>
<span data-ttu-id="60b8c-123">Objeto de retorno (se especificado).</span><span class="sxs-lookup"><span data-stu-id="60b8c-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="60b8c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60b8c-124">-ResourceGroupName</span></span>
<span data-ttu-id="60b8c-125">O grupo de recursos ao qual a política de WAF pertence.</span><span class="sxs-lookup"><span data-stu-id="60b8c-125">The resource group to which the WAF policy belongs.</span></span>

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

### <span data-ttu-id="60b8c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="60b8c-126">-ResourceId</span></span>
<span data-ttu-id="60b8c-127">ID do recurso da política WAF para excluir</span><span class="sxs-lookup"><span data-stu-id="60b8c-127">Resource Id of the WAF policy to delete</span></span>

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

### <span data-ttu-id="60b8c-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="60b8c-128">-Confirm</span></span>
<span data-ttu-id="60b8c-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60b8c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60b8c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60b8c-130">-WhatIf</span></span>
<span data-ttu-id="60b8c-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="60b8c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60b8c-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="60b8c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60b8c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60b8c-133">CommonParameters</span></span>
<span data-ttu-id="60b8c-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60b8c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60b8c-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="60b8c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60b8c-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="60b8c-136">INPUTS</span></span>

### <span data-ttu-id="60b8c-137">Microsoft. Azure. Commands. FrontDoor. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="60b8c-137">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="60b8c-138">System. String</span><span class="sxs-lookup"><span data-stu-id="60b8c-138">System.String</span></span>

## <span data-ttu-id="60b8c-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="60b8c-139">OUTPUTS</span></span>

### <span data-ttu-id="60b8c-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="60b8c-140">System.Boolean</span></span>

## <span data-ttu-id="60b8c-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="60b8c-141">NOTES</span></span>

## <span data-ttu-id="60b8c-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="60b8c-142">RELATED LINKS</span></span>

<span data-ttu-id="60b8c-143">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="60b8c-143">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)</span></span>
