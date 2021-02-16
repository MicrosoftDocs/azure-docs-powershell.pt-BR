---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/undo-AzKeyvaultsecretremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
ms.openlocfilehash: 9c240d3902aeba38af4281ba31bacea76bad0a58
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399083"
---
# <span data-ttu-id="39eb8-101">Undo-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="39eb8-101">Undo-AzKeyVaultSecretRemoval</span></span>

## <span data-ttu-id="39eb8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="39eb8-102">SYNOPSIS</span></span>
<span data-ttu-id="39eb8-103">Recupera um segredo excluído em um cofre de chave em um estado ativo.</span><span class="sxs-lookup"><span data-stu-id="39eb8-103">Recovers a deleted secret in a key vault into an active state.</span></span>

## <span data-ttu-id="39eb8-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="39eb8-104">SYNTAX</span></span>

```
Undo-AzKeyVaultSecretRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="39eb8-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="39eb8-105">DESCRIPTION</span></span>
<span data-ttu-id="39eb8-106">O cmdlet **Undo-AzKeyVaultSec cuevaRemoval** recuperará um segredo excluído anteriormente.</span><span class="sxs-lookup"><span data-stu-id="39eb8-106">The **Undo-AzKeyVaultSecretRemoval** cmdlet will recover a previously deleted secret.</span></span>
<span data-ttu-id="39eb8-107">O segredo recuperado estará ativo e poderá ser usado para todas as operações secretas normais.</span><span class="sxs-lookup"><span data-stu-id="39eb8-107">The recovered secret will be active and can be used for all normal secret operations.</span></span>
<span data-ttu-id="39eb8-108">O chamador precisa ter permissão de "recuperar" para executar esta operação.</span><span class="sxs-lookup"><span data-stu-id="39eb8-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="39eb8-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="39eb8-109">EXAMPLES</span></span>

### <span data-ttu-id="39eb8-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="39eb8-110">Example 1</span></span>
```
PS C:\> Undo-AzKeyVaultSecretRemoval -VaultName 'MyKeyVault' -Name 'MySecret'
```

<span data-ttu-id="39eb8-111">Esse comando recuperará o segredo "MySecsecsec" que foi excluído anteriormente em um estado ativo e acessível.</span><span class="sxs-lookup"><span data-stu-id="39eb8-111">This command will recover the secret 'MySecret' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="39eb8-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="39eb8-112">PARAMETERS</span></span>

### <span data-ttu-id="39eb8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39eb8-113">-DefaultProfile</span></span>
<span data-ttu-id="39eb8-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="39eb8-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39eb8-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="39eb8-115">-Name</span></span>
<span data-ttu-id="39eb8-116">Nome secreto.</span><span class="sxs-lookup"><span data-stu-id="39eb8-116">Secret name.</span></span>
<span data-ttu-id="39eb8-117">O cmdlet constrói o FQDN de um segredo do nome do cofre, do ambiente selecionado no momento e do nome secreto.</span><span class="sxs-lookup"><span data-stu-id="39eb8-117">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39eb8-118">-Nomedo Cofre</span><span class="sxs-lookup"><span data-stu-id="39eb8-118">-VaultName</span></span>
<span data-ttu-id="39eb8-119">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="39eb8-119">Vault name.</span></span>
<span data-ttu-id="39eb8-120">O Cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="39eb8-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39eb8-121">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="39eb8-121">-Confirm</span></span>
<span data-ttu-id="39eb8-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="39eb8-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39eb8-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39eb8-123">-WhatIf</span></span>
<span data-ttu-id="39eb8-124">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="39eb8-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39eb8-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="39eb8-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39eb8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39eb8-126">CommonParameters</span></span>
<span data-ttu-id="39eb8-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39eb8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39eb8-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39eb8-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39eb8-129">Entradas</span><span class="sxs-lookup"><span data-stu-id="39eb8-129">INPUTS</span></span>

### <span data-ttu-id="39eb8-130">System.String</span><span class="sxs-lookup"><span data-stu-id="39eb8-130">System.String</span></span>

## <span data-ttu-id="39eb8-131">Saídas</span><span class="sxs-lookup"><span data-stu-id="39eb8-131">OUTPUTS</span></span>

### <span data-ttu-id="39eb8-132">Microsoft.Azure.Commands.KeyVault.Models.Secret</span><span class="sxs-lookup"><span data-stu-id="39eb8-132">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>

## <span data-ttu-id="39eb8-133">Notas</span><span class="sxs-lookup"><span data-stu-id="39eb8-133">NOTES</span></span>

## <span data-ttu-id="39eb8-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="39eb8-134">RELATED LINKS</span></span>

[<span data-ttu-id="39eb8-135">Remove-AzKeyVaultSec cue</span><span class="sxs-lookup"><span data-stu-id="39eb8-135">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)


[<span data-ttu-id="39eb8-136">Get-AzKeyVaultSec cue</span><span class="sxs-lookup"><span data-stu-id="39eb8-136">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)
