---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2D09422F-82B1-4243-B835-8BF223A6F936
online version: ''
schema: 2.0.0
ms.openlocfilehash: a6f02f333601172341de4fe8a0bf629037f712a5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945975"
---
# New-AzureSiteRecoveryStorageMapping

## Sinopse
Cria um mapeamento entre um objeto de armazenamento do Azure e um objeto de armazenamento de recuperação.

## SYNTAX

```
New-AzureSiteRecoveryStorageMapping -PrimaryStorage <ASRStorage> -RecoveryStorage <ASRStorage>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **New-AzureSiteRecoveryStorageMapping** cria um mapeamento entre um objeto de armazenamento primário do Azure do Azure site Recovery e um objeto de armazenamento de recuperação.

## EXEMPLOS

### Exemplo 1: criar um mapeamento entre um objeto de armazenamento e um objeto de armazenamento de recuperação
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $Storages = Get-AzureSiteRecoveryStorage -Server $Servers[0]
PS C:\> New-AzureSiteRecoveryStorageMapping -PrimaryStorage $Storages[0] -RecoveryStorage $Storages[1]
```

O primeiro cmdlet de comando obtém servidores para o cofre do Azure site Recovery atual usando o cmdlet **Get-AzureSiteRecoveryServer** .
O comando armazena os servidores de recuperação de site na variável de matriz de $Servers.

O segundo comando obtém o armazenamento de recuperação do site para o primeiro servidor na matriz $Servers e, em seguida, armazena-o na $Storages.

O comando final cria um mapeamento entre a rede principal e a rede de recuperação.
O comando especifica o objeto de armazenamento principal como o primeiro elemento de $Storages.
O comando especifica o objeto de armazenamento de recuperação como o segundo elemento de $Storages.

## OS

### -PrimaryStorage
Especifica o armazenamento primário a ser mapeado para o armazenamento de recuperação.
Para obter um objeto **ASRStorage** , use o cmdlet Get-AzureSiteRecoveryStorage.

```yaml
Type: ASRStorage
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

### -RecoveryStorage
Especifica o objeto de armazenamento de recuperação.
Esse cmdlet mapeia o objeto de armazenamento principal para o objeto de armazenamento que esse parâmetro especifica.
Para obter um objeto **ASRStorage** , use **Get-AzureSiteRecoveryStorage**.

```yaml
Type: ASRStorage
Parameter Sets: (All)
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

[Get-AzureSiteRecoveryStorage](./Get-AzureSiteRecoveryStorage.md)

[Get-AzureSiteRecoveryStorageMapping](./Get-AzureSiteRecoveryStorageMapping.md)

[Remove-AzureSiteRecoveryStorageMapping](./Remove-AzureSiteRecoveryStorageMapping.md)


