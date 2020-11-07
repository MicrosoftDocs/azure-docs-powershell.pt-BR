---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 0DF54C9D-7A19-4591-A1FC-33C6A4C9BF33
online version: ''
schema: 2.0.0
ms.openlocfilehash: 05a99e1a4965329c0eeb29fe0e014814fd1807b2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945937"
---
# Test-AzureName

## Sinopse
Testa se um nome de serviço de nuvem do Microsoft Azure, nome do serviço de armazenamento ou nome do namespace de barramento de serviço existe ou não.

## SYNTAX

### Atender
```
Test-AzureName [-Service] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### SPS
```
Test-AzureName [-Storage] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ServiceBusNamespace
```
Test-AzureName [-ServiceBusNamespace] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### Site
```
Test-AzureName [-Website] -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
Se o nome existir, o cmdlet retornará $True.
Se o nome não existir, será retornado $False.

## EXEMPLOS

### Exemplo 1
```
PS C:\> Test-AzureName -Service "MyNameService1"
```

Esse comando testa se o "MyNameService1" é um nome de serviço de nuvem do Microsoft Azure existente.

### Exemplo 2
```
PS C:\> Test-AzureName -Storage "mystorename1"
```

Esse comando testa se o "mystorename1" é um nome de serviço de armazenamento do Microsoft Azure existente.

### Exemplo 3
```
PS C:\> Test-AzureName -ServiceBusNamespace "mynamespace"
```

Esse comando testa se o "MyNamespace" é um nome de namespace de barramento do serviço do Microsoft Azure existente.

## OS

### -Nome
Especifica o nome do serviço ou da conta de armazenamento a ser testada.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -Serviço
Especifica o teste para uma conta de serviço existente.

```yaml
Type: SwitchParameter
Parameter Sets: Service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceBusNamespace
Especifica o teste para um namespace de barramento de serviço existente.

```yaml
Type: SwitchParameter
Parameter Sets: ServiceBusNamespace
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Armazenamento
Especifica o teste para uma conta de armazenamento existente.

```yaml
Type: SwitchParameter
Parameter Sets: Storage
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Website
Especifica o teste para um site existente.

```yaml
Type: SwitchParameter
Parameter Sets: Website
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

## INFORMA
* nó-dev, php-dev, Python-dev

## LINKS RELACIONADOS

