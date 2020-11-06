---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 98836BC0-AB4F-4F24-88BE-E7DD350B71E8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADAppCredential.md
ms.openlocfilehash: 37354a29a0ec6b8994ef05d7bf8859be249e6e88
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430044"
---
# <span data-ttu-id="ee26c-101">New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="ee26c-101">New-AzureRmADAppCredential</span></span>

## <span data-ttu-id="ee26c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ee26c-102">SYNOPSIS</span></span>
<span data-ttu-id="ee26c-103">Adiciona uma credencial a um aplicativo existente.</span><span class="sxs-lookup"><span data-stu-id="ee26c-103">Adds a credential to an existing application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ee26c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ee26c-104">SYNTAX</span></span>

### <span data-ttu-id="ee26c-105">ApplicationObjectIdWithPasswordParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="ee26c-105">ApplicationObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzureRmADAppCredential -ObjectId <Guid> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee26c-106">ApplicationObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee26c-106">ApplicationObjectIdWithCertValueParameterSet</span></span>
```
New-AzureRmADAppCredential -ObjectId <Guid> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee26c-107">ApplicationIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee26c-107">ApplicationIdWithCertValueParameterSet</span></span>
```
New-AzureRmADAppCredential -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee26c-108">ApplicationIdWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee26c-108">ApplicationIdWithPasswordParameterSet</span></span>
```
New-AzureRmADAppCredential -ApplicationId <Guid> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee26c-109">DisplayNameWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee26c-109">DisplayNameWithPasswordParameterSet</span></span>
```
New-AzureRmADAppCredential -DisplayName <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee26c-110">DisplayNameWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee26c-110">DisplayNameWithCertValueParameterSet</span></span>
```
New-AzureRmADAppCredential -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee26c-111">ApplicationObjectWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee26c-111">ApplicationObjectWithCertValueParameterSet</span></span>
```
New-AzureRmADAppCredential -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee26c-112">ApplicationObjectWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee26c-112">ApplicationObjectWithPasswordParameterSet</span></span>
```
New-AzureRmADAppCredential -ApplicationObject <PSADApplication> -Password <SecureString>
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ee26c-113">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ee26c-113">DESCRIPTION</span></span>
<span data-ttu-id="ee26c-114">O cmdlet New-AzureRmADAppCredential pode ser usado para adicionar uma nova credencial ou para rolar credenciais para um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ee26c-114">The New-AzureRmADAppCredential cmdlet can be used to add a new credential or to roll credentials for an application.</span></span>
<span data-ttu-id="ee26c-115">O aplicativo é identificado fornecendo a identificação do objeto do aplicativo ou a ID do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ee26c-115">The application is identified by supplying either the application object id or application Id.</span></span>

## <span data-ttu-id="ee26c-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ee26c-116">EXAMPLES</span></span>

### <span data-ttu-id="ee26c-117">Exemplo 1-criar uma nova credencial de aplicativo usando uma senha</span><span class="sxs-lookup"><span data-stu-id="ee26c-117">Example 1 - Create a new application credential using a password</span></span>

```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzureRmADAppCredential -ObjectId 1f89cf81-0146-4f4e-beae-2007d0668416 -Password $SecureStringPassword
```

<span data-ttu-id="ee26c-118">Uma nova credencial de senha é adicionada ao appplication existente com a ID de objeto ' 1f89cf81-0146-4f4e-BEAE-2007d0668416 '.</span><span class="sxs-lookup"><span data-stu-id="ee26c-118">A new password credential is added to the existing appplication with object id '1f89cf81-0146-4f4e-beae-2007d0668416'.</span></span>

### <span data-ttu-id="ee26c-119">Exemplo 2-criar uma nova credencial de aplicativo usando um certificado</span><span class="sxs-lookup"><span data-stu-id="ee26c-119">Example 2 - Create a new application credential using a certificate</span></span>

```
PS C:\> $cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate 
PS C:\> $cer.Import("C:\myapp.cer") 
PS C:\> $binCert = $cer.GetRawCertData() 
PS C:\> $credValue = [System.Convert]::ToBase64String($binCert)
PS C:\> New-AzureRmADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 -CertValue $credValue -StartDate $cer.GetEffectiveDateString() -EndDate $cer.GetExpirationDateString()
```

<span data-ttu-id="ee26c-120">O certificado X509 público codificado em base64 fornecido ("MyApp. cer") é adicionado ao aplicativo existente com a ID de aplicativo ' 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 '.</span><span class="sxs-lookup"><span data-stu-id="ee26c-120">The supplied base64 encoded public X509 certificate ("myapp.cer") is added to the existing application with application id '4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58'.</span></span>

### <span data-ttu-id="ee26c-121">Exemplo 3-criar uma nova credencial de aplicativo usando o encanamento</span><span class="sxs-lookup"><span data-stu-id="ee26c-121">Example 3 - Create a new application credential using piping</span></span>

```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> Get-AzureRmADApplication -ObjectId 1f89cf81-0146-4f4e-beae-2007d0668416 | New-AzureRmADAppCredential -Password $SecureStringPassword
```

<span data-ttu-id="ee26c-122">Obtém o aplicativo com a ID de objeto ' 1f89cf81-0146-4f4e-BEAE-2007d0668416 ' e canaliza o New-AzureRmADAppCredential para criar uma nova credencial de aplicativo para esse aplicativo com a senha fornecida.</span><span class="sxs-lookup"><span data-stu-id="ee26c-122">Gets the application with object id '1f89cf81-0146-4f4e-beae-2007d0668416' and pipes that to the New-AzureRmADAppCredential to create a new application credential for that application with the given password.</span></span>

## <span data-ttu-id="ee26c-123">OS</span><span class="sxs-lookup"><span data-stu-id="ee26c-123">PARAMETERS</span></span>

### <span data-ttu-id="ee26c-124">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="ee26c-124">-ApplicationId</span></span>
<span data-ttu-id="ee26c-125">A ID do aplicativo do aplicativo ao qual adicionar as credenciais.</span><span class="sxs-lookup"><span data-stu-id="ee26c-125">The application id of the application to add the credentials to.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdWithCertValueParameterSet, ApplicationIdWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee26c-126">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="ee26c-126">-ApplicationObject</span></span>
<span data-ttu-id="ee26c-127">O objeto de aplicativo ao qual adicionar as credenciais.</span><span class="sxs-lookup"><span data-stu-id="ee26c-127">The application object to add the credentials to.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithCertValueParameterSet, ApplicationObjectWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ee26c-128">-Certvalue</span><span class="sxs-lookup"><span data-stu-id="ee26c-128">-CertValue</span></span>
<span data-ttu-id="ee26c-129">O valor do tipo de credencial "assimétricod".</span><span class="sxs-lookup"><span data-stu-id="ee26c-129">The value of the "asymmetric" credential type.</span></span> <span data-ttu-id="ee26c-130">Ele representa o certificado codificado básico do 64.</span><span class="sxs-lookup"><span data-stu-id="ee26c-130">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithCertValueParameterSet, ApplicationIdWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DisplayNameWithCertValueParameterSet, ApplicationObjectWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee26c-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee26c-131">-DefaultProfile</span></span>
<span data-ttu-id="ee26c-132">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="ee26c-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ee26c-133">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ee26c-133">-DisplayName</span></span>
<span data-ttu-id="ee26c-134">O nome de exibição do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ee26c-134">The display name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameWithPasswordParameterSet, DisplayNameWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee26c-135">-EndDate</span><span class="sxs-lookup"><span data-stu-id="ee26c-135">-EndDate</span></span>
<span data-ttu-id="ee26c-136">A data de término efetiva do uso da credencial.</span><span class="sxs-lookup"><span data-stu-id="ee26c-136">The effective end date of the credential usage.</span></span> <span data-ttu-id="ee26c-137">O valor padrão de data de término é um ano a partir de hoje.</span><span class="sxs-lookup"><span data-stu-id="ee26c-137">The default end date value is one year from today.</span></span>  <span data-ttu-id="ee26c-138">Para uma credencial de tipo "assimétrico", deve ser definida como at ou antes da data em que o certificado X509 é válido.</span><span class="sxs-lookup"><span data-stu-id="ee26c-138">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee26c-139">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="ee26c-139">-ObjectId</span></span>
<span data-ttu-id="ee26c-140">A ID do objeto do aplicativo para o qual adicionar as credenciais.</span><span class="sxs-lookup"><span data-stu-id="ee26c-140">The object id of the application to add the credentials to.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdWithPasswordParameterSet, ApplicationObjectIdWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee26c-141">-Senha</span><span class="sxs-lookup"><span data-stu-id="ee26c-141">-Password</span></span>
<span data-ttu-id="ee26c-142">A senha a ser associada ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ee26c-142">The password to be associated with the application.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ApplicationObjectIdWithPasswordParameterSet, ApplicationIdWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Security.SecureString
Parameter Sets: DisplayNameWithPasswordParameterSet, ApplicationObjectWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee26c-143">-StartDate</span><span class="sxs-lookup"><span data-stu-id="ee26c-143">-StartDate</span></span>
<span data-ttu-id="ee26c-144">A data de início efetiva do uso da credencial.</span><span class="sxs-lookup"><span data-stu-id="ee26c-144">The effective start date of the credential usage.</span></span> <span data-ttu-id="ee26c-145">O valor da data de início padrão é hoje.</span><span class="sxs-lookup"><span data-stu-id="ee26c-145">The default start date value is today.</span></span> <span data-ttu-id="ee26c-146">Para uma credencial de tipo "assimétrico", isso deve ser definido como ligado ou posterior à data a partir da qual o certificado X509 é válido.</span><span class="sxs-lookup"><span data-stu-id="ee26c-146">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee26c-147">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ee26c-147">-Confirm</span></span>
<span data-ttu-id="ee26c-148">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee26c-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee26c-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee26c-149">-WhatIf</span></span>
<span data-ttu-id="ee26c-150">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ee26c-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee26c-151">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ee26c-151">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee26c-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee26c-152">CommonParameters</span></span>
<span data-ttu-id="ee26c-153">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee26c-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee26c-154">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee26c-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee26c-155">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ee26c-155">INPUTS</span></span>

### <span data-ttu-id="ee26c-156">System. GUID</span><span class="sxs-lookup"><span data-stu-id="ee26c-156">System.Guid</span></span>

### <span data-ttu-id="ee26c-157">System. String</span><span class="sxs-lookup"><span data-stu-id="ee26c-157">System.String</span></span>

### <span data-ttu-id="ee26c-158">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="ee26c-158">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="ee26c-159">Parâmetros: applicationObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ee26c-159">Parameters: ApplicationObject (ByValue)</span></span>

### <span data-ttu-id="ee26c-160">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="ee26c-160">System.Security.SecureString</span></span>

### <span data-ttu-id="ee26c-161">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="ee26c-161">System.DateTime</span></span>

## <span data-ttu-id="ee26c-162">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ee26c-162">OUTPUTS</span></span>

### <span data-ttu-id="ee26c-163">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="ee26c-163">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="ee26c-164">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ee26c-164">NOTES</span></span>

## <span data-ttu-id="ee26c-165">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ee26c-165">RELATED LINKS</span></span>

[<span data-ttu-id="ee26c-166">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="ee26c-166">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="ee26c-167">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="ee26c-167">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="ee26c-168">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="ee26c-168">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

