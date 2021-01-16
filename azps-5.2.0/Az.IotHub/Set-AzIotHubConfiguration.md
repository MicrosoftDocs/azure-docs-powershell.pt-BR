---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubConfiguration.md
ms.openlocfilehash: 40fa5d382972c53de94187c9731748be5b1bfe2a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98260626"
---
# <span data-ttu-id="d2248-101">Set-AzIotHubConfiguration</span><span class="sxs-lookup"><span data-stu-id="d2248-101">Set-AzIotHubConfiguration</span></span>

## <span data-ttu-id="d2248-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d2248-102">SYNOPSIS</span></span>
<span data-ttu-id="d2248-103">Atualize os campos mutáveis do registro de configuração.</span><span class="sxs-lookup"><span data-stu-id="d2248-103">Update the mutable fields of the configuration registration.</span></span>

## <span data-ttu-id="d2248-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d2248-104">SYNTAX</span></span>

### <span data-ttu-id="d2248-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="d2248-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubConfiguration [-ResourceGroupName] <String> [-IotHubName] <String> [-Name] <String>
 [-Priority <Int32>] [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2248-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d2248-106">InputObjectSet</span></span>
```
Set-AzIotHubConfiguration [-InputObject] <PSIotHub> [-Name] <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2248-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="d2248-107">ResourceIdSet</span></span>
```
Set-AzIotHubConfiguration [-ResourceId] <String> [-Name] <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2248-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d2248-108">DESCRIPTION</span></span>
<span data-ttu-id="d2248-109">Atualize as propriedades especificadas de uma configuração de gerenciamento automático de dispositivos da IoT.</span><span class="sxs-lookup"><span data-stu-id="d2248-109">Update specified properties of an IoT automatic device management configuration.</span></span>
<span data-ttu-id="d2248-110">Observação: o conteúdo de configuração é imutável.</span><span class="sxs-lookup"><span data-stu-id="d2248-110">Note: Configuration content is immutable.</span></span> <span data-ttu-id="d2248-111">As propriedades de configuração que podem ser atualizadas são ' rótulos ', ' métricas ', ' prioridade ' e ' targetCondition '.</span><span class="sxs-lookup"><span data-stu-id="d2248-111">Configuration properties that can be updated are 'labels', 'metrics', 'priority' and 'targetCondition'.</span></span>
<span data-ttu-id="d2248-112">Consulte https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="d2248-112">See https://docs.microsoft.com/azure/iot-hub/iot-hub-automatic-device-management for more information.</span></span>

## <span data-ttu-id="d2248-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d2248-113">EXAMPLES</span></span>

### <span data-ttu-id="d2248-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d2248-114">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Priority 7 -TargetCondition "tags.building=3 and tags.environment='dev'"
```

<span data-ttu-id="d2248-115">Alterar a prioridade de uma configuração de dispositivo e atualizar sua condição de destino</span><span class="sxs-lookup"><span data-stu-id="d2248-115">Alter the priority of a device configuration and update its target condition</span></span>

### <span data-ttu-id="d2248-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d2248-116">Example 2</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Set-AzIotHubConfiguration -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "config1" -Label $labels -Metric $metrics
```

<span data-ttu-id="d2248-117">Atualizar as métricas e os rótulos de uma configuração de dispositivo</span><span class="sxs-lookup"><span data-stu-id="d2248-117">Update the metrics and labels of a device configuration</span></span>

## <span data-ttu-id="d2248-118">OS</span><span class="sxs-lookup"><span data-stu-id="d2248-118">PARAMETERS</span></span>

### <span data-ttu-id="d2248-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2248-119">-DefaultProfile</span></span>
<span data-ttu-id="d2248-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d2248-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2248-121">-Force</span><span class="sxs-lookup"><span data-stu-id="d2248-121">-Force</span></span>
<span data-ttu-id="d2248-122">Permite que o objeto de configuração seja substituído mesmo que tenha sido atualizado desde que tenha sido recuperado na última vez.</span><span class="sxs-lookup"><span data-stu-id="d2248-122">Allows configuration object to be replaced even if it was updated since it was retrieved last time.</span></span>

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

### <span data-ttu-id="d2248-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d2248-123">-InputObject</span></span>
<span data-ttu-id="d2248-124">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="d2248-124">IotHub object</span></span>

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

### <span data-ttu-id="d2248-125">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="d2248-125">-IotHubName</span></span>
<span data-ttu-id="d2248-126">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="d2248-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="d2248-127">-Rótulo</span><span class="sxs-lookup"><span data-stu-id="d2248-127">-Label</span></span>
<span data-ttu-id="d2248-128">Mapa de rótulos a serem aplicados à configuração de destino.</span><span class="sxs-lookup"><span data-stu-id="d2248-128">Map of labels to be applied to target configuration.</span></span>

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

### <span data-ttu-id="d2248-129">-Métrica</span><span class="sxs-lookup"><span data-stu-id="d2248-129">-Metric</span></span>
<span data-ttu-id="d2248-130">Coleção queries para definição de métricas de configuração.</span><span class="sxs-lookup"><span data-stu-id="d2248-130">Queries collection for configuration metrics definition.</span></span>

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

### <span data-ttu-id="d2248-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="d2248-131">-Name</span></span>
<span data-ttu-id="d2248-132">Identificador para a configuração.</span><span class="sxs-lookup"><span data-stu-id="d2248-132">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="d2248-133">-Priority</span><span class="sxs-lookup"><span data-stu-id="d2248-133">-Priority</span></span>
<span data-ttu-id="d2248-134">Peso da configuração do dispositivo em caso de regras concorrentes (WINS mais alto).</span><span class="sxs-lookup"><span data-stu-id="d2248-134">Weight of the device configuration in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="d2248-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2248-135">-ResourceGroupName</span></span>
<span data-ttu-id="d2248-136">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="d2248-136">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d2248-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d2248-137">-ResourceId</span></span>
<span data-ttu-id="d2248-138">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="d2248-138">IotHub Resource Id</span></span>

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

### <span data-ttu-id="d2248-139">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="d2248-139">-TargetCondition</span></span>
<span data-ttu-id="d2248-140">A condição de destino à qual a configuração do dispositivo se aplica.</span><span class="sxs-lookup"><span data-stu-id="d2248-140">Target condition in which a device configuration applies to.</span></span>

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

### <span data-ttu-id="d2248-141">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d2248-141">-Confirm</span></span>
<span data-ttu-id="d2248-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2248-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2248-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2248-143">-WhatIf</span></span>
<span data-ttu-id="d2248-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d2248-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2248-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d2248-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2248-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2248-146">CommonParameters</span></span>
<span data-ttu-id="d2248-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2248-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2248-148">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2248-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2248-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d2248-149">INPUTS</span></span>

### <span data-ttu-id="d2248-150">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="d2248-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="d2248-151">System. String</span><span class="sxs-lookup"><span data-stu-id="d2248-151">System.String</span></span>

## <span data-ttu-id="d2248-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d2248-152">OUTPUTS</span></span>

### <span data-ttu-id="d2248-153">Microsoft. Azure. Commands. Management. IotHub. Models. PSConfiguration</span><span class="sxs-lookup"><span data-stu-id="d2248-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfiguration</span></span>

## <span data-ttu-id="d2248-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d2248-154">NOTES</span></span>

## <span data-ttu-id="d2248-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d2248-155">RELATED LINKS</span></span>
