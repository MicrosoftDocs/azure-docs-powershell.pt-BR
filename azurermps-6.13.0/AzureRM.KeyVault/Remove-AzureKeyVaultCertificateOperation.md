---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2659C06A-AE5B-4F7B-B9EF-069A74E12560
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificateoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificateOperation.md
ms.openlocfilehash: 9bd02d11f0d8c6f60638b506fd09c953bc861b9d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430915"
---
# <span data-ttu-id="6c176-101">Remove-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="6c176-101">Remove-AzureKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="6c176-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6c176-102">SYNOPSIS</span></span>
<span data-ttu-id="6c176-103">Exclui uma operação de certificado de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="6c176-103">Deletes a certificate operation from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c176-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6c176-104">SYNTAX</span></span>

### <span data-ttu-id="6c176-105">Assume</span><span class="sxs-lookup"><span data-stu-id="6c176-105">Default</span></span>
```
Remove-AzureKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c176-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="6c176-106">InputObject</span></span>
```
Remove-AzureKeyVaultCertificateOperation [-InputObject] <PSKeyVaultCertificateOperation> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c176-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6c176-107">DESCRIPTION</span></span>
<span data-ttu-id="6c176-108">O cmdlet **Remove-AzureKeyVaultCertificateOperation** exclui uma operação de certificado de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="6c176-108">The **Remove-AzureKeyVaultCertificateOperation** cmdlet deletes a certificate operation from a key vault.</span></span>

## <span data-ttu-id="6c176-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6c176-109">EXAMPLES</span></span>

### <span data-ttu-id="6c176-110">Exemplo 1: remover uma operação de certificado</span><span class="sxs-lookup"><span data-stu-id="6c176-110">Example 1: Remove a certificate operation</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultCertificateOperation -VaultName "ContosoKV01" -Name "TestCert01" -Force

Id                        : https://contosokv01.vault.azure.net/certificates/testcert01/pending
Status                    : completed
StatusDetails             :
RequestId                 : f5dfd2ae486149a594dc98e800dceaaa
Target                    : https://contosokv01.vault.azure.net/certificates/testcert01
Issuer                    : Self
CancellationRequested     : False
CertificateSigningRequest : MIICpjCCAY4CAQAwFjEUMBIGA1UEAxMLY29udG9zby5jb20wggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQC73w3VRBOlgJ5Od1PjDh+2ytngNZp+ZP4fkuX8K1Ti5LA6Ih7eWx1fgAN/iTb6l
                            5K6LvAIJvsTNVePMNxfSdaEIJ70Inm45wVU4A/kf+UxQWAYVMsBrLtDFWxnVhzf6n7RGYke6HLBj3j5ASb9g+olSs6eON25ibF0t+u6JC+sIR0LmVGar9Q0eZys1rdfzJBIKq+laOM7z2pJijb5ANqve9
                            i7rH5mnhQk4V8WsRstOhYR9jgLqSSxokDoeaBClIOidSBYqVc1yNv4ASe1UWUCR7ZK6OQXiecNWSWPmgWEyawu6AR9eb1YotCr2ScheMOCxlm3103luitxrd8A7kMjAgMBAAGgSzBJBgkqhkiG9w0BCQ4
                            xPDA6MA4GA1UdDwEB/wQEAwIFoDAdBgNVHSUEFjAUBggrBgEFBQcDAQYIKwYBBQUHAwIwCQYDVR0TBAIwADANBgkqhkiG9w0BAQsFAAOCAQEAIHhsDJV37PKi8hor5eQf7+Tct1preIvSwqV0NF6Uo7O6
                            YnC9Py7Wp7CHfKzuqeptUk2Tsu7B5dHB+o9Ypeeqw8fWhTN0GFGRKO7WjZQlDqL+lRNcjlFSaP022oIP0kmvVhBcmZqRQlALXccAaxEclFA/3y/aNj2gwWeKpH/pwAkZ39zMEzpQCaRfnQk7e3l4MV8cf
                            eC2HPYdRWkXxAeDcNPxBuVmKy49AzYvly+APNVDU3v66gxl3fIKrGRsKi2Cp/nO5rBxG2h8t+0Za4l/HJ7ZWR9wKbd/xg7JhdZZFVBxMHYzw8KQ0ys13x8HY+PXU92Y7yD3uC2Rcj+zbAf+Kg==
                            ==
ErrorCode                 :
ErrorMessage              :
Name                      :
VaultName                 :
```

<span data-ttu-id="6c176-111">Esse comando Remove a operação de certificado chamada TestCert01 do cofre da chave ContosoKV01 sem solicitar confirmação.</span><span class="sxs-lookup"><span data-stu-id="6c176-111">This command removes the certificate operation named TestCert01 from the ContosoKV01 key vault without prompting for confirmation.</span></span>

## <span data-ttu-id="6c176-112">OS</span><span class="sxs-lookup"><span data-stu-id="6c176-112">PARAMETERS</span></span>

### <span data-ttu-id="6c176-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c176-113">-DefaultProfile</span></span>
<span data-ttu-id="6c176-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="6c176-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6c176-115">-Force</span><span class="sxs-lookup"><span data-stu-id="6c176-115">-Force</span></span>
<span data-ttu-id="6c176-116">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="6c176-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6c176-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6c176-117">-InputObject</span></span>
<span data-ttu-id="6c176-118">Objeto Operation</span><span class="sxs-lookup"><span data-stu-id="6c176-118">Operation object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6c176-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="6c176-119">-Name</span></span>
<span data-ttu-id="6c176-120">Especifica o nome de um certificado.</span><span class="sxs-lookup"><span data-stu-id="6c176-120">Specifies the name of a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c176-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6c176-121">-PassThru</span></span>
<span data-ttu-id="6c176-122">Retorna um objeto que representa o item com o qual você está trabalhando.</span><span class="sxs-lookup"><span data-stu-id="6c176-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6c176-123">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="6c176-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6c176-124">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="6c176-124">-VaultName</span></span>
<span data-ttu-id="6c176-125">Especifica o nome de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="6c176-125">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c176-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6c176-126">-Confirm</span></span>
<span data-ttu-id="6c176-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c176-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c176-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c176-128">-WhatIf</span></span>
<span data-ttu-id="6c176-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6c176-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c176-130">O cmdlet não é executado. Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6c176-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c176-131">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6c176-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c176-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c176-132">CommonParameters</span></span>
<span data-ttu-id="6c176-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c176-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c176-134">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c176-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c176-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6c176-135">INPUTS</span></span>

### <span data-ttu-id="6c176-136">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="6c176-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span></span>
<span data-ttu-id="6c176-137">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6c176-137">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="6c176-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6c176-138">OUTPUTS</span></span>

### <span data-ttu-id="6c176-139">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="6c176-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="6c176-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6c176-140">NOTES</span></span>

## <span data-ttu-id="6c176-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6c176-141">RELATED LINKS</span></span>

[<span data-ttu-id="6c176-142">Get-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="6c176-142">Get-AzureKeyVaultCertificateOperation</span></span>](./Get-AzureKeyVaultCertificateOperation.md)

[<span data-ttu-id="6c176-143">Parar-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="6c176-143">Stop-AzureKeyVaultCertificateOperation</span></span>](./Stop-AzureKeyVaultCertificateOperation.md)
