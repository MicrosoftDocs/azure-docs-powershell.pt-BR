---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 35FAA57F-B2BD-4E43-8238-12F7A8269E4D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: 1fbf5a5541fe3e1360e696f9c06a26d6ea131dc0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93439942"
---
# <span data-ttu-id="9e5c9-101">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="9e5c9-101">Remove-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="9e5c9-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9e5c9-102">SYNOPSIS</span></span>
<span data-ttu-id="9e5c9-103">Exclui um contato registrado para notificações de certificado de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="9e5c9-103">Deletes a contact that is registered for certificate notifications from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9e5c9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9e5c9-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e5c9-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="9e5c9-105">DESCRIPTION</span></span>
<span data-ttu-id="9e5c9-106">O cmdlet **Remove-AzureKeyVaultCertificateContact** exclui um contato que está registrado para notificações de certificado de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="9e5c9-106">The **Remove-AzureKeyVaultCertificateContact** cmdlet deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="9e5c9-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9e5c9-107">EXAMPLES</span></span>

### <span data-ttu-id="9e5c9-108">Exemplo 1: remover um contato de certificado</span><span class="sxs-lookup"><span data-stu-id="9e5c9-108">Example 1: Remove a certificate contact</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificateContact -VaultName "Contoso01" -EmailAddress "patti.fuller@contoso.com"
```

<span data-ttu-id="9e5c9-109">Esse comando Remove Patti pereira como um contato de certificado para o cofre de chaves Contoso01.</span><span class="sxs-lookup"><span data-stu-id="9e5c9-109">This command removes Patti Fuller as a certificate contact for the Contoso01 key vault.</span></span>

## <span data-ttu-id="9e5c9-110">OS</span><span class="sxs-lookup"><span data-stu-id="9e5c9-110">PARAMETERS</span></span>

### <span data-ttu-id="9e5c9-111">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="9e5c9-111">-EmailAddress</span></span>
<span data-ttu-id="9e5c9-112">Especifica o endereço de email do contato a ser removido.</span><span class="sxs-lookup"><span data-stu-id="9e5c9-112">Specifies the email address of the contact to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e5c9-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9e5c9-113">-PassThru</span></span>
<span data-ttu-id="9e5c9-114">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="9e5c9-114">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9e5c9-115">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="9e5c9-115">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e5c9-116">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="9e5c9-116">-VaultName</span></span>
<span data-ttu-id="9e5c9-117">Especifica o nome de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="9e5c9-117">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e5c9-118">-Confirme</span><span class="sxs-lookup"><span data-stu-id="9e5c9-118">-Confirm</span></span>
<span data-ttu-id="9e5c9-119">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9e5c9-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e5c9-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e5c9-120">-WhatIf</span></span>
<span data-ttu-id="9e5c9-121">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9e5c9-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e5c9-122">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9e5c9-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e5c9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e5c9-123">-DefaultProfile</span></span>
<span data-ttu-id="9e5c9-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9e5c9-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e5c9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e5c9-125">CommonParameters</span></span>
<span data-ttu-id="9e5c9-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e5c9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e5c9-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e5c9-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e5c9-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="9e5c9-128">INPUTS</span></span>

## <span data-ttu-id="9e5c9-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="9e5c9-129">OUTPUTS</span></span>

### <span data-ttu-id="9e5c9-130">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. keyvault. Models. KeyVaultCertificateContact]</span><span class="sxs-lookup"><span data-stu-id="9e5c9-130">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact]</span></span>

## <span data-ttu-id="9e5c9-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="9e5c9-131">NOTES</span></span>

## <span data-ttu-id="9e5c9-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9e5c9-132">RELATED LINKS</span></span>

[<span data-ttu-id="9e5c9-133">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="9e5c9-133">Add-AzureKeyVaultCertificateContact</span></span>](./Add-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="9e5c9-134">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="9e5c9-134">Get-AzureKeyVaultCertificateContact</span></span>](./Get-AzureKeyVaultCertificateContact.md)

