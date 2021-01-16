---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerRollout.md
ms.openlocfilehash: c01c41ff476ee4e6b8a6291f5ebcfbf4c176b775
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98256879"
---
# <span data-ttu-id="64ae5-101">Get-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="64ae5-101">Get-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="64ae5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="64ae5-102">SYNOPSIS</span></span>
<span data-ttu-id="64ae5-103">Obtém a distribuição.</span><span class="sxs-lookup"><span data-stu-id="64ae5-103">Gets the rollout.</span></span>

## <span data-ttu-id="64ae5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="64ae5-104">SYNTAX</span></span>

### <span data-ttu-id="64ae5-105">Interativo (padrão)</span><span class="sxs-lookup"><span data-stu-id="64ae5-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerRollout [-ResourceGroupName] <String> [[-Name] <String>] [-RetryAttempt <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64ae5-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="64ae5-106">ResourceId</span></span>
```
Get-AzDeploymentManagerRollout [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="64ae5-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="64ae5-107">InputObject</span></span>
```
Get-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="64ae5-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="64ae5-108">DESCRIPTION</span></span>
<span data-ttu-id="64ae5-109">O cmdlet **Get-AzDeploymentManagerRollout** Obtém uma distribuição e retorna um objeto que representa essa distribuição com todas as informações detalhadas sobre o andamento da distribuição.</span><span class="sxs-lookup"><span data-stu-id="64ae5-109">The **Get-AzDeploymentManagerRollout** cmdlet gets a rollout, and returns an object that represents that rollout with all the detailed information on the progress of the rollout.</span></span>
<span data-ttu-id="64ae5-110">Especifique a distribuição por nome e nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="64ae5-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="64ae5-111">Como alternativa, você pode fornecer o objeto de distribuição ou a ResourceId.</span><span class="sxs-lookup"><span data-stu-id="64ae5-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

<span data-ttu-id="64ae5-112">O objeto de distribuição retornado contém os serviços, as unidades de serviço e as etapas que foram implantadas e as em andamento.</span><span class="sxs-lookup"><span data-stu-id="64ae5-112">The returned rollout object contains the services, service units and steps that have been deployed and the ones in progress.</span></span> <span data-ttu-id="64ae5-113">Os que ainda não estão sendo implantados não estão na resposta.</span><span class="sxs-lookup"><span data-stu-id="64ae5-113">Those that are yet to be deployed are not in the response.</span></span>

## <span data-ttu-id="64ae5-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="64ae5-114">EXAMPLES</span></span>

### <span data-ttu-id="64ae5-115">Exemplo 1 obter a distribuição</span><span class="sxs-lookup"><span data-stu-id="64ae5-115">Example 1 Get the rollout</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="64ae5-116">Esse comando obtém uma distribuição chamada ContosoRollout no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="64ae5-116">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> 

### <span data-ttu-id="64ae5-117">Exemplo 2 obter e exibir os detalhes da distribuição</span><span class="sxs-lookup"><span data-stu-id="64ae5-117">Example 2 Get and display the rollout details</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -Verbose
```

<span data-ttu-id="64ae5-118">Esse comando obtém uma distribuição chamada ContosoRollout no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="64ae5-118">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> <span data-ttu-id="64ae5-119">A opção – Verbose exibe todos os detalhes da distribuição hierarquicamente; Mostrar os serviços, as unidades de serviço e as etapas em cada unidade de serviço e informações contextuais de cada etapa para uma exibição holística da distribuição.</span><span class="sxs-lookup"><span data-stu-id="64ae5-119">The -Verbose switch displays all the rollout details hierarchically; showing the Services, the ServiceUnits and the steps under each ServiceUnit and contextual information for each step for a holistic view of the rollout.</span></span>

### <span data-ttu-id="64ae5-120">Exemplo 3: obter uma distribuição usando o identificador de recursos</span><span class="sxs-lookup"><span data-stu-id="64ae5-120">Example 3: Get a rollout using the resource identifier</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="64ae5-121">Esse comando obtém uma distribuição chamada ContosoRollout no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="64ae5-121">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="64ae5-122">Exemplo 4: obter uma distribuição usando o objeto de distribuição.</span><span class="sxs-lookup"><span data-stu-id="64ae5-122">Example 4: Get a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="64ae5-123">Esse comando obtém uma distribuição cujo nome e o meu nome do contato correspondem às propriedades Name e ResourceGroupName do $rolloutObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="64ae5-123">This command gets a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="64ae5-124">OS</span><span class="sxs-lookup"><span data-stu-id="64ae5-124">PARAMETERS</span></span>

### <span data-ttu-id="64ae5-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64ae5-125">-DefaultProfile</span></span>
<span data-ttu-id="64ae5-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="64ae5-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64ae5-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="64ae5-127">-InputObject</span></span>
<span data-ttu-id="64ae5-128">Objeto de distribuição.</span><span class="sxs-lookup"><span data-stu-id="64ae5-128">Rollout object.</span></span>

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

### <span data-ttu-id="64ae5-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="64ae5-129">-Name</span></span>
<span data-ttu-id="64ae5-130">O nome da distribuição.</span><span class="sxs-lookup"><span data-stu-id="64ae5-130">The name of the rollout.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64ae5-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64ae5-131">-ResourceGroupName</span></span>
<span data-ttu-id="64ae5-132">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="64ae5-132">The resource group.</span></span>

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

### <span data-ttu-id="64ae5-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="64ae5-133">-ResourceId</span></span>
<span data-ttu-id="64ae5-134">O identificador do recurso.</span><span class="sxs-lookup"><span data-stu-id="64ae5-134">The resource identifier.</span></span>

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

### <span data-ttu-id="64ae5-135">-RetryAttempt</span><span class="sxs-lookup"><span data-stu-id="64ae5-135">-RetryAttempt</span></span>
<span data-ttu-id="64ae5-136">A tentativa de nova tentativa da distribuição.</span><span class="sxs-lookup"><span data-stu-id="64ae5-136">The retry attempt of the rollout.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Interactive
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64ae5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64ae5-137">CommonParameters</span></span>
<span data-ttu-id="64ae5-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64ae5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64ae5-139">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="64ae5-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64ae5-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="64ae5-140">INPUTS</span></span>

### <span data-ttu-id="64ae5-141">System. String</span><span class="sxs-lookup"><span data-stu-id="64ae5-141">System.String</span></span>

### <span data-ttu-id="64ae5-142">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="64ae5-142">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="64ae5-143">Microsoft. Azure. Commands. DeploymentManager. Models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="64ae5-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="64ae5-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="64ae5-144">OUTPUTS</span></span>

### <span data-ttu-id="64ae5-145">Microsoft. Azure. Commands. DeploymentManager. Models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="64ae5-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="64ae5-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="64ae5-146">NOTES</span></span>

## <span data-ttu-id="64ae5-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="64ae5-147">RELATED LINKS</span></span>
