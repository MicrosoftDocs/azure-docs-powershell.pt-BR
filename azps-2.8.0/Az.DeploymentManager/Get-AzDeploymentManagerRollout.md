---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerRollout.md
ms.openlocfilehash: fbcb93ec75dc0e136c1c18743a8686f7642ef02f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596670"
---
# <span data-ttu-id="d81a8-101">Get-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="d81a8-101">Get-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="d81a8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d81a8-102">SYNOPSIS</span></span>
<span data-ttu-id="d81a8-103">Obtém a distribuição.</span><span class="sxs-lookup"><span data-stu-id="d81a8-103">Gets the rollout.</span></span>

## <span data-ttu-id="d81a8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d81a8-104">SYNTAX</span></span>

### <span data-ttu-id="d81a8-105">Interativo (padrão)</span><span class="sxs-lookup"><span data-stu-id="d81a8-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [-RetryAttempt <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d81a8-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="d81a8-106">ResourceId</span></span>
```
Get-AzDeploymentManagerRollout [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d81a8-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="d81a8-107">InputObject</span></span>
```
Get-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d81a8-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d81a8-108">DESCRIPTION</span></span>
<span data-ttu-id="d81a8-109">O cmdlet **Get-AzDeploymentManagerRollout** Obtém uma distribuição e retorna um objeto que representa essa distribuição com todas as informações detalhadas sobre o andamento da distribuição.</span><span class="sxs-lookup"><span data-stu-id="d81a8-109">The **Get-AzDeploymentManagerRollout** cmdlet gets a rollout, and returns an object that represents that rollout with all the detailed information on the progress of the rollout.</span></span>
<span data-ttu-id="d81a8-110">Especifique a distribuição por nome e nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d81a8-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="d81a8-111">Como alternativa, você pode fornecer o objeto de distribuição ou a ResourceId.</span><span class="sxs-lookup"><span data-stu-id="d81a8-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

<span data-ttu-id="d81a8-112">O objeto de distribuição retornado contém os serviços, as unidades de serviço e as etapas que foram implantadas e as em andamento.</span><span class="sxs-lookup"><span data-stu-id="d81a8-112">The returned rollout object contains the services, service units and steps that have been deployed and the ones in progress.</span></span> <span data-ttu-id="d81a8-113">Os que ainda não estão sendo implantados não estão na resposta.</span><span class="sxs-lookup"><span data-stu-id="d81a8-113">Those that are yet to be deployed are not in the response.</span></span>

## <span data-ttu-id="d81a8-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d81a8-114">EXAMPLES</span></span>

### <span data-ttu-id="d81a8-115">Exemplo 1 obter a distribuição</span><span class="sxs-lookup"><span data-stu-id="d81a8-115">Example 1 Get the rollout</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="d81a8-116">Esse comando obtém uma distribuição chamada ContosoRollout no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="d81a8-116">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> 

### <span data-ttu-id="d81a8-117">Exemplo 2 obter e exibir os detalhes da distribuição</span><span class="sxs-lookup"><span data-stu-id="d81a8-117">Example 2 Get and display the rollout details</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -Verbose
```

<span data-ttu-id="d81a8-118">Esse comando obtém uma distribuição chamada ContosoRollout no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="d81a8-118">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> <span data-ttu-id="d81a8-119">A opção – Verbose exibe todos os detalhes da distribuição hierarquicamente; Mostrar os serviços, as unidades de serviço e as etapas em cada unidade de serviço e informações contextuais de cada etapa para uma exibição holística da distribuição.</span><span class="sxs-lookup"><span data-stu-id="d81a8-119">The -Verbose switch displays all the rollout details hierarchically; showing the Services, the ServiceUnits and the steps under each ServiceUnit and contextual information for each step for a holistic view of the rollout.</span></span>

### <span data-ttu-id="d81a8-120">Exemplo 3: obter uma distribuição usando o identificador de recursos</span><span class="sxs-lookup"><span data-stu-id="d81a8-120">Example 3: Get a rollout using the resource identifier</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="d81a8-121">Esse comando obtém uma distribuição chamada ContosoRollout no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="d81a8-121">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="d81a8-122">Exemplo 4: obter uma distribuição usando o objeto de distribuição.</span><span class="sxs-lookup"><span data-stu-id="d81a8-122">Example 4: Get a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="d81a8-123">Esse comando obtém uma distribuição cujo nome e o meu nome do contato correspondem às propriedades Name e ResourceGroupName do $rolloutObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="d81a8-123">This command gets a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="d81a8-124">OS</span><span class="sxs-lookup"><span data-stu-id="d81a8-124">PARAMETERS</span></span>

### <span data-ttu-id="d81a8-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d81a8-125">-DefaultProfile</span></span>
<span data-ttu-id="d81a8-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d81a8-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d81a8-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d81a8-127">-InputObject</span></span>
<span data-ttu-id="d81a8-128">Objeto de distribuição.</span><span class="sxs-lookup"><span data-stu-id="d81a8-128">Rollout object.</span></span>

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

### <span data-ttu-id="d81a8-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="d81a8-129">-Name</span></span>
<span data-ttu-id="d81a8-130">O nome da distribuição.</span><span class="sxs-lookup"><span data-stu-id="d81a8-130">The name of the rollout.</span></span>

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

### <span data-ttu-id="d81a8-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d81a8-131">-ResourceGroupName</span></span>
<span data-ttu-id="d81a8-132">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="d81a8-132">The resource group.</span></span>

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

### <span data-ttu-id="d81a8-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d81a8-133">-ResourceId</span></span>
<span data-ttu-id="d81a8-134">O identificador do recurso.</span><span class="sxs-lookup"><span data-stu-id="d81a8-134">The resource identifier.</span></span>

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

### <span data-ttu-id="d81a8-135">-RetryAttempt</span><span class="sxs-lookup"><span data-stu-id="d81a8-135">-RetryAttempt</span></span>
<span data-ttu-id="d81a8-136">A tentativa de nova tentativa da distribuição.</span><span class="sxs-lookup"><span data-stu-id="d81a8-136">The retry attempt of the rollout.</span></span>

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

### <span data-ttu-id="d81a8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d81a8-137">CommonParameters</span></span>
<span data-ttu-id="d81a8-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d81a8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d81a8-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d81a8-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d81a8-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d81a8-140">INPUTS</span></span>

### <span data-ttu-id="d81a8-141">System. String</span><span class="sxs-lookup"><span data-stu-id="d81a8-141">System.String</span></span>

### <span data-ttu-id="d81a8-142">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="d81a8-142">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="d81a8-143">Microsoft. Azure. Commands. DeploymentManager. Models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="d81a8-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="d81a8-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d81a8-144">OUTPUTS</span></span>

### <span data-ttu-id="d81a8-145">Microsoft. Azure. Commands. DeploymentManager. Models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="d81a8-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="d81a8-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d81a8-146">NOTES</span></span>

## <span data-ttu-id="d81a8-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d81a8-147">RELATED LINKS</span></span>
