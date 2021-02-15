---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerRollout.md
ms.openlocfilehash: c01c41ff476ee4e6b8a6291f5ebcfbf4c176b775
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116221"
---
# <span data-ttu-id="57870-101">Get-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="57870-101">Get-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="57870-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="57870-102">SYNOPSIS</span></span>
<span data-ttu-id="57870-103">Obtém a adoção.</span><span class="sxs-lookup"><span data-stu-id="57870-103">Gets the rollout.</span></span>

## <span data-ttu-id="57870-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="57870-104">SYNTAX</span></span>

### <span data-ttu-id="57870-105">Interativo (Padrão)</span><span class="sxs-lookup"><span data-stu-id="57870-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerRollout [-ResourceGroupName] <String> [[-Name] <String>] [-RetryAttempt <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57870-106">Resourceid</span><span class="sxs-lookup"><span data-stu-id="57870-106">ResourceId</span></span>
```
Get-AzDeploymentManagerRollout [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="57870-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="57870-107">InputObject</span></span>
```
Get-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="57870-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="57870-108">DESCRIPTION</span></span>
<span data-ttu-id="57870-109">O cmdlet **Get-AzDeploymentManagerRollout** obtém uma aprovação e retorna um objeto que representa essa adoção com todas as informações detalhadas sobre o andamento da apostila.</span><span class="sxs-lookup"><span data-stu-id="57870-109">The **Get-AzDeploymentManagerRollout** cmdlet gets a rollout, and returns an object that represents that rollout with all the detailed information on the progress of the rollout.</span></span>
<span data-ttu-id="57870-110">Especifique a distribuição pelo nome e nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="57870-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="57870-111">Como alternativa, você pode fornecer o objeto Distribuição ou o ResourceId.</span><span class="sxs-lookup"><span data-stu-id="57870-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

<span data-ttu-id="57870-112">O objeto de implantação retornado contém os serviços, as unidades de serviço e as etapas que foram implantadas e as em andamento.</span><span class="sxs-lookup"><span data-stu-id="57870-112">The returned rollout object contains the services, service units and steps that have been deployed and the ones in progress.</span></span> <span data-ttu-id="57870-113">Aqueles que ainda não devem ser implantados não estão na resposta.</span><span class="sxs-lookup"><span data-stu-id="57870-113">Those that are yet to be deployed are not in the response.</span></span>

## <span data-ttu-id="57870-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="57870-114">EXAMPLES</span></span>

### <span data-ttu-id="57870-115">Exemplo 1 Obter a adoção</span><span class="sxs-lookup"><span data-stu-id="57870-115">Example 1 Get the rollout</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="57870-116">Esse comando obtém uma adoção chamada ContosoRollout no Grupo ContosoResource.</span><span class="sxs-lookup"><span data-stu-id="57870-116">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> 

### <span data-ttu-id="57870-117">Exemplo 2 Obter e exibir os detalhes da adoção</span><span class="sxs-lookup"><span data-stu-id="57870-117">Example 2 Get and display the rollout details</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -Verbose
```

<span data-ttu-id="57870-118">Esse comando obtém uma adoção chamada ContosoRollout no Grupo ContosoResource.</span><span class="sxs-lookup"><span data-stu-id="57870-118">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> <span data-ttu-id="57870-119">A opção -Detalhado exibe todos os detalhes da adoção hierárquica; mostrando os Serviços, as ServiceUnits e as etapas em cada ServiceUnit e informações contextuais para cada etapa para uma exibição holística da adoção.</span><span class="sxs-lookup"><span data-stu-id="57870-119">The -Verbose switch displays all the rollout details hierarchically; showing the Services, the ServiceUnits and the steps under each ServiceUnit and contextual information for each step for a holistic view of the rollout.</span></span>

### <span data-ttu-id="57870-120">Exemplo 3: Obter uma distribuição usando o identificador de recurso</span><span class="sxs-lookup"><span data-stu-id="57870-120">Example 3: Get a rollout using the resource identifier</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="57870-121">Esse comando obtém uma adoção chamada ContosoRollout no Grupo ContosoResource.</span><span class="sxs-lookup"><span data-stu-id="57870-121">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="57870-122">Exemplo 4: Obter uma adoção usando o objeto de adoção.</span><span class="sxs-lookup"><span data-stu-id="57870-122">Example 4: Get a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="57870-123">Esse comando obtém uma distribuição cujo nome e Grupo de Recursos corresponderem às propriedades Nome e NomeDoGrupo de Recursos da $rolloutObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="57870-123">This command gets a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="57870-124">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="57870-124">PARAMETERS</span></span>

### <span data-ttu-id="57870-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57870-125">-DefaultProfile</span></span>
<span data-ttu-id="57870-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="57870-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57870-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="57870-127">-InputObject</span></span>
<span data-ttu-id="57870-128">Objeto de adoção.</span><span class="sxs-lookup"><span data-stu-id="57870-128">Rollout object.</span></span>

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

### <span data-ttu-id="57870-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="57870-129">-Name</span></span>
<span data-ttu-id="57870-130">O nome da apostila.</span><span class="sxs-lookup"><span data-stu-id="57870-130">The name of the rollout.</span></span>

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

### <span data-ttu-id="57870-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57870-131">-ResourceGroupName</span></span>
<span data-ttu-id="57870-132">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="57870-132">The resource group.</span></span>

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

### <span data-ttu-id="57870-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="57870-133">-ResourceId</span></span>
<span data-ttu-id="57870-134">O identificador de recurso.</span><span class="sxs-lookup"><span data-stu-id="57870-134">The resource identifier.</span></span>

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

### <span data-ttu-id="57870-135">-RetryAttempt</span><span class="sxs-lookup"><span data-stu-id="57870-135">-RetryAttempt</span></span>
<span data-ttu-id="57870-136">A tentativa de repetir a adoção.</span><span class="sxs-lookup"><span data-stu-id="57870-136">The retry attempt of the rollout.</span></span>

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

### <span data-ttu-id="57870-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57870-137">CommonParameters</span></span>
<span data-ttu-id="57870-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57870-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57870-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="57870-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57870-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="57870-140">INPUTS</span></span>

### <span data-ttu-id="57870-141">System.String</span><span class="sxs-lookup"><span data-stu-id="57870-141">System.String</span></span>

### <span data-ttu-id="57870-142">System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="57870-142">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="57870-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span><span class="sxs-lookup"><span data-stu-id="57870-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="57870-144">Saídas</span><span class="sxs-lookup"><span data-stu-id="57870-144">OUTPUTS</span></span>

### <span data-ttu-id="57870-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span><span class="sxs-lookup"><span data-stu-id="57870-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="57870-146">Notas</span><span class="sxs-lookup"><span data-stu-id="57870-146">NOTES</span></span>

## <span data-ttu-id="57870-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="57870-147">RELATED LINKS</span></span>
