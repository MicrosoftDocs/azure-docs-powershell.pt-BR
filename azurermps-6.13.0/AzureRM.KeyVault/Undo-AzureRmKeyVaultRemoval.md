---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurermkeyvaultremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureRmKeyVaultRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureRmKeyVaultRemoval.md
ms.openlocfilehash: af6ed0e4db688cdc9ad6da598c0bc240e9b3c958
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93430216"
---
# <span data-ttu-id="85f19-101">Undo-AzureRmKeyVaultRemoval</span><span class="sxs-lookup"><span data-stu-id="85f19-101">Undo-AzureRmKeyVaultRemoval</span></span>

## <span data-ttu-id="85f19-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="85f19-102">SYNOPSIS</span></span>
<span data-ttu-id="85f19-103">Recupera um cofre de chaves excluído para um estado ativo.</span><span class="sxs-lookup"><span data-stu-id="85f19-103">Recovers a deleted key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="85f19-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="85f19-104">SYNTAX</span></span>

### <span data-ttu-id="85f19-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="85f19-105">Default (Default)</span></span>
```
Undo-AzureRmKeyVaultRemoval [-VaultName] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85f19-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="85f19-106">InputObject</span></span>
```
Undo-AzureRmKeyVaultRemoval [-InputObject] <PSDeletedKeyVault> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85f19-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="85f19-107">DESCRIPTION</span></span>
<span data-ttu-id="85f19-108">O cmdlet **Undo-AzureRmKeyVaultRemoval** recuperará um cofre de chaves previamente excluído.</span><span class="sxs-lookup"><span data-stu-id="85f19-108">The **Undo-AzureRmKeyVaultRemoval** cmdlet will recover a previously deleted key vault.</span></span> <span data-ttu-id="85f19-109">O cofre recuperado estará ativo após a recuperação</span><span class="sxs-lookup"><span data-stu-id="85f19-109">The recovered vault will be active after recovery</span></span>

## <span data-ttu-id="85f19-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="85f19-110">EXAMPLES</span></span>

### <span data-ttu-id="85f19-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="85f19-111">Example 1</span></span>
```powershell
PS C:\> Undo-AzureRmKeyVaultRemoval -VaultName 'MyKeyVault' -ResourceGroupName 'MyResourceGroup' -Location 'eastus2' -Tag @{"x"= "y"}

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

<span data-ttu-id="85f19-112">Esse comando recuperará o cofre de chave ' MyKeyVault ' que foi excluído anteriormente da região eastus2 e do grupo de recursos ' MyResource Group ', em um estado ativo e utilizável.</span><span class="sxs-lookup"><span data-stu-id="85f19-112">This command will recover the key vault 'MyKeyVault' that was previously deleted from eastus2 region and 'MyResourceGroup' resource group, into an active and usable state.</span></span> <span data-ttu-id="85f19-113">Ele também substitui as marcas por nova marca.</span><span class="sxs-lookup"><span data-stu-id="85f19-113">It also replaces the tags with new tag.</span></span>

## <span data-ttu-id="85f19-114">OS</span><span class="sxs-lookup"><span data-stu-id="85f19-114">PARAMETERS</span></span>

### <span data-ttu-id="85f19-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85f19-115">-DefaultProfile</span></span>
<span data-ttu-id="85f19-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="85f19-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="85f19-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="85f19-117">-InputObject</span></span>
<span data-ttu-id="85f19-118">Objeto do cofre excluído</span><span class="sxs-lookup"><span data-stu-id="85f19-118">Deleted vault object</span></span>

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

### <span data-ttu-id="85f19-119">-Local</span><span class="sxs-lookup"><span data-stu-id="85f19-119">-Location</span></span>
<span data-ttu-id="85f19-120">Especifica a região original do Azure do cofre excluído.</span><span class="sxs-lookup"><span data-stu-id="85f19-120">Specifies the deleted vault original Azure region.</span></span>

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

### <span data-ttu-id="85f19-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85f19-121">-ResourceGroupName</span></span>
<span data-ttu-id="85f19-122">Especifica o nome de um grupo de recursos existente no qual criar o cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="85f19-122">Specifies the name of an existing resource group in which to create the key vault.</span></span>

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

### <span data-ttu-id="85f19-123">-Marca</span><span class="sxs-lookup"><span data-stu-id="85f19-123">-Tag</span></span>
<span data-ttu-id="85f19-124">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="85f19-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="85f19-125">Por exemplo: @ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="85f19-125">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="85f19-126">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="85f19-126">-VaultName</span></span>
<span data-ttu-id="85f19-127">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="85f19-127">Vault name.</span></span>
<span data-ttu-id="85f19-128">O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="85f19-128">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="85f19-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="85f19-129">-Confirm</span></span>
<span data-ttu-id="85f19-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85f19-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85f19-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85f19-131">-WhatIf</span></span>
<span data-ttu-id="85f19-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="85f19-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="85f19-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="85f19-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85f19-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85f19-134">CommonParameters</span></span>
<span data-ttu-id="85f19-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85f19-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85f19-136">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85f19-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85f19-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="85f19-137">INPUTS</span></span>

### <span data-ttu-id="85f19-138">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span><span class="sxs-lookup"><span data-stu-id="85f19-138">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span></span>
<span data-ttu-id="85f19-139">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="85f19-139">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="85f19-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="85f19-140">OUTPUTS</span></span>

### <span data-ttu-id="85f19-141">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="85f19-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="85f19-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="85f19-142">NOTES</span></span>

## <span data-ttu-id="85f19-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="85f19-143">RELATED LINKS</span></span>

[<span data-ttu-id="85f19-144">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="85f19-144">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)

[<span data-ttu-id="85f19-145">New-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="85f19-145">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)

[<span data-ttu-id="85f19-146">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="85f19-146">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)
