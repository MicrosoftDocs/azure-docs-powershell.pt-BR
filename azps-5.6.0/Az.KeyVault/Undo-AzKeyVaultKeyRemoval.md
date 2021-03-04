---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/undo-azkeyvaultkeyremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultKeyRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultKeyRemoval.md
ms.openlocfilehash: 9de4cc6572a20dc9ec241c6f93cb035162b914f9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893159"
---
# <span data-ttu-id="9f0da-101">Undo-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="9f0da-101">Undo-AzKeyVaultKeyRemoval</span></span>

## <span data-ttu-id="9f0da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f0da-102">SYNOPSIS</span></span>
<span data-ttu-id="9f0da-103">Recupera uma chave excluída em um cofre de chaves em um estado ativo.</span><span class="sxs-lookup"><span data-stu-id="9f0da-103">Recovers a deleted key in a key vault into an active state.</span></span>

## <span data-ttu-id="9f0da-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9f0da-104">SYNTAX</span></span>

### <span data-ttu-id="9f0da-105">Padrão (Padrão)</span><span class="sxs-lookup"><span data-stu-id="9f0da-105">Default (Default)</span></span>
```
Undo-AzKeyVaultKeyRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f0da-106">HsmInteractive</span><span class="sxs-lookup"><span data-stu-id="9f0da-106">HsmInteractive</span></span>
```
Undo-AzKeyVaultKeyRemoval -HsmName <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f0da-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="9f0da-107">InputObject</span></span>
```
Undo-AzKeyVaultKeyRemoval [-InputObject] <PSDeletedKeyVaultKeyIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f0da-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9f0da-108">DESCRIPTION</span></span>
<span data-ttu-id="9f0da-109">O cmdlet **Undo-AzKeyVaultKeyRemoval** recuperará uma chave excluída anteriormente.</span><span class="sxs-lookup"><span data-stu-id="9f0da-109">The **Undo-AzKeyVaultKeyRemoval** cmdlet will recover a previously deleted key.</span></span>
<span data-ttu-id="9f0da-110">A chave recuperada estará ativa e poderá ser usada para todas as operações de chave normais.</span><span class="sxs-lookup"><span data-stu-id="9f0da-110">The recovered key will be active and can be used for all normal key operations.</span></span>
<span data-ttu-id="9f0da-111">O chamador precisa ter permissão de 'recuperar' para executar essa operação.</span><span class="sxs-lookup"><span data-stu-id="9f0da-111">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="9f0da-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9f0da-112">EXAMPLES</span></span>

### <span data-ttu-id="9f0da-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9f0da-113">Example 1</span></span>
```powershell
PS C:\> Undo-AzKeyVaultKeyRemoval -VaultName 'MyKeyVault' -Name 'MyKey'

Vault Name     : MyKeyVault
Name           : MyKey
Version        : 1af807cc331a49d0b52b7c75e1b2366e
Id             : https://mykeybault.vault.azure.net:443/keys/mykey/1af807cc331a49d0b52b7c75e1b2366e
Enabled        : True
Expires        :
Not Before     :
Created        : 5/24/2018 8:32:27 PM
Updated        : 5/24/2018 8:32:27 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="9f0da-114">Este comando recuperará a chave 'MyKey' que foi excluída anteriormente, em um estado ativo e acessível.</span><span class="sxs-lookup"><span data-stu-id="9f0da-114">This command will recover the key 'MyKey' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="9f0da-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9f0da-115">PARAMETERS</span></span>

### <span data-ttu-id="9f0da-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f0da-116">-DefaultProfile</span></span>
<span data-ttu-id="9f0da-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="9f0da-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9f0da-118">-HsmName</span><span class="sxs-lookup"><span data-stu-id="9f0da-118">-HsmName</span></span>
<span data-ttu-id="9f0da-119">Nome do HSM.</span><span class="sxs-lookup"><span data-stu-id="9f0da-119">HSM name.</span></span> <span data-ttu-id="9f0da-120">O cmdlet constrói o FQDN de um HSM gerenciado com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="9f0da-120">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmInteractive
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f0da-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9f0da-121">-InputObject</span></span>
<span data-ttu-id="9f0da-122">Objeto key excluído</span><span class="sxs-lookup"><span data-stu-id="9f0da-122">Deleted key object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f0da-123">-Name</span><span class="sxs-lookup"><span data-stu-id="9f0da-123">-Name</span></span>
<span data-ttu-id="9f0da-124">Nome da chave.</span><span class="sxs-lookup"><span data-stu-id="9f0da-124">Key name.</span></span>
<span data-ttu-id="9f0da-125">O cmdlet constrói o FQDN de uma chave a partir do nome do cofre, do ambiente selecionado no momento e do nome da chave.</span><span class="sxs-lookup"><span data-stu-id="9f0da-125">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, HsmInteractive
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f0da-126">-VaultName</span><span class="sxs-lookup"><span data-stu-id="9f0da-126">-VaultName</span></span>
<span data-ttu-id="9f0da-127">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="9f0da-127">Vault name.</span></span>
<span data-ttu-id="9f0da-128">O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="9f0da-128">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="9f0da-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9f0da-129">-Confirm</span></span>
<span data-ttu-id="9f0da-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9f0da-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f0da-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f0da-131">-WhatIf</span></span>
<span data-ttu-id="9f0da-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9f0da-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f0da-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9f0da-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f0da-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f0da-134">CommonParameters</span></span>
<span data-ttu-id="9f0da-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9f0da-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f0da-136">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9f0da-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f0da-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9f0da-137">INPUTS</span></span>

### <span data-ttu-id="9f0da-138">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="9f0da-138">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="9f0da-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9f0da-139">OUTPUTS</span></span>

### <span data-ttu-id="9f0da-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="9f0da-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="9f0da-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="9f0da-141">NOTES</span></span>

## <span data-ttu-id="9f0da-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9f0da-142">RELATED LINKS</span></span>

[<span data-ttu-id="9f0da-143">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="9f0da-143">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="9f0da-144">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="9f0da-144">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="9f0da-145">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="9f0da-145">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

