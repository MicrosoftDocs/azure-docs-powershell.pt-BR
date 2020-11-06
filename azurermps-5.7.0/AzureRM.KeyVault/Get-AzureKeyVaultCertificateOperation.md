---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 0743C43D-2A1F-4950-B0F3-1FED4014EEC5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultcertificateoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultCertificateOperation.md
ms.openlocfilehash: 1f61207afbdf4c6553f6db4050775577d72c5eba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93428907"
---
# <span data-ttu-id="5a618-101">Get-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="5a618-101">Get-AzureKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="5a618-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5a618-102">SYNOPSIS</span></span>
<span data-ttu-id="5a618-103">Obtém o status de uma operação de certificado.</span><span class="sxs-lookup"><span data-stu-id="5a618-103">Gets the status of a certificate operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a618-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5a618-104">SYNTAX</span></span>

### <span data-ttu-id="5a618-105">ByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="5a618-105">ByName (Default)</span></span>
```
Get-AzureKeyVaultCertificateOperation [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a618-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5a618-106">ByInputObject</span></span>
```
Get-AzureKeyVaultCertificateOperation [-InputObject] <PSKeyVaultCertificateIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a618-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5a618-107">DESCRIPTION</span></span>
<span data-ttu-id="5a618-108">O cmdlet **Get-AzureKeyVaultCertificateOperation** Obtém o status de uma operação de certificado.</span><span class="sxs-lookup"><span data-stu-id="5a618-108">The **Get-AzureKeyVaultCertificateOperation** cmdlet gets the status of a certificate operation.</span></span>

## <span data-ttu-id="5a618-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5a618-109">EXAMPLES</span></span>

### <span data-ttu-id="5a618-110">Exemplo 1: obter o status de uma operação de certificado</span><span class="sxs-lookup"><span data-stu-id="5a618-110">Example 1: Get the status of a certificate operation</span></span>
```
PS C:\>Get-AzureKeyVaultCertificateOperation -VaultName "ContosoKV01" -Name "TestCert01"
Status                    : inProgress
CancellationRequested     : False
CertificateSigningRequest : MIICpjCCAY4CAQAwFjEUMBIGA1UEAxMLY29udG9zby5jb20wggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQC73w3VRBOlgJ5Od1PjDh+2ytngNZp+ZP4fkuX8K1Ti5LA6Ih7eWx1fgAN/iTb6l
                            5K6LvAIJvsTNVePMNxfSdaEIJ70Inm45wVU4A/kf+UxQWAYVMsBrLtDFWxnVhzf6n7RGYke6HLBj3j5ASb9g+olSs6eON25ibF0t+u6JC+sIR0LmVGar9Q0eZys1rdfzJBIKq+laOM7z2pJijb5ANqve9
                            i7rH5mnhQk4V8WsRstOhYR9jgLqSSxokDoeaBClIOidSBYqVc1yNv4ASe1UWUCR7ZK6OQXiecNWSWPmgWEyawu6AR9eb1YotCr2ScheMOCxlm3103luitxrd8A7kMjAgMBAAGgSzBJBgkqhkiG9w0BCQ4
                            xPDA6MA4GA1UdDwEB/wQEAwIFoDAdBgNVHSUEFjAUBggrBgEFBQcDAQYIKwYBBQUHAwIwCQYDVR0TBAIwADANBgkqhkiG9w0BAQsFAAOCAQEAIHhsDJV37PKi8hor5eQf7+Tct1preIvSwqV0NF6Uo7O6
                            YnC9Py7Wp7CHfKzuqeptUk2Tsu7B5dHB+o9Ypeeqw8fWhTN0GFGRKO7WjZQlDqL+lRNcjlFSaP022oIP0kmvVhBcmZqRQlALXccAaxEclFA/3y/aNj2gwWeKpH/pwAkZ39zMEzpQCaRfnQk7e3l4MV8cf
                            eC2HPYdRWkXxAeDcNPxBuVmKy49AzYvly+APNVDU3v66gxl3fIKrGRsKi2Cp/nO5rBxG2h8t+0Za4l/HJ7ZWR9wKbd/xg7JhdZZFVBxMHYzw8KQ0ys13x8HY+PXU92Y7yD3uC2Rcj+zbAf+Kg==
ErrorCode                 : 
ErrorMessage              :
```

<span data-ttu-id="5a618-111">Esse comando obtém o status da operação do certificado para TestCert01 no cofre da chave ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="5a618-111">This command gets the status of the certificate operation for TestCert01 on the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="5a618-112">OS</span><span class="sxs-lookup"><span data-stu-id="5a618-112">PARAMETERS</span></span>

### <span data-ttu-id="5a618-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a618-113">-DefaultProfile</span></span>
<span data-ttu-id="5a618-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="5a618-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5a618-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a618-115">-InputObject</span></span>
<span data-ttu-id="5a618-116">Objeto de certificado.</span><span class="sxs-lookup"><span data-stu-id="5a618-116">Certificate Object.</span></span>

```yaml
Type: PSKeyVaultCertificateIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a618-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="5a618-117">-Name</span></span>
<span data-ttu-id="5a618-118">Especifica o nome de um certificado.</span><span class="sxs-lookup"><span data-stu-id="5a618-118">Specifies the name of a certificate.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: CertificateName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a618-119">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="5a618-119">-VaultName</span></span>
<span data-ttu-id="5a618-120">Especifica o nome de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="5a618-120">Specifies the name of a key vault.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a618-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a618-121">CommonParameters</span></span>
<span data-ttu-id="5a618-122">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a618-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a618-123">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a618-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a618-124">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5a618-124">INPUTS</span></span>

### <span data-ttu-id="5a618-125">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="5a618-125">None</span></span>
<span data-ttu-id="5a618-126">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="5a618-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5a618-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5a618-127">OUTPUTS</span></span>

### <span data-ttu-id="5a618-128">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="5a618-128">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOperation</span></span>

## <span data-ttu-id="5a618-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5a618-129">NOTES</span></span>

## <span data-ttu-id="5a618-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5a618-130">RELATED LINKS</span></span>

[<span data-ttu-id="5a618-131">Remove-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="5a618-131">Remove-AzureKeyVaultCertificateOperation</span></span>](./Remove-AzureKeyVaultCertificateOperation.md)

[<span data-ttu-id="5a618-132">Parar-AzureKeyVaultCertificateOperation</span><span class="sxs-lookup"><span data-stu-id="5a618-132">Stop-AzureKeyVaultCertificateOperation</span></span>](./Stop-AzureKeyVaultCertificateOperation.md)

