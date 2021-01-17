---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: F58FD77E-2946-44B1-B410-6E983FC20E21
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADApplication.md
ms.openlocfilehash: 7ab7c679bc623a9eaa0f99bcdba1ab8281bd7d8f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427277"
---
# <span data-ttu-id="d3117-101">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="d3117-101">New-AzADApplication</span></span>

## <span data-ttu-id="d3117-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d3117-102">SYNOPSIS</span></span>
<span data-ttu-id="d3117-103">Cria um novo aplicativo Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d3117-103">Creates a new azure active directory application.</span></span>

## <span data-ttu-id="d3117-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d3117-104">SYNTAX</span></span>

### <span data-ttu-id="d3117-105">ApplicationWithoutCredentialParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="d3117-105">ApplicationWithoutCredentialParameterSet (Default)</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3117-106">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3117-106">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3117-107">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3117-107">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3117-108">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3117-108">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3117-109">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3117-109">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3117-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d3117-110">DESCRIPTION</span></span>
<span data-ttu-id="d3117-111">Cria um novo aplicativo Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d3117-111">Creates a new azure active directory application.</span></span> <span data-ttu-id="d3117-112">Veja a seguir as permissões necessárias para criar um aplicativo:</span><span class="sxs-lookup"><span data-stu-id="d3117-112">Below are the permissions needed to create an application:</span></span>

- <span data-ttu-id="d3117-113">Gráfico do Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="d3117-113">Azure Active Directory Graph</span></span>
  - <span data-ttu-id="d3117-114">Application. ReadWrite. OwnedBy</span><span class="sxs-lookup"><span data-stu-id="d3117-114">Application.ReadWrite.OwnedBy</span></span>
- <span data-ttu-id="d3117-115">Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="d3117-115">Microsoft Graph</span></span>
  - <span data-ttu-id="d3117-116">Directory. AccessAsUser. All</span><span class="sxs-lookup"><span data-stu-id="d3117-116">Directory.AccessAsUser.All</span></span>
  - <span data-ttu-id="d3117-117">Directory. ReadWrite. All</span><span class="sxs-lookup"><span data-stu-id="d3117-117">Directory.ReadWrite.All</span></span>

## <span data-ttu-id="d3117-118">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d3117-118">EXAMPLES</span></span>

### <span data-ttu-id="d3117-119">Exemplo 1: criar um novo aplicativo AAD.</span><span class="sxs-lookup"><span data-stu-id="d3117-119">Example 1: Create new AAD application.</span></span>

```powershell
PS C:\> New-AzADApplication -DisplayName "NewApplication" -HomePage "http://www.microsoft.com" -IdentifierUris "http://NewApplication"
```

<span data-ttu-id="d3117-120">Cria um novo aplicativo Azure Active Directory sem nenhuma credencial.</span><span class="sxs-lookup"><span data-stu-id="d3117-120">Creates a new azure active directory application without any credentials.</span></span>

### <span data-ttu-id="d3117-121">Exemplo 2: criar um novo aplicativo AAD com senha.</span><span class="sxs-lookup"><span data-stu-id="d3117-121">Example 2: Create new AAD application with password.</span></span>

```powershell
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzADApplication -DisplayName "NewApplication" -HomePage "http://www.microsoft.com" -IdentifierUris "http:
//NewApplication" -Password $SecureStringPassword
```

<span data-ttu-id="d3117-122">Cria um novo aplicativo do Azure Active Directory e associa as credenciais de senha a ele.</span><span class="sxs-lookup"><span data-stu-id="d3117-122">Creates a new azure active directory application and associates password credentials with it.</span></span>

## <span data-ttu-id="d3117-123">OS</span><span class="sxs-lookup"><span data-stu-id="d3117-123">PARAMETERS</span></span>

### <span data-ttu-id="d3117-124">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="d3117-124">-AvailableToOtherTenants</span></span>
<span data-ttu-id="d3117-125">O valor que especifica se o aplicativo é um único locatário ou um multi-locatário.</span><span class="sxs-lookup"><span data-stu-id="d3117-125">The value specifying whether the application is a single tenant or a multi-tenant.</span></span>

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

### <span data-ttu-id="d3117-126">-Certvalue</span><span class="sxs-lookup"><span data-stu-id="d3117-126">-CertValue</span></span>
<span data-ttu-id="d3117-127">O valor do tipo de credencial "assimétricod".</span><span class="sxs-lookup"><span data-stu-id="d3117-127">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="d3117-128">Ele representa o certificado codificado básico do 64.</span><span class="sxs-lookup"><span data-stu-id="d3117-128">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="d3117-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3117-129">-DefaultProfile</span></span>
<span data-ttu-id="d3117-130">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="d3117-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d3117-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d3117-131">-DisplayName</span></span>
<span data-ttu-id="d3117-132">Exiba o nome do novo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d3117-132">Display name of the new application.</span></span>

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

### <span data-ttu-id="d3117-133">-EndDate</span><span class="sxs-lookup"><span data-stu-id="d3117-133">-EndDate</span></span>
<span data-ttu-id="d3117-134">A data de término efetiva do uso da credencial.</span><span class="sxs-lookup"><span data-stu-id="d3117-134">The effective end date of the credential usage.</span></span>
<span data-ttu-id="d3117-135">O valor padrão de data de término é um ano a partir de hoje.</span><span class="sxs-lookup"><span data-stu-id="d3117-135">The default end date value is one year from today.</span></span> <span data-ttu-id="d3117-136">Para uma credencial de tipo "assimétrico", deve ser definida como at ou antes da data em que o certificado X509 é válido.</span><span class="sxs-lookup"><span data-stu-id="d3117-136">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="d3117-137">-Página inicial</span><span class="sxs-lookup"><span data-stu-id="d3117-137">-HomePage</span></span>
<span data-ttu-id="d3117-138">A URL para a página inicial do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d3117-138">The URL to the application homepage.</span></span>

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

### <span data-ttu-id="d3117-139">-IdentifierUris</span><span class="sxs-lookup"><span data-stu-id="d3117-139">-IdentifierUris</span></span>
<span data-ttu-id="d3117-140">Os URIs que identificam o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d3117-140">The URIs that identify the application.</span></span>

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

### <span data-ttu-id="d3117-141">-Keycredentials</span><span class="sxs-lookup"><span data-stu-id="d3117-141">-KeyCredentials</span></span>
<span data-ttu-id="d3117-142">A lista de credenciais de certificado associadas ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d3117-142">The list of certificate credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3117-143">-Senha</span><span class="sxs-lookup"><span data-stu-id="d3117-143">-Password</span></span>
<span data-ttu-id="d3117-144">A senha a ser associada ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d3117-144">The password to be associated with the application.</span></span>

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

### <span data-ttu-id="d3117-145">-PasswordCredentials</span><span class="sxs-lookup"><span data-stu-id="d3117-145">-PasswordCredentials</span></span>
<span data-ttu-id="d3117-146">A lista de credenciais de senha associadas ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d3117-146">The list of password credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3117-147">-ReplyUrls</span><span class="sxs-lookup"><span data-stu-id="d3117-147">-ReplyUrls</span></span>
<span data-ttu-id="d3117-148">As URLs de resposta do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d3117-148">The application reply urls.</span></span>

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

### <span data-ttu-id="d3117-149">-StartDate</span><span class="sxs-lookup"><span data-stu-id="d3117-149">-StartDate</span></span>
<span data-ttu-id="d3117-150">A data de início efetiva do uso da credencial.</span><span class="sxs-lookup"><span data-stu-id="d3117-150">The effective start date of the credential usage.</span></span>
<span data-ttu-id="d3117-151">O valor da data de início padrão é hoje.</span><span class="sxs-lookup"><span data-stu-id="d3117-151">The default start date value is today.</span></span> <span data-ttu-id="d3117-152">Para uma credencial de tipo "assimétrico", isso deve ser definido como ligado ou posterior à data a partir da qual o certificado X509 é válido.</span><span class="sxs-lookup"><span data-stu-id="d3117-152">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="d3117-153">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d3117-153">-Confirm</span></span>
<span data-ttu-id="d3117-154">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3117-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3117-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3117-155">-WhatIf</span></span>
<span data-ttu-id="d3117-156">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d3117-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3117-157">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d3117-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3117-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3117-158">CommonParameters</span></span>
<span data-ttu-id="d3117-159">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3117-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3117-160">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d3117-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3117-161">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d3117-161">INPUTS</span></span>

### <span data-ttu-id="d3117-162">System. String</span><span class="sxs-lookup"><span data-stu-id="d3117-162">System.String</span></span>

### <span data-ttu-id="d3117-163">System. String []</span><span class="sxs-lookup"><span data-stu-id="d3117-163">System.String[]</span></span>

### <span data-ttu-id="d3117-164">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d3117-164">System.Boolean</span></span>

### <span data-ttu-id="d3117-165">Microsoft. Azure. Commands. ActiveDirectory. PSADPasswordCredential []</span><span class="sxs-lookup"><span data-stu-id="d3117-165">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="d3117-166">Microsoft. Azure. Commands. ActiveDirectory. PSADKeyCredential []</span><span class="sxs-lookup"><span data-stu-id="d3117-166">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="d3117-167">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="d3117-167">System.Security.SecureString</span></span>

### <span data-ttu-id="d3117-168">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="d3117-168">System.DateTime</span></span>

## <span data-ttu-id="d3117-169">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d3117-169">OUTPUTS</span></span>

### <span data-ttu-id="d3117-170">Microsoft. Azure. Commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="d3117-170">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="d3117-171">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d3117-171">NOTES</span></span>
<span data-ttu-id="d3117-172">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, recurso, grupo, modelo, implantação</span><span class="sxs-lookup"><span data-stu-id="d3117-172">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="d3117-173">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d3117-173">RELATED LINKS</span></span>

[<span data-ttu-id="d3117-174">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="d3117-174">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="d3117-175">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="d3117-175">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="d3117-176">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="d3117-176">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)

[<span data-ttu-id="d3117-177">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="d3117-177">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="d3117-178">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="d3117-178">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="d3117-179">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="d3117-179">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

