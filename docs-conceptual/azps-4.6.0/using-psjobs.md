---
title: Executar cmdlets do Azure PowerShell nos Trabalhos do PowerShell
description: Saiba como executar os cmdlets do Azure PowerShell em paralelo ou como tarefas em segundo plano, usando -AsJob e Start-Job.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/21/2019
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 5d9028c0a433149c8f6cc346651bb8bf875bb42a
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "89241773"
---
# <a name="run-azure-powershell-cmdlets-in-powershell-jobs"></a>Executar cmdlets do Azure PowerShell nos Trabalhos do PowerShell

O Azure PowerShell depende da conexão com uma nuvem do Azure e da espera de respostas. Portanto, a maioria desses cmdlets bloqueia a sessão do PowerShell até receber uma resposta da nuvem.
Os Trabalhos do Powershell permitem que você execute cmdlets no segundo plano ou realize várias tarefas no Azure de uma só vez, de dentro de uma única sessão do PowerShell.

Este artigo é uma breve visão geral de como executar cmdlets do Azure PowerShell como Trabalhos do PowerShell e verificar a conclusão. A execução de comandos no Azure PowerShell requer o uso de contextos do Azure PowerShell, abordados detalhadamente em [contextos e credenciais de entrada do Azure](context-persistence.md).
Para saber mais sobre Trabalhos do PowerShell, confira [Sobre Trabalhos do PowerShell](/powershell/module/microsoft.powershell.core/about/about_jobs).

## <a name="azure-contexts-with-powershell-jobs"></a>Contextos do Azure com trabalhos do PowerShell

Os Trabalhos do PowerShell são executados como processos separados sem uma sessão do PowerShell anexada, portanto, suas credenciais do Azure devem ser compartilhadas com eles. As credenciais são passadas como objetos de contexto do Azure, usando um destes métodos:

* Persistência de contexto automática. A persistência de contexto é habilitada por padrão e preserva suas informações de conexão em várias sessões. Com a persistência de contexto habilitada, o contexto do Azure atual é passado para o novo processo:

  ```azurepowershell-interactive
  Enable-AzContextAutosave # Enables context autosave if not already on
  $creds = Get-Credential
  $job = Start-Job { param($vmadmin) New-AzVM -Name MyVm -Credential $vmadmin } -ArgumentList $creds
  ```

* Use o parâmetro `-AzContext` com cmdlets do Azure PowerShell para fornecer um objeto de contexto do Azure:

  ```azurepowershell-interactive
  $context = Get-AzContext -Name 'mycontext' # Get an Azure context object
  $creds = Get-Credential
  $job = Start-Job { param($context, $vmadmin) New-AzVM -Name MyVm -AzContext $context -Credential $vmadmin} -ArgumentList $context,$creds }
  ```

  Se a persistência de contexto estiver desabilitada, o argumento `-AzContext` será necessário.

* Use a opção `-AsJob` fornecida por alguns cmdlets do Azure PowerShell. Essa opção inicia automaticamente o cmdlet como um Trabalho do PowerShell, usando o contexto do Azure ativo no momento:

  ```azurepowershell-interactive
  $creds = Get-Credential
  $job = New-AzVM -Name MyVm -Credential $creds -AsJob
  ```

  Para ver se um cmdlet dá suporte ao `-AsJob`, confira sua documentação de referência. A opção `-AsJob` não requer que o salvamento automático de contexto seja habilitado.

Você pode verificar o status de um trabalho em execução com o cmdlet [Get-Job](/powershell/module/microsoft.powershell.core/get-job). Para obter a saída de um trabalho até o momento, use o cmdlet [Receive-Job](/powershell/module/microsoft.powershell.core/receive-job).

Para verificar o progresso de uma operação remotamente no Azure, use os cmdlets `Get-` associados ao tipo de recurso que está sendo modificado pelo trabalho:

```azurepowershell-interactive
$creds = Get-Credential
$context = Get-AzContext -Name 'mycontext'
$vmName = "MyVm"

$job = Start-Job { param($context, $vmName, $vmadmin) New-AzVM -Name $vmName -AzContext $context -Credential $vmadmin} -ArgumentList $context,$vmName,$creds }

Get-Job $job
Get-AzVM -Name $vmName
```

## <a name="see-also"></a>Consulte Também

* [Contextos do Azure PowerShell](context-persistence.md)
* [Sobre Trabalhos do PowerShell](/powershell/module/microsoft.powershell.core/about/about_jobs)
* [Referência Get-Job](/powershell/module/microsoft.powershell.core/get-job)
* [Referência Receive-Job](/powershell/module/microsoft.powershell.core/receive-job)
