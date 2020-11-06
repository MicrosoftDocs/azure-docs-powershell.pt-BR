---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 3BD243C7-A40E-4061-93FF-DDE7DECAD0A7
online version: https://go.microsoft.com/fwlink/?LinkId=822861
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificateAttribute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificateAttribute.md
ms.openlocfilehash: b8dac56d55446915af1c9a2f00f71d903f3daf03
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93441547"
---
# <span data-ttu-id="48519-101">Set-AzureKeyVaultCertificateAttribute</span><span class="sxs-lookup"><span data-stu-id="48519-101">Set-AzureKeyVaultCertificateAttribute</span></span>

## <span data-ttu-id="48519-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="48519-102">SYNOPSIS</span></span>
<span data-ttu-id="48519-103">Modifica atributos editáveis de um certificado.</span><span class="sxs-lookup"><span data-stu-id="48519-103">Modifies editable attributes of a certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48519-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="48519-104">SYNTAX</span></span>

```
Set-AzureKeyVaultCertificateAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-Enable <Boolean>] [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48519-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="48519-105">DESCRIPTION</span></span>
<span data-ttu-id="48519-106">O cmdlet **set-AzureKeyVaultCertificateAttribute** modifica os atributos editáveis de um certificado.</span><span class="sxs-lookup"><span data-stu-id="48519-106">The **Set-AzureKeyVaultCertificateAttribute** cmdlet modifies the editable attributes of a certificate.</span></span>

## <span data-ttu-id="48519-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="48519-107">EXAMPLES</span></span>

### <span data-ttu-id="48519-108">Exemplo 1: modificar as marcas associadas a um certificado</span><span class="sxs-lookup"><span data-stu-id="48519-108">Example 1: Modify the tags associated with a certificate</span></span>
```
PS C:\>$Tags = @{ "Team" = "Azure" ; "Role" = "Engg" }
PS C:\> Set-AzureKeyVaultCertificateAttribute -VaultName "ContosoKV01" -Name "TestCert01" -Tag $Tags
PS C:\> Get-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
Name        : "TestCert01"
Certificate : [Subject]
                CN=AZURE

              [Issuer]
                CN=AZURE

              [Serial Number]
                5A2EF60501F241D6A4336841B36FEA41

              [Not Before]
                7/27/2016 6:50:01 PM

              [Not After]
                7/27/2018 7:00:01 PM

              [Thumbprint]
                A565D568082FEE2BE33B356ECC3703C2E9886555

Id          : https://ContosoKV01.vault.azure.net:443/certificates/tt02
KeyId       : https://ContosoKV01.vault.azure.net:443/keys/tt02
SecretId    : https://ContosoKV01.vault.azure.net:443/secrets/tt02
Thumbprint  : A565D568082FEE2BE33B356ECC3703C2E9886555
Tags        : {[Role, Engg], [Team, Azure]}
Enabled     : True
Created     : 7/28/2016 2:00:01 AM
Updated     : 8/1/2016 5:37:48 PM
```

<span data-ttu-id="48519-109">O primeiro comando atribui uma matriz de pares de chave/valor à variável $Tags.</span><span class="sxs-lookup"><span data-stu-id="48519-109">The first command assigns an array of key/value pairs to the $Tags variable.</span></span>

<span data-ttu-id="48519-110">O segundo comando define o valor de marcas do certificado chamado TestCert01 para ser $Tags.</span><span class="sxs-lookup"><span data-stu-id="48519-110">The second command sets the tags value of the certificate named TestCert01 to be $Tags.</span></span>

<span data-ttu-id="48519-111">O comando final exibe o certificado TestCert01 usando o cmdlet Get-AzureKeyVaultCertificate para verificar a operação.</span><span class="sxs-lookup"><span data-stu-id="48519-111">The final command displays the TestCert01 certificate by using the Get-AzureKeyVaultCertificate cmdlet to verify the operation.</span></span>

## <span data-ttu-id="48519-112">OS</span><span class="sxs-lookup"><span data-stu-id="48519-112">PARAMETERS</span></span>

### <span data-ttu-id="48519-113">-Habilitar</span><span class="sxs-lookup"><span data-stu-id="48519-113">-Enable</span></span>
<span data-ttu-id="48519-114">Indica se um certificado deve ser habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="48519-114">Indicates whether to enable or disable a certificate.</span></span>
<span data-ttu-id="48519-115">Especifique $True para habilitar ou $False para desabilitar.</span><span class="sxs-lookup"><span data-stu-id="48519-115">Specify $True to enable or $False to disable.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48519-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="48519-116">-Name</span></span>
<span data-ttu-id="48519-117">Especifica o nome do certificado a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="48519-117">Specifies the name of the certificate to modify.</span></span> <span data-ttu-id="48519-118">Esse cmdlet constrói o FQDN de um certificado com base no nome do cofre de chaves, no ambiente selecionado atualmente, no nome do certificado e na versão do certificado.</span><span class="sxs-lookup"><span data-stu-id="48519-118">This cmdlet constructs the FQDN of a certificate based on the key vault name, your currently selected environment, the certificate name, and the certificate version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48519-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="48519-119">-PassThru</span></span>
<span data-ttu-id="48519-120">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="48519-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="48519-121">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="48519-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="48519-122">-Marca</span><span class="sxs-lookup"><span data-stu-id="48519-122">-Tag</span></span>
<span data-ttu-id="48519-123">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="48519-123">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="48519-124">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="48519-124">For example:</span></span>

<span data-ttu-id="48519-125">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="48519-125">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48519-126">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="48519-126">-VaultName</span></span>
<span data-ttu-id="48519-127">Especifica o nome do cofre de chaves no qual esse cmdlet modifica um certificado.</span><span class="sxs-lookup"><span data-stu-id="48519-127">Specifies the key vault name in which this cmdlet modifies a certificate.</span></span>
<span data-ttu-id="48519-128">Esse cmdlet constrói o FQDN de um cofre de chaves com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="48519-128">This cmdlet constructs the FQDN of a key vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="48519-129">-Versão</span><span class="sxs-lookup"><span data-stu-id="48519-129">-Version</span></span>
<span data-ttu-id="48519-130">Especifica a versão de um certificado.</span><span class="sxs-lookup"><span data-stu-id="48519-130">Specifies the version of a certificate.</span></span>
<span data-ttu-id="48519-131">Esse cmdlet constrói o FQDN de um certificado com base no nome do cofre de chaves, no ambiente selecionado atualmente, no nome do certificado e na versão do certificado.</span><span class="sxs-lookup"><span data-stu-id="48519-131">This cmdlet constructs the FQDN of a certificate based on the key vault name, your currently selected environment, the certificate name, and the certificate version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CertificateVersion

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48519-132">-Confirme</span><span class="sxs-lookup"><span data-stu-id="48519-132">-Confirm</span></span>
<span data-ttu-id="48519-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="48519-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48519-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48519-134">-WhatIf</span></span>
<span data-ttu-id="48519-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="48519-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48519-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="48519-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48519-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48519-137">-DefaultProfile</span></span>
<span data-ttu-id="48519-138">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="48519-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48519-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48519-139">CommonParameters</span></span>
<span data-ttu-id="48519-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48519-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48519-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48519-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48519-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="48519-142">INPUTS</span></span>

## <span data-ttu-id="48519-143">EXIBE</span><span class="sxs-lookup"><span data-stu-id="48519-143">OUTPUTS</span></span>

### <span data-ttu-id="48519-144">Microsoft. Azure. Commands. keyvault. Models. KeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="48519-144">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificate</span></span>

## <span data-ttu-id="48519-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="48519-145">NOTES</span></span>

## <span data-ttu-id="48519-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="48519-146">RELATED LINKS</span></span>

[<span data-ttu-id="48519-147">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="48519-147">Add-AzureKeyVaultCertificate</span></span>](./Add-AzureKeyVaultCertificate.md)
