---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 063BAA79-484D-48CF-9170-3808813752BD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADSpCredential.md
ms.openlocfilehash: bf2a42df42a343d9745cb55f4d72463513b44dc3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431628"
---
# <span data-ttu-id="db498-101">New-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="db498-101">New-AzureRmADSpCredential</span></span>

## <span data-ttu-id="db498-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="db498-102">SYNOPSIS</span></span>
<span data-ttu-id="db498-103">Adiciona uma credencial a uma entidade de serviço existente.</span><span class="sxs-lookup"><span data-stu-id="db498-103">Adds a credential to an existing service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db498-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="db498-104">SYNTAX</span></span>

### <span data-ttu-id="db498-105">SpObjectIdWithPasswordParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="db498-105">SpObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzureRmADSpCredential -ObjectId <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db498-106">SpObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="db498-106">SpObjectIdWithCertValueParameterSet</span></span>
```
New-AzureRmADSpCredential -ObjectId <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db498-107">SPNWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="db498-107">SPNWithCertValueParameterSet</span></span>
```
New-AzureRmADSpCredential -ServicePrincipalName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db498-108">SPNWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="db498-108">SPNWithPasswordParameterSet</span></span>
```
New-AzureRmADSpCredential -ServicePrincipalName <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db498-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="db498-109">DESCRIPTION</span></span>
<span data-ttu-id="db498-110">O cmdlet New-AzureRmADSpCredential pode ser usado para adicionar uma nova credencial ou para rolar credenciais para uma entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="db498-110">The New-AzureRmADSpCredential cmdlet can be used to add a new credential or to roll credentials for a service principal.</span></span>
<span data-ttu-id="db498-111">A entidade de serviço é identificada fornecendo a identificação do objeto ou o nome da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="db498-111">The service principal is identified by supplying either the object id or service principal name.</span></span>

## <span data-ttu-id="db498-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="db498-112">EXAMPLES</span></span>

### <span data-ttu-id="db498-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="db498-113">Example 1</span></span>
```
PS E:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS E:\> New-AzureRmADSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 -Password $SecureStringPassword
```

<span data-ttu-id="db498-114">Uma nova credencial de senha é adicionada a uma entidade de serviço existente.</span><span class="sxs-lookup"><span data-stu-id="db498-114">A new password credential is added to an existing service principal.</span></span>
<span data-ttu-id="db498-115">Neste exemplo, o valor de senha fornecido é adicionado à entidade de serviço usando o objectId.</span><span class="sxs-lookup"><span data-stu-id="db498-115">In this example, the supplied password value is added to the service principal using the objectId.</span></span>

### <span data-ttu-id="db498-116">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="db498-116">Example 2</span></span>
```
$cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate 

$cer.Import("C:\myapp.cer") 

$binCert = $cer.GetRawCertData() 

$credValue = [System.Convert]::ToBase64String($binCert)

PS E:\> New-AzureRmADSpCredential -ServicePrincipalName "http://test123" -CertValue $credValue -StartDate $cer.GetEffectiveDateString() -EndDate $cer.GetExpirationDateString()
```

<span data-ttu-id="db498-117">Uma nova credencial de chave é adicionada a uma entidade de serviço existente.</span><span class="sxs-lookup"><span data-stu-id="db498-117">A new key credential is added to an existing service principal.</span></span>
<span data-ttu-id="db498-118">Neste exemplo, o certificado X509 público codificado em base64 fornecido ("MyApp. cer") é adicionado à entidade de serviço usando seu SPN.</span><span class="sxs-lookup"><span data-stu-id="db498-118">In this example, the supplied base64 encoded public X509 certificate ("myapp.cer") is added to the service principal using its SPN.</span></span>

### <span data-ttu-id="db498-119">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="db498-119">Example 3</span></span>

```
PS E:\> New-AzureRmADSpCredential -ServicePrincipalName "http://test123" -CertValue $credValue
```

## <span data-ttu-id="db498-120">OS</span><span class="sxs-lookup"><span data-stu-id="db498-120">PARAMETERS</span></span>

### <span data-ttu-id="db498-121">-Certvalue</span><span class="sxs-lookup"><span data-stu-id="db498-121">-CertValue</span></span>
<span data-ttu-id="db498-122">O valor do tipo de credencial "assimétricod".</span><span class="sxs-lookup"><span data-stu-id="db498-122">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="db498-123">Ele representa o certificado codificado básico do 64.</span><span class="sxs-lookup"><span data-stu-id="db498-123">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: String
Parameter Sets: SpObjectIdWithCertValueParameterSet, SPNWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db498-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db498-124">-DefaultProfile</span></span>
<span data-ttu-id="db498-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="db498-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="db498-126">-EndDate</span><span class="sxs-lookup"><span data-stu-id="db498-126">-EndDate</span></span>
<span data-ttu-id="db498-127">A data de término efetiva do uso da credencial.</span><span class="sxs-lookup"><span data-stu-id="db498-127">The effective end date of the credential usage.</span></span>
<span data-ttu-id="db498-128">O valor padrão de data de término é um ano a partir de hoje.</span><span class="sxs-lookup"><span data-stu-id="db498-128">The default end date value is one year from today.</span></span> <span data-ttu-id="db498-129">Para uma credencial de tipo "assimétrico", deve ser definida como at ou antes da data em que o certificado X509 é válido.</span><span class="sxs-lookup"><span data-stu-id="db498-129">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db498-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="db498-130">-ObjectId</span></span>
<span data-ttu-id="db498-131">A ID de objeto da entidade de serviço para a qual as credenciais são adicionadas.</span><span class="sxs-lookup"><span data-stu-id="db498-131">The object id of the service principal to add the credentials to.</span></span>

```yaml
Type: String
Parameter Sets: SpObjectIdWithPasswordParameterSet, SpObjectIdWithCertValueParameterSet
Aliases: ServicePrincipalObjectId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db498-132">-Senha</span><span class="sxs-lookup"><span data-stu-id="db498-132">-Password</span></span>
<span data-ttu-id="db498-133">A senha a ser associada ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="db498-133">The password to be associated with the application.</span></span>

```yaml
Type: SecureString
Parameter Sets: SpObjectIdWithPasswordParameterSet, SPNWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db498-134">-Serviceprincipalnamename</span><span class="sxs-lookup"><span data-stu-id="db498-134">-ServicePrincipalName</span></span>
<span data-ttu-id="db498-135">O nome (SPN) da entidade de serviço para a qual adicionar as credenciais.</span><span class="sxs-lookup"><span data-stu-id="db498-135">The name (SPN) of the service principal to add the credentials to.</span></span>

```yaml
Type: String
Parameter Sets: SPNWithCertValueParameterSet, SPNWithPasswordParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db498-136">-StartDate</span><span class="sxs-lookup"><span data-stu-id="db498-136">-StartDate</span></span>
<span data-ttu-id="db498-137">A data de início efetiva do uso da credencial.</span><span class="sxs-lookup"><span data-stu-id="db498-137">The effective start date of the credential usage.</span></span>
<span data-ttu-id="db498-138">O valor da data de início padrão é hoje.</span><span class="sxs-lookup"><span data-stu-id="db498-138">The default start date value is today.</span></span> <span data-ttu-id="db498-139">Para uma credencial de tipo "assimétrico", isso deve ser definido como ligado ou posterior à data a partir da qual o certificado X509 é válido.</span><span class="sxs-lookup"><span data-stu-id="db498-139">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db498-140">-Confirme</span><span class="sxs-lookup"><span data-stu-id="db498-140">-Confirm</span></span>
<span data-ttu-id="db498-141">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db498-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db498-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db498-142">-WhatIf</span></span>
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

### <span data-ttu-id="db498-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db498-143">CommonParameters</span></span>
<span data-ttu-id="db498-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db498-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db498-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db498-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db498-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="db498-146">INPUTS</span></span>

### <span data-ttu-id="db498-147">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="db498-147">None</span></span>
<span data-ttu-id="db498-148">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="db498-148">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="db498-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="db498-149">OUTPUTS</span></span>

### <span data-ttu-id="db498-150">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="db498-150">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="db498-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="db498-151">NOTES</span></span>

## <span data-ttu-id="db498-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="db498-152">RELATED LINKS</span></span>

[<span data-ttu-id="db498-153">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="db498-153">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

[<span data-ttu-id="db498-154">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="db498-154">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

[<span data-ttu-id="db498-155">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="db498-155">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)



