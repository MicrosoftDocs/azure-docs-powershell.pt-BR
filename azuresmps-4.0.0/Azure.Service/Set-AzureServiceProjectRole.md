---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 5D093C10-F8B6-4F4A-ABD7-CC4D7AB7AFFA
online version: ''
schema: 2.0.0
ms.openlocfilehash: c78f53b95d18de600535368a1109b318294928c3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945952"
---
# Set-AzureServiceProjectRole

## Sinopse
Define o número de instâncias ou a versão de tempo de execução de uma função.

## SYNTAX

### Instância
```
Set-AzureServiceProjectRole [-RoleName <String>] -Instances <Int32> [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### Classpath
```
Set-AzureServiceProjectRole [-RoleName <String>] -Runtime <String> -Version <String> [-PassThru]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### VMSize
```
Set-AzureServiceProjectRole [-RoleName <String>] [-PassThru] -VMSize <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## DESCRITIVO
Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.
Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .

O cmdlet **set-AzureServiceProjectRole** define o número de instâncias de função para a função especificada.

## EXEMPLOS

### Exemplo 1: definir instâncias para uma função da Web
```
PS C:\> Set-AzureServiceProjectRole "MyWebRole" 2
```

Define o número de instâncias para a função da Web chamada MyWebRole1 para 2.

### Exemplo 2: definir instâncias para uma função de trabalhador
```
PS C:\> Set-AzureServiceProjectRole "MyWorkerRole1" 2
```

Define a contagem de instâncias de função para a função de trabalho chamada WorkerRole1 para 2.

### Exemplo 3: definir a versão do tempo de execução para um serviço de função
```
PS C:\> Set-AzureServiceProjectRole "MyRole1" node 0.6.20
```

Define a versão do node.exe Runtime para a função MyRole1 como 0.6.20.

## OS

### -Instâncias
Especifica o número de instâncias de função para a função de trabalho ou da Web especificada.

```yaml
Type: Int32
Parameter Sets: Instances
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Retorna um objeto que representa o item com o qual você está trabalhando.
Por padrão, esse cmdlet não gera nenhuma saída.

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

### -RoleName
Especifica o nome da função de trabalho ou Web a ser alterada.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Runtime
Especifica o tempo de execução para adicionar à função especificada.

```yaml
Type: String
Parameter Sets: Runtime
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Versão
Especifica a versão do tempo de execução para adicionar à função.

```yaml
Type: String
Parameter Sets: Runtime
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMSize
Especifica o tamanho da máquina virtual da função.

```yaml
Type: String
Parameter Sets: VMSize
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

###  
Especifica o tamanho da máquina virtual.

## EXIBE

## INFORMA

## LINKS RELACIONADOS

[Set-AzureServiceProject](./Set-AzureServiceProject.md)


