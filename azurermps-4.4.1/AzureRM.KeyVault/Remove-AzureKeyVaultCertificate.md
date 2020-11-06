---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 34985F06-4D8D-463B-B113-972666D18485
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificate.md
ms.openlocfilehash: 9a33d4efdd82ad03b94ea9a7e862fb5e13eb30d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441042"
---
# <span data-ttu-id="3b636-101">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="3b636-101">Remove-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="3b636-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3b636-102">SYNOPSIS</span></span>
<span data-ttu-id="3b636-103">Remove um certificado de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="3b636-103">Removes a certificate from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b636-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3b636-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-Force] [-InRemovedState] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b636-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3b636-105">DESCRIPTION</span></span>
<span data-ttu-id="3b636-106">O cmdlet **Remove-AzureKeyVaultCertificate** remove um certificado de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="3b636-106">The **Remove-AzureKeyVaultCertificate** cmdlet removes a certificate from a key vault.</span></span>

## <span data-ttu-id="3b636-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3b636-107">EXAMPLES</span></span>

### <span data-ttu-id="3b636-108">Exemplo 1: remover um certificado</span><span class="sxs-lookup"><span data-stu-id="3b636-108">Example 1: Remove a certificate</span></span>
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

<span data-ttu-id="3b636-109">Esse comando Remove o certificado chamado SelfSigned01 do cofre de chaves chamado ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="3b636-109">This command removes the certificate named SelfSigned01 from the key vault named ContosoKV01.</span></span>
<span data-ttu-id="3b636-110">Esse comando especifica o parâmetro *Force* .</span><span class="sxs-lookup"><span data-stu-id="3b636-110">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="3b636-111">Portanto, o cmdlet não solicita confirmação.</span><span class="sxs-lookup"><span data-stu-id="3b636-111">Therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="3b636-112">Exemplo 3: limpar o certificado excluído do cofre de chaves permanentemente</span><span class="sxs-lookup"><span data-stu-id="3b636-112">Example 3: Purge the deleted certificate from the key vault permanently</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="3b636-113">Esse comando remove permanentemente o certificado chamado ' MyCert ' do cofre de chaves chamado ' contoso '.</span><span class="sxs-lookup"><span data-stu-id="3b636-113">This command permanently removes the certificate named 'MyCert' from the key vault named 'Contoso'.</span></span>
<span data-ttu-id="3b636-114">A execução deste cmdlet requer a permissão ' limpar ', que deve ter sido concedida anteriormente e explicitamente ao usuário neste cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="3b636-114">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user on this key vault.</span></span>

## <span data-ttu-id="3b636-115">OS</span><span class="sxs-lookup"><span data-stu-id="3b636-115">PARAMETERS</span></span>

### <span data-ttu-id="3b636-116">-Force</span><span class="sxs-lookup"><span data-stu-id="3b636-116">-Force</span></span>
<span data-ttu-id="3b636-117">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="3b636-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3b636-118">-Inremovestate</span><span class="sxs-lookup"><span data-stu-id="3b636-118">-InRemovedState</span></span>
<span data-ttu-id="3b636-119">Se presente, remove permanentemente o certificado excluído anteriormente.</span><span class="sxs-lookup"><span data-stu-id="3b636-119">If present, removes the previously deleted certificate permanently.</span></span>

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

### <span data-ttu-id="3b636-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="3b636-120">-Name</span></span>
<span data-ttu-id="3b636-121">Especifica o nome do certificado que este cmdlet Remove de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="3b636-121">Specifies the name of the certificate that this cmdlet removes from a key vault.</span></span>
<span data-ttu-id="3b636-122">Esse cmdlet constrói o nome de domínio totalmente qualificado (FQDN) de um certificado com base no nome que esse parâmetro especifica, o nome do cofre de chaves e o ambiente atual.</span><span class="sxs-lookup"><span data-stu-id="3b636-122">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

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

### <span data-ttu-id="3b636-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3b636-123">-PassThru</span></span>
<span data-ttu-id="3b636-124">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="3b636-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3b636-125">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="3b636-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3b636-126">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="3b636-126">-VaultName</span></span>
<span data-ttu-id="3b636-127">Especifica o nome do cofre de chaves do qual esse cmdlet Remove um certificado.</span><span class="sxs-lookup"><span data-stu-id="3b636-127">Specifies the name of the key vault from which this cmdlet removes a certificate.</span></span>
<span data-ttu-id="3b636-128">Esse cmdlet constrói o FQDN de um cofre de chaves com base no nome especificado pelo parâmetro e no seu ambiente atual.</span><span class="sxs-lookup"><span data-stu-id="3b636-128">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="3b636-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3b636-129">-Confirm</span></span>
<span data-ttu-id="3b636-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b636-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b636-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b636-131">-WhatIf</span></span>
<span data-ttu-id="3b636-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3b636-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b636-133">O cmdlet não é executado. Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3b636-133">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b636-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3b636-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b636-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b636-135">-DefaultProfile</span></span>
<span data-ttu-id="3b636-136">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3b636-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b636-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b636-137">CommonParameters</span></span>
<span data-ttu-id="3b636-138">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b636-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b636-139">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b636-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b636-140">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3b636-140">INPUTS</span></span>

## <span data-ttu-id="3b636-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3b636-141">OUTPUTS</span></span>

### <span data-ttu-id="3b636-142">Microsoft. Azure. Commands. keyvault. Models. CertificateBundle</span><span class="sxs-lookup"><span data-stu-id="3b636-142">Microsoft.Azure.Commands.KeyVault.Models.CertificateBundle</span></span>

## <span data-ttu-id="3b636-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3b636-143">NOTES</span></span>

## <span data-ttu-id="3b636-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3b636-144">RELATED LINKS</span></span>

[<span data-ttu-id="3b636-145">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="3b636-145">Add-AzureKeyVaultCertificate</span></span>](./Add-AzureKeyVaultCertificate.md)

[<span data-ttu-id="3b636-146">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="3b636-146">Get-AzureKeyVaultCertificate</span></span>](./Get-AzureKeyVaultCertificate.md)

[<span data-ttu-id="3b636-147">Import-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="3b636-147">Import-AzureKeyVaultCertificate</span></span>](./Import-AzureKeyVaultCertificate.md)

[<span data-ttu-id="3b636-148">Desfazer-AzureKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="3b636-148">Undo-AzureKeyVaultCertificateRemoval</span></span>](./Undo-AzureKeyVaultCertificateRemoval.md)
