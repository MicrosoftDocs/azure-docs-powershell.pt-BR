---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D563ACF6-6BCD-4463-8731-175BA047A74D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2ceb2af6b359d5b9660397ef654d6c56e045ce64
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946166"
---
# Remove-AzureDataDisk

## Sinopse
Remove um disco de dados de uma máquina virtual do Azure.

## SYNTAX

```
Remove-AzureDataDisk [-LUN] <Int32> [-DeleteVHD] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Remove-AzureDataDisk** remove um disco de dados de uma máquina virtual do Azure.
Por padrão, esse cmdlet não remove o blob do disco de dados da conta de armazenamento.

## EXEMPLOS

### Exemplo 1: remover um disco de dados
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Remove-AzureDataDisk -LUN 0
```

Esse comando obtém a máquina virtual chamada VirtualMachine07 no serviço chamado ContosoService usando o cmdlet **Get-AzureVM** .
O comando passa a máquina virtual para o cmdlet atual usando o operador pipeline.
O cmdlet atual remove o disco de dados que tem o LUN 0.

### Exemplo 2: remover um disco de dados e o arquivo de disco rígido virtual
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine07" | Remove-AzureDataDisk -LUN 0 -DeleteVHD | Update-AzureVM
```

Esse comando obtém a máquina virtual chamada VirtualMachine07 no serviço chamado ContosoService.
O comando passa a máquina virtual para o cmdlet atual.
O cmdlet atual remove o disco de dados que tem o LUN 0.
O comando inclui o parâmetro *DeleteVHD* .
Portanto, ele também exclui o disco rígido virtual subjacente.
O comando atualiza a máquina virtual para refletir suas alterações usando o cmdlet **Update-AzureVM** .

## OS

### -DeleteVHD
Indica que esse cmdlet Remove o disco de dados e o disco rígido virtual (VHD) do armazenamento BLOB.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
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

### -LUN
Especifica o número de unidade lógica (LUN) para a unidade de dados na máquina virtual.
Os valores válidos são: de 0 a 15.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
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

### -VM
Especifica o objeto da máquina virtual que está anexado ao disco de dados.
Para obter um objeto de máquina virtual, use o cmdlet **Get-AzureVM** .

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

## INFORMA

## LINKS RELACIONADOS

[Add-AzureDataDisk](./Add-AzureDataDisk.md)

[Get-AzureDataDisk](./Get-AzureDataDisk.md)

[Get-AzureVM](./Get-AzureVM.md)

[Set-AzureDataDisk](./Set-AzureDataDisk.md)

[Update-AzureVM](./Update-AzureVM.md)


