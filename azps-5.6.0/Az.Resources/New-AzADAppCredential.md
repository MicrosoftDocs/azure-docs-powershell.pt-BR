---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 98836BC0-AB4F-4F24-88BE-E7DD350B71E8
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADAppCredential.md
ms.openlocfilehash: 1a80a5a2b6bb5e7af4d6467414feb3936377ea8c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889609"
---
# <span data-ttu-id="e27fc-101">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="e27fc-101">New-AzADAppCredential</span></span>

## <span data-ttu-id="e27fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e27fc-102">SYNOPSIS</span></span>
<span data-ttu-id="e27fc-103">Adiciona uma credencial a um aplicativo existente.</span><span class="sxs-lookup"><span data-stu-id="e27fc-103">Adds a credential to an existing application.</span></span>

## <span data-ttu-id="e27fc-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="e27fc-104">SYNTAX</span></span>

### <span data-ttu-id="e27fc-105">ApplicationObjectIdWithPasswordParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="e27fc-105">ApplicationObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzADAppCredential -ObjectId <String> -Password <SecureString> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e27fc-106">ApplicationObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="e27fc-106">ApplicationObjectIdWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -ObjectId <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e27fc-107">ApplicationIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="e27fc-107">ApplicationIdWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e27fc-108">ApplicationIdWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="e27fc-108">ApplicationIdWithPasswordParameterSet</span></span>
```
New-AzADAppCredential -ApplicationId <Guid> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e27fc-109">DisplayNameWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="e27fc-109">DisplayNameWithPasswordParameterSet</span></span>
```
New-AzADAppCredential -DisplayName <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e27fc-110">DisplayNameWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="e27fc-110">DisplayNameWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -DisplayName <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e27fc-111">ApplicationObjectWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="e27fc-111">ApplicationObjectWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e27fc-112">ApplicationObjectWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="e27fc-112">ApplicationObjectWithPasswordParameterSet</span></span>
```
New-AzADAppCredential -ApplicationObject <PSADApplication> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e27fc-113">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="e27fc-113">DESCRIPTION</span></span>
<span data-ttu-id="e27fc-114">O New-AzADAppCredential cmdlet pode ser usado para adicionar uma nova credencial ou rolar credenciais para um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e27fc-114">The New-AzADAppCredential cmdlet can be used to add a new credential or to roll credentials for an application.</span></span>
<span data-ttu-id="e27fc-115">O aplicativo é identificado fornecendo a ID do objeto de aplicativo ou a ID do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e27fc-115">The application is identified by supplying either the application object id or application Id.</span></span>

## <span data-ttu-id="e27fc-116">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e27fc-116">EXAMPLES</span></span>

### <span data-ttu-id="e27fc-117">Exemplo 1 - Criar uma nova credencial de aplicativo usando uma senha</span><span class="sxs-lookup"><span data-stu-id="e27fc-117">Example 1 - Create a new application credential using a password</span></span>

```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzADAppCredential -ObjectId 1f89cf81-0146-4f4e-beae-2007d0668416 -Password $SecureStringPassword
```

<span data-ttu-id="e27fc-118">Uma nova credencial de senha é adicionada ao aplicativo existente com a id do objeto '1f89cf81-0146-4f4e-beae-2007d0668416'.</span><span class="sxs-lookup"><span data-stu-id="e27fc-118">A new password credential is added to the existing application with object id '1f89cf81-0146-4f4e-beae-2007d0668416'.</span></span>

### <span data-ttu-id="e27fc-119">Exemplo 2 - Criar uma nova credencial de aplicativo usando um certificado</span><span class="sxs-lookup"><span data-stu-id="e27fc-119">Example 2 - Create a new application credential using a certificate</span></span>

```
PS C:\> $cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2
PS C:\> $cer.Import("C:\myapp.cer")
PS C:\> $binCert = $cer.GetRawCertData()
PS C:\> $credValue = [System.Convert]::ToBase64String($binCert)
PS C:\> New-AzADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 -CertValue $credValue -StartDate $cer.NotBefore -EndDate $cer.NotAfter
```

<span data-ttu-id="e27fc-120">O certificado X509 público codificado em base64 fornecido ("myapp.cer") é adicionado ao aplicativo existente com id de aplicativo '4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58'.</span><span class="sxs-lookup"><span data-stu-id="e27fc-120">The supplied base64 encoded public X509 certificate ("myapp.cer") is added to the existing application with application id '4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58'.</span></span>

### <span data-ttu-id="e27fc-121">Exemplo 3 - Criar uma nova credencial de aplicativo usando a canalização</span><span class="sxs-lookup"><span data-stu-id="e27fc-121">Example 3 - Create a new application credential using piping</span></span>

```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> Get-AzADApplication -ObjectId 1f89cf81-0146-4f4e-beae-2007d0668416 | New-AzADAppCredential -Password $SecureStringPassword
```

<span data-ttu-id="e27fc-122">Obtém o aplicativo com a id do objeto '1f89cf81-0146-4f4e-beae-2007d0668416' e canalizará isso para o New-AzADAppCredential para criar uma nova credencial de aplicativo para esse aplicativo com a senha determinada.</span><span class="sxs-lookup"><span data-stu-id="e27fc-122">Gets the application with object id '1f89cf81-0146-4f4e-beae-2007d0668416' and pipes that to the New-AzADAppCredential to create a new application credential for that application with the given password.</span></span>

## <span data-ttu-id="e27fc-123">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="e27fc-123">PARAMETERS</span></span>

### <span data-ttu-id="e27fc-124">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="e27fc-124">-ApplicationId</span></span>
<span data-ttu-id="e27fc-125">A ID do aplicativo para adicionar as credenciais.</span><span class="sxs-lookup"><span data-stu-id="e27fc-125">The application id of the application to add the credentials to.</span></span>

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

### <span data-ttu-id="e27fc-126">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="e27fc-126">-ApplicationObject</span></span>
<span data-ttu-id="e27fc-127">O objeto application para adicionar as credenciais.</span><span class="sxs-lookup"><span data-stu-id="e27fc-127">The application object to add the credentials to.</span></span>

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

### <span data-ttu-id="e27fc-128">-CertValue</span><span class="sxs-lookup"><span data-stu-id="e27fc-128">-CertValue</span></span>
<span data-ttu-id="e27fc-129">O valor do tipo de credencial "assimétrico".</span><span class="sxs-lookup"><span data-stu-id="e27fc-129">The value of the "asymmetric" credential type.</span></span> <span data-ttu-id="e27fc-130">Ele representa o certificado codificado base 64.</span><span class="sxs-lookup"><span data-stu-id="e27fc-130">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="e27fc-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e27fc-131">-DefaultProfile</span></span>
<span data-ttu-id="e27fc-132">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="e27fc-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e27fc-133">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e27fc-133">-DisplayName</span></span>
<span data-ttu-id="e27fc-134">O nome de exibição do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e27fc-134">The display name of the application.</span></span>

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

### <span data-ttu-id="e27fc-135">-EndDate</span><span class="sxs-lookup"><span data-stu-id="e27fc-135">-EndDate</span></span>
<span data-ttu-id="e27fc-136">A data de término efetiva do uso da credencial.</span><span class="sxs-lookup"><span data-stu-id="e27fc-136">The effective end date of the credential usage.</span></span> <span data-ttu-id="e27fc-137">O valor de data de término padrão é de um ano a partir de hoje.</span><span class="sxs-lookup"><span data-stu-id="e27fc-137">The default end date value is one year from today.</span></span>  <span data-ttu-id="e27fc-138">Para uma credencial de tipo "assimétrica", ela deve ser definida como em ou antes da data em que o certificado X509 é válido.</span><span class="sxs-lookup"><span data-stu-id="e27fc-138">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="e27fc-139">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="e27fc-139">-ObjectId</span></span>
<span data-ttu-id="e27fc-140">A ID do objeto do aplicativo para adicionar as credenciais.</span><span class="sxs-lookup"><span data-stu-id="e27fc-140">The object id of the application to add the credentials to.</span></span>

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

### <span data-ttu-id="e27fc-141">-Password</span><span class="sxs-lookup"><span data-stu-id="e27fc-141">-Password</span></span>
<span data-ttu-id="e27fc-142">A senha a ser associada ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="e27fc-142">The password to be associated with the application.</span></span>

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

### <span data-ttu-id="e27fc-143">-StartDate</span><span class="sxs-lookup"><span data-stu-id="e27fc-143">-StartDate</span></span>
<span data-ttu-id="e27fc-144">A data de início efetiva do uso da credencial.</span><span class="sxs-lookup"><span data-stu-id="e27fc-144">The effective start date of the credential usage.</span></span> <span data-ttu-id="e27fc-145">O valor de data de início padrão é hoje.</span><span class="sxs-lookup"><span data-stu-id="e27fc-145">The default start date value is today.</span></span> <span data-ttu-id="e27fc-146">Para uma credencial de tipo "assimétrica", ela deve ser definida como em ou após a data da qual o certificado X509 é válido.</span><span class="sxs-lookup"><span data-stu-id="e27fc-146">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="e27fc-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e27fc-147">-Confirm</span></span>
<span data-ttu-id="e27fc-148">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e27fc-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e27fc-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e27fc-149">-WhatIf</span></span>
<span data-ttu-id="e27fc-150">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e27fc-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e27fc-151">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e27fc-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e27fc-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e27fc-152">CommonParameters</span></span>
<span data-ttu-id="e27fc-153">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e27fc-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e27fc-154">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e27fc-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e27fc-155">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e27fc-155">INPUTS</span></span>

### <span data-ttu-id="e27fc-156">System.String</span><span class="sxs-lookup"><span data-stu-id="e27fc-156">System.String</span></span>

### <span data-ttu-id="e27fc-157">System.Guid</span><span class="sxs-lookup"><span data-stu-id="e27fc-157">System.Guid</span></span>

### <span data-ttu-id="e27fc-158">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="e27fc-158">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="e27fc-159">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="e27fc-159">System.Security.SecureString</span></span>

### <span data-ttu-id="e27fc-160">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="e27fc-160">System.DateTime</span></span>

## <span data-ttu-id="e27fc-161">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="e27fc-161">OUTPUTS</span></span>

### <span data-ttu-id="e27fc-162">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span><span class="sxs-lookup"><span data-stu-id="e27fc-162">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="e27fc-163">NOTES</span><span class="sxs-lookup"><span data-stu-id="e27fc-163">NOTES</span></span>

## <span data-ttu-id="e27fc-164">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e27fc-164">RELATED LINKS</span></span>

[<span data-ttu-id="e27fc-165">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="e27fc-165">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="e27fc-166">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="e27fc-166">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="e27fc-167">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="e27fc-167">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

