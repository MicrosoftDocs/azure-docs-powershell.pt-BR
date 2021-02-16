---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultsecretremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
ms.openlocfilehash: 9513cba1532ec70acb77cdf97d19de25db36434f
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100397927"
---
# <span data-ttu-id="b2a1c-101">Undo-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="b2a1c-101">Undo-AzKeyVaultSecretRemoval</span></span>

## <span data-ttu-id="b2a1c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b2a1c-102">SYNOPSIS</span></span>
<span data-ttu-id="b2a1c-103">Recupera um segredo excluído em um cofre de chave em um estado ativo.</span><span class="sxs-lookup"><span data-stu-id="b2a1c-103">Recovers a deleted secret in a key vault into an active state.</span></span>

## <span data-ttu-id="b2a1c-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b2a1c-104">SYNTAX</span></span>

### <span data-ttu-id="b2a1c-105">Padrão (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b2a1c-105">Default (Default)</span></span>
```
Undo-AzKeyVaultSecretRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b2a1c-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="b2a1c-106">InputObject</span></span>
```
Undo-AzKeyVaultSecretRemoval [-InputObject] <PSDeletedKeyVaultSecretIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2a1c-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="b2a1c-107">DESCRIPTION</span></span>
<span data-ttu-id="b2a1c-108">O cmdlet **Undo-AzKeyVaultSecsecoval** recuperará um segredo excluído anteriormente.</span><span class="sxs-lookup"><span data-stu-id="b2a1c-108">The **Undo-AzKeyVaultSecretRemoval** cmdlet will recover a previously deleted secret.</span></span>
<span data-ttu-id="b2a1c-109">O segredo recuperado estará ativo e poderá ser usado para todas as operações secretas normais.</span><span class="sxs-lookup"><span data-stu-id="b2a1c-109">The recovered secret will be active and can be used for all normal secret operations.</span></span>
<span data-ttu-id="b2a1c-110">O chamador precisa ter permissão de 'recuperar' para executar esta operação.</span><span class="sxs-lookup"><span data-stu-id="b2a1c-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="b2a1c-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b2a1c-111">EXAMPLES</span></span>

### <span data-ttu-id="b2a1c-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b2a1c-112">Example 1</span></span>
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

<span data-ttu-id="b2a1c-113">Esse comando recuperará o segredo "MySecsecsec" que foi excluído anteriormente em um estado ativo e acessível.</span><span class="sxs-lookup"><span data-stu-id="b2a1c-113">This command will recover the secret 'MySecret' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="b2a1c-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b2a1c-114">PARAMETERS</span></span>

### <span data-ttu-id="b2a1c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2a1c-115">-DefaultProfile</span></span>
<span data-ttu-id="b2a1c-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="b2a1c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b2a1c-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b2a1c-117">-InputObject</span></span>
<span data-ttu-id="b2a1c-118">Objeto secreto excluído</span><span class="sxs-lookup"><span data-stu-id="b2a1c-118">Deleted secret object</span></span>

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

### <span data-ttu-id="b2a1c-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="b2a1c-119">-Name</span></span>
<span data-ttu-id="b2a1c-120">Nome secreto.</span><span class="sxs-lookup"><span data-stu-id="b2a1c-120">Secret name.</span></span>
<span data-ttu-id="b2a1c-121">O Cmdlet constrói o FQDN de um segredo do nome do cofre, do ambiente selecionado no momento e do nome secreto.</span><span class="sxs-lookup"><span data-stu-id="b2a1c-121">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="b2a1c-122">-Nomedo Cofre</span><span class="sxs-lookup"><span data-stu-id="b2a1c-122">-VaultName</span></span>
<span data-ttu-id="b2a1c-123">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="b2a1c-123">Vault name.</span></span>
<span data-ttu-id="b2a1c-124">O Cmdlet construirá o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="b2a1c-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="b2a1c-125">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="b2a1c-125">-Confirm</span></span>
<span data-ttu-id="b2a1c-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b2a1c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2a1c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2a1c-127">-WhatIf</span></span>
<span data-ttu-id="b2a1c-128">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="b2a1c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b2a1c-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b2a1c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2a1c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2a1c-130">CommonParameters</span></span>
<span data-ttu-id="b2a1c-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2a1c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2a1c-132">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b2a1c-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2a1c-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="b2a1c-133">INPUTS</span></span>

### <span data-ttu-id="b2a1c-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecitorIdentityItem</span><span class="sxs-lookup"><span data-stu-id="b2a1c-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="b2a1c-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="b2a1c-135">OUTPUTS</span></span>

### <span data-ttu-id="b2a1c-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSec cue</span><span class="sxs-lookup"><span data-stu-id="b2a1c-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="b2a1c-137">Notas</span><span class="sxs-lookup"><span data-stu-id="b2a1c-137">NOTES</span></span>

## <span data-ttu-id="b2a1c-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b2a1c-138">RELATED LINKS</span></span>

[<span data-ttu-id="b2a1c-139">Remove-AzKeyVaultSec cue</span><span class="sxs-lookup"><span data-stu-id="b2a1c-139">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)


[<span data-ttu-id="b2a1c-140">Get-AzKeyVaultSec cue</span><span class="sxs-lookup"><span data-stu-id="b2a1c-140">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)
