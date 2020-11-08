---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubdeploymentmetricsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeploymentMetricsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubDeploymentMetricsQuery.md
ms.openlocfilehash: 570caa5d788fae000834a7f3a79230849daf372f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94114919"
---
# <span data-ttu-id="86287-101">Invoke-AzIotHubDeploymentMetricsQuery</span><span class="sxs-lookup"><span data-stu-id="86287-101">Invoke-AzIotHubDeploymentMetricsQuery</span></span>

## <span data-ttu-id="86287-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="86287-102">SYNOPSIS</span></span>
<span data-ttu-id="86287-103">Invocar uma consulta métrica de implantação de borda IoT.</span><span class="sxs-lookup"><span data-stu-id="86287-103">Invoke an IoT Edge deployment metric query.</span></span>

## <span data-ttu-id="86287-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="86287-104">SYNTAX</span></span>

### <span data-ttu-id="86287-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="86287-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubDeploymentMetricsQuery [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 -MetricName <String> [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86287-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="86287-106">InputObjectSet</span></span>
```
Invoke-AzIotHubDeploymentMetricsQuery [-InputObject] <PSIotHub> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="86287-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="86287-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubDeploymentMetricsQuery [-ResourceId] <String> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="86287-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="86287-108">DESCRIPTION</span></span>
<span data-ttu-id="86287-109">Avaliar um destino personalizado ou um sistema métrico definido em uma implantação de borda IoT.</span><span class="sxs-lookup"><span data-stu-id="86287-109">Evaluate a target custom or system metric defined in an IoT Edge deployment.</span></span>
<span data-ttu-id="86287-110">Há métricas de sistema predefinidas que são calculadas por Hub IOT e não podem ser personalizadas.</span><span class="sxs-lookup"><span data-stu-id="86287-110">There are pre-defined system metrics which are calculated by Iot Hub and cannot be customized.</span></span>
- <span data-ttu-id="86287-111">"Direcionado" mostra os dispositivos de borda IoT que correspondem à condição de direcionamento de implantação.</span><span class="sxs-lookup"><span data-stu-id="86287-111">"Targeted" shows the IoT Edge devices that match the deployment targeting condition.</span></span>
- <span data-ttu-id="86287-112">"Aplicado" mostra os dispositivos de borda IoT direcionados que não são direcionados a outra implantação de prioridade mais alta.</span><span class="sxs-lookup"><span data-stu-id="86287-112">"Applied" shows the targeted IoT Edge devices that are not targeted by another deployment of higher priority.</span></span>
- <span data-ttu-id="86287-113">"Relatório de sucesso" mostra os dispositivos de borda IoT que relataram que os módulos foram implantados com êxito.</span><span class="sxs-lookup"><span data-stu-id="86287-113">"Reporting Success" shows the IoT Edge devices that have reported that the modules have been deployed successfully.</span></span>
- <span data-ttu-id="86287-114">"Falha no relatório" mostra os dispositivos de borda IoT que relataram que um ou mais módulos não foram implantados com êxito.</span><span class="sxs-lookup"><span data-stu-id="86287-114">"Reporting Failure" shows the IoT Edge devices that have reported that one or more modules haven't been deployed successfully.</span></span> 
  <span data-ttu-id="86287-115">Para investigar ainda mais o erro, conecte-se remotamente a esses dispositivos e veja os arquivos de log.</span><span class="sxs-lookup"><span data-stu-id="86287-115">To further investigate the error, connect remotely to those devices and view the log files.</span></span>

## <span data-ttu-id="86287-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="86287-116">EXAMPLES</span></span>

### <span data-ttu-id="86287-117">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="86287-117">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubDeploymentMetricsQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myDeploy1" -MetricName "warningLimit"
```

<span data-ttu-id="86287-118">Avaliar a métrica ' warningLimit ' definida como personalizada.</span><span class="sxs-lookup"><span data-stu-id="86287-118">Evaluate the custom defined 'warningLimit' metric.</span></span>

### <span data-ttu-id="86287-119">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="86287-119">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubDeployMetric -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myDeploy1" -MetricName "Reporting Success" -MetricType "system"
```

<span data-ttu-id="86287-120">Avaliar a métrica do sistema ' êxito no relatório '.</span><span class="sxs-lookup"><span data-stu-id="86287-120">Evaluate the system 'Reporting Success' metric.</span></span>

## <span data-ttu-id="86287-121">OS</span><span class="sxs-lookup"><span data-stu-id="86287-121">PARAMETERS</span></span>

### <span data-ttu-id="86287-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86287-122">-DefaultProfile</span></span>
<span data-ttu-id="86287-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="86287-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86287-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="86287-124">-InputObject</span></span>
<span data-ttu-id="86287-125">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="86287-125">IotHub object</span></span>

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

### <span data-ttu-id="86287-126">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="86287-126">-IotHubName</span></span>
<span data-ttu-id="86287-127">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="86287-127">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="86287-128">-Metricname</span><span class="sxs-lookup"><span data-stu-id="86287-128">-MetricName</span></span>
<span data-ttu-id="86287-129">Métrica de destino para avaliação.</span><span class="sxs-lookup"><span data-stu-id="86287-129">Target metric for evaluation.</span></span>

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

### <span data-ttu-id="86287-130">-Metrictype</span><span class="sxs-lookup"><span data-stu-id="86287-130">-MetricType</span></span>
<span data-ttu-id="86287-131">Indica qual coleção métrica deve ser usada para pesquisar uma métrica.</span><span class="sxs-lookup"><span data-stu-id="86287-131">Indicates which metric collection should be used to lookup a metric.</span></span>

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

### <span data-ttu-id="86287-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="86287-132">-Name</span></span>
<span data-ttu-id="86287-133">Identificador para a implantação.</span><span class="sxs-lookup"><span data-stu-id="86287-133">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="86287-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86287-134">-ResourceGroupName</span></span>
<span data-ttu-id="86287-135">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="86287-135">Name of the Resource Group</span></span>

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

### <span data-ttu-id="86287-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="86287-136">-ResourceId</span></span>
<span data-ttu-id="86287-137">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="86287-137">IotHub Resource Id</span></span>

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

### <span data-ttu-id="86287-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="86287-138">-Confirm</span></span>
<span data-ttu-id="86287-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86287-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86287-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86287-140">-WhatIf</span></span>
<span data-ttu-id="86287-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="86287-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86287-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="86287-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86287-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86287-143">CommonParameters</span></span>
<span data-ttu-id="86287-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86287-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86287-145">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86287-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86287-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="86287-146">INPUTS</span></span>

### <span data-ttu-id="86287-147">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="86287-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="86287-148">System. String</span><span class="sxs-lookup"><span data-stu-id="86287-148">System.String</span></span>

## <span data-ttu-id="86287-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="86287-149">OUTPUTS</span></span>

### <span data-ttu-id="86287-150">Microsoft. Azure. Commands. Management. IotHub. Models. PSConfigurationMetricsResult</span><span class="sxs-lookup"><span data-stu-id="86287-150">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurationMetricsResult</span></span>

## <span data-ttu-id="86287-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="86287-151">NOTES</span></span>

## <span data-ttu-id="86287-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="86287-152">RELATED LINKS</span></span>
