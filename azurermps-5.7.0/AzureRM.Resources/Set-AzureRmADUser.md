---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 388D4173-A937-42FA-81CB-C4A27F9D0B04
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADUser.md
ms.openlocfilehash: 325f134baf860b728aec3f144d9c9cf455c6b4ce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93426619"
---
# Set-AzureRmADUser

## Sinopse
Atualiza um usuário existente do Active Directory.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Set-AzureRmADUser -UPNOrObjectId <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
Atualiza um usuário existente do Active Directory (conta corporativa/de estudante também conhecida como identificação da organização).
Para obter mais informações: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser

## EXEMPLOS

### Exemplo 1
```
PS C:\> {{ Add example code here }}
```

{{Adicionar exemplo de descrição aqui}}

## OS

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure

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

### -DisplayName
Novo nome para exibir no catálogo de endereços do usuário.
Exemplo-'Alex Wu '.

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

### -EnableAccount
Verdadeiro para habilitar a conta; caso contrário, false.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ForceChangePasswordNextLogin
Ele deve ser especificado somente quando você estiver atualizando a senha.
Caso contrário, ele será ignorado.
Ele deve ser especificado se o usuário precisar alterar a senha no próximo login bem-sucedido (verdadeiro).
O comportamento padrão é (falso) para não alterar a senha no próximo logon bem-sucedido.

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

### -Senha
Nova senha para o usuário.
Ele deve atender aos requisitos de complexidade da senha do locatário.
É recomendável definir uma senha forte.

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UPNOrObjectId
O nome UPN do usuário (por exemplo, ' someuser@contoso.com ') ou o ObjectID do usuário para o qual as propriedades precisam ser atualizadas.

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

### -Confirme
Solicita confirmação antes de executar o cmdlet.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
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

### Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmADUser](./Get-AzureRmADUser.md)

[New-AzureRmADUser](./New-AzureRmADUser.md)

[Remove-AzureRmADUser](./Remove-AzureRmADUser.md)

