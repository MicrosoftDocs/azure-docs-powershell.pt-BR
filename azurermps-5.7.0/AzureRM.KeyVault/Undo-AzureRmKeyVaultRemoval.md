---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurermkeyvaultremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureRmKeyVaultRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Undo-AzureRmKeyVaultRemoval.md
ms.openlocfilehash: 83737a7643c78ef4ec41d84e153690b3a53a8d5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610391"
---
# <span data-ttu-id="704e7-101">Undo-AzureRmKeyVaultRemoval</span><span class="sxs-lookup"><span data-stu-id="704e7-101">Undo-AzureRmKeyVaultRemoval</span></span>

## <span data-ttu-id="704e7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="704e7-102">SYNOPSIS</span></span>
<span data-ttu-id="704e7-103">Recupera um cofre de chaves excluído para um estado ativo.</span><span class="sxs-lookup"><span data-stu-id="704e7-103">Recovers a deleted key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="704e7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="704e7-104">SYNTAX</span></span>

### <span data-ttu-id="704e7-105">Padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="704e7-105">Default (Default)</span></span>
```
Undo-AzureRmKeyVaultRemoval [-VaultName] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="704e7-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="704e7-106">InputObject</span></span>
```
Undo-AzureRmKeyVaultRemoval [-InputObject] <PSDeletedKeyVault> [-ResourceGroupName] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="704e7-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="704e7-107">DESCRIPTION</span></span>
<span data-ttu-id="704e7-108">O cmdlet **Undo-AzureRmKeyVaultRemoval** recuperará um cofre de chaves previamente excluído.</span><span class="sxs-lookup"><span data-stu-id="704e7-108">The **Undo-AzureRmKeyVaultRemoval** cmdlet will recover a previously deleted key vault.</span></span> <span data-ttu-id="704e7-109">O cofre recuperado estará ativo após a recuperação</span><span class="sxs-lookup"><span data-stu-id="704e7-109">The recovered vault will be active after recovery</span></span>

## <span data-ttu-id="704e7-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="704e7-110">EXAMPLES</span></span>

### <span data-ttu-id="704e7-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="704e7-111">Example 1</span></span>
```
PS C:\> Undo-AzureRmKeyVaultRemoval -VaultName 'MyKeyVault' -ResourceGroupName 'MyResourceGroup' -Location 'eastus2' -Tag @{"x"= "y"}
```

<span data-ttu-id="704e7-112">Esse comando recuperará o cofre de chave ' MyKeyVault ' que foi excluído anteriormente da região eastus2 e do grupo de recursos ' MyResource Group ', em um estado ativo e utilizável.</span><span class="sxs-lookup"><span data-stu-id="704e7-112">This command will recover the key vault 'MyKeyVault' that was previously deleted from eastus2 region and 'MyResourceGroup' resource group, into an active and usable state.</span></span> <span data-ttu-id="704e7-113">Ele também substitui as marcas por nova marca.</span><span class="sxs-lookup"><span data-stu-id="704e7-113">It also replaces the tags with new tag.</span></span>

## <span data-ttu-id="704e7-114">OS</span><span class="sxs-lookup"><span data-stu-id="704e7-114">PARAMETERS</span></span>

### <span data-ttu-id="704e7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="704e7-115">-DefaultProfile</span></span>
<span data-ttu-id="704e7-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="704e7-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="704e7-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="704e7-117">-InputObject</span></span>
<span data-ttu-id="704e7-118">Objeto do cofre excluído</span><span class="sxs-lookup"><span data-stu-id="704e7-118">Deleted vault object</span></span>

```yaml
Type: PSDeletedKeyVault
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="704e7-119">-Local</span><span class="sxs-lookup"><span data-stu-id="704e7-119">-Location</span></span>
<span data-ttu-id="704e7-120">Especifica a região original do Azure do cofre excluído.</span><span class="sxs-lookup"><span data-stu-id="704e7-120">Specifies the deleted vault original Azure region.</span></span>

```yaml
Type: String
Parameter Sets: Default
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="704e7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="704e7-121">-ResourceGroupName</span></span>
<span data-ttu-id="704e7-122">Especifica o nome de um grupo de recursos existente no qual criar o cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="704e7-122">Specifies the name of an existing resource group in which to create the key vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="704e7-123">-Marca</span><span class="sxs-lookup"><span data-stu-id="704e7-123">-Tag</span></span>
<span data-ttu-id="704e7-124">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="704e7-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="704e7-125">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="704e7-125">For example:</span></span>

<span data-ttu-id="704e7-126">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="704e7-126">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="704e7-127">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="704e7-127">-VaultName</span></span>
<span data-ttu-id="704e7-128">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="704e7-128">Vault name.</span></span>
<span data-ttu-id="704e7-129">O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="704e7-129">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="704e7-130">-Confirme</span><span class="sxs-lookup"><span data-stu-id="704e7-130">-Confirm</span></span>
<span data-ttu-id="704e7-131">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="704e7-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="704e7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="704e7-132">-WhatIf</span></span>
<span data-ttu-id="704e7-133">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="704e7-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="704e7-134">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="704e7-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="704e7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="704e7-135">CommonParameters</span></span>
<span data-ttu-id="704e7-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="704e7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="704e7-137">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="704e7-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="704e7-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="704e7-138">INPUTS</span></span>

### <span data-ttu-id="704e7-139">System. String</span><span class="sxs-lookup"><span data-stu-id="704e7-139">System.String</span></span>
<span data-ttu-id="704e7-140">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="704e7-140">System.Collections.Hashtable</span></span>

## <span data-ttu-id="704e7-141">EXIBE</span><span class="sxs-lookup"><span data-stu-id="704e7-141">OUTPUTS</span></span>

### <span data-ttu-id="704e7-142">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="704e7-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="704e7-143">INFORMA</span><span class="sxs-lookup"><span data-stu-id="704e7-143">NOTES</span></span>

## <span data-ttu-id="704e7-144">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="704e7-144">RELATED LINKS</span></span>

[<span data-ttu-id="704e7-145">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="704e7-145">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)

[<span data-ttu-id="704e7-146">New-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="704e7-146">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)

[<span data-ttu-id="704e7-147">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="704e7-147">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)
