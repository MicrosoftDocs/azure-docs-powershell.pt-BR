---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/invoke-aziothubdeploymentmetricsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeploymentMetricsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeploymentMetricsQuery.md
ms.openlocfilehash: 02870d2bf0016704328e157b948b9db8ae1207f4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886758"
---
# <span data-ttu-id="b56e9-101">Invoke-AzIotHubDeploymentMetricsQuery</span><span class="sxs-lookup"><span data-stu-id="b56e9-101">Invoke-AzIotHubDeploymentMetricsQuery</span></span>

## <span data-ttu-id="b56e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b56e9-102">SYNOPSIS</span></span>
<span data-ttu-id="b56e9-103">Invocar uma consulta métrica de implantação de Borda de IoT.</span><span class="sxs-lookup"><span data-stu-id="b56e9-103">Invoke an IoT Edge deployment metric query.</span></span>

## <span data-ttu-id="b56e9-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="b56e9-104">SYNTAX</span></span>

### <span data-ttu-id="b56e9-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b56e9-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubDeploymentMetricsQuery [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 -MetricName <String> [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b56e9-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b56e9-106">InputObjectSet</span></span>
```
Invoke-AzIotHubDeploymentMetricsQuery [-InputObject] <PSIotHub> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b56e9-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b56e9-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubDeploymentMetricsQuery [-ResourceId] <String> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b56e9-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="b56e9-108">DESCRIPTION</span></span>
<span data-ttu-id="b56e9-109">Avalie uma métrica personalizada de destino ou sistema definida em uma implantação de Borda IoT.</span><span class="sxs-lookup"><span data-stu-id="b56e9-109">Evaluate a target custom or system metric defined in an IoT Edge deployment.</span></span>
<span data-ttu-id="b56e9-110">Há métricas de sistema pré-definidas que são calculadas pelo Hub de Iot e não podem ser personalizadas.</span><span class="sxs-lookup"><span data-stu-id="b56e9-110">There are pre-defined system metrics which are calculated by Iot Hub and cannot be customized.</span></span>
- <span data-ttu-id="b56e9-111">"Direcionado" mostra os dispositivos de Borda de IoT que corresponderem à condição de direcionamento de implantação.</span><span class="sxs-lookup"><span data-stu-id="b56e9-111">"Targeted" shows the IoT Edge devices that match the deployment targeting condition.</span></span>
- <span data-ttu-id="b56e9-112">"Aplicado" mostra os dispositivos de Borda de IoT direcionados que não são direcionados por outra implantação de prioridade mais alta.</span><span class="sxs-lookup"><span data-stu-id="b56e9-112">"Applied" shows the targeted IoT Edge devices that are not targeted by another deployment of higher priority.</span></span>
- <span data-ttu-id="b56e9-113">"Sucesso do Relatório" mostra os dispositivos de Borda de IoT que relataram que os módulos foram implantados com êxito.</span><span class="sxs-lookup"><span data-stu-id="b56e9-113">"Reporting Success" shows the IoT Edge devices that have reported that the modules have been deployed successfully.</span></span>
- <span data-ttu-id="b56e9-114">"Falha de Relatório" mostra os dispositivos de Borda de IoT que relataram que um ou mais módulos não foram implantados com êxito.</span><span class="sxs-lookup"><span data-stu-id="b56e9-114">"Reporting Failure" shows the IoT Edge devices that have reported that one or more modules haven't been deployed successfully.</span></span> 
  <span data-ttu-id="b56e9-115">Para investigar ainda mais o erro, conecte-se remotamente a esses dispositivos e veja os arquivos de log.</span><span class="sxs-lookup"><span data-stu-id="b56e9-115">To further investigate the error, connect remotely to those devices and view the log files.</span></span>

## <span data-ttu-id="b56e9-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b56e9-116">EXAMPLES</span></span>

### <span data-ttu-id="b56e9-117">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b56e9-117">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubDeploymentMetricsQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myDeploy1" -MetricName "warningLimit"
```

<span data-ttu-id="b56e9-118">Avalie a métrica "warningLimit" definida personalizada.</span><span class="sxs-lookup"><span data-stu-id="b56e9-118">Evaluate the custom defined 'warningLimit' metric.</span></span>

### <span data-ttu-id="b56e9-119">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="b56e9-119">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubDeployMetric -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myDeploy1" -MetricName "Reporting Success" -MetricType "system"
```

<span data-ttu-id="b56e9-120">Avalie a métrica do sistema 'Reporting Success'.</span><span class="sxs-lookup"><span data-stu-id="b56e9-120">Evaluate the system 'Reporting Success' metric.</span></span>

## <span data-ttu-id="b56e9-121">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="b56e9-121">PARAMETERS</span></span>

### <span data-ttu-id="b56e9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b56e9-122">-DefaultProfile</span></span>
<span data-ttu-id="b56e9-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b56e9-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b56e9-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b56e9-124">-InputObject</span></span>
<span data-ttu-id="b56e9-125">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="b56e9-125">IotHub object</span></span>

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

### <span data-ttu-id="b56e9-126">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="b56e9-126">-IotHubName</span></span>
<span data-ttu-id="b56e9-127">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="b56e9-127">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="b56e9-128">-MetricName</span><span class="sxs-lookup"><span data-stu-id="b56e9-128">-MetricName</span></span>
<span data-ttu-id="b56e9-129">Métrica de destino para avaliação.</span><span class="sxs-lookup"><span data-stu-id="b56e9-129">Target metric for evaluation.</span></span>

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

### <span data-ttu-id="b56e9-130">-MetricType</span><span class="sxs-lookup"><span data-stu-id="b56e9-130">-MetricType</span></span>
<span data-ttu-id="b56e9-131">Indica qual coleção métrica deve ser usada para procurar uma métrica.</span><span class="sxs-lookup"><span data-stu-id="b56e9-131">Indicates which metric collection should be used to lookup a metric.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurationMetricType
Parameter Sets: (All)
Aliases:
Accepted values: Custom, System

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b56e9-132">-Name</span><span class="sxs-lookup"><span data-stu-id="b56e9-132">-Name</span></span>
<span data-ttu-id="b56e9-133">Identificador da implantação.</span><span class="sxs-lookup"><span data-stu-id="b56e9-133">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="b56e9-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b56e9-134">-ResourceGroupName</span></span>
<span data-ttu-id="b56e9-135">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="b56e9-135">Name of the Resource Group</span></span>

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

### <span data-ttu-id="b56e9-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b56e9-136">-ResourceId</span></span>
<span data-ttu-id="b56e9-137">Id de Recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="b56e9-137">IotHub Resource Id</span></span>

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

### <span data-ttu-id="b56e9-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b56e9-138">-Confirm</span></span>
<span data-ttu-id="b56e9-139">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b56e9-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b56e9-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b56e9-140">-WhatIf</span></span>
<span data-ttu-id="b56e9-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b56e9-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b56e9-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b56e9-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b56e9-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b56e9-143">CommonParameters</span></span>
<span data-ttu-id="b56e9-144">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b56e9-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b56e9-145">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b56e9-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b56e9-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b56e9-146">INPUTS</span></span>

### <span data-ttu-id="b56e9-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="b56e9-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="b56e9-148">System.String</span><span class="sxs-lookup"><span data-stu-id="b56e9-148">System.String</span></span>

## <span data-ttu-id="b56e9-149">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="b56e9-149">OUTPUTS</span></span>

### <span data-ttu-id="b56e9-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurationMetricsResult</span><span class="sxs-lookup"><span data-stu-id="b56e9-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurationMetricsResult</span></span>

## <span data-ttu-id="b56e9-151">NOTES</span><span class="sxs-lookup"><span data-stu-id="b56e9-151">NOTES</span></span>

## <span data-ttu-id="b56e9-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b56e9-152">RELATED LINKS</span></span>
