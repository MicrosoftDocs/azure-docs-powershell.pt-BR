---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E27283AF-4057-48D9-9F08-7D36290DD907
online version: ''
schema: 2.0.0
ms.openlocfilehash: dfe55fb2ced2275eae06e96480249acd99d3ad6c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945896"
---
# <span data-ttu-id="dad83-101">New-AzureServiceExtensionConfig</span><span class="sxs-lookup"><span data-stu-id="dad83-101">New-AzureServiceExtensionConfig</span></span>

## <span data-ttu-id="dad83-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dad83-102">SYNOPSIS</span></span>
<span data-ttu-id="dad83-103">Cria uma configuração de extensão de serviço de nuvem para uma implantação.</span><span class="sxs-lookup"><span data-stu-id="dad83-103">Creates a cloud service extension configuration for a deployment.</span></span>

## <span data-ttu-id="dad83-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dad83-104">SYNTAX</span></span>

### <span data-ttu-id="dad83-105">NewExtension (padrão)</span><span class="sxs-lookup"><span data-stu-id="dad83-105">NewExtension (Default)</span></span>
```
New-AzureServiceExtensionConfig [[-Role] <String[]>] [[-X509Certificate] <X509Certificate2>]
 [[-ThumbprintAlgorithm] <String>] [-ExtensionName] <String> [-ProviderNamespace] <String>
 [-PublicConfiguration] <String> [-PrivateConfiguration] <String> [-Version] <String> [[-ExtensionId] <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="dad83-106">NewExtensionUsingThumbprint</span><span class="sxs-lookup"><span data-stu-id="dad83-106">NewExtensionUsingThumbprint</span></span>
```
New-AzureServiceExtensionConfig [[-Role] <String[]>] [-CertificateThumbprint] <String>
 [[-ThumbprintAlgorithm] <String>] [-ExtensionName] <String> [-ProviderNamespace] <String>
 [-PublicConfiguration] <String> [-PrivateConfiguration] <String> [-Version] <String> [[-ExtensionId] <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="dad83-107">UpdateExtensionStatusParameterSetName</span><span class="sxs-lookup"><span data-stu-id="dad83-107">UpdateExtensionStatusParameterSetName</span></span>
```
New-AzureServiceExtensionConfig [[-Role] <String[]>] [-ExtensionId] <String> [-ExtensionState] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="dad83-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dad83-108">DESCRIPTION</span></span>
<span data-ttu-id="dad83-109">O cmdlet **New-AzureServiceExtensionConfig** cria uma configuração de extensão de serviço de nuvem para uma implantação.</span><span class="sxs-lookup"><span data-stu-id="dad83-109">The **New-AzureServiceExtensionConfig** cmdlet creates a cloud service extension configuration for a deployment.</span></span>

## <span data-ttu-id="dad83-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dad83-110">EXAMPLES</span></span>

### <span data-ttu-id="dad83-111">Exemplo 1: criar uma configuração de extensão</span><span class="sxs-lookup"><span data-stu-id="dad83-111">Example 1: Create an extension configuration</span></span>
```
PS C:\> New-AzureServiceExtensionConfig -ExtensionName 'RDP' -Version '1.0' -ProviderNamespace Microsoft.Windows.Azure.Extensions -PublicConfiguration $p1 -PrivateConfiguration $p2;
```

<span data-ttu-id="dad83-112">Esse comando especifica uma configuração de extensão.</span><span class="sxs-lookup"><span data-stu-id="dad83-112">This command specifies an extension configuration.</span></span>

### <span data-ttu-id="dad83-113">Exemplo 2: criar uma configuração de extensão para uma função</span><span class="sxs-lookup"><span data-stu-id="dad83-113">Example 2: Create an extension configuration for a role</span></span>
```
PS C:\> New-AzureServiceExtensionConfig -Role WebRole1 -ExtensionName 'RDP' -ProviderNamespace Microsoft.Windows.Azure.Extensions -PublicConfiguration $p1 -PrivateConfiguration $p2;
```

<span data-ttu-id="dad83-114">Esse comando especifica uma configuração de extensão para a função WebRole1.</span><span class="sxs-lookup"><span data-stu-id="dad83-114">This command specifies an extension configuration for the role WebRole1.</span></span>

## <span data-ttu-id="dad83-115">OS</span><span class="sxs-lookup"><span data-stu-id="dad83-115">PARAMETERS</span></span>

### <span data-ttu-id="dad83-116">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="dad83-116">-CertificateThumbprint</span></span>
<span data-ttu-id="dad83-117">Especifica uma impressão digital de certificado a ser usada para criptografar a configuração particular.</span><span class="sxs-lookup"><span data-stu-id="dad83-117">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="dad83-118">Este certificado já existe no repositório de certificados.</span><span class="sxs-lookup"><span data-stu-id="dad83-118">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="dad83-119">Se você não especificar um certificado, esse cmdlet criará um certificado.</span><span class="sxs-lookup"><span data-stu-id="dad83-119">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

```yaml
Type: String
Parameter Sets: NewExtensionUsingThumbprint
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dad83-120">-ExtensionId</span><span class="sxs-lookup"><span data-stu-id="dad83-120">-ExtensionId</span></span>
<span data-ttu-id="dad83-121">Especifica o nome da extensão.</span><span class="sxs-lookup"><span data-stu-id="dad83-121">Specifies the name of the extension.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: UpdateExtensionStatusParameterSetName
Aliases: 

Required: True
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dad83-122">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="dad83-122">-ExtensionName</span></span>
<span data-ttu-id="dad83-123">Especifica o nome da extensão.</span><span class="sxs-lookup"><span data-stu-id="dad83-123">Specifies the name of the extension.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dad83-124">-Extensionstate</span><span class="sxs-lookup"><span data-stu-id="dad83-124">-ExtensionState</span></span>
<span data-ttu-id="dad83-125">Especifica o estado da extensão.</span><span class="sxs-lookup"><span data-stu-id="dad83-125">Specifies the state of the extension.</span></span>
<span data-ttu-id="dad83-126">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="dad83-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="dad83-127">Ativação</span><span class="sxs-lookup"><span data-stu-id="dad83-127">Enable</span></span> 
- <span data-ttu-id="dad83-128">Desabilita</span><span class="sxs-lookup"><span data-stu-id="dad83-128">Disable</span></span> 
- <span data-ttu-id="dad83-129">Remover</span><span class="sxs-lookup"><span data-stu-id="dad83-129">Uninstall</span></span>

```yaml
Type: String
Parameter Sets: UpdateExtensionStatusParameterSetName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dad83-130">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="dad83-130">-InformationAction</span></span>
<span data-ttu-id="dad83-131">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="dad83-131">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="dad83-132">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="dad83-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="dad83-133">Contínuo</span><span class="sxs-lookup"><span data-stu-id="dad83-133">Continue</span></span>
- <span data-ttu-id="dad83-134">Ignorar</span><span class="sxs-lookup"><span data-stu-id="dad83-134">Ignore</span></span>
- <span data-ttu-id="dad83-135">Inquire</span><span class="sxs-lookup"><span data-stu-id="dad83-135">Inquire</span></span>
- <span data-ttu-id="dad83-136">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="dad83-136">SilentlyContinue</span></span>
- <span data-ttu-id="dad83-137">Finaliza</span><span class="sxs-lookup"><span data-stu-id="dad83-137">Stop</span></span>
- <span data-ttu-id="dad83-138">Suspensão</span><span class="sxs-lookup"><span data-stu-id="dad83-138">Suspend</span></span>

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

### <span data-ttu-id="dad83-139">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="dad83-139">-InformationVariable</span></span>
<span data-ttu-id="dad83-140">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="dad83-140">Specifies an information variable.</span></span>

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

### <span data-ttu-id="dad83-141">-PrivateConfiguration</span><span class="sxs-lookup"><span data-stu-id="dad83-141">-PrivateConfiguration</span></span>
<span data-ttu-id="dad83-142">Especifica o texto de configuração particular.</span><span class="sxs-lookup"><span data-stu-id="dad83-142">Specifies the private configuration text.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dad83-143">-Perfil</span><span class="sxs-lookup"><span data-stu-id="dad83-143">-Profile</span></span>
<span data-ttu-id="dad83-144">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="dad83-144">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="dad83-145">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="dad83-145">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="dad83-146">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="dad83-146">-ProviderNamespace</span></span>
<span data-ttu-id="dad83-147">Especifica o namespace do provedor da extensão.</span><span class="sxs-lookup"><span data-stu-id="dad83-147">Specifies the Extension's Provider Namespace.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dad83-148">-PublicConfiguration</span><span class="sxs-lookup"><span data-stu-id="dad83-148">-PublicConfiguration</span></span>
<span data-ttu-id="dad83-149">Especifica o texto de configuração pública.</span><span class="sxs-lookup"><span data-stu-id="dad83-149">Specifies the public configuration text.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dad83-150">-Função</span><span class="sxs-lookup"><span data-stu-id="dad83-150">-Role</span></span>
<span data-ttu-id="dad83-151">Especifica uma matriz opcional de funções para especificar a configuração da área de trabalho remota para.</span><span class="sxs-lookup"><span data-stu-id="dad83-151">Specifies an optional array of roles to specify the remote desktop configuration for.</span></span>
<span data-ttu-id="dad83-152">Se não especificado, a configuração da área de trabalho remota será aplicada como a configuração padrão para todas as funções.</span><span class="sxs-lookup"><span data-stu-id="dad83-152">If not specified the remote desktop configuration is applied as the default configuration for all roles.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dad83-153">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="dad83-153">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="dad83-154">Especifica um algoritmo de hash de impressão digital que é usado com a impressão digital para identificar o certificado.</span><span class="sxs-lookup"><span data-stu-id="dad83-154">Specifies a thumbprint hashing algorithm which is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="dad83-155">Esse parâmetro é opcional, e o padrão é SHA1.</span><span class="sxs-lookup"><span data-stu-id="dad83-155">This parameter is optional and the default is sha1.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dad83-156">-Versão</span><span class="sxs-lookup"><span data-stu-id="dad83-156">-Version</span></span>
<span data-ttu-id="dad83-157">Especifica a versão de extensão.</span><span class="sxs-lookup"><span data-stu-id="dad83-157">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dad83-158">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="dad83-158">-X509Certificate</span></span>
<span data-ttu-id="dad83-159">Especifica um certificado X509 que quando especificado será carregado automaticamente para o serviço de nuvem e usado para criptografar a configuração privada de extensão.</span><span class="sxs-lookup"><span data-stu-id="dad83-159">Specifies an x509 certificate that when specified will be automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: NewExtension
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dad83-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dad83-160">CommonParameters</span></span>
<span data-ttu-id="dad83-161">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dad83-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dad83-162">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dad83-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dad83-163">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dad83-163">INPUTS</span></span>

## <span data-ttu-id="dad83-164">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dad83-164">OUTPUTS</span></span>

## <span data-ttu-id="dad83-165">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dad83-165">NOTES</span></span>

## <span data-ttu-id="dad83-166">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dad83-166">RELATED LINKS</span></span>

[<span data-ttu-id="dad83-167">Get-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="dad83-167">Get-AzureServiceExtension</span></span>](./Get-AzureServiceExtension.md)

[<span data-ttu-id="dad83-168">Set-AzureServiceExtension</span><span class="sxs-lookup"><span data-stu-id="dad83-168">Set-AzureServiceExtension</span></span>](./Set-AzureServiceExtension.md)


