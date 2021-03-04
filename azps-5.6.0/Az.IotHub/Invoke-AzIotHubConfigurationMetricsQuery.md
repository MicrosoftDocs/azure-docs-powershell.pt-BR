---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/invoke-aziothubconfigurationmetricsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubConfigurationMetricsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubConfigurationMetricsQuery.md
ms.openlocfilehash: 07772e7d0cbec3a2cd8241de3afa0100e1c253cc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886760"
---
# <span data-ttu-id="3a3ac-101">Invoke-AzIotHubConfigurationMetricsQuery</span><span class="sxs-lookup"><span data-stu-id="3a3ac-101">Invoke-AzIotHubConfigurationMetricsQuery</span></span>

## <span data-ttu-id="3a3ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a3ac-102">SYNOPSIS</span></span>
<span data-ttu-id="3a3ac-103">Invocar uma consulta métrica de configuração de dispositivo IoT.</span><span class="sxs-lookup"><span data-stu-id="3a3ac-103">Invoke an IoT device configuration metric query.</span></span>

## <span data-ttu-id="3a3ac-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="3a3ac-104">SYNTAX</span></span>

### <span data-ttu-id="3a3ac-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="3a3ac-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubConfigurationMetricsQuery [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 -MetricName <String> [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a3ac-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3a3ac-106">InputObjectSet</span></span>
```
Invoke-AzIotHubConfigurationMetricsQuery [-InputObject] <PSIotHub> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3a3ac-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="3a3ac-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubConfigurationMetricsQuery [-ResourceId] <String> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3a3ac-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="3a3ac-108">DESCRIPTION</span></span>
<span data-ttu-id="3a3ac-109">Avalie uma métrica personalizada de destino ou sistema definida em uma configuração de dispositivo IoT.</span><span class="sxs-lookup"><span data-stu-id="3a3ac-109">Evaluate a target custom or system metric defined in an IoT device configuration.</span></span>
<span data-ttu-id="3a3ac-110">Há métricas de sistema pré-definidas que são calculadas pelo Hub de Iot e não podem ser personalizadas.</span><span class="sxs-lookup"><span data-stu-id="3a3ac-110">There are pre-defined system metrics which are calculated by Iot Hub and cannot be customized.</span></span>
- <span data-ttu-id="3a3ac-111">"Direcionado" especifica o número de dispositivos que combinam com a condição de destino.</span><span class="sxs-lookup"><span data-stu-id="3a3ac-111">"Targeted" specifies the number of device twins that match the target condition.</span></span>
- <span data-ttu-id="3a3ac-112">"Aplicado" especificou o número de dispositivos que foram modificados pela configuração.</span><span class="sxs-lookup"><span data-stu-id="3a3ac-112">"Applied" specified the number of device twins that have been modified by the configuration.</span></span> 

## <span data-ttu-id="3a3ac-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3a3ac-113">EXAMPLES</span></span>

### <span data-ttu-id="3a3ac-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3a3ac-114">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubConfigurationMetricsQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myConfig1" -MetricName "warningLimit"
```

<span data-ttu-id="3a3ac-115">Avalie a métrica "warningLimit" definida personalizada.</span><span class="sxs-lookup"><span data-stu-id="3a3ac-115">Evaluate the custom defined 'warningLimit' metric.</span></span>

### <span data-ttu-id="3a3ac-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="3a3ac-116">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubConfigMetric -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myConfig1" -MetricName "applied" -MetricType "system"
```

<span data-ttu-id="3a3ac-117">Avalie a métrica "aplicada" do sistema.</span><span class="sxs-lookup"><span data-stu-id="3a3ac-117">Evaluate the system 'applied' metric.</span></span>

## <span data-ttu-id="3a3ac-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="3a3ac-118">PARAMETERS</span></span>

### <span data-ttu-id="3a3ac-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a3ac-119">-DefaultProfile</span></span>
<span data-ttu-id="3a3ac-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3a3ac-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a3ac-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3a3ac-121">-InputObject</span></span>
<span data-ttu-id="3a3ac-122">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="3a3ac-122">IotHub object</span></span>

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

### <span data-ttu-id="3a3ac-123">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="3a3ac-123">-IotHubName</span></span>
<span data-ttu-id="3a3ac-124">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="3a3ac-124">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="3a3ac-125">-MetricName</span><span class="sxs-lookup"><span data-stu-id="3a3ac-125">-MetricName</span></span>
<span data-ttu-id="3a3ac-126">Métrica de destino para avaliação.</span><span class="sxs-lookup"><span data-stu-id="3a3ac-126">Target metric for evaluation.</span></span>

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

### <span data-ttu-id="3a3ac-127">-MetricType</span><span class="sxs-lookup"><span data-stu-id="3a3ac-127">-MetricType</span></span>
<span data-ttu-id="3a3ac-128">Indica qual coleção métrica deve ser usada para procurar uma métrica.</span><span class="sxs-lookup"><span data-stu-id="3a3ac-128">Indicates which metric collection should be used to lookup a metric.</span></span>

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

### <span data-ttu-id="3a3ac-129">-Name</span><span class="sxs-lookup"><span data-stu-id="3a3ac-129">-Name</span></span>
<span data-ttu-id="3a3ac-130">Identificador da configuração.</span><span class="sxs-lookup"><span data-stu-id="3a3ac-130">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="3a3ac-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a3ac-131">-ResourceGroupName</span></span>
<span data-ttu-id="3a3ac-132">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="3a3ac-132">Name of the Resource Group</span></span>

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

### <span data-ttu-id="3a3ac-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3a3ac-133">-ResourceId</span></span>
<span data-ttu-id="3a3ac-134">Id de Recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="3a3ac-134">IotHub Resource Id</span></span>

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

### <span data-ttu-id="3a3ac-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3a3ac-135">-Confirm</span></span>
<span data-ttu-id="3a3ac-136">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a3ac-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a3ac-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a3ac-137">-WhatIf</span></span>
<span data-ttu-id="3a3ac-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3a3ac-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a3ac-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3a3ac-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a3ac-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a3ac-140">CommonParameters</span></span>
<span data-ttu-id="3a3ac-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a3ac-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a3ac-142">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a3ac-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a3ac-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3a3ac-143">INPUTS</span></span>

### <span data-ttu-id="3a3ac-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="3a3ac-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="3a3ac-145">System.String</span><span class="sxs-lookup"><span data-stu-id="3a3ac-145">System.String</span></span>

## <span data-ttu-id="3a3ac-146">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="3a3ac-146">OUTPUTS</span></span>

### <span data-ttu-id="3a3ac-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurationMetricsResult</span><span class="sxs-lookup"><span data-stu-id="3a3ac-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurationMetricsResult</span></span>

## <span data-ttu-id="3a3ac-148">NOTES</span><span class="sxs-lookup"><span data-stu-id="3a3ac-148">NOTES</span></span>

## <span data-ttu-id="3a3ac-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3a3ac-149">RELATED LINKS</span></span>
