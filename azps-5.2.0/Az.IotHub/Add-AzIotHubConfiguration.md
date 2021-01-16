---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/add-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Add-AzIotHubConfiguration.md
ms.openlocfilehash: d84d5b172d1a22880b508f8b43f071d5d454cf38
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260855"
---
# <span data-ttu-id="4211f-101">Add-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="4211f-101">Add-AzIotHubConfiguration</span></span>

## <span data-ttu-id="4211f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4211f-102">SYNOPSIS</span></span>
<span data-ttu-id="4211f-103">Adicionar uma configuração de gerenciamento automático de dispositivo IoT em um hub IoT de destino.</span><span class="sxs-lookup"><span data-stu-id="4211f-103">Add an IoT automatic device management configuration in a target IoT Hub.</span></span>

## <span data-ttu-id="4211f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4211f-104">SYNTAX</span></span>

### <span data-ttu-id="4211f-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="4211f-105">ResourceSet (Default)</span></span>
```
Add-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 [-DeviceContent <Hashtable>] [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>]
 [-Label <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4211f-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4211f-106">InputObjectSet</span></span>
```
Add-AzIotHubConfiguration [-InputObject] <PSIotHub> -Name <String> [-DeviceContent <Hashtable>]
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4211f-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="4211f-107">ResourceIdSet</span></span>
```
Add-AzIotHubConfiguration [-ResourceId] <String> -Name <String> [-DeviceContent <Hashtable>]
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4211f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4211f-108">DESCRIPTION</span></span>
<span data-ttu-id="4211f-109">O conteúdo de configuração é JSON e mais leve varia de acordo com a intenção do dispositivo ou do módulo.</span><span class="sxs-lookup"><span data-stu-id="4211f-109">Configuration content is json and slighty varies based on device or module intent.</span></span> <span data-ttu-id="4211f-110">As configurações de dispositivo estão na forma de {"deviceContent": {...}}</span><span class="sxs-lookup"><span data-stu-id="4211f-110">Device configurations are in the form of {"deviceContent":{...}}</span></span>
<span data-ttu-id="4211f-111">As configurações de módulo estão na forma de {"moduleContent": {...}}</span><span class="sxs-lookup"><span data-stu-id="4211f-111">Module configurations are in the form of {"moduleContent":{...}}</span></span>
<span data-ttu-id="4211f-112">As configurações podem ser definidas com as métricas fornecidas pelo usuário para avaliação sob demanda.</span><span class="sxs-lookup"><span data-stu-id="4211f-112">Configurations can be defined with user provided metrics for on demand evaluation.</span></span>
<span data-ttu-id="4211f-113">As métricas do usuário são JSON e na forma de {"consultas": {...}}</span><span class="sxs-lookup"><span data-stu-id="4211f-113">User metrics are json and in the form of {"queries":{...}}</span></span> <span data-ttu-id="4211f-114">ou {"Metrics": {"consultas": {...}}}.</span><span class="sxs-lookup"><span data-stu-id="4211f-114">or {"metrics":{"queries":{...}}}.</span></span>

<span data-ttu-id="4211f-115">Observação: a condição de destino para módulos deve começar com "from Devices. modules Where".</span><span class="sxs-lookup"><span data-stu-id="4211f-115">Note: Target condition for modules must start with "from devices.modules where".</span></span> <span data-ttu-id="4211f-116">Consulte https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="4211f-116">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="4211f-117">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4211f-117">EXAMPLES</span></span>

### <span data-ttu-id="4211f-118">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4211f-118">Example 1</span></span>
```powershell
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1"
```

<span data-ttu-id="4211f-119">Crie uma configuração de dispositivo com metadados padrão.</span><span class="sxs-lookup"><span data-stu-id="4211f-119">Create a device configuration with default metadata.</span></span>

### <span data-ttu-id="4211f-120">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="4211f-120">Example 2</span></span>
```powershell
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Priority 3 -TargetCondition "tags.building=9 and tags.environment='test'"
```

<span data-ttu-id="4211f-121">Crie uma configuração de dispositivo com uma prioridade de 3 que se aplica à condição quando um dispositivo é marcado no prédio 9 e o ambiente é ' teste '.</span><span class="sxs-lookup"><span data-stu-id="4211f-121">Create a device configuration with a priority of 3 that applies on condition when a device is tagged in building 9 and the environment is 'test'.</span></span>

### <span data-ttu-id="4211f-122">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="4211f-122">Example 3</span></span>
```powershell
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Metric $metrics
```

<span data-ttu-id="4211f-123">Crie uma configuração de dispositivo com métricas de usuário.</span><span class="sxs-lookup"><span data-stu-id="4211f-123">Create a device configuration with user metrics.</span></span>

### <span data-ttu-id="4211f-124">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="4211f-124">Example 4</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $labels.add("key1","value1")
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Label $labels
```

<span data-ttu-id="4211f-125">Crie uma configuração de dispositivo com rótulos.</span><span class="sxs-lookup"><span data-stu-id="4211f-125">Create a device configuration with labels.</span></span>

### <span data-ttu-id="4211f-126">Exemplo 5</span><span class="sxs-lookup"><span data-stu-id="4211f-126">Example 5</span></span>
```powershell
PS C:\> $prop = @{}
PS C:\> $prop.add("Location", "US")
PS C:\> $content = @{}
PS C:\> $content.add("properties.desired.Region", $prop)
PS C:\> Add-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -DeviceContent $content
```

<span data-ttu-id="4211f-127">Crie uma configuração de dispositivo com conteúdo.</span><span class="sxs-lookup"><span data-stu-id="4211f-127">Create a device configuration with content.</span></span>

## <span data-ttu-id="4211f-128">OS</span><span class="sxs-lookup"><span data-stu-id="4211f-128">PARAMETERS</span></span>

### <span data-ttu-id="4211f-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4211f-129">-DefaultProfile</span></span>
<span data-ttu-id="4211f-130">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4211f-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4211f-131">-DeviceContent</span><span class="sxs-lookup"><span data-stu-id="4211f-131">-DeviceContent</span></span>
<span data-ttu-id="4211f-132">Configuração para dispositivos IotHub.</span><span class="sxs-lookup"><span data-stu-id="4211f-132">Configuration for IotHub devices.</span></span>

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

### <span data-ttu-id="4211f-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4211f-133">-InputObject</span></span>
<span data-ttu-id="4211f-134">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="4211f-134">IotHub object</span></span>

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

### <span data-ttu-id="4211f-135">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="4211f-135">-IotHubName</span></span>
<span data-ttu-id="4211f-136">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="4211f-136">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="4211f-137">-Rótulo</span><span class="sxs-lookup"><span data-stu-id="4211f-137">-Label</span></span>
<span data-ttu-id="4211f-138">Mapa de rótulos a serem aplicados à configuração de destino.</span><span class="sxs-lookup"><span data-stu-id="4211f-138">Map of labels to be applied to target configuration.</span></span>

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

### <span data-ttu-id="4211f-139">-Métrica</span><span class="sxs-lookup"><span data-stu-id="4211f-139">-Metric</span></span>
<span data-ttu-id="4211f-140">Coleção queries para definição de métricas de configuração.</span><span class="sxs-lookup"><span data-stu-id="4211f-140">Queries collection for configuration metrics definition.</span></span>

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

### <span data-ttu-id="4211f-141">-Nome</span><span class="sxs-lookup"><span data-stu-id="4211f-141">-Name</span></span>
<span data-ttu-id="4211f-142">Identificador para a configuração.</span><span class="sxs-lookup"><span data-stu-id="4211f-142">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="4211f-143">-Priority</span><span class="sxs-lookup"><span data-stu-id="4211f-143">-Priority</span></span>
<span data-ttu-id="4211f-144">Peso da configuração do dispositivo em caso de regras concorrentes (WINS mais alto).</span><span class="sxs-lookup"><span data-stu-id="4211f-144">Weight of the device configuration in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="4211f-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4211f-145">-ResourceGroupName</span></span>
<span data-ttu-id="4211f-146">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="4211f-146">Name of the Resource Group</span></span>

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

### <span data-ttu-id="4211f-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4211f-147">-ResourceId</span></span>
<span data-ttu-id="4211f-148">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="4211f-148">IotHub Resource Id</span></span>

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

### <span data-ttu-id="4211f-149">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="4211f-149">-TargetCondition</span></span>
<span data-ttu-id="4211f-150">A condição de destino à qual a configuração do dispositivo se aplica.</span><span class="sxs-lookup"><span data-stu-id="4211f-150">Target condition in which a device configuration applies to.</span></span>

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

### <span data-ttu-id="4211f-151">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4211f-151">-Confirm</span></span>
<span data-ttu-id="4211f-152">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4211f-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4211f-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4211f-153">-WhatIf</span></span>
<span data-ttu-id="4211f-154">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4211f-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4211f-155">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4211f-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4211f-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4211f-156">CommonParameters</span></span>
<span data-ttu-id="4211f-157">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4211f-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4211f-158">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4211f-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4211f-159">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4211f-159">INPUTS</span></span>

### <span data-ttu-id="4211f-160">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="4211f-160">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="4211f-161">System. String</span><span class="sxs-lookup"><span data-stu-id="4211f-161">System.String</span></span>

## <span data-ttu-id="4211f-162">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4211f-162">OUTPUTS</span></span>

### <span data-ttu-id="4211f-163">Microsoft. Azure. Commands. Management. IotHub. Models. PSConfiguration</span><span class="sxs-lookup"><span data-stu-id="4211f-163">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span></span>

## <span data-ttu-id="4211f-164">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4211f-164">NOTES</span></span>

## <span data-ttu-id="4211f-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4211f-165">RELATED LINKS</span></span>
