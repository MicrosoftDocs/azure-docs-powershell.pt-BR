---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 35FAA57F-B2BD-4E43-8238-12F7A8269E4D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificatecontact
schema: 2.0.0
ms.openlocfilehash: 9bfb62388ce4a7a8994f4a618a4c1a00ac5868d6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785223"
---
# <span data-ttu-id="7c12a-101">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="7c12a-101">Remove-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="7c12a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7c12a-102">SYNOPSIS</span></span>
<span data-ttu-id="7c12a-103">Exclui um contato registrado para notificações de certificado de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="7c12a-103">Deletes a contact that is registered for certificate notifications from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7c12a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7c12a-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c12a-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7c12a-105">DESCRIPTION</span></span>
<span data-ttu-id="7c12a-106">O cmdlet **Remove-AzureKeyVaultCertificateContact** exclui um contato que está registrado para notificações de certificado de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="7c12a-106">The **Remove-AzureKeyVaultCertificateContact** cmdlet deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="7c12a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7c12a-107">EXAMPLES</span></span>

### <span data-ttu-id="7c12a-108">Exemplo 1: remover um contato de certificado</span><span class="sxs-lookup"><span data-stu-id="7c12a-108">Example 1: Remove a certificate contact</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificateContact -VaultName "Contoso01" -EmailAddress "patti.fuller@contoso.com"
```

<span data-ttu-id="7c12a-109">Esse comando Remove Patti pereira como um contato de certificado para o cofre de chaves Contoso01.</span><span class="sxs-lookup"><span data-stu-id="7c12a-109">This command removes Patti Fuller as a certificate contact for the Contoso01 key vault.</span></span>

## <span data-ttu-id="7c12a-110">OS</span><span class="sxs-lookup"><span data-stu-id="7c12a-110">PARAMETERS</span></span>

### <span data-ttu-id="7c12a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c12a-111">-DefaultProfile</span></span>
<span data-ttu-id="7c12a-112">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="7c12a-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7c12a-113">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="7c12a-113">-EmailAddress</span></span>
<span data-ttu-id="7c12a-114">Especifica o endereço de email do contato a ser removido.</span><span class="sxs-lookup"><span data-stu-id="7c12a-114">Specifies the email address of the contact to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c12a-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7c12a-115">-PassThru</span></span>
<span data-ttu-id="7c12a-116">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="7c12a-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7c12a-117">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="7c12a-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7c12a-118">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="7c12a-118">-VaultName</span></span>
<span data-ttu-id="7c12a-119">Especifica o nome de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="7c12a-119">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="7c12a-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7c12a-120">-Confirm</span></span>
<span data-ttu-id="7c12a-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c12a-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c12a-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c12a-122">-WhatIf</span></span>
<span data-ttu-id="7c12a-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7c12a-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c12a-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7c12a-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c12a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c12a-125">CommonParameters</span></span>
<span data-ttu-id="7c12a-126">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c12a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c12a-127">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c12a-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c12a-128">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7c12a-128">INPUTS</span></span>

## <span data-ttu-id="7c12a-129">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7c12a-129">OUTPUTS</span></span>

### <span data-ttu-id="7c12a-130">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. keyvault. Models. KeyVaultCertificateContact]</span><span class="sxs-lookup"><span data-stu-id="7c12a-130">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact]</span></span>

## <span data-ttu-id="7c12a-131">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7c12a-131">NOTES</span></span>

## <span data-ttu-id="7c12a-132">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7c12a-132">RELATED LINKS</span></span>

[<span data-ttu-id="7c12a-133">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="7c12a-133">Add-AzureKeyVaultCertificateContact</span></span>](./Add-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="7c12a-134">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="7c12a-134">Get-AzureKeyVaultCertificateContact</span></span>](./Get-AzureKeyVaultCertificateContact.md)

