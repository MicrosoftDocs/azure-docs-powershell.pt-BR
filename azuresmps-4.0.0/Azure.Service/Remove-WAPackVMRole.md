---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 9999E0EE-4A32-4C18-A6EC-2A073DC08710
online version: ''
schema: 2.0.0
ms.openlocfilehash: e5dfe0f42987ba51613ff9bafa000713456dfaf7
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/08/2020
ms.locfileid: "93947411"
---
# Remove-WAPackVMRole

## Sinopse
Remove objetos de função de máquina virtual.

## SYNTAX

### FromVMRoleObject (padrão)
```
Remove-WAPackVMRole -VMRole <VMRole> [-PassThru] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### FromCloudService
```
Remove-WAPackVMRole -VMRole <VMRole> -CloudServiceName <String> [-PassThru] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
Esses tópicos são preteridos e serão removidos no futuro.
Este tópico descreve o cmdlet na versão 0.8.1 do módulo do Microsoft Azure PowerShell.
Para descobrir a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .

O cmdlet **Remove-WAPackVMRole** remove objetos de função da máquina virtual.

## EXEMPLOS

### Exemplo 1: remover uma função de máquina virtual (que foi criada usando o portal de WAP)
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole01"
PS C:\> Remove-WAPackVMRole -VMRole $VMRole
```

O primeiro comando obtém a função da máquina virtual chamada ContosoVMRole01 usando o cmdlet **Get-WAPackVMRole** e armazena esse objeto na variável $VMRole.

O segundo comando Remove a função de máquina virtual armazenada em $VMRole.
O comando solicitará confirmação. Pressupondo que essa função da máquina virtual seja criada usando o portal de WAP, não é necessário especificar o nome do serviço de nuvem.

### Exemplo 2: remover uma função de máquina virtual que foi criada após a criação manual de um serviço na nuvem
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole02"
PS C:\> Remove-WAPackVMRole -VMRole $VMRole -CloudServiceName "ContosoCloudService02"
```

O primeiro comando obtém a função da máquina virtual chamada "ContosoVMRole02" usando o cmdlet **Get-WAPackVMRole** e armazena esse objeto na variável $VMRole.

O segundo comando Remove a função de máquina virtual armazenada em $VMRole.
O comando solicitará confirmação.
Pressupondo que essa função da máquina virtual não foi criada usando o portal, o usuário precisa especificar o nome do serviço de nuvem.
Nesse caso, chamado "ContosoCloudService02".

### Exemplo 3: remover uma função de máquina virtual sem confirmação
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole03"
PS C:\> Remove-WAPackVMRole -VMRole $VMRole -Force
```

O primeiro comando obtém o serviço de nuvem chamado ContosoVMRole03 usando o cmdlet **Get-WAPackVMRole** e armazena esse objeto na variável $VMRole.

O segundo comando Remove a função de máquina virtual armazenada em $VMRole.
Esse comando inclui o parâmetro *Force* .
O comando não solicita confirmação.

## OS

### -CloudServiceName
Especifica o nome do serviço em nuvem da função da máquina virtual.

```yaml
Type: String
Parameter Sets: FromCloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Força o comando a ser executado sem pedir confirmação do usuário.

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

### -VMRole
Especifica uma função de máquina virtual.
Para obter uma função de máquina virtual, use o cmdlet **Get-WAPackVMRole** .

```yaml
Type: VMRole
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Confirme
Solicita confirmação antes de executar o cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra o que aconteceria se o cmdlet fosse executado.
O cmdlet não é executado.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

## INFORMA

## LINKS RELACIONADOS

[Get-WAPackVMRole](./Get-WAPackVMRole.md)

[New-WAPackVMRole](./New-WAPackVMRole.md)

[Set-WAPackVMRole](./Set-WAPackVMRole.md)


