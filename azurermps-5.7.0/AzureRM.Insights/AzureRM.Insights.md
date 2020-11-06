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
# Módulo AzureRM. insights
## Descritivo
Este tópico exibe os tópicos da ajuda para os cmdlets do Azure insights.

## Cmdlets do AzureRM. insights
### [Add-AzureRmAutoscaleSetting](Add-AzureRmAutoscaleSetting.md)
Cria uma configuração de autoescala.

### [Add-AzureRmLogAlertRule](Add-AzureRmLogAlertRule.md)
Adiciona ou substitui uma regra de alerta de log.

### [Add-AzureRmLogProfile](Add-AzureRmLogProfile.md)
Cria um novo perfil de log de atividades. Esse perfil é usado para arquivar o log de atividades em uma conta de armazenamento do Azure ou transmiti-lo para um hub de eventos do Azure na mesma assinatura. 

- **Conta de armazenamento** somente conta de armazenamento padrão (conta de armazenamento Premium não é suportada) é suportada. Ele pode ser do tipo ARM ou Classic. Se estiver conectado a uma conta de armazenamento, o custo de armazenamento do log de atividades será cobrado em tarifas normais de armazenamento padrão. Pode haver apenas um perfil de log por assinatura com apenas uma conta de armazenamento por assinatura pode ser usada para exportar o log de atividades. 

- **Hub de eventos** – pode haver apenas um perfil de log por assinatura que apenas um hub de eventos por assinatura pode ser usado para exportar o log de atividades. Se o log de atividades for transmitido para um hub de eventos, será aplicado o preço padrão do Hub do evento. 

No log de atividades, os eventos podem pertencer a uma região ou podem ser "global". Basicamente, o global significa que esses eventos são independentes de região e são independentes da região, na verdade, a maioria dos eventos se encaixa nessa categoria. Se o perfil do log de atividades for definido no portal, ele adicionará implicitamente "global" juntamente com qualquer outra região selecionada na interface do usuário. Ao usar o cmdlet, o local como "global" deve ser explicitamente mencionado separadamente de qualquer outra região. 

**Observação** :- **falha ao definir "global" nos locais resultará na maioria dos registros de atividades não exportados.** 

### [Add-AzureRmMetricAlertRule](Add-AzureRmMetricAlertRule.md)
Adiciona ou atualiza uma regra de alerta baseada em métrica.

### [Add-AzureRmWebtestAlertRule](Add-AzureRmWebtestAlertRule.md)
Adiciona ou atualiza uma regra de alerta de WebTest.

### [Disable-AzureRmActivityLogAlert](Disable-AzureRmActivityLogAlert.md)
Desabilita um alerta de log de atividades e define suas marcas.

### [Enable-AzureRmActivityLogAlert](Enable-AzureRmActivityLogAlert.md)
Habilita um alerta de log de atividades e define suas marcas.

### [Get-AzureRmActionGroup](Get-AzureRmActionGroup.md)
Obtém grupo (s) de ação.

### [Get-AzureRmActivityLogAlert](Get-AzureRmActivityLogAlert.md)
Obtém um ou mais recursos de alerta de log de atividades.

### [Get-AzureRmAlertHistory](Get-AzureRmAlertHistory.md)
Obtém o histórico de alertas.

### [Get-AzureRmAlertRule](Get-AzureRmAlertRule.md)
Recebe regras de alerta.

### [Get-AzureRmAutoscaleHistory](Get-AzureRmAutoscaleHistory.md)
Obtém o histórico de dimensionamento automático.

### [Get-AzureRmAutoscaleSetting](Get-AzureRmAutoscaleSetting.md)
Obtém as configurações de autoescala.

### [Get-AzureRmDiagnosticSetting](Get-AzureRmDiagnosticSetting.md)
Obtém as categorias registradas e os refinamentos de tempo.

### [Get-AzureRmLog](Get-AzureRmLog.md)
Obtém um log de eventos.

### [Get-AzureRmLogProfile](Get-AzureRmLogProfile.md)
Obtém um perfil de log.

### [Get-AzureRmMetric](Get-AzureRmMetric.md)
Obtém os valores métricos de um recurso.

### [Get-AzureRmMetricDefinition](Get-AzureRmMetricDefinition.md)
Obtém definições métricas.

### [Get-AzureRmUsage](Get-AzureRmUsage.md)
Obtém as métricas de uso de um recurso.

### [New-AzureRmActionGroup](New-AzureRmActionGroup.md)
Cria um objeto de referência do objeto de ação na memória.

### [New-AzureRmActionGroupReceiver](New-AzureRmActionGroupReceiver.md)
Cria um novo receptor de grupo de ação.

### [New-AzureRmActivityLogAlertCondition](New-AzureRmActivityLogAlertCondition.md)
Cria um novo objeto de condição de alerta de log de atividades na memória.

### [New-AzureRmAlertRuleEmail](New-AzureRmAlertRuleEmail.md)
Cria uma ação de email para uma regra de alerta.

### [New-AzureRmAlertRuleWebhook](New-AzureRmAlertRuleWebhook.md)
Cria um webhook de regra de alerta.

### [New-AzureRmAutoscaleNotification](New-AzureRmAutoscaleNotification.md)
Cria uma notificação por email de autoescala.

### [New-AzureRmAutoscaleProfile](New-AzureRmAutoscaleProfile.md)
Cria um perfil de autoescala.

### [New-AzureRmAutoscaleRule](New-AzureRmAutoscaleRule.md)
Cria uma regra de autoescala.

### [New-AzureRmAutoscaleWebhook](New-AzureRmAutoscaleWebhook.md)
Cria um webhook de autoescala.

### [Remove-AzureRmActionGroup](Remove-AzureRmActionGroup.md)
Remove um grupo de ações.

### [Remove-AzureRmActivityLogAlert](Remove-AzureRmActivityLogAlert.md)
Remove um alerta de log de atividades.

### [Remove-AzureRmAlertRule](Remove-AzureRmAlertRule.md)
Remove uma regra de alerta.

### [Remove-AzureRmAutoscaleSetting](Remove-AzureRmAutoscaleSetting.md)
Remove uma configuração de autoescala.

### [Remove-AzureRmLogProfile](Remove-AzureRmLogProfile.md)
Remove um perfil de log.

### [Set-AzureRmActionGroup](Set-AzureRmActionGroup.md)
Cria uma nova ou atualiza um grupo de ações existente.

### [Set-AzureRmActivityLogAlert](Set-AzureRmActivityLogAlert.md)
Cria um novo ou define um alerta de log de atividades existente.

### [Set-AzureRmDiagnosticSetting](Set-AzureRmDiagnosticSetting.md)
Define as configurações de logs e métricas do recurso.

