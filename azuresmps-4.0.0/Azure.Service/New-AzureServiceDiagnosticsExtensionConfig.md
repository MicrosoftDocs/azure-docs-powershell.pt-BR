---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1F76C63E-5289-4F88-9522-3FF4EF732908
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8a232ec03da38ea3d527dcd9aa214dbf681bcc6a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945898"
---
# <span data-ttu-id="c506b-101">New-AzureServiceDiagnosticsExtensionConfig</span><span class="sxs-lookup"><span data-stu-id="c506b-101">New-AzureServiceDiagnosticsExtensionConfig</span></span>

## <span data-ttu-id="c506b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c506b-102">SYNOPSIS</span></span>
<span data-ttu-id="c506b-103">Gera uma configuração para uma extensão de diagnóstico para as funções especificadas ou todas as funções.</span><span class="sxs-lookup"><span data-stu-id="c506b-103">Generates a configuration for a diagnostics extension for specified role(s) or all roles.</span></span>

## <span data-ttu-id="c506b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c506b-104">SYNTAX</span></span>

### <span data-ttu-id="c506b-105">NewExtension (padrão)</span><span class="sxs-lookup"><span data-stu-id="c506b-105">NewExtension (Default)</span></span>
```
New-AzureServiceDiagnosticsExtensionConfig [[-Role] <String[]>] [[-X509Certificate] <X509Certificate2>]
 [[-ThumbprintAlgorithm] <String>] [[-StorageAccountName] <String>] [[-StorageAccountKey] <String>]
 [[-StorageAccountEndpoint] <String>] [[-StorageContext] <AzureStorageContext>]
 [-DiagnosticsConfigurationPath] <String> [[-ExtensionId] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="c506b-106">NewExtensionUsingThumbprint</span><span class="sxs-lookup"><span data-stu-id="c506b-106">NewExtensionUsingThumbprint</span></span>
```
New-AzureServiceDiagnosticsExtensionConfig [[-Role] <String[]>] [-CertificateThumbprint] <String>
 [[-ThumbprintAlgorithm] <String>] [[-StorageAccountKey] <String>] [[-StorageAccountEndpoint] <String>]
 [[-StorageContext] <AzureStorageContext>] [-DiagnosticsConfigurationPath] <String> [[-ExtensionId] <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="c506b-107">SetExtensionUsingThumbprint</span><span class="sxs-lookup"><span data-stu-id="c506b-107">SetExtensionUsingThumbprint</span></span>
```
New-AzureServiceDiagnosticsExtensionConfig [[-StorageAccountName] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c506b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c506b-108">DESCRIPTION</span></span>
<span data-ttu-id="c506b-109">O cmdlet **New-AzureServiceDiagnosticsExtensionConfig** gera uma configuração para uma extensão de diagnóstico para funções especificadas ou todas as funções.</span><span class="sxs-lookup"><span data-stu-id="c506b-109">The **New-AzureServiceDiagnosticsExtensionConfig** cmdlet generates a configuration for a diagnostics extension for specified roles or all roles.</span></span>

## <span data-ttu-id="c506b-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c506b-110">EXAMPLES</span></span>

### <span data-ttu-id="c506b-111">Exemplo 1: criar a extensão de diagnóstico do Azure para todas as funções no serviço na nuvem</span><span class="sxs-lookup"><span data-stu-id="c506b-111">Example 1: Create the Azure Diagnostics extension for all roles in the cloud service</span></span>
```
PS C:\> $WadConfig = New-AzureServiceDiagnosticExtensionConfig -StorageContext $StorageContext -DiagnosticsConfigurationPath $WadConfigXML
```

<span data-ttu-id="c506b-112">Esse comando cria a extensão de diagnóstico do Azure para todas as funções no serviço na nuvem.</span><span class="sxs-lookup"><span data-stu-id="c506b-112">This command creates the Azure Diagnostics extension for all of the roles in the cloud service.</span></span>

### <span data-ttu-id="c506b-113">Exemplo 2: criar a extensão de diagnóstico do Azure para uma função</span><span class="sxs-lookup"><span data-stu-id="c506b-113">Example 2: Create the Azure Diagnostics extension for a role</span></span>
```
PS C:\> $WadConfig = New-AzureServiceDiagnosticExtensionConfig -StorageContext $StorageContext -DiagnosticsConfigurationPath $WadConfigXML -Role "WebRole1"
```

<span data-ttu-id="c506b-114">Esse comando cria a extensão de diagnóstico do Azure para a função WebRole01 no serviço na nuvem.</span><span class="sxs-lookup"><span data-stu-id="c506b-114">This command creates the Azure Diagnostics extension for the role WebRole01 in the cloud service.</span></span>

## <span data-ttu-id="c506b-115">OS</span><span class="sxs-lookup"><span data-stu-id="c506b-115">PARAMETERS</span></span>

### <span data-ttu-id="c506b-116">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="c506b-116">-CertificateThumbprint</span></span>
<span data-ttu-id="c506b-117">Especifica uma impressão digital de certificado a ser usada para criptografar a configuração particular.</span><span class="sxs-lookup"><span data-stu-id="c506b-117">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="c506b-118">Este certificado já existe no repositório de certificados.</span><span class="sxs-lookup"><span data-stu-id="c506b-118">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="c506b-119">Se você não especificar um certificado, esse cmdlet criará um certificado.</span><span class="sxs-lookup"><span data-stu-id="c506b-119">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

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

### <span data-ttu-id="c506b-120">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="c506b-120">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="c506b-121">Especifica o caminho de configuração do diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="c506b-121">Specifies the diagnostics configuration path.</span></span>

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

### <span data-ttu-id="c506b-122">-ExtensionId</span><span class="sxs-lookup"><span data-stu-id="c506b-122">-ExtensionId</span></span>
<span data-ttu-id="c506b-123">Especifica a ID de extensão.</span><span class="sxs-lookup"><span data-stu-id="c506b-123">Specifies the extension ID.</span></span>

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

### <span data-ttu-id="c506b-124">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="c506b-124">-InformationAction</span></span>
<span data-ttu-id="c506b-125">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="c506b-125">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c506b-126">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="c506b-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c506b-127">Contínuo</span><span class="sxs-lookup"><span data-stu-id="c506b-127">Continue</span></span>
- <span data-ttu-id="c506b-128">Ignorar</span><span class="sxs-lookup"><span data-stu-id="c506b-128">Ignore</span></span>
- <span data-ttu-id="c506b-129">Inquire</span><span class="sxs-lookup"><span data-stu-id="c506b-129">Inquire</span></span>
- <span data-ttu-id="c506b-130">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c506b-130">SilentlyContinue</span></span>
- <span data-ttu-id="c506b-131">Finaliza</span><span class="sxs-lookup"><span data-stu-id="c506b-131">Stop</span></span>
- <span data-ttu-id="c506b-132">Suspensão</span><span class="sxs-lookup"><span data-stu-id="c506b-132">Suspend</span></span>

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

### <span data-ttu-id="c506b-133">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c506b-133">-InformationVariable</span></span>
<span data-ttu-id="c506b-134">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="c506b-134">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c506b-135">-Perfil</span><span class="sxs-lookup"><span data-stu-id="c506b-135">-Profile</span></span>
<span data-ttu-id="c506b-136">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="c506b-136">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c506b-137">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="c506b-137">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c506b-138">-Função</span><span class="sxs-lookup"><span data-stu-id="c506b-138">-Role</span></span>
<span data-ttu-id="c506b-139">Especifica uma matriz opcional de funções para especificar a configuração de diagnóstico para.</span><span class="sxs-lookup"><span data-stu-id="c506b-139">Specifies an optional array of roles to specify the diagnostics configuration for.</span></span>
<span data-ttu-id="c506b-140">Se não especificado, a configuração de diagnóstico será aplicada como a configuração padrão para todas as funções.</span><span class="sxs-lookup"><span data-stu-id="c506b-140">If not specified the diagnostics configuration is applied as the default configuration for all roles.</span></span>

```yaml
Type: String[]
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c506b-141">-StorageAccountEndpoint</span><span class="sxs-lookup"><span data-stu-id="c506b-141">-StorageAccountEndpoint</span></span>
<span data-ttu-id="c506b-142">Especifica o ponto de extremidade da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c506b-142">Specifies the storage account endpoint.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c506b-143">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="c506b-143">-StorageAccountKey</span></span>
<span data-ttu-id="c506b-144">Especifica a chave da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c506b-144">Specifies the storage account key.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c506b-145">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c506b-145">-StorageAccountName</span></span>
<span data-ttu-id="c506b-146">Especifica o nome da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c506b-146">Specifies the storage account name.</span></span>

```yaml
Type: String
Parameter Sets: NewExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c506b-147">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="c506b-147">-StorageContext</span></span>
<span data-ttu-id="c506b-148">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="c506b-148">Specifies an Azure storage context.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: NewExtension, NewExtensionUsingThumbprint
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c506b-149">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="c506b-149">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="c506b-150">Especifica um algoritmo de hash de impressão digital que é usado com a impressão digital para identificar o certificado.</span><span class="sxs-lookup"><span data-stu-id="c506b-150">Specifies a thumbprint hashing algorithm which is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="c506b-151">Esse parâmetro é opcional, e o padrão é SHA1.</span><span class="sxs-lookup"><span data-stu-id="c506b-151">This parameter is optional and the default is sha1.</span></span>

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

### <span data-ttu-id="c506b-152">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="c506b-152">-X509Certificate</span></span>
<span data-ttu-id="c506b-153">Especifica um certificado X. 509 que é carregado automaticamente para o serviço de nuvem e usado para criptografar a configuração privada de extensão.</span><span class="sxs-lookup"><span data-stu-id="c506b-153">Specifies an X.509 certificate that is automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

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

### <span data-ttu-id="c506b-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c506b-154">CommonParameters</span></span>
<span data-ttu-id="c506b-155">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c506b-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c506b-156">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c506b-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c506b-157">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c506b-157">INPUTS</span></span>

## <span data-ttu-id="c506b-158">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c506b-158">OUTPUTS</span></span>

## <span data-ttu-id="c506b-159">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c506b-159">NOTES</span></span>

## <span data-ttu-id="c506b-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c506b-160">RELATED LINKS</span></span>

[<span data-ttu-id="c506b-161">Get-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="c506b-161">Get-AzureServiceDiagnosticsExtension</span></span>](./Get-AzureServiceDiagnosticsExtension.md)

[<span data-ttu-id="c506b-162">Set-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="c506b-162">Set-AzureServiceDiagnosticsExtension</span></span>](./Set-AzureServiceDiagnosticsExtension.md)


