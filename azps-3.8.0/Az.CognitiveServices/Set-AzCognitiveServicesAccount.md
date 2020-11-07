---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 11E2D82A-1DF1-4E19-8328-44674641D1BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/set-azcognitiveservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Set-AzCognitiveServicesAccount.md
ms.openlocfilehash: fc510ebede11168dd8d8b090cd2069ce3e6de52c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93940300"
---
# <span data-ttu-id="a9d2e-101">Set-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="a9d2e-101">Set-AzCognitiveServicesAccount</span></span>

## <span data-ttu-id="a9d2e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a9d2e-102">SYNOPSIS</span></span>
<span data-ttu-id="a9d2e-103">Modifica uma conta.</span><span class="sxs-lookup"><span data-stu-id="a9d2e-103">Modifies an account.</span></span>

## <span data-ttu-id="a9d2e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a9d2e-104">SYNTAX</span></span>

### <span data-ttu-id="a9d2e-105">CognitiveServicesEncryption (padrão)</span><span class="sxs-lookup"><span data-stu-id="a9d2e-105">CognitiveServicesEncryption (Default)</span></span>
```
Set-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-AssignIdentity] [-IdentityType <IdentityType>]
 [-StorageAccountId <String[]>] [-CognitiveServicesEncryption] [-NetworkRuleSet <PSNetworkRuleSet>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9d2e-106">KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="a9d2e-106">KeyVaultEncryption</span></span>
```
Set-AzCognitiveServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName <String>]
 [-Tag <Hashtable[]>] [-CustomSubdomainName <String>] [-AssignIdentity] [-IdentityType <IdentityType>]
 [-StorageAccountId <String[]>] [-KeyVaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-NetworkRuleSet <PSNetworkRuleSet>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9d2e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a9d2e-107">DESCRIPTION</span></span>
<span data-ttu-id="a9d2e-108">O cmdlet **set-AzCognitiveServicesAccount** modifica a SKU ou marca da conta de serviços cognitivas especificada.</span><span class="sxs-lookup"><span data-stu-id="a9d2e-108">The **Set-AzCognitiveServicesAccount** cmdlet modifies the SKU or tags of the specified Cognitive Services account.</span></span>

## <span data-ttu-id="a9d2e-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a9d2e-109">EXAMPLES</span></span>

### <span data-ttu-id="a9d2e-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a9d2e-110">Example 1</span></span>
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

## <span data-ttu-id="a9d2e-111">OS</span><span class="sxs-lookup"><span data-stu-id="a9d2e-111">PARAMETERS</span></span>

### <span data-ttu-id="a9d2e-112">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="a9d2e-112">-AssignIdentity</span></span>
<span data-ttu-id="a9d2e-113">Gerar e atribuir uma nova identidade de conta de serviços cognitiva para esta conta de armazenamento para uso com os serviços de gerenciamento de chaves como o repositório de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="a9d2e-113">Generate and assign a new Cognitive Services Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="a9d2e-114">-CognitiveServicesEncryption</span><span class="sxs-lookup"><span data-stu-id="a9d2e-114">-CognitiveServicesEncryption</span></span>
<span data-ttu-id="a9d2e-115">Se você deve definir a fonte de origem de criptografia de conta de serviços cognitiva para Microsoft. Cognitivaservices ou not.</span><span class="sxs-lookup"><span data-stu-id="a9d2e-115">Whether to set Cognitive Services Account Encryption KeySource to Microsoft.CognitiveServices or not.</span></span>

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

### <span data-ttu-id="a9d2e-116">-CustomSubdomainName</span><span class="sxs-lookup"><span data-stu-id="a9d2e-116">-CustomSubdomainName</span></span>
<span data-ttu-id="a9d2e-117">Nome de subdomínio da conta de serviços cognitiva.</span><span class="sxs-lookup"><span data-stu-id="a9d2e-117">Cognitive Services Account Subdomain Name.</span></span>

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

### <span data-ttu-id="a9d2e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9d2e-118">-DefaultProfile</span></span>
<span data-ttu-id="a9d2e-119">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="a9d2e-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a9d2e-120">-Force</span><span class="sxs-lookup"><span data-stu-id="a9d2e-120">-Force</span></span>
<span data-ttu-id="a9d2e-121">Força o comando a ser executado sem pedir confirmação do usuário.</span><span class="sxs-lookup"><span data-stu-id="a9d2e-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a9d2e-122">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="a9d2e-122">-IdentityType</span></span>
<span data-ttu-id="a9d2e-123">Tipo de identidade de serviço gerenciado.</span><span class="sxs-lookup"><span data-stu-id="a9d2e-123">Type of managed service identity.</span></span>

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

### <span data-ttu-id="a9d2e-124">-KeyName</span><span class="sxs-lookup"><span data-stu-id="a9d2e-124">-KeyName</span></span>
<span data-ttu-id="a9d2e-125">O KeyName do cofre da fonte de criptografia de conta de serviços cognitiva</span><span class="sxs-lookup"><span data-stu-id="a9d2e-125">Cognitive Services Account encryption keySource KeyVault KeyName</span></span>

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

### <span data-ttu-id="a9d2e-126">-KeyVaultEncryption</span><span class="sxs-lookup"><span data-stu-id="a9d2e-126">-KeyVaultEncryption</span></span>
<span data-ttu-id="a9d2e-127">Se você deve definir a fonte de origem de criptografia de conta de serviços cognitiva para a Microsoft. keyvault ou não.</span><span class="sxs-lookup"><span data-stu-id="a9d2e-127">Whether to set Cognitive Services Account encryption keySource to Microsoft.KeyVault or not.</span></span> <span data-ttu-id="a9d2e-128">Se você especificar a KeyName, a keyversion e o KeyVaultUri, a origem de criptografia da conta de serviços cognitiva também será definida como Microsoft. Weather Weather esse parâmetro está definido ou não.</span><span class="sxs-lookup"><span data-stu-id="a9d2e-128">If you specify KeyName, KeyVersion and KeyVaultUri, Cognitive Services Account Encryption KeySource will also be set to Microsoft.KeyVault weather this parameter is set or not.</span></span>

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

### <span data-ttu-id="a9d2e-129">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="a9d2e-129">-KeyVaultUri</span></span>
<span data-ttu-id="a9d2e-130">KeyVaultUri de uma fonte de código de criptografia de conta de serviços cognitiva</span><span class="sxs-lookup"><span data-stu-id="a9d2e-130">Cognitive Services Account encryption keySource KeyVault KeyVaultUri</span></span>

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

### <span data-ttu-id="a9d2e-131">-Keyversion</span><span class="sxs-lookup"><span data-stu-id="a9d2e-131">-KeyVersion</span></span>
<span data-ttu-id="a9d2e-132">Subversão do cofre de conta de criptografia de conta de serviços cognitiva</span><span class="sxs-lookup"><span data-stu-id="a9d2e-132">Cognitive Services Account encryption keySource KeyVault KeyVersion</span></span>

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

### <span data-ttu-id="a9d2e-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="a9d2e-133">-Name</span></span>
<span data-ttu-id="a9d2e-134">Especifica o nome da conta a ser modificada.</span><span class="sxs-lookup"><span data-stu-id="a9d2e-134">Specifies the name of the account to modify.</span></span>

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

### <span data-ttu-id="a9d2e-135">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="a9d2e-135">-NetworkRuleSet</span></span>
<span data-ttu-id="a9d2e-136">NetworkRuleSet é usado para definir um conjunto de regras de configuração para firewalls e redes virtuais, bem como para definir valores para propriedades de rede, como manipular solicitações que não correspondem a nenhuma das regras definidas</span><span class="sxs-lookup"><span data-stu-id="a9d2e-136">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as how to handle requests that don't match any of the defined rules</span></span>

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

### <span data-ttu-id="a9d2e-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9d2e-137">-ResourceGroupName</span></span>
<span data-ttu-id="a9d2e-138">Especifica o nome do grupo de recursos ao qual a conta está atribuída.</span><span class="sxs-lookup"><span data-stu-id="a9d2e-138">Specifies the name of the resource group the account is assigned to.</span></span>

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

### <span data-ttu-id="a9d2e-139">-SkuName</span><span class="sxs-lookup"><span data-stu-id="a9d2e-139">-SkuName</span></span>
<span data-ttu-id="a9d2e-140">Especifica a SKU da conta.</span><span class="sxs-lookup"><span data-stu-id="a9d2e-140">Specifies the SKU for the account.</span></span>
<span data-ttu-id="a9d2e-141">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="a9d2e-141">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a9d2e-142">F0 (nível gratuito)</span><span class="sxs-lookup"><span data-stu-id="a9d2e-142">F0 (free tier)</span></span>
- <span data-ttu-id="a9d2e-143">S0</span><span class="sxs-lookup"><span data-stu-id="a9d2e-143">S0</span></span>
- <span data-ttu-id="a9d2e-144">Eles</span><span class="sxs-lookup"><span data-stu-id="a9d2e-144">S1</span></span>
- <span data-ttu-id="a9d2e-145">S2</span><span class="sxs-lookup"><span data-stu-id="a9d2e-145">S2</span></span>
- <span data-ttu-id="a9d2e-146">S3</span><span class="sxs-lookup"><span data-stu-id="a9d2e-146">S3</span></span>
- <span data-ttu-id="a9d2e-147">S4</span><span class="sxs-lookup"><span data-stu-id="a9d2e-147">S4</span></span>

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

### <span data-ttu-id="a9d2e-148">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="a9d2e-148">-StorageAccountId</span></span>
<span data-ttu-id="a9d2e-149">Lista de contas de armazenamento pertencentes ao usuário.</span><span class="sxs-lookup"><span data-stu-id="a9d2e-149">List of User Owned Storage Accounts.</span></span>

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

### <span data-ttu-id="a9d2e-150">-Marca</span><span class="sxs-lookup"><span data-stu-id="a9d2e-150">-Tag</span></span>
<span data-ttu-id="a9d2e-151">Especifica uma marca como um par de nome/valor.</span><span class="sxs-lookup"><span data-stu-id="a9d2e-151">Specifies a tag as a name/value pair.</span></span>

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

### <span data-ttu-id="a9d2e-152">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a9d2e-152">-Confirm</span></span>
<span data-ttu-id="a9d2e-153">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9d2e-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9d2e-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9d2e-154">-WhatIf</span></span>
<span data-ttu-id="a9d2e-155">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a9d2e-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9d2e-156">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a9d2e-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9d2e-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9d2e-157">CommonParameters</span></span>
<span data-ttu-id="a9d2e-158">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9d2e-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9d2e-159">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a9d2e-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9d2e-160">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a9d2e-160">INPUTS</span></span>

### <span data-ttu-id="a9d2e-161">System. String</span><span class="sxs-lookup"><span data-stu-id="a9d2e-161">System.String</span></span>

### <span data-ttu-id="a9d2e-162">System. Collections. Hashtable []</span><span class="sxs-lookup"><span data-stu-id="a9d2e-162">System.Collections.Hashtable[]</span></span>

## <span data-ttu-id="a9d2e-163">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a9d2e-163">OUTPUTS</span></span>

### <span data-ttu-id="a9d2e-164">Microsoft. Azure. Commands. Management. Cognitivaservices. Models. PSCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="a9d2e-164">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesAccount</span></span>

## <span data-ttu-id="a9d2e-165">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a9d2e-165">NOTES</span></span>

## <span data-ttu-id="a9d2e-166">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a9d2e-166">RELATED LINKS</span></span>

[<span data-ttu-id="a9d2e-167">Get-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="a9d2e-167">Get-AzCognitiveServicesAccount</span></span>](./Get-AzCognitiveServicesAccount.md)

[<span data-ttu-id="a9d2e-168">New-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="a9d2e-168">New-AzCognitiveServicesAccount</span></span>](./New-AzCognitiveServicesAccount.md)

[<span data-ttu-id="a9d2e-169">Remove-AzCognitiveServicesAccount</span><span class="sxs-lookup"><span data-stu-id="a9d2e-169">Remove-AzCognitiveServicesAccount</span></span>](./Remove-AzCognitiveServicesAccount.md)
