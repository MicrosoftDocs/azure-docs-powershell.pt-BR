---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeployment.md
ms.openlocfilehash: 947eec246c5dac9543522ade583426246c731d3e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98272802"
---
# <span data-ttu-id="588ef-101">Set-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="588ef-101">Set-AzIotHubDeployment</span></span>

## <span data-ttu-id="588ef-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="588ef-102">SYNOPSIS</span></span>
<span data-ttu-id="588ef-103">Atualize os campos mutáveis da implantação do IoT Edge.</span><span class="sxs-lookup"><span data-stu-id="588ef-103">Update the mutable fields of IoT Edge deployment.</span></span>

## <span data-ttu-id="588ef-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="588ef-104">SYNTAX</span></span>

### <span data-ttu-id="588ef-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="588ef-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="588ef-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="588ef-106">InputObjectSet</span></span>
```
Set-AzIotHubDeployment [-InputObject] <PSIotHub> -Name <String> [-Priority <Int32>] [-TargetCondition <String>]
 [-Metric <Hashtable>] [-Label <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="588ef-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="588ef-107">ResourceIdSet</span></span>
```
Set-AzIotHubDeployment [-ResourceId] <String> -Name <String> [-Priority <Int32>] [-TargetCondition <String>]
 [-Metric <Hashtable>] [-Label <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="588ef-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="588ef-108">DESCRIPTION</span></span>
<span data-ttu-id="588ef-109">Atualize as propriedades especificadas de uma implantação de borda IoT.</span><span class="sxs-lookup"><span data-stu-id="588ef-109">Update specified properties of an IoT Edge deployment.</span></span>
<span data-ttu-id="588ef-110">Observação: o conteúdo de configuração é imutável.</span><span class="sxs-lookup"><span data-stu-id="588ef-110">Note: Configuration content is immutable.</span></span> <span data-ttu-id="588ef-111">As propriedades de configuração que podem ser atualizadas são ' rótulos ', ' métricas ', ' prioridade ' e ' targetCondition '.</span><span class="sxs-lookup"><span data-stu-id="588ef-111">Configuration properties that can be updated are 'labels', 'metrics', 'priority' and 'targetCondition'.</span></span>
<span data-ttu-id="588ef-112">Consulte https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring  para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="588ef-112">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring  for more information.</span></span>

## <span data-ttu-id="588ef-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="588ef-113">EXAMPLES</span></span>

### <span data-ttu-id="588ef-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="588ef-114">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Priority 7 -TargetCondition "tags.building=3 and tags.environment='dev'"
```

<span data-ttu-id="588ef-115">Altere a prioridade da implantação de borda IoT e atualize sua condição de destino.</span><span class="sxs-lookup"><span data-stu-id="588ef-115">Alter the priority of IoT Edge deployment and update its target condition.</span></span>

### <span data-ttu-id="588ef-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="588ef-116">Example 2</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Set-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Label $labels -Metric $metrics
```

<span data-ttu-id="588ef-117">Atualize as métricas e os rótulos da implantação de borda IoT.</span><span class="sxs-lookup"><span data-stu-id="588ef-117">Update the metrics and labels of IoT Edge deployment.</span></span>

## <span data-ttu-id="588ef-118">OS</span><span class="sxs-lookup"><span data-stu-id="588ef-118">PARAMETERS</span></span>

### <span data-ttu-id="588ef-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="588ef-119">-DefaultProfile</span></span>
<span data-ttu-id="588ef-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="588ef-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="588ef-121">-Force</span><span class="sxs-lookup"><span data-stu-id="588ef-121">-Force</span></span>
<span data-ttu-id="588ef-122">Permite que o objeto de implantação seja substituído mesmo se ele tiver sido atualizado desde a última vez que foi recuperado.</span><span class="sxs-lookup"><span data-stu-id="588ef-122">Allows deployment object to be replaced even if it was updated since it was retrieved last time.</span></span>

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

### <span data-ttu-id="588ef-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="588ef-123">-InputObject</span></span>
<span data-ttu-id="588ef-124">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="588ef-124">IotHub object</span></span>

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

### <span data-ttu-id="588ef-125">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="588ef-125">-IotHubName</span></span>
<span data-ttu-id="588ef-126">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="588ef-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="588ef-127">-Rótulo</span><span class="sxs-lookup"><span data-stu-id="588ef-127">-Label</span></span>
<span data-ttu-id="588ef-128">Mapa de rótulos a serem aplicados à implantação de destino.</span><span class="sxs-lookup"><span data-stu-id="588ef-128">Map of labels to be applied to target deployment.</span></span>

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

### <span data-ttu-id="588ef-129">-Métrica</span><span class="sxs-lookup"><span data-stu-id="588ef-129">-Metric</span></span>
<span data-ttu-id="588ef-130">Coleção queries para definição de métricas de implantação de borda IoT.</span><span class="sxs-lookup"><span data-stu-id="588ef-130">Queries collection for IoT Edge deployment metrics definition.</span></span>

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

### <span data-ttu-id="588ef-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="588ef-131">-Name</span></span>
<span data-ttu-id="588ef-132">Identificador para a implantação.</span><span class="sxs-lookup"><span data-stu-id="588ef-132">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="588ef-133">-Priority</span><span class="sxs-lookup"><span data-stu-id="588ef-133">-Priority</span></span>
<span data-ttu-id="588ef-134">Peso da implantação em caso de regras concorrentes (WINS mais alto).</span><span class="sxs-lookup"><span data-stu-id="588ef-134">Weight of deployment in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="588ef-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="588ef-135">-ResourceGroupName</span></span>
<span data-ttu-id="588ef-136">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="588ef-136">Name of the Resource Group</span></span>

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

### <span data-ttu-id="588ef-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="588ef-137">-ResourceId</span></span>
<span data-ttu-id="588ef-138">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="588ef-138">IotHub Resource Id</span></span>

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

### <span data-ttu-id="588ef-139">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="588ef-139">-TargetCondition</span></span>
<span data-ttu-id="588ef-140">A condição de destino à qual a implantação de borda se aplica.</span><span class="sxs-lookup"><span data-stu-id="588ef-140">Target condition in which an Edge deployment applies to.</span></span>

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

### <span data-ttu-id="588ef-141">-Confirme</span><span class="sxs-lookup"><span data-stu-id="588ef-141">-Confirm</span></span>
<span data-ttu-id="588ef-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="588ef-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="588ef-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="588ef-143">-WhatIf</span></span>
<span data-ttu-id="588ef-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="588ef-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="588ef-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="588ef-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="588ef-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="588ef-146">CommonParameters</span></span>
<span data-ttu-id="588ef-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="588ef-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="588ef-148">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="588ef-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="588ef-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="588ef-149">INPUTS</span></span>

### <span data-ttu-id="588ef-150">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="588ef-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="588ef-151">System. String</span><span class="sxs-lookup"><span data-stu-id="588ef-151">System.String</span></span>

## <span data-ttu-id="588ef-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="588ef-152">OUTPUTS</span></span>

### <span data-ttu-id="588ef-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSDEployment</span><span class="sxs-lookup"><span data-stu-id="588ef-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span></span>

## <span data-ttu-id="588ef-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="588ef-154">NOTES</span></span>

## <span data-ttu-id="588ef-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="588ef-155">RELATED LINKS</span></span>
