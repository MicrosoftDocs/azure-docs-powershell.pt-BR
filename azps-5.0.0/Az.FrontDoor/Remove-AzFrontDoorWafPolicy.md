---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoorwafpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorWafPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorWafPolicy.md
ms.openlocfilehash: ec68316ecac3921f37641b83f45b9bd922e90b46
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115441"
---
# <span data-ttu-id="6710d-101">Remove-AzFrontDoorWafPolicy</span><span class="sxs-lookup"><span data-stu-id="6710d-101">Remove-AzFrontDoorWafPolicy</span></span>

## <span data-ttu-id="6710d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6710d-102">SYNOPSIS</span></span>
<span data-ttu-id="6710d-103">Remover política WAF</span><span class="sxs-lookup"><span data-stu-id="6710d-103">Remove WAF policy</span></span>

## <span data-ttu-id="6710d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6710d-104">SYNTAX</span></span>

### <span data-ttu-id="6710d-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="6710d-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzFrontDoorWafPolicy -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6710d-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6710d-106">ByObjectParameterSet</span></span>
```
Remove-AzFrontDoorWafPolicy -InputObject <PSPolicy> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6710d-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6710d-107">ByResourceIdParameterSet</span></span>
```
Remove-AzFrontDoorWafPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6710d-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6710d-108">DESCRIPTION</span></span>
<span data-ttu-id="6710d-109">O cmdlet **Remove-AzFrontDoorWafPolicy** remove uma política WAF sob a assinatura atual</span><span class="sxs-lookup"><span data-stu-id="6710d-109">The **Remove-AzFrontDoorWafPolicy** cmdlet removes a WAF policy under the current subscription</span></span>

## <span data-ttu-id="6710d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6710d-110">EXAMPLES</span></span>

### <span data-ttu-id="6710d-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6710d-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzFrontDoorWafPolicy -Name $policyName -ResourceGroupName $resourceGroupName
```

<span data-ttu-id="6710d-112">Remova a política WAF chamada $policyName em $resourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="6710d-112">Remove the WAF policy called $policyName in $resourceGroupName.</span></span>

### <span data-ttu-id="6710d-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="6710d-113">Example 2</span></span>
```powershell
PS C:\> Get-AzFrontDoorWafPolicy -ResourceGroupName $resourceGroupName | Remove-AzFrontDoorWafPolicy
```

<span data-ttu-id="6710d-114">Remover toda a política WAF em $resourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="6710d-114">Remove all WAF policy in $resourceGroupName.</span></span>

## <span data-ttu-id="6710d-115">OS</span><span class="sxs-lookup"><span data-stu-id="6710d-115">PARAMETERS</span></span>

### <span data-ttu-id="6710d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6710d-116">-DefaultProfile</span></span>
<span data-ttu-id="6710d-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6710d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6710d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6710d-118">-InputObject</span></span>
<span data-ttu-id="6710d-119">O objeto de política WAF a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="6710d-119">The WAF policy object to delete.</span></span>

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

### <span data-ttu-id="6710d-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="6710d-120">-Name</span></span>
<span data-ttu-id="6710d-121">O nome da política WAF a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="6710d-121">The name of the WAF policy to delete.</span></span>

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

### <span data-ttu-id="6710d-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6710d-122">-PassThru</span></span>
<span data-ttu-id="6710d-123">Objeto de retorno (se especificado).</span><span class="sxs-lookup"><span data-stu-id="6710d-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="6710d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6710d-124">-ResourceGroupName</span></span>
<span data-ttu-id="6710d-125">O grupo de recursos ao qual a política de WAF pertence.</span><span class="sxs-lookup"><span data-stu-id="6710d-125">The resource group to which the WAF policy belongs.</span></span>

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

### <span data-ttu-id="6710d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6710d-126">-ResourceId</span></span>
<span data-ttu-id="6710d-127">ID do recurso da política WAF para excluir</span><span class="sxs-lookup"><span data-stu-id="6710d-127">Resource Id of the WAF policy to delete</span></span>

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

### <span data-ttu-id="6710d-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6710d-128">-Confirm</span></span>
<span data-ttu-id="6710d-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6710d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6710d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6710d-130">-WhatIf</span></span>
<span data-ttu-id="6710d-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6710d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6710d-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6710d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6710d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6710d-133">CommonParameters</span></span>
<span data-ttu-id="6710d-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6710d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6710d-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6710d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6710d-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6710d-136">INPUTS</span></span>

### <span data-ttu-id="6710d-137">Microsoft. Azure. Commands. FrontDoor. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="6710d-137">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="6710d-138">System. String</span><span class="sxs-lookup"><span data-stu-id="6710d-138">System.String</span></span>

## <span data-ttu-id="6710d-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6710d-139">OUTPUTS</span></span>

### <span data-ttu-id="6710d-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6710d-140">System.Boolean</span></span>

## <span data-ttu-id="6710d-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6710d-141">NOTES</span></span>

## <span data-ttu-id="6710d-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6710d-142">RELATED LINKS</span></span>

<span data-ttu-id="6710d-143">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md) 
 [Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="6710d-143">[New-AzFrontDoorWafPolicy](./New-AzFrontDoorWafPolicy.md)
[Get-AzFrontDoorWafPolicy](./Get-AzFrontDoorWafPolicy.md)</span></span>
