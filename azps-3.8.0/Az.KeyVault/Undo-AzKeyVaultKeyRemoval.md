---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultkeyremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultKeyRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultKeyRemoval.md
ms.openlocfilehash: c2b4fec2524ed3ddac62cf687af33ba3f76f13e8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93777747"
---
# <span data-ttu-id="99c21-101">Undo-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="99c21-101">Undo-AzKeyVaultKeyRemoval</span></span>

## <span data-ttu-id="99c21-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="99c21-102">SYNOPSIS</span></span>
<span data-ttu-id="99c21-103">Recupera uma chave excluída em um cofre de chaves para um estado ativo.</span><span class="sxs-lookup"><span data-stu-id="99c21-103">Recovers a deleted key in a key vault into an active state.</span></span>

## <span data-ttu-id="99c21-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="99c21-104">SYNTAX</span></span>

### <span data-ttu-id="99c21-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="99c21-105">Default (Default)</span></span>
```
Undo-AzKeyVaultKeyRemoval [-VaultName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99c21-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="99c21-106">InputObject</span></span>
```
Undo-AzKeyVaultKeyRemoval [-InputObject] <PSDeletedKeyVaultKeyIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="99c21-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="99c21-107">DESCRIPTION</span></span>
<span data-ttu-id="99c21-108">O cmdlet **Undo-AzKeyVaultKeyRemoval** recuperará uma chave previamente excluída.</span><span class="sxs-lookup"><span data-stu-id="99c21-108">The **Undo-AzKeyVaultKeyRemoval** cmdlet will recover a previously deleted key.</span></span>
<span data-ttu-id="99c21-109">A chave recuperada estará ativa e poderá ser usada para todas as operações de chave normais.</span><span class="sxs-lookup"><span data-stu-id="99c21-109">The recovered key will be active and can be used for all normal key operations.</span></span>
<span data-ttu-id="99c21-110">O chamador precisa ter a permissão ' recuperar ' para executar essa operação.</span><span class="sxs-lookup"><span data-stu-id="99c21-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="99c21-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="99c21-111">EXAMPLES</span></span>

### <span data-ttu-id="99c21-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="99c21-112">Example 1</span></span>
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

<span data-ttu-id="99c21-113">Esse comando recuperará a chave ' MyKey ' que foi excluída anteriormente, em um estado ativo e utilizável.</span><span class="sxs-lookup"><span data-stu-id="99c21-113">This command will recover the key 'MyKey' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="99c21-114">OS</span><span class="sxs-lookup"><span data-stu-id="99c21-114">PARAMETERS</span></span>

### <span data-ttu-id="99c21-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99c21-115">-DefaultProfile</span></span>
<span data-ttu-id="99c21-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="99c21-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="99c21-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="99c21-117">-InputObject</span></span>
<span data-ttu-id="99c21-118">Objeto chave excluído</span><span class="sxs-lookup"><span data-stu-id="99c21-118">Deleted key object</span></span>

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

### <span data-ttu-id="99c21-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="99c21-119">-Name</span></span>
<span data-ttu-id="99c21-120">Nome da chave.</span><span class="sxs-lookup"><span data-stu-id="99c21-120">Key name.</span></span>
<span data-ttu-id="99c21-121">O cmdlet constrói o FQDN de uma chave do nome do cofre, o ambiente selecionado no momento e o nome da chave.</span><span class="sxs-lookup"><span data-stu-id="99c21-121">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99c21-122">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="99c21-122">-VaultName</span></span>
<span data-ttu-id="99c21-123">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="99c21-123">Vault name.</span></span>
<span data-ttu-id="99c21-124">O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="99c21-124">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="99c21-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="99c21-125">-Confirm</span></span>
<span data-ttu-id="99c21-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99c21-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99c21-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99c21-127">-WhatIf</span></span>
<span data-ttu-id="99c21-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="99c21-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="99c21-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="99c21-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99c21-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99c21-130">CommonParameters</span></span>
<span data-ttu-id="99c21-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99c21-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99c21-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="99c21-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99c21-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="99c21-133">INPUTS</span></span>

### <span data-ttu-id="99c21-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="99c21-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="99c21-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="99c21-135">OUTPUTS</span></span>

### <span data-ttu-id="99c21-136">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="99c21-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="99c21-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="99c21-137">NOTES</span></span>

## <span data-ttu-id="99c21-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="99c21-138">RELATED LINKS</span></span>

[<span data-ttu-id="99c21-139">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="99c21-139">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="99c21-140">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="99c21-140">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="99c21-141">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="99c21-141">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

