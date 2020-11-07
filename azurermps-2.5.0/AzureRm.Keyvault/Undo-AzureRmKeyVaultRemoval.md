---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/undo-azurermkeyvaultremoval
schema: 2.0.0
ms.openlocfilehash: a557676d35eb167438f29c36a729ee652a45d591
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785747"
---
# <span data-ttu-id="51911-101">Undo-AzureRmKeyVaultRemoval</span><span class="sxs-lookup"><span data-stu-id="51911-101">Undo-AzureRmKeyVaultRemoval</span></span>

## <span data-ttu-id="51911-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="51911-102">SYNOPSIS</span></span>
<span data-ttu-id="51911-103">Recupera um cofre de chaves excluído para um estado ativo.</span><span class="sxs-lookup"><span data-stu-id="51911-103">Recovers a deleted key vault into an active state.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51911-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="51911-104">SYNTAX</span></span>

```
Undo-AzureRmKeyVaultRemoval [-VaultName] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51911-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="51911-105">DESCRIPTION</span></span>
<span data-ttu-id="51911-106">O cmdlet **Undo-AzureRmKeyVaultRemoval** recuperará um cofre de chaves previamente excluído.</span><span class="sxs-lookup"><span data-stu-id="51911-106">The **Undo-AzureRmKeyVaultRemoval** cmdlet will recover a previously deleted key vault.</span></span> <span data-ttu-id="51911-107">O cofre recuperado estará ativo após a recuperação</span><span class="sxs-lookup"><span data-stu-id="51911-107">The recovered vault will be active after recovery</span></span>

## <span data-ttu-id="51911-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="51911-108">EXAMPLES</span></span>

### <span data-ttu-id="51911-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="51911-109">Example 1</span></span>
```
PS C:\> Undo-AzureRmKeyVaultRemoval -VaultName 'MyKeyVault' -ResourceGroupName 'MyResourceGroup' -Location 'eastus2' -Tag @{"x"= "y"}
```

<span data-ttu-id="51911-110">Esse comando recuperará o cofre de chave ' MyKeyVault ' que foi excluído anteriormente da região eastus2 e do grupo de recursos ' MyResource Group ', em um estado ativo e utilizável.</span><span class="sxs-lookup"><span data-stu-id="51911-110">This command will recover the key vault 'MyKeyVault' that was previously deleted from eastus2 region and 'MyResourceGroup' resource group, into an active and usable state.</span></span> <span data-ttu-id="51911-111">Ele também substitui as marcas por nova marca.</span><span class="sxs-lookup"><span data-stu-id="51911-111">It also replaces the tags with new tag.</span></span>

## <span data-ttu-id="51911-112">OS</span><span class="sxs-lookup"><span data-stu-id="51911-112">PARAMETERS</span></span>

### <span data-ttu-id="51911-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51911-113">-DefaultProfile</span></span>
<span data-ttu-id="51911-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="51911-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="51911-115">-Local</span><span class="sxs-lookup"><span data-stu-id="51911-115">-Location</span></span>
<span data-ttu-id="51911-116">Especifica a região original do Azure do cofre excluído.</span><span class="sxs-lookup"><span data-stu-id="51911-116">Specifies the deleted vault original Azure region.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51911-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51911-117">-ResourceGroupName</span></span>
<span data-ttu-id="51911-118">Especifica o nome de um grupo de recursos existente no qual criar o cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="51911-118">Specifies the name of an existing resource group in which to create the key vault.</span></span>

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

### <span data-ttu-id="51911-119">-Marca</span><span class="sxs-lookup"><span data-stu-id="51911-119">-Tag</span></span>
<span data-ttu-id="51911-120">Pares de valores chave na forma de uma tabela de hash.</span><span class="sxs-lookup"><span data-stu-id="51911-120">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="51911-121">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="51911-121">For example:</span></span>

<span data-ttu-id="51911-122">@ {Key0 = "value0"; key1 = $null; Key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="51911-122">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="51911-123">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="51911-123">-VaultName</span></span>
<span data-ttu-id="51911-124">Nome do cofre.</span><span class="sxs-lookup"><span data-stu-id="51911-124">Vault name.</span></span>
<span data-ttu-id="51911-125">O cmdlet constrói o FQDN de um cofre com base no nome e no ambiente selecionado no momento.</span><span class="sxs-lookup"><span data-stu-id="51911-125">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="51911-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="51911-126">-Confirm</span></span>
<span data-ttu-id="51911-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51911-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51911-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51911-128">-WhatIf</span></span>
<span data-ttu-id="51911-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="51911-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="51911-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="51911-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51911-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51911-131">CommonParameters</span></span>
<span data-ttu-id="51911-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51911-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51911-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51911-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51911-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="51911-134">INPUTS</span></span>

### <span data-ttu-id="51911-135">System. String</span><span class="sxs-lookup"><span data-stu-id="51911-135">System.String</span></span>
<span data-ttu-id="51911-136">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="51911-136">System.Collections.Hashtable</span></span>

## <span data-ttu-id="51911-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="51911-137">OUTPUTS</span></span>

### <span data-ttu-id="51911-138">Microsoft. Azure. Commands. keyvault. Models. PSVault</span><span class="sxs-lookup"><span data-stu-id="51911-138">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

## <span data-ttu-id="51911-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="51911-139">NOTES</span></span>

## <span data-ttu-id="51911-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="51911-140">RELATED LINKS</span></span>

[<span data-ttu-id="51911-141">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="51911-141">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)

[<span data-ttu-id="51911-142">New-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="51911-142">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)

[<span data-ttu-id="51911-143">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="51911-143">Get-AzureRmKeyVault</span></span>](./Get-AzureRmKeyVault.md)
