---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7D7D1FAE-5360-428B-AAE9-9D1109A7B67F
online version: ''
schema: 2.0.0
ms.openlocfilehash: faccd241929beca1f2423fa9c23f35793233205b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945549"
---
# Get-AzureStorageAccount

## Sinopse
Obtém as contas de armazenamento para a assinatura atual do Azure.

## SYNTAX

```
Get-AzureStorageAccount [[-StorageAccountName] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureStorageAccount** retorna um objeto que contém informações sobre as contas de armazenamento da assinatura atual.
Se o parâmetro *StorageAccountName* for especificado, apenas informações sobre a conta de armazenamento especificada serão retornadas.

## EXEMPLOS

### Exemplo 1: retornar todas as contas de armazenamento
```
PS C:\> Get-AzureStorageAccount
```

Esse comando retorna um objeto com todas as contas de armazenamento associadas à assinatura atual.

### Exemplo 2: retornar informações da conta para uma conta especificada
```
PS C:\> Get-AzureStorageAccount -StorageAccountName "ContosoStore01"
```

Esse comando retorna um objeto com apenas as informações da conta do ContosoStore01.

### Exemplo 3: exibir uma tabela de contas de armazenamento
```
PS C:\> Get-AzureStorageAccount | Format-Table -AutoSize -Property @{Label="Name";Expression={$_.StorageAccountName}},"Label","Location"
```

Esse comando retorna um objeto com todas as contas de armazenamento associadas à assinatura atual e os gera como uma tabela que mostra o nome da conta, o rótulo da conta e o local de armazenamento.

## OS

### -Informationaction
Especifica como esse cmdlet responde a um evento de informações.

Os valores aceitáveis para esse parâmetro são:

- Contínuo
- Ignorar
- Inquire
- SilentlyContinue
- Finaliza
- Suspensão

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Especifica uma variável de informações.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Perfil
Especifica o perfil do Azure do qual este cmdlet lê.
Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountName
Especifica o nome de uma conta de armazenamento.
Se especificado, esse cmdlet retornará apenas o objeto da conta de armazenamento especificado.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

### ManagementOperationContext

## INFORMA
* Digite `help node-dev` para obter ajuda sobre cmdlets relacionados a desenvolvimento Node.js. Digite `help php-dev` para obter ajuda sobre cmdlets relacionados ao desenvolvimento PHP.

## LINKS RELACIONADOS

[New-AzureStorageAccount](./New-AzureStorageAccount.md)

[Set-AzureStorageAccount](./Set-AzureStorageAccount.md)


