---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/get-azdeploymentmanagerrollout
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerRollout.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerRollout.md
ms.openlocfilehash: 53458d53dd6d8b3f698dc51fc6b1463c9a9134e8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887181"
---
# <span data-ttu-id="05d22-101">Get-AzDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="05d22-101">Get-AzDeploymentManagerRollout</span></span>

## <span data-ttu-id="05d22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05d22-102">SYNOPSIS</span></span>
<span data-ttu-id="05d22-103">Obtém a adoção.</span><span class="sxs-lookup"><span data-stu-id="05d22-103">Gets the rollout.</span></span>

## <span data-ttu-id="05d22-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="05d22-104">SYNTAX</span></span>

### <span data-ttu-id="05d22-105">Interativo (Padrão)</span><span class="sxs-lookup"><span data-stu-id="05d22-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerRollout [-ResourceGroupName] <String> [[-Name] <String>] [-RetryAttempt <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05d22-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="05d22-106">ResourceId</span></span>
```
Get-AzDeploymentManagerRollout [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="05d22-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="05d22-107">InputObject</span></span>
```
Get-AzDeploymentManagerRollout [-InputObject] <PSRollout> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="05d22-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="05d22-108">DESCRIPTION</span></span>
<span data-ttu-id="05d22-109">O cmdlet **Get-AzDeploymentManagerRollout** obtém uma adoção e retorna um objeto que representa essa rolagem com todas as informações detalhadas sobre o andamento da lançamento.</span><span class="sxs-lookup"><span data-stu-id="05d22-109">The **Get-AzDeploymentManagerRollout** cmdlet gets a rollout, and returns an object that represents that rollout with all the detailed information on the progress of the rollout.</span></span>
<span data-ttu-id="05d22-110">Especifique a distribuição pelo nome e o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="05d22-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="05d22-111">Como alternativa, você pode fornecer o objeto Rollout ou ResourceId.</span><span class="sxs-lookup"><span data-stu-id="05d22-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

<span data-ttu-id="05d22-112">O objeto de implantação retornado contém os serviços, unidades de serviço e etapas que foram implantadas e as que estão em andamento.</span><span class="sxs-lookup"><span data-stu-id="05d22-112">The returned rollout object contains the services, service units and steps that have been deployed and the ones in progress.</span></span> <span data-ttu-id="05d22-113">Aqueles que ainda não foram implantados não estão na resposta.</span><span class="sxs-lookup"><span data-stu-id="05d22-113">Those that are yet to be deployed are not in the response.</span></span>

## <span data-ttu-id="05d22-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="05d22-114">EXAMPLES</span></span>

### <span data-ttu-id="05d22-115">Exemplo 1 Obter a adoção</span><span class="sxs-lookup"><span data-stu-id="05d22-115">Example 1 Get the rollout</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="05d22-116">Este comando obtém um lançamento chamado ContosoRollout no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="05d22-116">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> 

### <span data-ttu-id="05d22-117">Exemplo 2 Obter e exibir os detalhes de lançamento</span><span class="sxs-lookup"><span data-stu-id="05d22-117">Example 2 Get and display the rollout details</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout -Verbose
```

<span data-ttu-id="05d22-118">Este comando obtém um lançamento chamado ContosoRollout no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="05d22-118">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span> <span data-ttu-id="05d22-119">A opção -Verbose exibe todos os detalhes de lançamento hierárquico; mostrando os Serviços, o ServiceUnits e as etapas em cada ServiceUnit e informações contextuais para cada etapa para uma exibição holística da rollout.</span><span class="sxs-lookup"><span data-stu-id="05d22-119">The -Verbose switch displays all the rollout details hierarchically; showing the Services, the ServiceUnits and the steps under each ServiceUnit and contextual information for each step for a holistic view of the rollout.</span></span>

### <span data-ttu-id="05d22-120">Exemplo 3: Obter uma distribuição usando o identificador de recurso</span><span class="sxs-lookup"><span data-stu-id="05d22-120">Example 3: Get a rollout using the resource identifier</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="05d22-121">Este comando obtém um lançamento chamado ContosoRollout no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="05d22-121">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="05d22-122">Exemplo 4: Obter uma adoção usando o objeto de lançamento.</span><span class="sxs-lookup"><span data-stu-id="05d22-122">Example 4: Get a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerRollout -InputObject $rolloutObject
```

<span data-ttu-id="05d22-123">Este comando obtém uma distribuição cujo nome e ResourceGroup corresponderem às propriedades Name e ResourceGroupName do $rolloutObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="05d22-123">This command gets a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="05d22-124">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="05d22-124">PARAMETERS</span></span>

### <span data-ttu-id="05d22-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05d22-125">-DefaultProfile</span></span>
<span data-ttu-id="05d22-126">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="05d22-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="05d22-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="05d22-127">-InputObject</span></span>
<span data-ttu-id="05d22-128">Objeto Rollout.</span><span class="sxs-lookup"><span data-stu-id="05d22-128">Rollout object.</span></span>

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

### <span data-ttu-id="05d22-129">-Name</span><span class="sxs-lookup"><span data-stu-id="05d22-129">-Name</span></span>
<span data-ttu-id="05d22-130">O nome da apostila.</span><span class="sxs-lookup"><span data-stu-id="05d22-130">The name of the rollout.</span></span>

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

### <span data-ttu-id="05d22-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05d22-131">-ResourceGroupName</span></span>
<span data-ttu-id="05d22-132">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="05d22-132">The resource group.</span></span>

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

### <span data-ttu-id="05d22-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="05d22-133">-ResourceId</span></span>
<span data-ttu-id="05d22-134">O identificador de recurso.</span><span class="sxs-lookup"><span data-stu-id="05d22-134">The resource identifier.</span></span>

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

### <span data-ttu-id="05d22-135">-RetryAttempt</span><span class="sxs-lookup"><span data-stu-id="05d22-135">-RetryAttempt</span></span>
<span data-ttu-id="05d22-136">A tentativa de nova tentativa de lançamento.</span><span class="sxs-lookup"><span data-stu-id="05d22-136">The retry attempt of the rollout.</span></span>

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

### <span data-ttu-id="05d22-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05d22-137">CommonParameters</span></span>
<span data-ttu-id="05d22-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05d22-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05d22-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="05d22-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05d22-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="05d22-140">INPUTS</span></span>

### <span data-ttu-id="05d22-141">System.String</span><span class="sxs-lookup"><span data-stu-id="05d22-141">System.String</span></span>

### <span data-ttu-id="05d22-142">System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="05d22-142">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="05d22-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span><span class="sxs-lookup"><span data-stu-id="05d22-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="05d22-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="05d22-144">OUTPUTS</span></span>

### <span data-ttu-id="05d22-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span><span class="sxs-lookup"><span data-stu-id="05d22-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="05d22-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="05d22-146">NOTES</span></span>

## <span data-ttu-id="05d22-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="05d22-147">RELATED LINKS</span></span>
