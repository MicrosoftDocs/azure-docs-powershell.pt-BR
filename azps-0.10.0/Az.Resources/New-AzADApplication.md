---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: F58FD77E-2946-44B1-B410-6E983FC20E21
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzADApplication.md
ms.openlocfilehash: 3850e5f142e7ec1496ace1225ab53c160794775a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776413"
---
# <span data-ttu-id="c2ce5-101">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="c2ce5-101">New-AzADApplication</span></span>

## <span data-ttu-id="c2ce5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c2ce5-102">SYNOPSIS</span></span>
<span data-ttu-id="c2ce5-103">Cria um novo aplicativo Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c2ce5-103">Creates a new azure active directory application.</span></span>

## <span data-ttu-id="c2ce5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c2ce5-104">SYNTAX</span></span>

### <span data-ttu-id="c2ce5-105">ApplicationWithoutCredentialParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="c2ce5-105">ApplicationWithoutCredentialParameterSet (Default)</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2ce5-106">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2ce5-106">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2ce5-107">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2ce5-107">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2ce5-108">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2ce5-108">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2ce5-109">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2ce5-109">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2ce5-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c2ce5-110">DESCRIPTION</span></span>
<span data-ttu-id="c2ce5-111">Cria um novo aplicativo Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c2ce5-111">Creates a new azure active directory application.</span></span>

## <span data-ttu-id="c2ce5-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c2ce5-112">EXAMPLES</span></span>

### <span data-ttu-id="c2ce5-113">Exemplo 1-criar novo aplicativo AAD.</span><span class="sxs-lookup"><span data-stu-id="c2ce5-113">Example 1 - Create new AAD application.</span></span>

```
PS C:\> New-AzADApplication -DisplayName "NewApplication" -HomePage "http://www.microsoft.com" -IdentifierUris "http://NewApplication"
```

<span data-ttu-id="c2ce5-114">Cria um novo aplicativo Azure Active Directory sem nenhuma credencial.</span><span class="sxs-lookup"><span data-stu-id="c2ce5-114">Creates a new azure active directory application without any credentials.</span></span>

### <span data-ttu-id="c2ce5-115">Exemplo 2-crie um novo aplicativo AAD com senha.</span><span class="sxs-lookup"><span data-stu-id="c2ce5-115">Example 2 - Create new AAD application with password.</span></span>

```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzADApplication -DisplayName "NewApplication" -HomePage "http://www.microsoft.com" -IdentifierUris "http:
//NewApplication" -Password $SecureStringPassword
```

<span data-ttu-id="c2ce5-116">Cria um novo aplicativo do Azure Active Directory e associa as credenciais de senha a ele.</span><span class="sxs-lookup"><span data-stu-id="c2ce5-116">Creates a new azure active directory application and associates password credentials with it.</span></span>

## <span data-ttu-id="c2ce5-117">OS</span><span class="sxs-lookup"><span data-stu-id="c2ce5-117">PARAMETERS</span></span>

### <span data-ttu-id="c2ce5-118">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="c2ce5-118">-AvailableToOtherTenants</span></span>
<span data-ttu-id="c2ce5-119">O valor que especifica se o aplicativo é um único locatário ou um multi-locatário.</span><span class="sxs-lookup"><span data-stu-id="c2ce5-119">The value specifying whether the application is a single tenant or a multi-tenant.</span></span>

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

### <span data-ttu-id="c2ce5-120">-Certvalue</span><span class="sxs-lookup"><span data-stu-id="c2ce5-120">-CertValue</span></span>
<span data-ttu-id="c2ce5-121">O valor do tipo de credencial "assimétricod".</span><span class="sxs-lookup"><span data-stu-id="c2ce5-121">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="c2ce5-122">Ele representa o certificado codificado básico do 64.</span><span class="sxs-lookup"><span data-stu-id="c2ce5-122">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="c2ce5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2ce5-123">-DefaultProfile</span></span>
<span data-ttu-id="c2ce5-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="c2ce5-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2ce5-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c2ce5-125">-DisplayName</span></span>
<span data-ttu-id="c2ce5-126">Exiba o nome do novo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c2ce5-126">Display name of the new application.</span></span>

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

### <span data-ttu-id="c2ce5-127">-EndDate</span><span class="sxs-lookup"><span data-stu-id="c2ce5-127">-EndDate</span></span>
<span data-ttu-id="c2ce5-128">A data de término efetiva do uso da credencial.</span><span class="sxs-lookup"><span data-stu-id="c2ce5-128">The effective end date of the credential usage.</span></span>
<span data-ttu-id="c2ce5-129">O valor padrão de data de término é um ano a partir de hoje.</span><span class="sxs-lookup"><span data-stu-id="c2ce5-129">The default end date value is one year from today.</span></span> <span data-ttu-id="c2ce5-130">Para uma credencial de tipo "assimétrico", deve ser definida como at ou antes da data em que o certificado X509 é válido.</span><span class="sxs-lookup"><span data-stu-id="c2ce5-130">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="c2ce5-131">-Página inicial</span><span class="sxs-lookup"><span data-stu-id="c2ce5-131">-HomePage</span></span>
<span data-ttu-id="c2ce5-132">A URL para a página inicial do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c2ce5-132">The URL to the application homepage.</span></span>

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

### <span data-ttu-id="c2ce5-133">-IdentifierUris</span><span class="sxs-lookup"><span data-stu-id="c2ce5-133">-IdentifierUris</span></span>
<span data-ttu-id="c2ce5-134">Os URIs que identificam o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c2ce5-134">The URIs that identify the application.</span></span>

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

### <span data-ttu-id="c2ce5-135">-Keycredentials</span><span class="sxs-lookup"><span data-stu-id="c2ce5-135">-KeyCredentials</span></span>
<span data-ttu-id="c2ce5-136">A lista de credenciais de certificado associadas ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c2ce5-136">The list of certificate credentials associated with the application.</span></span>

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

### <span data-ttu-id="c2ce5-137">-Senha</span><span class="sxs-lookup"><span data-stu-id="c2ce5-137">-Password</span></span>
<span data-ttu-id="c2ce5-138">A senha a ser associada ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c2ce5-138">The password to be associated with the application.</span></span>

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

### <span data-ttu-id="c2ce5-139">-PasswordCredentials</span><span class="sxs-lookup"><span data-stu-id="c2ce5-139">-PasswordCredentials</span></span>
<span data-ttu-id="c2ce5-140">A lista de credenciais de senha associadas ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c2ce5-140">The list of password credentials associated with the application.</span></span>

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

### <span data-ttu-id="c2ce5-141">-ReplyUrls</span><span class="sxs-lookup"><span data-stu-id="c2ce5-141">-ReplyUrls</span></span>
<span data-ttu-id="c2ce5-142">As URLs de resposta do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c2ce5-142">The application reply urls.</span></span>

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

### <span data-ttu-id="c2ce5-143">-StartDate</span><span class="sxs-lookup"><span data-stu-id="c2ce5-143">-StartDate</span></span>
<span data-ttu-id="c2ce5-144">A data de início efetiva do uso da credencial.</span><span class="sxs-lookup"><span data-stu-id="c2ce5-144">The effective start date of the credential usage.</span></span>
<span data-ttu-id="c2ce5-145">O valor da data de início padrão é hoje.</span><span class="sxs-lookup"><span data-stu-id="c2ce5-145">The default start date value is today.</span></span> <span data-ttu-id="c2ce5-146">Para uma credencial de tipo "assimétrico", isso deve ser definido como ligado ou posterior à data a partir da qual o certificado X509 é válido.</span><span class="sxs-lookup"><span data-stu-id="c2ce5-146">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="c2ce5-147">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c2ce5-147">-Confirm</span></span>
<span data-ttu-id="c2ce5-148">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2ce5-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2ce5-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2ce5-149">-WhatIf</span></span>
<span data-ttu-id="c2ce5-150">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c2ce5-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2ce5-151">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c2ce5-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2ce5-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2ce5-152">CommonParameters</span></span>
<span data-ttu-id="c2ce5-153">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2ce5-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2ce5-154">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2ce5-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2ce5-155">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c2ce5-155">INPUTS</span></span>

### <span data-ttu-id="c2ce5-156">System. String</span><span class="sxs-lookup"><span data-stu-id="c2ce5-156">System.String</span></span>

### <span data-ttu-id="c2ce5-157">System. String []</span><span class="sxs-lookup"><span data-stu-id="c2ce5-157">System.String[]</span></span>

### <span data-ttu-id="c2ce5-158">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c2ce5-158">System.Boolean</span></span>

### <span data-ttu-id="c2ce5-159">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADPasswordCredential []</span><span class="sxs-lookup"><span data-stu-id="c2ce5-159">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="c2ce5-160">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADKeyCredential []</span><span class="sxs-lookup"><span data-stu-id="c2ce5-160">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="c2ce5-161">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="c2ce5-161">System.Security.SecureString</span></span>

### <span data-ttu-id="c2ce5-162">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="c2ce5-162">System.DateTime</span></span>

## <span data-ttu-id="c2ce5-163">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c2ce5-163">OUTPUTS</span></span>

### <span data-ttu-id="c2ce5-164">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="c2ce5-164">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="c2ce5-165">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c2ce5-165">NOTES</span></span>
<span data-ttu-id="c2ce5-166">Palavras-chave: Azure, AZ, braço, recurso, gerenciamento, gerente, recurso, grupo, modelo, implantação</span><span class="sxs-lookup"><span data-stu-id="c2ce5-166">Keywords: azure, Az, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="c2ce5-167">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c2ce5-167">RELATED LINKS</span></span>

[<span data-ttu-id="c2ce5-168">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="c2ce5-168">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="c2ce5-169">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="c2ce5-169">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="c2ce5-170">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c2ce5-170">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)

[<span data-ttu-id="c2ce5-171">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="c2ce5-171">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="c2ce5-172">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="c2ce5-172">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="c2ce5-173">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="c2ce5-173">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

