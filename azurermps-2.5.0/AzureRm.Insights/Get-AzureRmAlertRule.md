---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A837077C-0A79-431C-93D2-799B2134EE69
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermalertrule
schema: 2.0.0
ms.openlocfilehash: fe763bcf6ff4aeeeedb3ff0dcb0c2ebd5c4b45cc
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786520"
---
# <span data-ttu-id="e5e20-101">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="e5e20-101">Get-AzureRmAlertRule</span></span>

## <span data-ttu-id="e5e20-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e5e20-102">SYNOPSIS</span></span>
<span data-ttu-id="e5e20-103">Recebe regras de alerta.</span><span class="sxs-lookup"><span data-stu-id="e5e20-103">Gets alert rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5e20-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e5e20-104">SYNTAX</span></span>

### <span data-ttu-id="e5e20-105">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e5e20-105">GetByResourceGroup</span></span>
```
Get-AzureRmAlertRule -ResourceGroupName <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e5e20-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="e5e20-106">GetByName</span></span>
```
Get-AzureRmAlertRule -ResourceGroupName <String> -Name <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e5e20-107">GetByResourceUri</span><span class="sxs-lookup"><span data-stu-id="e5e20-107">GetByResourceUri</span></span>
```
Get-AzureRmAlertRule -ResourceGroupName <String> -TargetResourceId <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5e20-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e5e20-108">DESCRIPTION</span></span>
<span data-ttu-id="e5e20-109">O cmdlet **Get-AzureRmAlertRule** Obtém uma regra de alerta por seu nome ou URI, ou todas as regras de alerta de um grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="e5e20-109">The **Get-AzureRmAlertRule** cmdlet gets an alert rule by its name or URI, or all alert rules from a specified resource group.</span></span>

## <span data-ttu-id="e5e20-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e5e20-110">EXAMPLES</span></span>

### <span data-ttu-id="e5e20-111">Exemplo 1: obter regras de alerta para um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="e5e20-111">Example 1: Get alert rules for a resource group</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS"
```

<span data-ttu-id="e5e20-112">Esse comando obtém todas as regras de alerta para o grupo de recursos chamado Default-Web-Centralus.</span><span class="sxs-lookup"><span data-stu-id="e5e20-112">This command gets all of the alert rules for the resource group named Default-Web-CentralUS.</span></span>
<span data-ttu-id="e5e20-113">A saída não contém detalhes sobre as regras porque o parâmetro *DetailedOutput* não está especificado.</span><span class="sxs-lookup"><span data-stu-id="e5e20-113">The output does not contain details about the rules because the *DetailedOutput* parameter is not specified.</span></span>

### <span data-ttu-id="e5e20-114">Exemplo 2: obter uma regra de alerta por nome</span><span class="sxs-lookup"><span data-stu-id="e5e20-114">Example 2: Get an alert rule by name</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
```

<span data-ttu-id="e5e20-115">Esse comando obtém a regra de alerta chamada MyALERT-7da64548-214d-42CA-b12b-b245bb8f0ac8.</span><span class="sxs-lookup"><span data-stu-id="e5e20-115">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="e5e20-116">Como o parâmetro *DetailedOutput* não é especificado, a saída contém apenas informações básicas sobre a regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="e5e20-116">Because the *DetailedOutput* parameter is not specified, the output contains only basic information about the alert rule.</span></span>

### <span data-ttu-id="e5e20-117">Exemplo 3: obter uma regra de alerta por nome com uma saída detalhada</span><span class="sxs-lookup"><span data-stu-id="e5e20-117">Example 3: Get an alert rule by name with detailed output</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8" -DetailedOutput
```

<span data-ttu-id="e5e20-118">Esse comando obtém a regra de alerta chamada MyALERT-7da64548-214d-42CA-b12b-b245bb8f0ac8.</span><span class="sxs-lookup"><span data-stu-id="e5e20-118">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="e5e20-119">O parâmetro *DetailedOutput* é especificado para que a saída seja detalhada.</span><span class="sxs-lookup"><span data-stu-id="e5e20-119">The *DetailedOutput* parameter is specified, so the output is detailed.</span></span>

## <span data-ttu-id="e5e20-120">OS</span><span class="sxs-lookup"><span data-stu-id="e5e20-120">PARAMETERS</span></span>

### <span data-ttu-id="e5e20-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5e20-121">-DefaultProfile</span></span>
<span data-ttu-id="e5e20-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="e5e20-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5e20-123">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="e5e20-123">-DetailedOutput</span></span>
<span data-ttu-id="e5e20-124">Exibe detalhes completos na saída.</span><span class="sxs-lookup"><span data-stu-id="e5e20-124">Displays full details in the output.</span></span>

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

### <span data-ttu-id="e5e20-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="e5e20-125">-Name</span></span>
<span data-ttu-id="e5e20-126">Especifica o nome da regra de alerta a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="e5e20-126">Specifies the name of the alert rule to get.</span></span>

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

### <span data-ttu-id="e5e20-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5e20-127">-ResourceGroupName</span></span>
<span data-ttu-id="e5e20-128">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e5e20-128">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="e5e20-129">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="e5e20-129">-TargetResourceId</span></span>
<span data-ttu-id="e5e20-130">Especifica a ID do recurso de destino.</span><span class="sxs-lookup"><span data-stu-id="e5e20-130">Specifies the ID of the target resource.</span></span>

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

### <span data-ttu-id="e5e20-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5e20-131">CommonParameters</span></span>
<span data-ttu-id="e5e20-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5e20-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5e20-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5e20-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5e20-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e5e20-134">INPUTS</span></span>

### <span data-ttu-id="e5e20-135">System. String</span><span class="sxs-lookup"><span data-stu-id="e5e20-135">System.String</span></span>

### <span data-ttu-id="e5e20-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e5e20-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e5e20-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e5e20-137">OUTPUTS</span></span>

### <span data-ttu-id="e5e20-138">Microsoft. Azure. Commands. insights. OutputClasses. PSAlertRule</span><span class="sxs-lookup"><span data-stu-id="e5e20-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSAlertRule</span></span>

## <span data-ttu-id="e5e20-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e5e20-139">NOTES</span></span>

## <span data-ttu-id="e5e20-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e5e20-140">RELATED LINKS</span></span>



[<span data-ttu-id="e5e20-141">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="e5e20-141">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="e5e20-142">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="e5e20-142">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="e5e20-143">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="e5e20-143">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="e5e20-144">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="e5e20-144">Remove-AzureRmAlertRule</span></span>](./Remove-AzureRmAlertRule.md)


