---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 64EF867E-5142-4317-9552-8BC94117208D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 899ecd0256bc3d6f88b8f942fa488db444a9bb41
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946066"
---
# Set-AzureDataDisk

## Sinopse
Modifica o cache do host de um disco de dados existente em uma máquina virtual do Azure.

## SYNTAX

### NoResize
```
Set-AzureDataDisk [-HostCaching] <String> [-LUN] <Int32> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### Dimensiona
```
Set-AzureDataDisk [-DiskName] <String> [-ResizedSizeInGB] <Int32> -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzureDataDisk** modifica os atributos de cache de um disco de dados existente em uma máquina virtual do Azure.
Especifique qual disco de dados atualizar por seu número de unidade lógica (LUN).

## EXEMPLOS

### Exemplo 1: modificar o cache do host para um disco de dados
```
PS C:\> Get-AzureVM "ContosoService" | Set-AzureDataDisk -VM "VirtualMachine07" -LUN 2 -HostCaching ReadOnly | Update-AzureVM
```

Esse comando obtém as máquinas virtuais executadas no serviço denominado ContosoService usando o cmdlet **Get-AzureVM** .
O comando passa a ele para o cmdlet atual usando o operador pipeline.
Esse cmdlet define o disco de dados na LUN 2 da máquina virtual nomeada VirtualMachine07 para usar o cache do host ReadOnly.
O comando atualiza a máquina virtual para refletir suas alterações usando o cmdlet **Update-AzureVM** .

### Exemplo 2: modificar o cache do host para todos os discos de dados em uma máquina virtual
```
PS C:\> Get-AzureVM "ContosoService" -Name "VirtualMachine07" | Get-AzureDataDisk | Set-AzureDataDisk -HostCaching ReadWrite | Update-AzureVM
```

Esse comando obtém um objeto para a máquina virtual nomeada VirtualMachine07 no serviço na nuvem do ContosoService.
O comando a passa para o cmdlet **Get-AzureDataDisk** , que obtém os discos de dados dessa máquina virtual.
Em seguida, o cmdlet atual define o modo de cache do host de cada disco de dados como ReadWrite.
O comando atualiza a máquina virtual para refletir suas alterações.

## OS

### -Diskname
Especifica o nome da configuração de disco de dados que esse cmdlet modifica.

```yaml
Type: String
Parameter Sets: Resize
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HostCaching

> [!WARNING]
> O cache de disco não é compatível com os discos 4 a TiB e maiores. Se vários discos estiverem conectados à sua VM, cada disco menor do que 4 TiB será compatível com o cache.
>
> Alterar a configuração do cache de um disco do Azure desconecta e anexa novamente o disco de destino. Se for o disco do sistema operacional, a VM será reiniciada. Pare todos os aplicativos/serviços que possam ser afetados por essa interrupção antes de alterar a configuração do cache de disco. Não seguir essas recomendações pode levar à corrupção de dados.

Especifica as configurações de cache do nível do host do disco.
Os valores válidos são:

- Nenhuma
- ReadOnly
- Leitura

```yaml
Type: String
Parameter Sets: NoResize
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
Especifica o LUN para a unidade de dados na máquina virtual.
Os valores válidos são: de 0 a 15.

```yaml
Type: Int32
Parameter Sets: NoResize
Aliases:

Required: True
Position: 1
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

### -ResizedSizeInGB
Especifica o novo tamanho, em gigabytes, para o disco de dados.
O novo tamanho deve ser maior do que o tamanho atual.

```yaml
Type: Int32
Parameter Sets: Resize
Aliases:

Required: True
Position: 4
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

[Get-AzureVM](./Get-AzureVM.md)

[Get-AzureDataDisk](./Get-AzureDataDisk.md)

[Remove-AzureDataDisk](./Remove-AzureDataDisk.md)

[Update-AzureVM](./Update-AzureVM.md)


