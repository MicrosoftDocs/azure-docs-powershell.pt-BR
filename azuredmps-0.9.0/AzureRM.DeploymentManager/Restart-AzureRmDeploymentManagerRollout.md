---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/restart-azurermdeploymentmanagerrollout
schema: 2.0.0
ms.openlocfilehash: ee1ef6e5b8bcee4af1d3aef67767269042c552df
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93426068"
---
# <span data-ttu-id="d23a5-101">Restart-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="d23a5-101">Restart-AzureRmDeploymentManagerRollout</span></span>

## <span data-ttu-id="d23a5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d23a5-102">SYNOPSIS</span></span>
<span data-ttu-id="d23a5-103">Reinicie uma distribuição com falha.</span><span class="sxs-lookup"><span data-stu-id="d23a5-103">Restart a failed rollout.</span></span>

## <span data-ttu-id="d23a5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d23a5-104">SYNTAX</span></span>

### <span data-ttu-id="d23a5-105">Interativo (padrão)</span><span class="sxs-lookup"><span data-stu-id="d23a5-105">Interactive (Default)</span></span>
```
Restart-AzureRmDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d23a5-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="d23a5-106">ResourceId</span></span>
```
Restart-AzureRmDeploymentManagerRollout [-ResourceId] <String> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d23a5-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="d23a5-107">InputObject</span></span>
```
Restart-AzureRmDeploymentManagerRollout [-Rollout] <PSRollout> [-SkipSucceeded]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d23a5-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d23a5-108">DESCRIPTION</span></span>
<span data-ttu-id="d23a5-109">O cmdlet **Restart-AzureRmDeploymentManagerRollout** reinicia uma distribuição com falha e retorna um objeto que representa essa distribuição com todas as informações detalhadas sobre o andamento da distribuição.</span><span class="sxs-lookup"><span data-stu-id="d23a5-109">The **Restart-AzureRmDeploymentManagerRollout** cmdlet restarts a failed rollout, and returns an object that represents that rollout with all the detailed information on the progress of the rollout.</span></span>
<span data-ttu-id="d23a5-110">Especifique a distribuição por nome e nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d23a5-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="d23a5-111">Como alternativa, você pode fornecer o objeto de distribuição ou a ResourceId.</span><span class="sxs-lookup"><span data-stu-id="d23a5-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>
<span data-ttu-id="d23a5-112">O parâmetro opcional SkipSucceeded permite que você ignore todas as etapas bem-sucedidas na execução anterior da distribuição.</span><span class="sxs-lookup"><span data-stu-id="d23a5-112">Optional parameter SkipSucceeded allows you to skip all the succeeded steps in the previous run of the rollout.</span></span>

## <span data-ttu-id="d23a5-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d23a5-113">EXAMPLES</span></span>

### <span data-ttu-id="d23a5-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d23a5-114">Example 1</span></span>
```powershell
PS C:\> Restart-AzureRmDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -SkipSucceeded
```

<span data-ttu-id="d23a5-115">Esse comando reinicia uma distribuição chamada ContosoRollout no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="d23a5-115">This command restarts a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> <span data-ttu-id="d23a5-116">O sinalizador SkipSucceeded indica que todas as etapas que já executaram com êxito devem ser ignoradas e a distribuição deve continuar a execução a partir de onde ela foi interrompida pela última vez.</span><span class="sxs-lookup"><span data-stu-id="d23a5-116">The SkipSucceeded flag indicates that all the steps that already ran successfully should be skipped and the rollout should continue execution from where it last failed.</span></span>

### <span data-ttu-id="d23a5-117">Exemplo 2: reiniciar uma distribuição usando o identificador de recursos</span><span class="sxs-lookup"><span data-stu-id="d23a5-117">Example 2: Restart a rollout using the resource identifier</span></span>
```powershell
PS C:\> Restart-AzureRmDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="d23a5-118">Esse comando reinicia uma distribuição chamada ContosoRollout no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="d23a5-118">This command restarts a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="d23a5-119">Exemplo 3: reiniciar uma distribuição usando o objeto de distribuição.</span><span class="sxs-lookup"><span data-stu-id="d23a5-119">Example 3: Restart a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerRollout -Rollout $rolloutObject
```

<span data-ttu-id="d23a5-120">Esse comando reinicia uma distribuição cujo nome e o nome da fonte de reinicialização correspondem às propriedades Name e ResourceGroupName do $rolloutObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="d23a5-120">This command restarts a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="d23a5-121">OS</span><span class="sxs-lookup"><span data-stu-id="d23a5-121">PARAMETERS</span></span>

### <span data-ttu-id="d23a5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d23a5-122">-DefaultProfile</span></span>
<span data-ttu-id="d23a5-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d23a5-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d23a5-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="d23a5-124">-Name</span></span>
<span data-ttu-id="d23a5-125">O nome da distribuição.</span><span class="sxs-lookup"><span data-stu-id="d23a5-125">The name of the rollout.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d23a5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d23a5-126">-ResourceGroupName</span></span>
<span data-ttu-id="d23a5-127">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d23a5-127">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d23a5-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d23a5-128">-ResourceId</span></span>
<span data-ttu-id="d23a5-129">O identificador do recurso.</span><span class="sxs-lookup"><span data-stu-id="d23a5-129">The resource identifier.</span></span>

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

### <span data-ttu-id="d23a5-130">-Distribuição</span><span class="sxs-lookup"><span data-stu-id="d23a5-130">-Rollout</span></span>
<span data-ttu-id="d23a5-131">O recurso a ser removido.</span><span class="sxs-lookup"><span data-stu-id="d23a5-131">The resource to be removed.</span></span>

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

### <span data-ttu-id="d23a5-132">-SkipSucceeded</span><span class="sxs-lookup"><span data-stu-id="d23a5-132">-SkipSucceeded</span></span>
<span data-ttu-id="d23a5-133">Ignorar etapas bem-sucedidas na execução anterior da distribuição.</span><span class="sxs-lookup"><span data-stu-id="d23a5-133">Skip steps that succeeded in the previous run of the rollout.</span></span>

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

### <span data-ttu-id="d23a5-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d23a5-134">-Confirm</span></span>
<span data-ttu-id="d23a5-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d23a5-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d23a5-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d23a5-136">-WhatIf</span></span>
<span data-ttu-id="d23a5-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d23a5-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d23a5-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d23a5-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d23a5-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d23a5-139">CommonParameters</span></span>
<span data-ttu-id="d23a5-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d23a5-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d23a5-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d23a5-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d23a5-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d23a5-142">INPUTS</span></span>

### <span data-ttu-id="d23a5-143">Microsoft. Azure. Commands. DeploymentManager. Models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="d23a5-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="d23a5-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d23a5-144">OUTPUTS</span></span>

### <span data-ttu-id="d23a5-145">Microsoft. Azure. Commands. DeploymentManager. Models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="d23a5-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="d23a5-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d23a5-146">NOTES</span></span>

## <span data-ttu-id="d23a5-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d23a5-147">RELATED LINKS</span></span>

[<span data-ttu-id="d23a5-148">Get-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="d23a5-148">Get-AzureRmDeploymentManagerRollout</span></span>](./Get-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="d23a5-149">Parar-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="d23a5-149">Stop-AzureRmDeploymentManagerRollout</span></span>](./Stop-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="d23a5-150">Remove-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="d23a5-150">Remove-AzureRmDeploymentManagerRollout</span></span>](./Remove-AzureRmDeploymentManagerRollout.md)