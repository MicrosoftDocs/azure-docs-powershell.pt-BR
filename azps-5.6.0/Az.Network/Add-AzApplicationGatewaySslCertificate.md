---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7EC4C642-1D23-4699-AE00-6E180C38271E
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewaysslcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewaySslCertificate.md
ms.openlocfilehash: 4dde5ab085dede4520b26a4fbeb3255cc62c0fe8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889197"
---
# <span data-ttu-id="30266-101">Add-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="30266-101">Add-AzApplicationGatewaySslCertificate</span></span>

## <span data-ttu-id="30266-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="30266-102">SYNOPSIS</span></span>
<span data-ttu-id="30266-103">Adiciona um certificado SSL a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="30266-103">Adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="30266-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="30266-104">SYNTAX</span></span>

```
Add-AzApplicationGatewaySslCertificate -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-CertificateFile <String>] [-Password <SecureString>] [-KeyVaultSecretId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30266-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="30266-105">DESCRIPTION</span></span>
<span data-ttu-id="30266-106">O cmdlet **Add-AzApplicationGatewaySslCertificate** adiciona um certificado SSL a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="30266-106">The **Add-AzApplicationGatewaySslCertificate** cmdlet adds an SSL certificate to an application gateway.</span></span>

## <span data-ttu-id="30266-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="30266-107">EXAMPLES</span></span>

### <span data-ttu-id="30266-108">Exemplo 1: Adicionar um certificado SSL usando pfx a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="30266-108">Example 1: Add an SSL certificate using pfx to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $password = ConvertTo-SecureString $passwordPlainString -AsPlainText -Force
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -CertificateFile "D:\cert01.pfx" -Password $password
```

<span data-ttu-id="30266-109">Esse comando obtém um gateway de aplicativo chamado ApplicationGateway01 e adiciona um certificado SSL chamado Cert01 a ele.</span><span class="sxs-lookup"><span data-stu-id="30266-109">This command gets an application gateway named ApplicationGateway01 and then adds an SSL certificate named Cert01 to it.</span></span>

### <span data-ttu-id="30266-110">Exemplo 2: Adicione um certificado SSL usando KeyVault Secret (secretId sem versão) a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="30266-110">Example 2: Add an SSL certificate using KeyVault Secret (version-less secretId) to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $secret = Get-AzKeyVaultCertificate -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.SecretId.Replace($secret.Version, "") # https://<keyvaultname>.vault.azure.net/secrets/
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="30266-111">Obter o segredo e fazer referência a ele no `Add-AzApplicationGatewaySslCertificate` para adicioná-lo ao Gateway de Aplicativos com o nome `Cert01` .</span><span class="sxs-lookup"><span data-stu-id="30266-111">Get the secret and reference it in the `Add-AzApplicationGatewaySslCertificate` to add it to the Application Gateway with name `Cert01`.</span></span>
<span data-ttu-id="30266-112">Observação: como secretId sem versão é fornecido aqui, o Gateway de Aplicativo sincroniza o certificado em intervalos regulares com o KeyVault.</span><span class="sxs-lookup"><span data-stu-id="30266-112">Note: As version-less secretId is provided here, Application Gateway will sync the certificate in regular intervals with the KeyVault.</span></span>

### <span data-ttu-id="30266-113">Exemplo 3: Adicione um certificado SSL usando KeyVault Secret (secretId com versão) a um gateway de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="30266-113">Example 3: Add an SSL certificate using KeyVault Secret (versioned secretId) to an application gateway.</span></span>
```
PS C:\> $AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $secret = Get-AzKeyVaultCertificate -VaultName "keyvault01" -Name "sslCert01"
PS C:\> $secretId = $secret.Id # https://<keyvaultname>.vault.azure.net/secrets/<hash>
PS C:\> $AppGW = Add-AzApplicationGatewaySslCertificate -ApplicationGateway $AppGW -Name "Cert01" -KeyVaultSecretId $secretId
```

<span data-ttu-id="30266-114">Obter o segredo e fazer referência a ele no `Add-AzApplicationGatewaySslCertificate` para adicioná-lo ao Gateway de Aplicativos com o nome `Cert01` .</span><span class="sxs-lookup"><span data-stu-id="30266-114">Get the secret and reference it in the `Add-AzApplicationGatewaySslCertificate` to add it to the Application Gateway with name `Cert01`.</span></span>
<span data-ttu-id="30266-115">Observação: se for necessário que o Gateway de Aplicativo sincronize o certificado com o KeyVault, forneça o secretId sem versão.</span><span class="sxs-lookup"><span data-stu-id="30266-115">Note: If it is required that Application Gateway syncs the certificate with the KeyVault, please provide the version-less secretId.</span></span>

## <span data-ttu-id="30266-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="30266-116">PARAMETERS</span></span>

### <span data-ttu-id="30266-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="30266-117">-ApplicationGateway</span></span>
<span data-ttu-id="30266-118">Especifica o nome do gateway de aplicativo ao qual este cmdlet adiciona um certificado SSL.</span><span class="sxs-lookup"><span data-stu-id="30266-118">Specifies the name of application gateway to which this cmdlet adds an SSL certificate.</span></span>

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

### <span data-ttu-id="30266-119">-CertificateFile</span><span class="sxs-lookup"><span data-stu-id="30266-119">-CertificateFile</span></span>
<span data-ttu-id="30266-120">Especifica o arquivo .pfx de um certificado SSL que este cmdlet adiciona.</span><span class="sxs-lookup"><span data-stu-id="30266-120">Specifies the .pfx file of an SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="30266-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30266-121">-DefaultProfile</span></span>
<span data-ttu-id="30266-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="30266-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30266-123">-KeyVaultSecretId</span><span class="sxs-lookup"><span data-stu-id="30266-123">-KeyVaultSecretId</span></span>
<span data-ttu-id="30266-124">SecretId (uri) do Segredo KeyVault.</span><span class="sxs-lookup"><span data-stu-id="30266-124">SecretId (uri) of the KeyVault Secret.</span></span> <span data-ttu-id="30266-125">Use essa opção quando uma versão específica do segredo precisar ser usada.</span><span class="sxs-lookup"><span data-stu-id="30266-125">Use this option when a specific version of secret needs to be used.</span></span>

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

### <span data-ttu-id="30266-126">-Name</span><span class="sxs-lookup"><span data-stu-id="30266-126">-Name</span></span>
<span data-ttu-id="30266-127">Especifica o nome do certificado SSL que este cmdlet adiciona.</span><span class="sxs-lookup"><span data-stu-id="30266-127">Specifies the name of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="30266-128">-Password</span><span class="sxs-lookup"><span data-stu-id="30266-128">-Password</span></span>
<span data-ttu-id="30266-129">Especifica a senha do certificado SSL que este cmdlet adiciona.</span><span class="sxs-lookup"><span data-stu-id="30266-129">Specifies the password of the SSL certificate that this cmdlet adds.</span></span>

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

### <span data-ttu-id="30266-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30266-130">CommonParameters</span></span>
<span data-ttu-id="30266-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30266-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30266-132">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30266-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30266-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="30266-133">INPUTS</span></span>

### <span data-ttu-id="30266-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="30266-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="30266-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="30266-135">OUTPUTS</span></span>

### <span data-ttu-id="30266-136">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="30266-136">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="30266-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="30266-137">NOTES</span></span>

## <span data-ttu-id="30266-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="30266-138">RELATED LINKS</span></span>

[<span data-ttu-id="30266-139">Get-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="30266-139">Get-AzApplicationGatewaySslCertificate</span></span>](./Get-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="30266-140">New-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="30266-140">New-AzApplicationGatewaySslCertificate</span></span>](./New-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="30266-141">Remove-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="30266-141">Remove-AzApplicationGatewaySslCertificate</span></span>](./Remove-AzApplicationGatewaySslCertificate.md)

[<span data-ttu-id="30266-142">Set-AzApplicationGatewaySslCertificate</span><span class="sxs-lookup"><span data-stu-id="30266-142">Set-AzApplicationGatewaySslCertificate</span></span>](./Set-AzApplicationGatewaySslCertificate.md)


