---
external help file: ''
Module Name: Azs.Storage.Admin
online version: https://docs.microsoft.com/powershell/module/azs.storage.admin/get-azsstoragequota
schema: 2.0.0
ms.openlocfilehash: ed5261a9b6d65918fce0fd90c8f2db0ff42baa3a
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/22/2020
ms.locfileid: "93945085"
---
# Get-AzsStorageQuota

## Sinopse


## SYNTAX

### Lista (padrão)
```
Get-AzsStorageQuota [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### Obter
```
Get-AzsStorageQuota -Name <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### GetViaIdentity
```
Get-AzsStorageQuota -InputObject <IStorageAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## DESCRITIVO


## EXEMPLOS

### Exemplo 1:
```powershell
PS C:\> Get-AzsStorageQuota
```

Obter a lista de cotas de armazenamento.

### Exemplo 2:
```powershell
PS C:\> Get-AzsStorageQuota -Name 'Default Quota'
```

Obter detalhes da cota de armazenamento especificada por nome.

## OS

### -DefaultProfile


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
Para construir, consulte a seção de observações para as propriedades INPUTobject e crie uma tabela de hash.

```yaml
Type: System.String
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### -Local


```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### -Nome


```yaml
Type: System.String
Parameter Sets: Get
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -SubscriptionId


```yaml
Type: System.String[]
Parameter Sets: Get, List
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

### Microsoft. Azure. PowerShell. cmdlets. StorageAdmin. Models. IStorageAdminIdentity

## EXIBE

### Microsoft. Azure. PowerShell. cmdlets. StorageAdmin. Models. Api201908Preview. IStorageQuota



## INFORMA

Propriedades de parâmetros complexas para criar os parâmetros descritos abaixo, construa uma tabela de hash contendo as propriedades adequadas. Para obter informações sobre tabelas de hash, execute Get-Help about_Hash_Tables.

INPUTobject <IStorageAdminIdentity> : 
  - `[AccountId <String>]`: ID da conta de armazenamento interno, que não está visível para locatário.
  - `[AsyncOperationId <String>]`: ID da operação assíncrona.
  - `[Id <String>]`: Caminho de identidade do recurso
  - `[Location <String>]`: Local do recurso.
  - `[QuotaName <String>]`: O nome da cota de armazenamento.
  - `[ResourceGroup <String>]`: Nome do grupo de recursos.
  - `[ServiceName <String>]`: Nome do serviço de armazenamento.
  - `[SubscriptionId <String>]`: ID da assinatura.

## LINKS RELACIONADOS

