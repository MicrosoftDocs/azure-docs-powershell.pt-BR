---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A837077C-0A79-431C-93D2-799B2134EE69
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmAlertRule.md
ms.openlocfilehash: 65c5bc7a2767fd00497b487783c4e6f0ce6d6723
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441048"
---
# <span data-ttu-id="63c9e-101">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="63c9e-101">Get-AzureRmAlertRule</span></span>

## <span data-ttu-id="63c9e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="63c9e-102">SYNOPSIS</span></span>
<span data-ttu-id="63c9e-103">Recebe regras de alerta.</span><span class="sxs-lookup"><span data-stu-id="63c9e-103">Gets alert rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63c9e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="63c9e-104">SYNTAX</span></span>

### <span data-ttu-id="63c9e-105">Parâmetros para Get-AzureRmAlertRule cmdlet</span><span class="sxs-lookup"><span data-stu-id="63c9e-105">Parameters for Get-AzureRmAlertRule cmdlet</span></span>
```
Get-AzureRmAlertRule -ResourceGroup <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="63c9e-106">Parâmetros para o cmdlet Get-AzureRmAlertRule usando o nome</span><span class="sxs-lookup"><span data-stu-id="63c9e-106">Parameters for Get-AzureRmAlertRule cmdlet using name</span></span>
```
Get-AzureRmAlertRule -ResourceGroup <String> -Name <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="63c9e-107">Parâmetros para o cmdlet Get-AzureRmAlertRule usando o URI do recurso de destino</span><span class="sxs-lookup"><span data-stu-id="63c9e-107">Parameters for Get-AzureRmAlertRule cmdlet using target resource uri</span></span>
```
Get-AzureRmAlertRule -ResourceGroup <String> -TargetResourceId <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="63c9e-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="63c9e-108">DESCRIPTION</span></span>
<span data-ttu-id="63c9e-109">O cmdlet **Get-AzureRmAlertRule** Obtém uma regra de alerta por seu nome ou URI, ou todas as regras de alerta de um grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="63c9e-109">The **Get-AzureRmAlertRule** cmdlet gets an alert rule by its name or URI, or all alert rules from a specified resource group.</span></span>

## <span data-ttu-id="63c9e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="63c9e-110">EXAMPLES</span></span>

### <span data-ttu-id="63c9e-111">Exemplo 1: obter regras de alerta para um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="63c9e-111">Example 1: Get alert rules for a resource group</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS"
```

<span data-ttu-id="63c9e-112">Esse comando obtém todas as regras de alerta para o grupo de recursos chamado Default-Web-Centralus.</span><span class="sxs-lookup"><span data-stu-id="63c9e-112">This command gets all of the alert rules for the resource group named Default-Web-CentralUS.</span></span>
<span data-ttu-id="63c9e-113">A saída não contém detalhes sobre as regras porque o parâmetro *DetailedOutput* não está especificado.</span><span class="sxs-lookup"><span data-stu-id="63c9e-113">The output does not contain details about the rules because the *DetailedOutput* parameter is not specified.</span></span>

### <span data-ttu-id="63c9e-114">Exemplo 2: obter uma regra de alerta por nome</span><span class="sxs-lookup"><span data-stu-id="63c9e-114">Example 2: Get an alert rule by name</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourcGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
```

<span data-ttu-id="63c9e-115">Esse comando obtém a regra de alerta chamada MyALERT-7da64548-214d-42CA-b12b-b245bb8f0ac8.</span><span class="sxs-lookup"><span data-stu-id="63c9e-115">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="63c9e-116">Como o parâmetro *DetailedOutput* não é especificado, a saída contém apenas informações básicas sobre a regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="63c9e-116">Because the *DetailedOutput* parameter is not specified, the output contains only basic information about the alert rule.</span></span>

### <span data-ttu-id="63c9e-117">Exemplo 3: obter uma regra de alerta por nome com uma saída detalhada</span><span class="sxs-lookup"><span data-stu-id="63c9e-117">Example 3: Get an alert rule by name with detailed output</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8" -DetailedOutput
```

<span data-ttu-id="63c9e-118">Esse comando obtém a regra de alerta chamada MyALERT-7da64548-214d-42CA-b12b-b245bb8f0ac8.</span><span class="sxs-lookup"><span data-stu-id="63c9e-118">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="63c9e-119">O parâmetro *DetailedOutput* é especificado para que a saída seja detalhada.</span><span class="sxs-lookup"><span data-stu-id="63c9e-119">The *DetailedOutput* parameter is specified, so the output is detailed.</span></span>

## <span data-ttu-id="63c9e-120">OS</span><span class="sxs-lookup"><span data-stu-id="63c9e-120">PARAMETERS</span></span>

### <span data-ttu-id="63c9e-121">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="63c9e-121">-DetailedOutput</span></span>
<span data-ttu-id="63c9e-122">Exibe detalhes completos na saída.</span><span class="sxs-lookup"><span data-stu-id="63c9e-122">Displays full details in the output.</span></span>

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

### <span data-ttu-id="63c9e-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="63c9e-123">-Name</span></span>
<span data-ttu-id="63c9e-124">Especifica o nome da regra de alerta a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="63c9e-124">Specifies the name of the alert rule to get.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters for Get-AzureRmAlertRule cmdlet using name
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63c9e-125">-Resource</span><span class="sxs-lookup"><span data-stu-id="63c9e-125">-ResourceGroup</span></span>
<span data-ttu-id="63c9e-126">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="63c9e-126">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63c9e-127">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="63c9e-127">-TargetResourceId</span></span>
<span data-ttu-id="63c9e-128">Especifica a ID do recurso de destino.</span><span class="sxs-lookup"><span data-stu-id="63c9e-128">Specifies the ID of the target resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters for Get-AzureRmAlertRule cmdlet using target resource uri
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63c9e-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63c9e-129">-DefaultProfile</span></span>
<span data-ttu-id="63c9e-130">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="63c9e-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63c9e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63c9e-131">CommonParameters</span></span>
<span data-ttu-id="63c9e-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63c9e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63c9e-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63c9e-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63c9e-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="63c9e-134">INPUTS</span></span>

## <span data-ttu-id="63c9e-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="63c9e-135">OUTPUTS</span></span>

### <span data-ttu-id="63c9e-136">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. insights. OutputClasses. PSManagementItemDescriptor]</span><span class="sxs-lookup"><span data-stu-id="63c9e-136">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSManagementItemDescriptor]</span></span>

## <span data-ttu-id="63c9e-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="63c9e-137">NOTES</span></span>

## <span data-ttu-id="63c9e-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="63c9e-138">RELATED LINKS</span></span>

[<span data-ttu-id="63c9e-139">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="63c9e-139">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="63c9e-140">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="63c9e-140">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="63c9e-141">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="63c9e-141">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="63c9e-142">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="63c9e-142">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="63c9e-143">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="63c9e-143">Remove-AzureRmAlertRule</span></span>](./Remove-AzureRmAlertRule.md)


