---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 92E2409B-14BC-428F-8BAF-60D8DAFA5F57
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1adaafdfdd4331bbba86530eb532964430ed7c69
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945935"
---
# Test-AzureTrafficManagerDomainName

## Sinopse
Verifica se um nome de domínio está disponível como um perfil do Gerenciador de tráfego.

## SYNTAX

```
Test-AzureTrafficManagerDomainName -DomainName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Test-AzureTrafficManagerDomainName** verifica se um nome de domínio está disponível como um perfil do Gerenciador de tráfego do Microsoft Azure.
Se o nome de domínio estiver disponível, esse cmdlet retornará um valor de $True.

## EXEMPLOS

### Exemplo 1: verificar se um nome de domínio está disponível
```
PS C:\>Test-AzureTrafficManagerDomainName -DomainName "ContosoApp.trafficmanager.net"
$True
```

Esse comando verifica se o nome de domínio ContosoApp.trafficmanager.net está disponível como um perfil do Gerenciador de tráfego.

## OS

### -DomainName
Especifica o nome de domínio a ser testado.
Você deve incluir a seguinte cadeia de caracteres: 

. trafficmanager.net

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

### System. Boolean
Este cmdlet gera $True ou $False.
Se o nome de domínio estiver disponível, esse cmdlet retornará um valor de $True.

## INFORMA

## LINKS RELACIONADOS

