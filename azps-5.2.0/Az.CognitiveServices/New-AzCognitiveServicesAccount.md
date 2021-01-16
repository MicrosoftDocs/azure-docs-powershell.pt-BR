---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
ms.openlocfilehash: 0c7e22174b0306a3b9b5a37bd99edeb06f124334
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98259480"
---
# <span data-ttu-id="72900-101">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="72900-101">New-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="72900-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="72900-102">SYNOPSIS</span></span>
<span data-ttu-id="72900-103">Cria uma conta de serviços cognitiva.</span><span class="sxs-lookup"><span data-stu-id="72900-103">Creates a Cognitive Services account.</span></span>

## <span data-ttu-id="72900-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="72900-104">SYNTAX</span></span>

### <span data-ttu-id="72900-105">CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="72900-105">CognitiveServicesEncryption</span></span>
```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>]
 [-AssignIdentity] [-StorageAccountId <String[]>] [-CognitiveServicesEncryption]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-PublicNetworkAccess <String>]
 [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="72900-106">KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="72900-106">KeyVaultEncryption</span></span>
```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>]
 [-AssignIdentity] [-StorageAccountId <String[]>] [-KeyVaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-NetworkRuleSet <PSNetworkRuleSet>] [-PublicNetworkAccess <String>]
 [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72900-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="72900-107">DESCRIPTION</span></span>
<span data-ttu-id="72900-108">O cmdlet **New-AzCognitiveServicesAccount** cria uma conta de serviços cognitivas com o tipo e a SKU especificados.</span><span class="sxs-lookup"><span data-stu-id="72900-108">The **New-AzCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="72900-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="72900-109">EXAMPLES</span></span>

### <span data-ttu-id="72900-110">1:</span><span class="sxs-lookup"><span data-stu-id="72900-110">1:</span></span>
```
PS C:\> New-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -Type LUIS -SkuName S0 -Locatio
n 'WestUS'


ResourceGroupName : cognitive-services-resource-group
AccountName       : myluis
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/cognitive-services-resource-group/providers/Microsoft.Cog
                    nitiveServices/accounts/myluis
Endpoint          : https://westus.api.cognitive.microsoft.com/luis/v2.0
Location          : WestUS
Sku               : Microsoft.Azure.Management.CognitiveServices.Models.Sku
AccountType       : LUIS
ResourceType      : Microsoft.CognitiveServices/accounts
Etag              : "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
ProvisioningState : Succeeded
Tags              :
```

## <span data-ttu-id="72900-111">OS</span><span class="sxs-lookup"><span data-stu-id="72900-111">PARAMETERS</span></span>

### <span data-ttu-id="72900-112">-ApiProperty</span><span class="sxs-lookup"><span data-stu-id="72900-112">-ApiProperty</span></span>
<span data-ttu-id="72900-113">O ApiProperties de uma conta de serviços cognitiva.</span><span class="sxs-lookup"><span data-stu-id="72900-113">The ApiProperties of Cognitive Services Account.</span></span> <span data-ttu-id="72900-114">Exigido por tipos específicos de conta.</span><span class="sxs-lookup"><span data-stu-id="72900-114">Required by specific account types.</span></span>

```yaml
Type: Microsoft.Azure.Management.CognitiveServices.Models.CognitiveServicesAccountApiProperties
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72900-115">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="72900-115">-AssignIdentity</span></span>
<span data-ttu-id="72900-116">Gerar e atribuir uma nova identidade de conta de serviços cognitiva para esta conta de armazenamento para uso com os serviços de gerenciamento de chaves como o repositório de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="72900-116">Generate and assign a new Cognitive Services Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72900-117">-CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="72900-117">-CognitiveServicesEncryption</span></span>
<span data-ttu-id="72900-118">Se você deve definir a fonte de origem de criptografia de conta de serviços cognitiva para Microsoft. Cognitivaservices ou not.</span><span class="sxs-lookup"><span data-stu-id="72900-118">Whether to set Cognitive Services Account Encryption KeySource to Microsoft.CognitiveServices or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CognitiveServicesEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72900-119">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="72900-119">-CustomSubdomainName</span></span>
<span data-ttu-id="72900-120">Nome de subdomínio da conta de serviços cognitiva.</span><span class="sxs-lookup"><span data-stu-id="72900-120">Cognitive Services Account Subdomain Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72900-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72900-121">-DefaultProfile</span></span>
<span data-ttu-id="72900-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="72900-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72900-123">-Force</span><span class="sxs-lookup"><span data-stu-id="72900-123">-Force</span></span>
<span data-ttu-id="72900-124">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="72900-124">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72900-125">-KeyName</span><span class="sxs-lookup"><span data-stu-id="72900-125">-KeyName</span></span>
<span data-ttu-id="72900-126">O KeyName do cofre da fonte de criptografia de conta de serviços cognitiva</span><span class="sxs-lookup"><span data-stu-id="72900-126">Cognitive Services Account encryption keySource KeyVault KeyName</span></span>

```yaml
Type: System.String
Parameter Sets: KeyVaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72900-127">-KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="72900-127">-KeyVaultEncryption</span></span>
<span data-ttu-id="72900-128">Se você deve definir a fonte de origem de criptografia de conta de serviços cognitiva para a Microsoft. keyvault ou não.</span><span class="sxs-lookup"><span data-stu-id="72900-128">Whether to set Cognitive Services Account encryption keySource to Microsoft.KeyVault or not.</span></span> <span data-ttu-id="72900-129">Se você especificar a KeyName, a keyversion e o KeyVaultUri, a origem de criptografia da conta de serviços cognitiva também será definida como Microsoft. Weather Weather esse parâmetro está definido ou não.</span><span class="sxs-lookup"><span data-stu-id="72900-129">If you specify KeyName, KeyVersion and KeyVaultUri, Cognitive Services Account Encryption KeySource will also be set to Microsoft.KeyVault weather this parameter is set or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: KeyVaultEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72900-130">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="72900-130">-KeyVaultUri</span></span>
<span data-ttu-id="72900-131">KeyVaultUri de uma fonte de código de criptografia de conta de serviços cognitiva</span><span class="sxs-lookup"><span data-stu-id="72900-131">Cognitive Services Account encryption keySource KeyVault KeyVaultUri</span></span>

```yaml
Type: System.String
Parameter Sets: KeyVaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72900-132">-Keyversion</span><span class="sxs-lookup"><span data-stu-id="72900-132">-KeyVersion</span></span>
<span data-ttu-id="72900-133">Subversão do cofre de conta de criptografia de conta de serviços cognitiva</span><span class="sxs-lookup"><span data-stu-id="72900-133">Cognitive Services Account encryption keySource KeyVault KeyVersion</span></span>

```yaml
Type: System.String
Parameter Sets: KeyVaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72900-134">-Local</span><span class="sxs-lookup"><span data-stu-id="72900-134">-Location</span></span>
<span data-ttu-id="72900-135">Especifica o local no qual criar a conta.</span><span class="sxs-lookup"><span data-stu-id="72900-135">Specifies the location in which to create the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72900-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="72900-136">-Name</span></span>
<span data-ttu-id="72900-137">Especifica o nome da conta.</span><span class="sxs-lookup"><span data-stu-id="72900-137">Specifies the name for the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72900-138">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="72900-138">-NetworkRuleSet</span></span>
<span data-ttu-id="72900-139">NetworkRuleSet é usado para definir um conjunto de regras de configuração para firewalls e redes virtuais, bem como para definir valores para propriedades de rede, como manipular solicitações que não correspondem a nenhuma das regras definidas</span><span class="sxs-lookup"><span data-stu-id="72900-139">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as how to handle requests that don't match any of the defined rules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72900-140">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="72900-140">-PublicNetworkAccess</span></span>
<span data-ttu-id="72900-141">O tipo de acesso à rede para a conta de serviços cognitiva.</span><span class="sxs-lookup"><span data-stu-id="72900-141">The network access type for Cognitive Services Account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72900-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72900-142">-ResourceGroupName</span></span>
<span data-ttu-id="72900-143">Especifica o nome do grupo de recursos ao qual a conta será atribuída.</span><span class="sxs-lookup"><span data-stu-id="72900-143">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="72900-144">O grupo de recursos já deve existir.</span><span class="sxs-lookup"><span data-stu-id="72900-144">The resource group must already exist.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72900-145">-SkuName</span><span class="sxs-lookup"><span data-stu-id="72900-145">-SkuName</span></span>
<span data-ttu-id="72900-146">Especifica a SKU da conta.</span><span class="sxs-lookup"><span data-stu-id="72900-146">Specifies the SKU for the account.</span></span>
<span data-ttu-id="72900-147">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="72900-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="72900-148">F0 (nível gratuito)</span><span class="sxs-lookup"><span data-stu-id="72900-148">F0 (free tier)</span></span>
- <span data-ttu-id="72900-149">S0</span><span class="sxs-lookup"><span data-stu-id="72900-149">S0</span></span>
- <span data-ttu-id="72900-150">Eles</span><span class="sxs-lookup"><span data-stu-id="72900-150">S1</span></span>
- <span data-ttu-id="72900-151">S2</span><span class="sxs-lookup"><span data-stu-id="72900-151">S2</span></span>
- <span data-ttu-id="72900-152">S3</span><span class="sxs-lookup"><span data-stu-id="72900-152">S3</span></span>
- <span data-ttu-id="72900-153">S4 para obter mais informações, consulte [APIs de serviço cognitiva](https://www.microsoft.com/cognitive-services/en-us/apis).</span><span class="sxs-lookup"><span data-stu-id="72900-153">S4 For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72900-154">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="72900-154">-StorageAccountId</span></span>
<span data-ttu-id="72900-155">Lista de contas de armazenamento pertencentes ao usuário.</span><span class="sxs-lookup"><span data-stu-id="72900-155">List of User Owned Storage Accounts.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72900-156">-Marca</span><span class="sxs-lookup"><span data-stu-id="72900-156">-Tag</span></span>
<span data-ttu-id="72900-157">Especifica uma marca como um par de nome/valor.</span><span class="sxs-lookup"><span data-stu-id="72900-157">Specifies a tag as a name/value pair.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72900-158">-Digite</span><span class="sxs-lookup"><span data-stu-id="72900-158">-Type</span></span>
<span data-ttu-id="72900-159">Especifica o tipo de conta a ser criada.</span><span class="sxs-lookup"><span data-stu-id="72900-159">Specifies the type of account to create.</span></span> <span data-ttu-id="72900-160">Use o `Get-AzCognitiveServicesAccountType` cmdlet para obter os valores aceitáveis atuais.</span><span class="sxs-lookup"><span data-stu-id="72900-160">Use `Get-AzCognitiveServicesAccountType` cmdlet to get current acceptable values.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountType, AccountType, Kind

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72900-161">-Confirme</span><span class="sxs-lookup"><span data-stu-id="72900-161">-Confirm</span></span>
<span data-ttu-id="72900-162">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72900-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72900-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72900-163">-WhatIf</span></span>
<span data-ttu-id="72900-164">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="72900-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72900-165">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="72900-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72900-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72900-166">CommonParameters</span></span>
<span data-ttu-id="72900-167">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72900-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72900-168">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="72900-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72900-169">SENSORES</span><span class="sxs-lookup"><span data-stu-id="72900-169">INPUTS</span></span>

### <span data-ttu-id="72900-170">System. String</span><span class="sxs-lookup"><span data-stu-id="72900-170">System.String</span></span>

## <span data-ttu-id="72900-171">EXIBE</span><span class="sxs-lookup"><span data-stu-id="72900-171">OUTPUTS</span></span>

### <span data-ttu-id="72900-172">Microsoft. Azure. Commands. Management. Cognitivaservices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="72900-172">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="72900-173">INFORMA</span><span class="sxs-lookup"><span data-stu-id="72900-173">NOTES</span></span>

## <span data-ttu-id="72900-174">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="72900-174">RELATED LINKS</span></span>

[<span data-ttu-id="72900-175">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="72900-175">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="72900-176">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="72900-176">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)

[<span data-ttu-id="72900-177">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="72900-177">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)
