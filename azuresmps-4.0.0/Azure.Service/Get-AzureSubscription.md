---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 32BC6CE6-60EF-4A46-912B-8FE4FCCDF7CC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2b91906a25d2f2d7c40f96ed07a4fd7463722023
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945537"
---
# Get-AzureSubscription

## Sinopse
Obtém assinaturas do Azure na conta do Azure.

## SYNTAX

### ByName (padrão)
```
Get-AzureSubscription [-SubscriptionName <String>] [-ExtendedDetails] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### ById
```
Get-AzureSubscription [-SubscriptionId <String>] [-ExtendedDetails] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### Assume
```
Get-AzureSubscription [-Default] [-ExtendedDetails] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### Atualizados
```
Get-AzureSubscription [-Current] [-ExtendedDetails] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureSubscription** Obtém as assinaturas na sua conta do Azure.
Você pode usar esse cmdlet para obter informações sobre a assinatura e para canalizar a assinatura para outros cmdlets.

**Get-AzureSubscription** requer acesso às suas contas do Azure.
Antes de executar **Get-AzureSubscription** , você deve executar o cmdlet **Add-AzureAccount** ou os cmdlets que baixam e instalam um arquivo de configurações de publicação ( **Get-AzurePublishSettingsFile** , **Import-AzurePublishSettingsFile**.

Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.
Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .

## EXEMPLOS

### Exemplo 1: obter todas as assinaturas
```
C:\PS>Get-AzureSubscription
```

Esse comando obtém todas as assinaturas na conta.

### Exemplo 2: obter uma assinatura por nome
```
C:\PS>Get-AzureSubscription -SubscriptionName "MyProdSubscription"
```

Esse comando obtém apenas a assinatura "MyProdSubsciption".

### Exemplo 3: obter a assinatura padrão
```
C:\PS>(Get-AzureSubscription -Default).SubscriptionName
```

Esse comando obtém apenas o nome da assinatura padrão.
O comando recebe primeiro a assinatura e, em seguida, usa o método dot para obter a propriedade **subscriptionname** da assinatura.

### Exemplo 4: obter as propriedades da assinatura selecionada
```
C:\PS>Get-AzureSubscription -Current | Format-List -Property SubscriptionName, Certificate
```

Esse comando retorna uma lista com o nome e o certificado da assinatura atual.
Ele usa um comando **Get-AzureSubscription** para obter a assinatura atual.
Em seguida, ele canaliza a assinatura para um comando de **lista de formatação** que exibe as propriedades selecionadas em uma lista.

### Exemplo 5: usar um arquivo de dados de assinatura alternativo
```
C:\PS>Get-AzureSubscription -SubscriptionDataFile "C:\Temp\MySubscriptions.xml"
```

Este comando obtém assinaturas do arquivo de dados de assinatura do C:\Temp\MySubscriptions.xml.
Use o parâmetro **SubscriptionDataFile** se você tiver especificado um arquivo de dados de assinatura alternativo ao executar os cmdlets **Add-AzureAccount** ou **Import-PublishSettingsFile** .

## OS

### -Atual
Obtém apenas a assinatura atual, ou seja, a assinatura designada como "atual". Por padrão, **Get-AzureSubscription** obtém todas as assinaturas em suas contas do Azure.
Para designar uma assinatura como "atual", use o parâmetro **atual** do cmdlet **Select-AzureSubscription** .

```yaml
Type: SwitchParameter
Parameter Sets: Current
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Padrão
Obtém apenas a assinatura padrão, ou seja, a assinatura designada como "padrão". Por padrão, **Get-AzureSubscription** obtém todas as assinaturas em suas contas do Azure.
Para designar uma assinatura como "padrão", use o parâmetro **padrão** do cmdlet **Select-AzureSubscription** .

```yaml
Type: SwitchParameter
Parameter Sets: Default
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExtendedDetails
Retorna as informações de cota da assinatura, além das configurações padrão.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Perfil
Especifica o perfil do Azure do qual este cmdlet lê. Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.

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

### -SubscriptionId
```yaml
Type: String
Parameter Sets: ById
Aliases: Id

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Subscriptionname
Obtém apenas a assinatura especificada.
Digite o nome da assinatura.
O valor diferencia maiúsculas de minúsculas.
Não há suporte para caracteres curinga.
Por padrão, **Get-AzureSubscription** obtém todas as assinaturas em suas contas do Azure.

```yaml
Type: String
Parameter Sets: ByName
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma
Você pode canalizar a entrada para a propriedade **subscriptionname** por nome, mas não por valor.

## EXIBE

### Microsoft. WindowsAzure. Commands. Utilities. Common. WindowsAzureSubscription

## INFORMA
* Get-AzureSubscription obtém dados do arquivo de dados de assinatura que os cmdlets **Add-AzureAccount** e **Import-PublishSettingsFile** criam.

## LINKS RELACIONADOS

[Add-AzureAccount](./Add-AzureAccount.md)

[Get-AzurePublishSettingsFile](./Get-AzurePublishSettingsFile.md)

[Import-AzurePublishSettingsFile](./Import-AzurePublishSettingsFile.md)

[Remove-AzureSubscription](./Remove-AzureSubscription.md)

[Set-AzureSubscription](./Set-AzureSubscription.md)


