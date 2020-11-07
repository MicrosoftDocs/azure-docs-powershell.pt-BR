---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2D3021B3-12C5-4797-8BF2-800E3CEAC56C
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificateContact.md
ms.openlocfilehash: ff363ae1bf6581baaeb177edd4e215494c82f85f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93770682"
---
# <span data-ttu-id="e0ad5-101">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="e0ad5-101">Add-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="e0ad5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e0ad5-102">SYNOPSIS</span></span>
<span data-ttu-id="e0ad5-103">Adiciona um contato para notificações de certificado.</span><span class="sxs-lookup"><span data-stu-id="e0ad5-103">Adds a contact for certificate notifications.</span></span>

## <span data-ttu-id="e0ad5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e0ad5-104">SYNTAX</span></span>

### <span data-ttu-id="e0ad5-105">Interativo (padrão)</span><span class="sxs-lookup"><span data-stu-id="e0ad5-105">Interactive (Default)</span></span>
```
Add-AzKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0ad5-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="e0ad5-106">ByObject</span></span>
```
Add-AzKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0ad5-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e0ad5-107">ByResourceId</span></span>
```
Add-AzKeyVaultCertificateContact [-ResourceId] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0ad5-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e0ad5-108">DESCRIPTION</span></span>
<span data-ttu-id="e0ad5-109">O cmdlet **Add-AzKeyVaultCertificateContact** adiciona um contato para um cofre de chaves para notificações de certificado no cofre de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="e0ad5-109">The **Add-AzKeyVaultCertificateContact** cmdlet adds a contact for a key vault for certificate notifications in Azure Key Vault.</span></span>
<span data-ttu-id="e0ad5-110">O contato recebe atualizações sobre eventos como certificado próximo a vencimento, certificado renovado e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="e0ad5-110">The contact receives updates about events such as certificate close to expiry, certificate renewed, and so on.</span></span>
<span data-ttu-id="e0ad5-111">Esses eventos são determinados pela política de certificado.</span><span class="sxs-lookup"><span data-stu-id="e0ad5-111">These events are determined by the certificate policy.</span></span>

## <span data-ttu-id="e0ad5-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e0ad5-112">EXAMPLES</span></span>

### <span data-ttu-id="e0ad5-113">Exemplo 1: adicionar um contato de certificado de cofre de chaves</span><span class="sxs-lookup"><span data-stu-id="e0ad5-113">Example 1: Add a key vault certificate contact</span></span>
```powershell
PS C:\> Add-AzKeyVaultCertificateContact -VaultName "ContosoKV01" -EmailAddress "patti.fuller@contoso.com" -PassThru

Email                    VaultName
-----                    ---------
patti.fuller@contoso.com ContosoKV01
```

<span data-ttu-id="e0ad5-114">Esse comando adiciona Patti pereira como um contato do certificado para o cofre da chave ContosoKV01 e retorna a lista de contatos do cofre "ContosoKV01".</span><span class="sxs-lookup"><span data-stu-id="e0ad5-114">This command adds Patti Fuller as a certificate contact for the ContosoKV01 key vault and returns the list of contacts for the "ContosoKV01" vault.</span></span>

## <span data-ttu-id="e0ad5-115">OS</span><span class="sxs-lookup"><span data-stu-id="e0ad5-115">PARAMETERS</span></span>

### <span data-ttu-id="e0ad5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0ad5-116">-DefaultProfile</span></span>
<span data-ttu-id="e0ad5-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="e0ad5-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0ad5-118">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="e0ad5-118">-EmailAddress</span></span>
<span data-ttu-id="e0ad5-119">Especifica o endereço de email do contato.</span><span class="sxs-lookup"><span data-stu-id="e0ad5-119">Specifies the email address of the contact.</span></span>

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

### <span data-ttu-id="e0ad5-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e0ad5-120">-InputObject</span></span>
<span data-ttu-id="e0ad5-121">Objeto do keyvault.</span><span class="sxs-lookup"><span data-stu-id="e0ad5-121">KeyVault object.</span></span>

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

### <span data-ttu-id="e0ad5-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e0ad5-122">-PassThru</span></span>
<span data-ttu-id="e0ad5-123">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="e0ad5-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e0ad5-124">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="e0ad5-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e0ad5-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e0ad5-125">-ResourceId</span></span>
<span data-ttu-id="e0ad5-126">ID do recurso do keyvault.</span><span class="sxs-lookup"><span data-stu-id="e0ad5-126">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="e0ad5-127">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="e0ad5-127">-VaultName</span></span>
<span data-ttu-id="e0ad5-128">Especifica o nome do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="e0ad5-128">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="e0ad5-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e0ad5-129">-Confirm</span></span>
<span data-ttu-id="e0ad5-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0ad5-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0ad5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0ad5-131">-WhatIf</span></span>
<span data-ttu-id="e0ad5-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e0ad5-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0ad5-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e0ad5-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0ad5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0ad5-134">CommonParameters</span></span>
<span data-ttu-id="e0ad5-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0ad5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0ad5-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0ad5-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0ad5-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e0ad5-137">INPUTS</span></span>

### <span data-ttu-id="e0ad5-138">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="e0ad5-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="e0ad5-139">System. String</span><span class="sxs-lookup"><span data-stu-id="e0ad5-139">System.String</span></span>

## <span data-ttu-id="e0ad5-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e0ad5-140">OUTPUTS</span></span>

### <span data-ttu-id="e0ad5-141">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="e0ad5-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="e0ad5-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e0ad5-142">NOTES</span></span>

## <span data-ttu-id="e0ad5-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e0ad5-143">RELATED LINKS</span></span>

[<span data-ttu-id="e0ad5-144">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="e0ad5-144">Get-AzKeyVaultCertificateContact</span></span>](./Get-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="e0ad5-145">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="e0ad5-145">Remove-AzKeyVaultCertificateContact</span></span>](./Remove-AzKeyVaultCertificateContact.md)

