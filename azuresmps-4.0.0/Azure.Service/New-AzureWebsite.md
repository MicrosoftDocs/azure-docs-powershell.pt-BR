---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: FBB55071-454D-4473-93BA-D97F33067785
online version: ''
schema: 2.0.0
ms.openlocfilehash: 768eff2dda32c6dfa0bad14f028338d3c5fa1abd
ms.sourcegitcommit: 87730c7ea4f98f628d3fe1b40aa4a9d2885e1c75
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/12/2021
ms.locfileid: "98110471"
---
# New-AzureWebsite

## SYNOPSIS
Crie um novo site para ser executado no Azure.

## SINTAXE

```
New-AzureWebsite [-Location <String>] [-Hostname <String>] [-PublishingUsername <String>] [-Git] [-GitHub]
 [-GitHubCredentials <PSCredential>] [-GitHubRepository <String>] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRIÇÃO
Este tópico descreve o cmdlet na versão 0.8.10 do módulo Microsoft Azure PowerShell.
Para obter a versão do módulo que você está usando, no console do Azure PowerShell, digite `(Get-Module -Name Azure).Version` .

O cmdlet cria um novo site para ser executado no Azure e se prepara para implantação por meio do GitHub.

## EXEMPLOS

### Exemplo 1: Criar um novo site com o Git
```
PS C:\> New-AzureWebsite mySite -Git
```

Este exemplo cria um novo site no Azure e um repositório git local a ser usado para implantar arquivos no novo site.

### Exemplo 2: Criar site integrado ao GitHub
```
PS C:\> New-AzureWebsite mysite -GitHub -GitHubRepository myaccount/myrepo
```

Este exemplo cria um novo site vinculado a um repositório do GitHub chamado myaccount/myrepo.
As confirmações no repositório do GitHub são adiadas para o site no Azure.

## PARÂMETROS

### -Git
Configura um repositório local do Git e o vincula ao site.
Se especificado, este parâmetro configura um repositório git no diretório local e adiciona um repositório remoto chamado 'azure' que se vincula ao site no Azure.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -GitHub
Indica que esse cmdlet vincula o novo site a um repositório existente do GitHub.
Confirmações para o repositório Giuthub são pressionadas para o site no Azure.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -GitHubCredentials
Especifica as credenciais de nome de usuário e senha para se conectar ao GitHub.

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -GitHubRepository
Especifica o nome completo do repositório do GitHub para vincular a este site.
Por exemplo, `myaccount/myrepo` .

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

### -Hostname
Especifica um nome de host alternativo para o novo site.

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

### -Location
Especifica o local do data center onde você deseja implantar o site.

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

### -Name
Especifica um nome para o site.

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

### -Profile
Especifica o perfil do Azure do qual este cmdlet lê.
Se você não especificar um perfil, este cmdlet lê do perfil padrão local.

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

### -PublishingUsername
Especifica o nome de usuário especificado na implantação do Portal do Azure para Git.

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

### -Slot
Especifica um nome de slot para o site.

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

### CommonParameters
Este cmdlet oferece suporte aos parâmetros comuns: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## ENTRADAS

## SAÍDAS

## OBSERVAÇÕES

## LINKS RELACIONADOS

[Set-AzureWebsite](./Set-AzureWebsite.md)


