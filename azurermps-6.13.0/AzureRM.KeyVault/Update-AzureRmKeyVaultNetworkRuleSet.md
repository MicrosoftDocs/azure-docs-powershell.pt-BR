---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/update-azurermkeyvaultnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureRmKeyVaultNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureRmKeyVaultNetworkRuleSet.md
ms.openlocfilehash: b1a0081f24932cf25026bdea4e9064e9dbb5a0cb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429515"
---
# <span data-ttu-id="41d87-101">Update-AzureRmKeyVaultNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="41d87-101">Update-AzureRmKeyVaultNetworkRuleSet</span></span>

## <span data-ttu-id="41d87-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="41d87-102">SYNOPSIS</span></span>
<span data-ttu-id="41d87-103">Atualiza o conjunto de regras de rede em um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="41d87-103">Updates the network rule set on a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41d87-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="41d87-104">SYNTAX</span></span>

### <span data-ttu-id="41d87-105">ByVaultName (padrão)</span><span class="sxs-lookup"><span data-stu-id="41d87-105">ByVaultName (Default)</span></span>
```
Update-AzureRmKeyVaultNetworkRuleSet [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>] [-Bypass <PSKeyVaultNetworkRuleBypassEnum>]
 [-IpAddressRange <String[]>] [-VirtualNetworkResourceId <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41d87-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="41d87-106">ByInputObject</span></span>
```
Update-AzureRmKeyVaultNetworkRuleSet [-InputObject] <PSKeyVault>
 [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>] [-Bypass <PSKeyVaultNetworkRuleBypassEnum>]
 [-IpAddressRange <String[]>] [-VirtualNetworkResourceId <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41d87-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="41d87-107">ByResourceId</span></span>
```
Update-AzureRmKeyVaultNetworkRuleSet [-ResourceId] <String>
 [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>] [-Bypass <PSKeyVaultNetworkRuleBypassEnum>]
 [-IpAddressRange <String[]>] [-VirtualNetworkResourceId <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="41d87-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="41d87-108">DESCRIPTION</span></span>
<span data-ttu-id="41d87-109">O comando **Update-AzureRmKeyVaultNetworkRuleSet** atualiza as regras de rede em vigor no cofre de chaves especificado.</span><span class="sxs-lookup"><span data-stu-id="41d87-109">The **Update-AzureRmKeyVaultNetworkRuleSet** command updates the network rules in effect on the specified key vault.</span></span> 

## <span data-ttu-id="41d87-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="41d87-110">EXAMPLES</span></span>

### <span data-ttu-id="41d87-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="41d87-111">Example 1</span></span>
```powershell
PS C:\> $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" -ServiceEndpoint Microsoft.KeyVault 
PS C:\> $virtualNetwork = New-AzureRmVirtualNetwork -Name myVNet -ResourceGroupName myRG -Location westus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
PS C:\> $myNetworkResId = (Get-AzureRmVirtualNetwork -Name myVNet -ResourceGroupName myRG).Subnets[0].Id
PS C:\> Update-AzureRmKeyVaultNetworkRuleSet -VaultName 'myVault' -ResourceGroupName myRG -Bypass AzureServices -IpAddressRange "10.0.1.0/24" -VirtualNetworkResourceId $myNetworkResId -PassThru

Vault Name                       : myVault
Resource Group Name              : myRG
Location                         : West US
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/myvault
Vault URI                        : https://myvault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : False
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             :
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        : get, create, delete, list, update,
                                   import, backup, restore, recover
                                   Permissions to Secrets                     : get, list, set, delete, backup,
                                   restore, recover
                                   Permissions to Certificates                : get, delete, list, create, import,
                                   update, deleteissuers, getissuers, listissuers, managecontacts, manageissuers,
                                   setissuers, recover, backup, restore
                                   Permissions to (Key Vault Managed) Storage : delete, deletesas, get, getsas, list,
                                   listsas, regeneratekey, set, setsas, update, recover, backup, restore


Network Rule Set                 :
                                   Default Action                             : Allow
                                   Bypass                                     : AzureServices
                                   IP Rules                                   : 10.0.1.0/24
                                   Virtual Network Rules                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-
                                   xxxxxxxxxxxxx/resourcegroups/myrg/providers/microsoft.network/virtualnetworks/myvn
                                   et/subnets/frontendsubnet

Tags                             :
```

<span data-ttu-id="41d87-112">Esse comando atualiza o conjunto de regras de rede no cofre chamado ' myvault ' para o intervalo IP especificado e a rede virtual, permitindo ignorar a regra de rede dos serviços do Azure.</span><span class="sxs-lookup"><span data-stu-id="41d87-112">This command updates the network ruleset on the vault named 'myVault' for the specified IP range and the virtual network, allowing bypassing of the network rule for Azure services.</span></span>

## <span data-ttu-id="41d87-113">OS</span><span class="sxs-lookup"><span data-stu-id="41d87-113">PARAMETERS</span></span>

### <span data-ttu-id="41d87-114">-Ignorar</span><span class="sxs-lookup"><span data-stu-id="41d87-114">-Bypass</span></span>
<span data-ttu-id="41d87-115">Especifica bypass da regra de rede.</span><span class="sxs-lookup"><span data-stu-id="41d87-115">Specifies bypass of network rule.</span></span>

```yaml
Type: PSKeyVaultNetworkRuleBypassEnum
Parameter Sets: (All)
Aliases:
Accepted values: None, AzureServices

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41d87-116">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="41d87-116">-DefaultAction</span></span>
<span data-ttu-id="41d87-117">Especifica a ação padrão da regra de rede.</span><span class="sxs-lookup"><span data-stu-id="41d87-117">Specifies default action of network rule.</span></span>

```yaml
Type: PSKeyVaultNetworkRuleDefaultActionEnum
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41d87-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41d87-118">-DefaultProfile</span></span>
<span data-ttu-id="41d87-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="41d87-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41d87-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="41d87-120">-InputObject</span></span>
<span data-ttu-id="41d87-121">Objeto do keyvault</span><span class="sxs-lookup"><span data-stu-id="41d87-121">KeyVault object</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="41d87-122">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="41d87-122">-IpAddressRange</span></span>
<span data-ttu-id="41d87-123">Especifica o intervalo de endereços IP de rede permitido da regra de rede.</span><span class="sxs-lookup"><span data-stu-id="41d87-123">Specifies allowed network IP address range of network rule.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41d87-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="41d87-124">-PassThru</span></span>
<span data-ttu-id="41d87-125">Esse cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="41d87-125">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="41d87-126">Se essa opção for especificada, ela retornará o objeto do cofre de chaves atualizado.</span><span class="sxs-lookup"><span data-stu-id="41d87-126">If this switch is specified, it returns the updated key vault object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41d87-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41d87-127">-ResourceGroupName</span></span>
<span data-ttu-id="41d87-128">Especifica o nome do grupo de recursos associado ao cofre de chaves cuja regra de rede está sendo modificada.</span><span class="sxs-lookup"><span data-stu-id="41d87-128">Specifies the name of the resource group associated with the key vault whose network rule is being modified.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41d87-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="41d87-129">-ResourceId</span></span>
<span data-ttu-id="41d87-130">ID do recurso do keyvault</span><span class="sxs-lookup"><span data-stu-id="41d87-130">KeyVault Resource Id</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41d87-131">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="41d87-131">-VaultName</span></span>
<span data-ttu-id="41d87-132">Especifica o nome de um cofre da chave cuja regra de rede está sendo modificada.</span><span class="sxs-lookup"><span data-stu-id="41d87-132">Specifies the name of a key vault whose network rule is being modified.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41d87-133">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="41d87-133">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="41d87-134">Especifica o identificador de recurso de rede virtual permitido da regra de rede.</span><span class="sxs-lookup"><span data-stu-id="41d87-134">Specifies allowed virtual network resource identifier of network rule.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41d87-135">-Confirme</span><span class="sxs-lookup"><span data-stu-id="41d87-135">-Confirm</span></span>
<span data-ttu-id="41d87-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41d87-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41d87-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41d87-137">-WhatIf</span></span>
<span data-ttu-id="41d87-138">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="41d87-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41d87-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="41d87-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41d87-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41d87-140">CommonParameters</span></span>
<span data-ttu-id="41d87-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41d87-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41d87-142">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41d87-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41d87-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="41d87-143">INPUTS</span></span>

### <span data-ttu-id="41d87-144">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="41d87-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="41d87-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="41d87-145">OUTPUTS</span></span>

### <span data-ttu-id="41d87-146">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="41d87-146">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="41d87-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="41d87-147">NOTES</span></span>

## <span data-ttu-id="41d87-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="41d87-148">RELATED LINKS</span></span>