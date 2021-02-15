---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/set-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Set-AzIotHubDeployment.md
ms.openlocfilehash: 947eec246c5dac9543522ade583426246c731d3e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114300"
---
# <span data-ttu-id="a9577-101">Set-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="a9577-101">Set-AzIotHubDeployment</span></span>

## <span data-ttu-id="a9577-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a9577-102">SYNOPSIS</span></span>
<span data-ttu-id="a9577-103">Atualize os campos de mutável da implantação de Borda IoT.</span><span class="sxs-lookup"><span data-stu-id="a9577-103">Update the mutable fields of IoT Edge deployment.</span></span>

## <span data-ttu-id="a9577-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a9577-104">SYNTAX</span></span>

### <span data-ttu-id="a9577-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a9577-105">ResourceSet (Default)</span></span>
```
Set-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String> [-Priority <Int32>]
 [-TargetCondition <String>] [-Metric <Hashtable>] [-Label <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9577-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a9577-106">InputObjectSet</span></span>
```
Set-AzIotHubDeployment [-InputObject] <PSIotHub> -Name <String> [-Priority <Int32>] [-TargetCondition <String>]
 [-Metric <Hashtable>] [-Label <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9577-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a9577-107">ResourceIdSet</span></span>
```
Set-AzIotHubDeployment [-ResourceId] <String> -Name <String> [-Priority <Int32>] [-TargetCondition <String>]
 [-Metric <Hashtable>] [-Label <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9577-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="a9577-108">DESCRIPTION</span></span>
<span data-ttu-id="a9577-109">Atualize as propriedades especificadas de uma implantação de Borda IoT.</span><span class="sxs-lookup"><span data-stu-id="a9577-109">Update specified properties of an IoT Edge deployment.</span></span>
<span data-ttu-id="a9577-110">Observação: o conteúdo da configuração é imutável.</span><span class="sxs-lookup"><span data-stu-id="a9577-110">Note: Configuration content is immutable.</span></span> <span data-ttu-id="a9577-111">As propriedades de configuração que podem ser atualizadas são "rótulos", "métricas", "prioridade" e "targetCondition".</span><span class="sxs-lookup"><span data-stu-id="a9577-111">Configuration properties that can be updated are 'labels', 'metrics', 'priority' and 'targetCondition'.</span></span>
<span data-ttu-id="a9577-112">Confira https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring  mais informações.</span><span class="sxs-lookup"><span data-stu-id="a9577-112">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring  for more information.</span></span>

## <span data-ttu-id="a9577-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a9577-113">EXAMPLES</span></span>

### <span data-ttu-id="a9577-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a9577-114">Example 1</span></span>
```powershell
PS C:\> Set-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Priority 7 -TargetCondition "tags.building=3 and tags.environment='dev'"
```

<span data-ttu-id="a9577-115">Altere a prioridade da implantação do Edge IoT e atualize sua condição de destino.</span><span class="sxs-lookup"><span data-stu-id="a9577-115">Alter the priority of IoT Edge deployment and update its target condition.</span></span>

### <span data-ttu-id="a9577-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="a9577-116">Example 2</span></span>
```powershell
PS C:\> $labels = @{}
PS C:\> $labels.add("key0","value0")
PS C:\> $metrics = @{}
PS C:\> $metrics.add("query1", "select deviceId from devices where tags.location='US'")
PS C:\> Set-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1" -Label $labels -Metric $metrics
```

<span data-ttu-id="a9577-117">Atualize as métricas e rótulos da implantação de Borda IoT.</span><span class="sxs-lookup"><span data-stu-id="a9577-117">Update the metrics and labels of IoT Edge deployment.</span></span>

## <span data-ttu-id="a9577-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a9577-118">PARAMETERS</span></span>

### <span data-ttu-id="a9577-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9577-119">-DefaultProfile</span></span>
<span data-ttu-id="a9577-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a9577-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9577-121">-Forçar</span><span class="sxs-lookup"><span data-stu-id="a9577-121">-Force</span></span>
<span data-ttu-id="a9577-122">Permite que o objeto de implantação seja substituído mesmo se ele tiver sido atualizado desde que foi recuperado da última vez.</span><span class="sxs-lookup"><span data-stu-id="a9577-122">Allows deployment object to be replaced even if it was updated since it was retrieved last time.</span></span>

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

### <span data-ttu-id="a9577-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a9577-123">-InputObject</span></span>
<span data-ttu-id="a9577-124">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="a9577-124">IotHub object</span></span>

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

### <span data-ttu-id="a9577-125">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="a9577-125">-IotHubName</span></span>
<span data-ttu-id="a9577-126">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="a9577-126">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="a9577-127">-Rótulo</span><span class="sxs-lookup"><span data-stu-id="a9577-127">-Label</span></span>
<span data-ttu-id="a9577-128">Mapa de rótulos a serem aplicados à implantação de destino.</span><span class="sxs-lookup"><span data-stu-id="a9577-128">Map of labels to be applied to target deployment.</span></span>

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

### <span data-ttu-id="a9577-129">-Métrica</span><span class="sxs-lookup"><span data-stu-id="a9577-129">-Metric</span></span>
<span data-ttu-id="a9577-130">Conjunto de consultas para definição de métricas de implantação de borda IoT.</span><span class="sxs-lookup"><span data-stu-id="a9577-130">Queries collection for IoT Edge deployment metrics definition.</span></span>

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

### <span data-ttu-id="a9577-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="a9577-131">-Name</span></span>
<span data-ttu-id="a9577-132">Identificador da implantação.</span><span class="sxs-lookup"><span data-stu-id="a9577-132">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="a9577-133">-Prioridade</span><span class="sxs-lookup"><span data-stu-id="a9577-133">-Priority</span></span>
<span data-ttu-id="a9577-134">Peso da implantação em caso de regras concorrentes (maiores vitórias).</span><span class="sxs-lookup"><span data-stu-id="a9577-134">Weight of deployment in case of competing rules (highest wins).</span></span>

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

### <span data-ttu-id="a9577-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9577-135">-ResourceGroupName</span></span>
<span data-ttu-id="a9577-136">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="a9577-136">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a9577-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a9577-137">-ResourceId</span></span>
<span data-ttu-id="a9577-138">ID de Recurso do IotHub</span><span class="sxs-lookup"><span data-stu-id="a9577-138">IotHub Resource Id</span></span>

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

### <span data-ttu-id="a9577-139">-TargetCondition</span><span class="sxs-lookup"><span data-stu-id="a9577-139">-TargetCondition</span></span>
<span data-ttu-id="a9577-140">Condição de destino à qual uma implantação de borda se aplica.</span><span class="sxs-lookup"><span data-stu-id="a9577-140">Target condition in which an Edge deployment applies to.</span></span>

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

### <span data-ttu-id="a9577-141">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="a9577-141">-Confirm</span></span>
<span data-ttu-id="a9577-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9577-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9577-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9577-143">-WhatIf</span></span>
<span data-ttu-id="a9577-144">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="a9577-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9577-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a9577-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9577-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9577-146">CommonParameters</span></span>
<span data-ttu-id="a9577-147">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9577-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9577-148">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9577-148">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9577-149">Entradas</span><span class="sxs-lookup"><span data-stu-id="a9577-149">INPUTS</span></span>

### <span data-ttu-id="a9577-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="a9577-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="a9577-151">System.String</span><span class="sxs-lookup"><span data-stu-id="a9577-151">System.String</span></span>

## <span data-ttu-id="a9577-152">Saídas</span><span class="sxs-lookup"><span data-stu-id="a9577-152">OUTPUTS</span></span>

### <span data-ttu-id="a9577-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="a9577-153">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeployment</span></span>

## <span data-ttu-id="a9577-154">Notas</span><span class="sxs-lookup"><span data-stu-id="a9577-154">NOTES</span></span>

## <span data-ttu-id="a9577-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a9577-155">RELATED LINKS</span></span>
