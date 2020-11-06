---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADServicePrincipal.md
ms.openlocfilehash: ca338fd648010b9158a6bc308bb4dcb2f1c48317
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432407"
---
# <span data-ttu-id="b7561-101">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b7561-101">New-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="b7561-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b7561-102">SYNOPSIS</span></span>
<span data-ttu-id="b7561-103">Cria uma nova entidade de serviço do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b7561-103">Creates a new azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b7561-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b7561-104">SYNTAX</span></span>

### <span data-ttu-id="b7561-105">ApplicationWithoutCredentialParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="b7561-105">ApplicationWithoutCredentialParameterSet (Default)</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7561-106">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7561-106">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7561-107">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7561-107">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7561-108">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7561-108">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7561-109">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7561-109">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7561-110">DisplayNameWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7561-110">DisplayNameWithoutCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7561-111">DisplayNameWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7561-111">DisplayNameWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7561-112">DisplayNameWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7561-112">DisplayNameWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7561-113">DisplayNameWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7561-113">DisplayNameWithKeyPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7561-114">DisplayNameWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7561-114">DisplayNameWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7561-115">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b7561-115">DESCRIPTION</span></span>
<span data-ttu-id="b7561-116">Cria uma nova entidade de serviço do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b7561-116">Creates a new azure active directory service principal.</span></span>

<span data-ttu-id="b7561-117">Observação: o cmdlet também cria implicitamente um aplicativo e define suas propriedades (se a ApplicationId não for fornecida).</span><span class="sxs-lookup"><span data-stu-id="b7561-117">Note: The cmdlet also implicitly creates an application and sets its properties (if the ApplicationId is not provided).</span></span>
<span data-ttu-id="b7561-118">Para atualizar os parâmetros específicos do aplicativo, use Set-AzureRmADApplication cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7561-118">In order to update the application specific parameters please use Set-AzureRmADApplication cmdlet.</span></span>

## <span data-ttu-id="b7561-119">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b7561-119">EXAMPLES</span></span>

### <span data-ttu-id="b7561-120">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b7561-120">Example 1</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId 34a28ad2-dec4-4a41-bc3b-d22ddf90000e
```

<span data-ttu-id="b7561-121">Cria uma nova entidade de serviço do Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b7561-121">Creates a new azure active directory service principal.</span></span>

<span data-ttu-id="b7561-122">Tipo de identificação do tipo DisplayName</span><span class="sxs-lookup"><span data-stu-id="b7561-122">DisplayName                    Type                           ObjectId</span></span>
-----------                    ----                           --------
<span data-ttu-id="b7561-123">DemoApp f95b6f5c-fc98-4af0-bb8a-34a14ca1dca1</span><span class="sxs-lookup"><span data-stu-id="b7561-123">DemoApp                        ServicePrincipal               f95b6f5c-fc98-4af0-bb8a-34a14ca1dca1</span></span>

### <span data-ttu-id="b7561-124">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="b7561-124">Example 2</span></span>
```
$SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
New-AzureRmADServicePrincipal -DisplayName SPForNoExistingApp -Password $SecureStringPassword
```

<span data-ttu-id="b7561-125">Cria uma nova entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="b7561-125">Creates a new service principal.</span></span>
<span data-ttu-id="b7561-126">O cmdlet também cria implicitamente um aplicativo, uma vez que um não é fornecido.</span><span class="sxs-lookup"><span data-stu-id="b7561-126">The cmdlet also implicitly creates an application since one is not provided.</span></span>

<span data-ttu-id="b7561-127">Tipo de identificação do tipo DisplayName</span><span class="sxs-lookup"><span data-stu-id="b7561-127">DisplayName                    Type                           ObjectId</span></span>
-----------                    ----                           --------
<span data-ttu-id="b7561-128">SPForNoExistingApp 784136ca-3ae2-4fdd-A388-89d993e7c780</span><span class="sxs-lookup"><span data-stu-id="b7561-128">SPForNoExistingApp             ServicePrincipal               784136ca-3ae2-4fdd-a388-89d993e7c780</span></span>

## <span data-ttu-id="b7561-129">OS</span><span class="sxs-lookup"><span data-stu-id="b7561-129">PARAMETERS</span></span>

### <span data-ttu-id="b7561-130">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="b7561-130">-ApplicationId</span></span>
<span data-ttu-id="b7561-131">A ID do aplicativo exclusivo para uma entidade de serviço em um locatário.</span><span class="sxs-lookup"><span data-stu-id="b7561-131">The unique application id for a service principal in a tenant.</span></span>
<span data-ttu-id="b7561-132">Uma vez criado, essa propriedade não pode ser alterada.</span><span class="sxs-lookup"><span data-stu-id="b7561-132">Once created this property cannot be changed.</span></span>
<span data-ttu-id="b7561-133">Se uma ID de aplicativo não for especificada, uma será gerada.</span><span class="sxs-lookup"><span data-stu-id="b7561-133">If an application id is not specified, one will be generated.</span></span>

```yaml
Type: Guid
Parameter Sets: ApplicationWithoutCredentialParameterSet, ApplicationWithPasswordPlainParameterSet, ApplicationWithPasswordCredentialParameterSet, ApplicationWithKeyPlainParameterSet, ApplicationWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7561-134">-Certvalue</span><span class="sxs-lookup"><span data-stu-id="b7561-134">-CertValue</span></span>
<span data-ttu-id="b7561-135">O valor do tipo de credencial "assimétricod".</span><span class="sxs-lookup"><span data-stu-id="b7561-135">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="b7561-136">Ele representa o certificado codificado básico do 64.</span><span class="sxs-lookup"><span data-stu-id="b7561-136">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationWithKeyPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7561-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7561-137">-DefaultProfile</span></span>
<span data-ttu-id="b7561-138">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="b7561-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b7561-139">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b7561-139">-DisplayName</span></span>
<span data-ttu-id="b7561-140">O nome amigável da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="b7561-140">The friendly name of the service principal.</span></span>

```yaml
Type: String
Parameter Sets: DisplayNameWithoutCredentialParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithPasswordCredentialParameterSet, DisplayNameWithKeyPlainParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7561-141">-EndDate</span><span class="sxs-lookup"><span data-stu-id="b7561-141">-EndDate</span></span>
<span data-ttu-id="b7561-142">A data de término efetiva do uso da credencial.</span><span class="sxs-lookup"><span data-stu-id="b7561-142">The effective end date of the credential usage.</span></span>
<span data-ttu-id="b7561-143">O valor padrão de data de término é um ano a partir de hoje.</span><span class="sxs-lookup"><span data-stu-id="b7561-143">The default end date value is one year from today.</span></span> <span data-ttu-id="b7561-144">Para uma credencial de tipo "assimétrico", deve ser definida como at ou antes da data em que o certificado X509 é válido.</span><span class="sxs-lookup"><span data-stu-id="b7561-144">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7561-145">-Keycredentials</span><span class="sxs-lookup"><span data-stu-id="b7561-145">-KeyCredentials</span></span>
<span data-ttu-id="b7561-146">A lista de credenciais de certificado associadas à entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="b7561-146">The list of certificate credentials associated with the service principal.</span></span>

```yaml
Type: PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7561-147">-Senha</span><span class="sxs-lookup"><span data-stu-id="b7561-147">-Password</span></span>
<span data-ttu-id="b7561-148">A senha a ser associada à entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="b7561-148">The password to be associated with the service principal.</span></span>

```yaml
Type: SecureString
Parameter Sets: ApplicationWithPasswordPlainParameterSet, DisplayNameWithPasswordPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7561-149">-PasswordCredentials</span><span class="sxs-lookup"><span data-stu-id="b7561-149">-PasswordCredentials</span></span>
<span data-ttu-id="b7561-150">A lista de credenciais de senha associadas à entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="b7561-150">The list of password credentials associated with the service principal.</span></span>

```yaml
Type: PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet, DisplayNameWithPasswordCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7561-151">-StartDate</span><span class="sxs-lookup"><span data-stu-id="b7561-151">-StartDate</span></span>
<span data-ttu-id="b7561-152">A data de início efetiva do uso da credencial.</span><span class="sxs-lookup"><span data-stu-id="b7561-152">The effective start date of the credential usage.</span></span>
<span data-ttu-id="b7561-153">O valor da data de início padrão é hoje.</span><span class="sxs-lookup"><span data-stu-id="b7561-153">The default start date value is today.</span></span> <span data-ttu-id="b7561-154">Para uma credencial de tipo "assimétrico", isso deve ser definido como ligado ou posterior à data a partir da qual o certificado X509 é válido.</span><span class="sxs-lookup"><span data-stu-id="b7561-154">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b7561-155">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b7561-155">-Confirm</span></span>
<span data-ttu-id="b7561-156">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7561-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7561-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7561-157">-WhatIf</span></span>
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

### <span data-ttu-id="b7561-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7561-158">CommonParameters</span></span>
<span data-ttu-id="b7561-159">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7561-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7561-160">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7561-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7561-161">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b7561-161">INPUTS</span></span>

### <span data-ttu-id="b7561-162">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="b7561-162">None</span></span>
<span data-ttu-id="b7561-163">Esse cmdlet não aceita nenhuma entrada.</span><span class="sxs-lookup"><span data-stu-id="b7561-163">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b7561-164">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b7561-164">OUTPUTS</span></span>

### <span data-ttu-id="b7561-165">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b7561-165">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="b7561-166">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b7561-166">NOTES</span></span>
<span data-ttu-id="b7561-167">Palavras-chave: Azure, azurerm, braço, recurso, gerenciamento, gerente, recurso, grupo, modelo, implantação</span><span class="sxs-lookup"><span data-stu-id="b7561-167">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="b7561-168">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b7561-168">RELATED LINKS</span></span>

[<span data-ttu-id="b7561-169">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b7561-169">Remove-AzureRmADServicePrincipal</span></span>](./Remove-AzureRmADServicePrincipal.md)

[<span data-ttu-id="b7561-170">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b7561-170">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="b7561-171">New-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="b7561-171">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

[<span data-ttu-id="b7561-172">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="b7561-172">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="b7561-173">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="b7561-173">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

[<span data-ttu-id="b7561-174">New-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="b7561-174">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="b7561-175">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="b7561-175">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

