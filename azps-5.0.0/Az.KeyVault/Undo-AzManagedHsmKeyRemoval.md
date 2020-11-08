---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azmanagedhsmkeyremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzManagedHsmKeyRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzManagedHsmKeyRemoval.md
ms.openlocfilehash: be1713584a1d0ce897c1c728f6aa7ae8b6ca3255
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115280"
---
# <span data-ttu-id="fe77c-101">Undo-AzManagedHsmKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="fe77c-101">Undo-AzManagedHsmKeyRemoval</span></span>

## <span data-ttu-id="fe77c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fe77c-102">SYNOPSIS</span></span>
<span data-ttu-id="fe77c-103">Recupera uma chave excluída em um HSM gerenciado em um estado ativo.</span><span class="sxs-lookup"><span data-stu-id="fe77c-103">Recovers a deleted key in a managed HSM into an active state.</span></span>

## <span data-ttu-id="fe77c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fe77c-104">SYNTAX</span></span>

### <span data-ttu-id="fe77c-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="fe77c-105">Default (Default)</span></span>
```
Undo-AzManagedHsmKeyRemoval [-HsmName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe77c-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="fe77c-106">InputObject</span></span>
```
Undo-AzManagedHsmKeyRemoval [-InputObject] <PSDeletedKeyVaultKeyIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe77c-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fe77c-107">DESCRIPTION</span></span>
<span data-ttu-id="fe77c-108">O cmdlet **Undo-AzManagedHsmKeyRemoval** recuperará uma chave previamente excluída.</span><span class="sxs-lookup"><span data-stu-id="fe77c-108">The **Undo-AzManagedHsmKeyRemoval** cmdlet will recover a previously deleted key.</span></span>
<span data-ttu-id="fe77c-109">A chave recuperada estará ativa e poderá ser usada para todas as operações de chave normais.</span><span class="sxs-lookup"><span data-stu-id="fe77c-109">The recovered key will be active and can be used for all normal key operations.</span></span>
<span data-ttu-id="fe77c-110">O chamador precisa ter a permissão ' recuperar ' para executar essa operação.</span><span class="sxs-lookup"><span data-stu-id="fe77c-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="fe77c-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fe77c-111">EXAMPLES</span></span>

### <span data-ttu-id="fe77c-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fe77c-112">Example 1</span></span>
```powershell
PS C:\> Undo-AzManagedHsmKeyRemoval -HsmName testmhsm -Name testkey001

Vault/HSM Name : testmhsm
Name           : testkey001
Version        : 7cff8510da04433b98144a3e33ad2bae
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey001/7cff8510da04433b98144a3e33ad2bae
Enabled        : True
Expires        :
Not Before     :
Created        : 10/14/2020 10:13:03 AM
Updated        : 10/14/2020 10:13:03 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="fe77c-113">Esse comando recuperará a chave ' testkey001 ' que foi excluída anteriormente, em um estado ativo e utilizável.</span><span class="sxs-lookup"><span data-stu-id="fe77c-113">This command will recover the key 'testkey001' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="fe77c-114">OS</span><span class="sxs-lookup"><span data-stu-id="fe77c-114">PARAMETERS</span></span>

### <span data-ttu-id="fe77c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe77c-115">-DefaultProfile</span></span>
<span data-ttu-id="fe77c-116">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fe77c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe77c-117">-HsmName</span><span class="sxs-lookup"><span data-stu-id="fe77c-117">-HsmName</span></span>
<span data-ttu-id="fe77c-118">Nome do HSM.</span><span class="sxs-lookup"><span data-stu-id="fe77c-118">HSM name.</span></span> <span data-ttu-id="fe77c-119">O cmdlet constrói o FQDN de um HSM gerenciado com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="fe77c-119">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="fe77c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fe77c-120">-InputObject</span></span>
<span data-ttu-id="fe77c-121">Objeto chave excluído</span><span class="sxs-lookup"><span data-stu-id="fe77c-121">Deleted key object</span></span>

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

### <span data-ttu-id="fe77c-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="fe77c-122">-Name</span></span>
<span data-ttu-id="fe77c-123">Nome da chave.</span><span class="sxs-lookup"><span data-stu-id="fe77c-123">Key name.</span></span>
<span data-ttu-id="fe77c-124">O cmdlet constrói o FQDN de uma chave do nome gerenciado do HSM, o ambiente selecionado no momento e o nome da chave.</span><span class="sxs-lookup"><span data-stu-id="fe77c-124">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment and key name.</span></span>

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

### <span data-ttu-id="fe77c-125">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fe77c-125">-Confirm</span></span>
<span data-ttu-id="fe77c-126">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe77c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe77c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe77c-127">-WhatIf</span></span>
<span data-ttu-id="fe77c-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fe77c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe77c-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fe77c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe77c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe77c-130">CommonParameters</span></span>
<span data-ttu-id="fe77c-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe77c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe77c-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fe77c-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe77c-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fe77c-133">INPUTS</span></span>

### <span data-ttu-id="fe77c-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="fe77c-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="fe77c-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fe77c-135">OUTPUTS</span></span>

### <span data-ttu-id="fe77c-136">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="fe77c-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="fe77c-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fe77c-137">NOTES</span></span>

## <span data-ttu-id="fe77c-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fe77c-138">RELATED LINKS</span></span>

[<span data-ttu-id="fe77c-139">Add-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="fe77c-139">Add-AzManagedHsmKey</span></span>](./Add-AzManagedHsmKey.md)

[<span data-ttu-id="fe77c-140">Backup-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="fe77c-140">Backup-AzManagedHsmKey</span></span>](./Backup-AzManagedHsmKey.md)

[<span data-ttu-id="fe77c-141">Remove-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="fe77c-141">Remove-AzManagedHsmKey</span></span>](./Remove-AzManagedHsmKey.md)

[<span data-ttu-id="fe77c-142">Restore-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="fe77c-142">Restore-AzManagedHsmKey</span></span>](./Restore-AzManagedHsmKey.md)

[<span data-ttu-id="fe77c-143">Get-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="fe77c-143">Get-AzManagedHsmKey</span></span>](./Get-AzManagedHsmKey.md)

[<span data-ttu-id="fe77c-144">Update-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="fe77c-144">Update-AzManagedHsmKey</span></span>](./Update-AzManagedHsmKey.md)