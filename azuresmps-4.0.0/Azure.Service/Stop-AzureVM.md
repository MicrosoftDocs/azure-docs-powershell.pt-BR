---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 4F347DD1-907C-47DB-8F1D-636DE031A56A
online version: ''
schema: 2.0.0
ms.openlocfilehash: e01265cf3db8a0dc3fd9d74a4a263a20965b10fb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945741"
---
# Stop-AzureVM

## Sinopse
Desliga uma máquina virtual do Azure.

## SYNTAX

### ByName (padrão)
```
Stop-AzureVM [-Name] <String[]> [-StayProvisioned] [-Force] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### Contribuição
```
Stop-AzureVM -VM <IPersistentVM[]> [-StayProvisioned] [-Force] [-ServiceName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Stop-AzureVM** desliga uma máquina virtual.

## EXEMPLOS

### Exemplo 1: desligar uma máquina virtual
```
PS C:\> Stop-AzureVM -ServiceName "ContosoService01" -Name "MyVM"
```

Esse comando desliga uma máquina virtual que o serviço especificado contém.

### Exemplo 2: desligar uma máquina virtual usando um objeto de máquina virtual
```
PS C:\> Get-AzureVM -ServiceName "ContosoService01" -Name "MyVM" | Stop-AzureVM
```

Esse comando desliga uma máquina virtual que o serviço especificado contém, usando o objeto da máquina virtual que **Get-AzureVM** retorna.

### Exemplo 3: encerrar uma VM e manter a VM provisionada
```
PS C:\> Stop-AzureVM -ServiceName "ContosoService01" -Name "MyVM" -StayProvisioned
```

Esse comando desliga uma máquina virtual que o serviço especificado contém e o mantém provisionado.

### Exemplo 4: encerrar uma VM e permitir a desalocação da última VM na implantação
```
PS C:\> Stop-AzureVM -ServiceName "ContosoService01" -Name "MyVM" -Force
```

Esse comando desliga uma máquina virtual que o serviço especificado contém e permite a desalocação da última máquina virtual na implantação.

### Exemplo 5: desligar várias VMs
```
PS C:\> Stop-AzureVM -ServiceName "PSTestService" -Name "*" -Force
```

Esse comando desliga várias máquinas virtuais que o serviço especificado contém.

## OS

### -Force
Especifica se a desalocação da última máquina virtual em uma implantação deve ser permitida.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
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

### -Nome
Especifica o nome da máquina virtual a ser encerrada.

Use o caractere curinga para parar várias máquinas virtuais de forma assíncrona.
Com um caractere curinga, esse cmdlet chama a operação de funções de desligamento https://msdn.microsoft.com/en-us/library/azure/dn469421.aspx ( https://msdn.microsoft.com/en-us/library/azure/dn469421.aspx) , em vez da operação de função de desligamento https://msdn.microsoft.com/en-us/library/azure/jj157195.aspx ( https://msdn.microsoft.com/en-us/library/azure/jj157195.aspx) .

```yaml
Type: String[]
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
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

### -ServiceName
Especifica o nome do serviço do Azure que contém a máquina virtual a ser encerrada.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StayProvisioned
Especifica que esse cmdlet mantém a máquina virtual provisionada.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
Especifica um objeto de máquina virtual que identifica a máquina virtual para desligar.

```yaml
Type: IPersistentVM[]
Parameter Sets: Input
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

## INFORMA

## LINKS RELACIONADOS

[Get-AzureVM](./Get-AzureVM.md)

[New-AzureVM](./New-AzureVM.md)

[Restart-AzureVM](./Restart-AzureVM.md)

[Start-AzureVM](./Start-AzureVM.md)


