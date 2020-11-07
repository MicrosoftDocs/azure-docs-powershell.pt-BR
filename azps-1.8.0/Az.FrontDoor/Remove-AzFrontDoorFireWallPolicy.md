---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/remove-azfrontdoorfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorFireWallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Remove-AzFrontDoorFireWallPolicy.md
ms.openlocfilehash: f081d403a47f457c48320238436d72ca4ebd15fe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770842"
---
# <span data-ttu-id="6fba8-101">Remove-AzFrontDoorFireWallPolicy</span><span class="sxs-lookup"><span data-stu-id="6fba8-101">Remove-AzFrontDoorFireWallPolicy</span></span>

## <span data-ttu-id="6fba8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6fba8-102">SYNOPSIS</span></span>
<span data-ttu-id="6fba8-103">Remover política WAF</span><span class="sxs-lookup"><span data-stu-id="6fba8-103">Remove WAF policy</span></span>

## <span data-ttu-id="6fba8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6fba8-104">SYNTAX</span></span>

### <span data-ttu-id="6fba8-105">ByFieldsParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="6fba8-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzFrontDoorFireWallPolicy -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fba8-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6fba8-106">ByObjectParameterSet</span></span>
```
Remove-AzFrontDoorFireWallPolicy -InputObject <PSPolicy> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fba8-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6fba8-107">ByResourceIdParameterSet</span></span>
```
Remove-AzFrontDoorFireWallPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6fba8-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6fba8-108">DESCRIPTION</span></span>
<span data-ttu-id="6fba8-109">O cmdlet **Remove-AzFrontDoorFireWallPolicy** remove uma política WAF sob a assinatura atual</span><span class="sxs-lookup"><span data-stu-id="6fba8-109">The **Remove-AzFrontDoorFireWallPolicy** cmdlet removes a WAF policy under the current subscription</span></span>

## <span data-ttu-id="6fba8-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6fba8-110">EXAMPLES</span></span>

### <span data-ttu-id="6fba8-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6fba8-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzFrontDoorFireWallPolicy -Name $policyName -ResourceGroupName $resourceGroupName
```

<span data-ttu-id="6fba8-112">Remova a política WAF chamada $policyName em $resourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="6fba8-112">Remove the WAF policy called $policyName in $resourceGroupName.</span></span>

### <span data-ttu-id="6fba8-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="6fba8-113">Example 2</span></span>
```powershell
PS C:\> Get-AzFrontDoorFireWallPolicy -ResourceGroupName $resourceGroupName | Remove-AzFrontDoorFireWallPolicy
```

<span data-ttu-id="6fba8-114">Remover toda a política WAF em $resourceGroupName.</span><span class="sxs-lookup"><span data-stu-id="6fba8-114">Remove all WAF policy in $resourceGroupName.</span></span>

## <span data-ttu-id="6fba8-115">OS</span><span class="sxs-lookup"><span data-stu-id="6fba8-115">PARAMETERS</span></span>

### <span data-ttu-id="6fba8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fba8-116">-DefaultProfile</span></span>
<span data-ttu-id="6fba8-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6fba8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fba8-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6fba8-118">-InputObject</span></span>
<span data-ttu-id="6fba8-119">O objeto de política WAF a ser excluído.</span><span class="sxs-lookup"><span data-stu-id="6fba8-119">The WAF policy object to delete.</span></span>

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

### <span data-ttu-id="6fba8-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="6fba8-120">-Name</span></span>
<span data-ttu-id="6fba8-121">O nome da política WAF a ser excluída.</span><span class="sxs-lookup"><span data-stu-id="6fba8-121">The name of the WAF policy to delete.</span></span>

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

### <span data-ttu-id="6fba8-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6fba8-122">-PassThru</span></span>
<span data-ttu-id="6fba8-123">Objeto de retorno (se especificado).</span><span class="sxs-lookup"><span data-stu-id="6fba8-123">Return object (if specified).</span></span>

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

### <span data-ttu-id="6fba8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fba8-124">-ResourceGroupName</span></span>
<span data-ttu-id="6fba8-125">O grupo de recursos ao qual a política de WAF pertence.</span><span class="sxs-lookup"><span data-stu-id="6fba8-125">The resource group to which the WAF policy belongs.</span></span>

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

### <span data-ttu-id="6fba8-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6fba8-126">-ResourceId</span></span>
<span data-ttu-id="6fba8-127">ID do recurso da política WAF para excluir</span><span class="sxs-lookup"><span data-stu-id="6fba8-127">Resource Id of the WAF policy to delete</span></span>

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

### <span data-ttu-id="6fba8-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6fba8-128">-Confirm</span></span>
<span data-ttu-id="6fba8-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6fba8-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fba8-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fba8-130">-WhatIf</span></span>
<span data-ttu-id="6fba8-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6fba8-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6fba8-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6fba8-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fba8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fba8-133">CommonParameters</span></span>
<span data-ttu-id="6fba8-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fba8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fba8-135">Para obter mais informações, consulte [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6fba8-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fba8-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6fba8-136">INPUTS</span></span>

### <span data-ttu-id="6fba8-137">Microsoft. Azure. Commands. FrontDoor. Models. PSPolicy</span><span class="sxs-lookup"><span data-stu-id="6fba8-137">Microsoft.Azure.Commands.FrontDoor.Models.PSPolicy</span></span>

### <span data-ttu-id="6fba8-138">System. String</span><span class="sxs-lookup"><span data-stu-id="6fba8-138">System.String</span></span>

## <span data-ttu-id="6fba8-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6fba8-139">OUTPUTS</span></span>

### <span data-ttu-id="6fba8-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6fba8-140">System.Boolean</span></span>

## <span data-ttu-id="6fba8-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6fba8-141">NOTES</span></span>

## <span data-ttu-id="6fba8-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6fba8-142">RELATED LINKS</span></span>

<span data-ttu-id="6fba8-143">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md) 
 [Get-AzFrontDoorFireWallPolicy](./Get-AzFrontDoorFireWallPolicy.md)</span><span class="sxs-lookup"><span data-stu-id="6fba8-143">[New-AzFrontDoorFireWallPolicy](./New-AzFrontDoorFireWallPolicy.md)
[Get-AzFrontDoorFireWallPolicy](./Get-AzFrontDoorFireWallPolicy.md)</span></span>
