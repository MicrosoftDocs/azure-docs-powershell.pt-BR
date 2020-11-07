---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 42042533-9F84-4189-8C9F-01FD62F89DC3
online version: ''
schema: 2.0.0
ms.openlocfilehash: db14b17e42d23e481468f563768b606d8baa2802
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/08/2020
ms.locfileid: "93947406"
---
# Remove-WAPackVNet

## Sinopse
Remove os objetos de rede virtual.

## SYNTAX

```
Remove-WAPackVNet -VNet <VMNetwork> [-PassThru] [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
Esses tópicos são preteridos e serão removidos no futuro.
Este tópico descreve o cmdlet na versão 0.8.1 do módulo do Microsoft Azure PowerShell.
Para descobrir a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .

O cmdlet **Remove-WAPackVNet** remove objetos de rede virtual.

## EXEMPLOS

### Exemplo 1: remover uma rede virtualizada
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> Remove-WAPackVM -VNet $VNet
```

O primeiro comando obtém a rede virtualizada chamada ContosoVNet01 usando o cmdlet **Get-WAPackVNet** e armazena esse objeto na variável $VNet.
O segundo comando Remove a rede virtualizada armazenada em $VNet.
O comando solicitará confirmação.

### Exemplo 2: remover uma rede virtualizada sem confirmação
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet02"
PS C:\> Remove-WAPackVNet -VNet $VNet -Force
```

O primeiro comando obtém o serviço de nuvem chamado ContosoVNet02 usando o cmdlet **Get-WAPackVNet** e armazena esse objeto na variável $VNet.
O segundo comando Remove a rede virtualizada armazenada em $VNet.
Esse comando inclui o parâmetro *Force* .
O comando não solicita confirmação.

## OS

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

### -VNet
Especifica uma rede virtualizada.
Para obter uma rede virtualizada, use o cmdlet **Get-WAPackVNet** .

```yaml
Type: VMNetwork
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

## INFORMA

## LINKS RELACIONADOS

[Get-WAPackVNet](./Get-WAPackVNet.md)

[New-WAPackVNet](./New-WAPackVNet.md)


