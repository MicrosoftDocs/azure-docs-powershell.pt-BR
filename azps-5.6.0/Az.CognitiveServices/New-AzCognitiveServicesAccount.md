---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: https://docs.microsoft.com/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
ms.openlocfilehash: e6ed6669c98a54a037bcbdc579e08459cdff568e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101889036"
---
# <span data-ttu-id="8b220-101">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="8b220-101">New-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="8b220-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b220-102">SYNOPSIS</span></span>
<span data-ttu-id="8b220-103">Cria uma conta dos Serviços Cognitivos.</span><span class="sxs-lookup"><span data-stu-id="8b220-103">Creates a Cognitive Services account.</span></span>

## <span data-ttu-id="8b220-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8b220-104">SYNTAX</span></span>

### <span data-ttu-id="8b220-105">CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="8b220-105">CognitiveServicesEncryption</span></span>
```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>]
 [-AssignIdentity] [-StorageAccountId <String[]>] [-CognitiveServicesEncryption]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-PublicNetworkAccess <String>]
 [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b220-106">KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="8b220-106">KeyVaultEncryption</span></span>
```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>]
 [-AssignIdentity] [-StorageAccountId <String[]>] [-KeyVaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-NetworkRuleSet <PSNetworkRuleSet>] [-PublicNetworkAccess <String>]
 [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b220-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8b220-107">DESCRIPTION</span></span>
<span data-ttu-id="8b220-108">O cmdlet **New-AzCognitiveServicesAccount** cria uma conta dos Serviços Cognitivos com o tipo especificado e o SKU.</span><span class="sxs-lookup"><span data-stu-id="8b220-108">The **New-AzCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="8b220-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8b220-109">EXAMPLES</span></span>

### <span data-ttu-id="8b220-110">1:</span><span class="sxs-lookup"><span data-stu-id="8b220-110">1:</span></span>
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

## <span data-ttu-id="8b220-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8b220-111">PARAMETERS</span></span>

### <span data-ttu-id="8b220-112">-ApiProperty</span><span class="sxs-lookup"><span data-stu-id="8b220-112">-ApiProperty</span></span>
<span data-ttu-id="8b220-113">The ApiProperties of Cognitive Services Account.</span><span class="sxs-lookup"><span data-stu-id="8b220-113">The ApiProperties of Cognitive Services Account.</span></span> <span data-ttu-id="8b220-114">Obrigatório por tipos de conta específicos.</span><span class="sxs-lookup"><span data-stu-id="8b220-114">Required by specific account types.</span></span>

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

### <span data-ttu-id="8b220-115">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="8b220-115">-AssignIdentity</span></span>
<span data-ttu-id="8b220-116">Gere e atribua uma nova Identidade de Conta de Serviços Cognitivos para essa conta de armazenamento para uso com serviços de gerenciamento importantes, como o Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="8b220-116">Generate and assign a new Cognitive Services Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="8b220-117">-CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="8b220-117">-CognitiveServicesEncryption</span></span>
<span data-ttu-id="8b220-118">Se deve definir Chaves de Criptografia de Conta dos Serviços CognitivosSource como Microsoft.CognitiveServices ou não.</span><span class="sxs-lookup"><span data-stu-id="8b220-118">Whether to set Cognitive Services Account Encryption KeySource to Microsoft.CognitiveServices or not.</span></span>

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

### <span data-ttu-id="8b220-119">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="8b220-119">-CustomSubdomainName</span></span>
<span data-ttu-id="8b220-120">Nome do subdomínio da Conta de Serviços Cognitivos.</span><span class="sxs-lookup"><span data-stu-id="8b220-120">Cognitive Services Account Subdomain Name.</span></span>

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

### <span data-ttu-id="8b220-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b220-121">-DefaultProfile</span></span>
<span data-ttu-id="8b220-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="8b220-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8b220-123">-Force</span><span class="sxs-lookup"><span data-stu-id="8b220-123">-Force</span></span>
<span data-ttu-id="8b220-124">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="8b220-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8b220-125">-KeyName</span><span class="sxs-lookup"><span data-stu-id="8b220-125">-KeyName</span></span>
<span data-ttu-id="8b220-126">Chave de criptografia de conta de serviços cognitivosSource KeyVault KeyName</span><span class="sxs-lookup"><span data-stu-id="8b220-126">Cognitive Services Account encryption keySource KeyVault KeyName</span></span>

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

### <span data-ttu-id="8b220-127">-KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="8b220-127">-KeyVaultEncryption</span></span>
<span data-ttu-id="8b220-128">Se deve definir chaves de criptografia de Conta dos Serviços CognitivosSource como Microsoft.KeyVault ou não.</span><span class="sxs-lookup"><span data-stu-id="8b220-128">Whether to set Cognitive Services Account encryption keySource to Microsoft.KeyVault or not.</span></span> <span data-ttu-id="8b220-129">Se você especificar KeyName, KeyVersion e KeyVaultUri, o Cognitive Services Account Encryption KeySource também será definido como clima Microsoft.KeyVault esse parâmetro será definido ou não.</span><span class="sxs-lookup"><span data-stu-id="8b220-129">If you specify KeyName, KeyVersion and KeyVaultUri, Cognitive Services Account Encryption KeySource will also be set to Microsoft.KeyVault weather this parameter is set or not.</span></span>

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

### <span data-ttu-id="8b220-130">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="8b220-130">-KeyVaultUri</span></span>
<span data-ttu-id="8b220-131">Chave de criptografia de conta de serviços cognitivosSource KeyVault KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="8b220-131">Cognitive Services Account encryption keySource KeyVault KeyVaultUri</span></span>

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

### <span data-ttu-id="8b220-132">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="8b220-132">-KeyVersion</span></span>
<span data-ttu-id="8b220-133">Chave de criptografia de conta de serviços cognitivosSource KeyVault KeyVersion</span><span class="sxs-lookup"><span data-stu-id="8b220-133">Cognitive Services Account encryption keySource KeyVault KeyVersion</span></span>

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

### <span data-ttu-id="8b220-134">-Location</span><span class="sxs-lookup"><span data-stu-id="8b220-134">-Location</span></span>
<span data-ttu-id="8b220-135">Especifica o local no qual criar a conta.</span><span class="sxs-lookup"><span data-stu-id="8b220-135">Specifies the location in which to create the account.</span></span>

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

### <span data-ttu-id="8b220-136">-Name</span><span class="sxs-lookup"><span data-stu-id="8b220-136">-Name</span></span>
<span data-ttu-id="8b220-137">Especifica o nome da conta.</span><span class="sxs-lookup"><span data-stu-id="8b220-137">Specifies the name for the account.</span></span>

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

### <span data-ttu-id="8b220-138">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="8b220-138">-NetworkRuleSet</span></span>
<span data-ttu-id="8b220-139">NetworkRuleSet é usado para definir um conjunto de regras de configuração para firewalls e redes virtuais, bem como para definir valores para propriedades de rede, como como lidar com solicitações que não corresponderem a nenhuma das regras definidas</span><span class="sxs-lookup"><span data-stu-id="8b220-139">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as how to handle requests that don't match any of the defined rules</span></span>

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

### <span data-ttu-id="8b220-140">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="8b220-140">-PublicNetworkAccess</span></span>
<span data-ttu-id="8b220-141">O tipo de acesso à rede para Conta de Serviços Cognitivos.</span><span class="sxs-lookup"><span data-stu-id="8b220-141">The network access type for Cognitive Services Account.</span></span>

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

### <span data-ttu-id="8b220-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b220-142">-ResourceGroupName</span></span>
<span data-ttu-id="8b220-143">Especifica o nome do grupo de recursos ao qual atribuir a conta.</span><span class="sxs-lookup"><span data-stu-id="8b220-143">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="8b220-144">O grupo de recursos já deve existir.</span><span class="sxs-lookup"><span data-stu-id="8b220-144">The resource group must already exist.</span></span>

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

### <span data-ttu-id="8b220-145">-SkuName</span><span class="sxs-lookup"><span data-stu-id="8b220-145">-SkuName</span></span>
<span data-ttu-id="8b220-146">Especifica o SKU da conta.</span><span class="sxs-lookup"><span data-stu-id="8b220-146">Specifies the SKU for the account.</span></span>
<span data-ttu-id="8b220-147">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="8b220-147">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8b220-148">F0 (camada livre)</span><span class="sxs-lookup"><span data-stu-id="8b220-148">F0 (free tier)</span></span>
- <span data-ttu-id="8b220-149">S0</span><span class="sxs-lookup"><span data-stu-id="8b220-149">S0</span></span>
- <span data-ttu-id="8b220-150">S1</span><span class="sxs-lookup"><span data-stu-id="8b220-150">S1</span></span>
- <span data-ttu-id="8b220-151">S2</span><span class="sxs-lookup"><span data-stu-id="8b220-151">S2</span></span>
- <span data-ttu-id="8b220-152">S3</span><span class="sxs-lookup"><span data-stu-id="8b220-152">S3</span></span>
- <span data-ttu-id="8b220-153">S4 Para obter mais informações, consulte [APIs do Serviço Cognitivo](https://www.microsoft.com/cognitive-services/en-us/apis).</span><span class="sxs-lookup"><span data-stu-id="8b220-153">S4 For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

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

### <span data-ttu-id="8b220-154">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="8b220-154">-StorageAccountId</span></span>
<span data-ttu-id="8b220-155">Lista de contas de armazenamento de propriedade do usuário.</span><span class="sxs-lookup"><span data-stu-id="8b220-155">List of User Owned Storage Accounts.</span></span>

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

### <span data-ttu-id="8b220-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="8b220-156">-Tag</span></span>
<span data-ttu-id="8b220-157">Especifica uma marca como um par de nome/valor.</span><span class="sxs-lookup"><span data-stu-id="8b220-157">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="8b220-158">-Type</span><span class="sxs-lookup"><span data-stu-id="8b220-158">-Type</span></span>
<span data-ttu-id="8b220-159">Especifica o tipo de conta a ser criado.</span><span class="sxs-lookup"><span data-stu-id="8b220-159">Specifies the type of account to create.</span></span> <span data-ttu-id="8b220-160">Use `Get-AzCognitiveServicesAccountType` cmdlet para obter valores aceitáveis atuais.</span><span class="sxs-lookup"><span data-stu-id="8b220-160">Use `Get-AzCognitiveServicesAccountType` cmdlet to get current acceptable values.</span></span>

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

### <span data-ttu-id="8b220-161">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8b220-161">-Confirm</span></span>
<span data-ttu-id="8b220-162">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b220-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b220-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b220-163">-WhatIf</span></span>
<span data-ttu-id="8b220-164">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8b220-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b220-165">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8b220-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b220-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b220-166">CommonParameters</span></span>
<span data-ttu-id="8b220-167">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b220-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b220-168">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8b220-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b220-169">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8b220-169">INPUTS</span></span>

### <span data-ttu-id="8b220-170">System.String</span><span class="sxs-lookup"><span data-stu-id="8b220-170">System.String</span></span>

## <span data-ttu-id="8b220-171">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8b220-171">OUTPUTS</span></span>

### <span data-ttu-id="8b220-172">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="8b220-172">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="8b220-173">NOTES</span><span class="sxs-lookup"><span data-stu-id="8b220-173">NOTES</span></span>

## <span data-ttu-id="8b220-174">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8b220-174">RELATED LINKS</span></span>

[<span data-ttu-id="8b220-175">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="8b220-175">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="8b220-176">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="8b220-176">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)

[<span data-ttu-id="8b220-177">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="8b220-177">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)
