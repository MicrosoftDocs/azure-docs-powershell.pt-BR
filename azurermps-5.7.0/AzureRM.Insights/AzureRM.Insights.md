---
Module Name: AzureRM.Insights
Module Guid: 698c387c-bd6b-41c6-82ce-721f1ef39548
Download Help Link:
  object Object: 
Help Version:
  object Object: 
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/AzureRM.Insights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/AzureRM.Insights.md
ms.openlocfilehash: d4f7819a3ddbf49f4a3c4ed56cd8273b1f2e1848
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "93425550"
---
# <span data-ttu-id="45313-101">Módulo AzureRM. insights</span><span class="sxs-lookup"><span data-stu-id="45313-101">AzureRM.Insights Module</span></span>
## <span data-ttu-id="45313-102">Descritivo</span><span class="sxs-lookup"><span data-stu-id="45313-102">Description</span></span>
<span data-ttu-id="45313-103">Este tópico exibe os tópicos da ajuda para os cmdlets do Azure insights.</span><span class="sxs-lookup"><span data-stu-id="45313-103">This topic displays help topics for the Azure Insights Cmdlets.</span></span>

## <span data-ttu-id="45313-104">Cmdlets do AzureRM. insights</span><span class="sxs-lookup"><span data-stu-id="45313-104">AzureRM.Insights Cmdlets</span></span>
### [<span data-ttu-id="45313-105">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="45313-105">Add-AzureRmAutoscaleSetting</span></span>](Add-AzureRmAutoscaleSetting.md)
<span data-ttu-id="45313-106">Cria uma configuração de autoescala.</span><span class="sxs-lookup"><span data-stu-id="45313-106">Creates an Autoscale setting.</span></span>

### [<span data-ttu-id="45313-107">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="45313-107">Add-AzureRmLogAlertRule</span></span>](Add-AzureRmLogAlertRule.md)
<span data-ttu-id="45313-108">Adiciona ou substitui uma regra de alerta de log.</span><span class="sxs-lookup"><span data-stu-id="45313-108">Adds or replaces a log alert rule.</span></span>

### [<span data-ttu-id="45313-109">Add-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="45313-109">Add-AzureRmLogProfile</span></span>](Add-AzureRmLogProfile.md)
<span data-ttu-id="45313-110">Cria um novo perfil de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="45313-110">Creates a new activity log profile.</span></span> <span data-ttu-id="45313-111">Esse perfil é usado para arquivar o log de atividades em uma conta de armazenamento do Azure ou transmiti-lo para um hub de eventos do Azure na mesma assinatura.</span><span class="sxs-lookup"><span data-stu-id="45313-111">This profile is used to either archive the activity log to an Azure storage account or stream it to an Azure event hub in the same subscription.</span></span> 

- <span data-ttu-id="45313-112">**Conta de armazenamento** somente conta de armazenamento padrão (conta de armazenamento Premium não é suportada) é suportada.</span><span class="sxs-lookup"><span data-stu-id="45313-112">**Storage Account** - Only standard storage account (premium storage account is not supported) is supported.</span></span> <span data-ttu-id="45313-113">Ele pode ser do tipo ARM ou Classic.</span><span class="sxs-lookup"><span data-stu-id="45313-113">It could either be of type ARM or Classic.</span></span> <span data-ttu-id="45313-114">Se estiver conectado a uma conta de armazenamento, o custo de armazenamento do log de atividades será cobrado em tarifas normais de armazenamento padrão.</span><span class="sxs-lookup"><span data-stu-id="45313-114">If it's logged to a storage account, the cost of storing the activity log is billed at normal standard storage rates.</span></span> <span data-ttu-id="45313-115">Pode haver apenas um perfil de log por assinatura com apenas uma conta de armazenamento por assinatura pode ser usada para exportar o log de atividades.</span><span class="sxs-lookup"><span data-stu-id="45313-115">There could be only one log profile per subscription consequentially only one storage account per subscription can be used to export activity log.</span></span> 

- <span data-ttu-id="45313-116">**Hub de eventos** – pode haver apenas um perfil de log por assinatura que apenas um hub de eventos por assinatura pode ser usado para exportar o log de atividades.</span><span class="sxs-lookup"><span data-stu-id="45313-116">**Event Hub** - There could be only one log profile per subscription consequentially only one event hub per subscription can be used to export activity log.</span></span> <span data-ttu-id="45313-117">Se o log de atividades for transmitido para um hub de eventos, será aplicado o preço padrão do Hub do evento.</span><span class="sxs-lookup"><span data-stu-id="45313-117">If activity log is streamed to an event hub, standard event hub pricing will apply.</span></span> 

<span data-ttu-id="45313-118">No log de atividades, os eventos podem pertencer a uma região ou podem ser "global".</span><span class="sxs-lookup"><span data-stu-id="45313-118">In the activity log, events can pertain to a region or could be "Global".</span></span> <span data-ttu-id="45313-119">Basicamente, o global significa que esses eventos são independentes de região e são independentes da região, na verdade, a maioria dos eventos se encaixa nessa categoria.</span><span class="sxs-lookup"><span data-stu-id="45313-119">Global essentially means these events are region agnostics and are independent of region, in fact majority of events fall into this category.</span></span> <span data-ttu-id="45313-120">Se o perfil do log de atividades for definido no portal, ele adicionará implicitamente "global" juntamente com qualquer outra região selecionada na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="45313-120">If the activity log profile is set from the portal, it implicitly adds "Global" along with any other region selected in the user interface.</span></span> <span data-ttu-id="45313-121">Ao usar o cmdlet, o local como "global" deve ser explicitamente mencionado separadamente de qualquer outra região.</span><span class="sxs-lookup"><span data-stu-id="45313-121">When using the cmdlet, the location as "Global" must be explicitly mentioned apart from any other region.</span></span> 

<span data-ttu-id="45313-122">**Observação** :- **falha ao definir "global" nos locais resultará na maioria dos registros de atividades não exportados.**</span><span class="sxs-lookup"><span data-stu-id="45313-122">**Note** :- **Failing to set "Global" in the locations will result in a majority of activity log not getting exported.**</span></span> 

### [<span data-ttu-id="45313-123">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="45313-123">Add-AzureRmMetricAlertRule</span></span>](Add-AzureRmMetricAlertRule.md)
<span data-ttu-id="45313-124">Adiciona ou atualiza uma regra de alerta baseada em métrica.</span><span class="sxs-lookup"><span data-stu-id="45313-124">Adds or updates a metric-based alert rule.</span></span>

### [<span data-ttu-id="45313-125">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="45313-125">Add-AzureRmWebtestAlertRule</span></span>](Add-AzureRmWebtestAlertRule.md)
<span data-ttu-id="45313-126">Adiciona ou atualiza uma regra de alerta de WebTest.</span><span class="sxs-lookup"><span data-stu-id="45313-126">Adds or updates a webtest alert rule.</span></span>

### [<span data-ttu-id="45313-127">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="45313-127">Disable-AzureRmActivityLogAlert</span></span>](Disable-AzureRmActivityLogAlert.md)
<span data-ttu-id="45313-128">Desabilita um alerta de log de atividades e define suas marcas.</span><span class="sxs-lookup"><span data-stu-id="45313-128">Disables an activity log alert and sets its tags.</span></span>

### [<span data-ttu-id="45313-129">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="45313-129">Enable-AzureRmActivityLogAlert</span></span>](Enable-AzureRmActivityLogAlert.md)
<span data-ttu-id="45313-130">Habilita um alerta de log de atividades e define suas marcas.</span><span class="sxs-lookup"><span data-stu-id="45313-130">Enables an activity log alert and sets its Tags.</span></span>

### [<span data-ttu-id="45313-131">Get-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="45313-131">Get-AzureRmActionGroup</span></span>](Get-AzureRmActionGroup.md)
<span data-ttu-id="45313-132">Obtém grupo (s) de ação.</span><span class="sxs-lookup"><span data-stu-id="45313-132">Gets action group(s).</span></span>

### [<span data-ttu-id="45313-133">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="45313-133">Get-AzureRmActivityLogAlert</span></span>](Get-AzureRmActivityLogAlert.md)
<span data-ttu-id="45313-134">Obtém um ou mais recursos de alerta de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="45313-134">Gets one or more activity log alert resources.</span></span>

### [<span data-ttu-id="45313-135">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="45313-135">Get-AzureRmAlertHistory</span></span>](Get-AzureRmAlertHistory.md)
<span data-ttu-id="45313-136">Obtém o histórico de alertas.</span><span class="sxs-lookup"><span data-stu-id="45313-136">Gets the history of alerts.</span></span>

### [<span data-ttu-id="45313-137">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="45313-137">Get-AzureRmAlertRule</span></span>](Get-AzureRmAlertRule.md)
<span data-ttu-id="45313-138">Recebe regras de alerta.</span><span class="sxs-lookup"><span data-stu-id="45313-138">Gets alert rules.</span></span>

### [<span data-ttu-id="45313-139">Get-AzureRmAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="45313-139">Get-AzureRmAutoscaleHistory</span></span>](Get-AzureRmAutoscaleHistory.md)
<span data-ttu-id="45313-140">Obtém o histórico de dimensionamento automático.</span><span class="sxs-lookup"><span data-stu-id="45313-140">Gets the Autoscale history.</span></span>

### [<span data-ttu-id="45313-141">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="45313-141">Get-AzureRmAutoscaleSetting</span></span>](Get-AzureRmAutoscaleSetting.md)
<span data-ttu-id="45313-142">Obtém as configurações de autoescala.</span><span class="sxs-lookup"><span data-stu-id="45313-142">Gets Autoscale settings.</span></span>

### [<span data-ttu-id="45313-143">Get-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="45313-143">Get-AzureRmDiagnosticSetting</span></span>](Get-AzureRmDiagnosticSetting.md)
<span data-ttu-id="45313-144">Obtém as categorias registradas e os refinamentos de tempo.</span><span class="sxs-lookup"><span data-stu-id="45313-144">Gets the logged categories and time grains.</span></span>

### [<span data-ttu-id="45313-145">Get-AzureRmLog</span><span class="sxs-lookup"><span data-stu-id="45313-145">Get-AzureRmLog</span></span>](Get-AzureRmLog.md)
<span data-ttu-id="45313-146">Obtém um log de eventos.</span><span class="sxs-lookup"><span data-stu-id="45313-146">Gets a log of events.</span></span>

### [<span data-ttu-id="45313-147">Get-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="45313-147">Get-AzureRmLogProfile</span></span>](Get-AzureRmLogProfile.md)
<span data-ttu-id="45313-148">Obtém um perfil de log.</span><span class="sxs-lookup"><span data-stu-id="45313-148">Gets a log profile.</span></span>

### [<span data-ttu-id="45313-149">Get-AzureRmMetric</span><span class="sxs-lookup"><span data-stu-id="45313-149">Get-AzureRmMetric</span></span>](Get-AzureRmMetric.md)
<span data-ttu-id="45313-150">Obtém os valores métricos de um recurso.</span><span class="sxs-lookup"><span data-stu-id="45313-150">Gets the metric values of a resource.</span></span>

### [<span data-ttu-id="45313-151">Get-AzureRmMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="45313-151">Get-AzureRmMetricDefinition</span></span>](Get-AzureRmMetricDefinition.md)
<span data-ttu-id="45313-152">Obtém definições métricas.</span><span class="sxs-lookup"><span data-stu-id="45313-152">Gets metric definitions.</span></span>

### [<span data-ttu-id="45313-153">Get-AzureRmUsage</span><span class="sxs-lookup"><span data-stu-id="45313-153">Get-AzureRmUsage</span></span>](Get-AzureRmUsage.md)
<span data-ttu-id="45313-154">Obtém as métricas de uso de um recurso.</span><span class="sxs-lookup"><span data-stu-id="45313-154">Gets the usage metrics for a resource.</span></span>

### [<span data-ttu-id="45313-155">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="45313-155">New-AzureRmActionGroup</span></span>](New-AzureRmActionGroup.md)
<span data-ttu-id="45313-156">Cria um objeto de referência do objeto de ação na memória.</span><span class="sxs-lookup"><span data-stu-id="45313-156">Creates an ActionGroup reference object in memory.</span></span>

### [<span data-ttu-id="45313-157">New-AzureRmActionGroupReceiver</span><span class="sxs-lookup"><span data-stu-id="45313-157">New-AzureRmActionGroupReceiver</span></span>](New-AzureRmActionGroupReceiver.md)
<span data-ttu-id="45313-158">Cria um novo receptor de grupo de ação.</span><span class="sxs-lookup"><span data-stu-id="45313-158">Creates an new action group receiver.</span></span>

### [<span data-ttu-id="45313-159">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="45313-159">New-AzureRmActivityLogAlertCondition</span></span>](New-AzureRmActivityLogAlertCondition.md)
<span data-ttu-id="45313-160">Cria um novo objeto de condição de alerta de log de atividades na memória.</span><span class="sxs-lookup"><span data-stu-id="45313-160">Creates an new activity log alert condition object in memory.</span></span>

### [<span data-ttu-id="45313-161">New-AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="45313-161">New-AzureRmAlertRuleEmail</span></span>](New-AzureRmAlertRuleEmail.md)
<span data-ttu-id="45313-162">Cria uma ação de email para uma regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="45313-162">Creates an email action for an alert rule.</span></span>

### [<span data-ttu-id="45313-163">New-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="45313-163">New-AzureRmAlertRuleWebhook</span></span>](New-AzureRmAlertRuleWebhook.md)
<span data-ttu-id="45313-164">Cria um webhook de regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="45313-164">Creates an alert rule webhook.</span></span>

### [<span data-ttu-id="45313-165">New-AzureRmAutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="45313-165">New-AzureRmAutoscaleNotification</span></span>](New-AzureRmAutoscaleNotification.md)
<span data-ttu-id="45313-166">Cria uma notificação por email de autoescala.</span><span class="sxs-lookup"><span data-stu-id="45313-166">Creates an Autoscale email notification.</span></span>

### [<span data-ttu-id="45313-167">New-AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="45313-167">New-AzureRmAutoscaleProfile</span></span>](New-AzureRmAutoscaleProfile.md)
<span data-ttu-id="45313-168">Cria um perfil de autoescala.</span><span class="sxs-lookup"><span data-stu-id="45313-168">Creates an Autoscale profile.</span></span>

### [<span data-ttu-id="45313-169">New-AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="45313-169">New-AzureRmAutoscaleRule</span></span>](New-AzureRmAutoscaleRule.md)
<span data-ttu-id="45313-170">Cria uma regra de autoescala.</span><span class="sxs-lookup"><span data-stu-id="45313-170">Creates an Autoscale rule.</span></span>

### [<span data-ttu-id="45313-171">New-AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="45313-171">New-AzureRmAutoscaleWebhook</span></span>](New-AzureRmAutoscaleWebhook.md)
<span data-ttu-id="45313-172">Cria um webhook de autoescala.</span><span class="sxs-lookup"><span data-stu-id="45313-172">Creates an Autoscale webhook.</span></span>

### [<span data-ttu-id="45313-173">Remove-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="45313-173">Remove-AzureRmActionGroup</span></span>](Remove-AzureRmActionGroup.md)
<span data-ttu-id="45313-174">Remove um grupo de ações.</span><span class="sxs-lookup"><span data-stu-id="45313-174">Removes an action group.</span></span>

### [<span data-ttu-id="45313-175">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="45313-175">Remove-AzureRmActivityLogAlert</span></span>](Remove-AzureRmActivityLogAlert.md)
<span data-ttu-id="45313-176">Remove um alerta de log de atividades.</span><span class="sxs-lookup"><span data-stu-id="45313-176">Removes an activity log alert.</span></span>

### [<span data-ttu-id="45313-177">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="45313-177">Remove-AzureRmAlertRule</span></span>](Remove-AzureRmAlertRule.md)
<span data-ttu-id="45313-178">Remove uma regra de alerta.</span><span class="sxs-lookup"><span data-stu-id="45313-178">Removes an alert rule.</span></span>

### [<span data-ttu-id="45313-179">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="45313-179">Remove-AzureRmAutoscaleSetting</span></span>](Remove-AzureRmAutoscaleSetting.md)
<span data-ttu-id="45313-180">Remove uma configuração de autoescala.</span><span class="sxs-lookup"><span data-stu-id="45313-180">Removes an Autoscale setting.</span></span>

### [<span data-ttu-id="45313-181">Remove-AzureRmLogProfile</span><span class="sxs-lookup"><span data-stu-id="45313-181">Remove-AzureRmLogProfile</span></span>](Remove-AzureRmLogProfile.md)
<span data-ttu-id="45313-182">Remove um perfil de log.</span><span class="sxs-lookup"><span data-stu-id="45313-182">Removes a log profile.</span></span>

### [<span data-ttu-id="45313-183">Set-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="45313-183">Set-AzureRmActionGroup</span></span>](Set-AzureRmActionGroup.md)
<span data-ttu-id="45313-184">Cria uma nova ou atualiza um grupo de ações existente.</span><span class="sxs-lookup"><span data-stu-id="45313-184">Creates a new or updates an existing action group.</span></span>

### [<span data-ttu-id="45313-185">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="45313-185">Set-AzureRmActivityLogAlert</span></span>](Set-AzureRmActivityLogAlert.md)
<span data-ttu-id="45313-186">Cria um novo ou define um alerta de log de atividades existente.</span><span class="sxs-lookup"><span data-stu-id="45313-186">Creates a new or sets an existing activity log alert.</span></span>

### [<span data-ttu-id="45313-187">Set-AzureRmDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="45313-187">Set-AzureRmDiagnosticSetting</span></span>](Set-AzureRmDiagnosticSetting.md)
<span data-ttu-id="45313-188">Define as configurações de logs e métricas do recurso.</span><span class="sxs-lookup"><span data-stu-id="45313-188">Sets the logs and metrics settings for the resource.</span></span>

