---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 0743C43D-2A1F-4950-B0F3-1FED4014EEC5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificateoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateOperation.md
ms.openlocfilehash: bc5b7b47c5567867a857ab32fe34c287e896ae75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93433250"
---
# <span data-ttu-id="301e6-101">Get-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="301e6-101">Get-AzureKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="301e6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="301e6-102">SYNOPSIS</span></span>
<span data-ttu-id="301e6-103">Obtém o status de uma operação de certificado.</span><span class="sxs-lookup"><span data-stu-id="301e6-103">Gets the status of a certificate operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="301e6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="301e6-104">SYNTAX</span></span>

### <span data-ttu-id="301e6-105">ByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="301e6-105">ByName (Default)</span></span>
```
Get-AzureKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="301e6-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="301e6-106">ByInputObject</span></span>
```
Get-AzureKeyVaultCertificateOperation [-InputObject] <PSKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="301e6-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="301e6-107">DESCRIPTION</span></span>
<span data-ttu-id="301e6-108">O cmdlet **Get-AzureKeyVaultCertificateOperation** Obtém o status de uma operação de certificado.</span><span class="sxs-lookup"><span data-stu-id="301e6-108">The **Get-AzureKeyVaultCertificateOperation** cmdlet gets the status of a certificate operation.</span></span>

## <span data-ttu-id="301e6-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="301e6-109">EXAMPLES</span></span>

### <span data-ttu-id="301e6-110">Exemplo 1: obter o status de uma operação de certificado</span><span class="sxs-lookup"><span data-stu-id="301e6-110">Example 1: Get the status of a certificate operation</span></span>
```powershell
PS C:\> Get-AzureKeyVaultCertificateOperation -VaultName "contosoKV01" -Name "TestCert01"

Id                        : https://contosoKV01.vault.azure.net/certificates/TestCert01/pending
Status                    : inProgress
StatusDetails             : Pending certificate created. Certificate request is in progress. This may take some time
                            based on the issuer provider. Please check again later.
RequestId                 : 32a63e80568442a2892dafb9f7cf366t
Target                    :
Issuer                    : Self
CancellationRequested     : False
CertificateSigningRequest : MIICpjCCAY4CAQAwFjEUMBIGA1UEAxMLY29udG9zby5jb20wggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQC73w3VRBOlgJ5Od1PjDh+2ytngNZp+ZP4fkuX8K1Ti5LA6Ih7eWx1fgAN/iTb6l
                            5K6LvAIJvsTNVePMNxfSdaEIJ70Inm45wVU4A/kf+UxQWAYVMsBrLtDFWxnVhzf6n7RGYke6HLBj3j5ASb9g+olSs6eON25ibF0t+u6JC+sIR0LmVGar9Q0eZys1rdfzJBIKq+laOM7z2pJijb5ANqve9
                            i7rH5mnhQk4V8WsRstOhYR9jgLqSSxokDoeaBClIOidSBYqVc1yNv4ASe1UWUCR7ZK6OQXiecNWSWPmgWEyawu6AR9eb1YotCr2ScheMOCxlm3103luitxrd8A7kMjAgMBAAGgSzBJBgkqhkiG9w0BCQ4
                            xPDA6MA4GA1UdDwEB/wQEAwIFoDAdBgNVHSUEFjAUBggrBgEFBQcDAQYIKwYBBQUHAwIwCQYDVR0TBAIwADANBgkqhkiG9w0BAQsFAAOCAQEAIHhsDJV37PKi8hor5eQf7+Tct1preIvSwqV0NF6Uo7O6
                            YnC9Py7Wp7CHfKzuqeptUk2Tsu7B5dHB+o9Ypeeqw8fWhTN0GFGRKO7WjZQlDqL+lRNcjlFSaP022oIP0kmvVhBcmZqRQlALXccAaxEclFA/3y/aNj2gwWeKpH/pwAkZ39zMEzpQCaRfnQk7e3l4MV8cf
                            eC2HPYdRWkXxAeDcNPxBuVmKy49AzYvly+APNVDU3v66gxl3fIKrGRsKi2Cp/nO5rBxG2h8t+0Za4l/HJ7ZWR9wKbd/xg7JhdZZFVBxMHYzw8KQ0ys13x8HY+PXU92Y7yD3uC2Rcj+zbAf+Kg==
ErrorCode                 :
ErrorMessage              :
Name                      :
VaultName                 :
```

<span data-ttu-id="301e6-111">Esse comando obtém o status da operação do certificado para TestCert01 no cofre da chave ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="301e6-111">This command gets the status of the certificate operation for TestCert01 on the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="301e6-112">OS</span><span class="sxs-lookup"><span data-stu-id="301e6-112">PARAMETERS</span></span>

### <span data-ttu-id="301e6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="301e6-113">-DefaultProfile</span></span>
<span data-ttu-id="301e6-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="301e6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="301e6-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="301e6-115">-InputObject</span></span>
<span data-ttu-id="301e6-116">Objeto de certificado.</span><span class="sxs-lookup"><span data-stu-id="301e6-116">Certificate Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="301e6-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="301e6-117">-Name</span></span>
<span data-ttu-id="301e6-118">Especifica o nome de um certificado.</span><span class="sxs-lookup"><span data-stu-id="301e6-118">Specifies the name of a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="301e6-119">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="301e6-119">-VaultName</span></span>
<span data-ttu-id="301e6-120">Especifica o nome de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="301e6-120">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="301e6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="301e6-121">CommonParameters</span></span>
<span data-ttu-id="301e6-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="301e6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="301e6-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="301e6-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="301e6-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="301e6-124">INPUTS</span></span>

### <span data-ttu-id="301e6-125">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="301e6-125">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>
<span data-ttu-id="301e6-126">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="301e6-126">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="301e6-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="301e6-127">OUTPUTS</span></span>

### <span data-ttu-id="301e6-128">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="301e6-128">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="301e6-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="301e6-129">NOTES</span></span>

## <span data-ttu-id="301e6-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="301e6-130">RELATED LINKS</span></span>

[<span data-ttu-id="301e6-131">Remove-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="301e6-131">Remove-AzureKeyVaultCertificateOperation</span></span>](./Remove-AzureKeyVaultCertificateOperation.md)

[<span data-ttu-id="301e6-132">Parar-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="301e6-132">Stop-AzureKeyVaultCertificateOperation</span></span>](./Stop-AzureKeyVaultCertificateOperation.md)

