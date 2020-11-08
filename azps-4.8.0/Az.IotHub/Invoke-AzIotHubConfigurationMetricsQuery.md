---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubconfigurationmetricsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubConfigurationMetricsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubConfigurationMetricsQuery.md
ms.openlocfilehash: 85793ba3097297de646db4695cac36173bb01673
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111960"
---
# <span data-ttu-id="8ebfd-101">Invoke-AzIotHubConfigurationMetricsQuery</span><span class="sxs-lookup"><span data-stu-id="8ebfd-101">Invoke-AzIotHubConfigurationMetricsQuery</span></span>

## <span data-ttu-id="8ebfd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8ebfd-102">SYNOPSIS</span></span>
<span data-ttu-id="8ebfd-103">Chame uma consulta métrica de configuração de dispositivo IoT.</span><span class="sxs-lookup"><span data-stu-id="8ebfd-103">Invoke an IoT device configuration metric query.</span></span>

## <span data-ttu-id="8ebfd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8ebfd-104">SYNTAX</span></span>

### <span data-ttu-id="8ebfd-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="8ebfd-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubConfigurationMetricsQuery [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 -MetricName <String> [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ebfd-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8ebfd-106">InputObjectSet</span></span>
```
Invoke-AzIotHubConfigurationMetricsQuery [-InputObject] <PSIotHub> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8ebfd-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="8ebfd-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubConfigurationMetricsQuery [-ResourceId] <String> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8ebfd-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8ebfd-108">DESCRIPTION</span></span>
<span data-ttu-id="8ebfd-109">Avaliar um destino personalizado ou um sistema métrico definido em uma configuração de dispositivo IoT.</span><span class="sxs-lookup"><span data-stu-id="8ebfd-109">Evaluate a target custom or system metric defined in an IoT device configuration.</span></span>
<span data-ttu-id="8ebfd-110">Há métricas de sistema predefinidas que são calculadas por Hub IOT e não podem ser personalizadas.</span><span class="sxs-lookup"><span data-stu-id="8ebfd-110">There are pre-defined system metrics which are calculated by Iot Hub and cannot be customized.</span></span>
- <span data-ttu-id="8ebfd-111">"Direcionado" especifica o número de Twins de dispositivo que correspondem à condição de destino.</span><span class="sxs-lookup"><span data-stu-id="8ebfd-111">"Targeted" specifies the number of device twins that match the target condition.</span></span>
- <span data-ttu-id="8ebfd-112">"Aplicado" especificou o número de Twins de dispositivo que foram modificadas pela configuração.</span><span class="sxs-lookup"><span data-stu-id="8ebfd-112">"Applied" specified the number of device twins that have been modified by the configuration.</span></span> 

## <span data-ttu-id="8ebfd-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8ebfd-113">EXAMPLES</span></span>

### <span data-ttu-id="8ebfd-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8ebfd-114">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubConfigurationMetricsQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myConfig1" -MetricName "warningLimit"
```

<span data-ttu-id="8ebfd-115">Avaliar a métrica ' warningLimit ' definida como personalizada.</span><span class="sxs-lookup"><span data-stu-id="8ebfd-115">Evaluate the custom defined 'warningLimit' metric.</span></span>

### <span data-ttu-id="8ebfd-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="8ebfd-116">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubConfigMetric -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myConfig1" -MetricName "applied" -MetricType "system"
```

<span data-ttu-id="8ebfd-117">Avalie a métrica do sistema ' aplicado '.</span><span class="sxs-lookup"><span data-stu-id="8ebfd-117">Evaluate the system 'applied' metric.</span></span>

## <span data-ttu-id="8ebfd-118">OS</span><span class="sxs-lookup"><span data-stu-id="8ebfd-118">PARAMETERS</span></span>

### <span data-ttu-id="8ebfd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ebfd-119">-DefaultProfile</span></span>
<span data-ttu-id="8ebfd-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8ebfd-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ebfd-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8ebfd-121">-InputObject</span></span>
<span data-ttu-id="8ebfd-122">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="8ebfd-122">IotHub object</span></span>

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

### <span data-ttu-id="8ebfd-123">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="8ebfd-123">-IotHubName</span></span>
<span data-ttu-id="8ebfd-124">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="8ebfd-124">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="8ebfd-125">-Metricname</span><span class="sxs-lookup"><span data-stu-id="8ebfd-125">-MetricName</span></span>
<span data-ttu-id="8ebfd-126">Métrica de destino para avaliação.</span><span class="sxs-lookup"><span data-stu-id="8ebfd-126">Target metric for evaluation.</span></span>

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

### <span data-ttu-id="8ebfd-127">-Metrictype</span><span class="sxs-lookup"><span data-stu-id="8ebfd-127">-MetricType</span></span>
<span data-ttu-id="8ebfd-128">Indica qual coleção métrica deve ser usada para pesquisar uma métrica.</span><span class="sxs-lookup"><span data-stu-id="8ebfd-128">Indicates which metric collection should be used to lookup a metric.</span></span>

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

### <span data-ttu-id="8ebfd-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="8ebfd-129">-Name</span></span>
<span data-ttu-id="8ebfd-130">Identificador para a configuração.</span><span class="sxs-lookup"><span data-stu-id="8ebfd-130">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="8ebfd-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ebfd-131">-ResourceGroupName</span></span>
<span data-ttu-id="8ebfd-132">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="8ebfd-132">Name of the Resource Group</span></span>

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

### <span data-ttu-id="8ebfd-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8ebfd-133">-ResourceId</span></span>
<span data-ttu-id="8ebfd-134">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="8ebfd-134">IotHub Resource Id</span></span>

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

### <span data-ttu-id="8ebfd-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8ebfd-135">-Confirm</span></span>
<span data-ttu-id="8ebfd-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ebfd-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ebfd-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ebfd-137">-WhatIf</span></span>
<span data-ttu-id="8ebfd-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8ebfd-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ebfd-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8ebfd-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ebfd-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ebfd-140">CommonParameters</span></span>
<span data-ttu-id="8ebfd-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ebfd-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ebfd-142">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ebfd-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ebfd-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8ebfd-143">INPUTS</span></span>

### <span data-ttu-id="8ebfd-144">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="8ebfd-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="8ebfd-145">System. String</span><span class="sxs-lookup"><span data-stu-id="8ebfd-145">System.String</span></span>

## <span data-ttu-id="8ebfd-146">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8ebfd-146">OUTPUTS</span></span>

### <span data-ttu-id="8ebfd-147">Microsoft. Azure. Commands. Management. IotHub. Models. PSConfigurationMetricsResult</span><span class="sxs-lookup"><span data-stu-id="8ebfd-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurationMetricsResult</span></span>

## <span data-ttu-id="8ebfd-148">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8ebfd-148">NOTES</span></span>

## <span data-ttu-id="8ebfd-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8ebfd-149">RELATED LINKS</span></span>
