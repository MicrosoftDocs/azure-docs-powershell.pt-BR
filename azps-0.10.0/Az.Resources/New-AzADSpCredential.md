---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 063BAA79-484D-48CF-9170-3808813752BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzADSpCredential.md
ms.openlocfilehash: 4c68470b97134019b0abf7724012f3a6fab4627f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776414"
---
# <span data-ttu-id="d6b36-101">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="d6b36-101">New-AzADSpCredential</span></span>

## <span data-ttu-id="d6b36-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d6b36-102">SYNOPSIS</span></span>
<span data-ttu-id="d6b36-103">Adiciona uma credencial a uma entidade de serviço existente.</span><span class="sxs-lookup"><span data-stu-id="d6b36-103">Adds a credential to an existing service principal.</span></span>

## <span data-ttu-id="d6b36-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d6b36-104">SYNTAX</span></span>

### <span data-ttu-id="d6b36-105">SpObjectIdWithPasswordParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="d6b36-105">SpObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzADSpCredential -ObjectId <Guid> [-Password <SecureString>] [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6b36-106">SpObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6b36-106">SpObjectIdWithCertValueParameterSet</span></span>
```
New-AzADSpCredential -ObjectId <Guid> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6b36-107">SPNWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6b36-107">SPNWithCertValueParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6b36-108">SPNWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6b36-108">SPNWithPasswordParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalName <String> [-Password <SecureString>] [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6b36-109">ServicePrincipalObjectWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6b36-109">ServicePrincipalObjectWithCertValueParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> -CertValue <String>
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d6b36-110">ServicePrincipalObjectWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6b36-110">ServicePrincipalObjectWithPasswordParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-Password <SecureString>]
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d6b36-111">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d6b36-111">DESCRIPTION</span></span>
<span data-ttu-id="d6b36-112">O cmdlet New-AzADSpCredential pode ser usado para adicionar uma nova credencial ou para rolar credenciais para uma entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="d6b36-112">The New-AzADSpCredential cmdlet can be used to add a new credential or to roll credentials for a service principal.</span></span>
<span data-ttu-id="d6b36-113">A entidade de serviço é identificada fornecendo a identificação do objeto ou o nome da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="d6b36-113">The service principal is identified by supplying either the object id or service principal name.</span></span>

## <span data-ttu-id="d6b36-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d6b36-114">EXAMPLES</span></span>

### <span data-ttu-id="d6b36-115">Exemplo 1-Crie uma nova credencial de entidade de serviço usando uma senha gerada</span><span class="sxs-lookup"><span data-stu-id="d6b36-115">Example 1 - Create a new service principal credential using a generated password</span></span>

```
PS C:\> New-AzADSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476

Secret    : System.Security.SecureString
StartDate : 11/12/2018 9:36:05 PM
EndDate   : 11/12/2019 9:36:05 PM
KeyId     : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Type      : Password
```

<span data-ttu-id="d6b36-116">Uma nova credencial de senha é adicionada à entidade de serviço existente com a ID de objeto ' 1f99cf81-0146-4f4e-BEAE-2007d0668476 '.</span><span class="sxs-lookup"><span data-stu-id="d6b36-116">A new password credential is added to the existing service principal with object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

### <span data-ttu-id="d6b36-117">Exemplo 2-criar uma nova credencial de entidade de serviço usando um certificado</span><span class="sxs-lookup"><span data-stu-id="d6b36-117">Example 2 - Create a new service principal credential using a certificate</span></span>

```
PS C:\> $cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate 
PS C:\> $cer.Import("C:\myapp.cer") 
PS C:\> $binCert = $cer.GetRawCertData() 
PS C:\> $credValue = [System.Convert]::ToBase64String($binCert)
PS C:\> New-AzADSpCredential -ServicePrincipalName "http://test123" -CertValue $credValue -StartDate $cer.GetEffectiveDateString() -EndDate $cer.GetExpirationDateString()
```

<span data-ttu-id="d6b36-118">O certificado X509 público codificado em base64 fornecido ("MyApp. cer") é adicionado à entidade de serviço existente usando seu SPN.</span><span class="sxs-lookup"><span data-stu-id="d6b36-118">The supplied base64 encoded public X509 certificate ("myapp.cer") is added to the existing service principal using its SPN.</span></span>

### <span data-ttu-id="d6b36-119">Exemplo 3-criar uma nova credencial de entidade de serviço usando o encanamento</span><span class="sxs-lookup"><span data-stu-id="d6b36-119">Example 3 - Create a new service principal credential using piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | New-AzADSpCredential

Secret    : System.Security.SecureString
StartDate : 11/12/2018 9:36:05 PM
EndDate   : 11/12/2019 9:36:05 PM
KeyId     : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Type      : Password
```

<span data-ttu-id="d6b36-120">Obtém a entidade de serviço com a ID de objeto ' 1f99cf81-0146-4f4e-BEAE-2007d0668476 ' e canaliza a New-AzADSpCredential para criar uma nova credencial de entidade de serviço para essa entidade de serviço com uma senha gerada.</span><span class="sxs-lookup"><span data-stu-id="d6b36-120">Gets the service principal with object id '1f99cf81-0146-4f4e-beae-2007d0668476' and pipes that to the New-AzADSpCredential to create a new service principal credential for that service principal with a generated password.</span></span>

## <span data-ttu-id="d6b36-121">OS</span><span class="sxs-lookup"><span data-stu-id="d6b36-121">PARAMETERS</span></span>

### <span data-ttu-id="d6b36-122">-Certvalue</span><span class="sxs-lookup"><span data-stu-id="d6b36-122">-CertValue</span></span>
<span data-ttu-id="d6b36-123">O valor do tipo de credencial "assimétricod".</span><span class="sxs-lookup"><span data-stu-id="d6b36-123">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="d6b36-124">Ele representa o certificado codificado básico do 64.</span><span class="sxs-lookup"><span data-stu-id="d6b36-124">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: SpObjectIdWithCertValueParameterSet, SPNWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServicePrincipalObjectWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6b36-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6b36-125">-DefaultProfile</span></span>
<span data-ttu-id="d6b36-126">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="d6b36-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d6b36-127">-EndDate</span><span class="sxs-lookup"><span data-stu-id="d6b36-127">-EndDate</span></span>
<span data-ttu-id="d6b36-128">A data de término efetiva do uso da credencial.</span><span class="sxs-lookup"><span data-stu-id="d6b36-128">The effective end date of the credential usage.</span></span>
<span data-ttu-id="d6b36-129">O valor padrão de data de término é um ano a partir de hoje.</span><span class="sxs-lookup"><span data-stu-id="d6b36-129">The default end date value is one year from today.</span></span> <span data-ttu-id="d6b36-130">Para uma credencial de tipo "assimétrico", deve ser definida como at ou antes da data em que o certificado X509 é válido.</span><span class="sxs-lookup"><span data-stu-id="d6b36-130">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="d6b36-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="d6b36-131">-ObjectId</span></span>
<span data-ttu-id="d6b36-132">A ID de objeto da entidade de serviço para a qual as credenciais são adicionadas.</span><span class="sxs-lookup"><span data-stu-id="d6b36-132">The object id of the service principal to add the credentials to.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SpObjectIdWithPasswordParameterSet, SpObjectIdWithCertValueParameterSet
Aliases: ServicePrincipalObjectId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6b36-133">-Senha</span><span class="sxs-lookup"><span data-stu-id="d6b36-133">-Password</span></span>
<span data-ttu-id="d6b36-134">A senha a ser associada ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d6b36-134">The password to be associated with the application.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: SpObjectIdWithPasswordParameterSet, SPNWithPasswordParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Security.SecureString
Parameter Sets: ServicePrincipalObjectWithPasswordParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6b36-135">-Serviceprincipalnamename</span><span class="sxs-lookup"><span data-stu-id="d6b36-135">-ServicePrincipalName</span></span>
<span data-ttu-id="d6b36-136">O nome (SPN) da entidade de serviço para a qual adicionar as credenciais.</span><span class="sxs-lookup"><span data-stu-id="d6b36-136">The name (SPN) of the service principal to add the credentials to.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNWithCertValueParameterSet, SPNWithPasswordParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6b36-137">-Serviceprincipalnameobject</span><span class="sxs-lookup"><span data-stu-id="d6b36-137">-ServicePrincipalObject</span></span>
<span data-ttu-id="d6b36-138">O objeto de entidade de serviço para o qual adicionar as credenciais.</span><span class="sxs-lookup"><span data-stu-id="d6b36-138">The service principal object to add the credentials to.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal
Parameter Sets: ServicePrincipalObjectWithCertValueParameterSet, ServicePrincipalObjectWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6b36-139">-StartDate</span><span class="sxs-lookup"><span data-stu-id="d6b36-139">-StartDate</span></span>
<span data-ttu-id="d6b36-140">A data de início efetiva do uso da credencial.</span><span class="sxs-lookup"><span data-stu-id="d6b36-140">The effective start date of the credential usage.</span></span>
<span data-ttu-id="d6b36-141">O valor da data de início padrão é hoje.</span><span class="sxs-lookup"><span data-stu-id="d6b36-141">The default start date value is today.</span></span> <span data-ttu-id="d6b36-142">Para uma credencial de tipo "assimétrico", isso deve ser definido como ligado ou posterior à data a partir da qual o certificado X509 é válido.</span><span class="sxs-lookup"><span data-stu-id="d6b36-142">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="d6b36-143">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d6b36-143">-Confirm</span></span>
<span data-ttu-id="d6b36-144">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6b36-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6b36-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6b36-145">-WhatIf</span></span>
<span data-ttu-id="d6b36-146">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d6b36-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6b36-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d6b36-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6b36-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6b36-148">CommonParameters</span></span>
<span data-ttu-id="d6b36-149">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6b36-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6b36-150">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6b36-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6b36-151">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d6b36-151">INPUTS</span></span>

### <span data-ttu-id="d6b36-152">System. GUID</span><span class="sxs-lookup"><span data-stu-id="d6b36-152">System.Guid</span></span>

### <span data-ttu-id="d6b36-153">System. String</span><span class="sxs-lookup"><span data-stu-id="d6b36-153">System.String</span></span>

### <span data-ttu-id="d6b36-154">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="d6b36-154">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>
<span data-ttu-id="d6b36-155">Parâmetros: servicePrincipalName (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d6b36-155">Parameters: ServicePrincipalObject (ByValue)</span></span>

### <span data-ttu-id="d6b36-156">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="d6b36-156">System.Security.SecureString</span></span>

### <span data-ttu-id="d6b36-157">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="d6b36-157">System.DateTime</span></span>

## <span data-ttu-id="d6b36-158">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d6b36-158">OUTPUTS</span></span>

### <span data-ttu-id="d6b36-159">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="d6b36-159">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

### <span data-ttu-id="d6b36-160">Microsoft. Azure. Commands. Resources. Models. Authorization. PSADCredentialWrapper</span><span class="sxs-lookup"><span data-stu-id="d6b36-160">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADCredentialWrapper</span></span>

## <span data-ttu-id="d6b36-161">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d6b36-161">NOTES</span></span>

## <span data-ttu-id="d6b36-162">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d6b36-162">RELATED LINKS</span></span>

[<span data-ttu-id="d6b36-163">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="d6b36-163">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="d6b36-164">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="d6b36-164">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)

[<span data-ttu-id="d6b36-165">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="d6b36-165">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)



