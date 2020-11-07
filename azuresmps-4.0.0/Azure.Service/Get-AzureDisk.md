---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 95DCD2EC-8327-4A46-B624-289D0A28F7EA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4614910b8c0ccd36bb8ef75ee98f662cf69a276a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946354"
---
# Get-AzureDisk

## Sinopse
Obtém informações sobre discos no repositório de discos do Azure.

## SYNTAX

```
Get-AzureDisk [[-DiskName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureDisk** Obtém informações sobre os discos que são armazenados no repositório de discos do Azure para a assinatura atual.
Esse cmdlet retorna uma lista de informações para todos os discos no repositório.
Para ver as informações de um disco específico, especifique o nome do disco.

## EXEMPLOS

### Exemplo 1: obter informações sobre um disco
```
PS C:\> Get-AzureDisk -DiskName "ContosoDataDisk"
```

Este comando obtém dados de informações sobre o disco chamado ContosoDataDisk do repositório de discos.

### Exemplo 2: obter informações sobre todos os discos
```
PS C:\> Get-AzureDisk
```

Esse comando obtém informações sobre todos os discos no repositório de discos.

### Exemplo 3: obter informações sobre um disco
```
PS C:\> Get-AzureDisk | Where-Object {$_.AttachedTo -eq $Null } | Format-Table -AutoSize -Property "DiskName","DiskSizeInGB","MediaLink"
```

Esse comando obtém dados de todos os discos no repositório de disco que não estão atualmente conectados a uma máquina virtual.
O comando obtém informações sobre todos os discos e passa cada objeto para o cmdlet **Where-Object** .
Esse cmdlet descartará qualquer disco que não tenha um valor de $Null para a propriedade **Attachedto** .
O comando formata a lista como uma tabela usando o cmdlet **Format-Table** .

## OS

### -Diskname
Especifica o nome do disco no repositório de disco sobre o qual esse cmdlet obtém informações.

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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

## INFORMA

## LINKS RELACIONADOS

[Add-AzureDisk](./Add-AzureDisk.md)

[Remove-AzureDisk](./Remove-AzureDisk.md)

[Update-AzureDisk](./Update-AzureDisk.md)


