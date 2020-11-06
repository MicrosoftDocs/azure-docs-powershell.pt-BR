---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: F58FD77E-2946-44B1-B410-6E983FC20E21
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADApplication.md
ms.openlocfilehash: e23e3db6cb574fb16b2c559c948372c808840de1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430043"
---
# <span data-ttu-id="97a88-101">New-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="97a88-101">New-AzureRmADApplication</span></span>

## <span data-ttu-id="97a88-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="97a88-102">SYNOPSIS</span></span>
<span data-ttu-id="97a88-103">Cria um novo aplicativo Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="97a88-103">Creates a new azure active directory application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97a88-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="97a88-104">SYNTAX</span></span>

### <span data-ttu-id="97a88-105">ApplicationWithoutCredentialParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="97a88-105">ApplicationWithoutCredentialParameterSet (Default)</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97a88-106">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="97a88-106">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97a88-107">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="97a88-107">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97a88-108">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="97a88-108">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97a88-109">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="97a88-109">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97a88-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="97a88-110">DESCRIPTION</span></span>
<span data-ttu-id="97a88-111">Cria um novo aplicativo Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="97a88-111">Creates a new azure active directory application.</span></span>

## <span data-ttu-id="97a88-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="97a88-112">EXAMPLES</span></span>

### <span data-ttu-id="97a88-113">Exemplo 1-criar novo aplicativo AAD.</span><span class="sxs-lookup"><span data-stu-id="97a88-113">Example 1 - Create new AAD application.</span></span>

```
PS C:\> New-AzureRmADApplication -DisplayName "NewApplication" -HomePage "https://www.microsoft.com" -IdentifierUris "http://NewApplication"
```

<span data-ttu-id="97a88-114">Cria um novo aplicativo Azure Active Directory sem nenhuma credencial.</span><span class="sxs-lookup"><span data-stu-id="97a88-114">Creates a new azure active directory application without any credentials.</span></span>

### <span data-ttu-id="97a88-115">Exemplo 2-crie um novo aplicativo AAD com senha.</span><span class="sxs-lookup"><span data-stu-id="97a88-115">Example 2 - Create new AAD application with password.</span></span>

```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzureRmADApplication -DisplayName "NewApplication" -HomePage "https://www.microsoft.com" -IdentifierUris "http:
//NewApplication" -Password $SecureStringPassword
```

<span data-ttu-id="97a88-116">Cria um novo aplicativo do Azure Active Directory e associa as credenciais de senha a ele.</span><span class="sxs-lookup"><span data-stu-id="97a88-116">Creates a new azure active directory application and associates password credentials with it.</span></span>

## <span data-ttu-id="97a88-117">OS</span><span class="sxs-lookup"><span data-stu-id="97a88-117">PARAMETERS</span></span>

### <span data-ttu-id="97a88-118">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="97a88-118">-AvailableToOtherTenants</span></span>
<span data-ttu-id="97a88-119">O valor que especifica se o aplicativo é um único locatário ou um multi-locatário.</span><span class="sxs-lookup"><span data-stu-id="97a88-119">The value specifying whether the application is a single tenant or a multi-tenant.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97a88-120">-Certvalue</span><span class="sxs-lookup"><span data-stu-id="97a88-120">-CertValue</span></span>
<span data-ttu-id="97a88-121">O valor do tipo de credencial "assimétricod".</span><span class="sxs-lookup"><span data-stu-id="97a88-121">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="97a88-122">Ele representa o certificado codificado básico do 64.</span><span class="sxs-lookup"><span data-stu-id="97a88-122">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97a88-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97a88-123">-DefaultProfile</span></span>
<span data-ttu-id="97a88-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="97a88-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97a88-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="97a88-125">-DisplayName</span></span>
<span data-ttu-id="97a88-126">Exiba o nome do novo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="97a88-126">Display name of the new application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97a88-127">-EndDate</span><span class="sxs-lookup"><span data-stu-id="97a88-127">-EndDate</span></span>
<span data-ttu-id="97a88-128">A data de término efetiva do uso da credencial.</span><span class="sxs-lookup"><span data-stu-id="97a88-128">The effective end date of the credential usage.</span></span>
<span data-ttu-id="97a88-129">O valor padrão de data de término é um ano a partir de hoje.</span><span class="sxs-lookup"><span data-stu-id="97a88-129">The default end date value is one year from today.</span></span> <span data-ttu-id="97a88-130">Para uma credencial de tipo "assimétrico", deve ser definida como at ou antes da data em que o certificado X509 é válido.</span><span class="sxs-lookup"><span data-stu-id="97a88-130">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97a88-131">-Página inicial</span><span class="sxs-lookup"><span data-stu-id="97a88-131">-HomePage</span></span>
<span data-ttu-id="97a88-132">A URL para a página inicial do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="97a88-132">The URL to the application homepage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97a88-133">-IdentifierUris</span><span class="sxs-lookup"><span data-stu-id="97a88-133">-IdentifierUris</span></span>
<span data-ttu-id="97a88-134">Os URIs que identificam o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="97a88-134">The URIs that identify the application.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97a88-135">-Keycredentials</span><span class="sxs-lookup"><span data-stu-id="97a88-135">-KeyCredentials</span></span>
<span data-ttu-id="97a88-136">A lista de credenciais de certificado associadas ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="97a88-136">The list of certificate credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97a88-137">-Senha</span><span class="sxs-lookup"><span data-stu-id="97a88-137">-Password</span></span>
<span data-ttu-id="97a88-138">A senha a ser associada ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="97a88-138">The password to be associated with the application.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ApplicationWithPasswordPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97a88-139">-PasswordCredentials</span><span class="sxs-lookup"><span data-stu-id="97a88-139">-PasswordCredentials</span></span>
<span data-ttu-id="97a88-140">A lista de credenciais de senha associadas ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="97a88-140">The list of password credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97a88-141">-ReplyUrls</span><span class="sxs-lookup"><span data-stu-id="97a88-141">-ReplyUrls</span></span>
<span data-ttu-id="97a88-142">As URLs de resposta do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="97a88-142">The application reply urls.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97a88-143">-StartDate</span><span class="sxs-lookup"><span data-stu-id="97a88-143">-StartDate</span></span>
<span data-ttu-id="97a88-144">A data de início efetiva do uso da credencial.</span><span class="sxs-lookup"><span data-stu-id="97a88-144">The effective start date of the credential usage.</span></span>
<span data-ttu-id="97a88-145">O valor da data de início padrão é hoje.</span><span class="sxs-lookup"><span data-stu-id="97a88-145">The default start date value is today.</span></span> <span data-ttu-id="97a88-146">Para uma credencial de tipo "assimétrico", isso deve ser definido como ligado ou posterior à data a partir da qual o certificado X509 é válido.</span><span class="sxs-lookup"><span data-stu-id="97a88-146">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97a88-147">-Confirme</span><span class="sxs-lookup"><span data-stu-id="97a88-147">-Confirm</span></span>
<span data-ttu-id="97a88-148">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97a88-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97a88-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97a88-149">-WhatIf</span></span>
<span data-ttu-id="97a88-150">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="97a88-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97a88-151">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="97a88-151">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97a88-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97a88-152">CommonParameters</span></span>
<span data-ttu-id="97a88-153">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97a88-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97a88-154">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97a88-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97a88-155">SENSORES</span><span class="sxs-lookup"><span data-stu-id="97a88-155">INPUTS</span></span>

### <span data-ttu-id="97a88-156">System. String</span><span class="sxs-lookup"><span data-stu-id="97a88-156">System.String</span></span>

### <span data-ttu-id="97a88-157">System. String []</span><span class="sxs-lookup"><span data-stu-id="97a88-157">System.String[]</span></span>

### <span data-ttu-id="97a88-158">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="97a88-158">System.Boolean</span></span>

### <span data-ttu-id="97a88-159">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADPasswordCredential []</span><span class="sxs-lookup"><span data-stu-id="97a88-159">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="97a88-160">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADKeyCredential []</span><span class="sxs-lookup"><span data-stu-id="97a88-160">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="97a88-161">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="97a88-161">System.Security.SecureString</span></span>

### <span data-ttu-id="97a88-162">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="97a88-162">System.DateTime</span></span>

## <span data-ttu-id="97a88-163">EXIBE</span><span class="sxs-lookup"><span data-stu-id="97a88-163">OUTPUTS</span></span>

### <span data-ttu-id="97a88-164">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="97a88-164">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="97a88-165">INFORMA</span><span class="sxs-lookup"><span data-stu-id="97a88-165">NOTES</span></span>
<span data-ttu-id="97a88-166">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, recurso, grupo, modelo, implantação</span><span class="sxs-lookup"><span data-stu-id="97a88-166">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="97a88-167">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="97a88-167">RELATED LINKS</span></span>

[<span data-ttu-id="97a88-168">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="97a88-168">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="97a88-169">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="97a88-169">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="97a88-170">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="97a88-170">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="97a88-171">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="97a88-171">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="97a88-172">New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="97a88-172">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="97a88-173">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="97a88-173">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

