---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificateContact.md
ms.openlocfilehash: 375cc5493bd3b3cac31f4318df57e155eda918c3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776680"
---
# <span data-ttu-id="07f31-101">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="07f31-101">Add-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="07f31-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="07f31-102">SYNOPSIS</span></span>
<span data-ttu-id="07f31-103">Adiciona um contato para notificações de certificado.</span><span class="sxs-lookup"><span data-stu-id="07f31-103">Adds a contact for certificate notifications.</span></span>

## <span data-ttu-id="07f31-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="07f31-104">SYNTAX</span></span>

```
Add-AzKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07f31-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="07f31-105">DESCRIPTION</span></span>
<span data-ttu-id="07f31-106">O cmdlet **Add-AzKeyVaultCertificateContact** adiciona um contato para um cofre de chaves para notificações de certificado no cofre de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="07f31-106">The **Add-AzKeyVaultCertificateContact** cmdlet adds a contact for a key vault for certificate notifications in Azure Key Vault.</span></span>
<span data-ttu-id="07f31-107">O contato recebe atualizações sobre eventos como certificado próximo a vencimento, certificado renovado e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="07f31-107">The contact receives updates about events such as certificate close to expiry, certificate renewed, and so on.</span></span>
<span data-ttu-id="07f31-108">Esses eventos são determinados pela política de certificado.</span><span class="sxs-lookup"><span data-stu-id="07f31-108">These events are determined by the certificate policy.</span></span>

## <span data-ttu-id="07f31-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="07f31-109">EXAMPLES</span></span>

### <span data-ttu-id="07f31-110">Exemplo 1: adicionar um contato de certificado de cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="07f31-110">Example 1: Add a key vault certificate contact</span></span>
```
PS C:\>Add-AzKeyVaultCertificateContact -VaultName "ContosoKV01" -EmailAddress "patti.fuller@contoso.com" -PassThru
```

<span data-ttu-id="07f31-111">Esse comando adiciona Patti pereira como um contato do certificado para o cofre da chave ContosoKV01 e retorna o objeto **KeyVaultCertificateContact** .</span><span class="sxs-lookup"><span data-stu-id="07f31-111">This command adds Patti Fuller as a certificate contact for the ContosoKV01 key vault and returns the **KeyVaultCertificateContact** object.</span></span>

## <span data-ttu-id="07f31-112">OS</span><span class="sxs-lookup"><span data-stu-id="07f31-112">PARAMETERS</span></span>

### <span data-ttu-id="07f31-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07f31-113">-DefaultProfile</span></span>
<span data-ttu-id="07f31-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="07f31-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07f31-115">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="07f31-115">-EmailAddress</span></span>
<span data-ttu-id="07f31-116">Especifica o endereço de email do contato.</span><span class="sxs-lookup"><span data-stu-id="07f31-116">Specifies the email address of the contact.</span></span>

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

### <span data-ttu-id="07f31-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="07f31-117">-PassThru</span></span>
<span data-ttu-id="07f31-118">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="07f31-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="07f31-119">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="07f31-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="07f31-120">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="07f31-120">-VaultName</span></span>
<span data-ttu-id="07f31-121">Especifica o nome do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="07f31-121">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="07f31-122">-Confirme</span><span class="sxs-lookup"><span data-stu-id="07f31-122">-Confirm</span></span>
<span data-ttu-id="07f31-123">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07f31-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07f31-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07f31-124">-WhatIf</span></span>
<span data-ttu-id="07f31-125">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="07f31-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07f31-126">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="07f31-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07f31-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07f31-127">CommonParameters</span></span>
<span data-ttu-id="07f31-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07f31-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07f31-129">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07f31-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07f31-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="07f31-130">INPUTS</span></span>

### <span data-ttu-id="07f31-131">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="07f31-131">None</span></span>
<span data-ttu-id="07f31-132">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="07f31-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="07f31-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="07f31-133">OUTPUTS</span></span>

### <span data-ttu-id="07f31-134">List<Microsoft. Azure. Commands. keyvault. Models. KeyVaultCertificateContact></span><span class="sxs-lookup"><span data-stu-id="07f31-134">List<Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact></span></span>

## <span data-ttu-id="07f31-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="07f31-135">NOTES</span></span>

## <span data-ttu-id="07f31-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="07f31-136">RELATED LINKS</span></span>

[<span data-ttu-id="07f31-137">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="07f31-137">Get-AzKeyVaultCertificateContact</span></span>](./Get-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="07f31-138">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="07f31-138">Remove-AzKeyVaultCertificateContact</span></span>](./Remove-AzKeyVaultCertificateContact.md)

