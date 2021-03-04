---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/undo-azkeyvaultsecretremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
ms.openlocfilehash: dc4c8925d4ddf00cc2e2739d3aa06285f628e423
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888510"
---
# <span data-ttu-id="4f454-101">Undo-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="4f454-101">Undo-AzKeyVaultSecretRemoval</span></span>

## <span data-ttu-id="4f454-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f454-102">SYNOPSIS</span></span>
<span data-ttu-id="4f454-103">Recupera um segredo excluído em um cofre de chaves em um estado ativo.</span><span class="sxs-lookup"><span data-stu-id="4f454-103">Recovers a deleted secret in a key vault into an active state.</span></span>

## <span data-ttu-id="4f454-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="4f454-104">SYNTAX</span></span>

### <span data-ttu-id="4f454-105">Padrão (Padrão)</span><span class="sxs-lookup"><span data-stu-id="4f454-105">Default (Default)</span></span>
```
Undo-AzKeyVaultSecretRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4f454-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="4f454-106">InputObject</span></span>
```
Undo-AzKeyVaultSecretRemoval [-InputObject] <PSDeletedKeyVaultSecretIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f454-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="4f454-107">DESCRIPTION</span></span>
<span data-ttu-id="4f454-108">O cmdlet **Undo-AzKeyVaultSecretRemoval** recuperará um segredo excluído anteriormente.</span><span class="sxs-lookup"><span data-stu-id="4f454-108">The **Undo-AzKeyVaultSecretRemoval** cmdlet will recover a previously deleted secret.</span></span>
<span data-ttu-id="4f454-109">O segredo recuperado estará ativo e poderá ser usado para todas as operações secretas normais.</span><span class="sxs-lookup"><span data-stu-id="4f454-109">The recovered secret will be active and can be used for all normal secret operations.</span></span>
<span data-ttu-id="4f454-110">O chamador precisa ter permissão de 'recuperar' para executar essa operação.</span><span class="sxs-lookup"><span data-stu-id="4f454-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="4f454-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4f454-111">EXAMPLES</span></span>

### <span data-ttu-id="4f454-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4f454-112">Example 1</span></span>
```powershell
PS C:\> Undo-AzKeyVaultSecretRemoval -VaultName 'MyKeyVault' -Name 'MySecret'

Vault Name   : MyKeyVault
Name         : MySecret
Version      : f622abc7b1394092812f1eb0f85dc91c
Id           : https://mykeyvault.vault.azure.net:443/secrets/mysecret/f622abc7b1394092812f1eb0f85dc91c
Enabled      : True
Expires      :
Not Before   :
Created      : 4/19/2018 5:56:02 PM
Updated      : 4/26/2018 7:48:40 PM
Content Type :
Tags         :
```

<span data-ttu-id="4f454-113">Este comando recuperará o segredo 'MySecret' que foi excluído anteriormente, em um estado ativo e acessível.</span><span class="sxs-lookup"><span data-stu-id="4f454-113">This command will recover the secret 'MySecret' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="4f454-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="4f454-114">PARAMETERS</span></span>

### <span data-ttu-id="4f454-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f454-115">-DefaultProfile</span></span>
<span data-ttu-id="4f454-116">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="4f454-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4f454-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4f454-117">-InputObject</span></span>
<span data-ttu-id="4f454-118">Objeto secreto excluído</span><span class="sxs-lookup"><span data-stu-id="4f454-118">Deleted secret object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4f454-119">-Name</span><span class="sxs-lookup"><span data-stu-id="4f454-119">-Name</span></span>
<span data-ttu-id="4f454-120">Nome secreto.</span><span class="sxs-lookup"><span data-stu-id="4f454-120">Secret name.</span></span>
<span data-ttu-id="4f454-121">O cmdlet constrói o FQDN de um segredo do nome do cofre, do ambiente selecionado no momento e do nome secreto.</span><span class="sxs-lookup"><span data-stu-id="4f454-121">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f454-122">-VaultName</span><span class="sxs-lookup"><span data-stu-id="4f454-122">-VaultName</span></span>
<span data-ttu-id="4f454-123">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="4f454-123">Vault name.</span></span>
<span data-ttu-id="4f454-124">O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="4f454-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="4f454-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4f454-125">-Confirm</span></span>
<span data-ttu-id="4f454-126">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f454-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f454-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f454-127">-WhatIf</span></span>
<span data-ttu-id="4f454-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4f454-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f454-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4f454-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f454-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f454-130">CommonParameters</span></span>
<span data-ttu-id="4f454-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f454-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f454-132">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4f454-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f454-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4f454-133">INPUTS</span></span>

### <span data-ttu-id="4f454-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="4f454-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="4f454-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="4f454-135">OUTPUTS</span></span>

### <span data-ttu-id="4f454-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="4f454-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="4f454-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="4f454-137">NOTES</span></span>

## <span data-ttu-id="4f454-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4f454-138">RELATED LINKS</span></span>

[<span data-ttu-id="4f454-139">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="4f454-139">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

[<span data-ttu-id="4f454-140">Add-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="4f454-140">Add-AzKeyVaultSecret</span></span>](./Add-AzKeyVaultSecret.md)

[<span data-ttu-id="4f454-141">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="4f454-141">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)
