---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2563898E-C4A0-4530-AB46-30A6FC1BE55C
online version: ''
schema: 2.0.0
ms.openlocfilehash: d295e2198cdbd8168d76b1f8e19e75fb4a662116
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945895"
---
# <span data-ttu-id="cc66d-101">New-AzureServiceRemoteDesktopExtensionConfig</span><span class="sxs-lookup"><span data-stu-id="cc66d-101">New-AzureServiceRemoteDesktopExtensionConfig</span></span>

## <span data-ttu-id="cc66d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="cc66d-102">SYNOPSIS</span></span>
<span data-ttu-id="cc66d-103">Gera uma configuração de extensão da área de trabalho remota para uma implantação.</span><span class="sxs-lookup"><span data-stu-id="cc66d-103">Generates a remote desktop extension configuration for a deployment.</span></span>

## <span data-ttu-id="cc66d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cc66d-104">SYNTAX</span></span>

### <span data-ttu-id="cc66d-105">NewExtension (padrão)</span><span class="sxs-lookup"><span data-stu-id="cc66d-105">NewExtension (Default)</span></span>
```
New-AzureServiceRemoteDesktopExtensionConfig [[-Role] <String[]>] [[-X509Certificate] <X509Certificate2>]
 [[-ThumbprintAlgorithm] <String>] [-Credential] <PSCredential> [[-Expiration] <DateTime>]
 [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="cc66d-106">NewExtensionUsingThumbprint</span><span class="sxs-lookup"><span data-stu-id="cc66d-106">NewExtensionUsingThumbprint</span></span>
```
New-AzureServiceRemoteDesktopExtensionConfig [[-Role] <String[]>] [-CertificateThumbprint] <String>
 [[-ThumbprintAlgorithm] <String>] [-Credential] <PSCredential> [[-Expiration] <DateTime>]
 [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="cc66d-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="cc66d-107">DESCRIPTION</span></span>
<span data-ttu-id="cc66d-108">O cmdlet **New-AzureServiceRemoteDesktopExtensionConfig** gera uma configuração para uma extensão da área de trabalho remota para uma implantação.</span><span class="sxs-lookup"><span data-stu-id="cc66d-108">The **New-AzureServiceRemoteDesktopExtensionConfig** cmdlet generates a configuration for a remote desktop extension for a deployment.</span></span>

## <span data-ttu-id="cc66d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="cc66d-109">EXAMPLES</span></span>

### <span data-ttu-id="cc66d-110">Exemplo 1: gerar uma configuração de extensão da área de trabalho remota</span><span class="sxs-lookup"><span data-stu-id="cc66d-110">Example 1: Generate a remote desktop extension configuration</span></span>
```
PS C:\> $rdpConfig = New-AzureServiceRemoteDesktopExtensionConfig -Credential $cred
```

<span data-ttu-id="cc66d-111">Esse comando gera uma configuração de extensão da área de trabalho remota para as credenciais especificadas.</span><span class="sxs-lookup"><span data-stu-id="cc66d-111">This command generates a remote desktop extension configuration for the specified credentials.</span></span>

### <span data-ttu-id="cc66d-112">Exemplo 2: gerar uma configuração de extensão da área de trabalho remota para uma função especificada</span><span class="sxs-lookup"><span data-stu-id="cc66d-112">Example 2: Generate a remote desktop extension configuration for a specified role</span></span>
```
PS C:\> $rdpConfig = New-AzureServiceRemoteDesktopExtensionConfig -Credential $cred -Role "WebRole01"
```

<span data-ttu-id="cc66d-113">Esse comando gera uma configuração de extensão da área de trabalho remota para as credenciais especificadas e para a função WebRole01.</span><span class="sxs-lookup"><span data-stu-id="cc66d-113">This command generates a remote desktop extension configuration for the specified credentials and the WebRole01 role.</span></span>

## <span data-ttu-id="cc66d-114">OS</span><span class="sxs-lookup"><span data-stu-id="cc66d-114">PARAMETERS</span></span>

### <span data-ttu-id="cc66d-115">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="cc66d-115">-CertificateThumbprint</span></span>
<span data-ttu-id="cc66d-116">Especifica uma impressão digital de certificado a ser usada para criptografar a configuração particular.</span><span class="sxs-lookup"><span data-stu-id="cc66d-116">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="cc66d-117">Este certificado já existe no repositório de certificados.</span><span class="sxs-lookup"><span data-stu-id="cc66d-117">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="cc66d-118">Se você não especificar um certificado, esse cmdlet criará um certificado.</span><span class="sxs-lookup"><span data-stu-id="cc66d-118">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

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

### <span data-ttu-id="cc66d-119">-Credential</span><span class="sxs-lookup"><span data-stu-id="cc66d-119">-Credential</span></span>
<span data-ttu-id="cc66d-120">Especifica as credenciais a serem habilitadas para a área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="cc66d-120">Specifies the credentials to enable for remote desktop.</span></span>
<span data-ttu-id="cc66d-121">As credenciais incluem um nome de usuário e uma senha.</span><span class="sxs-lookup"><span data-stu-id="cc66d-121">Credentials include a user name and password.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc66d-122">-Expiração</span><span class="sxs-lookup"><span data-stu-id="cc66d-122">-Expiration</span></span>
<span data-ttu-id="cc66d-123">Especifica um objeto **DateTime** que permite ao usuário especificar quando a conta de usuário expira.</span><span class="sxs-lookup"><span data-stu-id="cc66d-123">Specifies a **DateTime** object that allows the user to specify when the user account expires.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc66d-124">-ExtensionId</span><span class="sxs-lookup"><span data-stu-id="cc66d-124">-ExtensionId</span></span>
<span data-ttu-id="cc66d-125">Especifica a ID de extensão.</span><span class="sxs-lookup"><span data-stu-id="cc66d-125">Specifies the extension ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc66d-126">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="cc66d-126">-InformationAction</span></span>
<span data-ttu-id="cc66d-127">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="cc66d-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="cc66d-128">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="cc66d-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cc66d-129">Contínuo</span><span class="sxs-lookup"><span data-stu-id="cc66d-129">Continue</span></span>
- <span data-ttu-id="cc66d-130">Ignorar</span><span class="sxs-lookup"><span data-stu-id="cc66d-130">Ignore</span></span>
- <span data-ttu-id="cc66d-131">Inquire</span><span class="sxs-lookup"><span data-stu-id="cc66d-131">Inquire</span></span>
- <span data-ttu-id="cc66d-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="cc66d-132">SilentlyContinue</span></span>
- <span data-ttu-id="cc66d-133">Finaliza</span><span class="sxs-lookup"><span data-stu-id="cc66d-133">Stop</span></span>
- <span data-ttu-id="cc66d-134">Suspensão</span><span class="sxs-lookup"><span data-stu-id="cc66d-134">Suspend</span></span>

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

### <span data-ttu-id="cc66d-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="cc66d-135">-InformationVariable</span></span>
<span data-ttu-id="cc66d-136">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="cc66d-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="cc66d-137">-Perfil</span><span class="sxs-lookup"><span data-stu-id="cc66d-137">-Profile</span></span>
<span data-ttu-id="cc66d-138">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="cc66d-138">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="cc66d-139">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="cc66d-139">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="cc66d-140">-Função</span><span class="sxs-lookup"><span data-stu-id="cc66d-140">-Role</span></span>
<span data-ttu-id="cc66d-141">Especifica uma matriz opcional de funções para as quais especificar a configuração da área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="cc66d-141">Specifies an optional array of roles for which to specify the remote desktop configuration.</span></span>
<span data-ttu-id="cc66d-142">Se esse parâmetro não for especificado, a configuração da área de trabalho remota será aplicada como a configuração padrão para todas as funções.</span><span class="sxs-lookup"><span data-stu-id="cc66d-142">If this parameter is not specified the remote desktop configuration is applied as the default configuration for all roles.</span></span>

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

### <span data-ttu-id="cc66d-143">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="cc66d-143">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="cc66d-144">Especifica um algoritmo de hash de impressão digital que é usado com a impressão digital para identificar o certificado.</span><span class="sxs-lookup"><span data-stu-id="cc66d-144">Specifies a thumbprint hashing algorithm which is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="cc66d-145">Esse parâmetro é opcional, e o padrão é SHA1.</span><span class="sxs-lookup"><span data-stu-id="cc66d-145">This parameter is optional and the default is sha1.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc66d-146">-Versão</span><span class="sxs-lookup"><span data-stu-id="cc66d-146">-Version</span></span>
<span data-ttu-id="cc66d-147">Especifica a versão de extensão.</span><span class="sxs-lookup"><span data-stu-id="cc66d-147">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc66d-148">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="cc66d-148">-X509Certificate</span></span>
<span data-ttu-id="cc66d-149">Especifica um certificado X509 que quando especificado será carregado automaticamente para o serviço de nuvem e usado para criptografar a configuração privada de extensão.</span><span class="sxs-lookup"><span data-stu-id="cc66d-149">Specifies an x509 certificate that when specified will be automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

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

### <span data-ttu-id="cc66d-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc66d-150">CommonParameters</span></span>
<span data-ttu-id="cc66d-151">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc66d-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc66d-152">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cc66d-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc66d-153">SENSORES</span><span class="sxs-lookup"><span data-stu-id="cc66d-153">INPUTS</span></span>

## <span data-ttu-id="cc66d-154">EXIBE</span><span class="sxs-lookup"><span data-stu-id="cc66d-154">OUTPUTS</span></span>

## <span data-ttu-id="cc66d-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="cc66d-155">NOTES</span></span>

## <span data-ttu-id="cc66d-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="cc66d-156">RELATED LINKS</span></span>

[<span data-ttu-id="cc66d-157">Set-AzureServiceRemoteDesktopExtension</span><span class="sxs-lookup"><span data-stu-id="cc66d-157">Set-AzureServiceRemoteDesktopExtension</span></span>](./Set-AzureServiceRemoteDesktopExtension.md)


