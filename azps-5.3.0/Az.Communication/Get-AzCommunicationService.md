---
external help file: ''
Module Name: Az.Communication
online version: https://docs.microsoft.com/en-us/powershell/module/az.communication/get-azcommunicationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Get-AzCommunicationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Communication/help/Get-AzCommunicationService.md
ms.openlocfilehash: 3101ca2b120860dfa6df95786e235fc88fd0fc78
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98434403"
---
# Get-AzCommunicationService

## Sinopse
Obtenha o CommunicationService e suas propriedades.

## SYNTAX

### Lista (padrão)
```
Get-AzCommunicationService [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### Obter
```
Get-AzCommunicationService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzCommunicationService -InputObject <ICommunicationIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### List1
```
Get-AzCommunicationService -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## DESCRITIVO
Obtenha o CommunicationService e suas propriedades.

## EXEMPLOS

### Exemplo 1: listar as comunicações existentes para uma assinatura
```powershell
PS C:\> Get-AzCommunicationService -SubscriptionId 73fc3592-3cef-4300-5e19-8d18b65ce0e8

Location Name             Type                                          AzureAsyncOperation
-------- ----             ----                                          -------------------
global   ContosoResource1   Microsoft.Communication/communicationServices
global   ContosoResource4   Microsoft.Communication/communicationServices
global   ContosoResource3   Microsoft.Communication/communicationServices
global   ContosoResource5   Microsoft.Communication/communicationServices
```

Retorna uma lista de todos os recursos do ACS sob essa assinatura.

### Exemplo 2: obter informações sobre o recurso de comunicação do Azure especificado
```powershell
PS C:\> Get-AzCommunicationService -Name ContosoAcsResource1 -ResourceGroupName ContosoResourceProvider1

Location Name           Type                                          AzureAsyncOperation
-------- ----           ----                                          -------------------
Global   ContosoAcsResource1 Microsoft.Communication/communicationServices
```

Retorna as informações em um recurso ACS, se houver um parâmetro correspondente fornecido.

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Parâmetro de identidade para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Communication.Models.ICommunicationIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Nome
O nome do recurso CommunicationService.

```yaml
Type: System.String
Parameter Sets: Get
Aliases: CommunicationServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
O nome do grupo de recursos que contém o recurso.
Você pode obter esse valor da API do Azure Resource Manager ou do Portal.

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Obtém a ID da assinatura que identifica exclusivamente a assinatura do Microsoft Azure.
A ID da assinatura forma a parte do URI para cada chamada de serviço.

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## SENSORES

### Microsoft. Azure. PowerShell. cmdlets. Communication. Models. ICommunicationIdentity

## EXIBE

### Microsoft. Azure. PowerShell. cmdlets. Communication. Models. Api20200820Preview. ICommunicationServiceResource

## INFORMA

ALIASES

PROPRIEDADES DE PARÂMETROS COMPLEXAS

Para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas. Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.


INPUTobject <ICommunicationIdentity> : parâmetro de identidade
  - `[CommunicationServiceName <String>]`: O nome do recurso CommunicationService.
  - `[Id <String>]`: Caminho de identidade do recurso
  - `[Location <String>]`: A região do Azure
  - `[OperationId <String>]`: A ID de uma operação assíncrona em andamento
  - `[ResourceGroupName <String>]`: O nome do grupo de recursos que contém o recurso. Você pode obter esse valor da API do Azure Resource Manager ou do Portal.
  - `[SubscriptionId <String>]`: Obtém a ID de assinatura que identifica exclusivamente a assinatura do Microsoft Azure. A ID da assinatura forma a parte do URI para cada chamada de serviço.

## LINKS RELACIONADOS

