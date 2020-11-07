---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 51A1B699-03F6-4BB9-9186-FDFFB094F16A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 72420272e04519fa888660f8ccb6d432ecb0ee5d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946375"
---
# Enable-AzureTrafficManagerProfile

## Sinopse
Habilita um perfil do Gerenciador de tráfego.

## SYNTAX

```
Enable-AzureTrafficManagerProfile -Name <String> [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Enable-AzureTrafficManagerProfile** habilita um perfil do Gerenciador de tráfego do Microsoft Azure.
Especifique o parâmetro *PassThru* para exibir se a operação foi bem-sucedida.

## EXEMPLOS

### Exemplo 1: habilitar um perfil do Gerenciador de tráfego
```
PS C:\>Enable-AzureTrafficManagerProfile -Name "MyProfile"
```

Esse comando habilita o perfil do Gerenciador de tráfego chamado MyProfile.

### Exemplo 2: habilitar um perfil do Gerenciador de tráfego e exibir os resultados
```
PS C:\>Enable-AzureTrafficManagerProfile -Name "MyProfile" -PassThru
True
```

Esse comando habilita o perfil do Gerenciador de tráfego chamado MyProfile e exibe se o comando foi bem-sucedido.

## OS

### -Nome
Especifica o nome do perfil do Gerenciador de tráfego a ser habilitado.

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

[Disable-AzureTrafficManagerProfile](./Disable-AzureTrafficManagerProfile.md)

[Get-AzureTrafficManagerProfile](./Get-AzureTrafficManagerProfile.md)

[New-AzureTrafficManagerProfile](./New-AzureTrafficManagerProfile.md)

[Remove-AzureTrafficManagerProfile](./Remove-AzureTrafficManagerProfile.md)

[Set-AzureTrafficManagerProfile](./Set-AzureTrafficManagerProfile.md)


