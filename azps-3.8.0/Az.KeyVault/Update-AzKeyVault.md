---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
ms.openlocfilehash: 8932402fb9e4e6b27f284313bfddc764192c5e93
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93777735"
---
# <span data-ttu-id="43d75-101">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="43d75-101">Update-AzKeyVault</span></span>

## <span data-ttu-id="43d75-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="43d75-102">SYNOPSIS</span></span>
<span data-ttu-id="43d75-103">Atualize o estado de um cofre de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="43d75-103">Update the state of an Azure key vault.</span></span>

## <span data-ttu-id="43d75-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="43d75-104">SYNTAX</span></span>

### <span data-ttu-id="43d75-105">UpdateByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="43d75-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzKeyVault -ResourceGroupName <String> -VaultName <String> [-EnableSoftDelete] [-EnablePurgeProtection]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43d75-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="43d75-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzKeyVault -InputObject <PSKeyVault> [-EnableSoftDelete] [-EnablePurgeProtection]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="43d75-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="43d75-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzKeyVault -ResourceId <String> [-EnableSoftDelete] [-EnablePurgeProtection]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="43d75-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="43d75-108">DESCRIPTION</span></span>
<span data-ttu-id="43d75-109">Esse cmdlet atualiza o estado de um cofre de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="43d75-109">This cmdlet updates the state of an Azure key vault.</span></span>
<span data-ttu-id="43d75-110">Observação a atualização de algumas das propriedades é uma ação irreversível, por exemplo, uma vez que a exclusão reversível foi habilitada, ela não pode mais ser desabilitada.</span><span class="sxs-lookup"><span data-stu-id="43d75-110">Please note updating some of the properties is an irreversible action, for example once soft delete has been enabled, it cannot be disabled anymore.</span></span>

## <span data-ttu-id="43d75-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="43d75-111">EXAMPLES</span></span>

### <span data-ttu-id="43d75-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="43d75-112">Example 1</span></span>
```powershell
PS C:\> Update-AzKeyVault -VaultName $keyVaultName -ResourceGroupName $resourceGroupName -EnableSoftDelete
```

<span data-ttu-id="43d75-113">Permite a exclusão reversível no cofre de chaves nomeado `$keyVaultName` no grupo de recursos `$resourceGroupName` .</span><span class="sxs-lookup"><span data-stu-id="43d75-113">Enables soft delete on the key vault named `$keyVaultName` in resource group `$resourceGroupName`.</span></span>

### <span data-ttu-id="43d75-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="43d75-114">Example 1</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName -ResourceGroupName $resourceGroupName | Update-AzKeyVault -EnablePurgeProtection
```

<span data-ttu-id="43d75-115">Habilita a proteção de limpeza usando a sintaxe de tubulação.</span><span class="sxs-lookup"><span data-stu-id="43d75-115">Enables purge protection using piping syntax.</span></span>

## <span data-ttu-id="43d75-116">OS</span><span class="sxs-lookup"><span data-stu-id="43d75-116">PARAMETERS</span></span>

### <span data-ttu-id="43d75-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43d75-117">-DefaultProfile</span></span>
<span data-ttu-id="43d75-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="43d75-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43d75-119">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="43d75-119">-EnablePurgeProtection</span></span>
<span data-ttu-id="43d75-120">Habilite a funcionalidade de proteção de limpeza para este cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="43d75-120">Enable the purge protection functionality for this key vault.</span></span>
<span data-ttu-id="43d75-121">Uma vez habilitado, ele não pode ser desabilitado.</span><span class="sxs-lookup"><span data-stu-id="43d75-121">Once enabled it cannot be disabled.</span></span>
<span data-ttu-id="43d75-122">Requer que o soft-Delete esteja ativado.</span><span class="sxs-lookup"><span data-stu-id="43d75-122">It requires soft-delete to be turned on.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43d75-123">-EnableSoftDelete</span><span class="sxs-lookup"><span data-stu-id="43d75-123">-EnableSoftDelete</span></span>
<span data-ttu-id="43d75-124">Habilite a funcionalidade de exclusão suave para este cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="43d75-124">Enable the soft-delete functionality for this key vault.</span></span>
<span data-ttu-id="43d75-125">Uma vez habilitado, ele não pode ser desabilitado.</span><span class="sxs-lookup"><span data-stu-id="43d75-125">Once enabled it cannot be disabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43d75-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="43d75-126">-InputObject</span></span>
<span data-ttu-id="43d75-127">Objeto do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="43d75-127">Key vault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="43d75-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43d75-128">-ResourceGroupName</span></span>
<span data-ttu-id="43d75-129">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="43d75-129">Name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43d75-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="43d75-130">-ResourceId</span></span>
<span data-ttu-id="43d75-131">ID do recurso do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="43d75-131">Resource ID of the key vault.</span></span>

```yaml
Type: String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43d75-132">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="43d75-132">-VaultName</span></span>
<span data-ttu-id="43d75-133">Nome do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="43d75-133">Name of the key vault.</span></span>

```yaml
Type: String
Parameter Sets: UpdateByNameParameterSet
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="43d75-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="43d75-134">-Confirm</span></span>
<span data-ttu-id="43d75-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43d75-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43d75-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43d75-136">-WhatIf</span></span>
<span data-ttu-id="43d75-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="43d75-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43d75-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="43d75-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43d75-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43d75-139">CommonParameters</span></span>
<span data-ttu-id="43d75-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43d75-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43d75-141">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="43d75-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43d75-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="43d75-142">INPUTS</span></span>

### <span data-ttu-id="43d75-143">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="43d75-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="43d75-144">System. String</span><span class="sxs-lookup"><span data-stu-id="43d75-144">System.String</span></span>

## <span data-ttu-id="43d75-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="43d75-145">OUTPUTS</span></span>

### <span data-ttu-id="43d75-146">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="43d75-146">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="43d75-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="43d75-147">NOTES</span></span>

## <span data-ttu-id="43d75-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="43d75-148">RELATED LINKS</span></span>
