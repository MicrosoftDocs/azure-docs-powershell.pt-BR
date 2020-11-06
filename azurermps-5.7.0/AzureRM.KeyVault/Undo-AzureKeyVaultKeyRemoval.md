---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurekeyvaultkeyremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultKeyRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureKeyVaultKeyRemoval.md
ms.openlocfilehash: 29a7c2d3bb2060b77871cea0c088c50a59197cb1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93427548"
---
# <span data-ttu-id="32941-101">Undo-AzureKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="32941-101">Undo-AzureKeyVaultKeyRemoval</span></span>

## <span data-ttu-id="32941-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="32941-102">SYNOPSIS</span></span>
<span data-ttu-id="32941-103">Recupera uma chave excluída em um cofre de chaves para um estado ativo.</span><span class="sxs-lookup"><span data-stu-id="32941-103">Recovers a deleted key in a key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32941-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="32941-104">SYNTAX</span></span>

### <span data-ttu-id="32941-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="32941-105">Default (Default)</span></span>
```
Undo-AzureKeyVaultKeyRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32941-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="32941-106">InputObject</span></span>
```
Undo-AzureKeyVaultKeyRemoval [-InputObject] <PSDeletedKeyVaultKeyIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32941-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="32941-107">DESCRIPTION</span></span>
<span data-ttu-id="32941-108">O cmdlet **Undo-AzureKeyVaultKeyRemoval** recuperará uma chave previamente excluída.</span><span class="sxs-lookup"><span data-stu-id="32941-108">The **Undo-AzureKeyVaultKeyRemoval** cmdlet will recover a previously deleted key.</span></span>
<span data-ttu-id="32941-109">A chave recuperada estará ativa e poderá ser usada para todas as operações de chave normais.</span><span class="sxs-lookup"><span data-stu-id="32941-109">The recovered key will be active and can be used for all normal key operations.</span></span>
<span data-ttu-id="32941-110">O chamador precisa ter a permissão ' recuperar ' para executar essa operação.</span><span class="sxs-lookup"><span data-stu-id="32941-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="32941-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="32941-111">EXAMPLES</span></span>

### <span data-ttu-id="32941-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="32941-112">Example 1</span></span>
```
PS C:\>Undo-AzureKeyVaultKeyRemoval -VaultName 'MyKeyVault' -Name 'MyKey'
```

<span data-ttu-id="32941-113">Esse comando recuperará a chave ' MyKey ' que foi excluída anteriormente, em um estado ativo e utilizável.</span><span class="sxs-lookup"><span data-stu-id="32941-113">This command will recover the key 'MyKey' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="32941-114">OS</span><span class="sxs-lookup"><span data-stu-id="32941-114">PARAMETERS</span></span>

### <span data-ttu-id="32941-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32941-115">-DefaultProfile</span></span>
<span data-ttu-id="32941-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="32941-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="32941-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="32941-117">-InputObject</span></span>
<span data-ttu-id="32941-118">Objeto chave excluído</span><span class="sxs-lookup"><span data-stu-id="32941-118">Deleted key object</span></span>

```yaml
Type: PSDeletedKeyVaultKeyIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="32941-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="32941-119">-Name</span></span>
<span data-ttu-id="32941-120">Nome da chave.</span><span class="sxs-lookup"><span data-stu-id="32941-120">Key name.</span></span>
<span data-ttu-id="32941-121">O cmdlet constrói o FQDN de uma chave do nome do cofre, o ambiente selecionado no momento e o nome da chave.</span><span class="sxs-lookup"><span data-stu-id="32941-121">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32941-122">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="32941-122">-VaultName</span></span>
<span data-ttu-id="32941-123">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="32941-123">Vault name.</span></span>
<span data-ttu-id="32941-124">O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="32941-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="32941-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="32941-125">-Confirm</span></span>
<span data-ttu-id="32941-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32941-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32941-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32941-127">-WhatIf</span></span>
<span data-ttu-id="32941-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="32941-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32941-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="32941-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32941-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32941-130">CommonParameters</span></span>
<span data-ttu-id="32941-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32941-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32941-132">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32941-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32941-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="32941-133">INPUTS</span></span>

### <span data-ttu-id="32941-134">System. String</span><span class="sxs-lookup"><span data-stu-id="32941-134">System.String</span></span>

## <span data-ttu-id="32941-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="32941-135">OUTPUTS</span></span>

### <span data-ttu-id="32941-136">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="32941-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="32941-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="32941-137">NOTES</span></span>

## <span data-ttu-id="32941-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="32941-138">RELATED LINKS</span></span>

[<span data-ttu-id="32941-139">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="32941-139">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

[<span data-ttu-id="32941-140">Add-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="32941-140">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="32941-141">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="32941-141">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

