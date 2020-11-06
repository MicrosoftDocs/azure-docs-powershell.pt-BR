---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2D3021B3-12C5-4797-8BF2-800E3CEAC56C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/add-azurekeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: c56dad380d1e5a43b3f4dafdc0e0e964e6264ef3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440788"
---
# <span data-ttu-id="a1658-101">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="a1658-101">Add-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="a1658-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a1658-102">SYNOPSIS</span></span>
<span data-ttu-id="a1658-103">Adiciona um contato para notificações de certificado.</span><span class="sxs-lookup"><span data-stu-id="a1658-103">Adds a contact for certificate notifications.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1658-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a1658-104">SYNTAX</span></span>

### <span data-ttu-id="a1658-105">Interativo (padrão)</span><span class="sxs-lookup"><span data-stu-id="a1658-105">Interactive (Default)</span></span>
```
Add-AzureKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1658-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="a1658-106">ByObject</span></span>
```
Add-AzureKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1658-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a1658-107">ByResourceId</span></span>
```
Add-AzureKeyVaultCertificateContact [-ResourceId] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1658-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a1658-108">DESCRIPTION</span></span>
<span data-ttu-id="a1658-109">O cmdlet **Add-AzureKeyVaultCertificateContact** adiciona um contato para um cofre de chaves para notificações de certificado no cofre de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="a1658-109">The **Add-AzureKeyVaultCertificateContact** cmdlet adds a contact for a key vault for certificate notifications in Azure Key Vault.</span></span>
<span data-ttu-id="a1658-110">O contato recebe atualizações sobre eventos como certificado próximo a vencimento, certificado renovado e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="a1658-110">The contact receives updates about events such as certificate close to expiry, certificate renewed, and so on.</span></span>
<span data-ttu-id="a1658-111">Esses eventos são determinados pela política de certificado.</span><span class="sxs-lookup"><span data-stu-id="a1658-111">These events are determined by the certificate policy.</span></span>

## <span data-ttu-id="a1658-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a1658-112">EXAMPLES</span></span>

### <span data-ttu-id="a1658-113">Exemplo 1: adicionar um contato de certificado de cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="a1658-113">Example 1: Add a key vault certificate contact</span></span>
```powershell
PS C:\> Add-AzureKeyVaultCertificateContact -VaultName "ContosoKV01" -EmailAddress "patti.fuller@contoso.com" -PassThru

Email                    VaultName
-----                    ---------
patti.fuller@contoso.com ContosoKV01
```

<span data-ttu-id="a1658-114">Esse comando adiciona Patti pereira como um contato do certificado para o cofre da chave ContosoKV01 e retorna a lista de contatos do cofre "ContosoKV01".</span><span class="sxs-lookup"><span data-stu-id="a1658-114">This command adds Patti Fuller as a certificate contact for the ContosoKV01 key vault and returns the list of contacts for the "ContosoKV01" vault.</span></span>

## <span data-ttu-id="a1658-115">OS</span><span class="sxs-lookup"><span data-stu-id="a1658-115">PARAMETERS</span></span>

### <span data-ttu-id="a1658-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1658-116">-DefaultProfile</span></span>
<span data-ttu-id="a1658-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="a1658-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a1658-118">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="a1658-118">-EmailAddress</span></span>
<span data-ttu-id="a1658-119">Especifica o endereço de email do contato.</span><span class="sxs-lookup"><span data-stu-id="a1658-119">Specifies the email address of the contact.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1658-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a1658-120">-InputObject</span></span>
<span data-ttu-id="a1658-121">Objeto do keyvault.</span><span class="sxs-lookup"><span data-stu-id="a1658-121">KeyVault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1658-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a1658-122">-PassThru</span></span>
<span data-ttu-id="a1658-123">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="a1658-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a1658-124">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="a1658-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a1658-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a1658-125">-ResourceId</span></span>
<span data-ttu-id="a1658-126">ID do recurso do keyvault.</span><span class="sxs-lookup"><span data-stu-id="a1658-126">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1658-127">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="a1658-127">-VaultName</span></span>
<span data-ttu-id="a1658-128">Especifica o nome do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="a1658-128">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1658-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a1658-129">-Confirm</span></span>
<span data-ttu-id="a1658-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1658-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1658-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1658-131">-WhatIf</span></span>
<span data-ttu-id="a1658-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a1658-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1658-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a1658-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1658-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1658-134">CommonParameters</span></span>
<span data-ttu-id="a1658-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1658-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1658-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1658-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1658-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a1658-137">INPUTS</span></span>

### <span data-ttu-id="a1658-138">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="a1658-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="a1658-139">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a1658-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="a1658-140">System. String</span><span class="sxs-lookup"><span data-stu-id="a1658-140">System.String</span></span>

## <span data-ttu-id="a1658-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a1658-141">OUTPUTS</span></span>

### <span data-ttu-id="a1658-142">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="a1658-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="a1658-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a1658-143">NOTES</span></span>

## <span data-ttu-id="a1658-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a1658-144">RELATED LINKS</span></span>

[<span data-ttu-id="a1658-145">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="a1658-145">Get-AzureKeyVaultCertificateContact</span></span>](./Get-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="a1658-146">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="a1658-146">Remove-AzureKeyVaultCertificateContact</span></span>](./Remove-AzureKeyVaultCertificateContact.md)
