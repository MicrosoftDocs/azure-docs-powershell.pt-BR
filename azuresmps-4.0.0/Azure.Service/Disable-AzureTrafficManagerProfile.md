---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: ECE9C2A6-7DA2-4477-B877-9970FBE26D7C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8f378cbf8926a650699ec50a2a0a42873dcb7528
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945693"
---
# Disable-AzureTrafficManagerProfile

## Sinopse
Desabilita um perfil do Gerenciador de tráfego.

## SYNTAX

```
Disable-AzureTrafficManagerProfile -Name <String> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Disable-AzureTrafficManagerProfile** desabilita um perfil do Gerenciador de tráfego do Microsoft Azure.
Você pode usar o parâmetro *PassThru* para exibir se a operação foi bem-sucedida.

## EXEMPLOS

### Exemplo 1: desabilitar um perfil do Gerenciador de tráfego e exibir os resultados
```
PS C:\>Disable-AzureTrafficManagerProfile -Name "MyProfile" -PassThru
True
```

Esse comando desabilita o perfil do Gerenciador de tráfego chamado MyProfile.
O comando especifica o parâmetro *PassThru* para exibir se o comando foi bem-sucedido.

### Exemplo 2: desabilitar um perfil do Gerenciador de tráfego e exibir nenhum resultado
```
PS C:\>Disable-AzureTrafficManagerProfile -Name "MyProfile"
```

Esse comando desabilita o perfil do Gerenciador de tráfego chamado MyProfile, mas não exibe se o comando foi bem-sucedido.

## OS

### -Nome
Especifica o nome do perfil do Gerenciador de tráfego a ser desabilitado.

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

### -PassThru
Retorna $True se a operação for bem-sucedida; caso contrário, $False.
Por padrão, esse cmdlet não gera nenhuma saída.

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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

### System. Boolean
Este cmdlet gera $True ou $False.
Se a operação for bem-sucedida e se você especificar o parâmetro *PassThru* , esse cmdlet retornará um valor de $true.

## INFORMA

## LINKS RELACIONADOS

[Enable-AzureTrafficManagerProfile](./Enable-AzureTrafficManagerProfile.md)

[Get-AzureTrafficManagerProfile](./Get-AzureTrafficManagerProfile.md)

[New-AzureTrafficManagerProfile](./New-AzureTrafficManagerProfile.md)

[Remove-AzureTrafficManagerProfile](./Remove-AzureTrafficManagerProfile.md)

[Set-AzureTrafficManagerProfile](./Set-AzureTrafficManagerProfile.md)


