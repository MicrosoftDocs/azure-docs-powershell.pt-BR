---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultRemoval.md
ms.openlocfilehash: 98a3a023564c2c61f1398856e8a089276aeae7bc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113075"
---
# <span data-ttu-id="ab568-101">Undo-AzKeyVaultRemoval</span><span class="sxs-lookup"><span data-stu-id="ab568-101">Undo-AzKeyVaultRemoval</span></span>

## <span data-ttu-id="ab568-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ab568-102">SYNOPSIS</span></span>
<span data-ttu-id="ab568-103">Recupera um cofre de chave excluído em um estado ativo.</span><span class="sxs-lookup"><span data-stu-id="ab568-103">Recovers a deleted key vault into an active state.</span></span>

## <span data-ttu-id="ab568-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ab568-104">SYNTAX</span></span>

### <span data-ttu-id="ab568-105">Padrão (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ab568-105">Default (Default)</span></span>
```
Undo-AzKeyVaultRemoval [-VaultName] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab568-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="ab568-106">InputObject</span></span>
```
Undo-AzKeyVaultRemoval [-InputObject] <PSDeletedKeyVault> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab568-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="ab568-107">DESCRIPTION</span></span>
<span data-ttu-id="ab568-108">O cmdlet **Undo-AzKeyVaultRemoval** recuperará um cofre de chave excluído anteriormente.</span><span class="sxs-lookup"><span data-stu-id="ab568-108">The **Undo-AzKeyVaultRemoval** cmdlet will recover a previously deleted key vault.</span></span> <span data-ttu-id="ab568-109">O cofre recuperado estará ativo após a recuperação</span><span class="sxs-lookup"><span data-stu-id="ab568-109">The recovered vault will be active after recovery</span></span>

## <span data-ttu-id="ab568-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ab568-110">EXAMPLES</span></span>

### <span data-ttu-id="ab568-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ab568-111">Example 1</span></span>
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

<span data-ttu-id="ab568-112">Esse comando recuperará o cofre de chave 'MyKeyVault' que foi excluído anteriormente da região lesteus2 e do grupo de recursos 'MyResourceGroup', em um estado ativo e acessível.</span><span class="sxs-lookup"><span data-stu-id="ab568-112">This command will recover the key vault 'MyKeyVault' that was previously deleted from eastus2 region and 'MyResourceGroup' resource group, into an active and usable state.</span></span> <span data-ttu-id="ab568-113">Ele também substitui as marcas por uma nova marca.</span><span class="sxs-lookup"><span data-stu-id="ab568-113">It also replaces the tags with new tag.</span></span>

## <span data-ttu-id="ab568-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ab568-114">PARAMETERS</span></span>

### <span data-ttu-id="ab568-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab568-115">-DefaultProfile</span></span>
<span data-ttu-id="ab568-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="ab568-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ab568-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ab568-117">-InputObject</span></span>
<span data-ttu-id="ab568-118">Objeto do cofre excluído</span><span class="sxs-lookup"><span data-stu-id="ab568-118">Deleted vault object</span></span>

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

### <span data-ttu-id="ab568-119">-Local</span><span class="sxs-lookup"><span data-stu-id="ab568-119">-Location</span></span>
<span data-ttu-id="ab568-120">Especifica a região original do Azure do cofre excluído.</span><span class="sxs-lookup"><span data-stu-id="ab568-120">Specifies the deleted vault original Azure region.</span></span>

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

### <span data-ttu-id="ab568-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab568-121">-ResourceGroupName</span></span>
<span data-ttu-id="ab568-122">Especifica o nome de um grupo de recursos existente no qual se cria o cofre de chave.</span><span class="sxs-lookup"><span data-stu-id="ab568-122">Specifies the name of an existing resource group in which to create the key vault.</span></span>

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

### <span data-ttu-id="ab568-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="ab568-123">-Tag</span></span>
<span data-ttu-id="ab568-124">Pares de valor-chave na forma de uma tabela hash.</span><span class="sxs-lookup"><span data-stu-id="ab568-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ab568-125">Por exemplo: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="ab568-125">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ab568-126">-Nomedo Cofre</span><span class="sxs-lookup"><span data-stu-id="ab568-126">-VaultName</span></span>
<span data-ttu-id="ab568-127">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="ab568-127">Vault name.</span></span>
<span data-ttu-id="ab568-128">O Cmdlet construirá o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="ab568-128">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="ab568-129">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="ab568-129">-Confirm</span></span>
<span data-ttu-id="ab568-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab568-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab568-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab568-131">-WhatIf</span></span>
<span data-ttu-id="ab568-132">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="ab568-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ab568-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ab568-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab568-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab568-134">CommonParameters</span></span>
<span data-ttu-id="ab568-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab568-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab568-136">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ab568-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab568-137">Entradas</span><span class="sxs-lookup"><span data-stu-id="ab568-137">INPUTS</span></span>

### <span data-ttu-id="ab568-138">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span><span class="sxs-lookup"><span data-stu-id="ab568-138">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span></span>

## <span data-ttu-id="ab568-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="ab568-139">OUTPUTS</span></span>

### <span data-ttu-id="ab568-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="ab568-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="ab568-141">Notas</span><span class="sxs-lookup"><span data-stu-id="ab568-141">NOTES</span></span>

## <span data-ttu-id="ab568-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ab568-142">RELATED LINKS</span></span>

[<span data-ttu-id="ab568-143">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="ab568-143">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)

[<span data-ttu-id="ab568-144">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="ab568-144">New-AzKeyVault</span></span>](./New-AzKeyVault.md)

[<span data-ttu-id="ab568-145">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="ab568-145">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)
