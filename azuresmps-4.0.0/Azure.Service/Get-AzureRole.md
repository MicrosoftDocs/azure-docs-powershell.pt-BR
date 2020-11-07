---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7C50472E-CE36-4BF1-92C9-A3B9B183ACD1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 929b439c58c344a1902c497bbad6e056e3755025
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946314"
---
# Get-AzureRole

## Sinopse
Retorna uma lista de funções no seu serviço do Microsoft Azure.

## SYNTAX

```
Get-AzureRole [-ServiceName] <String> [[-Slot] <String>] [[-RoleName] <String>] [-InstanceDetails]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureRole** retorna um objeto List com detalhes sobre as funções em seu serviço do Microsoft Azure.
Se você especificar o parâmetro *roleName* , **Get-AzureRole** retornará detalhes sobre essa função apenas.
Se você especificar o parâmetro *InstanceDetails* , detalhes adicionais específicos da instância serão retornados.

## EXEMPLOS

### Exemplo 1: obter uma lista de funções para um serviço
```
PS C:\> Get-AzureRole -ServiceName "MySvc01" -Slot "Production"
```

Esse comando retorna um objeto com detalhes sobre todas as funções de produção em execução no serviço MySvc01.

### Exemplo 2: obter detalhes sobre uma função em execução em um serviço
```
PS C:\> Get-AzureRole -ServiceName "MySvc1" -Slot "Staging" -RoleName "MyTestVM3"
```

Esse comando retorna um objeto com detalhes na função MyTestVM3, em execução no ambiente de preparo do serviço MySvc01.

### Exemplo 3: obter informações de instância sobre instâncias de uma função em execução em um serviço
```
PS C:\> Get-AzureRole -ServiceName "MySvc01" -Slot "Production" -RoleName "MyTestVM02" -InstanceDetails
```

Esse comando retorna um objeto com detalhes nas instâncias da função MyTestVM02 em execução no ambiente de produção do serviço MySvc01.

### Exemplo 4: obter uma tabela das instâncias de função associadas a um serviço
```
PS C:\> Get-AzureRole -ServiceName "MySvc01" -Slot "Production" -InstanceDetails | Format-Table -Auto "InstanceName", "InstanceSize", "InstanceStatus"
```

Esse comando retorna uma tabela do nome da instância, tamanho e status de todas as instâncias de função em execução no ambiente de produção no serviço MySvc01.

## OS

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

### -InstanceDetails
Especifica que esse cmdlet retorna detalhes sobre as instâncias em cada função.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
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

### -RoleName
Especifica o nome da função a ser obtida.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceName
Especifica o nome do serviço do Azure.

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

### -Slot
Especifica o ambiente de implantação do Azure.
Os valores aceitáveis para esse parâmetro são: produção ou preparação.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
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

[Set-AzureRole](./Set-AzureRole.md)


