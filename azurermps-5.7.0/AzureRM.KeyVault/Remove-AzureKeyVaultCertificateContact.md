---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 35FAA57F-B2BD-4E43-8238-12F7A8269E4D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: c91aa7e43a36e1218f304c3675f1d3c9635002c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93439863"
---
# <span data-ttu-id="18e37-101">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="18e37-101">Remove-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="18e37-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="18e37-102">SYNOPSIS</span></span>
<span data-ttu-id="18e37-103">Exclui um contato registrado para notificações de certificado de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="18e37-103">Deletes a contact that is registered for certificate notifications from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18e37-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="18e37-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18e37-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="18e37-105">DESCRIPTION</span></span>
<span data-ttu-id="18e37-106">O cmdlet **Remove-AzureKeyVaultCertificateContact** exclui um contato que está registrado para notificações de certificado de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="18e37-106">The **Remove-AzureKeyVaultCertificateContact** cmdlet deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="18e37-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="18e37-107">EXAMPLES</span></span>

### <span data-ttu-id="18e37-108">Exemplo 1: remover um contato de certificado</span><span class="sxs-lookup"><span data-stu-id="18e37-108">Example 1: Remove a certificate contact</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificateContact -VaultName "Contoso01" -EmailAddress "patti.fuller@contoso.com"
```

<span data-ttu-id="18e37-109">Esse comando Remove Patti pereira como um contato de certificado para o cofre de chaves Contoso01.</span><span class="sxs-lookup"><span data-stu-id="18e37-109">This command removes Patti Fuller as a certificate contact for the Contoso01 key vault.</span></span>

## <span data-ttu-id="18e37-110">OS</span><span class="sxs-lookup"><span data-stu-id="18e37-110">PARAMETERS</span></span>

### <span data-ttu-id="18e37-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18e37-111">-DefaultProfile</span></span>
<span data-ttu-id="18e37-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="18e37-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="18e37-113">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="18e37-113">-EmailAddress</span></span>
<span data-ttu-id="18e37-114">Especifica o endereço de email do contato a ser removido.</span><span class="sxs-lookup"><span data-stu-id="18e37-114">Specifies the email address of the contact to remove.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18e37-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="18e37-115">-PassThru</span></span>
<span data-ttu-id="18e37-116">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="18e37-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="18e37-117">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="18e37-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="18e37-118">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="18e37-118">-VaultName</span></span>
<span data-ttu-id="18e37-119">Especifica o nome de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="18e37-119">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="18e37-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="18e37-120">-Confirm</span></span>
<span data-ttu-id="18e37-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18e37-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18e37-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18e37-122">-WhatIf</span></span>
<span data-ttu-id="18e37-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="18e37-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18e37-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="18e37-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18e37-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18e37-125">CommonParameters</span></span>
<span data-ttu-id="18e37-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18e37-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18e37-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18e37-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18e37-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="18e37-128">INPUTS</span></span>

### <span data-ttu-id="18e37-129">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="18e37-129">None</span></span>
<span data-ttu-id="18e37-130">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="18e37-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="18e37-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="18e37-131">OUTPUTS</span></span>

### <span data-ttu-id="18e37-132">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateContact]</span><span class="sxs-lookup"><span data-stu-id="18e37-132">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact]</span></span>

## <span data-ttu-id="18e37-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="18e37-133">NOTES</span></span>

## <span data-ttu-id="18e37-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="18e37-134">RELATED LINKS</span></span>

[<span data-ttu-id="18e37-135">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="18e37-135">Add-AzureKeyVaultCertificateContact</span></span>](./Add-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="18e37-136">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="18e37-136">Get-AzureKeyVaultCertificateContact</span></span>](./Get-AzureKeyVaultCertificateContact.md)

