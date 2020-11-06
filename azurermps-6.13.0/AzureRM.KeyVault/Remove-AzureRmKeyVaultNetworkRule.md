---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/add-azurermkeyvaultnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVaultNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVaultNetworkRule.md
ms.openlocfilehash: f1ff73a753c794ce7528c9af2b480f75d1460815
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430220"
---
# <span data-ttu-id="a9fcb-101">Remove-AzureRmKeyVaultNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a9fcb-101">Remove-AzureRmKeyVaultNetworkRule</span></span>

## <span data-ttu-id="a9fcb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a9fcb-102">SYNOPSIS</span></span>
<span data-ttu-id="a9fcb-103">Remove uma regra de rede de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="a9fcb-103">Removes a network rule from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9fcb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a9fcb-104">SYNTAX</span></span>

### <span data-ttu-id="a9fcb-105">ByVaultName (padrão)</span><span class="sxs-lookup"><span data-stu-id="a9fcb-105">ByVaultName (Default)</span></span>
```
Remove-AzureRmKeyVaultNetworkRule [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-IpAddressRange <String[]>] [-VirtualNetworkResourceId <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9fcb-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a9fcb-106">ByInputObject</span></span>
```
Remove-AzureRmKeyVaultNetworkRule [-InputObject] <PSKeyVault> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9fcb-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a9fcb-107">ByResourceId</span></span>
```
Remove-AzureRmKeyVaultNetworkRule [-ResourceId] <String> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9fcb-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a9fcb-108">DESCRIPTION</span></span>
<span data-ttu-id="a9fcb-109">Remove uma regra de rede de um cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="a9fcb-109">Removes a network rule from a key vault.</span></span>

## <span data-ttu-id="a9fcb-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a9fcb-110">EXAMPLES</span></span>

### <span data-ttu-id="a9fcb-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a9fcb-111">Example 1</span></span>
```powershell
PS C:\> $myNetworkResId = (Get-AzureRmVirtualNetwork -Name myVNetName -ResourceGroupName myRG).Subnets[0].Id
PS C:\> Remove-AzureRmKeyVaultNetworkRule -VaultName myVault -IpAddressRange "10.0.0.1/26" -VirtualNetworkResourceId $myNetworkResId -PassThru

Vault Name                       : myVault
Resource Group Name              : myrg
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
                                   IP Rules                                   : 
                                   Virtual Network Rules                      :

Tags                             :
```

<span data-ttu-id="a9fcb-112">Esse comando Remove uma regra de rede do cofre especificado, contanto que uma regra seja encontrada, correspondendo ao endereço IP especificado e ao identificador de recursos de rede virtual.</span><span class="sxs-lookup"><span data-stu-id="a9fcb-112">This command removes a network rule from the specified vault, provided a rule is found matching the specified IP address and the virtual network resource identifier.</span></span>

## <span data-ttu-id="a9fcb-113">OS</span><span class="sxs-lookup"><span data-stu-id="a9fcb-113">PARAMETERS</span></span>

### <span data-ttu-id="a9fcb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9fcb-114">-DefaultProfile</span></span>
<span data-ttu-id="a9fcb-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a9fcb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9fcb-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a9fcb-116">-InputObject</span></span>
<span data-ttu-id="a9fcb-117">Objeto do keyvault</span><span class="sxs-lookup"><span data-stu-id="a9fcb-117">KeyVault object</span></span>

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

### <span data-ttu-id="a9fcb-118">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="a9fcb-118">-IpAddressRange</span></span>
<span data-ttu-id="a9fcb-119">Especifica o intervalo de endereços IP de rede permitido da regra de rede.</span><span class="sxs-lookup"><span data-stu-id="a9fcb-119">Specifies allowed network IP address range of network rule.</span></span>

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

### <span data-ttu-id="a9fcb-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a9fcb-120">-PassThru</span></span>
<span data-ttu-id="a9fcb-121">Esse cmdlet não retorna um objeto por padrão.</span><span class="sxs-lookup"><span data-stu-id="a9fcb-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="a9fcb-122">Se essa opção for especificada, ela retornará o objeto do cofre de chaves atualizado.</span><span class="sxs-lookup"><span data-stu-id="a9fcb-122">If this switch is specified, it returns the updated key vault object.</span></span>

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

### <span data-ttu-id="a9fcb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9fcb-123">-ResourceGroupName</span></span>
<span data-ttu-id="a9fcb-124">Especifica o nome do grupo de recursos associado ao cofre de chaves cuja regra de rede está sendo modificada.</span><span class="sxs-lookup"><span data-stu-id="a9fcb-124">Specifies the name of the resource group associated with the key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="a9fcb-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a9fcb-125">-ResourceId</span></span>
<span data-ttu-id="a9fcb-126">ID do recurso do keyvault</span><span class="sxs-lookup"><span data-stu-id="a9fcb-126">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="a9fcb-127">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="a9fcb-127">-VaultName</span></span>
<span data-ttu-id="a9fcb-128">Especifica o nome de um cofre da chave cuja regra de rede está sendo modificada.</span><span class="sxs-lookup"><span data-stu-id="a9fcb-128">Specifies the name of a key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="a9fcb-129">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="a9fcb-129">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="a9fcb-130">Especifica o identificador de recurso de rede virtual permitido da regra de rede.</span><span class="sxs-lookup"><span data-stu-id="a9fcb-130">Specifies allowed virtual network resource identifier of network rule.</span></span>

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

### <span data-ttu-id="a9fcb-131">-Confirme</span><span class="sxs-lookup"><span data-stu-id="a9fcb-131">-Confirm</span></span>
<span data-ttu-id="a9fcb-132">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9fcb-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9fcb-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9fcb-133">-WhatIf</span></span>
<span data-ttu-id="a9fcb-134">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a9fcb-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9fcb-135">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a9fcb-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9fcb-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9fcb-136">CommonParameters</span></span>
<span data-ttu-id="a9fcb-137">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9fcb-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9fcb-138">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9fcb-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9fcb-139">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a9fcb-139">INPUTS</span></span>

### <span data-ttu-id="a9fcb-140">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="a9fcb-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="a9fcb-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a9fcb-141">OUTPUTS</span></span>

### <span data-ttu-id="a9fcb-142">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="a9fcb-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="a9fcb-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a9fcb-143">NOTES</span></span>

## <span data-ttu-id="a9fcb-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a9fcb-144">RELATED LINKS</span></span>
