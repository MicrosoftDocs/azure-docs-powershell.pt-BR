---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 98836BC0-AB4F-4F24-88BE-E7DD350B71E8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADAppCredential.md
ms.openlocfilehash: 15b3e3fd90a7bacf87062bc12269ca2853276370
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93440965"
---
# <span data-ttu-id="2c001-101">New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="2c001-101">New-AzureRmADAppCredential</span></span>

## <span data-ttu-id="2c001-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2c001-102">SYNOPSIS</span></span>
<span data-ttu-id="2c001-103">Adiciona uma credencial a um aplicativo existente.</span><span class="sxs-lookup"><span data-stu-id="2c001-103">Adds a credential to an existing application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c001-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2c001-104">SYNTAX</span></span>

### <span data-ttu-id="2c001-105">ApplicationObjectIdWithPasswordParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="2c001-105">ApplicationObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzureRmADAppCredential -ObjectId <String> -Password <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c001-106">ApplicationObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c001-106">ApplicationObjectIdWithCertValueParameterSet</span></span>
```
New-AzureRmADAppCredential -ObjectId <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c001-107">ApplicationIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c001-107">ApplicationIdWithCertValueParameterSet</span></span>
```
New-AzureRmADAppCredential -ApplicationId <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c001-108">ApplicationIdWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="2c001-108">ApplicationIdWithPasswordParameterSet</span></span>
```
New-AzureRmADAppCredential -ApplicationId <String> -Password <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c001-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2c001-109">DESCRIPTION</span></span>
<span data-ttu-id="2c001-110">O cmdlet New-AzureRmADAppCredential pode ser usado para adicionar uma nova credencial ou para rolar credenciais para um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2c001-110">The New-AzureRmADAppCredential cmdlet can be used to add a new credential or to roll credentials for an application.</span></span>
<span data-ttu-id="2c001-111">O aplicativo é identificado fornecendo a identificação do objeto do aplicativo ou a ID do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2c001-111">The application is identified by supplying either the application object id or application Id.</span></span>

## <span data-ttu-id="2c001-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2c001-112">EXAMPLES</span></span>

### <span data-ttu-id="2c001-113">--------------------------Exemplo 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="2c001-113">--------------------------  Example 1  --------------------------</span></span>
```
PS E:\> New-AzureRmADAppCredential -ObjectId 1f89cf81-0146-4f4e-beae-2007d0668416 -Password P@ssw0rd!
```

<span data-ttu-id="2c001-114">Uma nova credencial de senha é adicionada a um aplicativo existente.</span><span class="sxs-lookup"><span data-stu-id="2c001-114">A new password credential is added to an existing application.</span></span>
<span data-ttu-id="2c001-115">Neste exemplo, o valor de senha fornecido é adicionado ao aplicativo usando a ID do objeto de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2c001-115">In this example, the supplied password value is added to the application using the application object id.</span></span>

### <span data-ttu-id="2c001-116">--------------------------Exemplo 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="2c001-116">--------------------------  Example 2  --------------------------</span></span>
```
$cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate 

$cer.Import("C:\myapp.cer") 

$binCert = $cer.GetRawCertData() 

$credValue = [System.Convert]::ToBase64String($binCert)

PS E:\> New-AzureRmADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 -CertValue $credValue -StartDate $cer.GetEffectiveDateString() -EndDate $cer.GetExpirationDateString()
```

<span data-ttu-id="2c001-117">Uma nova credencial de chave é adicionada a um aplicativo existente.</span><span class="sxs-lookup"><span data-stu-id="2c001-117">A new key credential is added to an existing application.</span></span>
<span data-ttu-id="2c001-118">Neste exemplo, o certificado X509 público codificado em base64 fornecido ("MyApp. cer") é adicionado ao aplicativo usando a applicationId.</span><span class="sxs-lookup"><span data-stu-id="2c001-118">In this example, the supplied base64 encoded public X509 certificate ("myapp.cer") is added to the application using the applicationId.</span></span>

### <span data-ttu-id="2c001-119">--------------------------Exemplo 3--------------------------</span><span class="sxs-lookup"><span data-stu-id="2c001-119">--------------------------  Example 3  --------------------------</span></span>
```
PS E:\> New-AzureRmADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 -CertValue $credValue
```

## <span data-ttu-id="2c001-120">OS</span><span class="sxs-lookup"><span data-stu-id="2c001-120">PARAMETERS</span></span>

### <span data-ttu-id="2c001-121">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="2c001-121">-ApplicationId</span></span>
<span data-ttu-id="2c001-122">A ID do aplicativo para o qual adicionar as credenciais.</span><span class="sxs-lookup"><span data-stu-id="2c001-122">The id of the application to add the credentials to.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationIdWithCertValueParameterSet, ApplicationIdWithPasswordParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c001-123">-Certvalue</span><span class="sxs-lookup"><span data-stu-id="2c001-123">-CertValue</span></span>
<span data-ttu-id="2c001-124">O valor do tipo de credencial "assimétricod".</span><span class="sxs-lookup"><span data-stu-id="2c001-124">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="2c001-125">Ele representa o certificado codificado básico do 64.</span><span class="sxs-lookup"><span data-stu-id="2c001-125">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="2c001-126">-EndDate</span><span class="sxs-lookup"><span data-stu-id="2c001-126">-EndDate</span></span>
<span data-ttu-id="2c001-127">A data de término efetiva do uso da credencial.</span><span class="sxs-lookup"><span data-stu-id="2c001-127">The effective end date of the credential usage.</span></span>
<span data-ttu-id="2c001-128">O valor padrão de data de término é um ano a partir de hoje.</span><span class="sxs-lookup"><span data-stu-id="2c001-128">The default end date value is one year from today.</span></span> <span data-ttu-id="2c001-129">Para uma credencial de tipo "assimétrico", deve ser definida como at ou antes da data em que o certificado X509 é válido.</span><span class="sxs-lookup"><span data-stu-id="2c001-129">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="2c001-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="2c001-130">-ObjectId</span></span>
<span data-ttu-id="2c001-131">A ID do objeto do aplicativo para o qual adicionar as credenciais.</span><span class="sxs-lookup"><span data-stu-id="2c001-131">The object id of the application to add the credentials to.</span></span>

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

### <span data-ttu-id="2c001-132">-Senha</span><span class="sxs-lookup"><span data-stu-id="2c001-132">-Password</span></span>
<span data-ttu-id="2c001-133">A senha a ser associada ao aplicativo.</span><span class="sxs-lookup"><span data-stu-id="2c001-133">The password to be associated with the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithPasswordParameterSet, ApplicationIdWithPasswordParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c001-134">-StartDate</span><span class="sxs-lookup"><span data-stu-id="2c001-134">-StartDate</span></span>
<span data-ttu-id="2c001-135">A data de início efetiva do uso da credencial.</span><span class="sxs-lookup"><span data-stu-id="2c001-135">The effective start date of the credential usage.</span></span>
<span data-ttu-id="2c001-136">O valor da data de início padrão é hoje.</span><span class="sxs-lookup"><span data-stu-id="2c001-136">The default start date value is today.</span></span>
<span data-ttu-id="2c001-137">Para uma credencial de tipo "assimétrico", isso deve ser definido como ligado ou posterior à data a partir da qual o certificado X509 é válido.</span><span class="sxs-lookup"><span data-stu-id="2c001-137">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="2c001-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="2c001-138">-Confirm</span></span>
<span data-ttu-id="2c001-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c001-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c001-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c001-140">-WhatIf</span></span>
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

### <span data-ttu-id="2c001-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c001-141">-DefaultProfile</span></span>
<span data-ttu-id="2c001-142">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2c001-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c001-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c001-143">CommonParameters</span></span>
<span data-ttu-id="2c001-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c001-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c001-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c001-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c001-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2c001-146">INPUTS</span></span>

## <span data-ttu-id="2c001-147">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2c001-147">OUTPUTS</span></span>

### <span data-ttu-id="2c001-148">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="2c001-148">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="2c001-149">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2c001-149">NOTES</span></span>

## <span data-ttu-id="2c001-150">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2c001-150">RELATED LINKS</span></span>

[<span data-ttu-id="2c001-151">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="2c001-151">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="2c001-152">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="2c001-152">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="2c001-153">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="2c001-153">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

