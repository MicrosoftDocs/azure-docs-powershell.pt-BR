---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6FFE1B64-C80B-423D-A043-55C90A224752
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 0749f964831962c946c5682db6c746da644cb0ce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93600377"
---
# <span data-ttu-id="d0716-101">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="d0716-101">New-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="d0716-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d0716-102">SYNOPSIS</span></span>
<span data-ttu-id="d0716-103">Cria um certificado SSL para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="d0716-103">Creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="d0716-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d0716-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySslCertificate -Name <String> [-CertificateFile <String>] [-Password <SecureString>]
 [-KeyVaultSecretId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0716-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d0716-105">DESCRIPTION</span></span>
<span data-ttu-id="d0716-106">O cmdlet **New-AzApplicationGatewaySslCertificate** cria um certificado SSL para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="d0716-106">The **New-AzApplicationGatewaySslCertificate** cmdlet creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="d0716-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d0716-107">EXAMPLES</span></span>

### <span data-ttu-id="d0716-108">Exemplo 1: criar um certificado SSL para um gateway do aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="d0716-108">Example 1: Create an SSL certificate for an Azure application gateway.</span></span>
```
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="d0716-109">Esse comando cria um certificado SSL chamado Cert01 para o gateway do aplicativo padrão e armazena o resultado na variável chamada $Cert.</span><span class="sxs-lookup"><span data-stu-id="d0716-109">This command creates a SSL certificate named Cert01 for the default application gateway and stores the result in the variable named $Cert.</span></span>

### <span data-ttu-id="d0716-110">Exemplo 2: criar um certificado SSL usando o segredo do keyvault (versão menos secreta) e adicionar a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d0716-110">Example 2: Create an SSL certificate using KeyVault Secret (version-less secretId) and add to an application gateway.</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id.Replace($secret.Version, "") # https://<keyvaultname>.vault.azure.net/secrets/
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="d0716-111">Obtenha o segredo e crie um certificado SSL usando o `New-AzApplicationGatewaySslCertificate` .</span><span class="sxs-lookup"><span data-stu-id="d0716-111">Get the secret and create an SSL Certificate using `New-AzApplicationGatewaySslCertificate`.</span></span>
<span data-ttu-id="d0716-112">Observação: como a versão-menos secreta é fornecida aqui, o Application Gateway sincronizará o certificado em intervalos regulares com o cofre de chave.</span><span class="sxs-lookup"><span data-stu-id="d0716-112">Note: As version-less secretId is provided here, Application Gateway will sync the certificate in regular intervals with the KeyVault.</span></span>

### <span data-ttu-id="d0716-113">Exemplo 3: criar um certificado SSL usando o segredo do keyvault e adicionar a um gateway do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d0716-113">Example 3: Create an SSL certificate using KeyVault Secret and add to an Application Gateway.</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id # https://<keyvaultname>.vault.azure.net/secrets/<hash>
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="d0716-114">Obtenha o segredo e crie um certificado SSL usando o `New-AzApplicationGatewaySslCertificate` .</span><span class="sxs-lookup"><span data-stu-id="d0716-114">Get the secret and create an SSL Certificate using `New-AzApplicationGatewaySslCertificate`.</span></span>
<span data-ttu-id="d0716-115">Observação: se for necessário que o Application Gateway Sincronize o certificado com o keyvault, forneça o nome secreto sem versão.</span><span class="sxs-lookup"><span data-stu-id="d0716-115">Note: If it is required that Application Gateway syncs the certificate with the KeyVault, please provide the version-less secretId.</span></span>

## <span data-ttu-id="d0716-116">OS</span><span class="sxs-lookup"><span data-stu-id="d0716-116">PARAMETERS</span></span>

### <span data-ttu-id="d0716-117">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="d0716-117">-CertificateFile</span></span>
<span data-ttu-id="d0716-118">Especifica o caminho do arquivo. pfx do certificado SSL criado por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0716-118">Specifies the path of the .pfx file of the SSL certificate that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0716-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0716-119">-DefaultProfile</span></span>
<span data-ttu-id="d0716-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d0716-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0716-121">-KeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="d0716-121">-KeyVaultSecretId</span></span>
<span data-ttu-id="d0716-122">Secretid (URI) do segredo do keyvault.</span><span class="sxs-lookup"><span data-stu-id="d0716-122">SecretId (uri) of the KeyVault Secret.</span></span> <span data-ttu-id="d0716-123">Use esta opção quando for preciso usar uma versão específica do segredo.</span><span class="sxs-lookup"><span data-stu-id="d0716-123">Use this option when a specific version of secret needs to be used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0716-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="d0716-124">-Name</span></span>
<span data-ttu-id="d0716-125">Especifica o nome do certificado SSL criado por esse cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0716-125">Specifies the name of the SSL certificate that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0716-126">-Senha</span><span class="sxs-lookup"><span data-stu-id="d0716-126">-Password</span></span>
<span data-ttu-id="d0716-127">Especifica a senha do SSL que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="d0716-127">Specifies the password of the SSL that this cmdlet creates.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0716-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0716-128">CommonParameters</span></span>
<span data-ttu-id="d0716-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0716-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0716-130">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0716-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0716-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d0716-131">INPUTS</span></span>

### <span data-ttu-id="d0716-132">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="d0716-132">None</span></span>

## <span data-ttu-id="d0716-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d0716-133">OUTPUTS</span></span>

### <span data-ttu-id="d0716-134">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="d0716-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="d0716-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d0716-135">NOTES</span></span>

## <span data-ttu-id="d0716-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d0716-136">RELATED LINKS</span></span>

[<span data-ttu-id="d0716-137">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="d0716-137">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="d0716-138">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="d0716-138">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="d0716-139">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="d0716-139">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="d0716-140">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="d0716-140">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


