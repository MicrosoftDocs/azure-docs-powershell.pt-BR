---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 11A521DF-E77C-4D6F-A2D9-1C2CF8972F57
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmLogAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmLogAlertRule.md
ms.openlocfilehash: 38644018ac9ae19d1c413123ca071f564d336fa7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441062"
---
# <span data-ttu-id="c97b7-101">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="c97b7-101">Add-AzureRmLogAlertRule</span></span>

## <span data-ttu-id="c97b7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c97b7-102">SYNOPSIS</span></span>
<span data-ttu-id="c97b7-103">Adiciona ou substitui uma regra de alerta de log.</span><span class="sxs-lookup"><span data-stu-id="c97b7-103">Adds or replaces a log alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c97b7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c97b7-104">SYNTAX</span></span>

```
Add-AzureRmLogAlertRule [-TargetResourceGroup <String>] [-TargetResourceId <String>] [-Level <String>]
 -OperationName <String> [-TargetResourceProvider <String>] [-Status <String>] [-SubStatus <String>]
 -Location <String> [-Description <String>] [-DisableRule] -ResourceGroup <String> -Name <String>
 [-Actions <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c97b7-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c97b7-105">DESCRIPTION</span></span>
<span data-ttu-id="c97b7-106">O cmdlet **Add-AzureRmLogAlertRule** adiciona ou substitui uma regra de alerta de evento.</span><span class="sxs-lookup"><span data-stu-id="c97b7-106">The **Add-AzureRmLogAlertRule** cmdlet adds or replaces an event alert rule.</span></span>
<span data-ttu-id="c97b7-107">A regra adicionada está associada a um grupo de recursos e tem um nome.</span><span class="sxs-lookup"><span data-stu-id="c97b7-107">The added rule is associated with a resource group and has a name.</span></span>

<span data-ttu-id="c97b7-108">Como anunciado nas versões anteriores: **o cmdlet Add-AzureRMLogAlertRule será preterido em uma versão futura.**</span><span class="sxs-lookup"><span data-stu-id="c97b7-108">As announced in previous releases: **Add-AzureRMLogAlertRule cmdlet will be deprecated in a future release.**</span></span> <span data-ttu-id="c97b7-109">Após 1º de outubro de 2017 usar esse cmdlet não terá mais nenhum efeito, pois essa funcionalidade está sendo transformada em alertas de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="c97b7-109">After October 1st 2017 using this cmdlet will no longer have any effect as this functionality is being transitioned to Activity Log Alerts.</span></span> <span data-ttu-id="c97b7-110">Para obter **_https://aka.ms/migratemealerts_** mais informações, consulte.</span><span class="sxs-lookup"><span data-stu-id="c97b7-110">Please see **_https://aka.ms/migratemealerts_** for more information.</span></span>

## <span data-ttu-id="c97b7-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c97b7-111">EXAMPLES</span></span>

### <span data-ttu-id="c97b7-112">Exemplo 1: adicionar uma regra de alerta de log</span><span class="sxs-lookup"><span data-stu-id="c97b7-112">Example 1: Add a log alert rule</span></span>
```
PS C:\>Add-AzureRmLogAlertRule -Name "logRule" -Location "East US" -ResourceGroup "Default-Web-EastUS" -OperationName "Create" -TargetResourceId "/subscriptions/abbfb07c-6c93-40be-bc9b-4f0deba32f4c/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/misitiooeltuyo" -Description "My log rule"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="c97b7-113">Esse comando adiciona ou atualiza uma regra de alerta baseada em eventos.</span><span class="sxs-lookup"><span data-stu-id="c97b7-113">This command adds or updates an event-based alert rule.</span></span>

## <span data-ttu-id="c97b7-114">OS</span><span class="sxs-lookup"><span data-stu-id="c97b7-114">PARAMETERS</span></span>

### <span data-ttu-id="c97b7-115">-Ações</span><span class="sxs-lookup"><span data-stu-id="c97b7-115">-Actions</span></span>
<span data-ttu-id="c97b7-116">Especifica uma lista de ações separada por vírgulas.</span><span class="sxs-lookup"><span data-stu-id="c97b7-116">Specifies a comma-separated list of actions.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c97b7-117">-Descrição</span><span class="sxs-lookup"><span data-stu-id="c97b7-117">-Description</span></span>
<span data-ttu-id="c97b7-118">Especifica uma descrição da regra.</span><span class="sxs-lookup"><span data-stu-id="c97b7-118">Specifies a description of the rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c97b7-119">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="c97b7-119">-DisableRule</span></span>
<span data-ttu-id="c97b7-120">Desabilita uma regra.</span><span class="sxs-lookup"><span data-stu-id="c97b7-120">Disables a rule.</span></span>
<span data-ttu-id="c97b7-121">Se você não especificar esse parâmetro, a regra estará habilitada.</span><span class="sxs-lookup"><span data-stu-id="c97b7-121">If you do not specify this parameter, the rule is enabled.</span></span>

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

### <span data-ttu-id="c97b7-122">-Level</span><span class="sxs-lookup"><span data-stu-id="c97b7-122">-Level</span></span>
<span data-ttu-id="c97b7-123">Especifica o nível do evento que a regra está monitorando.</span><span class="sxs-lookup"><span data-stu-id="c97b7-123">Specifies the level of the event the rule is monitoring.</span></span>
<span data-ttu-id="c97b7-124">Especifique esse parâmetro somente para regras baseadas em eventos.</span><span class="sxs-lookup"><span data-stu-id="c97b7-124">Specify this parameter only for event-based rules.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c97b7-125">-Local</span><span class="sxs-lookup"><span data-stu-id="c97b7-125">-Location</span></span>
<span data-ttu-id="c97b7-126">Especifica o local para a regra.</span><span class="sxs-lookup"><span data-stu-id="c97b7-126">Specifies the location for the rule.</span></span>

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

### <span data-ttu-id="c97b7-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="c97b7-127">-Name</span></span>
<span data-ttu-id="c97b7-128">Especifica o nome da regra.</span><span class="sxs-lookup"><span data-stu-id="c97b7-128">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="c97b7-129">-OperationName</span><span class="sxs-lookup"><span data-stu-id="c97b7-129">-OperationName</span></span>
<span data-ttu-id="c97b7-130">Especifica o nome da operação.</span><span class="sxs-lookup"><span data-stu-id="c97b7-130">Specifies the name of the operation.</span></span>

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

### <span data-ttu-id="c97b7-131">-Resource</span><span class="sxs-lookup"><span data-stu-id="c97b7-131">-ResourceGroup</span></span>
<span data-ttu-id="c97b7-132">Especifica o nome do grupo de recursos para a regra.</span><span class="sxs-lookup"><span data-stu-id="c97b7-132">Specifies the name of the resource group for the rule.</span></span>

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

### <span data-ttu-id="c97b7-133">-Status</span><span class="sxs-lookup"><span data-stu-id="c97b7-133">-Status</span></span>
<span data-ttu-id="c97b7-134">Especifica o status.</span><span class="sxs-lookup"><span data-stu-id="c97b7-134">Specifies the status.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c97b7-135">-Substatus</span><span class="sxs-lookup"><span data-stu-id="c97b7-135">-SubStatus</span></span>
<span data-ttu-id="c97b7-136">Especifica o substatus.</span><span class="sxs-lookup"><span data-stu-id="c97b7-136">Specifies the substatus.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c97b7-137">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c97b7-137">-TargetResourceGroup</span></span>
<span data-ttu-id="c97b7-138">Especifica o grupo de recursos do recurso que a regra está monitorando.</span><span class="sxs-lookup"><span data-stu-id="c97b7-138">Specifies the resource group of the resource the rule is monitoring.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c97b7-139">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="c97b7-139">-TargetResourceId</span></span>
<span data-ttu-id="c97b7-140">Especifica a ID do recurso que a regra está monitorando.</span><span class="sxs-lookup"><span data-stu-id="c97b7-140">Specifies the ID of the resource the rule is monitoring.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c97b7-141">-TargetResourceProvider</span><span class="sxs-lookup"><span data-stu-id="c97b7-141">-TargetResourceProvider</span></span>
<span data-ttu-id="c97b7-142">Especifica o provedor de recursos do recurso que a regra está monitorando.</span><span class="sxs-lookup"><span data-stu-id="c97b7-142">Specifies the resource provider of the resource the rule is monitoring.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c97b7-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c97b7-143">-DefaultProfile</span></span>
<span data-ttu-id="c97b7-144">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c97b7-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c97b7-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c97b7-145">CommonParameters</span></span>
<span data-ttu-id="c97b7-146">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c97b7-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c97b7-147">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c97b7-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c97b7-148">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c97b7-148">INPUTS</span></span>

## <span data-ttu-id="c97b7-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c97b7-149">OUTPUTS</span></span>

### <span data-ttu-id="c97b7-150">Microsoft. Azure. Commands. insights. OutputClasses. PSAddAlertRuleOperationResponse</span><span class="sxs-lookup"><span data-stu-id="c97b7-150">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="c97b7-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c97b7-151">NOTES</span></span>

## <span data-ttu-id="c97b7-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c97b7-152">RELATED LINKS</span></span>

[<span data-ttu-id="c97b7-153">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="c97b7-153">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="c97b7-154">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="c97b7-154">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="c97b7-155">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="c97b7-155">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="c97b7-156">New-AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="c97b7-156">New-AzureRmAlertRuleEmail</span></span>](./New-AzureRmAlertRuleEmail.md)

[<span data-ttu-id="c97b7-157">New-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="c97b7-157">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


