---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerStep.md
ms.openlocfilehash: 2cd73cad57f36130ed11e37ad6dc2147e6c081ae
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127020"
---
# <span data-ttu-id="f781c-101">Set-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="f781c-101">Set-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="f781c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f781c-102">SYNOPSIS</span></span>
<span data-ttu-id="f781c-103">Atualiza a etapa.</span><span class="sxs-lookup"><span data-stu-id="f781c-103">Updates the step.</span></span>

## <span data-ttu-id="f781c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f781c-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerStep [-InputObject] <PSStepResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f781c-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="f781c-105">DESCRIPTION</span></span>
<span data-ttu-id="f781c-106">O cmdlet **Set-AzDeploymentManagerStep** atualiza uma etapa com o objeto de etapa especificado.</span><span class="sxs-lookup"><span data-stu-id="f781c-106">The **Set-AzDeploymentManagerStep** cmdlet updates a step with the specified step object.</span></span>
<span data-ttu-id="f781c-107">O cmdlet retorna o objeto de etapa atualizado.</span><span class="sxs-lookup"><span data-stu-id="f781c-107">The cmdlet returns the updated step object.</span></span>

## <span data-ttu-id="f781c-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f781c-108">EXAMPLES</span></span>

### <span data-ttu-id="f781c-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f781c-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerStep -InputObject $stepObject
```

<span data-ttu-id="f781c-110">Esse comando atualiza uma etapa cujo nome e Grupo de Recursos corresponderem às propriedades Nome e NomeDoGrupo de Recursos do $stepObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="f781c-110">This command updates a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>
<span data-ttu-id="f781c-111">A etapa seria atualizada para as propriedades definidas no $stepObject.</span><span class="sxs-lookup"><span data-stu-id="f781c-111">The step would be updated to the properties set in the $stepObject.</span></span>

## <span data-ttu-id="f781c-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f781c-112">PARAMETERS</span></span>

### <span data-ttu-id="f781c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f781c-113">-DefaultProfile</span></span>
<span data-ttu-id="f781c-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f781c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f781c-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f781c-115">-InputObject</span></span>
<span data-ttu-id="f781c-116">O objeto de etapa.</span><span class="sxs-lookup"><span data-stu-id="f781c-116">The step object.</span></span>

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

### <span data-ttu-id="f781c-117">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="f781c-117">-Confirm</span></span>
<span data-ttu-id="f781c-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f781c-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f781c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f781c-119">-WhatIf</span></span>
<span data-ttu-id="f781c-120">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="f781c-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f781c-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f781c-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f781c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f781c-122">CommonParameters</span></span>
<span data-ttu-id="f781c-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f781c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f781c-124">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f781c-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f781c-125">Entradas</span><span class="sxs-lookup"><span data-stu-id="f781c-125">INPUTS</span></span>

### <span data-ttu-id="f781c-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span><span class="sxs-lookup"><span data-stu-id="f781c-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="f781c-127">Saídas</span><span class="sxs-lookup"><span data-stu-id="f781c-127">OUTPUTS</span></span>

### <span data-ttu-id="f781c-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span><span class="sxs-lookup"><span data-stu-id="f781c-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="f781c-129">Notas</span><span class="sxs-lookup"><span data-stu-id="f781c-129">NOTES</span></span>

## <span data-ttu-id="f781c-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f781c-130">RELATED LINKS</span></span>
