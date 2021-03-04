---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/undo-azkeyvaultremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultRemoval.md
ms.openlocfilehash: ff7dea63b4731b4a2a6becfc31d0b312345978bf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888511"
---
# <span data-ttu-id="4b942-101">Undo-AzKeyVaultRemoval</span><span class="sxs-lookup"><span data-stu-id="4b942-101">Undo-AzKeyVaultRemoval</span></span>

## <span data-ttu-id="4b942-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b942-102">SYNOPSIS</span></span>
<span data-ttu-id="4b942-103">Recupera um cofre de chaves excluído em um estado ativo.</span><span class="sxs-lookup"><span data-stu-id="4b942-103">Recovers a deleted key vault into an active state.</span></span>

## <span data-ttu-id="4b942-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4b942-104">SYNTAX</span></span>

### <span data-ttu-id="4b942-105">Padrão (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4b942-105">Default (Default)</span></span>
```
Undo-AzKeyVaultRemoval [-VaultName] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b942-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="4b942-106">InputObject</span></span>
```
Undo-AzKeyVaultRemoval [-InputObject] <PSDeletedKeyVault> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b942-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4b942-107">DESCRIPTION</span></span>
<span data-ttu-id="4b942-108">O cmdlet **Undo-AzKeyVaultRemoval** recuperará um cofre de chaves excluído anteriormente.</span><span class="sxs-lookup"><span data-stu-id="4b942-108">The **Undo-AzKeyVaultRemoval** cmdlet will recover a previously deleted key vault.</span></span> <span data-ttu-id="4b942-109">O cofre recuperado estará ativo após a recuperação</span><span class="sxs-lookup"><span data-stu-id="4b942-109">The recovered vault will be active after recovery</span></span>

## <span data-ttu-id="4b942-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4b942-110">EXAMPLES</span></span>

### <span data-ttu-id="4b942-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4b942-111">Example 1</span></span>
```powershell
PS C:\> Undo-AzKeyVaultRemoval -VaultName 'MyKeyVault' -ResourceGroupName 'MyResourceGroup' -Location 'eastus2' -Tag @{"x"= "y"}

Vault Name                       : MyKeyVault
Resource Group Name              : MyResourceGroup
Location                         : eastus2
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers
                                   /Microsoft.KeyVault/vaults/mykeyvault
Vault URI                        : https://mykeyvault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : True
Enabled For Template Deployment? : True
Enabled For Disk Encryption?     : True
Soft Delete Enabled?             : True
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
                                   setissuers, recover
                                   Permissions to (Key Vault Managed) Storage : delete, deletesas, get, getsas, list,
                                   listsas, regeneratekey, set, setsas, update

Tags                             :
                                   Name  Value
                                   ====  =====
                                   x     y
```

<span data-ttu-id="4b942-112">Este comando recuperará o cofre de chaves 'MyKeyVault' que foi excluído anteriormente da região eastus2 e do grupo de recursos 'MyResourceGroup', em um estado ativo e usável.</span><span class="sxs-lookup"><span data-stu-id="4b942-112">This command will recover the key vault 'MyKeyVault' that was previously deleted from eastus2 region and 'MyResourceGroup' resource group, into an active and usable state.</span></span> <span data-ttu-id="4b942-113">Ele também substitui as marcas por uma nova marca.</span><span class="sxs-lookup"><span data-stu-id="4b942-113">It also replaces the tags with new tag.</span></span>

## <span data-ttu-id="4b942-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4b942-114">PARAMETERS</span></span>

### <span data-ttu-id="4b942-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b942-115">-DefaultProfile</span></span>
<span data-ttu-id="4b942-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="4b942-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4b942-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4b942-117">-InputObject</span></span>
<span data-ttu-id="4b942-118">Objeto vault excluído</span><span class="sxs-lookup"><span data-stu-id="4b942-118">Deleted vault object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4b942-119">-Location</span><span class="sxs-lookup"><span data-stu-id="4b942-119">-Location</span></span>
<span data-ttu-id="4b942-120">Especifica a região original do Azure do cofre excluído.</span><span class="sxs-lookup"><span data-stu-id="4b942-120">Specifies the deleted vault original Azure region.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b942-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b942-121">-ResourceGroupName</span></span>
<span data-ttu-id="4b942-122">Especifica o nome de um grupo de recursos existente no qual criar o cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="4b942-122">Specifies the name of an existing resource group in which to create the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b942-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="4b942-123">-Tag</span></span>
<span data-ttu-id="4b942-124">Pares de valores-chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="4b942-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4b942-125">Por exemplo: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="4b942-125">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b942-126">-VaultName</span><span class="sxs-lookup"><span data-stu-id="4b942-126">-VaultName</span></span>
<span data-ttu-id="4b942-127">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="4b942-127">Vault name.</span></span>
<span data-ttu-id="4b942-128">O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="4b942-128">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b942-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4b942-129">-Confirm</span></span>
<span data-ttu-id="4b942-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b942-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b942-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b942-131">-WhatIf</span></span>
<span data-ttu-id="4b942-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4b942-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4b942-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4b942-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b942-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b942-134">CommonParameters</span></span>
<span data-ttu-id="4b942-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b942-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b942-136">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4b942-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b942-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4b942-137">INPUTS</span></span>

### <span data-ttu-id="4b942-138">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span><span class="sxs-lookup"><span data-stu-id="4b942-138">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span></span>

## <span data-ttu-id="4b942-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4b942-139">OUTPUTS</span></span>

### <span data-ttu-id="4b942-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="4b942-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="4b942-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="4b942-141">NOTES</span></span>

## <span data-ttu-id="4b942-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4b942-142">RELATED LINKS</span></span>

[<span data-ttu-id="4b942-143">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="4b942-143">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)

[<span data-ttu-id="4b942-144">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="4b942-144">New-AzKeyVault</span></span>](./New-AzKeyVault.md)

[<span data-ttu-id="4b942-145">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="4b942-145">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)
