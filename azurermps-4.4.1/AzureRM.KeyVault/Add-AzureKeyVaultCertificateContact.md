---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2D3021B3-12C5-4797-8BF2-800E3CEAC56C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: af66ad82d37c29d1dcd455cb3ccf7ae11676828c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440641"
---
# <span data-ttu-id="deecf-101">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="deecf-101">Add-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="deecf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="deecf-102">SYNOPSIS</span></span>
<span data-ttu-id="deecf-103">Adiciona um contato para notificações de certificado.</span><span class="sxs-lookup"><span data-stu-id="deecf-103">Adds a contact for certificate notifications.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="deecf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="deecf-104">SYNTAX</span></span>

```
Add-AzureKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="deecf-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="deecf-105">DESCRIPTION</span></span>
<span data-ttu-id="deecf-106">O cmdlet **Add-AzureKeyVaultCertificateContact** adiciona um contato para um cofre de chaves para notificações de certificado no cofre de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="deecf-106">The **Add-AzureKeyVaultCertificateContact** cmdlet adds a contact for a key vault for certificate notifications in Azure Key Vault.</span></span>
<span data-ttu-id="deecf-107">O contato recebe atualizações sobre eventos como certificado próximo a vencimento, certificado renovado e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="deecf-107">The contact receives updates about events such as certificate close to expiry, certificate renewed, and so on.</span></span>
<span data-ttu-id="deecf-108">Esses eventos são determinados pela política de certificado.</span><span class="sxs-lookup"><span data-stu-id="deecf-108">These events are determined by the certificate policy.</span></span>

## <span data-ttu-id="deecf-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="deecf-109">EXAMPLES</span></span>

### <span data-ttu-id="deecf-110">Exemplo 1: adicionar um contato de certificado de cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="deecf-110">Example 1: Add a key vault certificate contact</span></span>
```
PS C:\>Add-AzureKeyVaultCertificateContact -VaultName "ContosoKV01" -EmailAddress "patti.fuller@contoso.com" -PassThru
```

<span data-ttu-id="deecf-111">Esse comando adiciona Patti pereira como um contato do certificado para o cofre da chave ContosoKV01 e retorna o objeto **KeyVaultCertificateContact** .</span><span class="sxs-lookup"><span data-stu-id="deecf-111">This command adds Patti Fuller as a certificate contact for the ContosoKV01 key vault and returns the **KeyVaultCertificateContact** object.</span></span>

## <span data-ttu-id="deecf-112">OS</span><span class="sxs-lookup"><span data-stu-id="deecf-112">PARAMETERS</span></span>

### <span data-ttu-id="deecf-113">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="deecf-113">-EmailAddress</span></span>
<span data-ttu-id="deecf-114">Especifica o endereço de email do contato.</span><span class="sxs-lookup"><span data-stu-id="deecf-114">Specifies the email address of the contact.</span></span>

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

### <span data-ttu-id="deecf-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="deecf-115">-PassThru</span></span>
<span data-ttu-id="deecf-116">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="deecf-116">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="deecf-117">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="deecf-117">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="deecf-118">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="deecf-118">-VaultName</span></span>
<span data-ttu-id="deecf-119">Especifica o nome do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="deecf-119">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="deecf-120">-Confirme</span><span class="sxs-lookup"><span data-stu-id="deecf-120">-Confirm</span></span>
<span data-ttu-id="deecf-121">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="deecf-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="deecf-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="deecf-122">-WhatIf</span></span>
<span data-ttu-id="deecf-123">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="deecf-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="deecf-124">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="deecf-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="deecf-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="deecf-125">-DefaultProfile</span></span>
<span data-ttu-id="deecf-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="deecf-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="deecf-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="deecf-127">CommonParameters</span></span>
<span data-ttu-id="deecf-128">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="deecf-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="deecf-129">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="deecf-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="deecf-130">SENSORES</span><span class="sxs-lookup"><span data-stu-id="deecf-130">INPUTS</span></span>

## <span data-ttu-id="deecf-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="deecf-131">OUTPUTS</span></span>

### <span data-ttu-id="deecf-132">List<Microsoft. Azure. Commands. keyvault. Models. KeyVaultCertificateContact></span><span class="sxs-lookup"><span data-stu-id="deecf-132">List<Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateContact></span></span>

## <span data-ttu-id="deecf-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="deecf-133">NOTES</span></span>

## <span data-ttu-id="deecf-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="deecf-134">RELATED LINKS</span></span>

[<span data-ttu-id="deecf-135">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="deecf-135">Get-AzureKeyVaultCertificateContact</span></span>](./Get-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="deecf-136">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="deecf-136">Remove-AzureKeyVaultCertificateContact</span></span>](./Remove-AzureKeyVaultCertificateContact.md)

