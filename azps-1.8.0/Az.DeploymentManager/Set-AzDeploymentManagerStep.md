---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerStep.md
ms.openlocfilehash: 15944b324cc2b33d3186d7c84da16c72351dcc99
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600967"
---
# <span data-ttu-id="116f0-101">Set-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="116f0-101">Set-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="116f0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="116f0-102">SYNOPSIS</span></span>
<span data-ttu-id="116f0-103">Atualiza a etapa.</span><span class="sxs-lookup"><span data-stu-id="116f0-103">Updates the step.</span></span>

## <span data-ttu-id="116f0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="116f0-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerStep [-InputObject] <PSStepResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="116f0-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="116f0-105">DESCRIPTION</span></span>
<span data-ttu-id="116f0-106">O cmdlet **set-AzDeploymentManagerStep** atualiza uma etapa com o objeto Step especificado.</span><span class="sxs-lookup"><span data-stu-id="116f0-106">The **Set-AzDeploymentManagerStep** cmdlet updates a step with the specified step object.</span></span>
<span data-ttu-id="116f0-107">O cmdlet retorna o objeto Step atualizado.</span><span class="sxs-lookup"><span data-stu-id="116f0-107">The cmdlet returns the updated step object.</span></span>

## <span data-ttu-id="116f0-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="116f0-108">EXAMPLES</span></span>

### <span data-ttu-id="116f0-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="116f0-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerStep -InputObject $stepObject
```

<span data-ttu-id="116f0-110">Esse comando atualiza uma etapa cujo nome e o meu nome do elemento de Resource correspondem às propriedades Name e ResourceGroupName do $stepObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="116f0-110">This command updates a step whose name and ResourceGroup match the Name and ResourceGroupName properties of the $stepObject, respectively.</span></span>
<span data-ttu-id="116f0-111">A etapa seria atualizada para as propriedades definidas no $stepObject.</span><span class="sxs-lookup"><span data-stu-id="116f0-111">The step would be updated to the properties set in the $stepObject.</span></span>

## <span data-ttu-id="116f0-112">OS</span><span class="sxs-lookup"><span data-stu-id="116f0-112">PARAMETERS</span></span>

### <span data-ttu-id="116f0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="116f0-113">-DefaultProfile</span></span>
<span data-ttu-id="116f0-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="116f0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="116f0-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="116f0-115">-InputObject</span></span>
<span data-ttu-id="116f0-116">O objeto Step.</span><span class="sxs-lookup"><span data-stu-id="116f0-116">The step object.</span></span>

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

### <span data-ttu-id="116f0-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="116f0-117">-Confirm</span></span>
<span data-ttu-id="116f0-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="116f0-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="116f0-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="116f0-119">-WhatIf</span></span>
<span data-ttu-id="116f0-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="116f0-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="116f0-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="116f0-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="116f0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="116f0-122">CommonParameters</span></span>
<span data-ttu-id="116f0-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="116f0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="116f0-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="116f0-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="116f0-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="116f0-125">INPUTS</span></span>

### <span data-ttu-id="116f0-126">Microsoft. Azure. Commands. DeploymentManager. Models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="116f0-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="116f0-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="116f0-127">OUTPUTS</span></span>

### <span data-ttu-id="116f0-128">Microsoft. Azure. Commands. DeploymentManager. Models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="116f0-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="116f0-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="116f0-129">NOTES</span></span>

## <span data-ttu-id="116f0-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="116f0-130">RELATED LINKS</span></span>
