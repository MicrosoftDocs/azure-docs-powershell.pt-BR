---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/invoke-aziothubconfigurationmetricsquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubConfigurationMetricsQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Invoke-AzIotHubConfigurationMetricsQuery.md
ms.openlocfilehash: 85793ba3097297de646db4695cac36173bb01673
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117613"
---
# <span data-ttu-id="420d4-101">Invoke-AzIotHubConfigurationMetricsQuery</span><span class="sxs-lookup"><span data-stu-id="420d4-101">Invoke-AzIotHubConfigurationMetricsQuery</span></span>

## <span data-ttu-id="420d4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="420d4-102">SYNOPSIS</span></span>
<span data-ttu-id="420d4-103">Invocar uma consulta métrica de configuração de dispositivo IoT.</span><span class="sxs-lookup"><span data-stu-id="420d4-103">Invoke an IoT device configuration metric query.</span></span>

## <span data-ttu-id="420d4-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="420d4-104">SYNTAX</span></span>

### <span data-ttu-id="420d4-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="420d4-105">ResourceSet (Default)</span></span>
```
Invoke-AzIotHubConfigurationMetricsQuery [-ResourceGroupName] <String> [-IotHubName] <String> -Name <String>
 -MetricName <String> [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="420d4-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="420d4-106">InputObjectSet</span></span>
```
Invoke-AzIotHubConfigurationMetricsQuery [-InputObject] <PSIotHub> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="420d4-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="420d4-107">ResourceIdSet</span></span>
```
Invoke-AzIotHubConfigurationMetricsQuery [-ResourceId] <String> -Name <String> -MetricName <String>
 [-MetricType <PSConfigurationMetricType>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="420d4-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="420d4-108">DESCRIPTION</span></span>
<span data-ttu-id="420d4-109">Avalie uma métrica de sistema ou personalizada de destino definida em uma configuração de dispositivo IoT.</span><span class="sxs-lookup"><span data-stu-id="420d4-109">Evaluate a target custom or system metric defined in an IoT device configuration.</span></span>
<span data-ttu-id="420d4-110">Há métricas de sistema pré-definidas que são calculadas pelo Hub Iot e não podem ser personalizadas.</span><span class="sxs-lookup"><span data-stu-id="420d4-110">There are pre-defined system metrics which are calculated by Iot Hub and cannot be customized.</span></span>
- <span data-ttu-id="420d4-111">"Direcionado" especifica o número de dispositivos que combinam com a condição de destino.</span><span class="sxs-lookup"><span data-stu-id="420d4-111">"Targeted" specifies the number of device twins that match the target condition.</span></span>
- <span data-ttu-id="420d4-112">"Aplicado" especificou o número de dispositivos que foram modificados pela configuração.</span><span class="sxs-lookup"><span data-stu-id="420d4-112">"Applied" specified the number of device twins that have been modified by the configuration.</span></span> 

## <span data-ttu-id="420d4-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="420d4-113">EXAMPLES</span></span>

### <span data-ttu-id="420d4-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="420d4-114">Example 1</span></span>
```powershell
PS C:\> Invoke-AzIotHubConfigurationMetricsQuery -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myConfig1" -MetricName "warningLimit"
```

<span data-ttu-id="420d4-115">Avalie a métrica personalizada definida como "avisoLimit".</span><span class="sxs-lookup"><span data-stu-id="420d4-115">Evaluate the custom defined 'warningLimit' metric.</span></span>

### <span data-ttu-id="420d4-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="420d4-116">Example 2</span></span>
```powershell
PS C:\> Invoke-AzIotHubConfigMetric -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "myConfig1" -MetricName "applied" -MetricType "system"
```

<span data-ttu-id="420d4-117">Avalie a métrica do sistema "aplicada".</span><span class="sxs-lookup"><span data-stu-id="420d4-117">Evaluate the system 'applied' metric.</span></span>

## <span data-ttu-id="420d4-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="420d4-118">PARAMETERS</span></span>

### <span data-ttu-id="420d4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="420d4-119">-DefaultProfile</span></span>
<span data-ttu-id="420d4-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="420d4-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="420d4-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="420d4-121">-InputObject</span></span>
<span data-ttu-id="420d4-122">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="420d4-122">IotHub object</span></span>

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

### <span data-ttu-id="420d4-123">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="420d4-123">-IotHubName</span></span>
<span data-ttu-id="420d4-124">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="420d4-124">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="420d4-125">-MetricName</span><span class="sxs-lookup"><span data-stu-id="420d4-125">-MetricName</span></span>
<span data-ttu-id="420d4-126">Métrica de destino para avaliação.</span><span class="sxs-lookup"><span data-stu-id="420d4-126">Target metric for evaluation.</span></span>

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

### <span data-ttu-id="420d4-127">-MetricType</span><span class="sxs-lookup"><span data-stu-id="420d4-127">-MetricType</span></span>
<span data-ttu-id="420d4-128">Indica qual conjunto métrico deve ser usado para procurar uma métrica.</span><span class="sxs-lookup"><span data-stu-id="420d4-128">Indicates which metric collection should be used to lookup a metric.</span></span>

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

### <span data-ttu-id="420d4-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="420d4-129">-Name</span></span>
<span data-ttu-id="420d4-130">Identificador da configuração.</span><span class="sxs-lookup"><span data-stu-id="420d4-130">Identifier for the configuration.</span></span>

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

### <span data-ttu-id="420d4-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="420d4-131">-ResourceGroupName</span></span>
<span data-ttu-id="420d4-132">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="420d4-132">Name of the Resource Group</span></span>

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

### <span data-ttu-id="420d4-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="420d4-133">-ResourceId</span></span>
<span data-ttu-id="420d4-134">ID de Recurso do IotHub</span><span class="sxs-lookup"><span data-stu-id="420d4-134">IotHub Resource Id</span></span>

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

### <span data-ttu-id="420d4-135">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="420d4-135">-Confirm</span></span>
<span data-ttu-id="420d4-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="420d4-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="420d4-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="420d4-137">-WhatIf</span></span>
<span data-ttu-id="420d4-138">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="420d4-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="420d4-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="420d4-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="420d4-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="420d4-140">CommonParameters</span></span>
<span data-ttu-id="420d4-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="420d4-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="420d4-142">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="420d4-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="420d4-143">Entradas</span><span class="sxs-lookup"><span data-stu-id="420d4-143">INPUTS</span></span>

### <span data-ttu-id="420d4-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="420d4-144">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="420d4-145">System.String</span><span class="sxs-lookup"><span data-stu-id="420d4-145">System.String</span></span>

## <span data-ttu-id="420d4-146">Saídas</span><span class="sxs-lookup"><span data-stu-id="420d4-146">OUTPUTS</span></span>

### <span data-ttu-id="420d4-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurationMetricsResult</span><span class="sxs-lookup"><span data-stu-id="420d4-147">Microsoft.Azure.Commands.Management.IotHub.Models.PSConfigurationMetricsResult</span></span>

## <span data-ttu-id="420d4-148">Notas</span><span class="sxs-lookup"><span data-stu-id="420d4-148">NOTES</span></span>

## <span data-ttu-id="420d4-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="420d4-149">RELATED LINKS</span></span>
