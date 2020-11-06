---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurekeyvaultsecretremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultSecretRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultSecretRemoval.md
ms.openlocfilehash: 07c62b1b106453cf9b19610867be39458943bcab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93431667"
---
# <span data-ttu-id="f6aff-101">Undo-AzureKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="f6aff-101">Undo-AzureKeyVaultSecretRemoval</span></span>

## <span data-ttu-id="f6aff-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f6aff-102">SYNOPSIS</span></span>
<span data-ttu-id="f6aff-103">Recupera um segredo excluído em um cofre de chaves para um estado ativo.</span><span class="sxs-lookup"><span data-stu-id="f6aff-103">Recovers a deleted secret in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6aff-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f6aff-104">SYNTAX</span></span>

### <span data-ttu-id="f6aff-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="f6aff-105">Default (Default)</span></span>
```
Undo-AzureKeyVaultSecretRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6aff-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="f6aff-106">InputObject</span></span>
```
Undo-AzureKeyVaultSecretRemoval [-InputObject] <PSDeletedKeyVaultSecretIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6aff-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="f6aff-107">DESCRIPTION</span></span>
<span data-ttu-id="f6aff-108">O cmdlet **Undo-AzureKeyVaultSecretRemoval** recuperará um segredo excluído anteriormente.</span><span class="sxs-lookup"><span data-stu-id="f6aff-108">The **Undo-AzureKeyVaultSecretRemoval** cmdlet will recover a previously deleted secret.</span></span>
<span data-ttu-id="f6aff-109">O segredo recuperado estará ativo e poderá ser usado para todas as operações de segredo normal.</span><span class="sxs-lookup"><span data-stu-id="f6aff-109">The recovered secret will be active and can be used for all normal secret operations.</span></span>
<span data-ttu-id="f6aff-110">O chamador precisa ter a permissão ' recuperar ' para executar essa operação.</span><span class="sxs-lookup"><span data-stu-id="f6aff-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="f6aff-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="f6aff-111">EXAMPLES</span></span>

### <span data-ttu-id="f6aff-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="f6aff-112">Example 1</span></span>
```
PS C:\> Undo-AzureKeyVaultSecretRemoval -VaultName 'MyKeyVault' -Name 'MySecret'
```

<span data-ttu-id="f6aff-113">Esse comando recuperará o segredo ' MySecret ', que foi excluído anteriormente, em um estado ativo e utilizável.</span><span class="sxs-lookup"><span data-stu-id="f6aff-113">This command will recover the secret 'MySecret' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="f6aff-114">OS</span><span class="sxs-lookup"><span data-stu-id="f6aff-114">PARAMETERS</span></span>

### <span data-ttu-id="f6aff-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6aff-115">-DefaultProfile</span></span>
<span data-ttu-id="f6aff-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="f6aff-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f6aff-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f6aff-117">-InputObject</span></span>
<span data-ttu-id="f6aff-118">Objeto secreto excluído</span><span class="sxs-lookup"><span data-stu-id="f6aff-118">Deleted secret object</span></span>

```yaml
Type: PSDeletedKeyVaultSecretIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f6aff-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="f6aff-119">-Name</span></span>
<span data-ttu-id="f6aff-120">Nome do segredo.</span><span class="sxs-lookup"><span data-stu-id="f6aff-120">Secret name.</span></span>
<span data-ttu-id="f6aff-121">O cmdlet constrói o FQDN de um segredo do nome do cofre, do ambiente selecionado no momento e do nome do segredo.</span><span class="sxs-lookup"><span data-stu-id="f6aff-121">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6aff-122">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="f6aff-122">-VaultName</span></span>
<span data-ttu-id="f6aff-123">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="f6aff-123">Vault name.</span></span>
<span data-ttu-id="f6aff-124">O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="f6aff-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6aff-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="f6aff-125">-Confirm</span></span>
<span data-ttu-id="f6aff-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6aff-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6aff-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6aff-127">-WhatIf</span></span>
<span data-ttu-id="f6aff-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="f6aff-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6aff-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="f6aff-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6aff-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6aff-130">CommonParameters</span></span>
<span data-ttu-id="f6aff-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6aff-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6aff-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6aff-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6aff-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="f6aff-133">INPUTS</span></span>

### <span data-ttu-id="f6aff-134">System. String</span><span class="sxs-lookup"><span data-stu-id="f6aff-134">System.String</span></span>

## <span data-ttu-id="f6aff-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="f6aff-135">OUTPUTS</span></span>

### <span data-ttu-id="f6aff-136">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="f6aff-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="f6aff-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="f6aff-137">NOTES</span></span>

## <span data-ttu-id="f6aff-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f6aff-138">RELATED LINKS</span></span>

[<span data-ttu-id="f6aff-139">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="f6aff-139">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)

[<span data-ttu-id="f6aff-140">Add-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="f6aff-140">Add-AzureKeyVaultSecret</span></span>](./Add-AzureKeyVaultSecret.md)

[<span data-ttu-id="f6aff-141">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="f6aff-141">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)
