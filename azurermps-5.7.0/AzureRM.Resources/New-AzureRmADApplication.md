---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: F58FD77E-2946-44B1-B410-6E983FC20E21
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADApplication.md
ms.openlocfilehash: 171f09e2d9a9e6e646731817526451b311f94482
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432409"
---
# <span data-ttu-id="083a7-101">New-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="083a7-101">New-AzureRmADApplication</span></span>

## <span data-ttu-id="083a7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="083a7-102">SYNOPSIS</span></span>
<span data-ttu-id="083a7-103">Cria um novo aplicativo Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="083a7-103">Creates a new azure active directory application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="083a7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="083a7-104">SYNTAX</span></span>

### <span data-ttu-id="083a7-105">ApplicationWithoutCredentialParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="083a7-105">ApplicationWithoutCredentialParameterSet (Default)</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="083a7-106">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="083a7-106">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="083a7-107">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="083a7-107">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="083a7-108">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="083a7-108">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="083a7-109">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="083a7-109">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="083a7-110">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="083a7-110">DESCRIPTION</span></span>
<span data-ttu-id="083a7-111">Cria um novo aplicativo Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="083a7-111">Creates a new azure active directory application.</span></span>

## <span data-ttu-id="083a7-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="083a7-112">EXAMPLES</span></span>

### <span data-ttu-id="083a7-113">Criar novo aplicativo AAD.</span><span class="sxs-lookup"><span data-stu-id="083a7-113">Create new AAD application.</span></span>
```
PS C:\> New-AzureRmADApplication -DisplayName "NewApplication" -HomePage "https://www.microsoft.com" -IdentifierUris "http://NewApplication"
```

<span data-ttu-id="083a7-114">Cria um novo aplicativo Azure Active Directory sem nenhuma credencial.</span><span class="sxs-lookup"><span data-stu-id="083a7-114">Creates a new azure active directory application without any credentials.</span></span>

### <span data-ttu-id="083a7-115">Crie um novo aplicativo AAD com senha.</span><span class="sxs-lookup"><span data-stu-id="083a7-115">Create new AAD application with password.</span></span>
```
PS E:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzureRmADApplication -DisplayName "NewApplication" -HomePage "https://www.microsoft.com" -IdentifierUris "http:
//NewApplication" -Password $SecureStringPassword
```

<span data-ttu-id="083a7-116">Cria um novo aplicativo do Azure Active Directory e associa as credenciais de senha a ele.</span><span class="sxs-lookup"><span data-stu-id="083a7-116">Creates a new azure active directory application and associates password credentials with it.</span></span>

## <span data-ttu-id="083a7-117">OS</span><span class="sxs-lookup"><span data-stu-id="083a7-117">PARAMETERS</span></span>

### <span data-ttu-id="083a7-118">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="083a7-118">-AvailableToOtherTenants</span></span>
<span data-ttu-id="083a7-119">O valor que especifica se o aplicativo é um único locatário ou um multi-locatário.</span><span class="sxs-lookup"><span data-stu-id="083a7-119">The value specifying whether the application is a single tenant or a multi-tenant.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="083a7-120">-Certvalue</span><span class="sxs-lookup"><span data-stu-id="083a7-120">-CertValue</span></span>
<span data-ttu-id="083a7-121">O valor do tipo de credencial "assimétricod".</span><span class="sxs-lookup"><span data-stu-id="083a7-121">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="083a7-122">Ele representa o certificado codificado básico do 64.</span><span class="sxs-lookup"><span data-stu-id="083a7-122">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="083a7-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="083a7-123">-DefaultProfile</span></span>
<span data-ttu-id="083a7-124">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="083a7-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="083a7-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="083a7-125">-DisplayName</span></span>
<span data-ttu-id="083a7-126">Exiba o nome do novo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="083a7-126">Display name of the new application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="083a7-127">-EndDate</span><span class="sxs-lookup"><span data-stu-id="083a7-127">-EndDate</span></span>
<span data-ttu-id="083a7-128">A data de término efetiva do uso da credencial.</span><span class="sxs-lookup"><span data-stu-id="083a7-128">The effective end date of the credential usage.</span></span>
<span data-ttu-id="083a7-129">O valor padrão de data de término é um ano a partir de hoje.</span><span class="sxs-lookup"><span data-stu-id="083a7-129">The default end date value is one year from today.</span></span> <span data-ttu-id="083a7-130">Para uma credencial de tipo "assimétrico", deve ser definida como at ou antes da data em que o certificado X509 é válido.</span><span class="sxs-lookup"><span data-stu-id="083a7-130">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="083a7-131">-Página inicial</span><span class="sxs-lookup"><span data-stu-id="083a7-131">-HomePage</span></span>
<span data-ttu-id="083a7-132">A URL para a página inicial do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="083a7-132">The URL to the application homepage.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="083a7-133">-IdentifierUris</span><span class="sxs-lookup"><span data-stu-id="083a7-133">-IdentifierUris</span></span>
<span data-ttu-id="083a7-134">Os URIs que identificam o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="083a7-134">The URIs that identify the application.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="083a7-135">-Keycredentials</span><span class="sxs-lookup"><span data-stu-id="083a7-135">-KeyCredentials</span></span>
<span data-ttu-id="083a7-136">A lista de credenciais de certificado associadas ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="083a7-136">The list of certificate credentials associated with the application.</span></span>

```yaml
Type: PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="083a7-137">-Senha</span><span class="sxs-lookup"><span data-stu-id="083a7-137">-Password</span></span>
<span data-ttu-id="083a7-138">A senha a ser associada ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="083a7-138">The password to be associated with the application.</span></span>

```yaml
Type: SecureString
Parameter Sets: ApplicationWithPasswordPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="083a7-139">-PasswordCredentials</span><span class="sxs-lookup"><span data-stu-id="083a7-139">-PasswordCredentials</span></span>
<span data-ttu-id="083a7-140">A lista de credenciais de senha associadas ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="083a7-140">The list of password credentials associated with the application.</span></span>

```yaml
Type: PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="083a7-141">-ReplyUrls</span><span class="sxs-lookup"><span data-stu-id="083a7-141">-ReplyUrls</span></span>
<span data-ttu-id="083a7-142">As URLs de resposta do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="083a7-142">The application reply urls.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="083a7-143">-StartDate</span><span class="sxs-lookup"><span data-stu-id="083a7-143">-StartDate</span></span>
<span data-ttu-id="083a7-144">A data de início efetiva do uso da credencial.</span><span class="sxs-lookup"><span data-stu-id="083a7-144">The effective start date of the credential usage.</span></span>
<span data-ttu-id="083a7-145">O valor da data de início padrão é hoje.</span><span class="sxs-lookup"><span data-stu-id="083a7-145">The default start date value is today.</span></span> <span data-ttu-id="083a7-146">Para uma credencial de tipo "assimétrico", isso deve ser definido como ligado ou posterior à data a partir da qual o certificado X509 é válido.</span><span class="sxs-lookup"><span data-stu-id="083a7-146">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="083a7-147">-Confirme</span><span class="sxs-lookup"><span data-stu-id="083a7-147">-Confirm</span></span>
<span data-ttu-id="083a7-148">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="083a7-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="083a7-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="083a7-149">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="083a7-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="083a7-150">CommonParameters</span></span>
<span data-ttu-id="083a7-151">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="083a7-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="083a7-152">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="083a7-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="083a7-153">SENSORES</span><span class="sxs-lookup"><span data-stu-id="083a7-153">INPUTS</span></span>

### <span data-ttu-id="083a7-154">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="083a7-154">None</span></span>
<span data-ttu-id="083a7-155">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="083a7-155">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="083a7-156">EXIBE</span><span class="sxs-lookup"><span data-stu-id="083a7-156">OUTPUTS</span></span>

### <span data-ttu-id="083a7-157">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="083a7-157">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="083a7-158">INFORMA</span><span class="sxs-lookup"><span data-stu-id="083a7-158">NOTES</span></span>
<span data-ttu-id="083a7-159">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, recurso, grupo, modelo, implantação</span><span class="sxs-lookup"><span data-stu-id="083a7-159">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="083a7-160">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="083a7-160">RELATED LINKS</span></span>

[<span data-ttu-id="083a7-161">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="083a7-161">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="083a7-162">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="083a7-162">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="083a7-163">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="083a7-163">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="083a7-164">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="083a7-164">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="083a7-165">New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="083a7-165">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="083a7-166">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="083a7-166">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

