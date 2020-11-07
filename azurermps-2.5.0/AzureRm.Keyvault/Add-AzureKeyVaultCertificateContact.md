---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2D3021B3-12C5-4797-8BF2-800E3CEAC56C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/add-azurekeyvaultcertificatecontact
schema: 2.0.0
ms.openlocfilehash: 9f52889f044ba6bf497b57a53f3e2daaea0dbf3b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785233"
---
# <span data-ttu-id="8325e-101">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="8325e-101">Add-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="8325e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8325e-102">SYNOPSIS</span></span>
<span data-ttu-id="8325e-103">Adiciona um contato para notificações de certificado.</span><span class="sxs-lookup"><span data-stu-id="8325e-103">Adds a contact for certificate notifications.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8325e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8325e-104">SYNTAX</span></span>

```
Add-AzureKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8325e-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8325e-105">DESCRIPTION</span></span>
<span data-ttu-id="8325e-106">O cmdlet **Add-AzureKeyVaultCertificateContact** adiciona um contato para um cofre de chaves para notificações de certificado no cofre de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="8325e-106">The **Add-AzureKeyVaultCertificateContact** cmdlet adds a contact for a key vault for certificate notifications in Azure Key Vault.</span></span>
<span data-ttu-id="8325e-107">O contato recebe atualizações sobre eventos como certificado próximo a vencimento, certificado renovado e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="8325e-107">The contact receives updates about events such as certificate close to expiry, certificate renewed, and so on.</span></span>
<span data-ttu-id="8325e-108">Esses eventos são determinados pela política de certificado.</span><span class="sxs-lookup"><span data-stu-id="8325e-108">These events are determined by the certificate policy.</span></span>

## <span data-ttu-id="8325e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8325e-109">EXAMPLES</span></span>

### <span data-ttu-id="8325e-110">Exemplo 1: adicionar um contato de certificado de cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="8325e-110">Example 1: Add a key vault certificate contact</span></span>
```
PS C:\>Add-AzureKeyVaultCertificateContact -VaultName "ContosoKV01" -EmailAddress "patti.fuller@contoso.com" -PassThru
```

<span data-ttu-id="8325e-111">Esse comando adiciona Patti pereira como um contato do certificado para o cofre da chave ContosoKV01 e retorna o objeto **KeyVaultCertificateContact** .</span><span class="sxs-lookup"><span data-stu-id="8325e-111">This command adds Patti Fuller as a certificate contact for the ContosoKV01 key vault and returns the **KeyVaultCertificateContact** object.</span></span>

## <span data-ttu-id="8325e-112">OS</span><span class="sxs-lookup"><span data-stu-id="8325e-112">PARAMETERS</span></span>

### <span data-ttu-id="8325e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8325e-113">-DefaultProfile</span></span>
<span data-ttu-id="8325e-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="8325e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8325e-115">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="8325e-115">-EmailAddress</span></span>
<span data-ttu-id="8325e-116">Especifica o endereço de email do contato.</span><span class="sxs-lookup"><span data-stu-id="8325e-116">Specifies the email address of the contact.</span></span>

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

### <span data-ttu-id="8325e-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8325e-117">-PassThru</span></span>
<span data-ttu-id="8325e-118">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="8325e-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8325e-119">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="8325e-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8325e-120">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="8325e-120">-VaultName</span></span>
<span data-ttu-id="8325e-121">Especifica o nome do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="8325e-121">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="8325e-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="8325e-122">-Confirm</span></span>
<span data-ttu-id="8325e-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8325e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8325e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8325e-124">-WhatIf</span></span>
<span data-ttu-id="8325e-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8325e-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8325e-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8325e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8325e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8325e-127">CommonParameters</span></span>
<span data-ttu-id="8325e-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8325e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8325e-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8325e-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8325e-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8325e-130">INPUTS</span></span>

## <span data-ttu-id="8325e-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8325e-131">OUTPUTS</span></span>

### <span data-ttu-id="8325e-132">List<Microsoft. Azure. Commands. keyvault. Models. KeyVaultCertificateContact></span><span class="sxs-lookup"><span data-stu-id="8325e-132">List<Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact></span></span>

## <span data-ttu-id="8325e-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8325e-133">NOTES</span></span>

## <span data-ttu-id="8325e-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8325e-134">RELATED LINKS</span></span>

[<span data-ttu-id="8325e-135">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="8325e-135">Get-AzureKeyVaultCertificateContact</span></span>](./Get-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="8325e-136">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="8325e-136">Remove-AzureKeyVaultCertificateContact</span></span>](./Remove-AzureKeyVaultCertificateContact.md)

