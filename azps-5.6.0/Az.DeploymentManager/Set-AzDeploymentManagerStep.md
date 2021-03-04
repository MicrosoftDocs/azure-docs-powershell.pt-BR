---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/set-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerStep.md
ms.openlocfilehash: f8412ac037372d89373c64c77f43c10db1730100
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887164"
---
# <span data-ttu-id="658d6-101">Set-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="658d6-101">Set-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="658d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="658d6-102">SYNOPSIS</span></span>
<span data-ttu-id="658d6-103">Atualiza a etapa.</span><span class="sxs-lookup"><span data-stu-id="658d6-103">Updates the step.</span></span>

## <span data-ttu-id="658d6-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="658d6-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerStep [-InputObject] <PSStepResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="658d6-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="658d6-105">DESCRIPTION</span></span>
<span data-ttu-id="658d6-106">O cmdlet **Set-AzDeploymentManagerStep** atualiza uma etapa com o objeto step especificado.</span><span class="sxs-lookup"><span data-stu-id="658d6-106">The **Set-AzDeploymentManagerStep** cmdlet updates a step with the specified step object.</span></span>
<span data-ttu-id="658d6-107">O cmdlet retorna o objeto step atualizado.</span><span class="sxs-lookup"><span data-stu-id="658d6-107">The cmdlet returns the updated step object.</span></span>

## <span data-ttu-id="658d6-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="658d6-108">EXAMPLES</span></span>

### <span data-ttu-id="658d6-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="658d6-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerStep -InputObject $stepObject
```

<span data-ttu-id="658d6-110">Este comando atualiza uma etapa cujo nome e ResourceGroup corresponderem às propriedades Name e ResourceGroupName do $stepObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="658d6-110">This command updates a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>
<span data-ttu-id="658d6-111">A etapa seria atualizada para as propriedades definidas no $stepObject.</span><span class="sxs-lookup"><span data-stu-id="658d6-111">The step would be updated to the properties set in the $stepObject.</span></span>

## <span data-ttu-id="658d6-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="658d6-112">PARAMETERS</span></span>

### <span data-ttu-id="658d6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="658d6-113">-DefaultProfile</span></span>
<span data-ttu-id="658d6-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="658d6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="658d6-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="658d6-115">-InputObject</span></span>
<span data-ttu-id="658d6-116">O objeto step.</span><span class="sxs-lookup"><span data-stu-id="658d6-116">The step object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="658d6-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="658d6-117">-Confirm</span></span>
<span data-ttu-id="658d6-118">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="658d6-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="658d6-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="658d6-119">-WhatIf</span></span>
<span data-ttu-id="658d6-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="658d6-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="658d6-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="658d6-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="658d6-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="658d6-122">CommonParameters</span></span>
<span data-ttu-id="658d6-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="658d6-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="658d6-124">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="658d6-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="658d6-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="658d6-125">INPUTS</span></span>

### <span data-ttu-id="658d6-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span><span class="sxs-lookup"><span data-stu-id="658d6-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="658d6-127">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="658d6-127">OUTPUTS</span></span>

### <span data-ttu-id="658d6-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span><span class="sxs-lookup"><span data-stu-id="658d6-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="658d6-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="658d6-129">NOTES</span></span>

## <span data-ttu-id="658d6-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="658d6-130">RELATED LINKS</span></span>
