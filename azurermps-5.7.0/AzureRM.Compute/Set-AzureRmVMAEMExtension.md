---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 3B15C734-DF57-433A-8854-ACE2B35FF6CB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMAEMExtension.md
ms.openlocfilehash: edc91b756b90684299d84228c04862a0ce6c2e21
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426781"
---
# Set-AzureRmVMAEMExtension

## Sinopse
Habilita o suporte para monitoramento de sistemas SAP.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Set-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [-DisableWAD] [-EnableWAD]
 [[-WADStorageAccountName] <String>] [[-OSType] <String>] [-SkipStorage] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzureRmVMAEMExtension** atualiza a configuração de uma máquina virtual para habilitar ou atualizar o suporte para o monitoramento de sistemas SAP instalados na máquina virtual.
O cmdlet instala a extensão do Azure Enhanced Monitoring (AEM) que coleta os dados de desempenho e o torna detectável para o sistema SAP.

## EXEMPLOS

### Exemplo 1: usar a extensão do AEM
```
PS C:\> Set-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server" -WADStorageAccountName "stdstorage"
```

Este comando configura a máquina virtual chamada contoso-Server para usar a extensão do AEM.
O comando especifica a conta de armazenamento chamada stdstorage.

## OS

### -DisableWAD
Indica que esse cmdlet não habilita o diagnóstico do Azure para a máquina virtual.

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

### -EnableWAD
Se esse parâmetro for fornecido, o commandlet habilitará o diagnóstico do Windows Azure para esta máquina virtual.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -OSType
Especifica o tipo de sistema operacional do disco do sistema operacional.
Se o disco do sistema operacional não tiver um tipo, você deve especificar esse parâmetro.
Os valores aceitáveis para esse parâmetro são: Windows e Linux.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome do grupo de recursos da máquina virtual que esse cmdlet modifica.

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

### -SkipStorage
Indica que esse cmdlet ignora a configuração de armazenamento.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VMName
Especifica o nome de uma máquina virtual.
Esse cmdlet adiciona a extensão do AEM para a máquina virtual que esse parâmetro especifica.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WADStorageAccountName
Especifica o nome da conta de armazenamento que este cmdlet usa para configurar a extensão LinuxDiagnostics ou IaaSDiagnostics.
Se a máquina virtual não usar uma conta de armazenamento padrão, você deve especificar um valor para esse parâmetro.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma
Esse cmdlet não aceita nenhuma entrada.

## EXIBE

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmVMAEMExtension](./Get-AzureRmVMAEMExtension.md)

[Remove-AzureRmVMAEMExtension](./Remove-AzureRmVMAEMExtension.md)

[Test-AzureRmVMAEMExtension](./Test-AzureRmVMAEMExtension.md)


