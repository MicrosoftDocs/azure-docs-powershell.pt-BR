---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 910239BE-9E48-4DC5-85EA-CC6D466FE62F
online version: https://docs.microsoft.com/powershell/module/az.websites/new-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSSLBinding.md
ms.openlocfilehash: 3429868b1d603606f64c75ec23505cf63f9ade03
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891545"
---
# <span data-ttu-id="8afab-101">New-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="8afab-101">New-AzWebAppSSLBinding</span></span>

## <span data-ttu-id="8afab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8afab-102">SYNOPSIS</span></span>
<span data-ttu-id="8afab-103">Cria uma associação de certificado SSL para um Aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="8afab-103">Creates an SSL certificate binding for an Azure Web App.</span></span>

## <span data-ttu-id="8afab-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8afab-104">SYNTAX</span></span>

### <span data-ttu-id="8afab-105">S1</span><span class="sxs-lookup"><span data-stu-id="8afab-105">S1</span></span>
```
New-AzWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>] [-Name] <String>
 [[-SslState] <SslState>] [-CertificateFilePath] <String> [-CertificatePassword] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8afab-106">S2</span><span class="sxs-lookup"><span data-stu-id="8afab-106">S2</span></span>
```
New-AzWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>] [-Name] <String>
 [[-SslState] <SslState>] [-Thumbprint] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8afab-107">S3</span><span class="sxs-lookup"><span data-stu-id="8afab-107">S3</span></span>
```
New-AzWebAppSSLBinding [-WebApp] <PSSite> [-Name] <String> [[-SslState] <SslState>]
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8afab-108">S4</span><span class="sxs-lookup"><span data-stu-id="8afab-108">S4</span></span>
```
New-AzWebAppSSLBinding [-WebApp] <PSSite> [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8afab-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8afab-109">DESCRIPTION</span></span>
<span data-ttu-id="8afab-110">O cmdlet **New-AzWebAppSSLBinding** cria uma associação de certificado SSL (Secure Socket Layer) para um Aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="8afab-110">The **New-AzWebAppSSLBinding** cmdlet creates a Secure Socket Layer (SSL) certificate binding for an Azure Web App.</span></span>
<span data-ttu-id="8afab-111">O cmdlet cria uma associação SSL de duas maneiras:</span><span class="sxs-lookup"><span data-stu-id="8afab-111">The cmdlet creates an SSL binding in two ways:</span></span> 
- <span data-ttu-id="8afab-112">Você pode vincular um Aplicativo Web a um certificado existente.</span><span class="sxs-lookup"><span data-stu-id="8afab-112">You can bind a Web App to an existing certificate.</span></span>
- <span data-ttu-id="8afab-113">Você pode carregar um novo certificado e, em seguida, vincular o Aplicativo Web a esse novo certificado.</span><span class="sxs-lookup"><span data-stu-id="8afab-113">You can upload a new certificate and then bind the Web App to this new certificate.</span></span>
<span data-ttu-id="8afab-114">Independentemente da abordagem usada, o certificado e o Aplicativo Web devem estar associados ao mesmo grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="8afab-114">Regardless of which approach you use, the certificate and the Web App must be associated with the same Azure resource group.</span></span>
<span data-ttu-id="8afab-115">Se você tiver um Aplicativo Web no Grupo de Recursos A e quiser vincular esse Aplicativo Web a um certificado no Grupo de Recursos B, a única maneira de fazer isso é carregar uma cópia do certificado para o Grupo de Recursos A. Se você carregar um novo certificado, lembre-se dos seguintes requisitos para um certificado SSL do Azure:</span><span class="sxs-lookup"><span data-stu-id="8afab-115">If you have a Web App in Resource Group A and you want to bind that Web App to a certificate in Resource Group B, the only way to do that is to upload a copy of the certificate to Resource Group A. If you upload a new certificate, keep in mind the following requirements for an Azure SSL certificate:</span></span> 
- <span data-ttu-id="8afab-116">O certificado deve conter uma chave privada.</span><span class="sxs-lookup"><span data-stu-id="8afab-116">The certificate must contain a private key.</span></span> 
- <span data-ttu-id="8afab-117">O certificado deve usar o formato PFX (Personal Information Exchange).</span><span class="sxs-lookup"><span data-stu-id="8afab-117">The certificate must use the Personal Information Exchange (PFX) format.</span></span> 
- <span data-ttu-id="8afab-118">O nome de assunto do certificado deve corresponder ao domínio usado para acessar o Aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="8afab-118">The certificate's subject name must match the domain used to access the Web App.</span></span> 
- <span data-ttu-id="8afab-119">O certificado deve usar um mínimo de criptografia de 2048 bits.</span><span class="sxs-lookup"><span data-stu-id="8afab-119">The certificate must use a minimum of 2048-bit encryption.</span></span>

## <span data-ttu-id="8afab-120">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8afab-120">EXAMPLES</span></span>

### <span data-ttu-id="8afab-121">Exemplo 1: vincular um certificado a um aplicativo Web</span><span class="sxs-lookup"><span data-stu-id="8afab-121">Example 1: Bind a certificate to a Web App</span></span>
```powershell
PS C:\>New-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" -Name "www.contoso.com"
```

<span data-ttu-id="8afab-122">Este comando vincula um certificado existente do Azure (um certificado com a impressão digital E3A38EBA60CAA1C162785A2E1C44A15AD450199C3) ao aplicativo Web chamado ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="8afab-122">This command binds an existing Azure certificate (a certificate with the Thumbprint E3A38EBA60CAA1C162785A2E1C44A15AD450199C3) to the web app named ContosoWebApp.</span></span>

### <span data-ttu-id="8afab-123">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="8afab-123">Example 2</span></span>

<span data-ttu-id="8afab-124">Cria uma associação de certificado SSL para um Aplicativo Web do Azure.</span><span class="sxs-lookup"><span data-stu-id="8afab-124">Creates an SSL certificate binding for an Azure Web App.</span></span> <span data-ttu-id="8afab-125">(gerado automaticamente)</span><span class="sxs-lookup"><span data-stu-id="8afab-125">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzWebAppSSLBinding -Name 'www.contoso.com' -ResourceGroupName 'ContosoResourceGroup' -SslState Disabled -Thumbprint 'E3A38EBA60CAA1C162785A2E1C44A15AD450199C3' -WebAppName 'ContosoWebApp'
```

## <span data-ttu-id="8afab-126">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8afab-126">PARAMETERS</span></span>

### <span data-ttu-id="8afab-127">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="8afab-127">-CertificateFilePath</span></span>
<span data-ttu-id="8afab-128">Especifica o caminho do arquivo para o certificado a ser carregado.</span><span class="sxs-lookup"><span data-stu-id="8afab-128">Specifies the file path for the certificate to be uploaded.</span></span>
<span data-ttu-id="8afab-129">O *parâmetro CertificateFilePath* só será necessário se o certificado ainda não tiver sido carregado no Azure.</span><span class="sxs-lookup"><span data-stu-id="8afab-129">The *CertificateFilePath* parameter is only required if the certificate has not yet been uploaded to Azure.</span></span>

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

### <span data-ttu-id="8afab-130">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="8afab-130">-CertificatePassword</span></span>
<span data-ttu-id="8afab-131">Especifica a senha de descriptografia do certificado.</span><span class="sxs-lookup"><span data-stu-id="8afab-131">Specifies the decryption password for the certificate.</span></span>

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

### <span data-ttu-id="8afab-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8afab-132">-DefaultProfile</span></span>
<span data-ttu-id="8afab-133">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="8afab-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8afab-134">-Name</span><span class="sxs-lookup"><span data-stu-id="8afab-134">-Name</span></span>
<span data-ttu-id="8afab-135">Especifica o nome do Aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="8afab-135">Specifies the name of the Web App.</span></span>

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

### <span data-ttu-id="8afab-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8afab-136">-ResourceGroupName</span></span>
<span data-ttu-id="8afab-137">Especifica o nome do grupo de recursos ao que o certificado é atribuído.</span><span class="sxs-lookup"><span data-stu-id="8afab-137">Specifies the name of the resource group that the certificate is assigned to.</span></span>
<span data-ttu-id="8afab-138">Não é possível usar o *parâmetro ResourceGroupName* e o *parâmetro WebApp* no mesmo comando.</span><span class="sxs-lookup"><span data-stu-id="8afab-138">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="8afab-139">-Slot</span><span class="sxs-lookup"><span data-stu-id="8afab-139">-Slot</span></span>
<span data-ttu-id="8afab-140">Especifica o nome do slot de implantação do Web App.</span><span class="sxs-lookup"><span data-stu-id="8afab-140">Specifies the name of the Web App deployment slot.</span></span>
<span data-ttu-id="8afab-141">Você pode usar o cmdlet Get-AzWebAppSlot para obter um slot.</span><span class="sxs-lookup"><span data-stu-id="8afab-141">You can use the Get-AzWebAppSlot cmdlet to get a slot.</span></span>
<span data-ttu-id="8afab-142">Os slots de implantação fornecem uma maneira de você fazer estágios e validar aplicativos Web sem que esses aplicativos sejam acessíveis pela Internet.</span><span class="sxs-lookup"><span data-stu-id="8afab-142">Deployment slots provide a way for you to stage and validate web apps without those apps being accessible over the Internet.</span></span>
<span data-ttu-id="8afab-143">Normalmente, você implantará suas alterações em um site de preparação, validará essas alterações e implantará no site de produção (acessível à Internet).</span><span class="sxs-lookup"><span data-stu-id="8afab-143">Typically you will deploy your changes to a staging site, validate those changes, and then deploy to the production (Internet-accessible) site.</span></span>

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

### <span data-ttu-id="8afab-144">-SslState</span><span class="sxs-lookup"><span data-stu-id="8afab-144">-SslState</span></span>
<span data-ttu-id="8afab-145">Especifica se o certificado está habilitado.</span><span class="sxs-lookup"><span data-stu-id="8afab-145">Specifies whether the certificate is enabled.</span></span>
<span data-ttu-id="8afab-146">Defina o *parâmetro SSLState* como 1 para habilitar o certificado ou defina *SSLState* como 0 para desabilitar o certificado.</span><span class="sxs-lookup"><span data-stu-id="8afab-146">Set the *SSLState* parameter to 1 to enable the certificate, or set *SSLState* to 0 to disable the certificate.</span></span>

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

### <span data-ttu-id="8afab-147">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="8afab-147">-Thumbprint</span></span>
<span data-ttu-id="8afab-148">Especifica o identificador exclusivo do certificado.</span><span class="sxs-lookup"><span data-stu-id="8afab-148">Specifies the unique identifier for the certificate.</span></span>

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

### <span data-ttu-id="8afab-149">-WebApp</span><span class="sxs-lookup"><span data-stu-id="8afab-149">-WebApp</span></span>
<span data-ttu-id="8afab-150">Especifica um Aplicativo Web.</span><span class="sxs-lookup"><span data-stu-id="8afab-150">Specifies a Web App.</span></span>
<span data-ttu-id="8afab-151">Para obter um Aplicativo Web, use o Get-AzWebApp cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8afab-151">To get a Web App, use the Get-AzWebApp cmdlet.</span></span>
<span data-ttu-id="8afab-152">Não é possível usar o *parâmetro WebApp* no mesmo comando que o *parâmetro ResourceGroupName* e/ou *o WebAppName*.</span><span class="sxs-lookup"><span data-stu-id="8afab-152">You cannot use the *WebApp* parameter in the same command as the *ResourceGroupName* parameter and/or the *WebAppName*.</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S3, S4
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8afab-153">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="8afab-153">-WebAppName</span></span>
<span data-ttu-id="8afab-154">Especifica o nome do Aplicativo Web para o qual a nova associação SSL está sendo criada.</span><span class="sxs-lookup"><span data-stu-id="8afab-154">Specifies the name of the Web App for which the new SSL binding is being created.</span></span>
<span data-ttu-id="8afab-155">Não é possível usar o *parâmetro WebAppName* e o *parâmetro WebApp* no mesmo comando.</span><span class="sxs-lookup"><span data-stu-id="8afab-155">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

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

### <span data-ttu-id="8afab-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8afab-156">CommonParameters</span></span>
<span data-ttu-id="8afab-157">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8afab-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8afab-158">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8afab-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8afab-159">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8afab-159">INPUTS</span></span>

### <span data-ttu-id="8afab-160">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="8afab-160">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="8afab-161">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8afab-161">OUTPUTS</span></span>

### <span data-ttu-id="8afab-162">Microsoft.Azure.Management.WebSites.Models.HostNameSslState</span><span class="sxs-lookup"><span data-stu-id="8afab-162">Microsoft.Azure.Management.WebSites.Models.HostNameSslState</span></span>

## <span data-ttu-id="8afab-163">NOTES</span><span class="sxs-lookup"><span data-stu-id="8afab-163">NOTES</span></span>

## <span data-ttu-id="8afab-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8afab-164">RELATED LINKS</span></span>

[<span data-ttu-id="8afab-165">Get-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="8afab-165">Get-AzWebAppSSLBinding</span></span>](./Get-AzWebAppSSLBinding.md)

[<span data-ttu-id="8afab-166">Remove-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="8afab-166">Remove-AzWebAppSSLBinding</span></span>](./Remove-AzWebAppSSLBinding.md)

[<span data-ttu-id="8afab-167">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="8afab-167">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="8afab-168">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="8afab-168">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


