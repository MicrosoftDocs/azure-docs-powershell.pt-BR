---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/set-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubConfiguration.md
ms.openlocfilehash: a0a3b4c27d3ed2f73efacade6136e8407764b5be
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886479"
---
# <span data-ttu-id="38dfa-101">Set-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="38dfa-101">Set-AzIotHubConfiguration</span></span>

## <span data-ttu-id="38dfa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38dfa-102">SYNOPSIS</span></span>
<span data-ttu-id="38dfa-103">Atualize os campos de mutáveis do registro de configuração.</span><span class="sxs-lookup"><span data-stu-id="38dfa-103">Update the mutable fields of the configuration registration.</span></span>

## <span data-ttu-id="38dfa-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="38dfa-104">SYNTAX</span></span>

### <span data-ttu-id="38dfa-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="38dfa-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> [-Name] <String>
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38dfa-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="38dfa-106">InputObjectSet</span></span>
```
Set-AzIotHubConfiguration [-InputObject] <PSIotHub> [-Name] <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38dfa-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="38dfa-107">ResourceIdSet</span></span>
```
Set-AzIotHubConfiguration [-ResourceId] <String> [-Name] <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38dfa-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="38dfa-108">DESCRIPTION</span></span>
<span data-ttu-id="38dfa-109">Atualize as propriedades especificadas de uma configuração de gerenciamento automático de dispositivoSoT.</span><span class="sxs-lookup"><span data-stu-id="38dfa-109">Update specified properties of an IoT automatic device management configuration.</span></span>
<span data-ttu-id="38dfa-110">Observação: o conteúdo da configuração é imutável.</span><span class="sxs-lookup"><span data-stu-id="38dfa-110">Note: Configuration content is immutable.</span></span> <span data-ttu-id="38dfa-111">As propriedades de configuração que podem ser atualizadas são 'labels', 'metrics', 'priority' e 'targetCondition'.</span><span class="sxs-lookup"><span data-stu-id="38dfa-111">Configuration properties that can be updated are 'labels', 'metrics', 'priority' and 'targetCondition'.</span></span>
<span data-ttu-id="38dfa-112">Confira https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management mais informações.</span><span class="sxs-lookup"><span data-stu-id="38dfa-112">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="38dfa-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="38dfa-113">EXAMPLES</span></span>

### <span data-ttu-id="38dfa-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="38dfa-114">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Priority 7 -TargetCondition "tags.building=3 and tags.environment='dev'"
```

<span data-ttu-id="38dfa-115">Altere a prioridade de uma configuração de dispositivo e atualize sua condição de destino</span><span class="sxs-lookup"><span data-stu-id="38dfa-115">Alter the priority of a device configuration and update its target condition</span></span>

### <span data-ttu-id="38dfa-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="38dfa-116">Example 2</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Set-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Label $labels -Metric $metrics
```

<span data-ttu-id="38dfa-117">Atualizar as métricas e rótulos de uma configuração de dispositivo</span><span class="sxs-lookup"><span data-stu-id="38dfa-117">Update the metrics and labels of a device configuration</span></span>

## <span data-ttu-id="38dfa-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="38dfa-118">PARAMETERS</span></span>

### <span data-ttu-id="38dfa-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38dfa-119">-DefaultProfile</span></span>
<span data-ttu-id="38dfa-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="38dfa-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38dfa-121">-Force</span><span class="sxs-lookup"><span data-stu-id="38dfa-121">-Force</span></span>
<span data-ttu-id="38dfa-122">Permite que o objeto de configuração seja substituído mesmo que ele foi atualizado desde que foi recuperado da última vez.</span><span class="sxs-lookup"><span data-stu-id="38dfa-122">Allows configuration object to be replaced even if it was updated since it was retrieved last time.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38dfa-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="38dfa-123">-InputObject</span></span>
<span data-ttu-id="38dfa-124">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="38dfa-124">IotHub object</span></span>

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

### <span data-ttu-id="38dfa-125">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="38dfa-125">-IotHubName</span></span>
<span data-ttu-id="38dfa-126">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="38dfa-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="38dfa-127">-Label</span><span class="sxs-lookup"><span data-stu-id="38dfa-127">-Label</span></span>
<span data-ttu-id="38dfa-128">Mapa de rótulos a serem aplicados à configuração de destino.</span><span class="sxs-lookup"><span data-stu-id="38dfa-128">Map of labels to be applied to target configuration.</span></span>

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

### <span data-ttu-id="38dfa-129">-Metric</span><span class="sxs-lookup"><span data-stu-id="38dfa-129">-Metric</span></span>
<span data-ttu-id="38dfa-130">Coleção Consultas para definição de métricas de configuração.</span><span class="sxs-lookup"><span data-stu-id="38dfa-130">Queries collection for configuration metrics definition.</span></span>

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

### <span data-ttu-id="38dfa-131">-Name</span><span class="sxs-lookup"><span data-stu-id="38dfa-131">-Name</span></span>
<span data-ttu-id="38dfa-132">Identificador da configuração.</span><span class="sxs-lookup"><span data-stu-id="38dfa-132">Identifier for the configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38dfa-133">-Priority</span><span class="sxs-lookup"><span data-stu-id="38dfa-133">-Priority</span></span>
<span data-ttu-id="38dfa-134">Peso da configuração do dispositivo no caso de regras concorrentes (maiores ganhos).</span><span class="sxs-lookup"><span data-stu-id="38dfa-134">Weight of the device configuration in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="38dfa-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38dfa-135">-ResourceGroupName</span></span>
<span data-ttu-id="38dfa-136">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="38dfa-136">Name of the Resource Group</span></span>

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

### <span data-ttu-id="38dfa-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="38dfa-137">-ResourceId</span></span>
<span data-ttu-id="38dfa-138">Id de Recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="38dfa-138">IotHub Resource Id</span></span>

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

### <span data-ttu-id="38dfa-139">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="38dfa-139">-TargetCondition</span></span>
<span data-ttu-id="38dfa-140">Condição de destino na qual uma configuração de dispositivo se aplica.</span><span class="sxs-lookup"><span data-stu-id="38dfa-140">Target condition in which a device configuration applies to.</span></span>

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

### <span data-ttu-id="38dfa-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="38dfa-141">-Confirm</span></span>
<span data-ttu-id="38dfa-142">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38dfa-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38dfa-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38dfa-143">-WhatIf</span></span>
<span data-ttu-id="38dfa-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="38dfa-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38dfa-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="38dfa-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38dfa-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38dfa-146">CommonParameters</span></span>
<span data-ttu-id="38dfa-147">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38dfa-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38dfa-148">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38dfa-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38dfa-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="38dfa-149">INPUTS</span></span>

### <span data-ttu-id="38dfa-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="38dfa-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="38dfa-151">System.String</span><span class="sxs-lookup"><span data-stu-id="38dfa-151">System.String</span></span>

## <span data-ttu-id="38dfa-152">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="38dfa-152">OUTPUTS</span></span>

### <span data-ttu-id="38dfa-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span><span class="sxs-lookup"><span data-stu-id="38dfa-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span></span>

## <span data-ttu-id="38dfa-154">NOTES</span><span class="sxs-lookup"><span data-stu-id="38dfa-154">NOTES</span></span>

## <span data-ttu-id="38dfa-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="38dfa-155">RELATED LINKS</span></span>
