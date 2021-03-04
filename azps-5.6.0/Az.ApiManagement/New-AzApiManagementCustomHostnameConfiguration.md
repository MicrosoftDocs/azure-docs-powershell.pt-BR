---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementcustomhostnameconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCustomHostnameConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCustomHostnameConfiguration.md
ms.openlocfilehash: e2f7ca5ac27faa3730742f77495b6b21ac084553
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885504"
---
# <span data-ttu-id="ef425-101">New-AzApiManagementCustomHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="ef425-101">New-AzApiManagementCustomHostnameConfiguration</span></span>

## <span data-ttu-id="ef425-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef425-102">SYNOPSIS</span></span>
<span data-ttu-id="ef425-103">Cria uma instância de `PsApiManagementCustomHostNameConfiguration` .</span><span class="sxs-lookup"><span data-stu-id="ef425-103">Creates an instance of `PsApiManagementCustomHostNameConfiguration`.</span></span>

## <span data-ttu-id="ef425-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ef425-104">SYNTAX</span></span>

### <span data-ttu-id="ef425-105">NoChangeCertificate (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ef425-105">NoChangeCertificate (Default)</span></span>
```
New-AzApiManagementCustomHostnameConfiguration -Hostname <String> -HostnameType <PsApiManagementHostnameType>
 -HostNameCertificateInformation <PsApiManagementCertificateInformation> [-DefaultSslBinding]
 [-NegotiateClientCertificate] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef425-106">SslCertificateFromFile</span><span class="sxs-lookup"><span data-stu-id="ef425-106">SslCertificateFromFile</span></span>
```
New-AzApiManagementCustomHostnameConfiguration -Hostname <String> -HostnameType <PsApiManagementHostnameType>
 -PfxPath <String> [-PfxPassword <SecureString>] [-DefaultSslBinding] [-NegotiateClientCertificate]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef425-107">SslCertificateFromKeyVault</span><span class="sxs-lookup"><span data-stu-id="ef425-107">SslCertificateFromKeyVault</span></span>
```
New-AzApiManagementCustomHostnameConfiguration -Hostname <String> -HostnameType <PsApiManagementHostnameType>
 -KeyVaultId <String> [-DefaultSslBinding] [-NegotiateClientCertificate]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef425-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ef425-108">DESCRIPTION</span></span>
<span data-ttu-id="ef425-109">O cmdlet **New-AzApiManagementCustomHostnameConfiguration** é um comando auxiliar que cria uma instância de **PsApiManagementCustomHostNameConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="ef425-109">The **New-AzApiManagementCustomHostnameConfiguration** cmdlet is a helper command that creates an instance of **PsApiManagementCustomHostNameConfiguration**.</span></span>
<span data-ttu-id="ef425-110">Esse comando é usado com o New-AzApiManagement e Set-AzApiManagement cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef425-110">This command is used with the New-AzApiManagement and Set-AzApiManagement cmdlet.</span></span>

## <span data-ttu-id="ef425-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ef425-111">EXAMPLES</span></span>

### <span data-ttu-id="ef425-112">Exemplo 1: Criar e inicializar uma instância de PsApiManagementCustomHostNameConfiguration usando um Certificado Ssl do arquivo</span><span class="sxs-lookup"><span data-stu-id="ef425-112">Example 1: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Ssl Certificate from file</span></span>
```powershell
PS C:\>$portal = New-AzApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -PfxPath "C:\contoso\certificates\apimanagement.pfx" -PfxPassword "1111" -DefaultSslBinding
PS C:\>$customConfig = @($portal)
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -CustomHostnameConfiguration $customConfig
```

<span data-ttu-id="ef425-113">Este comando cria e inicializa uma instância **de PsApiManagementCustomHostNameConfiguration** para Portal.</span><span class="sxs-lookup"><span data-stu-id="ef425-113">This command creates and initializes an instance of **PsApiManagementCustomHostNameConfiguration** for Portal.</span></span> <span data-ttu-id="ef425-114">Em seguida, ele cria um novo serviço ApiManagement com configuração de nome de host personalizada.</span><span class="sxs-lookup"><span data-stu-id="ef425-114">Then it creates a new ApiManagement service with custom hostname configuration.</span></span>

### <span data-ttu-id="ef425-115">Exemplo 2: Criar e inicializar uma instância de PsApiManagementCustomHostNameConfiguration usando um Segredo do Recurso KeyVault</span><span class="sxs-lookup"><span data-stu-id="ef425-115">Example 2: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Secret from KeyVault Resource</span></span>
```powershell
PS C:\>$portal = New-AzApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/api-portal-custom-ssl.pfx"

PS C:\>$customConfig = @($portal)
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -CustomHostnameConfiguration $customConfig -SystemAssignedIdentity
```

<span data-ttu-id="ef425-116">Este comando cria e inicializa uma instância de **PsApiManagementCustomHostNameConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="ef425-116">This command creates and initializes an instance of **PsApiManagementCustomHostNameConfiguration**.</span></span>

## <span data-ttu-id="ef425-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ef425-117">PARAMETERS</span></span>

### <span data-ttu-id="ef425-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef425-118">-DefaultProfile</span></span>
<span data-ttu-id="ef425-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ef425-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef425-120">-DefaultSslBinding</span><span class="sxs-lookup"><span data-stu-id="ef425-120">-DefaultSslBinding</span></span>
<span data-ttu-id="ef425-121">Determina se o valor é um segredo e deve ser criptografado ou não.</span><span class="sxs-lookup"><span data-stu-id="ef425-121">Determines whether the value is a secret and should be encrypted or not.</span></span>
<span data-ttu-id="ef425-122">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="ef425-122">This parameter is optional.</span></span>
<span data-ttu-id="ef425-123">Valor padrão é false.</span><span class="sxs-lookup"><span data-stu-id="ef425-123">Default Value is false.</span></span>

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

### <span data-ttu-id="ef425-124">-Hostname</span><span class="sxs-lookup"><span data-stu-id="ef425-124">-Hostname</span></span>
<span data-ttu-id="ef425-125">Hostname personalizado</span><span class="sxs-lookup"><span data-stu-id="ef425-125">Custom Hostname</span></span>

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

### <span data-ttu-id="ef425-126">-HostNameCertificateInformation</span><span class="sxs-lookup"><span data-stu-id="ef425-126">-HostNameCertificateInformation</span></span>
<span data-ttu-id="ef425-127">Configuração de certificado existente.</span><span class="sxs-lookup"><span data-stu-id="ef425-127">Existing Certificate Configuration.</span></span>

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

### <span data-ttu-id="ef425-128">-HostnameType</span><span class="sxs-lookup"><span data-stu-id="ef425-128">-HostnameType</span></span>
<span data-ttu-id="ef425-129">Tipo hostname</span><span class="sxs-lookup"><span data-stu-id="ef425-129">Hostname Type</span></span>

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

### <span data-ttu-id="ef425-130">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="ef425-130">-KeyVaultId</span></span>
<span data-ttu-id="ef425-131">KeyVaultId para o armazenamento secreto do Certificado SSL Personalizado.</span><span class="sxs-lookup"><span data-stu-id="ef425-131">KeyVaultId to the secret storing the Custom SSL Certificate.</span></span>

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

### <span data-ttu-id="ef425-132">-NegotiateClientCertificate</span><span class="sxs-lookup"><span data-stu-id="ef425-132">-NegotiateClientCertificate</span></span>
<span data-ttu-id="ef425-133">Determina se o valor é um segredo e deve ser criptografado ou não.</span><span class="sxs-lookup"><span data-stu-id="ef425-133">Determines whether the value is a secret and should be encrypted or not.</span></span>
<span data-ttu-id="ef425-134">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="ef425-134">This parameter is optional.</span></span>
<span data-ttu-id="ef425-135">Valor padrão é false.</span><span class="sxs-lookup"><span data-stu-id="ef425-135">Default Value is false.</span></span>

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

### <span data-ttu-id="ef425-136">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="ef425-136">-PfxPassword</span></span>
<span data-ttu-id="ef425-137">Senha para o arquivo de certificado .pfx.</span><span class="sxs-lookup"><span data-stu-id="ef425-137">Password for the .pfx certificate file.</span></span>

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

### <span data-ttu-id="ef425-138">-PfxPath</span><span class="sxs-lookup"><span data-stu-id="ef425-138">-PfxPath</span></span>
<span data-ttu-id="ef425-139">Caminho para um arquivo de certificado .pfx.</span><span class="sxs-lookup"><span data-stu-id="ef425-139">Path to a .pfx certificate file.</span></span>

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

### <span data-ttu-id="ef425-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef425-140">CommonParameters</span></span>
<span data-ttu-id="ef425-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef425-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef425-142">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ef425-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef425-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ef425-143">INPUTS</span></span>

### <span data-ttu-id="ef425-144">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCertificateInformation</span><span class="sxs-lookup"><span data-stu-id="ef425-144">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCertificateInformation</span></span>

## <span data-ttu-id="ef425-145">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ef425-145">OUTPUTS</span></span>

### <span data-ttu-id="ef425-146">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration</span><span class="sxs-lookup"><span data-stu-id="ef425-146">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration</span></span>

## <span data-ttu-id="ef425-147">NOTES</span><span class="sxs-lookup"><span data-stu-id="ef425-147">NOTES</span></span>

## <span data-ttu-id="ef425-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ef425-148">RELATED LINKS</span></span>

[<span data-ttu-id="ef425-149">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="ef425-149">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="ef425-150">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="ef425-150">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)