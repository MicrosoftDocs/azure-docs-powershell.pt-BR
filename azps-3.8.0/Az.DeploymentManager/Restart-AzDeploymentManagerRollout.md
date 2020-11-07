---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/restart-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Restart-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Restart-AzDeploymentManagerRollout.md
ms.openlocfilehash: ba7b62d42764f5098868e6a15eb073cb6b898e82
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944376"
---
# <span data-ttu-id="ddbcb-101">Restart-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="ddbcb-101">Restart-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="ddbcb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ddbcb-102">SYNOPSIS</span></span>
<span data-ttu-id="ddbcb-103">Reinicia uma distribuição com falha.</span><span class="sxs-lookup"><span data-stu-id="ddbcb-103">Restarts a failed rollout.</span></span>

## <span data-ttu-id="ddbcb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ddbcb-104">SYNTAX</span></span>

### <span data-ttu-id="ddbcb-105">Interativo (padrão)</span><span class="sxs-lookup"><span data-stu-id="ddbcb-105">Interactive (Default)</span></span>
```
Restart-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddbcb-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="ddbcb-106">ResourceId</span></span>
```
Restart-AzDeploymentManagerRollout [-ResourceId] <String> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddbcb-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="ddbcb-107">InputObject</span></span>
```
Restart-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ddbcb-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ddbcb-108">DESCRIPTION</span></span>
<span data-ttu-id="ddbcb-109">O cmdlet **Restart-AzDeploymentManagerRollout** reinicia uma distribuição com falha e retorna um objeto que representa essa distribuição com todas as informações detalhadas sobre o andamento da distribuição.</span><span class="sxs-lookup"><span data-stu-id="ddbcb-109">The **Restart-AzDeploymentManagerRollout** cmdlet restarts a failed rollout, and returns an object that represents that rollout with all the detailed information on the progress of the rollout.</span></span>
<span data-ttu-id="ddbcb-110">Especifique a distribuição por nome e nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ddbcb-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="ddbcb-111">Como alternativa, você pode fornecer o objeto de distribuição ou a ResourceId.</span><span class="sxs-lookup"><span data-stu-id="ddbcb-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>
<span data-ttu-id="ddbcb-112">O parâmetro opcional SkipSucceeded permite que você ignore todas as etapas bem-sucedidas na execução anterior da distribuição.</span><span class="sxs-lookup"><span data-stu-id="ddbcb-112">Optional parameter SkipSucceeded allows you to skip all the succeeded steps in the previous run of the rollout.</span></span>

## <span data-ttu-id="ddbcb-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ddbcb-113">EXAMPLES</span></span>

### <span data-ttu-id="ddbcb-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ddbcb-114">Example 1</span></span>
```powershell
PS C:\> Restart-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -SkipSucceeded
```

<span data-ttu-id="ddbcb-115">Esse comando reinicia uma distribuição chamada ContosoRollout no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ddbcb-115">This command restarts a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> <span data-ttu-id="ddbcb-116">O sinalizador SkipSucceeded indica que todas as etapas que já executaram com êxito devem ser ignoradas e a distribuição deve continuar a execução a partir de onde ela foi interrompida pela última vez.</span><span class="sxs-lookup"><span data-stu-id="ddbcb-116">The SkipSucceeded flag indicates that all the steps that already ran successfully should be skipped and the rollout should continue execution from where it last failed.</span></span>

### <span data-ttu-id="ddbcb-117">Exemplo 2: reiniciar uma distribuição usando o identificador de recursos</span><span class="sxs-lookup"><span data-stu-id="ddbcb-117">Example 2: Restart a rollout using the resource identifier</span></span>
```powershell
PS C:\> Restart-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="ddbcb-118">Esse comando reinicia uma distribuição chamada ContosoRollout no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="ddbcb-118">This command restarts a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="ddbcb-119">Exemplo 3: reiniciar uma distribuição usando o objeto de distribuição.</span><span class="sxs-lookup"><span data-stu-id="ddbcb-119">Example 3: Restart a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="ddbcb-120">Esse comando reinicia uma distribuição cujo nome e o nome da fonte de reinicialização correspondem às propriedades Name e ResourceGroupName do $rolloutObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="ddbcb-120">This command restarts a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="ddbcb-121">OS</span><span class="sxs-lookup"><span data-stu-id="ddbcb-121">PARAMETERS</span></span>

### <span data-ttu-id="ddbcb-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddbcb-122">-DefaultProfile</span></span>
<span data-ttu-id="ddbcb-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ddbcb-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ddbcb-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ddbcb-124">-InputObject</span></span>
<span data-ttu-id="ddbcb-125">O recurso a ser removido.</span><span class="sxs-lookup"><span data-stu-id="ddbcb-125">The resource to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ddbcb-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="ddbcb-126">-Name</span></span>
<span data-ttu-id="ddbcb-127">O nome da distribuição.</span><span class="sxs-lookup"><span data-stu-id="ddbcb-127">The name of the rollout.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddbcb-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddbcb-128">-ResourceGroupName</span></span>
<span data-ttu-id="ddbcb-129">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ddbcb-129">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ddbcb-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ddbcb-130">-ResourceId</span></span>
<span data-ttu-id="ddbcb-131">O identificador do recurso.</span><span class="sxs-lookup"><span data-stu-id="ddbcb-131">The resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddbcb-132">-SkipSucceeded</span><span class="sxs-lookup"><span data-stu-id="ddbcb-132">-SkipSucceeded</span></span>
<span data-ttu-id="ddbcb-133">Ignorar etapas bem-sucedidas na execução anterior da distribuição.</span><span class="sxs-lookup"><span data-stu-id="ddbcb-133">Skip steps that succeeded in the previous run of the rollout.</span></span>

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

### <span data-ttu-id="ddbcb-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ddbcb-134">-Confirm</span></span>
<span data-ttu-id="ddbcb-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ddbcb-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddbcb-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddbcb-136">-WhatIf</span></span>
<span data-ttu-id="ddbcb-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ddbcb-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddbcb-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ddbcb-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddbcb-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddbcb-139">CommonParameters</span></span>
<span data-ttu-id="ddbcb-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddbcb-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddbcb-141">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ddbcb-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddbcb-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ddbcb-142">INPUTS</span></span>

### <span data-ttu-id="ddbcb-143">System. String</span><span class="sxs-lookup"><span data-stu-id="ddbcb-143">System.String</span></span>

### <span data-ttu-id="ddbcb-144">Microsoft. Azure. Commands. DeploymentManager. Models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="ddbcb-144">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="ddbcb-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ddbcb-145">OUTPUTS</span></span>

### <span data-ttu-id="ddbcb-146">Microsoft. Azure. Commands. DeploymentManager. Models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="ddbcb-146">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="ddbcb-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ddbcb-147">NOTES</span></span>

## <span data-ttu-id="ddbcb-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ddbcb-148">RELATED LINKS</span></span>
