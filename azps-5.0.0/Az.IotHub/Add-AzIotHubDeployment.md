---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeployment.md
ms.openlocfilehash: 375e225d4c09368fac82db240988132952a0ada7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94117790"
---
# <span data-ttu-id="c6e47-101">Add-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="c6e47-101">Add-AzIotHubDeployment</span></span>

## <span data-ttu-id="c6e47-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c6e47-102">SYNOPSIS</span></span>
<span data-ttu-id="c6e47-103">Adicionar uma implantação de borda IoT a um hub IoT de destino.</span><span class="sxs-lookup"><span data-stu-id="c6e47-103">Add an IoT Edge deployment in a target IoT Hub.</span></span>

## <span data-ttu-id="c6e47-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c6e47-104">SYNTAX</span></span>

### <span data-ttu-id="c6e47-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="c6e47-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 [-ModulesContent <Hashtable>] [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>]
 [-Label <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6e47-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c6e47-106">InputObjectSet</span></span>
```
Add-AzIotHubDeployment [-InputObject] <PSIotHub> -Name <String> [-ModulesContent <Hashtable>]
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6e47-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="c6e47-107">ResourceIdSet</span></span>
```
Add-AzIotHubDeployment [-ResourceId] <String> -Name <String> [-ModulesContent <Hashtable>] [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6e47-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c6e47-108">DESCRIPTION</span></span>
<span data-ttu-id="c6e47-109">Implantações de borda podem ser criadas com métricas definidas pelo usuário para avaliação sob demanda.</span><span class="sxs-lookup"><span data-stu-id="c6e47-109">Edge deployments can be created with user defined metrics for on demand evaluation.</span></span>
<span data-ttu-id="c6e47-110">Consulte https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="c6e47-110">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring for more information.</span></span>

## <span data-ttu-id="c6e47-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c6e47-111">EXAMPLES</span></span>

### <span data-ttu-id="c6e47-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c6e47-112">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1"
```

<span data-ttu-id="c6e47-113">Criar uma implantação de borda com metadados padrão.</span><span class="sxs-lookup"><span data-stu-id="c6e47-113">Create an Edge deployment with default metadata.</span></span>

### <span data-ttu-id="c6e47-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c6e47-114">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Priority 3 -TargetCondition "tags.building=9 and tags.environment='test'"
```

<span data-ttu-id="c6e47-115">Crie uma implantação de borda com uma prioridade de 3 que se aplica à condição quando um dispositivo é marcado no prédio 9 e o ambiente é ' teste '.</span><span class="sxs-lookup"><span data-stu-id="c6e47-115">Create an Edge deployment with a priority of 3 that applies on condition when a device is tagged in building 9 and the environment is 'test'.</span></span>

### <span data-ttu-id="c6e47-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c6e47-116">Example 2</span></span>
```powershell
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Metric $metrics
```

<span data-ttu-id="c6e47-117">Crie uma implantação de borda com métricas de usuário.</span><span class="sxs-lookup"><span data-stu-id="c6e47-117">Create an Edge deployment with user metrics.</span></span>

### <span data-ttu-id="c6e47-118">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="c6e47-118">Example 3</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $labels.add("key1","value1")
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Label $labels
```

<span data-ttu-id="c6e47-119">Criar uma implantação de borda com rótulos.</span><span class="sxs-lookup"><span data-stu-id="c6e47-119">Create an Edge deployment with labels.</span></span>

### <span data-ttu-id="c6e47-120">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="c6e47-120">Example 4</span></span>
```powershell
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -ModulesContent $content
```

<span data-ttu-id="c6e47-121">Criar uma implantação de borda com conteúdo.</span><span class="sxs-lookup"><span data-stu-id="c6e47-121">Create an Edge deployment with content.</span></span>

## <span data-ttu-id="c6e47-122">OS</span><span class="sxs-lookup"><span data-stu-id="c6e47-122">PARAMETERS</span></span>

### <span data-ttu-id="c6e47-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6e47-123">-DefaultProfile</span></span>
<span data-ttu-id="c6e47-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c6e47-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6e47-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c6e47-125">-InputObject</span></span>
<span data-ttu-id="c6e47-126">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="c6e47-126">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6e47-127">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="c6e47-127">-IotHubName</span></span>
<span data-ttu-id="c6e47-128">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="c6e47-128">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6e47-129">-Rótulo</span><span class="sxs-lookup"><span data-stu-id="c6e47-129">-Label</span></span>
<span data-ttu-id="c6e47-130">Mapa de rótulos a serem aplicados à implantação de destino.</span><span class="sxs-lookup"><span data-stu-id="c6e47-130">Map of labels to be applied to target deployment.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6e47-131">-Métrica</span><span class="sxs-lookup"><span data-stu-id="c6e47-131">-Metric</span></span>
<span data-ttu-id="c6e47-132">Coleção queries para definição de métricas de implantação de borda IoT.</span><span class="sxs-lookup"><span data-stu-id="c6e47-132">Queries collection for IoT Edge deployment metrics definition.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6e47-133">-ModulesContent</span><span class="sxs-lookup"><span data-stu-id="c6e47-133">-ModulesContent</span></span>
<span data-ttu-id="c6e47-134">Conteúdo de implantação de módulos para dispositivos de borda IoT.</span><span class="sxs-lookup"><span data-stu-id="c6e47-134">Deployment content of modules for IoT Edge devices.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6e47-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="c6e47-135">-Name</span></span>
<span data-ttu-id="c6e47-136">Identificador para a implantação.</span><span class="sxs-lookup"><span data-stu-id="c6e47-136">Identifier for the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6e47-137">-Priority</span><span class="sxs-lookup"><span data-stu-id="c6e47-137">-Priority</span></span>
<span data-ttu-id="c6e47-138">Peso da implantação em caso de regras concorrentes (WINS mais alto).</span><span class="sxs-lookup"><span data-stu-id="c6e47-138">Weight of deployment in case of competing rules (highest wins).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6e47-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6e47-139">-ResourceGroupName</span></span>
<span data-ttu-id="c6e47-140">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="c6e47-140">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6e47-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c6e47-141">-ResourceId</span></span>
<span data-ttu-id="c6e47-142">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="c6e47-142">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6e47-143">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="c6e47-143">-TargetCondition</span></span>
<span data-ttu-id="c6e47-144">A condição de destino à qual a implantação de borda se aplica.</span><span class="sxs-lookup"><span data-stu-id="c6e47-144">Target condition in which an Edge deployment applies to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6e47-145">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c6e47-145">-Confirm</span></span>
<span data-ttu-id="c6e47-146">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6e47-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6e47-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6e47-147">-WhatIf</span></span>
<span data-ttu-id="c6e47-148">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c6e47-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6e47-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c6e47-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6e47-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6e47-150">CommonParameters</span></span>
<span data-ttu-id="c6e47-151">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6e47-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6e47-152">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6e47-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6e47-153">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c6e47-153">INPUTS</span></span>

### <span data-ttu-id="c6e47-154">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="c6e47-154">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="c6e47-155">System. String</span><span class="sxs-lookup"><span data-stu-id="c6e47-155">System.String</span></span>

## <span data-ttu-id="c6e47-156">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c6e47-156">OUTPUTS</span></span>

### <span data-ttu-id="c6e47-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSDEployment</span><span class="sxs-lookup"><span data-stu-id="c6e47-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span></span>

## <span data-ttu-id="c6e47-158">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c6e47-158">NOTES</span></span>

## <span data-ttu-id="c6e47-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c6e47-159">RELATED LINKS</span></span>
