---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 910239BE-9E48-4DC5-85EA-CC6D466FE62F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSSLBinding.md
ms.openlocfilehash: 99d7d4a0feeb0f548ef65d06234eecb1ad2baf6c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440917"
---
# <span data-ttu-id="a833e-101">New-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="a833e-101">New-AzureRmWebAppSSLBinding</span></span>

## <span data-ttu-id="a833e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a833e-102">SYNOPSIS</span></span>
<span data-ttu-id="a833e-103">Cria uma associação de certificado SSL para um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="a833e-103">Creates an SSL certificate binding for an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a833e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a833e-104">SYNTAX</span></span>

### <span data-ttu-id="a833e-105">Eles</span><span class="sxs-lookup"><span data-stu-id="a833e-105">S1</span></span>
```
New-AzureRmWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-Name] <String> [[-SslState] <SslState>] [-CertificateFilePath] <String> [-CertificatePassword] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a833e-106">S2</span><span class="sxs-lookup"><span data-stu-id="a833e-106">S2</span></span>
```
New-AzureRmWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a833e-107">S3</span><span class="sxs-lookup"><span data-stu-id="a833e-107">S3</span></span>
```
New-AzureRmWebAppSSLBinding [-WebApp] <Site> [-Name] <String> [[-SslState] <SslState>]
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a833e-108">S4</span><span class="sxs-lookup"><span data-stu-id="a833e-108">S4</span></span>
```
New-AzureRmWebAppSSLBinding [-WebApp] <Site> [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a833e-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a833e-109">DESCRIPTION</span></span>
<span data-ttu-id="a833e-110">O cmdlet **New-AzureRmWebAppSSLBinding** cria uma associação de certificado SSL (Secure Socket Layer) para um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="a833e-110">The **New-AzureRmWebAppSSLBinding** cmdlet creates a Secure Socket Layer (SSL) certificate binding for an Azure Web App.</span></span>
<span data-ttu-id="a833e-111">O cmdlet cria uma associação SSL de duas maneiras:</span><span class="sxs-lookup"><span data-stu-id="a833e-111">The cmdlet creates an SSL binding in two ways:</span></span> 

- <span data-ttu-id="a833e-112">Você pode associar um aplicativo Web a um certificado existente.</span><span class="sxs-lookup"><span data-stu-id="a833e-112">You can bind a Web App to an existing certificate.</span></span>
- <span data-ttu-id="a833e-113">Você pode carregar um novo certificado e, em seguida, associar o aplicativo Web a esse novo certificado.</span><span class="sxs-lookup"><span data-stu-id="a833e-113">You can upload a new certificate and then bind the Web App to this new certificate.</span></span>

<span data-ttu-id="a833e-114">Independentemente da abordagem que você usa, o certificado e o aplicativo Web devem estar associados ao mesmo grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="a833e-114">Regardless of which approach you use, the certificate and the Web App must be associated with the same Azure resource group.</span></span>
<span data-ttu-id="a833e-115">Se você tiver um aplicativo Web no grupo de recursos A e quiser associar esse aplicativo Web a um certificado no grupo de recursos B, a única maneira de fazer isso é carregar uma cópia do certificado para o grupo de recursos A.</span><span class="sxs-lookup"><span data-stu-id="a833e-115">If you have a Web App in Resource Group A and you want to bind that Web App to a certificate in Resource Group B, the only way to do that is to upload a copy of the certificate to Resource Group A.</span></span>

<span data-ttu-id="a833e-116">Se você carregar um novo certificado, lembre-se dos seguintes requisitos para um certificado SSL do Azure:</span><span class="sxs-lookup"><span data-stu-id="a833e-116">If you upload a new certificate, keep in mind the following requirements for an Azure SSL certificate:</span></span> 

- <span data-ttu-id="a833e-117">O certificado deve conter uma chave privada.</span><span class="sxs-lookup"><span data-stu-id="a833e-117">The certificate must contain a private key.</span></span> 
- <span data-ttu-id="a833e-118">O certificado deve usar o formato PFX (troca de informações pessoais).</span><span class="sxs-lookup"><span data-stu-id="a833e-118">The certificate must use the Personal Information Exchange (PFX) format.</span></span> 
- <span data-ttu-id="a833e-119">O nome do requerente do certificado deve corresponder ao domínio usado para acessar o aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="a833e-119">The certificate's subject name must match the domain used to access the Web App.</span></span> 
- <span data-ttu-id="a833e-120">O certificado deve usar uma criptografia mínima de 2048 bits.</span><span class="sxs-lookup"><span data-stu-id="a833e-120">The certificate must use a minimum of 2048-bit encryption.</span></span>

## <span data-ttu-id="a833e-121">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a833e-121">EXAMPLES</span></span>

### <span data-ttu-id="a833e-122">Exemplo 1: associar um certificado a um aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="a833e-122">Example 1: Bind a certificate to a Web App</span></span>
```
PS C:\>New-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" -Name "www.contoso.com" -CertificatePassword "p@ssw0rd"
```

<span data-ttu-id="a833e-123">Esse comando associa um certificado existente do Azure (um certificado com o E3A38EBA60CAA1C162785A2E1C44A15AD450199C3 de impressão digital) ao aplicativo Web chamado ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="a833e-123">This command binds an existing Azure certificate (a certificate with the Thumbprint E3A38EBA60CAA1C162785A2E1C44A15AD450199C3) to the web app named ContosoWebApp.</span></span>

### <span data-ttu-id="a833e-124">Exemplo 2: carregar um certificado e associá-lo a um aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="a833e-124">Example 2: Upload a certificate and bind it to a Web App</span></span>
```
PS C:\>New-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" -Name "www.contoso.com" -CertificatePassword "p@ssw0rd" -CertificateFilePath "C:\Certificates\ContosoWebSite.pfx"
```

<span data-ttu-id="a833e-125">O exemplo 2 também associa o certificado E3A38EBA60CAA1C162785A2E1C44A15AD450199C3 ao aplicativo Web chamado ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="a833e-125">Example 2 also binds the certificate E3A38EBA60CAA1C162785A2E1C44A15AD450199C3 to the Web App named ContosoWebApp.</span></span>
<span data-ttu-id="a833e-126">Nesse caso, no entanto, o certificado ainda não foi carregado no Azure.</span><span class="sxs-lookup"><span data-stu-id="a833e-126">In this case, however, the certificate has not yet been uploaded to Azure.</span></span>
<span data-ttu-id="a833e-127">Por isso, o parâmetro *CertificateFilePath* é usado para especificar a cópia local do certificado. Arquivo PFX.</span><span class="sxs-lookup"><span data-stu-id="a833e-127">Because of that, the *CertificateFilePath* parameter is used to specify the local copy of the certificate .PFX file.</span></span>
<span data-ttu-id="a833e-128">Esse certificado será carregado no Azure e, em seguida, as novas associações SSL serão criadas.</span><span class="sxs-lookup"><span data-stu-id="a833e-128">This certificate will be uploaded to Azure and then the new SSL bindings will be created.</span></span>

## <span data-ttu-id="a833e-129">OS</span><span class="sxs-lookup"><span data-stu-id="a833e-129">PARAMETERS</span></span>

### <span data-ttu-id="a833e-130">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="a833e-130">-CertificateFilePath</span></span>
<span data-ttu-id="a833e-131">Especifica o caminho do arquivo para o certificado a ser carregado.</span><span class="sxs-lookup"><span data-stu-id="a833e-131">Specifies the file path for the certificate to be uploaded.</span></span>

<span data-ttu-id="a833e-132">O parâmetro *CertificateFilePath* será necessário apenas se o certificado ainda não tiver sido carregado no Azure.</span><span class="sxs-lookup"><span data-stu-id="a833e-132">The *CertificateFilePath* parameter is only required if the certificate has not yet been uploaded to Azure.</span></span>

```yaml
Type: System.String
Parameter Sets: S1, S3
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a833e-133">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="a833e-133">-CertificatePassword</span></span>
<span data-ttu-id="a833e-134">Especifica a senha de descriptografia do certificado.</span><span class="sxs-lookup"><span data-stu-id="a833e-134">Specifies the decryption password for the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: S1, S3
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a833e-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="a833e-135">-Name</span></span>
<span data-ttu-id="a833e-136">Especifica o nome do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="a833e-136">Specifies the name of the Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a833e-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a833e-137">-ResourceGroupName</span></span>
<span data-ttu-id="a833e-138">Especifica o nome do grupo de recursos ao qual o certificado está atribuído.</span><span class="sxs-lookup"><span data-stu-id="a833e-138">Specifies the name of the resource group that the certificate is assigned to.</span></span>

<span data-ttu-id="a833e-139">Não é possível usar o parâmetro *ResourceGroupName* e o parâmetro *webapp* no mesmo comando.</span><span class="sxs-lookup"><span data-stu-id="a833e-139">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: System.String
Parameter Sets: S1, S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a833e-140">-Slot</span><span class="sxs-lookup"><span data-stu-id="a833e-140">-Slot</span></span>
<span data-ttu-id="a833e-141">Especifica o nome do slot de implantação do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="a833e-141">Specifies the name of the Web App deployment slot.</span></span>
<span data-ttu-id="a833e-142">Você pode usar o cmdlet Get-AzureRMWebAppSlot para obter um slot.</span><span class="sxs-lookup"><span data-stu-id="a833e-142">You can use the Get-AzureRMWebAppSlot cmdlet to get a slot.</span></span>

<span data-ttu-id="a833e-143">Os slots de implantação fornecem uma maneira de testar e validar aplicativos Web sem esses aplicativos serem acessíveis pela Internet.</span><span class="sxs-lookup"><span data-stu-id="a833e-143">Deployment slots provide a way for you to stage and validate web apps without those apps being accessible over the Internet.</span></span>
<span data-ttu-id="a833e-144">Normalmente, você implantará as alterações em um site temporário, validará essas alterações e, em seguida, implantará no site de produção (acessível à Internet).</span><span class="sxs-lookup"><span data-stu-id="a833e-144">Typically you will deploy your changes to a staging site, validate those changes, and then deploy to the production (Internet-accessible) site.</span></span>

```yaml
Type: System.String
Parameter Sets: S1, S2
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a833e-145">-SslState</span><span class="sxs-lookup"><span data-stu-id="a833e-145">-SslState</span></span>
<span data-ttu-id="a833e-146">Especifica se o certificado está habilitado.</span><span class="sxs-lookup"><span data-stu-id="a833e-146">Specifies whether the certificate is enabled.</span></span>
<span data-ttu-id="a833e-147">Defina o parâmetro *SSLState* como 1 para habilitar o certificado ou defina *SSLState* como 0 para desabilitar o certificado.</span><span class="sxs-lookup"><span data-stu-id="a833e-147">Set the *SSLState* parameter to 1 to enable the certificate, or set *SSLState* to 0 to disable the certificate.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.WebSites.Models.SslState]
Parameter Sets: (All)
Aliases: 
Accepted values: Disabled, SniEnabled, IpBasedEnabled

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a833e-148">-Impressão digital</span><span class="sxs-lookup"><span data-stu-id="a833e-148">-Thumbprint</span></span>
<span data-ttu-id="a833e-149">Especifica o identificador exclusivo do certificado.</span><span class="sxs-lookup"><span data-stu-id="a833e-149">Specifies the unique identifier for the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: S2, S4
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a833e-150">-WebApp</span><span class="sxs-lookup"><span data-stu-id="a833e-150">-WebApp</span></span>
<span data-ttu-id="a833e-151">Especifica um aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="a833e-151">Specifies a Web App.</span></span>
<span data-ttu-id="a833e-152">Para obter um aplicativo Web, use o cmdlet Get-AzureRmWebApp.</span><span class="sxs-lookup"><span data-stu-id="a833e-152">To get a Web App, use the Get-AzureRmWebApp cmdlet.</span></span>

<span data-ttu-id="a833e-153">Não é possível usar o parâmetro *webapp* no mesmo comando que o parâmetro *ResourceGroupName* e/ou o *webappname*.</span><span class="sxs-lookup"><span data-stu-id="a833e-153">You cannot use the *WebApp* parameter in the same command as the *ResourceGroupName* parameter and/or the *WebAppName*.</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: S3, S4
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a833e-154">-WebAppname</span><span class="sxs-lookup"><span data-stu-id="a833e-154">-WebAppName</span></span>
<span data-ttu-id="a833e-155">Especifica o nome do aplicativo Web para o qual a nova associação SSL está sendo criada.</span><span class="sxs-lookup"><span data-stu-id="a833e-155">Specifies the name of the Web App for which the new SSL binding is being created.</span></span>

<span data-ttu-id="a833e-156">Não é possível usar o parâmetro *webappname* e o parâmetro *webapp* no mesmo comando.</span><span class="sxs-lookup"><span data-stu-id="a833e-156">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: System.String
Parameter Sets: S1, S2
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a833e-157">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a833e-157">-DefaultProfile</span></span>
<span data-ttu-id="a833e-158">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a833e-158">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a833e-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a833e-159">CommonParameters</span></span>
<span data-ttu-id="a833e-160">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a833e-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a833e-161">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a833e-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a833e-162">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a833e-162">INPUTS</span></span>

### <span data-ttu-id="a833e-163">Instalação</span><span class="sxs-lookup"><span data-stu-id="a833e-163">Site</span></span>
<span data-ttu-id="a833e-164">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="a833e-164">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="a833e-165">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a833e-165">OUTPUTS</span></span>

## <span data-ttu-id="a833e-166">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a833e-166">NOTES</span></span>

## <span data-ttu-id="a833e-167">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a833e-167">RELATED LINKS</span></span>

[<span data-ttu-id="a833e-168">Get-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="a833e-168">Get-AzureRmWebAppSSLBinding</span></span>](./Get-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="a833e-169">Remove-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="a833e-169">Remove-AzureRmWebAppSSLBinding</span></span>](./Remove-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="a833e-170">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="a833e-170">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="a833e-171">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="a833e-171">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

