---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 11E2D82A-1DF1-4E19-8328-44674641D1BB
online version: https://docs.microsoft.com/powershell/module/az.cognitiveservices/set-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
ms.openlocfilehash: 2c995157b56bafb56df7b385c250b6f7c4fdd4e0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890477"
---
# <span data-ttu-id="c120b-101">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="c120b-101">Set-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="c120b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c120b-102">SYNOPSIS</span></span>
<span data-ttu-id="c120b-103">Modifica uma conta.</span><span class="sxs-lookup"><span data-stu-id="c120b-103">Modifies an account.</span></span>

## <span data-ttu-id="c120b-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="c120b-104">SYNTAX</span></span>

### <span data-ttu-id="c120b-105">CognitiveServicesEncryption (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c120b-105">CognitiveServicesEncryption (Default)</span></span>
```
Set-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-AssignIdentity] [-IdentityType <IdentityType>]
 [-StorageAccountId <String[]>] [-CognitiveServicesEncryption] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-PublicNetworkAccess <String>] [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c120b-106">KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="c120b-106">KeyVaultEncryption</span></span>
```
Set-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-AssignIdentity] [-IdentityType <IdentityType>]
 [-StorageAccountId <String[]>] [-KeyVaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-NetworkRuleSet <PSNetworkRuleSet>] [-PublicNetworkAccess <String>]
 [-ApiProperty <CognitiveServicesAccountApiProperties>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c120b-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="c120b-107">DESCRIPTION</span></span>
<span data-ttu-id="c120b-108">O cmdlet **Set-AzCognitiveServicesAccount** modifica a SKU ou as marcas da conta de Serviços Cognitivos especificada.</span><span class="sxs-lookup"><span data-stu-id="c120b-108">The **Set-AzCognitiveServicesAccount** cmdlet modifies the SKU or tags of the specified Cognitive Services account.</span></span>

## <span data-ttu-id="c120b-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c120b-109">EXAMPLES</span></span>

### <span data-ttu-id="c120b-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c120b-110">Example 1</span></span>
```powershell
PS C:\> Set-AzCognitiveServicesAccount -ResourceGroupName cognitive-services-resource-group -name myluis -SkuName S0


ResourceGroupName : cognitive-services-resource-group
AccountName       : myluis
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/cognitive-services-resource-group/providers/Microsoft.Cog
                    nitiveServices/accounts/myluis
Endpoint          : https://westus.api.cognitive.microsoft.com/luis/v2.0
Location          : WESTUS
Sku               : Microsoft.Azure.Management.CognitiveServices.Models.Sku
AccountType       : LUIS
ResourceType      : Microsoft.CognitiveServices/accounts
Etag              : "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"
ProvisioningState : Succeeded
Tags              :
```

## <span data-ttu-id="c120b-111">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="c120b-111">PARAMETERS</span></span>

### <span data-ttu-id="c120b-112">-ApiProperty</span><span class="sxs-lookup"><span data-stu-id="c120b-112">-ApiProperty</span></span>
<span data-ttu-id="c120b-113">The ApiProperties of Cognitive Services Account.</span><span class="sxs-lookup"><span data-stu-id="c120b-113">The ApiProperties of Cognitive Services Account.</span></span> <span data-ttu-id="c120b-114">Obrigatório por tipos de conta específicos.</span><span class="sxs-lookup"><span data-stu-id="c120b-114">Required by specific account types.</span></span>

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

### <span data-ttu-id="c120b-115">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="c120b-115">-AssignIdentity</span></span>
<span data-ttu-id="c120b-116">Gere e atribua uma nova Identidade de Conta de Serviços Cognitivos para essa conta de armazenamento para uso com serviços de gerenciamento importantes, como o Azure KeyVault.</span><span class="sxs-lookup"><span data-stu-id="c120b-116">Generate and assign a new Cognitive Services Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="c120b-117">-CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="c120b-117">-CognitiveServicesEncryption</span></span>
<span data-ttu-id="c120b-118">Se deve definir Chaves de Criptografia de Conta dos Serviços CognitivosSource como Microsoft.CognitiveServices ou não.</span><span class="sxs-lookup"><span data-stu-id="c120b-118">Whether to set Cognitive Services Account Encryption KeySource to Microsoft.CognitiveServices or not.</span></span>

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

### <span data-ttu-id="c120b-119">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="c120b-119">-CustomSubdomainName</span></span>
<span data-ttu-id="c120b-120">Nome do subdomínio da Conta de Serviços Cognitivos.</span><span class="sxs-lookup"><span data-stu-id="c120b-120">Cognitive Services Account Subdomain Name.</span></span>

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

### <span data-ttu-id="c120b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c120b-121">-DefaultProfile</span></span>
<span data-ttu-id="c120b-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="c120b-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c120b-123">-Force</span><span class="sxs-lookup"><span data-stu-id="c120b-123">-Force</span></span>
<span data-ttu-id="c120b-124">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="c120b-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c120b-125">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="c120b-125">-IdentityType</span></span>
<span data-ttu-id="c120b-126">Tipo de identidade de serviço gerenciado.</span><span class="sxs-lookup"><span data-stu-id="c120b-126">Type of managed service identity.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.CognitiveServices.Models.IdentityType]
Parameter Sets: (All)
Aliases:
Accepted values: None, SystemAssigned, UserAssigned

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c120b-127">-KeyName</span><span class="sxs-lookup"><span data-stu-id="c120b-127">-KeyName</span></span>
<span data-ttu-id="c120b-128">Chave de criptografia de conta de serviços cognitivosSource KeyVault KeyName</span><span class="sxs-lookup"><span data-stu-id="c120b-128">Cognitive Services Account encryption keySource KeyVault KeyName</span></span>

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

### <span data-ttu-id="c120b-129">-KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="c120b-129">-KeyVaultEncryption</span></span>
<span data-ttu-id="c120b-130">Se deve definir chaves de criptografia de Conta dos Serviços CognitivosSource como Microsoft.KeyVault ou não.</span><span class="sxs-lookup"><span data-stu-id="c120b-130">Whether to set Cognitive Services Account encryption keySource to Microsoft.KeyVault or not.</span></span> <span data-ttu-id="c120b-131">Se você especificar KeyName, KeyVersion e KeyVaultUri, o Cognitive Services Account Encryption KeySource também será definido como clima Microsoft.KeyVault esse parâmetro será definido ou não.</span><span class="sxs-lookup"><span data-stu-id="c120b-131">If you specify KeyName, KeyVersion and KeyVaultUri, Cognitive Services Account Encryption KeySource will also be set to Microsoft.KeyVault weather this parameter is set or not.</span></span>

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

### <span data-ttu-id="c120b-132">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="c120b-132">-KeyVaultUri</span></span>
<span data-ttu-id="c120b-133">Chave de criptografia de conta de serviços cognitivosSource KeyVault KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="c120b-133">Cognitive Services Account encryption keySource KeyVault KeyVaultUri</span></span>

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

### <span data-ttu-id="c120b-134">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="c120b-134">-KeyVersion</span></span>
<span data-ttu-id="c120b-135">Chave de criptografia de conta de serviços cognitivosSource KeyVault KeyVersion</span><span class="sxs-lookup"><span data-stu-id="c120b-135">Cognitive Services Account encryption keySource KeyVault KeyVersion</span></span>

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

### <span data-ttu-id="c120b-136">-Name</span><span class="sxs-lookup"><span data-stu-id="c120b-136">-Name</span></span>
<span data-ttu-id="c120b-137">Especifica o nome da conta a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="c120b-137">Specifies the name of the account to modify.</span></span>

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

### <span data-ttu-id="c120b-138">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="c120b-138">-NetworkRuleSet</span></span>
<span data-ttu-id="c120b-139">NetworkRuleSet é usado para definir um conjunto de regras de configuração para firewalls e redes virtuais, bem como para definir valores para propriedades de rede, como como lidar com solicitações que não corresponderem a nenhuma das regras definidas</span><span class="sxs-lookup"><span data-stu-id="c120b-139">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as how to handle requests that don't match any of the defined rules</span></span>

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

### <span data-ttu-id="c120b-140">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="c120b-140">-PublicNetworkAccess</span></span>
<span data-ttu-id="c120b-141">O tipo de acesso à rede para Conta de Serviços Cognitivos.</span><span class="sxs-lookup"><span data-stu-id="c120b-141">The network access type for Cognitive Services Account.</span></span>

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

### <span data-ttu-id="c120b-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c120b-142">-ResourceGroupName</span></span>
<span data-ttu-id="c120b-143">Especifica o nome do grupo de recursos ao que a conta é atribuída.</span><span class="sxs-lookup"><span data-stu-id="c120b-143">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="c120b-144">-SkuName</span><span class="sxs-lookup"><span data-stu-id="c120b-144">-SkuName</span></span>
<span data-ttu-id="c120b-145">Especifica o SKU da conta.</span><span class="sxs-lookup"><span data-stu-id="c120b-145">Specifies the SKU for the account.</span></span>
<span data-ttu-id="c120b-146">Os valores aceitáveis para este parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="c120b-146">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c120b-147">F0 (camada livre)</span><span class="sxs-lookup"><span data-stu-id="c120b-147">F0 (free tier)</span></span>
- <span data-ttu-id="c120b-148">S0</span><span class="sxs-lookup"><span data-stu-id="c120b-148">S0</span></span>
- <span data-ttu-id="c120b-149">S1</span><span class="sxs-lookup"><span data-stu-id="c120b-149">S1</span></span>
- <span data-ttu-id="c120b-150">S2</span><span class="sxs-lookup"><span data-stu-id="c120b-150">S2</span></span>
- <span data-ttu-id="c120b-151">S3</span><span class="sxs-lookup"><span data-stu-id="c120b-151">S3</span></span>
- <span data-ttu-id="c120b-152">S4</span><span class="sxs-lookup"><span data-stu-id="c120b-152">S4</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c120b-153">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="c120b-153">-StorageAccountId</span></span>
<span data-ttu-id="c120b-154">Lista de contas de armazenamento de propriedade do usuário.</span><span class="sxs-lookup"><span data-stu-id="c120b-154">List of User Owned Storage Accounts.</span></span>

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

### <span data-ttu-id="c120b-155">-Tag</span><span class="sxs-lookup"><span data-stu-id="c120b-155">-Tag</span></span>
<span data-ttu-id="c120b-156">Especifica uma marca como um par de nome/valor.</span><span class="sxs-lookup"><span data-stu-id="c120b-156">Specifies a tag as a name/value pair.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c120b-157">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c120b-157">-Confirm</span></span>
<span data-ttu-id="c120b-158">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c120b-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c120b-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c120b-159">-WhatIf</span></span>
<span data-ttu-id="c120b-160">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c120b-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c120b-161">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c120b-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c120b-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c120b-162">CommonParameters</span></span>
<span data-ttu-id="c120b-163">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c120b-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c120b-164">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c120b-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c120b-165">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c120b-165">INPUTS</span></span>

### <span data-ttu-id="c120b-166">System.String</span><span class="sxs-lookup"><span data-stu-id="c120b-166">System.String</span></span>

### <span data-ttu-id="c120b-167">System.Collections.Hashtable[]</span><span class="sxs-lookup"><span data-stu-id="c120b-167">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="c120b-168">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="c120b-168">OUTPUTS</span></span>

### <span data-ttu-id="c120b-169">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="c120b-169">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="c120b-170">NOTES</span><span class="sxs-lookup"><span data-stu-id="c120b-170">NOTES</span></span>

## <span data-ttu-id="c120b-171">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c120b-171">RELATED LINKS</span></span>

[<span data-ttu-id="c120b-172">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="c120b-172">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="c120b-173">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="c120b-173">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="c120b-174">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="c120b-174">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)
