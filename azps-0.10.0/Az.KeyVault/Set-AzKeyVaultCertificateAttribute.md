---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 3BD243C7-A40E-4061-93FF-DDE7DECAD0A7
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/set-AzKeyvaultcertificateattribute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificateAttribute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificateAttribute.md
ms.openlocfilehash: 9297e523e623542c19df1915d3da29d9e39cec40
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776651"
---
# <span data-ttu-id="abc4c-101">Set-AzKeyVaultCertificateAttribute</span><span class="sxs-lookup"><span data-stu-id="abc4c-101">Set-AzKeyVaultCertificateAttribute</span></span>

## <span data-ttu-id="abc4c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="abc4c-102">SYNOPSIS</span></span>
<span data-ttu-id="abc4c-103">Modifica atributos editáveis de um certificado.</span><span class="sxs-lookup"><span data-stu-id="abc4c-103">Modifies editable attributes of a certificate.</span></span>

## <span data-ttu-id="abc4c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="abc4c-104">SYNTAX</span></span>

```
Set-AzKeyVaultCertificateAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-Enable <Boolean>] [-Tag <Hashtable>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abc4c-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="abc4c-105">DESCRIPTION</span></span>
<span data-ttu-id="abc4c-106">O cmdlet **set-AzKeyVaultCertificateAttribute** modifica os atributos editáveis de um certificado.</span><span class="sxs-lookup"><span data-stu-id="abc4c-106">The **Set-AzKeyVaultCertificateAttribute** cmdlet modifies the editable attributes of a certificate.</span></span>

## <span data-ttu-id="abc4c-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="abc4c-107">EXAMPLES</span></span>

### <span data-ttu-id="abc4c-108">Exemplo 1: modificar as marcas associadas a um certificado</span><span class="sxs-lookup"><span data-stu-id="abc4c-108">Example 1: Modify the tags associated with a certificate</span></span>
```
PS C:\>$Tags = @{ "Team" = "Azure" ; "Role" = "Engg" }
PS C:\> Set-AzKeyVaultCertificateAttribute -VaultName "ContosoKV01" -Name "TestCert01" -Tag $Tags
PS C:\> Get-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "TestCert01"
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

<span data-ttu-id="abc4c-109">O primeiro comando atribui uma matriz de pares de chave/valor à variável $Tags.</span><span class="sxs-lookup"><span data-stu-id="abc4c-109">The first command assigns an array of key/value pairs to the $Tags variable.</span></span>

<span data-ttu-id="abc4c-110">O segundo comando define o valor de marcas do certificado chamado TestCert01 para ser $Tags.</span><span class="sxs-lookup"><span data-stu-id="abc4c-110">The second command sets the tags value of the certificate named TestCert01 to be $Tags.</span></span>

<span data-ttu-id="abc4c-111">O comando final exibe o certificado TestCert01 usando o cmdlet Get-AzKeyVaultCertificate para verificar a operação.</span><span class="sxs-lookup"><span data-stu-id="abc4c-111">The final command displays the TestCert01 certificate by using the Get-AzKeyVaultCertificate cmdlet to verify the operation.</span></span>

## <span data-ttu-id="abc4c-112">OS</span><span class="sxs-lookup"><span data-stu-id="abc4c-112">PARAMETERS</span></span>

### <span data-ttu-id="abc4c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abc4c-113">-DefaultProfile</span></span>
<span data-ttu-id="abc4c-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="abc4c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abc4c-115">-Habilitar</span><span class="sxs-lookup"><span data-stu-id="abc4c-115">-Enable</span></span>
<span data-ttu-id="abc4c-116">Indica se um certificado deve ser habilitado ou desabilitado.</span><span class="sxs-lookup"><span data-stu-id="abc4c-116">Indicates whether to enable or disable a certificate.</span></span>
<span data-ttu-id="abc4c-117">Especifique $True para habilitar ou $False para desabilitar.</span><span class="sxs-lookup"><span data-stu-id="abc4c-117">Specify $True to enable or $False to disable.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="abc4c-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="abc4c-118">-Name</span></span>
<span data-ttu-id="abc4c-119">Especifica o nome do certificado a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="abc4c-119">Specifies the name of the certificate to modify.</span></span> <span data-ttu-id="abc4c-120">Esse cmdlet constrói o FQDN de um certificado com base no nome do cofre de chaves, no ambiente selecionado atualmente, no nome do certificado e na versão do certificado.</span><span class="sxs-lookup"><span data-stu-id="abc4c-120">This cmdlet constructs the FQDN of a certificate based on the key vault name, your currently selected environment, the certificate name, and the certificate version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abc4c-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="abc4c-121">-PassThru</span></span>
<span data-ttu-id="abc4c-122">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="abc4c-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="abc4c-123">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="abc4c-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="abc4c-124">-Marca</span><span class="sxs-lookup"><span data-stu-id="abc4c-124">-Tag</span></span>
<span data-ttu-id="abc4c-125">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="abc4c-125">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="abc4c-126">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="abc4c-126">For example:</span></span>

<span data-ttu-id="abc4c-127">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="abc4c-127">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abc4c-128">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="abc4c-128">-VaultName</span></span>
<span data-ttu-id="abc4c-129">Especifica o nome do cofre de chaves no qual esse cmdlet modifica um certificado.</span><span class="sxs-lookup"><span data-stu-id="abc4c-129">Specifies the key vault name in which this cmdlet modifies a certificate.</span></span>
<span data-ttu-id="abc4c-130">Esse cmdlet constrói o FQDN de um cofre de chaves com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="abc4c-130">This cmdlet constructs the FQDN of a key vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abc4c-131">-Versão</span><span class="sxs-lookup"><span data-stu-id="abc4c-131">-Version</span></span>
<span data-ttu-id="abc4c-132">Especifica a versão de um certificado.</span><span class="sxs-lookup"><span data-stu-id="abc4c-132">Specifies the version of a certificate.</span></span>
<span data-ttu-id="abc4c-133">Esse cmdlet constrói o FQDN de um certificado com base no nome do cofre de chaves, no ambiente selecionado atualmente, no nome do certificado e na versão do certificado.</span><span class="sxs-lookup"><span data-stu-id="abc4c-133">This cmdlet constructs the FQDN of a certificate based on the key vault name, your currently selected environment, the certificate name, and the certificate version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: CertificateVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abc4c-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="abc4c-134">-Confirm</span></span>
<span data-ttu-id="abc4c-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="abc4c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abc4c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abc4c-136">-WhatIf</span></span>
<span data-ttu-id="abc4c-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="abc4c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abc4c-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="abc4c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abc4c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abc4c-139">CommonParameters</span></span>
<span data-ttu-id="abc4c-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abc4c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abc4c-141">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abc4c-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abc4c-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="abc4c-142">INPUTS</span></span>

### <span data-ttu-id="abc4c-143">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="abc4c-143">None</span></span>
<span data-ttu-id="abc4c-144">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="abc4c-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="abc4c-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="abc4c-145">OUTPUTS</span></span>

### <span data-ttu-id="abc4c-146">Microsoft. Azure. Commands. keyvault. Models. KeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="abc4c-146">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificate</span></span>

## <span data-ttu-id="abc4c-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="abc4c-147">NOTES</span></span>

## <span data-ttu-id="abc4c-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="abc4c-148">RELATED LINKS</span></span>

[<span data-ttu-id="abc4c-149">Add-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="abc4c-149">Add-AzKeyVaultCertificate</span></span>](./Add-AzKeyVaultCertificate.md)