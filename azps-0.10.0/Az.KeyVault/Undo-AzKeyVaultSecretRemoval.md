---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/undo-AzKeyvaultsecretremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultSecretRemoval.md
ms.openlocfilehash: e65bef4119c51b989287bbf0db2e7587fef50271
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776640"
---
# <span data-ttu-id="722f8-101">Undo-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="722f8-101">Undo-AzKeyVaultSecretRemoval</span></span>

## <span data-ttu-id="722f8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="722f8-102">SYNOPSIS</span></span>
<span data-ttu-id="722f8-103">Recupera um segredo excluído em um cofre de chaves para um estado ativo.</span><span class="sxs-lookup"><span data-stu-id="722f8-103">Recovers a deleted secret in a key vault into an active state.</span></span>

## <span data-ttu-id="722f8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="722f8-104">SYNTAX</span></span>

```
Undo-AzKeyVaultSecretRemoval [-VaultName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="722f8-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="722f8-105">DESCRIPTION</span></span>
<span data-ttu-id="722f8-106">O cmdlet **Undo-AzKeyVaultSecretRemoval** recuperará um segredo excluído anteriormente.</span><span class="sxs-lookup"><span data-stu-id="722f8-106">The **Undo-AzKeyVaultSecretRemoval** cmdlet will recover a previously deleted secret.</span></span>
<span data-ttu-id="722f8-107">O segredo recuperado estará ativo e poderá ser usado para todas as operações de segredo normal.</span><span class="sxs-lookup"><span data-stu-id="722f8-107">The recovered secret will be active and can be used for all normal secret operations.</span></span>
<span data-ttu-id="722f8-108">O chamador precisa ter a permissão ' recuperar ' para executar essa operação.</span><span class="sxs-lookup"><span data-stu-id="722f8-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="722f8-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="722f8-109">EXAMPLES</span></span>

### <span data-ttu-id="722f8-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="722f8-110">Example 1</span></span>
```
PS C:\> Undo-AzKeyVaultSecretRemoval -VaultName 'MyKeyVault' -Name 'MySecret'
```

<span data-ttu-id="722f8-111">Esse comando recuperará o segredo ' MySecret ', que foi excluído anteriormente, em um estado ativo e utilizável.</span><span class="sxs-lookup"><span data-stu-id="722f8-111">This command will recover the secret 'MySecret' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="722f8-112">OS</span><span class="sxs-lookup"><span data-stu-id="722f8-112">PARAMETERS</span></span>

### <span data-ttu-id="722f8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="722f8-113">-DefaultProfile</span></span>
<span data-ttu-id="722f8-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="722f8-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="722f8-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="722f8-115">-Name</span></span>
<span data-ttu-id="722f8-116">Nome do segredo.</span><span class="sxs-lookup"><span data-stu-id="722f8-116">Secret name.</span></span>
<span data-ttu-id="722f8-117">O cmdlet constrói o FQDN de um segredo do nome do cofre, do ambiente selecionado no momento e do nome do segredo.</span><span class="sxs-lookup"><span data-stu-id="722f8-117">Cmdlet constructs the FQDN of a secret from vault name, currently selected environment and secret name.</span></span>

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

### <span data-ttu-id="722f8-118">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="722f8-118">-VaultName</span></span>
<span data-ttu-id="722f8-119">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="722f8-119">Vault name.</span></span>
<span data-ttu-id="722f8-120">O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="722f8-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="722f8-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="722f8-121">-Confirm</span></span>
<span data-ttu-id="722f8-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="722f8-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="722f8-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="722f8-123">-WhatIf</span></span>
<span data-ttu-id="722f8-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="722f8-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="722f8-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="722f8-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="722f8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="722f8-126">CommonParameters</span></span>
<span data-ttu-id="722f8-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="722f8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="722f8-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="722f8-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="722f8-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="722f8-129">INPUTS</span></span>

### <span data-ttu-id="722f8-130">System. String</span><span class="sxs-lookup"><span data-stu-id="722f8-130">System.String</span></span>

## <span data-ttu-id="722f8-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="722f8-131">OUTPUTS</span></span>

### <span data-ttu-id="722f8-132">Microsoft. Azure. Commands. keyvault. Models. Secret</span><span class="sxs-lookup"><span data-stu-id="722f8-132">Microsoft.Azure.Commands.KeyVault.Models.Secret</span></span>

## <span data-ttu-id="722f8-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="722f8-133">NOTES</span></span>

## <span data-ttu-id="722f8-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="722f8-134">RELATED LINKS</span></span>

[<span data-ttu-id="722f8-135">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="722f8-135">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

[<span data-ttu-id="722f8-136">Add-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="722f8-136">Add-AzKeyVaultSecret</span></span>](./Add-AzKeyVaultSecret.md)

[<span data-ttu-id="722f8-137">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="722f8-137">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)
