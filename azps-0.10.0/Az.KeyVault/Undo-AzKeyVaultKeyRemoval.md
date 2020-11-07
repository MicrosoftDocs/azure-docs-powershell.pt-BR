---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/undo-AzKeyvaultkeyremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultKeyRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Undo-AzKeyVaultKeyRemoval.md
ms.openlocfilehash: 5b0e67fbbead536803dba8efeb2c8a61d7f75c5a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776645"
---
# <span data-ttu-id="e1702-101">Undo-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="e1702-101">Undo-AzKeyVaultKeyRemoval</span></span>

## <span data-ttu-id="e1702-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e1702-102">SYNOPSIS</span></span>
<span data-ttu-id="e1702-103">Recupera uma chave excluída em um cofre de chaves para um estado ativo.</span><span class="sxs-lookup"><span data-stu-id="e1702-103">Recovers a deleted key in a key vault into an active state.</span></span>

## <span data-ttu-id="e1702-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e1702-104">SYNTAX</span></span>

```
Undo-AzKeyVaultKeyRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1702-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e1702-105">DESCRIPTION</span></span>
<span data-ttu-id="e1702-106">O cmdlet **Undo-AzKeyVaultKeyRemoval** recuperará uma chave previamente excluída.</span><span class="sxs-lookup"><span data-stu-id="e1702-106">The **Undo-AzKeyVaultKeyRemoval** cmdlet will recover a previously deleted key.</span></span>
<span data-ttu-id="e1702-107">A chave recuperada estará ativa e poderá ser usada para todas as operações de chave normais.</span><span class="sxs-lookup"><span data-stu-id="e1702-107">The recovered key will be active and can be used for all normal key operations.</span></span>
<span data-ttu-id="e1702-108">O chamador precisa ter a permissão ' recuperar ' para executar essa operação.</span><span class="sxs-lookup"><span data-stu-id="e1702-108">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="e1702-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e1702-109">EXAMPLES</span></span>

### <span data-ttu-id="e1702-110">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e1702-110">Example 1</span></span>
```
PS C:\>Undo-AzKeyVaultKeyRemoval -VaultName 'MyKeyVault' -Name 'MyKey'
```

<span data-ttu-id="e1702-111">Esse comando recuperará a chave ' MyKey ' que foi excluída anteriormente, em um estado ativo e utilizável.</span><span class="sxs-lookup"><span data-stu-id="e1702-111">This command will recover the key 'MyKey' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="e1702-112">OS</span><span class="sxs-lookup"><span data-stu-id="e1702-112">PARAMETERS</span></span>

### <span data-ttu-id="e1702-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1702-113">-DefaultProfile</span></span>
<span data-ttu-id="e1702-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="e1702-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e1702-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="e1702-115">-Name</span></span>
<span data-ttu-id="e1702-116">Nome da chave.</span><span class="sxs-lookup"><span data-stu-id="e1702-116">Key name.</span></span>
<span data-ttu-id="e1702-117">O cmdlet constrói o FQDN de uma chave do nome do cofre, o ambiente selecionado no momento e o nome da chave.</span><span class="sxs-lookup"><span data-stu-id="e1702-117">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1702-118">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="e1702-118">-VaultName</span></span>
<span data-ttu-id="e1702-119">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="e1702-119">Vault name.</span></span>
<span data-ttu-id="e1702-120">O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="e1702-120">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="e1702-121">-Confirme</span><span class="sxs-lookup"><span data-stu-id="e1702-121">-Confirm</span></span>
<span data-ttu-id="e1702-122">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1702-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1702-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1702-123">-WhatIf</span></span>
<span data-ttu-id="e1702-124">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="e1702-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1702-125">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="e1702-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1702-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1702-126">CommonParameters</span></span>
<span data-ttu-id="e1702-127">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1702-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1702-128">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1702-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1702-129">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e1702-129">INPUTS</span></span>

### <span data-ttu-id="e1702-130">System. String</span><span class="sxs-lookup"><span data-stu-id="e1702-130">System.String</span></span>

## <span data-ttu-id="e1702-131">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e1702-131">OUTPUTS</span></span>

### <span data-ttu-id="e1702-132">Microsoft. Azure. Commands. keyvault. Models. keybundle</span><span class="sxs-lookup"><span data-stu-id="e1702-132">Microsoft.Azure.Commands.KeyVault.Models.KeyBundle</span></span>

## <span data-ttu-id="e1702-133">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e1702-133">NOTES</span></span>

## <span data-ttu-id="e1702-134">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e1702-134">RELATED LINKS</span></span>

[<span data-ttu-id="e1702-135">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e1702-135">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="e1702-136">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e1702-136">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="e1702-137">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e1702-137">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

