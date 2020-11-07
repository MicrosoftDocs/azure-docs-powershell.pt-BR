---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 79D64D7C-6671-4F03-8776-70A716F36512
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2bc0525ee7238de421842b74f52f7dd4fa59df1a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946261"
---
# Import-AzurePublishSettingsFile

## Sinopse
Importa um arquivo de configurações de publicação que permite que você gerencie suas contas do Azure no Windows PowerShell.

## SYNTAX

```
Import-AzurePublishSettingsFile -PublishSettingsFile <String> [-Environment <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Import-AzurePublishSettingsFile** importa um arquivo de configurações de publicação (*. publishsettings) que contém informações sobre suas contas do Azure e salva um arquivo de dados de assinatura em seu computador.
Quando o cmdlet é concluído, você pode gerenciar suas contas do Azure no Windows PowerShell.

Antes de executar **Import-AzurePublishSettingsFile** , execute **Get-AzurePublishSettingsFile** , que baixa e salva o arquivo de configurações de publicação para que você possa importá-lo.

Para disponibilizar sua conta do Azure para o Windows PowerShell, você pode usar um arquivo de configurações de publicação ou o cmdlet **Add-AzureAccount** .
Os arquivos de configurações de publicação permitem que você prepare a sessão antecipadamente para poder executar scripts e trabalhos em segundo plano autônomos.
No entanto, nem todos os serviços dão suporte a arquivos de configurações de publicação.
Por exemplo, o módulo **AzureResourceManager** não dá suporte a arquivos de configurações de publicação.

**Observação de segurança:** Os arquivos de configurações de publicação contêm um certificado de gerenciamento codificado, mas não criptografado.
Se usuários mal-intencionados acessarem o arquivo de configurações de publicação, eles poderão editar, criar e excluir seus serviços do Azure.
Como prática recomendada de segurança, salve o arquivo em um local na sua pasta downloads ou documentos e, em seguida, exclua-o depois de usar o cmdlet **Import-AzurePublishSettingsFile** para importar as configurações.

## EXEMPLOS

### Exemplo 1: importar um arquivo
```
PS C:\> Import-AzurePublishSettingsFile -PublishSettingsFile C:\Temp\MyAccount.publishsettings
```

Esse comando importa o arquivo "C:\Temp\MyAccount.publishsettings".

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
Accept pipeline input: False
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

### -PublishSettingsFile
```yaml
Type: String
Parameter Sets: (All)
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

### Nenhuma
Você pode canalizar a entrada para esse cmdlet pelo nome da propriedade, mas não por valor.

## EXIBE

### Nenhuma
Esse cmdlet não gera nenhuma saída.

## INFORMA
* Um "arquivo de configurações de publicação" é um arquivo XML com uma extensão de nome de arquivo. publishsettings. O arquivo contém um certificado codificado que fornece credenciais de gerenciamento para suas assinaturas do Azure. Depois de importar esse arquivo, exclua-o para evitar riscos de segurança.
* Um "arquivo de dados de assinatura" é um arquivo XML que pode ser salvo em seu computador com segurança. Por padrão, ele é salvo no perfil de usuário móvel ($home/AppData/Roaming).

## LINKS RELACIONADOS

[Como instalar e configurar o Azure PowerShell](https://azure.microsoft.com/documentation/articles/install-configure-powershell/)

[Add-AzureAccount](./Add-AzureAccount.md)

[Get-AzurePublishSettingsFile](./Get-AzurePublishSettingsFile.md)


