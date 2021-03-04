---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 35FAA57F-B2BD-4E43-8238-12F7A8269E4D
online version: https://docs.microsoft.com/powershell/module/az.keyvault/remove-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateContact.md
ms.openlocfilehash: fa229e9f18b628430cc58388919fb3bfcda74704
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901477"
---
# <span data-ttu-id="74164-101">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="74164-101">Remove-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="74164-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74164-102">SYNOPSIS</span></span>
<span data-ttu-id="74164-103">Exclui um contato registrado para notificações de certificado de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="74164-103">Deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="74164-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="74164-104">SYNTAX</span></span>

### <span data-ttu-id="74164-105">ByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="74164-105">ByName (Default)</span></span>
```
Remove-AzKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74164-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="74164-106">ByObject</span></span>
```
Remove-AzKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="74164-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="74164-107">ByResourceId</span></span>
```
Remove-AzKeyVaultCertificateContact [-ResourceId] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74164-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="74164-108">DESCRIPTION</span></span>
<span data-ttu-id="74164-109">O cmdlet **Remove-AzKeyVaultCertificateContact** exclui um contato registrado para notificações de certificado de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="74164-109">The **Remove-AzKeyVaultCertificateContact** cmdlet deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="74164-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="74164-110">EXAMPLES</span></span>

### <span data-ttu-id="74164-111">Exemplo 1: Remover um contato de certificado</span><span class="sxs-lookup"><span data-stu-id="74164-111">Example 1: Remove a certificate contact</span></span>
```powershell
PS C:\> Remove-AzKeyVaultCertificateContact -VaultName "Contoso01" -EmailAddress "patti.fuller@contoso.com" -PassThru

Email               VaultName
-----               ---------
user1@microsoft.com mvault2
user2@microsoft.com mvault2
user3@microsoft.com mvault2
user4@microsoft.com mvault2
```

<span data-ttu-id="74164-112">Este comando remove Patti Fuller como um contato de certificado para o cofre de chaves Contoso01.</span><span class="sxs-lookup"><span data-stu-id="74164-112">This command removes Patti Fuller as a certificate contact for the Contoso01 key vault.</span></span>  <span data-ttu-id="74164-113">Se PassThru for especificado, o cmdlet retornará a lista de contatos restantes do certificado.</span><span class="sxs-lookup"><span data-stu-id="74164-113">If PassThru is specified, the cmdlet returns the list of remaining certificate contacts.</span></span>

## <span data-ttu-id="74164-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="74164-114">PARAMETERS</span></span>

### <span data-ttu-id="74164-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74164-115">-DefaultProfile</span></span>
<span data-ttu-id="74164-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="74164-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="74164-117">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="74164-117">-EmailAddress</span></span>
<span data-ttu-id="74164-118">Especifica o endereço de email do contato a ser removido.</span><span class="sxs-lookup"><span data-stu-id="74164-118">Specifies the email address of the contact to remove.</span></span>

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

### <span data-ttu-id="74164-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="74164-119">-InputObject</span></span>
<span data-ttu-id="74164-120">Objeto KeyVault.</span><span class="sxs-lookup"><span data-stu-id="74164-120">KeyVault object.</span></span>

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

### <span data-ttu-id="74164-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="74164-121">-PassThru</span></span>
<span data-ttu-id="74164-122">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="74164-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="74164-123">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="74164-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="74164-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="74164-124">-ResourceId</span></span>
<span data-ttu-id="74164-125">ID do Recurso KeyVault.</span><span class="sxs-lookup"><span data-stu-id="74164-125">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="74164-126">-VaultName</span><span class="sxs-lookup"><span data-stu-id="74164-126">-VaultName</span></span>
<span data-ttu-id="74164-127">Especifica o nome de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="74164-127">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="74164-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="74164-128">-Confirm</span></span>
<span data-ttu-id="74164-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74164-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74164-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74164-130">-WhatIf</span></span>
<span data-ttu-id="74164-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="74164-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74164-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="74164-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74164-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74164-133">CommonParameters</span></span>
<span data-ttu-id="74164-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74164-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74164-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="74164-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74164-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="74164-136">INPUTS</span></span>

### <span data-ttu-id="74164-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="74164-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="74164-138">System.String</span><span class="sxs-lookup"><span data-stu-id="74164-138">System.String</span></span>

## <span data-ttu-id="74164-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="74164-139">OUTPUTS</span></span>

### <span data-ttu-id="74164-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="74164-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="74164-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="74164-141">NOTES</span></span>

## <span data-ttu-id="74164-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="74164-142">RELATED LINKS</span></span>

[<span data-ttu-id="74164-143">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="74164-143">Add-AzKeyVaultCertificateContact</span></span>](./Add-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="74164-144">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="74164-144">Get-AzKeyVaultCertificateContact</span></span>](./Get-AzKeyVaultCertificateContact.md)

