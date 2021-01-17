---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeployment.md
ms.openlocfilehash: 0e3065cb2ee668f6b0ef5b20ac25ee51d922edc7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98433670"
---
# <span data-ttu-id="6f1af-101">Add-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="6f1af-101">Add-AzIotHubDeployment</span></span>

## <span data-ttu-id="6f1af-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6f1af-102">SYNOPSIS</span></span>
<span data-ttu-id="6f1af-103">Adicionar uma implantação de borda IoT a um hub IoT de destino.</span><span class="sxs-lookup"><span data-stu-id="6f1af-103">Add an IoT Edge deployment in a target IoT Hub.</span></span>

## <span data-ttu-id="6f1af-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6f1af-104">SYNTAX</span></span>

### <span data-ttu-id="6f1af-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="6f1af-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 [-ModulesContent <Hashtable>] [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>]
 [-Label <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f1af-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6f1af-106">InputObjectSet</span></span>
```
Add-AzIotHubDeployment [-InputObject] <PSIotHub> -Name <String> [-ModulesContent <Hashtable>]
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f1af-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="6f1af-107">ResourceIdSet</span></span>
```
Add-AzIotHubDeployment [-ResourceId] <String> -Name <String> [-ModulesContent <Hashtable>] [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f1af-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6f1af-108">DESCRIPTION</span></span>
<span data-ttu-id="6f1af-109">Implantações de borda podem ser criadas com métricas definidas pelo usuário para avaliação sob demanda.</span><span class="sxs-lookup"><span data-stu-id="6f1af-109">Edge deployments can be created with user defined metrics for on demand evaluation.</span></span>
<span data-ttu-id="6f1af-110">Consulte https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="6f1af-110">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring for more information.</span></span>

## <span data-ttu-id="6f1af-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6f1af-111">EXAMPLES</span></span>

### <span data-ttu-id="6f1af-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6f1af-112">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1"
```

<span data-ttu-id="6f1af-113">Criar uma implantação de borda com metadados padrão.</span><span class="sxs-lookup"><span data-stu-id="6f1af-113">Create an Edge deployment with default metadata.</span></span>

### <span data-ttu-id="6f1af-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="6f1af-114">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Priority 3 -TargetCondition "tags.building=9 and tags.environment='test'"
```

<span data-ttu-id="6f1af-115">Crie uma implantação de borda com uma prioridade de 3 que se aplica à condição quando um dispositivo é marcado no prédio 9 e o ambiente é ' teste '.</span><span class="sxs-lookup"><span data-stu-id="6f1af-115">Create an Edge deployment with a priority of 3 that applies on condition when a device is tagged in building 9 and the environment is 'test'.</span></span>

### <span data-ttu-id="6f1af-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="6f1af-116">Example 2</span></span>
```powershell
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Metric $metrics
```

<span data-ttu-id="6f1af-117">Crie uma implantação de borda com métricas de usuário.</span><span class="sxs-lookup"><span data-stu-id="6f1af-117">Create an Edge deployment with user metrics.</span></span>

### <span data-ttu-id="6f1af-118">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="6f1af-118">Example 3</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $labels.add("key1","value1")
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Label $labels
```

<span data-ttu-id="6f1af-119">Criar uma implantação de borda com rótulos.</span><span class="sxs-lookup"><span data-stu-id="6f1af-119">Create an Edge deployment with labels.</span></span>

### <span data-ttu-id="6f1af-120">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="6f1af-120">Example 4</span></span>
```powershell
PS C:\> $content = Get-Content "C:/Edge/modules.json" | ConvertFrom-Json -AsHashtable
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -ModulesContent $content -TargetCondition "from devices.modules where tags.environment='test'"
```

<span data-ttu-id="6f1af-121">Criar uma implantação de borda com conteúdo.</span><span class="sxs-lookup"><span data-stu-id="6f1af-121">Create an Edge deployment with content.</span></span>

## <span data-ttu-id="6f1af-122">OS</span><span class="sxs-lookup"><span data-stu-id="6f1af-122">PARAMETERS</span></span>

### <span data-ttu-id="6f1af-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f1af-123">-DefaultProfile</span></span>
<span data-ttu-id="6f1af-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6f1af-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f1af-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6f1af-125">-InputObject</span></span>
<span data-ttu-id="6f1af-126">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="6f1af-126">IotHub object</span></span>

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

### <span data-ttu-id="6f1af-127">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="6f1af-127">-IotHubName</span></span>
<span data-ttu-id="6f1af-128">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="6f1af-128">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="6f1af-129">-Rótulo</span><span class="sxs-lookup"><span data-stu-id="6f1af-129">-Label</span></span>
<span data-ttu-id="6f1af-130">Mapa de rótulos a serem aplicados à implantação de destino.</span><span class="sxs-lookup"><span data-stu-id="6f1af-130">Map of labels to be applied to target deployment.</span></span>

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

### <span data-ttu-id="6f1af-131">-Métrica</span><span class="sxs-lookup"><span data-stu-id="6f1af-131">-Metric</span></span>
<span data-ttu-id="6f1af-132">Coleção queries para definição de métricas de implantação de borda IoT.</span><span class="sxs-lookup"><span data-stu-id="6f1af-132">Queries collection for IoT Edge deployment metrics definition.</span></span>

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

### <span data-ttu-id="6f1af-133">-ModulesContent</span><span class="sxs-lookup"><span data-stu-id="6f1af-133">-ModulesContent</span></span>
<span data-ttu-id="6f1af-134">Conteúdo de implantação de módulos para dispositivos de borda IoT.</span><span class="sxs-lookup"><span data-stu-id="6f1af-134">Deployment content of modules for IoT Edge devices.</span></span>

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

### <span data-ttu-id="6f1af-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="6f1af-135">-Name</span></span>
<span data-ttu-id="6f1af-136">Identificador para a implantação.</span><span class="sxs-lookup"><span data-stu-id="6f1af-136">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="6f1af-137">-Priority</span><span class="sxs-lookup"><span data-stu-id="6f1af-137">-Priority</span></span>
<span data-ttu-id="6f1af-138">Peso da implantação em caso de regras concorrentes (WINS mais alto).</span><span class="sxs-lookup"><span data-stu-id="6f1af-138">Weight of deployment in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="6f1af-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f1af-139">-ResourceGroupName</span></span>
<span data-ttu-id="6f1af-140">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="6f1af-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="6f1af-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6f1af-141">-ResourceId</span></span>
<span data-ttu-id="6f1af-142">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="6f1af-142">IotHub Resource Id</span></span>

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

### <span data-ttu-id="6f1af-143">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="6f1af-143">-TargetCondition</span></span>
<span data-ttu-id="6f1af-144">A condição de destino à qual a implantação de borda se aplica.</span><span class="sxs-lookup"><span data-stu-id="6f1af-144">Target condition in which an Edge deployment applies to.</span></span>

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

### <span data-ttu-id="6f1af-145">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6f1af-145">-Confirm</span></span>
<span data-ttu-id="6f1af-146">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f1af-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f1af-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f1af-147">-WhatIf</span></span>
<span data-ttu-id="6f1af-148">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6f1af-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f1af-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6f1af-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f1af-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f1af-150">CommonParameters</span></span>
<span data-ttu-id="6f1af-151">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f1af-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f1af-152">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f1af-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f1af-153">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6f1af-153">INPUTS</span></span>

### <span data-ttu-id="6f1af-154">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="6f1af-154">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="6f1af-155">System. String</span><span class="sxs-lookup"><span data-stu-id="6f1af-155">System.String</span></span>

## <span data-ttu-id="6f1af-156">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6f1af-156">OUTPUTS</span></span>

### <span data-ttu-id="6f1af-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSDEployment</span><span class="sxs-lookup"><span data-stu-id="6f1af-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span></span>

## <span data-ttu-id="6f1af-158">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6f1af-158">NOTES</span></span>

## <span data-ttu-id="6f1af-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6f1af-159">RELATED LINKS</span></span>
