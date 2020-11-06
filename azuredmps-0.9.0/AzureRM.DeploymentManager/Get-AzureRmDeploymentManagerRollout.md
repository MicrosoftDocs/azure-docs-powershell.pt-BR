---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerrollout
schema: 2.0.0
ms.openlocfilehash: 21d0b4f7feec5b32ff732f880924becddd84db73
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425606"
---
# <span data-ttu-id="7fff3-101">Get-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="7fff3-101">Get-AzureRmDeploymentManagerRollout</span></span>

## <span data-ttu-id="7fff3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7fff3-102">SYNOPSIS</span></span>
<span data-ttu-id="7fff3-103">Obtém uma distribuição.</span><span class="sxs-lookup"><span data-stu-id="7fff3-103">Gets a rollout.</span></span>

## <span data-ttu-id="7fff3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7fff3-104">SYNTAX</span></span>

### <span data-ttu-id="7fff3-105">Interativo (padrão)</span><span class="sxs-lookup"><span data-stu-id="7fff3-105">Interactive (Default)</span></span>
```
Get-AzureRmDeploymentManagerRollout [-ResourceGroupName] <String> [-Name] <String> [[-RetryAttempt] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7fff3-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="7fff3-106">ResourceId</span></span>
```
Get-AzureRmDeploymentManagerRollout [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7fff3-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="7fff3-107">InputObject</span></span>
```
Get-AzureRmDeploymentManagerRollout [-Rollout] <PSRollout> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7fff3-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7fff3-108">DESCRIPTION</span></span>
<span data-ttu-id="7fff3-109">O cmdlet **Get-AzureRmDeploymentManagerRollout** Obtém uma distribuição e retorna um objeto que representa essa distribuição com todas as informações detalhadas sobre o andamento da distribuição.</span><span class="sxs-lookup"><span data-stu-id="7fff3-109">The **Get-AzureRmDeploymentManagerRollout** cmdlet gets a rollout, and returns an object that represents that rollout with all the detailed information on the progress of the rollout.</span></span>
<span data-ttu-id="7fff3-110">Especifique a distribuição por nome e nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7fff3-110">Specify the rollout by its name and resource group name.</span></span> <span data-ttu-id="7fff3-111">Como alternativa, você pode fornecer o objeto de distribuição ou a ResourceId.</span><span class="sxs-lookup"><span data-stu-id="7fff3-111">Alternately, you can provide the Rollout object or the ResourceId.</span></span>

## <span data-ttu-id="7fff3-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7fff3-112">EXAMPLES</span></span>

### <span data-ttu-id="7fff3-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7fff3-113">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerRollout -ResourceGroupName ContosoResourceGroup -Name ContosoRollout
```

<span data-ttu-id="7fff3-114">Esse comando obtém uma distribuição chamada ContosoRollout no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="7fff3-114">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="7fff3-115">Exemplo 2: obter uma distribuição usando o identificador de recursos</span><span class="sxs-lookup"><span data-stu-id="7fff3-115">Example 2: Get a rollout using the resource identifier</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerRollout -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/rollouts/ContosoRollout"
```

<span data-ttu-id="7fff3-116">Esse comando obtém uma distribuição chamada ContosoRollout no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="7fff3-116">This command gets a rollout named ContosoRollout in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="7fff3-117">Exemplo 3: obter uma distribuição usando o objeto de distribuição.</span><span class="sxs-lookup"><span data-stu-id="7fff3-117">Example 3: Get a rollout using the rollout object.</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerRollout -Rollout $rolloutObject
```

<span data-ttu-id="7fff3-118">Esse comando obtém uma distribuição cujo nome e o meu nome do contato correspondem às propriedades Name e ResourceGroupName do $rolloutObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="7fff3-118">This command gets a rollout whose name and ResourceGroup match the Name and ResourceGroupName properties of the $rolloutObject, respectively.</span></span>

## <span data-ttu-id="7fff3-119">OS</span><span class="sxs-lookup"><span data-stu-id="7fff3-119">PARAMETERS</span></span>

### <span data-ttu-id="7fff3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fff3-120">-DefaultProfile</span></span>
<span data-ttu-id="7fff3-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7fff3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7fff3-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="7fff3-122">-Name</span></span>
<span data-ttu-id="7fff3-123">O nome da distribuição.</span><span class="sxs-lookup"><span data-stu-id="7fff3-123">The name of the rollout.</span></span>

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

### <span data-ttu-id="7fff3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fff3-124">-ResourceGroupName</span></span>
<span data-ttu-id="7fff3-125">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="7fff3-125">The resource group.</span></span>

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

### <span data-ttu-id="7fff3-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7fff3-126">-ResourceId</span></span>
<span data-ttu-id="7fff3-127">O identificador do recurso.</span><span class="sxs-lookup"><span data-stu-id="7fff3-127">The resource identifier.</span></span>

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

### <span data-ttu-id="7fff3-128">-RetryAttempt</span><span class="sxs-lookup"><span data-stu-id="7fff3-128">-RetryAttempt</span></span>
<span data-ttu-id="7fff3-129">A tentativa de nova tentativa da distribuição.</span><span class="sxs-lookup"><span data-stu-id="7fff3-129">The retry attempt of the rollout.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: Interactive
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fff3-130">-Distribuição</span><span class="sxs-lookup"><span data-stu-id="7fff3-130">-Rollout</span></span>
<span data-ttu-id="7fff3-131">Objeto de distribuição.</span><span class="sxs-lookup"><span data-stu-id="7fff3-131">Rollout object.</span></span>

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

### <span data-ttu-id="7fff3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fff3-132">CommonParameters</span></span>
<span data-ttu-id="7fff3-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fff3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fff3-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fff3-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fff3-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7fff3-135">INPUTS</span></span>

### <span data-ttu-id="7fff3-136">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="7fff3-136">None</span></span>

## <span data-ttu-id="7fff3-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7fff3-137">OUTPUTS</span></span>

### <span data-ttu-id="7fff3-138">Microsoft. Azure. Commands. DeploymentManager. Models. PSRollout</span><span class="sxs-lookup"><span data-stu-id="7fff3-138">Microsoft.Azure.Commands.DeploymentManager.Models.PSRollout</span></span>

## <span data-ttu-id="7fff3-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7fff3-139">NOTES</span></span>

## <span data-ttu-id="7fff3-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7fff3-140">RELATED LINKS</span></span>

[<span data-ttu-id="7fff3-141">Parar-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="7fff3-141">Stop-AzureRmDeploymentManagerRollout</span></span>](./Stop-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="7fff3-142">Restart-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="7fff3-142">Restart-AzureRmDeploymentManagerRollout</span></span>](./Restart-AzureRmDeploymentManagerRollout.md)

[<span data-ttu-id="7fff3-143">Remove-AzureRmDeploymentManagerRollout</span><span class="sxs-lookup"><span data-stu-id="7fff3-143">Remove-AzureRmDeploymentManagerRollout</span></span>](./Remove-AzureRmDeploymentManagerRollout.md)