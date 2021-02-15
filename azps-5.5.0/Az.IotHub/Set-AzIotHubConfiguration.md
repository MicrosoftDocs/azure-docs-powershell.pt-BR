---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubConfiguration.md
ms.openlocfilehash: 40fa5d382972c53de94187c9731748be5b1bfe2a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114303"
---
# <span data-ttu-id="a10eb-101">Set-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="a10eb-101">Set-AzIotHubConfiguration</span></span>

## <span data-ttu-id="a10eb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a10eb-102">SYNOPSIS</span></span>
<span data-ttu-id="a10eb-103">Atualize os campos de mutável do registro de configuração.</span><span class="sxs-lookup"><span data-stu-id="a10eb-103">Update the mutable fields of the configuration registration.</span></span>

## <span data-ttu-id="a10eb-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a10eb-104">SYNTAX</span></span>

### <span data-ttu-id="a10eb-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a10eb-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> [-Name] <String>
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a10eb-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a10eb-106">InputObjectSet</span></span>
```
Set-AzIotHubConfiguration [-InputObject] <PSIotHub> [-Name] <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a10eb-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a10eb-107">ResourceIdSet</span></span>
```
Set-AzIotHubConfiguration [-ResourceId] <String> [-Name] <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a10eb-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="a10eb-108">DESCRIPTION</span></span>
<span data-ttu-id="a10eb-109">Atualize as propriedades especificadas de uma configuração de gerenciamento de dispositivo automática de IoT.</span><span class="sxs-lookup"><span data-stu-id="a10eb-109">Update specified properties of an IoT automatic device management configuration.</span></span>
<span data-ttu-id="a10eb-110">Observação: o conteúdo da configuração é imutável.</span><span class="sxs-lookup"><span data-stu-id="a10eb-110">Note: Configuration content is immutable.</span></span> <span data-ttu-id="a10eb-111">As propriedades de configuração que podem ser atualizadas são "rótulos", "métricas", "prioridade" e "targetCondition".</span><span class="sxs-lookup"><span data-stu-id="a10eb-111">Configuration properties that can be updated are 'labels', 'metrics', 'priority' and 'targetCondition'.</span></span>
<span data-ttu-id="a10eb-112">Confira https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management mais informações.</span><span class="sxs-lookup"><span data-stu-id="a10eb-112">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="a10eb-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a10eb-113">EXAMPLES</span></span>

### <span data-ttu-id="a10eb-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a10eb-114">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Priority 7 -TargetCondition "tags.building=3 and tags.environment='dev'"
```

<span data-ttu-id="a10eb-115">Alterar a prioridade de uma configuração de dispositivo e atualizar sua condição de destino</span><span class="sxs-lookup"><span data-stu-id="a10eb-115">Alter the priority of a device configuration and update its target condition</span></span>

### <span data-ttu-id="a10eb-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="a10eb-116">Example 2</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Set-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Label $labels -Metric $metrics
```

<span data-ttu-id="a10eb-117">Atualizar as métricas e rótulos de uma configuração de dispositivo</span><span class="sxs-lookup"><span data-stu-id="a10eb-117">Update the metrics and labels of a device configuration</span></span>

## <span data-ttu-id="a10eb-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a10eb-118">PARAMETERS</span></span>

### <span data-ttu-id="a10eb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a10eb-119">-DefaultProfile</span></span>
<span data-ttu-id="a10eb-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a10eb-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a10eb-121">-Forçar</span><span class="sxs-lookup"><span data-stu-id="a10eb-121">-Force</span></span>
<span data-ttu-id="a10eb-122">Permite que o objeto de configuração seja substituído mesmo se ele tiver sido atualizado desde que foi recuperado da última vez.</span><span class="sxs-lookup"><span data-stu-id="a10eb-122">Allows configuration object to be replaced even if it was updated since it was retrieved last time.</span></span>

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

### <span data-ttu-id="a10eb-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a10eb-123">-InputObject</span></span>
<span data-ttu-id="a10eb-124">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="a10eb-124">IotHub object</span></span>

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

### <span data-ttu-id="a10eb-125">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="a10eb-125">-IotHubName</span></span>
<span data-ttu-id="a10eb-126">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="a10eb-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="a10eb-127">-Rótulo</span><span class="sxs-lookup"><span data-stu-id="a10eb-127">-Label</span></span>
<span data-ttu-id="a10eb-128">Mapa de rótulos a serem aplicados à configuração de destino.</span><span class="sxs-lookup"><span data-stu-id="a10eb-128">Map of labels to be applied to target configuration.</span></span>

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

### <span data-ttu-id="a10eb-129">-Métrica</span><span class="sxs-lookup"><span data-stu-id="a10eb-129">-Metric</span></span>
<span data-ttu-id="a10eb-130">Conjunto de consultas para definição de métricas de configuração.</span><span class="sxs-lookup"><span data-stu-id="a10eb-130">Queries collection for configuration metrics definition.</span></span>

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

### <span data-ttu-id="a10eb-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="a10eb-131">-Name</span></span>
<span data-ttu-id="a10eb-132">Identificador da configuração.</span><span class="sxs-lookup"><span data-stu-id="a10eb-132">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="a10eb-133">-Prioridade</span><span class="sxs-lookup"><span data-stu-id="a10eb-133">-Priority</span></span>
<span data-ttu-id="a10eb-134">Peso da configuração do dispositivo em caso de regras concorrentes (maiores vitórias).</span><span class="sxs-lookup"><span data-stu-id="a10eb-134">Weight of the device configuration in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="a10eb-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a10eb-135">-ResourceGroupName</span></span>
<span data-ttu-id="a10eb-136">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="a10eb-136">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a10eb-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a10eb-137">-ResourceId</span></span>
<span data-ttu-id="a10eb-138">ID de Recurso do IotHub</span><span class="sxs-lookup"><span data-stu-id="a10eb-138">IotHub Resource Id</span></span>

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

### <span data-ttu-id="a10eb-139">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="a10eb-139">-TargetCondition</span></span>
<span data-ttu-id="a10eb-140">Condição de destino à qual uma configuração de dispositivo se aplica.</span><span class="sxs-lookup"><span data-stu-id="a10eb-140">Target condition in which a device configuration applies to.</span></span>

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

### <span data-ttu-id="a10eb-141">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="a10eb-141">-Confirm</span></span>
<span data-ttu-id="a10eb-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a10eb-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a10eb-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a10eb-143">-WhatIf</span></span>
<span data-ttu-id="a10eb-144">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="a10eb-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a10eb-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a10eb-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a10eb-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a10eb-146">CommonParameters</span></span>
<span data-ttu-id="a10eb-147">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a10eb-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a10eb-148">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a10eb-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a10eb-149">Entradas</span><span class="sxs-lookup"><span data-stu-id="a10eb-149">INPUTS</span></span>

### <span data-ttu-id="a10eb-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="a10eb-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="a10eb-151">System.String</span><span class="sxs-lookup"><span data-stu-id="a10eb-151">System.String</span></span>

## <span data-ttu-id="a10eb-152">Saídas</span><span class="sxs-lookup"><span data-stu-id="a10eb-152">OUTPUTS</span></span>

### <span data-ttu-id="a10eb-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span><span class="sxs-lookup"><span data-stu-id="a10eb-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span></span>

## <span data-ttu-id="a10eb-154">Notas</span><span class="sxs-lookup"><span data-stu-id="a10eb-154">NOTES</span></span>

## <span data-ttu-id="a10eb-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a10eb-155">RELATED LINKS</span></span>
