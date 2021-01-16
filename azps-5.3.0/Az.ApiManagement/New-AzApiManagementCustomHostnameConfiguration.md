---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcustomhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCustomHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCustomHostnameConfiguration.md
ms.openlocfilehash: a5c619a88f9366699f37124eab5afb2302717762
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98432653"
---
# <span data-ttu-id="47528-101">New-AzApiManagementCustomHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="47528-101">New-AzApiManagementCustomHostnameConfiguration</span></span>

## <span data-ttu-id="47528-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="47528-102">SYNOPSIS</span></span>
<span data-ttu-id="47528-103">Cria uma instância de `PsApiManagementCustomHostNameConfiguration` .</span><span class="sxs-lookup"><span data-stu-id="47528-103">Creates an instance of `PsApiManagementCustomHostNameConfiguration`.</span></span>

## <span data-ttu-id="47528-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="47528-104">SYNTAX</span></span>

### <span data-ttu-id="47528-105">NoChangeCertificate (padrão)</span><span class="sxs-lookup"><span data-stu-id="47528-105">NoChangeCertificate (Default)</span></span>
```
New-AzApiManagementCustomHostnameConfiguration -Hostname <String> -HostnameType <PsApiManagementHostnameType>
 -HostNameCertificateInformation <PsApiManagementCertificateInformation> [-DefaultSslBinding]
 [-NegotiateClientCertificate] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47528-106">SslCertificateFromFile</span><span class="sxs-lookup"><span data-stu-id="47528-106">SslCertificateFromFile</span></span>
```
New-AzApiManagementCustomHostnameConfiguration -Hostname <String> -HostnameType <PsApiManagementHostnameType>
 -PfxPath <String> [-PfxPassword <SecureString>] [-DefaultSslBinding] [-NegotiateClientCertificate]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47528-107">SslCertificateFromKeyVault</span><span class="sxs-lookup"><span data-stu-id="47528-107">SslCertificateFromKeyVault</span></span>
```
New-AzApiManagementCustomHostnameConfiguration -Hostname <String> -HostnameType <PsApiManagementHostnameType>
 -KeyVaultId <String> [-DefaultSslBinding] [-NegotiateClientCertificate]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47528-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="47528-108">DESCRIPTION</span></span>
<span data-ttu-id="47528-109">O cmdlet **New-AzApiManagementCustomHostnameConfiguration** é um comando auxiliar que cria uma instância de **PsApiManagementCustomHostNameConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="47528-109">The **New-AzApiManagementCustomHostnameConfiguration** cmdlet is a helper command that creates an instance of **PsApiManagementCustomHostNameConfiguration**.</span></span>
<span data-ttu-id="47528-110">Esse comando é usado com o cmdlet New-AzApiManagement e Set-AzApiManagement.</span><span class="sxs-lookup"><span data-stu-id="47528-110">This command is used with the New-AzApiManagement and Set-AzApiManagement cmdlet.</span></span>

## <span data-ttu-id="47528-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="47528-111">EXAMPLES</span></span>

### <span data-ttu-id="47528-112">Exemplo 1: criar e inicializar uma instância do PsApiManagementCustomHostNameConfiguration usando um certificado SSL de um arquivo</span><span class="sxs-lookup"><span data-stu-id="47528-112">Example 1: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Ssl Certificate from file</span></span>
```powershell
PS C:\>$portal = New-AzApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -PfxPath "C:\contoso\certificates\apimanagement.pfx" -PfxPassword "1111" -DefaultSslBinding
PS C:\>$customConfig = @($portal)
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -CustomHostnameConfiguration $customConfig
```

<span data-ttu-id="47528-113">Esse comando cria e Inicializa uma instância de **PsApiManagementCustomHostNameConfiguration** para o Portal.</span><span class="sxs-lookup"><span data-stu-id="47528-113">This command creates and initializes an instance of **PsApiManagementCustomHostNameConfiguration** for Portal.</span></span> <span data-ttu-id="47528-114">Em seguida, ele cria um novo serviço ApiManagement com configuração de nome de host personalizada.</span><span class="sxs-lookup"><span data-stu-id="47528-114">Then it creates a new ApiManagement service with custom hostname configuration.</span></span>

### <span data-ttu-id="47528-115">Exemplo 2: criar e inicializar uma instância do PsApiManagementCustomHostNameConfiguration usando um segredo do recurso de keyvault</span><span class="sxs-lookup"><span data-stu-id="47528-115">Example 2: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Secret from KeyVault Resource</span></span>
```powershell
PS C:\>$portal = New-AzApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/api-portal-custom-ssl.pfx"

PS C:\>$customConfig = @($portal)
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -CustomHostnameConfiguration $customConfig -SystemAssignedIdentity
```

<span data-ttu-id="47528-116">Esse comando cria e Inicializa uma instância de **PsApiManagementCustomHostNameConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="47528-116">This command creates and initializes an instance of **PsApiManagementCustomHostNameConfiguration**.</span></span>

## <span data-ttu-id="47528-117">OS</span><span class="sxs-lookup"><span data-stu-id="47528-117">PARAMETERS</span></span>

### <span data-ttu-id="47528-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47528-118">-DefaultProfile</span></span>
<span data-ttu-id="47528-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="47528-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47528-120">-DefaultSslBinding</span><span class="sxs-lookup"><span data-stu-id="47528-120">-DefaultSslBinding</span></span>
<span data-ttu-id="47528-121">Determina se o valor é um segredo e se deve ser criptografado ou não.</span><span class="sxs-lookup"><span data-stu-id="47528-121">Determines whether the value is a secret and should be encrypted or not.</span></span>
<span data-ttu-id="47528-122">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="47528-122">This parameter is optional.</span></span>
<span data-ttu-id="47528-123">O valor padrão é false.</span><span class="sxs-lookup"><span data-stu-id="47528-123">Default Value is false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47528-124">-Hostname</span><span class="sxs-lookup"><span data-stu-id="47528-124">-Hostname</span></span>
<span data-ttu-id="47528-125">Nome do host personalizado</span><span class="sxs-lookup"><span data-stu-id="47528-125">Custom Hostname</span></span>

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

### <span data-ttu-id="47528-126">-HostNameCertificateInformation</span><span class="sxs-lookup"><span data-stu-id="47528-126">-HostNameCertificateInformation</span></span>
<span data-ttu-id="47528-127">Configuração de certificado existente.</span><span class="sxs-lookup"><span data-stu-id="47528-127">Existing Certificate Configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCertificateInformation
Parameter Sets: NoChangeCertificate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47528-128">-HostNameType</span><span class="sxs-lookup"><span data-stu-id="47528-128">-HostnameType</span></span>
<span data-ttu-id="47528-129">Tipo de nome de host</span><span class="sxs-lookup"><span data-stu-id="47528-129">Hostname Type</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameType
Parameter Sets: (All)
Aliases:
Accepted values: Proxy, Portal, Management, Scm, DeveloperPortal

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47528-130">-Keyvaultid</span><span class="sxs-lookup"><span data-stu-id="47528-130">-KeyVaultId</span></span>
<span data-ttu-id="47528-131">Keyvaultid para o segredo que armazena o certificado SSL personalizado.</span><span class="sxs-lookup"><span data-stu-id="47528-131">KeyVaultId to the secret storing the Custom SSL Certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: SslCertificateFromKeyVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47528-132">-NegotiateClientCertificate</span><span class="sxs-lookup"><span data-stu-id="47528-132">-NegotiateClientCertificate</span></span>
<span data-ttu-id="47528-133">Determina se o valor é um segredo e se deve ser criptografado ou não.</span><span class="sxs-lookup"><span data-stu-id="47528-133">Determines whether the value is a secret and should be encrypted or not.</span></span>
<span data-ttu-id="47528-134">Este parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="47528-134">This parameter is optional.</span></span>
<span data-ttu-id="47528-135">O valor padrão é false.</span><span class="sxs-lookup"><span data-stu-id="47528-135">Default Value is false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47528-136">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="47528-136">-PfxPassword</span></span>
<span data-ttu-id="47528-137">Senha para o arquivo de certificado. pfx.</span><span class="sxs-lookup"><span data-stu-id="47528-137">Password for the .pfx certificate file.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: SslCertificateFromFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47528-138">-PfxPath</span><span class="sxs-lookup"><span data-stu-id="47528-138">-PfxPath</span></span>
<span data-ttu-id="47528-139">Caminho para um arquivo de certificado. pfx.</span><span class="sxs-lookup"><span data-stu-id="47528-139">Path to a .pfx certificate file.</span></span>

```yaml
Type: System.String
Parameter Sets: SslCertificateFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47528-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47528-140">CommonParameters</span></span>
<span data-ttu-id="47528-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47528-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47528-142">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="47528-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47528-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="47528-143">INPUTS</span></span>

### <span data-ttu-id="47528-144">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementCertificateInformation</span><span class="sxs-lookup"><span data-stu-id="47528-144">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCertificateInformation</span></span>

## <span data-ttu-id="47528-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="47528-145">OUTPUTS</span></span>

### <span data-ttu-id="47528-146">Microsoft. Azure. Commands. ApiManagement. Models. PsApiManagementCustomHostNameConfiguration</span><span class="sxs-lookup"><span data-stu-id="47528-146">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration</span></span>

## <span data-ttu-id="47528-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="47528-147">NOTES</span></span>

## <span data-ttu-id="47528-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="47528-148">RELATED LINKS</span></span>

[<span data-ttu-id="47528-149">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="47528-149">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="47528-150">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="47528-150">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)