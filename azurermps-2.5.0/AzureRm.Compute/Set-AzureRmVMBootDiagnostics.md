---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 9A6F140C-9F1C-4701-9603-FC6107FCAF92
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmbootdiagnostics
schema: 2.0.0
ms.openlocfilehash: 2faa28fc0f0e4c27e384c178b96b8d38cae16a3d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786126"
---
# Set-AzureRmVMBootDiagnostics

## Sinopse
Modifica as propriedades de diagnóstico de inicialização de uma máquina virtual.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

### EnableBootDiagnostics
```
Set-AzureRmVMBootDiagnostics [-VM] <PSVirtualMachine> [-Enable] [-ResourceGroupName] <String>
 [[-StorageAccountName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### DisableBootDiagnostics
```
Set-AzureRmVMBootDiagnostics [-VM] <PSVirtualMachine> [-Disable] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzureRmVMBootDiagnostics** modifica as propriedades de diagnóstico de inicialização de uma máquina virtual.

## EXEMPLOS

### Exemplo 1: habilitar o diagnóstico de inicialização
```
PS C:\> $VM = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07"
PS C:\> Set-AzureRmVMBootDiagnostics -VM $VM -Enable -ResourceGroupName "ResourceGroup11" -StorageAccountName "DiagnosticStorage"
```

O primeiro comando obtém a máquina virtual chamada ContosoVM07 usando **Get-AzureRmVM**.
O comando o armazena na variável $VM.

O segundo comando habilita o diagnóstico de inicialização para a máquina virtual em $VM.
Os dados de diagnóstico são armazenados na conta especificada.

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Disable
Indica que esse cmdlet desabilita o diagnóstico de inicialização para a máquina virtual.

```yaml
Type: SwitchParameter
Parameter Sets: DisableBootDiagnostics
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Habilitar
Indica que esse cmdlet habilita o diagnóstico de inicialização para a máquina virtual.

```yaml
Type: SwitchParameter
Parameter Sets: EnableBootDiagnostics
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome do grupo de recursos da máquina virtual.

```yaml
Type: String
Parameter Sets: EnableBootDiagnostics
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountName
Especifica o nome da conta de armazenamento na qual os dados de diagnóstico de inicialização são salvos.

```yaml
Type: String
Parameter Sets: EnableBootDiagnostics
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Especifica a máquina virtual para a qual esse cmdlet altera o diagnóstico de inicialização.
Para obter um objeto de máquina virtual, use o cmdlet Get-AzureRmVM.

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### PSVirtualMachine
O parâmetro ' VM ' aceita o valor do tipo ' PSVirtualMachine ' do pipeline

## EXIBE

### Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmVM](./Get-AzureRmVM.md)

[Get-AzureRmVMBootDiagnosticsData](./Get-AzureRmVMBootDiagnosticsData.md)


