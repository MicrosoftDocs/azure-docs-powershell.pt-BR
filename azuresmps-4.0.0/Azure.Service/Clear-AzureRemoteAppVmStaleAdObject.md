---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DA8EC1BD-1219-4B98-B661-40A28897271F
online version: ''
schema: 2.0.0
ms.openlocfilehash: dcbca5ab73d64bd0336f723d623c7f976237ecba
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945703"
---
# Clear-AzureRemoteAppVmStaleAdObject

## Sinopse
Remove objetos no Azure Active Directory associados a máquinas virtuais do Azure RemoteApp que não existem mais.

## SYNTAX

```
Clear-AzureRemoteAppVmStaleAdObject -CollectionName <String> [-Credential <PSCredential>]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Clear-AzureRemoteAppVmStaleAdObject** remove objetos do Azure Active Directory associados a máquinas virtuais do Azure RemoteApp que não existem mais.
Você deve usar credenciais que tenham direitos para remover objetos do Azure Active Directory.
Se você especificar o parâmetro Common *Verbose* , esse cmdlet exibirá o nome de cada objeto que ele excluir.

## EXEMPLOS

### Exemplo 1: limpar objetos obsoletos para uma coleção
```
PS C:\> $AdminCredentials = Get-Credential
PS C:\> Clear-AzureRemoteAppVmStaleAdObject -CollectionName "Contoso" -Credential $AdminCredentials
```

O primeiro comando solicita um nome de usuário e uma senha usando **Get-Credential**.
O comando armazena os resultados na variável $AdminCredentials.

O segundo comando limpa os objetos obsoletos da coleção chamada contoso.
O comando usa as credenciais armazenadas na variável $AdminCredentials.
Para que o comando tenha êxito, essas credenciais devem ter direitos apropriados.

## OS

### -CollectionName
Especifica o nome da coleção do Azure RemoteApp.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Credential
Especifica uma credencial que tem direitos para executar esta ação.
Para obter um objeto **PSCredential** , use o cmdlet **Get-Credential** .
Se você não especificar esse parâmetro, esse cmdlet usará as credenciais do usuário atual.

```yaml
Type: PSCredential
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

### -Confirme
Solicita confirmação antes de executar o cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra o que aconteceria se o cmdlet fosse executado.
O cmdlet não é executado.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRemoteAppVmStaleAdObject](./Get-AzureRemoteAppVmStaleAdObject.md)


