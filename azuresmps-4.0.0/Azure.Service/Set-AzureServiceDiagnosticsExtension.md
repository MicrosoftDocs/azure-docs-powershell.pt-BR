---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2E738CEF-BBDD-425D-B12C-86FF7C45A634
online version: ''
schema: 2.0.0
ms.openlocfilehash: 518528d4af8889cf36b30c417e0170e0ea228ebf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946047"
---
# <span data-ttu-id="0b365-101">Set-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="0b365-101">Set-AzureServiceDiagnosticsExtension</span></span>

## <span data-ttu-id="0b365-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="0b365-102">SYNOPSIS</span></span>
<span data-ttu-id="0b365-103">Habilita a extensão do diagnóstico do Azure em funções especificadas ou todas as funções em um serviço implantado ou na implantação.</span><span class="sxs-lookup"><span data-stu-id="0b365-103">Enables Azure Diagnostics extension on specified roles or all roles on a deployed service or at deployment.</span></span>

## <span data-ttu-id="0b365-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0b365-104">SYNTAX</span></span>

### <span data-ttu-id="0b365-105">Setextension (padrão)</span><span class="sxs-lookup"><span data-stu-id="0b365-105">SetExtension (Default)</span></span>
```
Set-AzureServiceDiagnosticsExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-X509Certificate] <X509Certificate2>] [[-ThumbprintAlgorithm] <String>] [[-StorageAccountName] <String>]
 [[-StorageAccountKey] <String>] [[-StorageAccountEndpoint] <String>] [[-StorageContext] <AzureStorageContext>]
 [-DiagnosticsConfigurationPath] <String> [[-Version] <String>] [[-ExtensionId] <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="0b365-106">SetExtensionUsingThumbprint</span><span class="sxs-lookup"><span data-stu-id="0b365-106">SetExtensionUsingThumbprint</span></span>
```
Set-AzureServiceDiagnosticsExtension [[-ServiceName] <String>] [[-Slot] <String>] [[-Role] <String[]>]
 [[-CertificateThumbprint] <String>] [[-ThumbprintAlgorithm] <String>] [[-StorageAccountName] <String>]
 [[-StorageAccountKey] <String>] [[-StorageAccountEndpoint] <String>] [[-StorageContext] <AzureStorageContext>]
 [-DiagnosticsConfigurationPath] <String> [[-Version] <String>] [[-ExtensionId] <String>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="0b365-107">SetExtensionUsingDiagnosticsConfiguration</span><span class="sxs-lookup"><span data-stu-id="0b365-107">SetExtensionUsingDiagnosticsConfiguration</span></span>
```
Set-AzureServiceDiagnosticsExtension [[-ServiceName] <String>] [[-Slot] <String>]
 [-DiagnosticsConfiguration] <ExtensionConfigurationInput[]> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="0b365-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="0b365-108">DESCRIPTION</span></span>
<span data-ttu-id="0b365-109">O cmdlet **set-AzureServiceDiagnosticsExtension** habilita a extensão do diagnóstico do Azure em funções especificadas ou todas as funções em um serviço implantado ou na implantação.</span><span class="sxs-lookup"><span data-stu-id="0b365-109">The **Set-AzureServiceDiagnosticsExtension** cmdlet enables Azure Diagnostics extension on specified roles or all roles on a deployed service or at deployment.</span></span>

## <span data-ttu-id="0b365-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="0b365-110">EXAMPLES</span></span>

### <span data-ttu-id="0b365-111">Exemplo 1: habilitar a extensão do diagnóstico do Azure</span><span class="sxs-lookup"><span data-stu-id="0b365-111">Example 1: Enable Azure Diagnostics extension</span></span>
```
PS C:\> Set-AzureServiceDiagnosticsExtension -ServiceName $Svc -StorageContext $StorageContext -DiagnosticsConfigurationPath $WadConfigXML
```

<span data-ttu-id="0b365-112">Esse comando habilita a extensão do diagnóstico do Azure para todas as funções.</span><span class="sxs-lookup"><span data-stu-id="0b365-112">This command enables the Azure Diagnostics extension for all roles.</span></span>

### <span data-ttu-id="0b365-113">Exemplo 2: habilitar a extensão do diagnóstico do Azure para uma função especificada</span><span class="sxs-lookup"><span data-stu-id="0b365-113">Example 2: Enable Azure Diagnostics extension for a specified role</span></span>
```
PS C:\> Set-AzureServiceDiagnosticsExtension -ServiceName $Svc -StorageContext $StorageContext -DiagnosticsConfigurationPath $WadConfigXML -Role "WebRole01"
```

<span data-ttu-id="0b365-114">Esse comando habilita a extensão do diagnóstico do Azure para uma função especificada.</span><span class="sxs-lookup"><span data-stu-id="0b365-114">This command enables the Azure Diagnostics extension for a specified role.</span></span>

## <span data-ttu-id="0b365-115">OS</span><span class="sxs-lookup"><span data-stu-id="0b365-115">PARAMETERS</span></span>

### <span data-ttu-id="0b365-116">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="0b365-116">-CertificateThumbprint</span></span>
<span data-ttu-id="0b365-117">Especifica uma impressão digital de certificado a ser usada para criptografar a configuração particular.</span><span class="sxs-lookup"><span data-stu-id="0b365-117">Specifies a certificate thumbprint to use to encrypt the private configuration.</span></span>
<span data-ttu-id="0b365-118">Este certificado já existe no repositório de certificados.</span><span class="sxs-lookup"><span data-stu-id="0b365-118">This certificate has to already exist in the certificate store.</span></span>
<span data-ttu-id="0b365-119">Se você não especificar um certificado, esse cmdlet criará um certificado.</span><span class="sxs-lookup"><span data-stu-id="0b365-119">If you do not specify a certificate, this cmdlet creates a certificate.</span></span>

```yaml
Type: String
Parameter Sets: SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b365-120">-DiagnosticsConfiguration</span><span class="sxs-lookup"><span data-stu-id="0b365-120">-DiagnosticsConfiguration</span></span>
<span data-ttu-id="0b365-121">Especifica uma matriz de configuração para o diagnóstico do Azure.</span><span class="sxs-lookup"><span data-stu-id="0b365-121">Specifies an array of configuration for Azure Diagnostics.</span></span>

```yaml
Type: ExtensionConfigurationInput[]
Parameter Sets: SetExtensionUsingDiagnosticsConfiguration
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b365-122">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="0b365-122">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="0b365-123">Especifica a configuração do diagnóstico do Azure.</span><span class="sxs-lookup"><span data-stu-id="0b365-123">Specifies the configuration for Azure Diagnostics.</span></span>
<span data-ttu-id="0b365-124">Você pode baixar o esquema usando o seguinte comando:</span><span class="sxs-lookup"><span data-stu-id="0b365-124">You can download the schema by using the following command:</span></span> 

`(Get-AzureServiceAvailableExtension -ExtensionName 'PaaSDiagnostics' -ProviderNamespace 'Microsoft.Azure.Diagnostics').PublicConfigurationSchema | Out-File -Encoding utf8 -FilePath 'WadConfig.xsd'`

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: True
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b365-125">-ExtensionId</span><span class="sxs-lookup"><span data-stu-id="0b365-125">-ExtensionId</span></span>
<span data-ttu-id="0b365-126">Especifica a ID da extensão</span><span class="sxs-lookup"><span data-stu-id="0b365-126">Specifies the extension ID</span></span>

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b365-127">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="0b365-127">-InformationAction</span></span>
<span data-ttu-id="0b365-128">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="0b365-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="0b365-129">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="0b365-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0b365-130">Contínuo</span><span class="sxs-lookup"><span data-stu-id="0b365-130">Continue</span></span>
- <span data-ttu-id="0b365-131">Ignorar</span><span class="sxs-lookup"><span data-stu-id="0b365-131">Ignore</span></span>
- <span data-ttu-id="0b365-132">Inquire</span><span class="sxs-lookup"><span data-stu-id="0b365-132">Inquire</span></span>
- <span data-ttu-id="0b365-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="0b365-133">SilentlyContinue</span></span>
- <span data-ttu-id="0b365-134">Finaliza</span><span class="sxs-lookup"><span data-stu-id="0b365-134">Stop</span></span>
- <span data-ttu-id="0b365-135">Suspensão</span><span class="sxs-lookup"><span data-stu-id="0b365-135">Suspend</span></span>

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

### <span data-ttu-id="0b365-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="0b365-136">-InformationVariable</span></span>
<span data-ttu-id="0b365-137">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="0b365-137">Specifies an information variable.</span></span>

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

### <span data-ttu-id="0b365-138">-Perfil</span><span class="sxs-lookup"><span data-stu-id="0b365-138">-Profile</span></span>
<span data-ttu-id="0b365-139">Especifica o perfil do Azure do qual este cmdlet lê.</span><span class="sxs-lookup"><span data-stu-id="0b365-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0b365-140">Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.</span><span class="sxs-lookup"><span data-stu-id="0b365-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0b365-141">-Função</span><span class="sxs-lookup"><span data-stu-id="0b365-141">-Role</span></span>
<span data-ttu-id="0b365-142">Especifica uma matriz opcional de funções para as quais especificar a configuração do Azure Diagnostics.</span><span class="sxs-lookup"><span data-stu-id="0b365-142">Specifies an optional array of roles for which to specify the Azure Diagnostics configuration.</span></span>
<span data-ttu-id="0b365-143">Se você não especificar esse parâmetro, a configuração de diagnóstico será aplicada como a configuração padrão para todas as funções.</span><span class="sxs-lookup"><span data-stu-id="0b365-143">If you do not specify this parameter, the diagnostics configuration is applied as the default configuration for all roles.</span></span>

```yaml
Type: String[]
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b365-144">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="0b365-144">-ServiceName</span></span>
<span data-ttu-id="0b365-145">Especifica o nome do serviço do Azure da implantação.</span><span class="sxs-lookup"><span data-stu-id="0b365-145">Specifies the Azure service name of the deployment.</span></span>

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

### <span data-ttu-id="0b365-146">-Slot</span><span class="sxs-lookup"><span data-stu-id="0b365-146">-Slot</span></span>
<span data-ttu-id="0b365-147">Especifica o ambiente da implantação a ser modificado.</span><span class="sxs-lookup"><span data-stu-id="0b365-147">Specifies the environment of the deployment to modify.</span></span>
<span data-ttu-id="0b365-148">Os valores aceitáveis para esse parâmetro são: produção ou preparação.</span><span class="sxs-lookup"><span data-stu-id="0b365-148">The acceptable values for this parameter are: Production or Staging.</span></span>

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

### <span data-ttu-id="0b365-149">-StorageAccountEndpoint</span><span class="sxs-lookup"><span data-stu-id="0b365-149">-StorageAccountEndpoint</span></span>
<span data-ttu-id="0b365-150">Especifica um ponto de extremidade da conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="0b365-150">Specifies a storage account endpoint.</span></span>

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b365-151">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="0b365-151">-StorageAccountKey</span></span>
<span data-ttu-id="0b365-152">Especifica uma chave de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="0b365-152">Specifies a storage account key.</span></span>

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b365-153">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0b365-153">-StorageAccountName</span></span>
<span data-ttu-id="0b365-154">Especifica um nome de conta de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="0b365-154">Specifies a storage account name.</span></span>

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b365-155">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="0b365-155">-StorageContext</span></span>
<span data-ttu-id="0b365-156">Especifica um contexto de armazenamento do Azure.</span><span class="sxs-lookup"><span data-stu-id="0b365-156">Specifies an Azure storage context.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b365-157">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="0b365-157">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="0b365-158">Especifica um algoritmo de hash de impressão digital que é usado com a impressão digital para identificar o certificado.</span><span class="sxs-lookup"><span data-stu-id="0b365-158">Specifies a thumbprint hashing algorithm that is used with the thumbprint to identify the certificate.</span></span>
<span data-ttu-id="0b365-159">Esse parâmetro é opcional, e o padrão é SHA1.</span><span class="sxs-lookup"><span data-stu-id="0b365-159">This parameter is optional and the default is sha1.</span></span>

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b365-160">-Versão</span><span class="sxs-lookup"><span data-stu-id="0b365-160">-Version</span></span>
<span data-ttu-id="0b365-161">Especifica a versão da extensão.</span><span class="sxs-lookup"><span data-stu-id="0b365-161">Specifies the version of the extension.</span></span>

```yaml
Type: String
Parameter Sets: SetExtension, SetExtensionUsingThumbprint
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b365-162">-X509Certificate</span><span class="sxs-lookup"><span data-stu-id="0b365-162">-X509Certificate</span></span>
<span data-ttu-id="0b365-163">Especifica um certificado X. 509 que, quando especificado, é carregado automaticamente para o serviço de nuvem e usado para criptografar a configuração privada de extensão.</span><span class="sxs-lookup"><span data-stu-id="0b365-163">Specifies an X.509 certificate that, when specified, is automatically uploaded to the cloud service and used for encrypting the extension private configuration.</span></span>

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

### <span data-ttu-id="0b365-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b365-164">CommonParameters</span></span>
<span data-ttu-id="0b365-165">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b365-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b365-166">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b365-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b365-167">SENSORES</span><span class="sxs-lookup"><span data-stu-id="0b365-167">INPUTS</span></span>

## <span data-ttu-id="0b365-168">EXIBE</span><span class="sxs-lookup"><span data-stu-id="0b365-168">OUTPUTS</span></span>

## <span data-ttu-id="0b365-169">INFORMA</span><span class="sxs-lookup"><span data-stu-id="0b365-169">NOTES</span></span>

## <span data-ttu-id="0b365-170">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="0b365-170">RELATED LINKS</span></span>

[<span data-ttu-id="0b365-171">Get-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="0b365-171">Get-AzureServiceDiagnosticsExtension</span></span>](./Get-AzureServiceDiagnosticsExtension.md)

[<span data-ttu-id="0b365-172">Remove-AzureServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="0b365-172">Remove-AzureServiceDiagnosticsExtension</span></span>](./Remove-AzureServiceDiagnosticsExtension.md)


