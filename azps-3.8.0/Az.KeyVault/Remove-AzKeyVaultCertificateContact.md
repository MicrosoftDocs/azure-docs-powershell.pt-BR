---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 35FAA57F-B2BD-4E43-8238-12F7A8269E4D
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateContact.md
ms.openlocfilehash: 12fe8cdc0e8e7210a2db7c7c6ccab1a0fcceeba3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942553"
---
# <span data-ttu-id="e7a7f-101">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="e7a7f-101">Remove-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="e7a7f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e7a7f-102">SYNOPSIS</span></span>
<span data-ttu-id="e7a7f-103">Exclui um contato registrado para notificações de certificado de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="e7a7f-103">Deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="e7a7f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e7a7f-104">SYNTAX</span></span>

### <span data-ttu-id="e7a7f-105">ByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="e7a7f-105">ByName (Default)</span></span>
```
Remove-AzKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7a7f-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="e7a7f-106">ByObject</span></span>
```
Remove-AzKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7a7f-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e7a7f-107">ByResourceId</span></span>
```
Remove-AzKeyVaultCertificateContact [-ResourceId] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7a7f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e7a7f-108">DESCRIPTION</span></span>
<span data-ttu-id="e7a7f-109">O cmdlet **Remove-AzKeyVaultCertificateContact** exclui um contato que está registrado para notificações de certificado de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="e7a7f-109">The **Remove-AzKeyVaultCertificateContact** cmdlet deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="e7a7f-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e7a7f-110">EXAMPLES</span></span>

### <span data-ttu-id="e7a7f-111">Exemplo 1: remover um contato de certificado</span><span class="sxs-lookup"><span data-stu-id="e7a7f-111">Example 1: Remove a certificate contact</span></span>
```powershell
PS C:\> Remove-AzKeyVaultCertificateContact -VaultName "Contoso01" -EmailAddress "patti.fuller@contoso.com" -PassThru

Email               VaultName
-----               ---------
user1@microsoft.com mvault2
user2@microsoft.com mvault2
user3@microsoft.com mvault2
user4@microsoft.com mvault2
```

<span data-ttu-id="e7a7f-112">Esse comando Remove Patti pereira como um contato de certificado para o cofre de chaves Contoso01.</span><span class="sxs-lookup"><span data-stu-id="e7a7f-112">This command removes Patti Fuller as a certificate contact for the Contoso01 key vault.</span></span>  <span data-ttu-id="e7a7f-113">Se PassThru for especificado, o cmdlet retornará a lista de contatos de certificado restantes.</span><span class="sxs-lookup"><span data-stu-id="e7a7f-113">If PassThru is specified, the cmdlet returns the list of remaining certificate contacts.</span></span>

## <span data-ttu-id="e7a7f-114">OS</span><span class="sxs-lookup"><span data-stu-id="e7a7f-114">PARAMETERS</span></span>

### <span data-ttu-id="e7a7f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7a7f-115">-DefaultProfile</span></span>
<span data-ttu-id="e7a7f-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="e7a7f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e7a7f-117">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="e7a7f-117">-EmailAddress</span></span>
<span data-ttu-id="e7a7f-118">Especifica o endereço de email do contato a ser removido.</span><span class="sxs-lookup"><span data-stu-id="e7a7f-118">Specifies the email address of the contact to remove.</span></span>

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

### <span data-ttu-id="e7a7f-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e7a7f-119">-InputObject</span></span>
<span data-ttu-id="e7a7f-120">Objeto do keyvault.</span><span class="sxs-lookup"><span data-stu-id="e7a7f-120">KeyVault object.</span></span>

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

### <span data-ttu-id="e7a7f-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e7a7f-121">-PassThru</span></span>
<span data-ttu-id="e7a7f-122">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="e7a7f-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e7a7f-123">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="e7a7f-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e7a7f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e7a7f-124">-ResourceId</span></span>
<span data-ttu-id="e7a7f-125">ID do recurso do keyvault.</span><span class="sxs-lookup"><span data-stu-id="e7a7f-125">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="e7a7f-126">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="e7a7f-126">-VaultName</span></span>
<span data-ttu-id="e7a7f-127">Especifica o nome de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="e7a7f-127">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e7a7f-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e7a7f-128">-Confirm</span></span>
<span data-ttu-id="e7a7f-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7a7f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7a7f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7a7f-130">-WhatIf</span></span>
<span data-ttu-id="e7a7f-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e7a7f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7a7f-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e7a7f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7a7f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7a7f-133">CommonParameters</span></span>
<span data-ttu-id="e7a7f-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7a7f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7a7f-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e7a7f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7a7f-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e7a7f-136">INPUTS</span></span>

### <span data-ttu-id="e7a7f-137">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="e7a7f-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="e7a7f-138">System. String</span><span class="sxs-lookup"><span data-stu-id="e7a7f-138">System.String</span></span>

## <span data-ttu-id="e7a7f-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e7a7f-139">OUTPUTS</span></span>

### <span data-ttu-id="e7a7f-140">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="e7a7f-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="e7a7f-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e7a7f-141">NOTES</span></span>

## <span data-ttu-id="e7a7f-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e7a7f-142">RELATED LINKS</span></span>

[<span data-ttu-id="e7a7f-143">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="e7a7f-143">Add-AzKeyVaultCertificateContact</span></span>](./Add-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="e7a7f-144">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="e7a7f-144">Get-AzKeyVaultCertificateContact</span></span>](./Get-AzKeyVaultCertificateContact.md)

