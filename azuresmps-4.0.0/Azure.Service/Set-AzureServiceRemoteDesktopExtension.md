---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5C8B1482-80B0-4060-A35D-E9D394156886
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9a6303e685ea02408772a237c6b5f154764107e4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945813"
---
# <span data-ttu-id="ba0cb-101">Set-AzureServiceRemoteDesktopExtension</span><span class="sxs-lookup"><span data-stu-id="ba0cb-101">Set-AzureServiceRemoteDesktopExtension</span></span>

## <span data-ttu-id="ba0cb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ba0cb-102">SYNOPSIS</span></span>
<span data-ttu-id="ba0cb-103">Habilita a extensão da área de trabalho remota em funções especificadas ou todas as funções em um serviço implantado ou na implantação.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-103">Enables remote desktop extension on specified role(s) or all roles on a deployed service or at deployment.</span></span>

## <span data-ttu-id="ba0cb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ba0cb-104">SYNTAX</span></span>

### <span data-ttu-id="ba0cb-105">Setextension (padrão)</span><span class="sxs-lookup"><span data-stu-id="ba0cb-105">SetExtension (Default)</span></span>
```
Set-AzureServiceRemoteDesktopExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-X509Certificate] <X509Certificate2>] [[-ThumbprintAlgorithm] <String>] [-Credential] <PSCredential>
 [[-Expiration] <DateTime>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="ba0cb-106">SetExtensionUsingThumbprint</span><span class="sxs-lookup"><span data-stu-id="ba0cb-106">SetExtensionUsingThumbprint</span></span>
```
Set-AzureServiceRemoteDesktopExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [-CertificateThumbprint] <String> [[-ThumbprintAlgorithm] <String>] [-Credential] <PSCredential>
 [[-Expiration] <DateTime>] [[-Version] <String>] [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ba0cb-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ba0cb-107">DESCRIPTION</span></span>
<span data-ttu-id="ba0cb-108">O cmdlet **set-AzureServiceRemoteDesktopExtension** habilita a extensão da área de trabalho remota em funções especificadas ou todas as funções em um serviço implantado ou na implantação.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-108">The **Set-AzureServiceRemoteDesktopExtension** cmdlet enables remote desktop extension on specified roles or all roles on a deployed service or at deployment.</span></span>

## <span data-ttu-id="ba0cb-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ba0cb-109">EXAMPLES</span></span>

### <span data-ttu-id="ba0cb-110">Exemplo 1: habilitar a extensão da área de trabalho remota</span><span class="sxs-lookup"><span data-stu-id="ba0cb-110">Example 1: Enable remote desktop extension</span></span>
```
PS C:\> Set-AzureServiceRemoteDesktopExtension -ServiceName $svc -Credentials $creds
```

<span data-ttu-id="ba0cb-111">Esse comando habilita a extensão da área de trabalho remota para o serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-111">This command enables the remote desktop extension for the specified service.</span></span>

### <span data-ttu-id="ba0cb-112">Exemplo 2: habilitar a extensão da área de trabalho remota para uma função especificada</span><span class="sxs-lookup"><span data-stu-id="ba0cb-112">Example 2: Enable remote desktop extension for a specified role</span></span>
```
PS C:\> Set-AzureServiceRemoteDesktopExtension -ServiceName $svc -Credentials $creds -Role "WebRole1"
```

<span data-ttu-id="ba0cb-113">Esse comando habilita a extensão da área de trabalho remota para o serviço e função especificados.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-113">This command enables the remote desktop extension for the specified service and role.</span></span>

## <span data-ttu-id="ba0cb-114">OS</span><span class="sxs-lookup"><span data-stu-id="ba0cb-114">PARAMETERS</span></span>

### <span data-ttu-id="ba0cb-115">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="ba0cb-115">-CertificateThumbprint</span></span>
<span data-ttu-id="ba0cb-116">Especifica uma impressão digital de certificado a ser usada para criptografar a configuração particular.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-116">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="ba0cb-117">Este certificado já existe no repositório de certificados.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-117">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="ba0cb-118">Se você não especificar um certificado, esse cmdlet criará um certificado.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-118">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

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

### <span data-ttu-id="ba0cb-119">-Credential</span><span class="sxs-lookup"><span data-stu-id="ba0cb-119">-Credential</span></span>
<span data-ttu-id="ba0cb-120">Especifica as credenciais a serem habilitadas para a área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-120">Specifies the credentials to enable for remote desktop.</span></span>
<span data-ttu-id="ba0cb-121">As credenciais incluem um nome de usuário e uma senha.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-121">Credentials include a user name and password.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba0cb-122">-Expiração</span><span class="sxs-lookup"><span data-stu-id="ba0cb-122">-Expiration</span></span>
<span data-ttu-id="ba0cb-123">Especifica um objeto de data/hora que permite ao usuário especificar quando a conta de usuário expira.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-123">Specifies a date time object that allows the user to specify when the user account expires.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba0cb-124">-ExtensionId</span><span class="sxs-lookup"><span data-stu-id="ba0cb-124">-ExtensionId</span></span>
<span data-ttu-id="ba0cb-125">Especifica a ID de extensão.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-125">Specifies the extension ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba0cb-126">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="ba0cb-126">-InformationAction</span></span>
<span data-ttu-id="ba0cb-127">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ba0cb-128">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="ba0cb-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ba0cb-129">Contínuo</span><span class="sxs-lookup"><span data-stu-id="ba0cb-129">Continue</span></span>
- <span data-ttu-id="ba0cb-130">Ignorar</span><span class="sxs-lookup"><span data-stu-id="ba0cb-130">Ignore</span></span>
- <span data-ttu-id="ba0cb-131">Inquire</span><span class="sxs-lookup"><span data-stu-id="ba0cb-131">Inquire</span></span>
- <span data-ttu-id="ba0cb-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ba0cb-132">SilentlyContinue</span></span>
- <span data-ttu-id="ba0cb-133">Finaliza</span><span class="sxs-lookup"><span data-stu-id="ba0cb-133">Stop</span></span>
- <span data-ttu-id="ba0cb-134">Suspensão</span><span class="sxs-lookup"><span data-stu-id="ba0cb-134">Suspend</span></span>

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

### <span data-ttu-id="ba0cb-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ba0cb-135">-InformationVariable</span></span>
<span data-ttu-id="ba0cb-136">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-136">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ba0cb-137">-Perfil</span><span class="sxs-lookup"><span data-stu-id="ba0cb-137">-Profile</span></span>
<span data-ttu-id="ba0cb-138">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-138">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ba0cb-139">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-139">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ba0cb-140">-Função</span><span class="sxs-lookup"><span data-stu-id="ba0cb-140">-Role</span></span>
<span data-ttu-id="ba0cb-141">Especifica uma matriz opcional de funções para as quais especificar a configuração da área de trabalho remota.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-141">Specifies an optional array of roles for which to specify the remote desktop configuration.</span></span>
<span data-ttu-id="ba0cb-142">Se esse parâmetro não for especificado, a configuração da área de trabalho remota será aplicada como a configuração padrão para todas as funções.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-142">If this parameter is not specified, the remote desktop configuration is applied as the default configuration for all roles.</span></span>

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

### <span data-ttu-id="ba0cb-143">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="ba0cb-143">-ServiceName</span></span>
<span data-ttu-id="ba0cb-144">Especifica o nome do serviço do Azure da implantação.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-144">Specifies the Azure service name of the deployment.</span></span>

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

### <span data-ttu-id="ba0cb-145">-Slot</span><span class="sxs-lookup"><span data-stu-id="ba0cb-145">-Slot</span></span>
<span data-ttu-id="ba0cb-146">Especifica o ambiente da implantação a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-146">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="ba0cb-147">Os valores aceitáveis para esse parâmetro são: produção, preparação.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-147">The acceptable values for this parameter are: Production, Staging.</span></span>

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

### <span data-ttu-id="ba0cb-148">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="ba0cb-148">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="ba0cb-149">Especifica um algoritmo de hash de impressão digital que é usado com a impressão digital para identificar o certificado.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-149">Specifies a thumbprint hashing algorithm which is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="ba0cb-150">Esse parâmetro é opcional, e o padrão é SHA1.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-150">This parameter is optional and the default is sha1.</span></span>

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

### <span data-ttu-id="ba0cb-151">-Versão</span><span class="sxs-lookup"><span data-stu-id="ba0cb-151">-Version</span></span>
<span data-ttu-id="ba0cb-152">Especifica a versão de extensão.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-152">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba0cb-153">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="ba0cb-153">-X509Certificate</span></span>
<span data-ttu-id="ba0cb-154">Especifica um certificado X509 que é carregado automaticamente para o serviço na nuvem e usado para criptografar a configuração particular da extensão.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-154">Specifies an x509 certificate that is automatically uploaded to the cloud service and used for encrypting the private configuration of the extension.</span></span>

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

### <span data-ttu-id="ba0cb-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba0cb-155">CommonParameters</span></span>
<span data-ttu-id="ba0cb-156">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba0cb-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba0cb-157">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba0cb-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba0cb-158">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ba0cb-158">INPUTS</span></span>

## <span data-ttu-id="ba0cb-159">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ba0cb-159">OUTPUTS</span></span>

## <span data-ttu-id="ba0cb-160">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ba0cb-160">NOTES</span></span>

## <span data-ttu-id="ba0cb-161">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ba0cb-161">RELATED LINKS</span></span>

[<span data-ttu-id="ba0cb-162">Get-AzureServiceRemoteDesktopExtension</span><span class="sxs-lookup"><span data-stu-id="ba0cb-162">Get-AzureServiceRemoteDesktopExtension</span></span>](./Get-AzureServiceRemoteDesktopExtension.md)


