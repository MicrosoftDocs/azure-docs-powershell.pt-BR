---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 58DABEB0-D3B6-478B-9B83-80E4C67A7792
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1d4717e795bcfea9728cbabb1b7c788713907aaa
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946570"
---
# Get-AzureRemoteAppVNet

## Sinopse
Recupera informações sobre as redes virtuais do Azure RemoteApp no Azure.

## SYNTAX

```
Get-AzureRemoteAppVNet [[-VNetName] <String>] [-IncludeSharedKey] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRemoteAppVNet** recupera informações sobre as redes virtuais do Azure RemoteApp no Microsoft Azure.
Esse cmdlet retorna um objeto que contém informações sobre uma rede virtual especificada.
Se nenhuma rede virtual for especificada, esse cmdlet retornará informações sobre todas as redes virtuais na assinatura atual.

## EXEMPLOS

### Exemplo 1: recuperar informações sobre uma rede virtual
```
PS C:\> Get-AzureRemoteAppVNet -VNetName "ContosoVNet"
```

Esse comando obtém informações sobre a rede virtual chamada ContosoVNet.

## OS

### -IncludeSharedKey
Indica que esse cmdlet inclui o valor da chave compartilhada nas informações que ele recupera sobre a rede virtual.

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

### -VNetName
Especifica o nome da rede virtual do Azure RemoteApp.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: True
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

## INFORMA

## LINKS RELACIONADOS

[Set-AzureRemoteAppVNet](./Set-AzureRemoteAppVNet.md)


