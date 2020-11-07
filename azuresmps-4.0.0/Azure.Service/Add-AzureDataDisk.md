---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: FDEDBF4F-7507-43FF-A983-7E431C0C1950
online version: ''
schema: 2.0.0
ms.openlocfilehash: 967fbaf83efa12bd305fc9fe075a9abffdd62dc3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945735"
---
# Add-AzureDataDisk

## Sinopse
Adiciona um disco de dados a uma máquina virtual.

## SYNTAX

### CreateNew (padrão)
```
Add-AzureDataDisk [-CreateNew] [-DiskSizeInGB] <Int32> [-DiskLabel] <String> [-LUN] <Int32>
 [-MediaLocation <String>] [-HostCaching <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### Importações
```
Add-AzureDataDisk [-Import] [-DiskName] <String> [-LUN] <Int32> [-HostCaching <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### ImportFrom
```
Add-AzureDataDisk [-ImportFrom] [-DiskLabel] <String> [-LUN] <Int32> -MediaLocation <String>
 [-HostCaching <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Add-AzureDataDisk** adiciona um disco de dados novo ou existente a um objeto de máquina virtual do Azure.
Use o parâmetro *CreateNew* para criar um novo disco de dados que tenha um tamanho e um rótulo especificados.
Use o parâmetro de *importação* para anexar um disco existente do repositório de imagens.
Use o parâmetro *ImportFrom* para anexar um disco existente de um blob em uma conta de armazenamento.
Você pode especificar o modo de cache do host do disco de dados anexado.

## EXEMPLOS

### Exemplo 1: importar um disco de dados do repositório
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Add-AzureDataDisk -Import -DiskName "Disk68" -LUN 0 | Update-AzureVM
```

Este comando obtém um objeto de máquina virtual para a máquina virtual nomeada VirtualMachine07 no serviço de nuvem do ContosoService usando o cmdlet **Get-AzureVM** .
O comando passa a ele para o cmdlet atual usando o operador pipeline.
Esse comando anexa um disco de dados existente do repositório à máquina virtual.
O disco de dados tem um LUN de 0.
O comando atualiza a máquina virtual para refletir suas alterações usando o cmdlet **Update-AzureVM** .

### Exemplo 2: adicionar um novo disco de dados
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine08" | Add-AzureDataDisk -CreateNew -DiskSizeInGB 128 -DiskLabel "main" -LUN 0 | Update-AzureVM
```

Este comando obtém um objeto da máquina virtual para a máquina virtual chamada VirtualMachine08.
O comando a passa para o cmdlet atual.
Esse comando anexa um novo disco de dados chamado MyNewDisk. vhd.
O cmdlet cria o disco no contêiner VHDs na conta de armazenamento padrão da assinatura atual.
O comando atualiza a máquina virtual para refletir suas alterações.

### Exemplo 3: adicionar um disco de dados de um local especificado
```
PS C:\> Get-AzureVM "ContosoService" -Name "Database" | Add-AzureDataDisk -ImportFrom -MediaLocation "https://contosostorage.blob.core.windows.net/container07/Disk14.vhd" -DiskLabel "main" -LUN 0 | Update-AzureVM
```

Este comando obtém um objeto de máquina virtual para a máquina virtual nomeada banco de dados.
O comando a passa para o cmdlet atual.
Esse comando anexa um disco de dados existente chamado Disk14. vhd do local especificado.
O comando atualiza a máquina virtual para refletir suas alterações.

## OS

### -CreateNew
Indica que esse cmdlet cria um disco de dados.

```yaml
Type: SwitchParameter
Parameter Sets: CreateNew
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DiskLabel
Especifica o rótulo de disco para um novo disco de dados.

```yaml
Type: String
Parameter Sets: CreateNew, ImportFrom
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Diskname
Especifica o nome de um disco de dados no repositório de discos.

```yaml
Type: String
Parameter Sets: Import
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DiskSizeInGB
Especifica o tamanho do disco lógico, em gigabytes, para um novo disco de dados.

```yaml
Type: Int32
Parameter Sets: CreateNew
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HostCaching
Especifica as configurações de cache do nível do host do disco.
Os valores válidos são: 

- Nenhuma 
- ReadOnly 
- Leitura

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Importar
Indica que esse cmdlet importa um disco de dados existente do repositório de imagens.

```yaml
Type: SwitchParameter
Parameter Sets: Import
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ImportFrom
Indica que esse cmdlet importa um disco de dados existente de um blob em uma conta de armazenamento.

```yaml
Type: SwitchParameter
Parameter Sets: ImportFrom
Aliases: 

Required: True
Position: 0
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
Cada disco de dados deve ter um LUN exclusivo.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MediaLocation
Especifica o local do blob em uma conta de armazenamento do Azure na qual esse cmdlet armazena o disco de dados.
Se você não especificar um local, o cmdlet armazenará o disco de dados no contêiner VHDs na conta de armazenamento padrão para a assinatura atual.
Se um contêiner de VHDs não existir, o cmdlet criará um contêiner de VHDs.

```yaml
Type: String
Parameter Sets: CreateNew
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ImportFrom
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Especifica o objeto da máquina virtual para o qual esse cmdlet anexa um disco de dados.
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

[Get-AzureDataDisk](./Get-AzureDataDisk.md)

[Get-AzureVM](./Get-AzureVM.md)

[Remove-AzureDataDisk](./Remove-AzureDataDisk.md)

[Set-AzureDataDisk](./Set-AzureDataDisk.md)

[Update-AzureVM](./Update-AzureVM.md)


