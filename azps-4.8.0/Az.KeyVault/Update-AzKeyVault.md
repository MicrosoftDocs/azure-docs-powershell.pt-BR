---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
ms.openlocfilehash: 4302f2f9c4c2d6b2c7afa879fc28e2ff4edbb592
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111701"
---
# <span data-ttu-id="94df0-101">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="94df0-101">Update-AzKeyVault</span></span>

## <span data-ttu-id="94df0-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="94df0-102">SYNOPSIS</span></span>
<span data-ttu-id="94df0-103">Atualize o estado de um cofre de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="94df0-103">Update the state of an Azure key vault.</span></span>

## <span data-ttu-id="94df0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="94df0-104">SYNTAX</span></span>

### <span data-ttu-id="94df0-105">UpdateByNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="94df0-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzKeyVault -ResourceGroupName <String> -VaultName <String> [-EnableSoftDelete] [-EnablePurgeProtection]
 [-EnableRbacAuthorization <Boolean>] [-SoftDeleteRetentionInDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94df0-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="94df0-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzKeyVault -InputObject <PSKeyVault> [-EnableSoftDelete] [-EnablePurgeProtection]
 [-EnableRbacAuthorization <Boolean>] [-SoftDeleteRetentionInDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94df0-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="94df0-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzKeyVault -ResourceId <String> [-EnableSoftDelete] [-EnablePurgeProtection]
 [-EnableRbacAuthorization <Boolean>] [-SoftDeleteRetentionInDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94df0-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="94df0-108">DESCRIPTION</span></span>
<span data-ttu-id="94df0-109">Esse cmdlet atualiza o estado de um cofre de chaves do Azure.</span><span class="sxs-lookup"><span data-stu-id="94df0-109">This cmdlet updates the state of an Azure key vault.</span></span>
<span data-ttu-id="94df0-110">Observação a atualização de algumas das propriedades é uma ação irreversível, por exemplo, uma vez que a exclusão reversível foi habilitada, ela não pode mais ser desabilitada.</span><span class="sxs-lookup"><span data-stu-id="94df0-110">Please note updating some of the properties is an irreversible action, for example once soft delete has been enabled, it cannot be disabled anymore.</span></span>

## <span data-ttu-id="94df0-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="94df0-111">EXAMPLES</span></span>

### <span data-ttu-id="94df0-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="94df0-112">Example 1</span></span>
```powershell
PS C:\> Update-AzKeyVault -VaultName $keyVaultName -ResourceGroupName $resourceGroupName -EnableSoftDelete
```

<span data-ttu-id="94df0-113">Permite a exclusão reversível no cofre de chaves nomeado `$keyVaultName` no grupo de recursos `$resourceGroupName` .</span><span class="sxs-lookup"><span data-stu-id="94df0-113">Enables soft delete on the key vault named `$keyVaultName` in resource group `$resourceGroupName`.</span></span>

### <span data-ttu-id="94df0-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="94df0-114">Example 1</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName -ResourceGroupName $resourceGroupName | Update-AzKeyVault -EnablePurgeProtection
```

<span data-ttu-id="94df0-115">Habilita a proteção de limpeza usando a sintaxe de tubulação.</span><span class="sxs-lookup"><span data-stu-id="94df0-115">Enables purge protection using piping syntax.</span></span>

## <span data-ttu-id="94df0-116">OS</span><span class="sxs-lookup"><span data-stu-id="94df0-116">PARAMETERS</span></span>

### <span data-ttu-id="94df0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94df0-117">-DefaultProfile</span></span>
<span data-ttu-id="94df0-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="94df0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94df0-119">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="94df0-119">-EnablePurgeProtection</span></span>
<span data-ttu-id="94df0-120">Habilite a funcionalidade de proteção de limpeza para este cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="94df0-120">Enable the purge protection functionality for this key vault.</span></span>
<span data-ttu-id="94df0-121">Uma vez habilitado, ele não pode ser desabilitado.</span><span class="sxs-lookup"><span data-stu-id="94df0-121">Once enabled it cannot be disabled.</span></span>
<span data-ttu-id="94df0-122">Requer que o soft-Delete esteja ativado.</span><span class="sxs-lookup"><span data-stu-id="94df0-122">It requires soft-delete to be turned on.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94df0-123">-EnableRbacAuthorization</span><span class="sxs-lookup"><span data-stu-id="94df0-123">-EnableRbacAuthorization</span></span>
<span data-ttu-id="94df0-124">Habilite ou desabilite este cofre de chaves para autorizar ações de dados pelo controle de acesso baseado em função (RBAC).</span><span class="sxs-lookup"><span data-stu-id="94df0-124">Enable or disable this key vault to authorize data actions by Role Based Access Control (RBAC).</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94df0-125">-EnableSoftDelete</span><span class="sxs-lookup"><span data-stu-id="94df0-125">-EnableSoftDelete</span></span>
<span data-ttu-id="94df0-126">Habilite a funcionalidade de exclusão suave para este cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="94df0-126">Enable the soft-delete functionality for this key vault.</span></span>
<span data-ttu-id="94df0-127">Uma vez habilitado, ele não pode ser desabilitado.</span><span class="sxs-lookup"><span data-stu-id="94df0-127">Once enabled it cannot be disabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94df0-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="94df0-128">-InputObject</span></span>
<span data-ttu-id="94df0-129">Objeto do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="94df0-129">Key vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94df0-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94df0-130">-ResourceGroupName</span></span>
<span data-ttu-id="94df0-131">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="94df0-131">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94df0-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="94df0-132">-ResourceId</span></span>
<span data-ttu-id="94df0-133">ID do recurso do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="94df0-133">Resource ID of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94df0-134">-SoftDeleteRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="94df0-134">-SoftDeleteRetentionInDays</span></span>
<span data-ttu-id="94df0-135">Especifica por quanto tempo os recursos excluídos são mantidos e quanto tempo até um cofre ou um objeto no estado excluído pode ser limpo.</span><span class="sxs-lookup"><span data-stu-id="94df0-135">Specifies how long deleted resources are retained, and how long until a vault or an object in the deleted state can be purged.</span></span> <span data-ttu-id="94df0-136">O padrão é 90 dias.</span><span class="sxs-lookup"><span data-stu-id="94df0-136">The default is 90 days.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94df0-137">-Cofrename</span><span class="sxs-lookup"><span data-stu-id="94df0-137">-VaultName</span></span>
<span data-ttu-id="94df0-138">Nome do cofre de chaves.</span><span class="sxs-lookup"><span data-stu-id="94df0-138">Name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94df0-139">-Confirme</span><span class="sxs-lookup"><span data-stu-id="94df0-139">-Confirm</span></span>
<span data-ttu-id="94df0-140">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="94df0-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94df0-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94df0-141">-WhatIf</span></span>
<span data-ttu-id="94df0-142">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="94df0-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94df0-143">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="94df0-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94df0-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94df0-144">CommonParameters</span></span>
<span data-ttu-id="94df0-145">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94df0-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94df0-146">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="94df0-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94df0-147">SENSORES</span><span class="sxs-lookup"><span data-stu-id="94df0-147">INPUTS</span></span>

### <span data-ttu-id="94df0-148">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="94df0-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="94df0-149">System. String</span><span class="sxs-lookup"><span data-stu-id="94df0-149">System.String</span></span>

## <span data-ttu-id="94df0-150">EXIBE</span><span class="sxs-lookup"><span data-stu-id="94df0-150">OUTPUTS</span></span>

### <span data-ttu-id="94df0-151">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="94df0-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="94df0-152">INFORMA</span><span class="sxs-lookup"><span data-stu-id="94df0-152">NOTES</span></span>

## <span data-ttu-id="94df0-153">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="94df0-153">RELATED LINKS</span></span>
