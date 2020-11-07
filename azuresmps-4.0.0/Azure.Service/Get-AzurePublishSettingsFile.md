---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: A5419F76-B85E-445D-84EA-CC695B175C8D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1364cf1bbec1fdca2a8c9901556d38de0b620358
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945633"
---
# Get-AzurePublishSettingsFile

## Sinopse
Baixa o arquivo de configurações de publicação para uma assinatura do Azure.

## SYNTAX

```
Get-AzurePublishSettingsFile [-Environment <String>] [-Realm <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzurePublishSettingsFile** faz o download de um arquivo de configurações de publicação para uma assinatura na sua conta.
Quando o comando é concluído, você pode usar o cmdlet **Import-PublishSettingsFile** para fazer as configurações no arquivo disponíveis para o Windows PowerShell.

Para disponibilizar sua conta do Azure para o Windows PowerShell, você pode usar um arquivo de configurações de publicação ou o cmdlet **Add-AzureAccount** .
Os arquivos de configurações de publicação permitem que você prepare a sessão antecipadamente para poder executar scripts e trabalhos em segundo plano autônomos.
No entanto, nem todos os serviços dão suporte a arquivos de configurações de publicação.
Por exemplo, o módulo **AzureResourceManager** não dá suporte a arquivos de configurações de publicação.

Quando você executa o **Get-AzurePublishSettingsFile** , ele abre o navegador padrão e solicita que você entre na sua conta do Azure, selecione uma assinatura e selecione um local do sistema de arquivos para o arquivo de configurações de publicação.
Em seguida, ele baixa o arquivo de configurações de publicação para a sua assinatura no arquivo que você selecionou.

Um "arquivo de configurações de publicação" é um arquivo XML com uma extensão de nome de arquivo. publishsettings.
O arquivo contém um certificado codificado que fornece credenciais de gerenciamento para suas assinaturas do Azure.

**Observação de segurança:** Os arquivos de configurações de publicação contêm credenciais usadas para administrar suas assinaturas e serviços do Azure.
Se usuários mal-intencionados acessarem o arquivo de configurações de publicação, poderão editar, criar e excluir seus serviços do Azure.
Como prática recomendada de segurança, salve o arquivo em um local na sua pasta downloads ou documentos e, em seguida, exclua-o depois de usar o cmdlet **Import-AzurePublishSettingsFile** para importar as configurações.

Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.
Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .

## EXEMPLOS

### Exemplo 1: baixar um arquivo de configurações de publicação
```
PS C:\> Get-AzurePublishSettingsFile
```

Esse comando abre o navegador padrão, se conecta à sua conta do Windows Azure e, em seguida, baixa o arquivo. publishsettings para a sua conta.

### Exemplo 2: especificar um território
```
PS C:\> Get-AzurePublishSettingsFile -Realm contoso.com -Passthru
```

Esse comando baixa o arquivo de configurações de publicação de uma conta no domínio contoso.com.
Use um comando com o parâmetro de **território** quando você se conectar ao Azure com uma conta organizacional, em vez de uma conta da Microsoft.

## OS

### -Ambiente
Especifica um ambiente do Azure.

Um ambiente do Azure uma implantação independente do Microsoft Azure, como o AzureCloud para global Azure e o AzureChinaCloud para Azure operado pela 21Vianet na China.
Você também pode criar ambientes do Azure locais usando o Azure Pack e os cmdlets do WAPack.
Para obter mais informações, consulte [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .

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

### -PassThru
Retorna $True se o comando tiver êxito e $False se falhar.
Por padrão, esse cmdlet não retorna nenhuma saída.

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

### -Perfil
Especifica o perfil do Azure do qual este cmdlet lê. Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.

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

### -Território
Especifica a organização em uma ID organizacional.
Por exemplo, se você se conectar ao Azure como admin@contoso.com , o valor do parâmetro de **território** será contoso.com.
Use esse parâmetro quando usar uma ID da organização para entrar no portal do Azure.
Esse parâmetro não é necessário quando você usa uma conta da Microsoft, como uma conta do outlook.com ou do live.com.

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
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma
Você pode canalizar a entrada para esse cmdlet pelo nome da propriedade, mas não por valor.

## EXIBE

### None ou System. Boolean
Quando você usa o parâmetro *PassThru* , esse cmdlet retorna um valor booliano.
Caso contrário, esse cmdlet não retorna nenhuma saída

## INFORMA

## LINKS RELACIONADOS

[Add-AzureAccount](./Add-AzureAccount.md)

[Import-AzurePublishSettingsFile](./Import-AzurePublishSettingsFile.md)


