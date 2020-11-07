---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 86438393-8D5A-46A0-B467-6A4434E18011
online version: ''
schema: 2.0.0
ms.openlocfilehash: 42c8760dee1aa095086d4fad3309a3a5da64b296
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946309"
---
# Get-AzureService

## Sinopse
Retorna um objeto com informações sobre os serviços de nuvem para a assinatura atual.

## SYNTAX

```
Get-AzureService [[-ServiceName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureService** retorna um objeto List com todos os serviços de nuvem do Azure associados à assinatura atual.
Se você especificar o parâmetro *ServiceName* , **Get-AzureService** retornará apenas as informações sobre o serviço correspondente.

## EXEMPLOS

### Exemplo 1: obter informações sobre todos os serviços
```
PS C:\> Get-AzureService
```

Esse comando retorna um objeto que contém informações sobre todos os serviços do Azure associados à assinatura atual.

### Exemplo 2: obter informações sobre um serviço especificado
```
PS C:\> Get-AzureService -ServiceName $MySvc
```

Esse comando retorna informações sobre o serviço de $MySvc.

### Exemplo 3: Exibir métodos e propriedades disponíveis
```
PS C:\> Get-AzureService | Get-Member
```

Esse comando exibe as propriedades e os métodos que estão disponíveis a partir do cmdlet **Get-AzureService** .

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

### -ServiceName
Especifica o nome de um serviço no qual você deve retornar informações.

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

### HostedServiceContext

## INFORMA

## LINKS RELACIONADOS

[New-AzureService](./New-AzureService.md)

[Set-AzureService](./Set-AzureService.md)


