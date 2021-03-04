---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/add-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeployment.md
ms.openlocfilehash: 80494fd18216ce42883a962920ab78bbc2aa628b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891369"
---
# <span data-ttu-id="7a83c-101">Add-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="7a83c-101">Add-AzIotHubDeployment</span></span>

## <span data-ttu-id="7a83c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a83c-102">SYNOPSIS</span></span>
<span data-ttu-id="7a83c-103">Adicione uma implantação de Borda de IoT em um Hub de IoT de destino.</span><span class="sxs-lookup"><span data-stu-id="7a83c-103">Add an IoT Edge deployment in a target IoT Hub.</span></span>

## <span data-ttu-id="7a83c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7a83c-104">SYNTAX</span></span>

### <span data-ttu-id="7a83c-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7a83c-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 [-ModulesContent <Hashtable>] [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>]
 [-Label <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a83c-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7a83c-106">InputObjectSet</span></span>
```
Add-AzIotHubDeployment [-InputObject] <PSIotHub> -Name <String> [-ModulesContent <Hashtable>]
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a83c-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7a83c-107">ResourceIdSet</span></span>
```
Add-AzIotHubDeployment [-ResourceId] <String> -Name <String> [-ModulesContent <Hashtable>] [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a83c-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7a83c-108">DESCRIPTION</span></span>
<span data-ttu-id="7a83c-109">As implantações de borda podem ser criadas com métricas definidas pelo usuário para avaliação sob demanda.</span><span class="sxs-lookup"><span data-stu-id="7a83c-109">Edge deployments can be created with user defined metrics for on demand evaluation.</span></span>
<span data-ttu-id="7a83c-110">Confira https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring mais informações.</span><span class="sxs-lookup"><span data-stu-id="7a83c-110">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring for more information.</span></span>

## <span data-ttu-id="7a83c-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7a83c-111">EXAMPLES</span></span>

### <span data-ttu-id="7a83c-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7a83c-112">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1"
```

<span data-ttu-id="7a83c-113">Crie uma implantação de Borda com metadados padrão.</span><span class="sxs-lookup"><span data-stu-id="7a83c-113">Create an Edge deployment with default metadata.</span></span>

### <span data-ttu-id="7a83c-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="7a83c-114">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Priority 3 -TargetCondition "tags.building=9 and tags.environment='test'"
```

<span data-ttu-id="7a83c-115">Crie uma implantação de Borda com uma prioridade 3 que se aplica na condição quando um dispositivo é marcado no edifício 9 e o ambiente é 'test'.</span><span class="sxs-lookup"><span data-stu-id="7a83c-115">Create an Edge deployment with a priority of 3 that applies on condition when a device is tagged in building 9 and the environment is 'test'.</span></span>

### <span data-ttu-id="7a83c-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="7a83c-116">Example 2</span></span>
```powershell
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Metric $metrics
```

<span data-ttu-id="7a83c-117">Crie uma implantação de Borda com métricas de usuário.</span><span class="sxs-lookup"><span data-stu-id="7a83c-117">Create an Edge deployment with user metrics.</span></span>

### <span data-ttu-id="7a83c-118">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="7a83c-118">Example 3</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $labels.add("key1","value1")
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Label $labels
```

<span data-ttu-id="7a83c-119">Crie uma implantação de Borda com rótulos.</span><span class="sxs-lookup"><span data-stu-id="7a83c-119">Create an Edge deployment with labels.</span></span>

### <span data-ttu-id="7a83c-120">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="7a83c-120">Example 4</span></span>
```powershell
PS C:\> $content = Get-Content "C:/Edge/modules.json" | ConvertFrom-Json -AsHashtable
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -ModulesContent $content -TargetCondition "from devices.modules where tags.environment='test'"
```

<span data-ttu-id="7a83c-121">Crie uma implantação de Borda com conteúdo.</span><span class="sxs-lookup"><span data-stu-id="7a83c-121">Create an Edge deployment with content.</span></span>

## <span data-ttu-id="7a83c-122">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7a83c-122">PARAMETERS</span></span>

### <span data-ttu-id="7a83c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a83c-123">-DefaultProfile</span></span>
<span data-ttu-id="7a83c-124">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7a83c-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a83c-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a83c-125">-InputObject</span></span>
<span data-ttu-id="7a83c-126">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="7a83c-126">IotHub object</span></span>

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

### <span data-ttu-id="7a83c-127">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="7a83c-127">-IotHubName</span></span>
<span data-ttu-id="7a83c-128">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="7a83c-128">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="7a83c-129">-Label</span><span class="sxs-lookup"><span data-stu-id="7a83c-129">-Label</span></span>
<span data-ttu-id="7a83c-130">Mapa de rótulos a serem aplicados à implantação de destino.</span><span class="sxs-lookup"><span data-stu-id="7a83c-130">Map of labels to be applied to target deployment.</span></span>

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

### <span data-ttu-id="7a83c-131">-Metric</span><span class="sxs-lookup"><span data-stu-id="7a83c-131">-Metric</span></span>
<span data-ttu-id="7a83c-132">Coleção Consultas para definição de métricas de implantação de Borda de IoT.</span><span class="sxs-lookup"><span data-stu-id="7a83c-132">Queries collection for IoT Edge deployment metrics definition.</span></span>

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

### <span data-ttu-id="7a83c-133">-ModulesContent</span><span class="sxs-lookup"><span data-stu-id="7a83c-133">-ModulesContent</span></span>
<span data-ttu-id="7a83c-134">Conteúdo de implantação de módulos para dispositivos de Borda de IoT.</span><span class="sxs-lookup"><span data-stu-id="7a83c-134">Deployment content of modules for IoT Edge devices.</span></span>

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

### <span data-ttu-id="7a83c-135">-Name</span><span class="sxs-lookup"><span data-stu-id="7a83c-135">-Name</span></span>
<span data-ttu-id="7a83c-136">Identificador da implantação.</span><span class="sxs-lookup"><span data-stu-id="7a83c-136">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="7a83c-137">-Priority</span><span class="sxs-lookup"><span data-stu-id="7a83c-137">-Priority</span></span>
<span data-ttu-id="7a83c-138">Peso da implantação em caso de regras concorrentes (maiores ganhos).</span><span class="sxs-lookup"><span data-stu-id="7a83c-138">Weight of deployment in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="7a83c-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a83c-139">-ResourceGroupName</span></span>
<span data-ttu-id="7a83c-140">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="7a83c-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="7a83c-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7a83c-141">-ResourceId</span></span>
<span data-ttu-id="7a83c-142">Id de Recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="7a83c-142">IotHub Resource Id</span></span>

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

### <span data-ttu-id="7a83c-143">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="7a83c-143">-TargetCondition</span></span>
<span data-ttu-id="7a83c-144">Condição de destino na qual uma implantação de Borda se aplica.</span><span class="sxs-lookup"><span data-stu-id="7a83c-144">Target condition in which an Edge deployment applies to.</span></span>

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

### <span data-ttu-id="7a83c-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7a83c-145">-Confirm</span></span>
<span data-ttu-id="7a83c-146">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a83c-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a83c-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a83c-147">-WhatIf</span></span>
<span data-ttu-id="7a83c-148">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7a83c-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a83c-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7a83c-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a83c-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a83c-150">CommonParameters</span></span>
<span data-ttu-id="7a83c-151">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a83c-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a83c-152">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a83c-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a83c-153">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7a83c-153">INPUTS</span></span>

### <span data-ttu-id="7a83c-154">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="7a83c-154">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="7a83c-155">System.String</span><span class="sxs-lookup"><span data-stu-id="7a83c-155">System.String</span></span>

## <span data-ttu-id="7a83c-156">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7a83c-156">OUTPUTS</span></span>

### <span data-ttu-id="7a83c-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="7a83c-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span></span>

## <span data-ttu-id="7a83c-158">NOTES</span><span class="sxs-lookup"><span data-stu-id="7a83c-158">NOTES</span></span>

## <span data-ttu-id="7a83c-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7a83c-159">RELATED LINKS</span></span>
