---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EC4C642-1D23-4699-AE00-6E180C38271E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 47c2f4dcb3e18c969c57d037d9e4f0104b1980f3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94117049"
---
# <span data-ttu-id="a3f34-101">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a3f34-101">Add-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="a3f34-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a3f34-102">SYNOPSIS</span></span>
<span data-ttu-id="a3f34-103">Adiciona um certificado SSL a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a3f34-103">Adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="a3f34-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a3f34-104">SYNTAX</span></span>

```
Add-AzApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-CertificateFile <String>] [-Password <SecureString>] [-KeyVaultSecretId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3f34-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a3f34-105">DESCRIPTION</span></span>
<span data-ttu-id="a3f34-106">O cmdlet **Add-AzApplicationGatewaySslCertificate** adiciona um certificado SSL a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a3f34-106">The **Add-AzApplicationGatewaySslCertificate** cmdlet adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="a3f34-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a3f34-107">EXAMPLES</span></span>

### <span data-ttu-id="a3f34-108">Exemplo 1: adicionar um certificado SSL usando pfx a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a3f34-108">Example 1: Add an SSL certificate using pfx to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString "P@ssw0rd" -AsPlainText -Force
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="a3f34-109">Esse comando obtém um gateway do aplicativo chamado ApplicationGateway01 e, em seguida, adiciona um certificado SSL chamado Cert01 a ele.</span><span class="sxs-lookup"><span data-stu-id="a3f34-109">This command gets an application gateway named ApplicationGateway01 and then adds an SSL certificate named Cert01 to it.</span></span>

### <span data-ttu-id="a3f34-110">Exemplo 2: adicionar um certificado SSL usando o segredo do keyvault (versão menos secreta) para um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a3f34-110">Example 2: Add an SSL certificate using KeyVault Secret (version-less secretId) to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $secret = Get-AzKeyVaultCertificate -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.SecretId.Replace($secret.Version, "") # https://<keyvaultname>.vault.azure.net/secrets/
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="a3f34-111">Obtenha o segredo e faça referência a ele no `Add-AzApplicationGatewaySslCertificate` para adicioná-lo ao gateway do aplicativo com o nome `Cert01` .</span><span class="sxs-lookup"><span data-stu-id="a3f34-111">Get the secret and reference it in the `Add-AzApplicationGatewaySslCertificate` to add it to the Application Gateway with name `Cert01`.</span></span>
<span data-ttu-id="a3f34-112">Observação: como a versão-menos secreta é fornecida aqui, o Application Gateway sincronizará o certificado em intervalos regulares com o cofre de chave.</span><span class="sxs-lookup"><span data-stu-id="a3f34-112">Note: As version-less secretId is provided here, Application Gateway will sync the certificate in regular intervals with the KeyVault.</span></span>

### <span data-ttu-id="a3f34-113">Exemplo 3: adicionar um certificado SSL usando o segredo do keyvault (com versão secretaid) em um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a3f34-113">Example 3: Add an SSL certificate using KeyVault Secret (versioned secretId) to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $secret = Get-AzKeyVaultCertificate -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id # https://<keyvaultname>.vault.azure.net/secrets/<hash>
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="a3f34-114">Obtenha o segredo e faça referência a ele no `Add-AzApplicationGatewaySslCertificate` para adicioná-lo ao gateway do aplicativo com o nome `Cert01` .</span><span class="sxs-lookup"><span data-stu-id="a3f34-114">Get the secret and reference it in the `Add-AzApplicationGatewaySslCertificate` to add it to the Application Gateway with name `Cert01`.</span></span>
<span data-ttu-id="a3f34-115">Observação: se for necessário que o Application Gateway Sincronize o certificado com o keyvault, forneça o nome secreto sem versão.</span><span class="sxs-lookup"><span data-stu-id="a3f34-115">Note: If it is required that Application Gateway syncs the certificate with the KeyVault, please provide the version-less secretId.</span></span>

## <span data-ttu-id="a3f34-116">OS</span><span class="sxs-lookup"><span data-stu-id="a3f34-116">PARAMETERS</span></span>

### <span data-ttu-id="a3f34-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a3f34-117">-ApplicationGateway</span></span>
<span data-ttu-id="a3f34-118">Especifica o nome do gateway do aplicativo para o qual esse cmdlet adiciona um certificado SSL.</span><span class="sxs-lookup"><span data-stu-id="a3f34-118">Specifies the name of application gateway to which this cmdlet adds an SSL certificate.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a3f34-119">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="a3f34-119">-CertificateFile</span></span>
<span data-ttu-id="a3f34-120">Especifica o arquivo. pfx de um certificado SSL que este cmdlet adiciona.</span><span class="sxs-lookup"><span data-stu-id="a3f34-120">Specifies the .pfx file of an SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="a3f34-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3f34-121">-DefaultProfile</span></span>
<span data-ttu-id="a3f34-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a3f34-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3f34-123">-KeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="a3f34-123">-KeyVaultSecretId</span></span>
<span data-ttu-id="a3f34-124">Secretid (URI) do segredo do keyvault.</span><span class="sxs-lookup"><span data-stu-id="a3f34-124">SecretId (uri) of the KeyVault Secret.</span></span> <span data-ttu-id="a3f34-125">Use esta opção quando for preciso usar uma versão específica do segredo.</span><span class="sxs-lookup"><span data-stu-id="a3f34-125">Use this option when a specific version of secret needs to be used.</span></span>

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

### <span data-ttu-id="a3f34-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="a3f34-126">-Name</span></span>
<span data-ttu-id="a3f34-127">Especifica o nome do certificado SSL que este cmdlet adiciona.</span><span class="sxs-lookup"><span data-stu-id="a3f34-127">Specifies the name of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="a3f34-128">-Senha</span><span class="sxs-lookup"><span data-stu-id="a3f34-128">-Password</span></span>
<span data-ttu-id="a3f34-129">Especifica a senha do certificado SSL que este cmdlet adiciona.</span><span class="sxs-lookup"><span data-stu-id="a3f34-129">Specifies the password of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="a3f34-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3f34-130">CommonParameters</span></span>
<span data-ttu-id="a3f34-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3f34-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3f34-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3f34-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3f34-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a3f34-133">INPUTS</span></span>

### <span data-ttu-id="a3f34-134">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a3f34-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a3f34-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a3f34-135">OUTPUTS</span></span>

### <span data-ttu-id="a3f34-136">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a3f34-136">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a3f34-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a3f34-137">NOTES</span></span>

## <span data-ttu-id="a3f34-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a3f34-138">RELATED LINKS</span></span>

[<span data-ttu-id="a3f34-139">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a3f34-139">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="a3f34-140">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a3f34-140">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="a3f34-141">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a3f34-141">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="a3f34-142">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="a3f34-142">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


