---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: A2B4ACC1-6F53-47DE-A2D4-831E8AC89A5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/new-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/New-AzCognitiveServicesAccount.md
ms.openlocfilehash: 713c5cb34133a233bace576ea80035b8e004eb7f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940313"
---
# <span data-ttu-id="d071d-101">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="d071d-101">New-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="d071d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d071d-102">SYNOPSIS</span></span>
<span data-ttu-id="d071d-103">Cria uma conta de serviços cognitiva.</span><span class="sxs-lookup"><span data-stu-id="d071d-103">Creates a Cognitive Services account.</span></span>

## <span data-ttu-id="d071d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d071d-104">SYNTAX</span></span>

### <span data-ttu-id="d071d-105">CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="d071d-105">CognitiveServicesEncryption</span></span>
```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>]
 [-AssignIdentity] [-StorageAccountId <String[]>] [-CognitiveServicesEncryption]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d071d-106">KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="d071d-106">KeyVaultEncryption</span></span>
```
New-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-Type] <String>
 [-SkuName] <String> [-Location] <String> [-Tag <Hashtable[]>] [-CustomSubdomainName <String>]
 [-AssignIdentity] [-StorageAccountId <String[]>] [-KeyVaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-NetworkRuleSet <PSNetworkRuleSet>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d071d-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d071d-107">DESCRIPTION</span></span>
<span data-ttu-id="d071d-108">O cmdlet **New-AzCognitiveServicesAccount** cria uma conta de serviços cognitivas com o tipo e a SKU especificados.</span><span class="sxs-lookup"><span data-stu-id="d071d-108">The **New-AzCognitiveServicesAccount** cmdlet creates a Cognitive Services account with the specified type and SKU.</span></span>

## <span data-ttu-id="d071d-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d071d-109">EXAMPLES</span></span>

### <span data-ttu-id="d071d-110">1:</span><span class="sxs-lookup"><span data-stu-id="d071d-110">1:</span></span>
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

## <span data-ttu-id="d071d-111">OS</span><span class="sxs-lookup"><span data-stu-id="d071d-111">PARAMETERS</span></span>

### <span data-ttu-id="d071d-112">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="d071d-112">-AssignIdentity</span></span>
<span data-ttu-id="d071d-113">Gerar e atribuir uma nova identidade de conta de serviços cognitiva para esta conta de armazenamento para uso com os serviços de gerenciamento de chaves como o repositório de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="d071d-113">Generate and assign a new Cognitive Services Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="d071d-114">-CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="d071d-114">-CognitiveServicesEncryption</span></span>
<span data-ttu-id="d071d-115">Se você deve definir a fonte de origem de criptografia de conta de serviços cognitiva para Microsoft. Cognitivaservices ou not.</span><span class="sxs-lookup"><span data-stu-id="d071d-115">Whether to set Cognitive Services Account Encryption KeySource to Microsoft.CognitiveServices or not.</span></span>

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

### <span data-ttu-id="d071d-116">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="d071d-116">-CustomSubdomainName</span></span>
<span data-ttu-id="d071d-117">Nome de subdomínio da conta de serviços cognitiva.</span><span class="sxs-lookup"><span data-stu-id="d071d-117">Cognitive Services Account Subdomain Name.</span></span>

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

### <span data-ttu-id="d071d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d071d-118">-DefaultProfile</span></span>
<span data-ttu-id="d071d-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="d071d-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d071d-120">-Force</span><span class="sxs-lookup"><span data-stu-id="d071d-120">-Force</span></span>
<span data-ttu-id="d071d-121">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="d071d-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d071d-122">-KeyName</span><span class="sxs-lookup"><span data-stu-id="d071d-122">-KeyName</span></span>
<span data-ttu-id="d071d-123">O KeyName do cofre da fonte de criptografia de conta de serviços cognitiva</span><span class="sxs-lookup"><span data-stu-id="d071d-123">Cognitive Services Account encryption keySource KeyVault KeyName</span></span>

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

### <span data-ttu-id="d071d-124">-KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="d071d-124">-KeyVaultEncryption</span></span>
<span data-ttu-id="d071d-125">Se você deve definir a fonte de origem de criptografia de conta de serviços cognitiva para a Microsoft. keyvault ou não.</span><span class="sxs-lookup"><span data-stu-id="d071d-125">Whether to set Cognitive Services Account encryption keySource to Microsoft.KeyVault or not.</span></span> <span data-ttu-id="d071d-126">Se você especificar a KeyName, a keyversion e o KeyVaultUri, a origem de criptografia da conta de serviços cognitiva também será definida como Microsoft. Weather Weather esse parâmetro está definido ou não.</span><span class="sxs-lookup"><span data-stu-id="d071d-126">If you specify KeyName, KeyVersion and KeyVaultUri, Cognitive Services Account Encryption KeySource will also be set to Microsoft.KeyVault weather this parameter is set or not.</span></span>

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

### <span data-ttu-id="d071d-127">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="d071d-127">-KeyVaultUri</span></span>
<span data-ttu-id="d071d-128">KeyVaultUri de uma fonte de código de criptografia de conta de serviços cognitiva</span><span class="sxs-lookup"><span data-stu-id="d071d-128">Cognitive Services Account encryption keySource KeyVault KeyVaultUri</span></span>

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

### <span data-ttu-id="d071d-129">-Keyversion</span><span class="sxs-lookup"><span data-stu-id="d071d-129">-KeyVersion</span></span>
<span data-ttu-id="d071d-130">Subversão do cofre de conta de criptografia de conta de serviços cognitiva</span><span class="sxs-lookup"><span data-stu-id="d071d-130">Cognitive Services Account encryption keySource KeyVault KeyVersion</span></span>

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

### <span data-ttu-id="d071d-131">-Local</span><span class="sxs-lookup"><span data-stu-id="d071d-131">-Location</span></span>
<span data-ttu-id="d071d-132">Especifica o local no qual criar a conta.</span><span class="sxs-lookup"><span data-stu-id="d071d-132">Specifies the location in which to create the account.</span></span>

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

### <span data-ttu-id="d071d-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="d071d-133">-Name</span></span>
<span data-ttu-id="d071d-134">Especifica o nome da conta.</span><span class="sxs-lookup"><span data-stu-id="d071d-134">Specifies the name for the account.</span></span>

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

### <span data-ttu-id="d071d-135">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="d071d-135">-NetworkRuleSet</span></span>
<span data-ttu-id="d071d-136">NetworkRuleSet é usado para definir um conjunto de regras de configuração para firewalls e redes virtuais, bem como para definir valores para propriedades de rede, como manipular solicitações que não correspondem a nenhuma das regras definidas</span><span class="sxs-lookup"><span data-stu-id="d071d-136">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as how to handle requests that don't match any of the defined rules</span></span>

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

### <span data-ttu-id="d071d-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d071d-137">-ResourceGroupName</span></span>
<span data-ttu-id="d071d-138">Especifica o nome do grupo de recursos ao qual a conta será atribuída.</span><span class="sxs-lookup"><span data-stu-id="d071d-138">Specifies the name of the resource group to which to assign the account.</span></span>
<span data-ttu-id="d071d-139">O grupo de recursos já deve existir.</span><span class="sxs-lookup"><span data-stu-id="d071d-139">The resource group must already exist.</span></span>

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

### <span data-ttu-id="d071d-140">-SkuName</span><span class="sxs-lookup"><span data-stu-id="d071d-140">-SkuName</span></span>
<span data-ttu-id="d071d-141">Especifica a SKU da conta.</span><span class="sxs-lookup"><span data-stu-id="d071d-141">Specifies the SKU for the account.</span></span>
<span data-ttu-id="d071d-142">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="d071d-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d071d-143">F0 (nível gratuito)</span><span class="sxs-lookup"><span data-stu-id="d071d-143">F0 (free tier)</span></span>
- <span data-ttu-id="d071d-144">S0</span><span class="sxs-lookup"><span data-stu-id="d071d-144">S0</span></span>
- <span data-ttu-id="d071d-145">Eles</span><span class="sxs-lookup"><span data-stu-id="d071d-145">S1</span></span>
- <span data-ttu-id="d071d-146">S2</span><span class="sxs-lookup"><span data-stu-id="d071d-146">S2</span></span>
- <span data-ttu-id="d071d-147">S3</span><span class="sxs-lookup"><span data-stu-id="d071d-147">S3</span></span>
- <span data-ttu-id="d071d-148">S4 para obter mais informações, consulte [APIs de serviço cognitiva](https://www.microsoft.com/cognitive-services/en-us/apis).</span><span class="sxs-lookup"><span data-stu-id="d071d-148">S4 For more information, see [Cognitive Service APIs](https://www.microsoft.com/cognitive-services/en-us/apis).</span></span>

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

### <span data-ttu-id="d071d-149">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="d071d-149">-StorageAccountId</span></span>
<span data-ttu-id="d071d-150">Lista de contas de armazenamento pertencentes ao usuário.</span><span class="sxs-lookup"><span data-stu-id="d071d-150">List of User Owned Storage Accounts.</span></span>

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

### <span data-ttu-id="d071d-151">-Marca</span><span class="sxs-lookup"><span data-stu-id="d071d-151">-Tag</span></span>
<span data-ttu-id="d071d-152">Especifica uma marca como um par de nome/valor.</span><span class="sxs-lookup"><span data-stu-id="d071d-152">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="d071d-153">-Digite</span><span class="sxs-lookup"><span data-stu-id="d071d-153">-Type</span></span>
<span data-ttu-id="d071d-154">Especifica o tipo de conta a ser criada.</span><span class="sxs-lookup"><span data-stu-id="d071d-154">Specifies the type of account to create.</span></span> <span data-ttu-id="d071d-155">Use o `Get-AzCognitiveServicesAccountType` cmdlet para obter os valores aceitáveis atuais.</span><span class="sxs-lookup"><span data-stu-id="d071d-155">Use `Get-AzCognitiveServicesAccountType` cmdlet to get current acceptable values.</span></span>

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

### <span data-ttu-id="d071d-156">-Confirme</span><span class="sxs-lookup"><span data-stu-id="d071d-156">-Confirm</span></span>
<span data-ttu-id="d071d-157">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d071d-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d071d-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d071d-158">-WhatIf</span></span>
<span data-ttu-id="d071d-159">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d071d-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d071d-160">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d071d-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d071d-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d071d-161">CommonParameters</span></span>
<span data-ttu-id="d071d-162">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d071d-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d071d-163">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d071d-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d071d-164">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d071d-164">INPUTS</span></span>

### <span data-ttu-id="d071d-165">System. String</span><span class="sxs-lookup"><span data-stu-id="d071d-165">System.String</span></span>

## <span data-ttu-id="d071d-166">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d071d-166">OUTPUTS</span></span>

### <span data-ttu-id="d071d-167">Microsoft. Azure. Commands. Management. Cognitivaservices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="d071d-167">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="d071d-168">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d071d-168">NOTES</span></span>

## <span data-ttu-id="d071d-169">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d071d-169">RELATED LINKS</span></span>

[<span data-ttu-id="d071d-170">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="d071d-170">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="d071d-171">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="d071d-171">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)

[<span data-ttu-id="d071d-172">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="d071d-172">Set-AzCognitiveServicesAccount</span></span>](./Set-AzCognitiveServicesAccount.md)
