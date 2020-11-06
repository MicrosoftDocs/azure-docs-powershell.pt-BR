---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 34985F06-4D8D-463B-B113-972666D18485
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificate.md
ms.openlocfilehash: 6c8fcc5476ea2defda78ea03cc1acce7b7e3dea9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93439864"
---
# <span data-ttu-id="f5800-101">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="f5800-101">Remove-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="f5800-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f5800-102">SYNOPSIS</span></span>
<span data-ttu-id="f5800-103">Remove um certificado de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="f5800-103">Removes a certificate from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5800-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f5800-104">SYNTAX</span></span>

### <span data-ttu-id="f5800-105">ByVaultNameAndName (padrão)</span><span class="sxs-lookup"><span data-stu-id="f5800-105">ByVaultNameAndName (Default)</span></span>
```
Remove-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-InRemovedState] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5800-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="f5800-106">ByObject</span></span>
```
Remove-AzureKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [-InRemovedState] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5800-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f5800-107">DESCRIPTION</span></span>
<span data-ttu-id="f5800-108">O cmdlet **Remove-AzureKeyVaultCertificate** remove um certificado de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="f5800-108">The **Remove-AzureKeyVaultCertificate** cmdlet removes a certificate from a key vault.</span></span>

## <span data-ttu-id="f5800-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f5800-109">EXAMPLES</span></span>

### <span data-ttu-id="f5800-110">Exemplo 1: remover um certificado</span><span class="sxs-lookup"><span data-stu-id="f5800-110">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "SelfSigned01" -PassThru -Force
Name        : selfSigned01
Certificate : 
Thumbprint  : 
Tags        : 
Enabled     : True
Created     : 2/8/2016 11:29:33 PM
Updated     : 2/8/2016 11:29:33 PM
```

<span data-ttu-id="f5800-111">Esse comando Remove o certificado chamado SelfSigned01 do cofre de chaves chamado ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="f5800-111">This command removes the certificate named SelfSigned01 from the key vault named ContosoKV01.</span></span>
<span data-ttu-id="f5800-112">Esse comando especifica o parâmetro *Force* .</span><span class="sxs-lookup"><span data-stu-id="f5800-112">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="f5800-113">Portanto, o cmdlet não solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="f5800-113">Therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="f5800-114">Exemplo 3: limpar o certificado excluído do cofre de chaves permanentemente</span><span class="sxs-lookup"><span data-stu-id="f5800-114">Example 3: Purge the deleted certificate from the key vault permanently</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="f5800-115">Esse comando remove permanentemente o certificado chamado ' MyCert ' do cofre de chaves chamado ' contoso '.</span><span class="sxs-lookup"><span data-stu-id="f5800-115">This command permanently removes the certificate named 'MyCert' from the key vault named 'Contoso'.</span></span>
<span data-ttu-id="f5800-116">A execução deste cmdlet requer a permissão ' limpar ', que deve ter sido concedida anteriormente e explicitamente ao usuário neste cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="f5800-116">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user on this key vault.</span></span>

## <span data-ttu-id="f5800-117">OS</span><span class="sxs-lookup"><span data-stu-id="f5800-117">PARAMETERS</span></span>

### <span data-ttu-id="f5800-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5800-118">-DefaultProfile</span></span>
<span data-ttu-id="f5800-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="f5800-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f5800-120">-Force</span><span class="sxs-lookup"><span data-stu-id="f5800-120">-Force</span></span>
<span data-ttu-id="f5800-121">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="f5800-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f5800-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f5800-122">-InputObject</span></span>
<span data-ttu-id="f5800-123">Objeto de certificado.</span><span class="sxs-lookup"><span data-stu-id="f5800-123">Certificate Object.</span></span>

```yaml
Type: PSKeyVaultCertificateIdentityItem
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f5800-124">-Inremovestate</span><span class="sxs-lookup"><span data-stu-id="f5800-124">-InRemovedState</span></span>
<span data-ttu-id="f5800-125">Se presente, remove permanentemente o certificado excluído anteriormente</span><span class="sxs-lookup"><span data-stu-id="f5800-125">If present, removes the previously deleted certificate permanently</span></span>

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

### <span data-ttu-id="f5800-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="f5800-126">-Name</span></span>
<span data-ttu-id="f5800-127">Especifica o nome do certificado que este cmdlet Remove de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="f5800-127">Specifies the name of the certificate that this cmdlet removes from a key vault.</span></span>
<span data-ttu-id="f5800-128">Esse cmdlet constrói o nome de domínio totalmente qualificado (FQDN) de um certificado com base no nome que esse parâmetro especifica, o nome do cofre de chaves e o ambiente atual.</span><span class="sxs-lookup"><span data-stu-id="f5800-128">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultNameAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5800-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f5800-129">-PassThru</span></span>
<span data-ttu-id="f5800-130">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="f5800-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f5800-131">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="f5800-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f5800-132">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="f5800-132">-VaultName</span></span>
<span data-ttu-id="f5800-133">Especifica o nome do cofre de chaves do qual esse cmdlet Remove um certificado.</span><span class="sxs-lookup"><span data-stu-id="f5800-133">Specifies the name of the key vault from which this cmdlet removes a certificate.</span></span>
<span data-ttu-id="f5800-134">Esse cmdlet constrói o FQDN de um cofre de chaves com base no nome especificado pelo parâmetro e no seu ambiente atual.</span><span class="sxs-lookup"><span data-stu-id="f5800-134">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultNameAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5800-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f5800-135">-Confirm</span></span>
<span data-ttu-id="f5800-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5800-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5800-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5800-137">-WhatIf</span></span>
<span data-ttu-id="f5800-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f5800-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5800-139">O cmdlet não é executado. Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f5800-139">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5800-140">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f5800-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5800-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5800-141">CommonParameters</span></span>
<span data-ttu-id="f5800-142">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5800-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5800-143">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5800-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5800-144">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f5800-144">INPUTS</span></span>

### <span data-ttu-id="f5800-145">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="f5800-145">None</span></span>
<span data-ttu-id="f5800-146">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="f5800-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f5800-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f5800-147">OUTPUTS</span></span>

### <span data-ttu-id="f5800-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="f5800-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span></span>

## <span data-ttu-id="f5800-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f5800-149">NOTES</span></span>

## <span data-ttu-id="f5800-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f5800-150">RELATED LINKS</span></span>

[<span data-ttu-id="f5800-151">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="f5800-151">Add-AzureKeyVaultCertificate</span></span>](./Add-AzureKeyVaultCertificate.md)

[<span data-ttu-id="f5800-152">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="f5800-152">Get-AzureKeyVaultCertificate</span></span>](./Get-AzureKeyVaultCertificate.md)

[<span data-ttu-id="f5800-153">Import-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="f5800-153">Import-AzureKeyVaultCertificate</span></span>](./Import-AzureKeyVaultCertificate.md)

[<span data-ttu-id="f5800-154">Desfazer-AzureKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="f5800-154">Undo-AzureKeyVaultCertificateRemoval</span></span>](./Undo-AzureKeyVaultCertificateRemoval.md)
