---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 98836BC0-AB4F-4F24-88BE-E7DD350B71E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADAppCredential.md
ms.openlocfilehash: e0d842e1cd93932b92eff82d2c60dc228817b0e7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772574"
---
# <span data-ttu-id="54f79-101">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="54f79-101">New-AzADAppCredential</span></span>

## <span data-ttu-id="54f79-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="54f79-102">SYNOPSIS</span></span>
<span data-ttu-id="54f79-103">Adiciona uma credencial a um aplicativo existente.</span><span class="sxs-lookup"><span data-stu-id="54f79-103">Adds a credential to an existing application.</span></span>

## <span data-ttu-id="54f79-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="54f79-104">SYNTAX</span></span>

### <span data-ttu-id="54f79-105">ApplicationObjectIdWithPasswordParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="54f79-105">ApplicationObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzADAppCredential -ObjectId <String> -Password <SecureString> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54f79-106">ApplicationObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="54f79-106">ApplicationObjectIdWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -ObjectId <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54f79-107">ApplicationIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="54f79-107">ApplicationIdWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54f79-108">ApplicationIdWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="54f79-108">ApplicationIdWithPasswordParameterSet</span></span>
```
New-AzADAppCredential -ApplicationId <Guid> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54f79-109">DisplayNameWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="54f79-109">DisplayNameWithPasswordParameterSet</span></span>
```
New-AzADAppCredential -DisplayName <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54f79-110">DisplayNameWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="54f79-110">DisplayNameWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -DisplayName <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54f79-111">ApplicationObjectWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="54f79-111">ApplicationObjectWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54f79-112">ApplicationObjectWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="54f79-112">ApplicationObjectWithPasswordParameterSet</span></span>
```
New-AzADAppCredential -ApplicationObject <PSADApplication> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54f79-113">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="54f79-113">DESCRIPTION</span></span>
<span data-ttu-id="54f79-114">O cmdlet New-AzADAppCredential pode ser usado para adicionar uma nova credencial ou para rolar credenciais para um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="54f79-114">The New-AzADAppCredential cmdlet can be used to add a new credential or to roll credentials for an application.</span></span>
<span data-ttu-id="54f79-115">O aplicativo é identificado fornecendo a identificação do objeto do aplicativo ou a ID do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="54f79-115">The application is identified by supplying either the application object id or application Id.</span></span>

## <span data-ttu-id="54f79-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="54f79-116">EXAMPLES</span></span>

### <span data-ttu-id="54f79-117">Exemplo 1-criar uma nova credencial de aplicativo usando uma senha</span><span class="sxs-lookup"><span data-stu-id="54f79-117">Example 1 - Create a new application credential using a password</span></span>

```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzADAppCredential -ObjectId 1f89cf81-0146-4f4e-beae-2007d0668416 -Password $SecureStringPassword
```

<span data-ttu-id="54f79-118">Uma nova credencial de senha é adicionada ao aplicativo existente com a ID de objeto ' 1f89cf81-0146-4f4e-BEAE-2007d0668416 '.</span><span class="sxs-lookup"><span data-stu-id="54f79-118">A new password credential is added to the existing application with object id '1f89cf81-0146-4f4e-beae-2007d0668416'.</span></span>

### <span data-ttu-id="54f79-119">Exemplo 2-criar uma nova credencial de aplicativo usando um certificado</span><span class="sxs-lookup"><span data-stu-id="54f79-119">Example 2 - Create a new application credential using a certificate</span></span>

```
PS C:\> $cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2
PS C:\> $cer.Import("C:\myapp.cer")
PS C:\> $binCert = $cer.GetRawCertData()
PS C:\> $credValue = [System.Convert]::ToBase64String($binCert)
PS C:\> New-AzADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 -CertValue $credValue -StartDate $cer.NotBefore -EndDate $cer.NotAfter
```

<span data-ttu-id="54f79-120">O certificado X509 público codificado em base64 fornecido ("MyApp. cer") é adicionado ao aplicativo existente com a ID de aplicativo ' 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 '.</span><span class="sxs-lookup"><span data-stu-id="54f79-120">The supplied base64 encoded public X509 certificate ("myapp.cer") is added to the existing application with application id '4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58'.</span></span>

### <span data-ttu-id="54f79-121">Exemplo 3-criar uma nova credencial de aplicativo usando o encanamento</span><span class="sxs-lookup"><span data-stu-id="54f79-121">Example 3 - Create a new application credential using piping</span></span>

```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> Get-AzADApplication -ObjectId 1f89cf81-0146-4f4e-beae-2007d0668416 | New-AzADAppCredential -Password $SecureStringPassword
```

<span data-ttu-id="54f79-122">Obtém o aplicativo com a ID de objeto ' 1f89cf81-0146-4f4e-BEAE-2007d0668416 ' e canaliza o New-AzADAppCredential para criar uma nova credencial de aplicativo para esse aplicativo com a senha fornecida.</span><span class="sxs-lookup"><span data-stu-id="54f79-122">Gets the application with object id '1f89cf81-0146-4f4e-beae-2007d0668416' and pipes that to the New-AzADAppCredential to create a new application credential for that application with the given password.</span></span>

## <span data-ttu-id="54f79-123">OS</span><span class="sxs-lookup"><span data-stu-id="54f79-123">PARAMETERS</span></span>

### <span data-ttu-id="54f79-124">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="54f79-124">-ApplicationId</span></span>
<span data-ttu-id="54f79-125">A ID do aplicativo do aplicativo ao qual adicionar as credenciais.</span><span class="sxs-lookup"><span data-stu-id="54f79-125">The application id of the application to add the credentials to.</span></span>

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

### <span data-ttu-id="54f79-126">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="54f79-126">-ApplicationObject</span></span>
<span data-ttu-id="54f79-127">O objeto de aplicativo ao qual adicionar as credenciais.</span><span class="sxs-lookup"><span data-stu-id="54f79-127">The application object to add the credentials to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithCertValueParameterSet, ApplicationObjectWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="54f79-128">-Certvalue</span><span class="sxs-lookup"><span data-stu-id="54f79-128">-CertValue</span></span>
<span data-ttu-id="54f79-129">O valor do tipo de credencial "assimétricod".</span><span class="sxs-lookup"><span data-stu-id="54f79-129">The value of the "asymmetric" credential type.</span></span> <span data-ttu-id="54f79-130">Ele representa o certificado codificado básico do 64.</span><span class="sxs-lookup"><span data-stu-id="54f79-130">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="54f79-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54f79-131">-DefaultProfile</span></span>
<span data-ttu-id="54f79-132">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="54f79-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="54f79-133">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="54f79-133">-DisplayName</span></span>
<span data-ttu-id="54f79-134">O nome de exibição do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="54f79-134">The display name of the application.</span></span>

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

### <span data-ttu-id="54f79-135">-EndDate</span><span class="sxs-lookup"><span data-stu-id="54f79-135">-EndDate</span></span>
<span data-ttu-id="54f79-136">A data de término efetiva do uso da credencial.</span><span class="sxs-lookup"><span data-stu-id="54f79-136">The effective end date of the credential usage.</span></span> <span data-ttu-id="54f79-137">O valor padrão de data de término é um ano a partir de hoje.</span><span class="sxs-lookup"><span data-stu-id="54f79-137">The default end date value is one year from today.</span></span>  <span data-ttu-id="54f79-138">Para uma credencial de tipo "assimétrico", deve ser definida como at ou antes da data em que o certificado X509 é válido.</span><span class="sxs-lookup"><span data-stu-id="54f79-138">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="54f79-139">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="54f79-139">-ObjectId</span></span>
<span data-ttu-id="54f79-140">A ID do objeto do aplicativo para o qual adicionar as credenciais.</span><span class="sxs-lookup"><span data-stu-id="54f79-140">The object id of the application to add the credentials to.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithPasswordParameterSet, ApplicationObjectIdWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54f79-141">-Senha</span><span class="sxs-lookup"><span data-stu-id="54f79-141">-Password</span></span>
<span data-ttu-id="54f79-142">A senha a ser associada ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="54f79-142">The password to be associated with the application.</span></span>

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

### <span data-ttu-id="54f79-143">-StartDate</span><span class="sxs-lookup"><span data-stu-id="54f79-143">-StartDate</span></span>
<span data-ttu-id="54f79-144">A data de início efetiva do uso da credencial.</span><span class="sxs-lookup"><span data-stu-id="54f79-144">The effective start date of the credential usage.</span></span> <span data-ttu-id="54f79-145">O valor da data de início padrão é hoje.</span><span class="sxs-lookup"><span data-stu-id="54f79-145">The default start date value is today.</span></span> <span data-ttu-id="54f79-146">Para uma credencial de tipo "assimétrico", isso deve ser definido como ligado ou posterior à data a partir da qual o certificado X509 é válido.</span><span class="sxs-lookup"><span data-stu-id="54f79-146">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="54f79-147">-Confirme</span><span class="sxs-lookup"><span data-stu-id="54f79-147">-Confirm</span></span>
<span data-ttu-id="54f79-148">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54f79-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54f79-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54f79-149">-WhatIf</span></span>
<span data-ttu-id="54f79-150">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="54f79-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54f79-151">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="54f79-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54f79-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54f79-152">CommonParameters</span></span>
<span data-ttu-id="54f79-153">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54f79-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54f79-154">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54f79-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54f79-155">SENSORES</span><span class="sxs-lookup"><span data-stu-id="54f79-155">INPUTS</span></span>

### <span data-ttu-id="54f79-156">System. String</span><span class="sxs-lookup"><span data-stu-id="54f79-156">System.String</span></span>

### <span data-ttu-id="54f79-157">System. GUID</span><span class="sxs-lookup"><span data-stu-id="54f79-157">System.Guid</span></span>

### <span data-ttu-id="54f79-158">Microsoft. Azure. Commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="54f79-158">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="54f79-159">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="54f79-159">System.Security.SecureString</span></span>

### <span data-ttu-id="54f79-160">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="54f79-160">System.DateTime</span></span>

## <span data-ttu-id="54f79-161">EXIBE</span><span class="sxs-lookup"><span data-stu-id="54f79-161">OUTPUTS</span></span>

### <span data-ttu-id="54f79-162">Microsoft. Azure. Commands. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="54f79-162">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="54f79-163">INFORMA</span><span class="sxs-lookup"><span data-stu-id="54f79-163">NOTES</span></span>

## <span data-ttu-id="54f79-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="54f79-164">RELATED LINKS</span></span>

[<span data-ttu-id="54f79-165">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="54f79-165">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="54f79-166">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="54f79-166">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="54f79-167">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="54f79-167">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

