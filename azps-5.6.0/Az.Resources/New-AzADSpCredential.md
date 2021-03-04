---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 063BAA79-484D-48CF-9170-3808813752BD
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADSpCredential.md
ms.openlocfilehash: 38952cb7c7deebb76568bef2a2062d20c3c1b497
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887968"
---
# <span data-ttu-id="9f259-101">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="9f259-101">New-AzADSpCredential</span></span>

## <span data-ttu-id="9f259-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f259-102">SYNOPSIS</span></span>
<span data-ttu-id="9f259-103">Adiciona uma credencial a uma entidade de serviço existente.</span><span class="sxs-lookup"><span data-stu-id="9f259-103">Adds a credential to an existing service principal.</span></span>

## <span data-ttu-id="9f259-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9f259-104">SYNTAX</span></span>

### <span data-ttu-id="9f259-105">SpObjectIdWithPasswordParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="9f259-105">SpObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzADSpCredential -ObjectId <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f259-106">SpObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f259-106">SpObjectIdWithCertValueParameterSet</span></span>
```
New-AzADSpCredential -ObjectId <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f259-107">SPNWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f259-107">SPNWithCertValueParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f259-108">SPNWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f259-108">SPNWithPasswordParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalName <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f259-109">ServicePrincipalObjectWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f259-109">ServicePrincipalObjectWithCertValueParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f259-110">ServicePrincipalObjectWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f259-110">ServicePrincipalObjectWithPasswordParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f259-111">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9f259-111">DESCRIPTION</span></span>
<span data-ttu-id="9f259-112">O New-AzADSpCredential cmdlet pode ser usado para adicionar uma nova credencial ou rolar credenciais para uma entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="9f259-112">The New-AzADSpCredential cmdlet can be used to add a new credential or to roll credentials for a service principal.</span></span>
<span data-ttu-id="9f259-113">A entidade de serviço é identificada fornecendo o ID do objeto ou o nome principal do serviço.</span><span class="sxs-lookup"><span data-stu-id="9f259-113">The service principal is identified by supplying either the object id or service principal name.</span></span>

## <span data-ttu-id="9f259-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9f259-114">EXAMPLES</span></span>

### <span data-ttu-id="9f259-115">Exemplo 1: Criar uma nova credencial de entidade de serviço usando uma senha gerada</span><span class="sxs-lookup"><span data-stu-id="9f259-115">Example 1: Create a new service principal credential using a generated password</span></span>

```powershell
PS C:\> New-AzADSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476

Secret    : System.Security.SecureString
StartDate : 11/12/2018 9:36:05 PM
EndDate   : 11/12/2019 9:36:05 PM
KeyId     : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Type      : Password
```

<span data-ttu-id="9f259-116">Uma nova credencial de senha é adicionada à entidade de serviço existente com a id do objeto '1f99cf81-0146-4f4e-beae-2007d0668476'.</span><span class="sxs-lookup"><span data-stu-id="9f259-116">A new password credential is added to the existing service principal with object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

### <span data-ttu-id="9f259-117">Exemplo 2: Criar uma nova credencial de entidade de serviço usando um certificado</span><span class="sxs-lookup"><span data-stu-id="9f259-117">Example 2: Create a new service principal credential using a certificate</span></span>

```powershell
PS C:\> $cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2
PS C:\> $cer.Import("C:\myapp.cer")
PS C:\> $binCert = $cer.GetRawCertData()
PS C:\> $credValue = [System.Convert]::ToBase64String($binCert)
PS C:\> New-AzADSpCredential -ServicePrincipalName "http://test123" -CertValue $credValue -StartDate $cer.NotBefore -EndDate $cer.NotAfter
```

<span data-ttu-id="9f259-118">O certificado X509 público codificado em base64 fornecido ("myapp.cer") é adicionado à entidade de serviço existente usando seu SPN.</span><span class="sxs-lookup"><span data-stu-id="9f259-118">The supplied base64 encoded public X509 certificate ("myapp.cer") is added to the existing service principal using its SPN.</span></span>

### <span data-ttu-id="9f259-119">Exemplo 3: Criar uma nova credencial de entidade de serviço usando a canalização</span><span class="sxs-lookup"><span data-stu-id="9f259-119">Example 3: Create a new service principal credential using piping</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | New-AzADSpCredential

Secret    : System.Security.SecureString
StartDate : 11/12/2018 9:36:05 PM
EndDate   : 11/12/2019 9:36:05 PM
KeyId     : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Type      : Password
```

<span data-ttu-id="9f259-120">Obtém a entidade de serviço com a id do objeto '1f99cf81-0146-4f4e-beae-2007d0668476' e canalizará isso para o New-AzADSpCredential para criar uma nova credencial de entidade de serviço para essa entidade de serviço com uma senha gerada.</span><span class="sxs-lookup"><span data-stu-id="9f259-120">Gets the service principal with object id '1f99cf81-0146-4f4e-beae-2007d0668476' and pipes that to the New-AzADSpCredential to create a new service principal credential for that service principal with a generated password.</span></span>

## <span data-ttu-id="9f259-121">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9f259-121">PARAMETERS</span></span>

### <span data-ttu-id="9f259-122">-CertValue</span><span class="sxs-lookup"><span data-stu-id="9f259-122">-CertValue</span></span>
<span data-ttu-id="9f259-123">O valor do tipo de credencial "assimétrico".</span><span class="sxs-lookup"><span data-stu-id="9f259-123">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="9f259-124">Ele representa o certificado codificado base 64.</span><span class="sxs-lookup"><span data-stu-id="9f259-124">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="9f259-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f259-125">-DefaultProfile</span></span>
<span data-ttu-id="9f259-126">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="9f259-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9f259-127">-EndDate</span><span class="sxs-lookup"><span data-stu-id="9f259-127">-EndDate</span></span>
<span data-ttu-id="9f259-128">A data de término efetiva do uso da credencial.</span><span class="sxs-lookup"><span data-stu-id="9f259-128">The effective end date of the credential usage.</span></span>
<span data-ttu-id="9f259-129">O valor de data de término padrão é de um ano a partir de hoje.</span><span class="sxs-lookup"><span data-stu-id="9f259-129">The default end date value is one year from today.</span></span>
<span data-ttu-id="9f259-130">Para uma credencial de tipo "assimétrica", ela deve ser definida como em ou antes da data em que o certificado X509 é válido.</span><span class="sxs-lookup"><span data-stu-id="9f259-130">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="9f259-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="9f259-131">-ObjectId</span></span>
<span data-ttu-id="9f259-132">A id do objeto da entidade de serviço para adicionar as credenciais.</span><span class="sxs-lookup"><span data-stu-id="9f259-132">The object id of the service principal to add the credentials to.</span></span>

```yaml
Type: System.String
Parameter Sets: SpObjectIdWithPasswordParameterSet, SpObjectIdWithCertValueParameterSet
Aliases: ServicePrincipalObjectId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9f259-133">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="9f259-133">-ServicePrincipalName</span></span>
<span data-ttu-id="9f259-134">O nome (SPN) da entidade de serviço para adicionar as credenciais.</span><span class="sxs-lookup"><span data-stu-id="9f259-134">The name (SPN) of the service principal to add the credentials to.</span></span>

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

### <span data-ttu-id="9f259-135">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="9f259-135">-ServicePrincipalObject</span></span>
<span data-ttu-id="9f259-136">O objeto principal do serviço ao que adicionar as credenciais.</span><span class="sxs-lookup"><span data-stu-id="9f259-136">The service principal object to add the credentials to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal
Parameter Sets: ServicePrincipalObjectWithCertValueParameterSet, ServicePrincipalObjectWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f259-137">-StartDate</span><span class="sxs-lookup"><span data-stu-id="9f259-137">-StartDate</span></span>
<span data-ttu-id="9f259-138">A data de início efetiva do uso da credencial.</span><span class="sxs-lookup"><span data-stu-id="9f259-138">The effective start date of the credential usage.</span></span>
<span data-ttu-id="9f259-139">O valor de data de início padrão é hoje.</span><span class="sxs-lookup"><span data-stu-id="9f259-139">The default start date value is today.</span></span>
<span data-ttu-id="9f259-140">Para uma credencial de tipo "assimétrica", ela deve ser definida como em ou após a data da qual o certificado X509 é válido.</span><span class="sxs-lookup"><span data-stu-id="9f259-140">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="9f259-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9f259-141">-Confirm</span></span>
<span data-ttu-id="9f259-142">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f259-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f259-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f259-143">-WhatIf</span></span>
<span data-ttu-id="9f259-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9f259-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f259-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9f259-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f259-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f259-146">CommonParameters</span></span>
<span data-ttu-id="9f259-147">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f259-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f259-148">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9f259-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f259-149">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9f259-149">INPUTS</span></span>

### <span data-ttu-id="9f259-150">System.String</span><span class="sxs-lookup"><span data-stu-id="9f259-150">System.String</span></span>

### <span data-ttu-id="9f259-151">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="9f259-151">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="9f259-152">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="9f259-152">System.DateTime</span></span>

## <span data-ttu-id="9f259-153">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9f259-153">OUTPUTS</span></span>

### <span data-ttu-id="9f259-154">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span><span class="sxs-lookup"><span data-stu-id="9f259-154">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

### <span data-ttu-id="9f259-155">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADCredentialWrapper</span><span class="sxs-lookup"><span data-stu-id="9f259-155">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADCredentialWrapper</span></span>

## <span data-ttu-id="9f259-156">NOTES</span><span class="sxs-lookup"><span data-stu-id="9f259-156">NOTES</span></span>

## <span data-ttu-id="9f259-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9f259-157">RELATED LINKS</span></span>

[<span data-ttu-id="9f259-158">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="9f259-158">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="9f259-159">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="9f259-159">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)

[<span data-ttu-id="9f259-160">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="9f259-160">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)



