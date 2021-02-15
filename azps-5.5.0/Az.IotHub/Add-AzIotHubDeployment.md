---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubDeployment.md
ms.openlocfilehash: 0e3065cb2ee668f6b0ef5b20ac25ee51d922edc7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113786"
---
# <span data-ttu-id="0e381-101">Add-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="0e381-101">Add-AzIotHubDeployment</span></span>

## <span data-ttu-id="0e381-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0e381-102">SYNOPSIS</span></span>
<span data-ttu-id="0e381-103">Adicione uma implantação de borda IoT em um Hub de IoT de destino.</span><span class="sxs-lookup"><span data-stu-id="0e381-103">Add an IoT Edge deployment in a target IoT Hub.</span></span>

## <span data-ttu-id="0e381-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0e381-104">SYNTAX</span></span>

### <span data-ttu-id="0e381-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="0e381-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 [-ModulesContent <Hashtable>] [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>]
 [-Label <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e381-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="0e381-106">InputObjectSet</span></span>
```
Add-AzIotHubDeployment [-InputObject] <PSIotHub> -Name <String> [-ModulesContent <Hashtable>]
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e381-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="0e381-107">ResourceIdSet</span></span>
```
Add-AzIotHubDeployment [-ResourceId] <String> -Name <String> [-ModulesContent <Hashtable>] [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e381-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="0e381-108">DESCRIPTION</span></span>
<span data-ttu-id="0e381-109">As implantações de borda podem ser criadas com métricas definidas pelo usuário para avaliação sob demanda.</span><span class="sxs-lookup"><span data-stu-id="0e381-109">Edge deployments can be created with user defined metrics for on demand evaluation.</span></span>
<span data-ttu-id="0e381-110">Confira https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring mais informações.</span><span class="sxs-lookup"><span data-stu-id="0e381-110">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring for more information.</span></span>

## <span data-ttu-id="0e381-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0e381-111">EXAMPLES</span></span>

### <span data-ttu-id="0e381-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="0e381-112">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1"
```

<span data-ttu-id="0e381-113">Crie uma implantação de Borda com metadados padrão.</span><span class="sxs-lookup"><span data-stu-id="0e381-113">Create an Edge deployment with default metadata.</span></span>

### <span data-ttu-id="0e381-114">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="0e381-114">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Priority 3 -TargetCondition "tags.building=9 and tags.environment='test'"
```

<span data-ttu-id="0e381-115">Crie uma implantação de Borda com uma prioridade 3 que se aplica na condição quando um dispositivo está marcado no edifício 9 e o ambiente é "teste".</span><span class="sxs-lookup"><span data-stu-id="0e381-115">Create an Edge deployment with a priority of 3 that applies on condition when a device is tagged in building 9 and the environment is 'test'.</span></span>

### <span data-ttu-id="0e381-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="0e381-116">Example 2</span></span>
```powershell
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Metric $metrics
```

<span data-ttu-id="0e381-117">Crie uma implantação de Borda com métricas de usuário.</span><span class="sxs-lookup"><span data-stu-id="0e381-117">Create an Edge deployment with user metrics.</span></span>

### <span data-ttu-id="0e381-118">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="0e381-118">Example 3</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $labels.add("key1","value1")
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Label $labels
```

<span data-ttu-id="0e381-119">Crie uma implantação de Borda com rótulos.</span><span class="sxs-lookup"><span data-stu-id="0e381-119">Create an Edge deployment with labels.</span></span>

### <span data-ttu-id="0e381-120">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="0e381-120">Example 4</span></span>
```powershell
PS C:\> $content = Get-Content "C:/Edge/modules.json" | ConvertFrom-Json -AsHashtable
PS C:\> Add-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -ModulesContent $content -TargetCondition "from devices.modules where tags.environment='test'"
```

<span data-ttu-id="0e381-121">Crie uma implantação de Borda com conteúdo.</span><span class="sxs-lookup"><span data-stu-id="0e381-121">Create an Edge deployment with content.</span></span>

## <span data-ttu-id="0e381-122">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0e381-122">PARAMETERS</span></span>

### <span data-ttu-id="0e381-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e381-123">-DefaultProfile</span></span>
<span data-ttu-id="0e381-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="0e381-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e381-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0e381-125">-InputObject</span></span>
<span data-ttu-id="0e381-126">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="0e381-126">IotHub object</span></span>

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

### <span data-ttu-id="0e381-127">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="0e381-127">-IotHubName</span></span>
<span data-ttu-id="0e381-128">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="0e381-128">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="0e381-129">-Rótulo</span><span class="sxs-lookup"><span data-stu-id="0e381-129">-Label</span></span>
<span data-ttu-id="0e381-130">Mapa de rótulos a serem aplicados à implantação de destino.</span><span class="sxs-lookup"><span data-stu-id="0e381-130">Map of labels to be applied to target deployment.</span></span>

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

### <span data-ttu-id="0e381-131">-Métrica</span><span class="sxs-lookup"><span data-stu-id="0e381-131">-Metric</span></span>
<span data-ttu-id="0e381-132">Conjunto de consultas para definição de métricas de implantação de borda IoT.</span><span class="sxs-lookup"><span data-stu-id="0e381-132">Queries collection for IoT Edge deployment metrics definition.</span></span>

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

### <span data-ttu-id="0e381-133">-ModulesContent</span><span class="sxs-lookup"><span data-stu-id="0e381-133">-ModulesContent</span></span>
<span data-ttu-id="0e381-134">Conteúdo de implantação de módulos para dispositivos de borda IoT.</span><span class="sxs-lookup"><span data-stu-id="0e381-134">Deployment content of modules for IoT Edge devices.</span></span>

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

### <span data-ttu-id="0e381-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="0e381-135">-Name</span></span>
<span data-ttu-id="0e381-136">Identificador da implantação.</span><span class="sxs-lookup"><span data-stu-id="0e381-136">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="0e381-137">-Prioridade</span><span class="sxs-lookup"><span data-stu-id="0e381-137">-Priority</span></span>
<span data-ttu-id="0e381-138">Peso da implantação em caso de regras concorrentes (maiores vitórias).</span><span class="sxs-lookup"><span data-stu-id="0e381-138">Weight of deployment in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="0e381-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e381-139">-ResourceGroupName</span></span>
<span data-ttu-id="0e381-140">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="0e381-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="0e381-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0e381-141">-ResourceId</span></span>
<span data-ttu-id="0e381-142">ID de Recurso do IotHub</span><span class="sxs-lookup"><span data-stu-id="0e381-142">IotHub Resource Id</span></span>

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

### <span data-ttu-id="0e381-143">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="0e381-143">-TargetCondition</span></span>
<span data-ttu-id="0e381-144">Condição de destino na qual uma implantação de borda se aplica.</span><span class="sxs-lookup"><span data-stu-id="0e381-144">Target condition in which an Edge deployment applies to.</span></span>

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

### <span data-ttu-id="0e381-145">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="0e381-145">-Confirm</span></span>
<span data-ttu-id="0e381-146">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e381-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e381-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e381-147">-WhatIf</span></span>
<span data-ttu-id="0e381-148">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="0e381-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e381-149">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="0e381-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e381-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e381-150">CommonParameters</span></span>
<span data-ttu-id="0e381-151">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e381-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e381-152">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e381-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e381-153">Entradas</span><span class="sxs-lookup"><span data-stu-id="0e381-153">INPUTS</span></span>

### <span data-ttu-id="0e381-154">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="0e381-154">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="0e381-155">System.String</span><span class="sxs-lookup"><span data-stu-id="0e381-155">System.String</span></span>

## <span data-ttu-id="0e381-156">Saídas</span><span class="sxs-lookup"><span data-stu-id="0e381-156">OUTPUTS</span></span>

### <span data-ttu-id="0e381-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="0e381-157">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span></span>

## <span data-ttu-id="0e381-158">Notas</span><span class="sxs-lookup"><span data-stu-id="0e381-158">NOTES</span></span>

## <span data-ttu-id="0e381-159">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0e381-159">RELATED LINKS</span></span>
