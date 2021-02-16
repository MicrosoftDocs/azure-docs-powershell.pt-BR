---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A837077C-0A79-431C-93D2-799B2134EE69
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzAlertRule.md
ms.openlocfilehash: fb485d185fdb1e04a40208408dbd5fd352e0905f
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100406376"
---
# <span data-ttu-id="2d167-101">Get-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="2d167-101">Get-AzAlertRule</span></span>

## <span data-ttu-id="2d167-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2d167-102">SYNOPSIS</span></span>
<span data-ttu-id="2d167-103">Recebe regras de alerta.</span><span class="sxs-lookup"><span data-stu-id="2d167-103">Gets alert rules.</span></span>

## <span data-ttu-id="2d167-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2d167-104">SYNTAX</span></span>

### <span data-ttu-id="2d167-105">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2d167-105">GetByResourceGroup</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2d167-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="2d167-106">GetByName</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> -Name <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2d167-107">GetByResourceUri</span><span class="sxs-lookup"><span data-stu-id="2d167-107">GetByResourceUri</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> -TargetResourceId <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d167-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="2d167-108">DESCRIPTION</span></span>
<span data-ttu-id="2d167-109">O **cmdlet Get-AzAlertRule** obtém uma regra de alerta pelo nome ou URI, ou todas as regras de alerta de um grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="2d167-109">The **Get-AzAlertRule** cmdlet gets an alert rule by its name or URI, or all alert rules from a specified resource group.</span></span>

## <span data-ttu-id="2d167-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2d167-110">EXAMPLES</span></span>

### <span data-ttu-id="2d167-111">Exemplo 1: Obter regras de alerta para um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="2d167-111">Example 1: Get alert rules for a resource group</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS"
```

<span data-ttu-id="2d167-112">Esse comando obtém todas as regras de alerta do grupo de recursos chamado Default-Web-CentralUS.</span><span class="sxs-lookup"><span data-stu-id="2d167-112">This command gets all of the alert rules for the resource group named Default-Web-CentralUS.</span></span>
<span data-ttu-id="2d167-113">A saída não contém detalhes sobre as regras porque o parâmetro *DetailedOutput* não está especificado.</span><span class="sxs-lookup"><span data-stu-id="2d167-113">The output does not contain details about the rules because the *DetailedOutput* parameter is not specified.</span></span>

### <span data-ttu-id="2d167-114">Exemplo 2: Obter uma regra de alerta por nome</span><span class="sxs-lookup"><span data-stu-id="2d167-114">Example 2: Get an alert rule by name</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
```

<span data-ttu-id="2d167-115">Esse comando obtém a regra de alerta chamada myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span><span class="sxs-lookup"><span data-stu-id="2d167-115">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="2d167-116">Como o *parâmetro DetailedOutput* não é especificado, a saída contém apenas informações básicas sobre a regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="2d167-116">Because the *DetailedOutput* parameter is not specified, the output contains only basic information about the alert rule.</span></span>

### <span data-ttu-id="2d167-117">Exemplo 3: Obter uma regra de alerta por nome com saída detalhada</span><span class="sxs-lookup"><span data-stu-id="2d167-117">Example 3: Get an alert rule by name with detailed output</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8" -DetailedOutput
```

<span data-ttu-id="2d167-118">Esse comando obtém a regra de alerta chamada myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span><span class="sxs-lookup"><span data-stu-id="2d167-118">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="2d167-119">O *parâmetro DetailedOutput* é especificado, portanto, a saída é detalhada.</span><span class="sxs-lookup"><span data-stu-id="2d167-119">The *DetailedOutput* parameter is specified, so the output is detailed.</span></span>

## <span data-ttu-id="2d167-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2d167-120">PARAMETERS</span></span>

### <span data-ttu-id="2d167-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d167-121">-DefaultProfile</span></span>
<span data-ttu-id="2d167-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="2d167-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2d167-123">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="2d167-123">-DetailedOutput</span></span>
<span data-ttu-id="2d167-124">Exibe detalhes completos na saída.</span><span class="sxs-lookup"><span data-stu-id="2d167-124">Displays full details in the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d167-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="2d167-125">-Name</span></span>
<span data-ttu-id="2d167-126">Especifica o nome da regra de alerta para obter.</span><span class="sxs-lookup"><span data-stu-id="2d167-126">Specifies the name of the alert rule to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d167-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d167-127">-ResourceGroupName</span></span>
<span data-ttu-id="2d167-128">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2d167-128">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d167-129">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="2d167-129">-TargetResourceId</span></span>
<span data-ttu-id="2d167-130">Especifica a ID do recurso de destino.</span><span class="sxs-lookup"><span data-stu-id="2d167-130">Specifies the ID of the target resource.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d167-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d167-131">CommonParameters</span></span>
<span data-ttu-id="2d167-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d167-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d167-133">Para obter mais informações, [consulte about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2d167-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d167-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="2d167-134">INPUTS</span></span>

### <span data-ttu-id="2d167-135">System.String</span><span class="sxs-lookup"><span data-stu-id="2d167-135">System.String</span></span>

### <span data-ttu-id="2d167-136">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2d167-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2d167-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="2d167-137">OUTPUTS</span></span>

### <span data-ttu-id="2d167-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSAlertRule</span><span class="sxs-lookup"><span data-stu-id="2d167-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSAlertRule</span></span>

## <span data-ttu-id="2d167-139">Notas</span><span class="sxs-lookup"><span data-stu-id="2d167-139">NOTES</span></span>

## <span data-ttu-id="2d167-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2d167-140">RELATED LINKS</span></span>


[<span data-ttu-id="2d167-141">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="2d167-141">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="2d167-142">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="2d167-142">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="2d167-143">Get-AzAlertHistory</span><span class="sxs-lookup"><span data-stu-id="2d167-143">Get-AzAlertHistory</span></span>](./Get-AzAlertHistory.md)

[<span data-ttu-id="2d167-144">Remove-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="2d167-144">Remove-AzAlertRule</span></span>](./Remove-AzAlertRule.md)


