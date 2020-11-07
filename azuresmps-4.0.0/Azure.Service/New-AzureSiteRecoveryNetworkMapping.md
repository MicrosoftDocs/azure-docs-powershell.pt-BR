---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 6802F2E9-5925-4E92-AEB8-827B5A303617
online version: ''
schema: 2.0.0
ms.openlocfilehash: 153e30c03de7a0a5c404526bd06b9acb2f0678f3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946217"
---
# New-AzureSiteRecoveryNetworkMapping

## Sinopse
Cria um mapeamento entre redes virtuais.

## SYNTAX

### EnterpriseToEnterprise
```
New-AzureSiteRecoveryNetworkMapping -PrimaryNetwork <ASRNetwork> -RecoveryNetwork <ASRNetwork>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### EnterpriseToAzure
```
New-AzureSiteRecoveryNetworkMapping -PrimaryNetwork <ASRNetwork> -AzureSubscriptionId <String>
 -AzureVMNetworkId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzureSiteRecoveryNetworkMapping** cria um mapeamento entre duas redes virtuais e retorna um trabalho do Azure site Recovery para controlá-la.

## EXEMPLOS

### Exemplo 1: criar um mapeamento entre uma rede e uma rede de recuperação
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $Networks = Get-AzureSiteRecoveryNetwork -Server $Servers[0]
PS C:\> New-AzureSiteRecoveryNetworkMapping -PrimaryNetwork $Networks[0] -RecoveryNetwork $Networks[1]
```

O primeiro cmdlet de comando obtém servidores para o cofre do Azure site Recovery atual usando o cmdlet **Get-AzureSiteRecoveryServer** .
O comando armazena os servidores de recuperação de site na variável de matriz de $Servers.

O segundo comando obtém a rede de recuperação de site para o primeiro servidor na matriz $Servers usando o cmdlet **Get-AzureSiteRecoveryNetwork** .
O comando armazena as redes na variável $Networks.

O comando final cria um mapeamento entre a rede principal e a rede de recuperação.
O comando especifica a rede principal como o primeiro elemento de $Networks.
O comando especifica a rede de recuperação como o segundo elemento de $Networks.

## OS

### -AzureSubscriptionId
Especifica a ID da sua assinatura do Azure.

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AzureVMNetworkId
Especifica a ID de rede virtual do Azure.

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrimaryNetwork
Especifica o objeto de rede principal.

```yaml
Type: ASRNetwork
Parameter Sets: (All)
Aliases: 

Required: True
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

### -RecoveryNetwork
Especifica o objeto de rede de recuperação.

```yaml
Type: ASRNetwork
Parameter Sets: EnterpriseToEnterprise
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

## LINKS RELACIONADOS

[Get-AzureSiteRecoveryNetworkMapping](./Get-AzureSiteRecoveryNetworkMapping.md)

[Get-AzureSiteRecoveryServer](./Get-AzureSiteRecoveryServer.md)

[Remove-AzureSiteRecoveryNetworkMapping](./Remove-AzureSiteRecoveryNetworkMapping.md)


