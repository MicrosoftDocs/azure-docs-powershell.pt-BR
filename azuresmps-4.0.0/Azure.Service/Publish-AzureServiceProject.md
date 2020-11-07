---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: CF7E7C62-88FC-48CA-940F-9A6C7442BEF2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8166cd3faa951171dd3ac865b17b8a03bcefdd45
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945883"
---
# Publish-AzureServiceProject

## Sinopse
Publicar o serviço atual para o Windows Azure.

## SYNTAX

### PublishFromServiceDefinition (padrão)
```
Publish-AzureServiceProject [-ServiceName <String>] [-StorageAccountName <String>] [-Location <String>]
 [-Slot <String>] [-Launch] [-AffinityGroup <String>] [-DeploymentName <String>] [-ForceUpgrade]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### PublishFromPackage
```
Publish-AzureServiceProject [-Package <String>] -Configuration <String> [-StorageAccountName <String>]
 [-Location <String>] [-Slot <String>] [-Launch] [-AffinityGroup <String>] [-DeploymentName <String>]
 [-ForceUpgrade] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.
Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .

O cmdlet **Publish-AzureServiceProject** publica o serviço atual para a nuvem.
Você pode especificar a configuração de publicação (como **assinatura** , **StorageAccountName** , **local** , **slot** ) na linha de comando ou em configurações locais por meio do cmdlet **set-AzureServiceProject** .

## EXEMPLOS

### Exemplo 1: publicar um projeto de serviço com valores padrão
```
PS C:\> Publish-AzureServiceProject
```

Este exemplo publica o serviço atual, usando as configurações de serviço atuais e o perfil de publicação atual do Azure.

### Exemplo 2: criar um pacote de implantação
```
PS C:\> Publish-AzureServiceProject -PackageOnly
```

Este exemplo cria um arquivo de pacote de implantação (. cspkg) no diretório de serviço e não publica no Windows Azure.

## OS

### -AffinityGroup
Especifica o grupo de afinidade que você deseja que o serviço use.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Configuração
Especifica o arquivo de configuração do serviço.
Se você especificar esse parâmetro, especifique o parâmetro *Package* .

```yaml
Type: String
Parameter Sets: PublishFromPackage
Aliases: cc

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Deploymentname
Especifica o nome da implantação.

```yaml
Type: String
Parameter Sets: (All)
Aliases: dn

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ForceUpgrade
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: f

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Iniciar
Abre uma janela do navegador para que você possa exibir o aplicativo após a implantação.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: ln

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Local
A região na qual o aplicativo será hospedado.
Os valores possíveis são: 
  
- Qualquer lugar da Ásia
- Em qualquer lugar da Europa
- Em qualquer lugar nos EUA
- Leste da Ásia
- Leste dos EUA
- Centro Norte dos EUA
- Norte da Europa
- Centro-Sul dos EUA
- Sudeste Asiático
- Oeste da Europa
- Oeste dos EUA
 
Se não for especificada nenhuma localização, o local especificado na última chamada a **set-AzureServiceProject** será usado. Se nenhum local for especificado, o local será escolhido aleatoriamente nos locais ' centro-norte-americano ' e ' centro-sul '.

```yaml
Type: String
Parameter Sets: (All)
Aliases: l

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Package
Especifica o arquivo de pacote a ser implantado.
Especifique um arquivo local que tenha a extensão de nome de arquivo. cspkg ou um URI de um blob que contenha o pacote.
Se você especificar esse parâmetro, não especifique o parâmetro *ServiceName* .

```yaml
Type: String
Parameter Sets: PublishFromPackage
Aliases: sp

Required: False
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

### -ServiceName
Especifica o nome a ser usado para o serviço durante a publicação no Windows Azure.
O nome determina parte da etiqueta no subdomínio cloudapp.net que é usado para endereçar o serviço quando hospedado no Windows Azure (ou seja, **Name**. cloudapp.net).
Qualquer nome especificado durante a publicação do serviço substitui o nome dado quando o serviço foi criado.
(Consulte o cmdlet **New-AzureServiceProject** ).

```yaml
Type: String
Parameter Sets: PublishFromServiceDefinition
Aliases: sv

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Slot
O slot de implantação a ser usado para este serviço.
Os valores possíveis são ' preparação ' e ' produção '.
Se nenhum slot for especificado, o slot fornecido na última chamada para Set-AzureDeploymentSlot será usado.
Se nenhum slot for especificado, o slot ' produção ' será usado.

```yaml
Type: String
Parameter Sets: (All)
Aliases: sl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountName
Especifica o nome da conta de armazenamento do Windows Azure a ser usado durante a publicação do serviço.
Esse valor não é usado até que o serviço seja publicado.
Quando esse parâmetro não é especificado, o valor é obtido do último comando **set-AzureServiceProject** .
Se nenhuma conta de armazenamento for especificada, uma conta de armazenamento correspondente ao nome do serviço será usada.
Se não houver tal conta de armazenamento, o cmdlet tentará criar uma nova.
No entanto, a tentativa poderá falhar se uma conta de armazenamento que corresponda ao nome do serviço existir em outra assinatura.

```yaml
Type: String
Parameter Sets: (All)
Aliases: st

Required: False
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

[Enable-AzureServiceProjectRemoteDesktop](./Enable-AzureServiceProjectRemoteDesktop.md)

[Set-AzureServiceProject](./Set-AzureServiceProject.md)


