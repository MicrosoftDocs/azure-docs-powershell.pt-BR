---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2D3021B3-12C5-4797-8BF2-800E3CEAC56C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/add-azurekeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: 96f793c763a3e9a710c7e401c29880ccc0136b38
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440455"
---
# <span data-ttu-id="72641-101">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="72641-101">Add-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="72641-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="72641-102">SYNOPSIS</span></span>
<span data-ttu-id="72641-103">Adiciona um contato para notificações de certificado.</span><span class="sxs-lookup"><span data-stu-id="72641-103">Adds a contact for certificate notifications.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="72641-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="72641-104">SYNTAX</span></span>

### <span data-ttu-id="72641-105">Interativo (padrão)</span><span class="sxs-lookup"><span data-stu-id="72641-105">Interactive (Default)</span></span>
```
Add-AzureKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72641-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="72641-106">ByObject</span></span>
```
Add-AzureKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72641-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="72641-107">DESCRIPTION</span></span>
<span data-ttu-id="72641-108">O cmdlet **Add-AzureKeyVaultCertificateContact** adiciona um contato para um cofre de chaves para notificações de certificado no cofre de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="72641-108">The **Add-AzureKeyVaultCertificateContact** cmdlet adds a contact for a key vault for certificate notifications in Azure Key Vault.</span></span>
<span data-ttu-id="72641-109">O contato recebe atualizações sobre eventos como certificado próximo a vencimento, certificado renovado e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="72641-109">The contact receives updates about events such as certificate close to expiry, certificate renewed, and so on.</span></span>
<span data-ttu-id="72641-110">Esses eventos são determinados pela política de certificado.</span><span class="sxs-lookup"><span data-stu-id="72641-110">These events are determined by the certificate policy.</span></span>

## <span data-ttu-id="72641-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="72641-111">EXAMPLES</span></span>

### <span data-ttu-id="72641-112">Exemplo 1: adicionar um contato de certificado de cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="72641-112">Example 1: Add a key vault certificate contact</span></span>
```
PS C:\>Add-AzureKeyVaultCertificateContact -VaultName "ContosoKV01" -EmailAddress "patti.fuller@contoso.com" -PassThru
```

<span data-ttu-id="72641-113">Esse comando adiciona Patti pereira como um contato do certificado para o cofre da chave ContosoKV01 e retorna o objeto **KeyVaultCertificateContact** .</span><span class="sxs-lookup"><span data-stu-id="72641-113">This command adds Patti Fuller as a certificate contact for the ContosoKV01 key vault and returns the **KeyVaultCertificateContact** object.</span></span>

## <span data-ttu-id="72641-114">OS</span><span class="sxs-lookup"><span data-stu-id="72641-114">PARAMETERS</span></span>

### <span data-ttu-id="72641-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72641-115">-DefaultProfile</span></span>
<span data-ttu-id="72641-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="72641-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72641-117">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="72641-117">-EmailAddress</span></span>
<span data-ttu-id="72641-118">Especifica o endereço de email do contato.</span><span class="sxs-lookup"><span data-stu-id="72641-118">Specifies the email address of the contact.</span></span>

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

### <span data-ttu-id="72641-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="72641-119">-InputObject</span></span>
<span data-ttu-id="72641-120">Objeto do keyvault.</span><span class="sxs-lookup"><span data-stu-id="72641-120">KeyVault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="72641-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="72641-121">-PassThru</span></span>
<span data-ttu-id="72641-122">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="72641-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="72641-123">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="72641-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="72641-124">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="72641-124">-VaultName</span></span>
<span data-ttu-id="72641-125">Especifica o nome do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="72641-125">Specifies the name of the key vault.</span></span>

```yaml
Type: String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72641-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="72641-126">-Confirm</span></span>
<span data-ttu-id="72641-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72641-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72641-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72641-128">-WhatIf</span></span>
<span data-ttu-id="72641-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="72641-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72641-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="72641-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72641-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72641-131">CommonParameters</span></span>
<span data-ttu-id="72641-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72641-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72641-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72641-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72641-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="72641-134">INPUTS</span></span>

### <span data-ttu-id="72641-135">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="72641-135">None</span></span>
<span data-ttu-id="72641-136">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="72641-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="72641-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="72641-137">OUTPUTS</span></span>

### <span data-ttu-id="72641-138">List<Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateContact></span><span class="sxs-lookup"><span data-stu-id="72641-138">List<Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact></span></span>

## <span data-ttu-id="72641-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="72641-139">NOTES</span></span>

## <span data-ttu-id="72641-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="72641-140">RELATED LINKS</span></span>

[<span data-ttu-id="72641-141">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="72641-141">Get-AzureKeyVaultCertificateContact</span></span>](./Get-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="72641-142">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="72641-142">Remove-AzureKeyVaultCertificateContact</span></span>](./Remove-AzureKeyVaultCertificateContact.md)

