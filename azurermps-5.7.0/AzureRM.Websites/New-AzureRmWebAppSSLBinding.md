---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 910239BE-9E48-4DC5-85EA-CC6D466FE62F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSSLBinding.md
ms.openlocfilehash: d3971c2838b3fed04e1aa38d96e2cd27b2e8276e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432843"
---
# <span data-ttu-id="f2f34-101">New-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="f2f34-101">New-AzureRmWebAppSSLBinding</span></span>

## <span data-ttu-id="f2f34-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f2f34-102">SYNOPSIS</span></span>
<span data-ttu-id="f2f34-103">Cria uma associação de certificado SSL para um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="f2f34-103">Creates an SSL certificate binding for an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2f34-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f2f34-104">SYNTAX</span></span>

### <span data-ttu-id="f2f34-105">Eles</span><span class="sxs-lookup"><span data-stu-id="f2f34-105">S1</span></span>
```
New-AzureRmWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-Name] <String> [[-SslState] <SslState>] [-CertificateFilePath] <String> [-CertificatePassword] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2f34-106">S2</span><span class="sxs-lookup"><span data-stu-id="f2f34-106">S2</span></span>
```
New-AzureRmWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f2f34-107">S3</span><span class="sxs-lookup"><span data-stu-id="f2f34-107">S3</span></span>
```
New-AzureRmWebAppSSLBinding [-WebApp] <Site> [-Name] <String> [[-SslState] <SslState>]
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f2f34-108">S4</span><span class="sxs-lookup"><span data-stu-id="f2f34-108">S4</span></span>
```
New-AzureRmWebAppSSLBinding [-WebApp] <Site> [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2f34-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f2f34-109">DESCRIPTION</span></span>
<span data-ttu-id="f2f34-110">O cmdlet **New-AzureRmWebAppSSLBinding** cria uma associação de certificado SSL (Secure Socket Layer) para um aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="f2f34-110">The **New-AzureRmWebAppSSLBinding** cmdlet creates a Secure Socket Layer (SSL) certificate binding for an Azure Web App.</span></span>
<span data-ttu-id="f2f34-111">O cmdlet cria uma associação SSL de duas maneiras:</span><span class="sxs-lookup"><span data-stu-id="f2f34-111">The cmdlet creates an SSL binding in two ways:</span></span> 

- <span data-ttu-id="f2f34-112">Você pode associar um aplicativo Web a um certificado existente.</span><span class="sxs-lookup"><span data-stu-id="f2f34-112">You can bind a Web App to an existing certificate.</span></span>
- <span data-ttu-id="f2f34-113">Você pode carregar um novo certificado e, em seguida, associar o aplicativo Web a esse novo certificado.</span><span class="sxs-lookup"><span data-stu-id="f2f34-113">You can upload a new certificate and then bind the Web App to this new certificate.</span></span>

<span data-ttu-id="f2f34-114">Independentemente da abordagem que você usa, o certificado e o aplicativo Web devem estar associados ao mesmo grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="f2f34-114">Regardless of which approach you use, the certificate and the Web App must be associated with the same Azure resource group.</span></span>
<span data-ttu-id="f2f34-115">Se você tiver um aplicativo Web no grupo de recursos A e quiser associar esse aplicativo Web a um certificado no grupo de recursos B, a única maneira de fazer isso é carregar uma cópia do certificado para o grupo de recursos A.</span><span class="sxs-lookup"><span data-stu-id="f2f34-115">If you have a Web App in Resource Group A and you want to bind that Web App to a certificate in Resource Group B, the only way to do that is to upload a copy of the certificate to Resource Group A.</span></span>

<span data-ttu-id="f2f34-116">Se você carregar um novo certificado, lembre-se dos seguintes requisitos para um certificado SSL do Azure:</span><span class="sxs-lookup"><span data-stu-id="f2f34-116">If you upload a new certificate, keep in mind the following requirements for an Azure SSL certificate:</span></span> 

- <span data-ttu-id="f2f34-117">O certificado deve conter uma chave privada.</span><span class="sxs-lookup"><span data-stu-id="f2f34-117">The certificate must contain a private key.</span></span> 
- <span data-ttu-id="f2f34-118">O certificado deve usar o formato PFX (troca de informações pessoais).</span><span class="sxs-lookup"><span data-stu-id="f2f34-118">The certificate must use the Personal Information Exchange (PFX) format.</span></span> 
- <span data-ttu-id="f2f34-119">O nome do requerente do certificado deve corresponder ao domínio usado para acessar o aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="f2f34-119">The certificate's subject name must match the domain used to access the Web App.</span></span> 
- <span data-ttu-id="f2f34-120">O certificado deve usar uma criptografia mínima de 2048 bits.</span><span class="sxs-lookup"><span data-stu-id="f2f34-120">The certificate must use a minimum of 2048-bit encryption.</span></span>

## <span data-ttu-id="f2f34-121">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f2f34-121">EXAMPLES</span></span>

### <span data-ttu-id="f2f34-122">Exemplo 1: associar um certificado a um aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="f2f34-122">Example 1: Bind a certificate to a Web App</span></span>
```
PS C:\>New-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" -Name "www.contoso.com"
```

<span data-ttu-id="f2f34-123">Esse comando associa um certificado existente do Azure (um certificado com o E3A38EBA60CAA1C162785A2E1C44A15AD450199C3 de impressão digital) ao aplicativo Web chamado ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="f2f34-123">This command binds an existing Azure certificate (a certificate with the Thumbprint E3A38EBA60CAA1C162785A2E1C44A15AD450199C3) to the web app named ContosoWebApp.</span></span>

## <span data-ttu-id="f2f34-124">OS</span><span class="sxs-lookup"><span data-stu-id="f2f34-124">PARAMETERS</span></span>

### <span data-ttu-id="f2f34-125">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="f2f34-125">-CertificateFilePath</span></span>
<span data-ttu-id="f2f34-126">Especifica o caminho do arquivo para o certificado a ser carregado.</span><span class="sxs-lookup"><span data-stu-id="f2f34-126">Specifies the file path for the certificate to be uploaded.</span></span>

<span data-ttu-id="f2f34-127">O parâmetro *CertificateFilePath* será necessário apenas se o certificado ainda não tiver sido carregado no Azure.</span><span class="sxs-lookup"><span data-stu-id="f2f34-127">The *CertificateFilePath* parameter is only required if the certificate has not yet been uploaded to Azure.</span></span>

```yaml
Type: String
Parameter Sets: S1, S3
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2f34-128">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="f2f34-128">-CertificatePassword</span></span>
<span data-ttu-id="f2f34-129">Especifica a senha de descriptografia do certificado.</span><span class="sxs-lookup"><span data-stu-id="f2f34-129">Specifies the decryption password for the certificate.</span></span>

```yaml
Type: String
Parameter Sets: S1, S3
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2f34-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2f34-130">-DefaultProfile</span></span>
<span data-ttu-id="f2f34-131">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f2f34-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2f34-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="f2f34-132">-Name</span></span>
<span data-ttu-id="f2f34-133">Especifica o nome do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="f2f34-133">Specifies the name of the Web App.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2f34-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2f34-134">-ResourceGroupName</span></span>
<span data-ttu-id="f2f34-135">Especifica o nome do grupo de recursos ao qual o certificado está atribuído.</span><span class="sxs-lookup"><span data-stu-id="f2f34-135">Specifies the name of the resource group that the certificate is assigned to.</span></span>

<span data-ttu-id="f2f34-136">Não é possível usar o parâmetro *ResourceGroupName* e o parâmetro *webapp* no mesmo comando.</span><span class="sxs-lookup"><span data-stu-id="f2f34-136">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: String
Parameter Sets: S1, S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2f34-137">-Slot</span><span class="sxs-lookup"><span data-stu-id="f2f34-137">-Slot</span></span>
<span data-ttu-id="f2f34-138">Especifica o nome do slot de implantação do aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="f2f34-138">Specifies the name of the Web App deployment slot.</span></span>
<span data-ttu-id="f2f34-139">Você pode usar o cmdlet Get-AzureRMWebAppSlot para obter um slot.</span><span class="sxs-lookup"><span data-stu-id="f2f34-139">You can use the Get-AzureRMWebAppSlot cmdlet to get a slot.</span></span>

<span data-ttu-id="f2f34-140">Os slots de implantação fornecem uma maneira de testar e validar aplicativos Web sem esses aplicativos serem acessíveis pela Internet.</span><span class="sxs-lookup"><span data-stu-id="f2f34-140">Deployment slots provide a way for you to stage and validate web apps without those apps being accessible over the Internet.</span></span>
<span data-ttu-id="f2f34-141">Normalmente, você implantará as alterações em um site temporário, validará essas alterações e, em seguida, implantará no site de produção (acessível à Internet).</span><span class="sxs-lookup"><span data-stu-id="f2f34-141">Typically you will deploy your changes to a staging site, validate those changes, and then deploy to the production (Internet-accessible) site.</span></span>

```yaml
Type: String
Parameter Sets: S1, S2
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2f34-142">-SslState</span><span class="sxs-lookup"><span data-stu-id="f2f34-142">-SslState</span></span>
<span data-ttu-id="f2f34-143">Especifica se o certificado está habilitado.</span><span class="sxs-lookup"><span data-stu-id="f2f34-143">Specifies whether the certificate is enabled.</span></span>
<span data-ttu-id="f2f34-144">Defina o parâmetro *SSLState* como 1 para habilitar o certificado ou defina *SSLState* como 0 para desabilitar o certificado.</span><span class="sxs-lookup"><span data-stu-id="f2f34-144">Set the *SSLState* parameter to 1 to enable the certificate, or set *SSLState* to 0 to disable the certificate.</span></span>

```yaml
Type: SslState
Parameter Sets: (All)
Aliases: 
Accepted values: Disabled, SniEnabled, IpBasedEnabled

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2f34-145">-Impressão digital</span><span class="sxs-lookup"><span data-stu-id="f2f34-145">-Thumbprint</span></span>
<span data-ttu-id="f2f34-146">Especifica o identificador exclusivo do certificado.</span><span class="sxs-lookup"><span data-stu-id="f2f34-146">Specifies the unique identifier for the certificate.</span></span>

```yaml
Type: String
Parameter Sets: S2, S4
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2f34-147">-WebApp</span><span class="sxs-lookup"><span data-stu-id="f2f34-147">-WebApp</span></span>
<span data-ttu-id="f2f34-148">Especifica um aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="f2f34-148">Specifies a Web App.</span></span>
<span data-ttu-id="f2f34-149">Para obter um aplicativo Web, use o cmdlet Get-AzureRmWebApp.</span><span class="sxs-lookup"><span data-stu-id="f2f34-149">To get a Web App, use the Get-AzureRmWebApp cmdlet.</span></span>

<span data-ttu-id="f2f34-150">Não é possível usar o parâmetro *webapp* no mesmo comando que o parâmetro *ResourceGroupName* e/ou o *webappname*.</span><span class="sxs-lookup"><span data-stu-id="f2f34-150">You cannot use the *WebApp* parameter in the same command as the *ResourceGroupName* parameter and/or the *WebAppName*.</span></span>

```yaml
Type: Site
Parameter Sets: S3, S4
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2f34-151">-WebAppname</span><span class="sxs-lookup"><span data-stu-id="f2f34-151">-WebAppName</span></span>
<span data-ttu-id="f2f34-152">Especifica o nome do aplicativo Web para o qual a nova associação SSL está sendo criada.</span><span class="sxs-lookup"><span data-stu-id="f2f34-152">Specifies the name of the Web App for which the new SSL binding is being created.</span></span>

<span data-ttu-id="f2f34-153">Não é possível usar o parâmetro *webappname* e o parâmetro *webapp* no mesmo comando.</span><span class="sxs-lookup"><span data-stu-id="f2f34-153">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: String
Parameter Sets: S1, S2
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2f34-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2f34-154">CommonParameters</span></span>
<span data-ttu-id="f2f34-155">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2f34-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2f34-156">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2f34-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2f34-157">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f2f34-157">INPUTS</span></span>

### <span data-ttu-id="f2f34-158">Instalação</span><span class="sxs-lookup"><span data-stu-id="f2f34-158">Site</span></span>
<span data-ttu-id="f2f34-159">O parâmetro ' WebApp ' aceita o valor do tipo ' site ' da pipeline</span><span class="sxs-lookup"><span data-stu-id="f2f34-159">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="f2f34-160">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f2f34-160">OUTPUTS</span></span>

## <span data-ttu-id="f2f34-161">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f2f34-161">NOTES</span></span>

## <span data-ttu-id="f2f34-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f2f34-162">RELATED LINKS</span></span>

[<span data-ttu-id="f2f34-163">Get-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="f2f34-163">Get-AzureRmWebAppSSLBinding</span></span>](./Get-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="f2f34-164">Remove-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="f2f34-164">Remove-AzureRmWebAppSSLBinding</span></span>](./Remove-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="f2f34-165">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="f2f34-165">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="f2f34-166">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="f2f34-166">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)


