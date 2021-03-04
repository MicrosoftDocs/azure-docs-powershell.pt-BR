---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/set-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeployment.md
ms.openlocfilehash: 5a0c56a946e9f81163a94a092e646acbc99fb6cd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885904"
---
# <span data-ttu-id="56c20-101">Set-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="56c20-101">Set-AzIotHubDeployment</span></span>

## <span data-ttu-id="56c20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56c20-102">SYNOPSIS</span></span>
<span data-ttu-id="56c20-103">Atualize os campos de mutáveis da implantação de Borda de IoT.</span><span class="sxs-lookup"><span data-stu-id="56c20-103">Update the mutable fields of IoT Edge deployment.</span></span>

## <span data-ttu-id="56c20-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="56c20-104">SYNTAX</span></span>

### <span data-ttu-id="56c20-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="56c20-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56c20-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="56c20-106">InputObjectSet</span></span>
```
Set-AzIotHubDeployment [-InputObject] <PSIotHub> -Name <String> [-Priority <Int32>] [-TargetCondition <String>]
 [-Metric <Hashtable>] [-Label <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56c20-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="56c20-107">ResourceIdSet</span></span>
```
Set-AzIotHubDeployment [-ResourceId] <String> -Name <String> [-Priority <Int32>] [-TargetCondition <String>]
 [-Metric <Hashtable>] [-Label <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56c20-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="56c20-108">DESCRIPTION</span></span>
<span data-ttu-id="56c20-109">Atualizar propriedades especificadas de uma implantação de Borda de IoT.</span><span class="sxs-lookup"><span data-stu-id="56c20-109">Update specified properties of an IoT Edge deployment.</span></span>
<span data-ttu-id="56c20-110">Observação: o conteúdo da configuração é imutável.</span><span class="sxs-lookup"><span data-stu-id="56c20-110">Note: Configuration content is immutable.</span></span> <span data-ttu-id="56c20-111">As propriedades de configuração que podem ser atualizadas são 'labels', 'metrics', 'priority' e 'targetCondition'.</span><span class="sxs-lookup"><span data-stu-id="56c20-111">Configuration properties that can be updated are 'labels', 'metrics', 'priority' and 'targetCondition'.</span></span>
<span data-ttu-id="56c20-112">Confira https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring  mais informações.</span><span class="sxs-lookup"><span data-stu-id="56c20-112">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring  for more information.</span></span>

## <span data-ttu-id="56c20-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="56c20-113">EXAMPLES</span></span>

### <span data-ttu-id="56c20-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="56c20-114">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Priority 7 -TargetCondition "tags.building=3 and tags.environment='dev'"
```

<span data-ttu-id="56c20-115">Altere a prioridade da implantação de Borda de IoT e atualize sua condição de destino.</span><span class="sxs-lookup"><span data-stu-id="56c20-115">Alter the priority of IoT Edge deployment and update its target condition.</span></span>

### <span data-ttu-id="56c20-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="56c20-116">Example 2</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Set-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Label $labels -Metric $metrics
```

<span data-ttu-id="56c20-117">Atualize as métricas e os rótulos da implantação de Borda de IoT.</span><span class="sxs-lookup"><span data-stu-id="56c20-117">Update the metrics and labels of IoT Edge deployment.</span></span>

## <span data-ttu-id="56c20-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="56c20-118">PARAMETERS</span></span>

### <span data-ttu-id="56c20-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56c20-119">-DefaultProfile</span></span>
<span data-ttu-id="56c20-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="56c20-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56c20-121">-Force</span><span class="sxs-lookup"><span data-stu-id="56c20-121">-Force</span></span>
<span data-ttu-id="56c20-122">Permite que o objeto de implantação seja substituído mesmo que ele foi atualizado desde que foi recuperado da última vez.</span><span class="sxs-lookup"><span data-stu-id="56c20-122">Allows deployment object to be replaced even if it was updated since it was retrieved last time.</span></span>

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

### <span data-ttu-id="56c20-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="56c20-123">-InputObject</span></span>
<span data-ttu-id="56c20-124">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="56c20-124">IotHub object</span></span>

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

### <span data-ttu-id="56c20-125">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="56c20-125">-IotHubName</span></span>
<span data-ttu-id="56c20-126">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="56c20-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="56c20-127">-Label</span><span class="sxs-lookup"><span data-stu-id="56c20-127">-Label</span></span>
<span data-ttu-id="56c20-128">Mapa de rótulos a serem aplicados à implantação de destino.</span><span class="sxs-lookup"><span data-stu-id="56c20-128">Map of labels to be applied to target deployment.</span></span>

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

### <span data-ttu-id="56c20-129">-Metric</span><span class="sxs-lookup"><span data-stu-id="56c20-129">-Metric</span></span>
<span data-ttu-id="56c20-130">Coleção Consultas para definição de métricas de implantação de Borda de IoT.</span><span class="sxs-lookup"><span data-stu-id="56c20-130">Queries collection for IoT Edge deployment metrics definition.</span></span>

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

### <span data-ttu-id="56c20-131">-Name</span><span class="sxs-lookup"><span data-stu-id="56c20-131">-Name</span></span>
<span data-ttu-id="56c20-132">Identificador da implantação.</span><span class="sxs-lookup"><span data-stu-id="56c20-132">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="56c20-133">-Priority</span><span class="sxs-lookup"><span data-stu-id="56c20-133">-Priority</span></span>
<span data-ttu-id="56c20-134">Peso da implantação em caso de regras concorrentes (maiores ganhos).</span><span class="sxs-lookup"><span data-stu-id="56c20-134">Weight of deployment in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="56c20-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56c20-135">-ResourceGroupName</span></span>
<span data-ttu-id="56c20-136">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="56c20-136">Name of the Resource Group</span></span>

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

### <span data-ttu-id="56c20-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="56c20-137">-ResourceId</span></span>
<span data-ttu-id="56c20-138">Id de Recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="56c20-138">IotHub Resource Id</span></span>

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

### <span data-ttu-id="56c20-139">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="56c20-139">-TargetCondition</span></span>
<span data-ttu-id="56c20-140">Condição de destino na qual uma implantação de Borda se aplica.</span><span class="sxs-lookup"><span data-stu-id="56c20-140">Target condition in which an Edge deployment applies to.</span></span>

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

### <span data-ttu-id="56c20-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="56c20-141">-Confirm</span></span>
<span data-ttu-id="56c20-142">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56c20-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56c20-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56c20-143">-WhatIf</span></span>
<span data-ttu-id="56c20-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="56c20-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56c20-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="56c20-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56c20-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56c20-146">CommonParameters</span></span>
<span data-ttu-id="56c20-147">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56c20-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56c20-148">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56c20-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56c20-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="56c20-149">INPUTS</span></span>

### <span data-ttu-id="56c20-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="56c20-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="56c20-151">System.String</span><span class="sxs-lookup"><span data-stu-id="56c20-151">System.String</span></span>

## <span data-ttu-id="56c20-152">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="56c20-152">OUTPUTS</span></span>

### <span data-ttu-id="56c20-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="56c20-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span></span>

## <span data-ttu-id="56c20-154">NOTES</span><span class="sxs-lookup"><span data-stu-id="56c20-154">NOTES</span></span>

## <span data-ttu-id="56c20-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="56c20-155">RELATED LINKS</span></span>
