---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 35FAA57F-B2BD-4E43-8238-12F7A8269E4D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: aee18adf3530976af4b17ffa15f94624248a7db7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430234"
---
# <span data-ttu-id="4f30c-101">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="4f30c-101">Remove-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="4f30c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4f30c-102">SYNOPSIS</span></span>
<span data-ttu-id="4f30c-103">Exclui um contato registrado para notificações de certificado de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="4f30c-103">Deletes a contact that is registered for certificate notifications from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f30c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4f30c-104">SYNTAX</span></span>

### <span data-ttu-id="4f30c-105">ByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="4f30c-105">ByName (Default)</span></span>
```
Remove-AzureKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f30c-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="4f30c-106">ByObject</span></span>
```
Remove-AzureKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f30c-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4f30c-107">ByResourceId</span></span>
```
Remove-AzureKeyVaultCertificateContact [-ResourceId] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f30c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4f30c-108">DESCRIPTION</span></span>
<span data-ttu-id="4f30c-109">O cmdlet **Remove-AzureKeyVaultCertificateContact** exclui um contato que está registrado para notificações de certificado de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="4f30c-109">The **Remove-AzureKeyVaultCertificateContact** cmdlet deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="4f30c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4f30c-110">EXAMPLES</span></span>

### <span data-ttu-id="4f30c-111">Exemplo 1: remover um contato de certificado</span><span class="sxs-lookup"><span data-stu-id="4f30c-111">Example 1: Remove a certificate contact</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultCertificateContact -VaultName "Contoso01" -EmailAddress "patti.fuller@contoso.com" -PassThru

Email               VaultName
-----               ---------
user1@microsoft.com mvault2
user2@microsoft.com mvault2
user3@microsoft.com mvault2
user4@microsoft.com mvault2
```

<span data-ttu-id="4f30c-112">Esse comando Remove Patti pereira como um contato de certificado para o cofre de chaves Contoso01.</span><span class="sxs-lookup"><span data-stu-id="4f30c-112">This command removes Patti Fuller as a certificate contact for the Contoso01 key vault.</span></span>  <span data-ttu-id="4f30c-113">Se PassThru for especificado, o cmdlet retornará a lista de contatos de certificado restantes.</span><span class="sxs-lookup"><span data-stu-id="4f30c-113">If PassThru is specified, the cmdlet returns the list of remaining certificate contacts.</span></span>

## <span data-ttu-id="4f30c-114">OS</span><span class="sxs-lookup"><span data-stu-id="4f30c-114">PARAMETERS</span></span>

### <span data-ttu-id="4f30c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f30c-115">-DefaultProfile</span></span>
<span data-ttu-id="4f30c-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="4f30c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4f30c-117">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="4f30c-117">-EmailAddress</span></span>
<span data-ttu-id="4f30c-118">Especifica o endereço de email do contato a ser removido.</span><span class="sxs-lookup"><span data-stu-id="4f30c-118">Specifies the email address of the contact to remove.</span></span>

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

### <span data-ttu-id="4f30c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4f30c-119">-InputObject</span></span>
<span data-ttu-id="4f30c-120">Objeto do keyvault.</span><span class="sxs-lookup"><span data-stu-id="4f30c-120">KeyVault object.</span></span>

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

### <span data-ttu-id="4f30c-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4f30c-121">-PassThru</span></span>
<span data-ttu-id="4f30c-122">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="4f30c-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4f30c-123">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="4f30c-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4f30c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4f30c-124">-ResourceId</span></span>
<span data-ttu-id="4f30c-125">ID do recurso do keyvault.</span><span class="sxs-lookup"><span data-stu-id="4f30c-125">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="4f30c-126">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="4f30c-126">-VaultName</span></span>
<span data-ttu-id="4f30c-127">Especifica o nome de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="4f30c-127">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="4f30c-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4f30c-128">-Confirm</span></span>
<span data-ttu-id="4f30c-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f30c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f30c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f30c-130">-WhatIf</span></span>
<span data-ttu-id="4f30c-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4f30c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f30c-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4f30c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f30c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f30c-133">CommonParameters</span></span>
<span data-ttu-id="4f30c-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f30c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f30c-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f30c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f30c-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4f30c-136">INPUTS</span></span>

### <span data-ttu-id="4f30c-137">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="4f30c-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="4f30c-138">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4f30c-138">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="4f30c-139">System. String</span><span class="sxs-lookup"><span data-stu-id="4f30c-139">System.String</span></span>

## <span data-ttu-id="4f30c-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4f30c-140">OUTPUTS</span></span>

### <span data-ttu-id="4f30c-141">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="4f30c-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="4f30c-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4f30c-142">NOTES</span></span>

## <span data-ttu-id="4f30c-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4f30c-143">RELATED LINKS</span></span>

[<span data-ttu-id="4f30c-144">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="4f30c-144">Add-AzureKeyVaultCertificateContact</span></span>](./Add-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="4f30c-145">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="4f30c-145">Get-AzureKeyVaultCertificateContact</span></span>](./Get-AzureKeyVaultCertificateContact.md)

