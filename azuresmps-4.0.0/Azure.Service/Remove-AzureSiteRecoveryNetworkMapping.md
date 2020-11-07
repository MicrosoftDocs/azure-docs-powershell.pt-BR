---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: BB36A434-6BE3-46BF-B10A-FCD6C766CB84
online version: ''
schema: 2.0.0
ms.openlocfilehash: 87414a56778123053615bb36a06113e2b0b0633f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946110"
---
# Remove-AzureSiteRecoveryNetworkMapping

## Sinopse
Remove um mapeamento de rede de um cofre de recuperação de site.

## SYNTAX

```
Remove-AzureSiteRecoveryNetworkMapping -NetworkMapping <ASRNetworkMapping> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Remove-AzureSiteRecoveryNetworkMapping** remove um mapeamento de rede do cofre do Azure site Recovery atual.

## EXEMPLOS

### Exemplo 1: remover o mapeamento entre uma rede e uma rede de recuperação
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $NetworkMapping = Get-AzureSiteRecoveryNetworkMapping -PrimaryServer $Servers[0] -RecoveryServer $Servers[0]
PS C:\> Remove-AzureSiteRecoveryNetworkMapping -NetworkMapping $NetworkMapping
```

O primeiro cmdlet de comando obtém servidores para o cofre do Azure site Recovery atual usando o cmdlet **Get-AzureSiteRecoveryServer** .
O comando armazena os servidores de recuperação de site na variável de matriz de $Servers.

O segundo comando obtém o mapeamento entre a rede principal e a rede de recuperação e, em seguida, armazena-a na variável $NetworkMapping.
O comando especifica o servidor primário para o mapeamento de rede como o primeiro elemento de $Servers.
O comando especifica o servidor para a rede de recuperação como o segundo elemento de $Servers.

O comando final remove o mapeamento de rede em $NetworkMapping.

### Exemplo 2: remover o mapeamento entre uma rede e uma rede de máquina virtual do Azure
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $NetworkMapping = Get-AzureSiteRecoveryNetworkMapping -PrimaryServer $Servers[0] -Azure
PS C:\> Remove-AzureSiteRecoveryNetworkMapping -NetworkMapping $NetworkMapping
```

O primeiro cmdlet de comando obtém servidores para o cofre de recuperação de site atual.
O comando armazena os servidores de recuperação de site na variável de matriz de $Servers.

O segundo comando obtém um mapeamento entre a rede principal e uma rede de máquina virtual do Azure e, em seguida, armazena-a na variável $NetworkMapping.
O comando especifica o servidor primário da rede como o primeiro elemento de $Servers.
O comando especifica o parâmetro *do Azure* .
Portanto, o comando obtém o mapeamento para uma rede de máquina virtual do Azure.

O comando final remove o mapeamento de rede em $NetworkMapping.

## OS

### -NetworkMapping
Especifica o mapeamento de rede a ser removido.

```yaml
Type: ASRNetworkMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

## INFORMA

## LINKS RELACIONADOS

[Get-AzureSiteRecoveryNetworkMapping](./Get-AzureSiteRecoveryNetworkMapping.md)

[New-AzureSiteRecoveryNetworkMapping](./New-AzureSiteRecoveryNetworkMapping.md)

[Get-AzureSiteRecoveryServer](./Get-AzureSiteRecoveryServer.md)


