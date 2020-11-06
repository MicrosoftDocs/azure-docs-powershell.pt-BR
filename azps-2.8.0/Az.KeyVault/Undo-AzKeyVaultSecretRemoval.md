---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultsecretremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
ms.openlocfilehash: 26bf7b91b330032e05f96f425cb21908fc3df55d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596130"
---
# <span data-ttu-id="7ef62-101">Undo-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="7ef62-101">Undo-AzKeyVaultSecretRemoval</span></span>

## <span data-ttu-id="7ef62-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="7ef62-102">SYNOPSIS</span></span>
<span data-ttu-id="7ef62-103">Recupera um segredo excluído em um cofre de chaves para um estado ativo.</span><span class="sxs-lookup"><span data-stu-id="7ef62-103">Recovers a deleted secret in a key vault into an active state.</span></span>

## <span data-ttu-id="7ef62-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7ef62-104">SYNTAX</span></span>

### <span data-ttu-id="7ef62-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="7ef62-105">Default (Default)</span></span>
```
Undo-AzKeyVaultSecretRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ef62-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="7ef62-106">InputObject</span></span>
```
Undo-AzKeyVaultSecretRemoval [-InputObject] <PSDeletedKeyVaultSecretIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ef62-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="7ef62-107">DESCRIPTION</span></span>
<span data-ttu-id="7ef62-108">O cmdlet **Undo-AzKeyVaultSecretRemoval** recuperará um segredo excluído anteriormente.</span><span class="sxs-lookup"><span data-stu-id="7ef62-108">The **Undo-AzKeyVaultSecretRemoval** cmdlet will recover a previously deleted secret.</span></span>
<span data-ttu-id="7ef62-109">O segredo recuperado estará ativo e poderá ser usado para todas as operações de segredo normal.</span><span class="sxs-lookup"><span data-stu-id="7ef62-109">The recovered secret will be active and can be used for all normal secret operations.</span></span>
<span data-ttu-id="7ef62-110">O chamador precisa ter a permissão ' recuperar ' para executar essa operação.</span><span class="sxs-lookup"><span data-stu-id="7ef62-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="7ef62-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7ef62-111">EXAMPLES</span></span>

### <span data-ttu-id="7ef62-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7ef62-112">Example 1</span></span>
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

<span data-ttu-id="7ef62-113">Esse comando recuperará o segredo ' MySecret ', que foi excluído anteriormente, em um estado ativo e utilizável.</span><span class="sxs-lookup"><span data-stu-id="7ef62-113">This command will recover the secret 'MySecret' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="7ef62-114">OS</span><span class="sxs-lookup"><span data-stu-id="7ef62-114">PARAMETERS</span></span>

### <span data-ttu-id="7ef62-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ef62-115">-DefaultProfile</span></span>
<span data-ttu-id="7ef62-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="7ef62-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7ef62-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7ef62-117">-InputObject</span></span>
<span data-ttu-id="7ef62-118">Objeto secreto excluído</span><span class="sxs-lookup"><span data-stu-id="7ef62-118">Deleted secret object</span></span>

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

### <span data-ttu-id="7ef62-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="7ef62-119">-Name</span></span>
<span data-ttu-id="7ef62-120">Nome do segredo.</span><span class="sxs-lookup"><span data-stu-id="7ef62-120">Secret name.</span></span>
<span data-ttu-id="7ef62-121">O cmdlet constrói o FQDN de um segredo do nome do cofre, do ambiente selecionado no momento e do nome do segredo.</span><span class="sxs-lookup"><span data-stu-id="7ef62-121">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="7ef62-122">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="7ef62-122">-VaultName</span></span>
<span data-ttu-id="7ef62-123">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="7ef62-123">Vault name.</span></span>
<span data-ttu-id="7ef62-124">O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="7ef62-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="7ef62-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="7ef62-125">-Confirm</span></span>
<span data-ttu-id="7ef62-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ef62-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ef62-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ef62-127">-WhatIf</span></span>
<span data-ttu-id="7ef62-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7ef62-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ef62-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7ef62-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ef62-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ef62-130">CommonParameters</span></span>
<span data-ttu-id="7ef62-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ef62-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ef62-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ef62-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ef62-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="7ef62-133">INPUTS</span></span>

### <span data-ttu-id="7ef62-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="7ef62-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="7ef62-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="7ef62-135">OUTPUTS</span></span>

### <span data-ttu-id="7ef62-136">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="7ef62-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="7ef62-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="7ef62-137">NOTES</span></span>

## <span data-ttu-id="7ef62-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7ef62-138">RELATED LINKS</span></span>

[<span data-ttu-id="7ef62-139">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="7ef62-139">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

[<span data-ttu-id="7ef62-140">Add-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="7ef62-140">Add-AzKeyVaultSecret</span></span>](./Add-AzKeyVaultSecret.md)

[<span data-ttu-id="7ef62-141">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="7ef62-141">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)
