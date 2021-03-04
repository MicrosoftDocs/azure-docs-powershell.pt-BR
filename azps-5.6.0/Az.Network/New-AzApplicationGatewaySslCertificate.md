---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6FFE1B64-C80B-423D-A043-55C90A224752
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 84465161d726108749e09d4a928e22aea8050c92
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101901458"
---
# <span data-ttu-id="0430a-101">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0430a-101">New-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="0430a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0430a-102">SYNOPSIS</span></span>
<span data-ttu-id="0430a-103">Cria um certificado SSL para um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="0430a-103">Creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="0430a-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="0430a-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySslCertificate -Name <String> [-CertificateFile <String>] [-Password <SecureString>]
 [-KeyVaultSecretId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0430a-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="0430a-105">DESCRIPTION</span></span>
<span data-ttu-id="0430a-106">O cmdlet **New-AzApplicationGatewaySslCertificate** cria um certificado SSL para um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="0430a-106">The **New-AzApplicationGatewaySslCertificate** cmdlet creates an SSL certificate for an Azure application gateway.</span></span>

## <span data-ttu-id="0430a-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0430a-107">EXAMPLES</span></span>

### <span data-ttu-id="0430a-108">Exemplo 1: Criar um certificado SSL para um gateway de aplicativo do Azure.</span><span class="sxs-lookup"><span data-stu-id="0430a-108">Example 1: Create an SSL certificate for an Azure application gateway.</span></span>
```
PS C:\> $password = ConvertTo-SecureString $passwordPlainString -AsPlainText -Force
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="0430a-109">Este comando cria um certificado SSL chamado Cert01 para o gateway de aplicativo padrão e armazena o resultado na variável chamada $Cert.</span><span class="sxs-lookup"><span data-stu-id="0430a-109">This command creates a SSL certificate named Cert01 for the default application gateway and stores the result in the variable named $Cert.</span></span>

### <span data-ttu-id="0430a-110">Exemplo 2: crie um certificado SSL usando KeyVault Secret (secretId sem versão) e adicione a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0430a-110">Example 2: Create an SSL certificate using KeyVault Secret (version-less secretId) and add to an application gateway.</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id.Replace($secret.Version, "") # https://<keyvaultname>.vault.azure.net/secrets/
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="0430a-111">Obter o segredo e criar um Certificado SSL usando `New-AzApplicationGatewaySslCertificate` .</span><span class="sxs-lookup"><span data-stu-id="0430a-111">Get the secret and create an SSL Certificate using `New-AzApplicationGatewaySslCertificate`.</span></span>
<span data-ttu-id="0430a-112">Observação: como secretId sem versão é fornecido aqui, o Gateway de Aplicativo sincroniza o certificado em intervalos regulares com o KeyVault.</span><span class="sxs-lookup"><span data-stu-id="0430a-112">Note: As version-less secretId is provided here, Application Gateway will sync the certificate in regular intervals with the KeyVault.</span></span>

### <span data-ttu-id="0430a-113">Exemplo 3: Crie um certificado SSL usando Segredo keyVault e adicione a um Gateway de Aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0430a-113">Example 3: Create an SSL certificate using KeyVault Secret and add to an Application Gateway.</span></span>
```
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id # https://<keyvaultname>.vault.azure.net/secrets/<hash>
PS C:\> $cert = New-AzApplicationGatewaySslCertificate -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="0430a-114">Obter o segredo e criar um Certificado SSL usando `New-AzApplicationGatewaySslCertificate` .</span><span class="sxs-lookup"><span data-stu-id="0430a-114">Get the secret and create an SSL Certificate using `New-AzApplicationGatewaySslCertificate`.</span></span>
<span data-ttu-id="0430a-115">Observação: se for necessário que o Gateway de Aplicativo sincronize o certificado com o KeyVault, forneça o secretId sem versão.</span><span class="sxs-lookup"><span data-stu-id="0430a-115">Note: If it is required that Application Gateway syncs the certificate with the KeyVault, please provide the version-less secretId.</span></span>

## <span data-ttu-id="0430a-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="0430a-116">PARAMETERS</span></span>

### <span data-ttu-id="0430a-117">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="0430a-117">-CertificateFile</span></span>
<span data-ttu-id="0430a-118">Especifica o caminho do arquivo .pfx do certificado SSL que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="0430a-118">Specifies the path of the .pfx file of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="0430a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0430a-119">-DefaultProfile</span></span>
<span data-ttu-id="0430a-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="0430a-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0430a-121">-KeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="0430a-121">-KeyVaultSecretId</span></span>
<span data-ttu-id="0430a-122">SecretId (uri) do Segredo KeyVault.</span><span class="sxs-lookup"><span data-stu-id="0430a-122">SecretId (uri) of the KeyVault Secret.</span></span> <span data-ttu-id="0430a-123">Use essa opção quando uma versão específica do segredo precisar ser usada.</span><span class="sxs-lookup"><span data-stu-id="0430a-123">Use this option when a specific version of secret needs to be used.</span></span>

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

### <span data-ttu-id="0430a-124">-Name</span><span class="sxs-lookup"><span data-stu-id="0430a-124">-Name</span></span>
<span data-ttu-id="0430a-125">Especifica o nome do certificado SSL que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="0430a-125">Specifies the name of the SSL certificate that this cmdlet creates.</span></span>

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

### <span data-ttu-id="0430a-126">-Password</span><span class="sxs-lookup"><span data-stu-id="0430a-126">-Password</span></span>
<span data-ttu-id="0430a-127">Especifica a senha do SSL que este cmdlet cria.</span><span class="sxs-lookup"><span data-stu-id="0430a-127">Specifies the password of the SSL that this cmdlet creates.</span></span>

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

### <span data-ttu-id="0430a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0430a-128">CommonParameters</span></span>
<span data-ttu-id="0430a-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0430a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0430a-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0430a-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0430a-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0430a-131">INPUTS</span></span>

### <span data-ttu-id="0430a-132">Nenhum</span><span class="sxs-lookup"><span data-stu-id="0430a-132">None</span></span>

## <span data-ttu-id="0430a-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="0430a-133">OUTPUTS</span></span>

### <span data-ttu-id="0430a-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0430a-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="0430a-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="0430a-135">NOTES</span></span>

## <span data-ttu-id="0430a-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0430a-136">RELATED LINKS</span></span>

[<span data-ttu-id="0430a-137">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0430a-137">Add-AzApplicationGatewaySslCertificate</span></span>](./Add-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="0430a-138">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0430a-138">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="0430a-139">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0430a-139">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="0430a-140">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="0430a-140">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


