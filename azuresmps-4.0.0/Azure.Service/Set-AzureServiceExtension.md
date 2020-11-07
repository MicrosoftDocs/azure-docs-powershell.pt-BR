---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D37920D3-AF6C-4CFC-B9A3-8ED931AEC0DC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 318683c26d05c624549363ff1afe4a2b963c1fe6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945447"
---
# <span data-ttu-id="74042-101">Set-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="74042-101">Set-AzureServiceExtension</span></span>

## <span data-ttu-id="74042-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="74042-102">SYNOPSIS</span></span>
<span data-ttu-id="74042-103">Adiciona uma extensão de serviço de nuvem a uma implantação.</span><span class="sxs-lookup"><span data-stu-id="74042-103">Adds a cloud service extension to a deployment.</span></span>

## <span data-ttu-id="74042-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="74042-104">SYNTAX</span></span>

### <span data-ttu-id="74042-105">Setextension (padrão)</span><span class="sxs-lookup"><span data-stu-id="74042-105">SetExtension (Default)</span></span>
```
Set-AzureServiceExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-X509Certificate] <X509Certificate2>] [[-ThumbprintAlgorithm] <String>] [-ExtensionName] <String>
 [-ProviderNamespace] <String> [-PublicConfiguration] <String> [-PrivateConfiguration] <String>
 [-Version] <String> [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="74042-106">SetExtensionUsingThumbprint</span><span class="sxs-lookup"><span data-stu-id="74042-106">SetExtensionUsingThumbprint</span></span>
```
Set-AzureServiceExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-CertificateThumbprint] <String> [[-ThumbprintAlgorithm] <String>] [-ExtensionName] <String>
 [-ProviderNamespace] <String> [-PublicConfiguration] <String> [-PrivateConfiguration] <String>
 [-Version] <String> [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="74042-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="74042-107">DESCRIPTION</span></span>
<span data-ttu-id="74042-108">O cmdlet **set-AzureServiceExtension** adiciona uma extensão de serviço de nuvem a uma implantação.</span><span class="sxs-lookup"><span data-stu-id="74042-108">The **Set-AzureServiceExtension** cmdlet adds a cloud service extension to a deployment.</span></span>

## <span data-ttu-id="74042-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="74042-109">EXAMPLES</span></span>

### <span data-ttu-id="74042-110">Exemplo 1: adicionar um serviço de nuvem a uma implantação</span><span class="sxs-lookup"><span data-stu-id="74042-110">Example 1: Add a cloud service to a deployment</span></span>
```
PS C:\> Set-AzureServiceExtension -Service $Svc -Slot "Production" -ExtensionName "RDP" -Version "1.0" -ProviderNamespace "Microsoft.Windows.Azure.Extensions" -PublicConfiguration $P1 -PrivateConfiguration $P2;
```

<span data-ttu-id="74042-111">Esse comando adiciona um serviço na nuvem a uma implantação.</span><span class="sxs-lookup"><span data-stu-id="74042-111">This command adds a cloud service to a deployment.</span></span>

### <span data-ttu-id="74042-112">Exemplo 2: adicionar um serviço de nuvem a uma implantação para uma função especificada</span><span class="sxs-lookup"><span data-stu-id="74042-112">Example 2: Add a cloud service to a deployment for a specified role</span></span>
```
PS C:\> Set-AzureServiceExtension -Service $Svc -Slot "Production" -Role "WebRole1" -ExtensionName "RDP" -ProviderNamespace "Microsoft.Windows.Azure.Extensions" -PublicConfiguration $P1 -PrivateConfiguration $P2;
```

<span data-ttu-id="74042-113">Esse comando adiciona um serviço na nuvem a uma implantação para uma função especificada.</span><span class="sxs-lookup"><span data-stu-id="74042-113">This command adds a cloud service to a deployment for a specified role.</span></span>

## <span data-ttu-id="74042-114">OS</span><span class="sxs-lookup"><span data-stu-id="74042-114">PARAMETERS</span></span>

### <span data-ttu-id="74042-115">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="74042-115">-CertificateThumbprint</span></span>
<span data-ttu-id="74042-116">Especifica uma impressão digital de certificado a ser usada para criptografar a configuração particular.</span><span class="sxs-lookup"><span data-stu-id="74042-116">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="74042-117">Este certificado já existe no repositório de certificados.</span><span class="sxs-lookup"><span data-stu-id="74042-117">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="74042-118">Se você não especificar um certificado, esse cmdlet criará um certificado.</span><span class="sxs-lookup"><span data-stu-id="74042-118">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

```yaml
Type: String
Parameter Sets: SetExtensionUsingThumbprint
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74042-119">-ExtensionId</span><span class="sxs-lookup"><span data-stu-id="74042-119">-ExtensionId</span></span>
<span data-ttu-id="74042-120">Especifica a ID de extensão.</span><span class="sxs-lookup"><span data-stu-id="74042-120">Specifies the extension ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74042-121">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="74042-121">-ExtensionName</span></span>
<span data-ttu-id="74042-122">Especifica o nome da extensão.</span><span class="sxs-lookup"><span data-stu-id="74042-122">Specifies the extension name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74042-123">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="74042-123">-InformationAction</span></span>
<span data-ttu-id="74042-124">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="74042-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="74042-125">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="74042-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="74042-126">Contínuo</span><span class="sxs-lookup"><span data-stu-id="74042-126">Continue</span></span>
- <span data-ttu-id="74042-127">Ignorar</span><span class="sxs-lookup"><span data-stu-id="74042-127">Ignore</span></span>
- <span data-ttu-id="74042-128">Inquire</span><span class="sxs-lookup"><span data-stu-id="74042-128">Inquire</span></span>
- <span data-ttu-id="74042-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="74042-129">SilentlyContinue</span></span>
- <span data-ttu-id="74042-130">Finaliza</span><span class="sxs-lookup"><span data-stu-id="74042-130">Stop</span></span>
- <span data-ttu-id="74042-131">Suspensão</span><span class="sxs-lookup"><span data-stu-id="74042-131">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74042-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="74042-132">-InformationVariable</span></span>
<span data-ttu-id="74042-133">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="74042-133">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74042-134">-PrivateConfiguration</span><span class="sxs-lookup"><span data-stu-id="74042-134">-PrivateConfiguration</span></span>
<span data-ttu-id="74042-135">Especifica o texto de configuração particular.</span><span class="sxs-lookup"><span data-stu-id="74042-135">Specifies the private configuration text.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74042-136">-Perfil</span><span class="sxs-lookup"><span data-stu-id="74042-136">-Profile</span></span>
<span data-ttu-id="74042-137">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="74042-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="74042-138">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="74042-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74042-139">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="74042-139">-ProviderNamespace</span></span>
<span data-ttu-id="74042-140">Especifica o namespace do provedor de extensão.</span><span class="sxs-lookup"><span data-stu-id="74042-140">Specifies the extension provider namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74042-141">-PublicConfiguration</span><span class="sxs-lookup"><span data-stu-id="74042-141">-PublicConfiguration</span></span>
<span data-ttu-id="74042-142">Especifica o texto de configuração pública.</span><span class="sxs-lookup"><span data-stu-id="74042-142">Specifies the public configuration text.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74042-143">-Função</span><span class="sxs-lookup"><span data-stu-id="74042-143">-Role</span></span>
<span data-ttu-id="74042-144">Especifica uma matriz opcional de funções para as quais especificar a configuração da área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="74042-144">Specifies an optional array of roles for which to specify the remote desktop configuration.</span></span>
<span data-ttu-id="74042-145">Se esse parâmetro não for especificado, a configuração da área de trabalho remota será aplicada como a configuração padrão para todas as funções.</span><span class="sxs-lookup"><span data-stu-id="74042-145">If this parameter is not specified the remote desktop configuration is applied as the default configuration for all roles.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74042-146">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="74042-146">-ServiceName</span></span>
<span data-ttu-id="74042-147">Especifica o nome do serviço do Azure da implantação.</span><span class="sxs-lookup"><span data-stu-id="74042-147">Specifies the Azure service name of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74042-148">-Slot</span><span class="sxs-lookup"><span data-stu-id="74042-148">-Slot</span></span>
<span data-ttu-id="74042-149">Especifica o ambiente da implantação a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="74042-149">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="74042-150">Os valores válidos são: produção ou preparação.</span><span class="sxs-lookup"><span data-stu-id="74042-150">Valid values are: Production or Staging.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74042-151">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="74042-151">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="74042-152">Especifica o algoritmo de hash de impressão digital que é usado com a impressão digital para identificar o certificado.</span><span class="sxs-lookup"><span data-stu-id="74042-152">Specifies the thumbprint hashing algorithm which is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="74042-153">Esse parâmetro é opcional, e o padrão é SHA1.</span><span class="sxs-lookup"><span data-stu-id="74042-153">This parameter is optional and the default is sha1.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74042-154">-Versão</span><span class="sxs-lookup"><span data-stu-id="74042-154">-Version</span></span>
<span data-ttu-id="74042-155">Especifica a versão de extensão.</span><span class="sxs-lookup"><span data-stu-id="74042-155">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74042-156">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="74042-156">-X509Certificate</span></span>
<span data-ttu-id="74042-157">Especifica um certificado X. 509 que é carregado automaticamente para o serviço de nuvem e usado para criptografar a configuração privada de extensão.</span><span class="sxs-lookup"><span data-stu-id="74042-157">Specifies an X.509 certificate that is automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: SetExtension
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74042-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74042-158">CommonParameters</span></span>
<span data-ttu-id="74042-159">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74042-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74042-160">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74042-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74042-161">SENSORES</span><span class="sxs-lookup"><span data-stu-id="74042-161">INPUTS</span></span>

## <span data-ttu-id="74042-162">EXIBE</span><span class="sxs-lookup"><span data-stu-id="74042-162">OUTPUTS</span></span>

## <span data-ttu-id="74042-163">INFORMA</span><span class="sxs-lookup"><span data-stu-id="74042-163">NOTES</span></span>

## <span data-ttu-id="74042-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="74042-164">RELATED LINKS</span></span>

[<span data-ttu-id="74042-165">Get-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="74042-165">Get-AzureServiceExtension</span></span>](./Get-AzureServiceExtension.md)

[<span data-ttu-id="74042-166">Remove-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="74042-166">Remove-AzureServiceExtension</span></span>](./Remove-AzureServiceExtension.md)


